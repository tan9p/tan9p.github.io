---
title: 双曲函数探秘
layout: post
tags: 函数 三角函数
categories: 初等数学
---

在学习函数奇偶性时，我们会遇到诸如$f(x)=a^x+a^{-x}$和$g(x)=a^x-a^{-x}$这样的函数奇偶性判断问题，这样的函数结构，和双曲正余弦函数有关，什么是双曲正余弦函数？为什么这样命名，它们有何性质？在各类考试题中是如何考查的？下面我们就来探究一下.

## 双曲正余弦函数的获得
如果将$\mathrm{e}^x$写成一个奇函数$f(x)$和一个偶函数$g(x)$的和：$\mathrm{e}^x=f(x)+g(x)$，利用奇偶性的定义，可得：$\mathrm{e}^{-x}=f(-x)+g(-x)=-f(x)+g(x)$，解方程得：$f(x)=\frac{\mathrm{e}^x-\mathrm{e}^{-x}}{2}$，$g(x)=\frac{\mathrm{e}^x+\mathrm{e}^{-x}}{2}$.
把$f(x)$称为双曲正弦函数，记作$\sinh x=\frac{\mathrm{e}^x-\mathrm{e}^{-x}}{2}$;
把$g(x)$称为双曲余弦函数，记作$\cosh x=\frac{\mathrm{e}^x+\mathrm{e}^{-x}}{2}$.
## 双曲正余弦函数名称的由来
这两个函数为何有这样的名称？双曲体现在哪？正余弦又体现在哪？
利用完全平方公式，容易验证如下恒等式：$\cosh^2 x-\sinh^2 x=(\frac{\mathrm{e}^x+\mathrm{e}^{-x}}{2})^2-(\frac{\mathrm{e}^x-\mathrm{e}^{-x}}{2})^2=1$
这表明当$t$变动时，动点$P(\cosh t,\sinh t)$在**单位双曲线**$X^2-Y^2=1$上，这就是名称中"双曲"的来源.
类比$P(\cos\theta,\sin\theta)$在单位圆$X^2+Y^2=1$上，我们将$\cosh x$称为**双曲余弦函数**，$\sinh x$称为**双曲正弦函数**.
不像$\theta$在单位圆中有明确的几何意义（$OP$和$x$轴正半轴所成的角），$t$的几何意义不太明确和直接.可以推出，记$OP$和$x$轴正半轴所成的角为$\theta$，则$\tan \theta=\frac{\sinh t}{\cosh t}$.
仿照正切函数的定义，我们可以把**双曲正切函数**定义为$\tanh x=\frac{\sinh x}{\cosh x}=\frac{\mathrm{e}^x-\mathrm{e}^{-x}}{\mathrm{e}^x+\mathrm{e}^{-x}}=\frac{\mathrm{e}^{2x}-1}{\mathrm{e}^{2x}+1}$.
这样就有$\tan \theta=\tanh t$.
## 双曲函数的图象和性质
借助计算机作图工具或函数的性质讨论，可以得到上述三个双曲函数的图象和性质：
这里有一个表格.

|        | 双曲正弦函数                                                 | 双曲余弦函数                                                 | 双曲正切函数                                                 |
| ------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 解析式 | $\sinh x=\frac{\mathrm{e}^x-\mathrm{e}^{-x}}{2}$             | $\cosh x=\frac{\mathrm{e}^x+\mathrm{e}^{-x}}{2}$             | $\tanh x=\frac{\mathrm{e}^{2x}-1}{\mathrm{e}^{2x}+1}$        |
| 图象   | ![image-20260915152855769](https://raw.giteeusercontent.com/tan9p/picstorage/raw/master/2026-9-19/image-20260915152855769.png){: style="width: 300%; max-width: 30%;"} | ![image-20260915152949550](https://raw.giteeusercontent.com/tan9p/picstorage/raw/master/2026-9-19/image-20260915152949550.png){: style="width: 300%; max-width: 30%;"}| ![image-20260915153058734](https://raw.giteeusercontent.com/tan9p/picstorage/raw/master/2026-9-19/image-20260915153058734.png){: style="width: 300%; max-width: 30%;"} |
| 值域   | $R$                                                          | $[1,+\infty)$                                                | $(-1,1)$                                                     |
| 奇偶性 | 奇函数                                                       | 偶函数                                                       | 奇函数                                                       |
| 单调性 | $R$上单增                                                    | $(-\infty,0]$上单减，$[0,+\infty)$上单增                     | $R$上单增                                                    |



## 双曲函数的和、差、二倍角公式（与三角函数的对比）

| 三角函数                                                  | 双曲函数                                                     |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| $\sin^2 x+\cos^2 x=1$                                     | $\cosh^2 x-\sinh^2 x=1$                                      |
| $\cos(x\pm y)=\cos x\cos y\mp\sin x \sin y$               | $\cosh(x\pm y)=\cosh x\cosh y\pm\sinh x\sinh y$              |
| $\sin(x\pm y)=\sin x\cos y\pm \cos x\sin y$               | $\sinh(x\pm y)=\sinh x\cosh y\pm \cosh x\sinh y$             |
| $\tan(x\pm y)=\frac{\tan x\pm \tan y}{1\mp \tan x\tan y}$ | $\tanh(x\pm y)=\frac{\tanh x\pm \tanh y}{1\pm \tanh x\tanh y}$ |
| $\sin 2x=2\sin x\cos x$                                   | $\sinh 2x=2\sinh x\cosh x$                                   |
| $\cos 2x=\cos^2x-\sin^2x=2\cos^2x-1=1-2\sin^2x$           | $\cosh 2x=\cosh^2 x+\sinh^2x=2\cosh^2x-1=1+2\sinh^2 x$       |
| $\tan 2x=\frac{2\tan x}{1-\tan^2 x}$                      | $\tanh 2x =\frac{2\tanh x}{1+\tanh^2 x}$                     |

可以发现，双曲函数的公式和三角函数非常相似，部分公式只有正负号的差别，更进一步，双曲函数也会有和差化积公式和积化和差公式.
## 双曲函数的导数公式
容易验证：$(\sinh x)'=\cosh x$，$(\cosh x)'=\sinh x$，$(\tanh x)'=(\frac{\sinh x}{\cosh x})'=\frac{\cosh^2 x-\sinh^2 x}{\cosh^2x}=\frac{1}{\cosh^2 x}$,也非常接近于三角函数.

## 为何双曲函数与三角函数的公式如此接近？
一种看法是Taylor级数的视角：
$\mathrm{e}^x=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\frac{x^4}{4!}+\cdots$
$\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots$
$\cos x=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\cdots$
$\sinh x = x+\frac{x^3}{3!}+\frac{x^5}{5!}+\cdots$
$\cosh x=1+\frac{x^2}{2!}+\frac{x^4}{4!}+\cdots$
引入虚数单位$i$，可以发现$\mathrm{e}^{ix}=\cos x+i\sin x$
而$\mathrm{e}^x=\cosh x+\sinh x$
可以认为$\cosh x=\cos(ix)$，$\sinh x =-i\sin(ix)$或者$\cos x=\cosh(ix)$，$\sin x=-i\sinh(ix)$.
于是，大部分公式的结构是不变的，只有在在涉及到$\sin x\sin y$和$\sinh x\sinh y$的结构时，两者会差一个负号.

## 双曲函数在考题中的应用
教材中的题目（人教A版160页，复习参考题4，第6题）：
![image-20260915105447024](https://raw.giteeusercontent.com/tan9p/picstorage/raw/master/2026-9-19/image-20260915105447024.png)

正好是前面介绍的公式，通过直接带入计算，很容易得出结果.

2025年八省高考综合改革适应性演练T10
在人工神经网络中，单个神经元输入与输出的函数关系可以称为激励函数.双曲正切函数是一种激励函数.定义双曲正弦函数$\sinh x=\frac{\mathrm{e}^x-\mathrm{e}^{-x}}{2}$，双曲余弦函数$\cosh x=\frac{\mathrm{e}^x+\mathrm{e}^{-x}}{2}$，双曲正切函数$\tanh x=\frac{\sinh x}{\cosh x}$.则
A. 双曲正弦函数是增函数
B. 双曲余弦函数是增函数
C. 双曲正切函数是增函数
D. $\tanh(x+y)=\frac{\tanh x+\tanh y}{1+\tanh x\tanh y}$

前三个选项直接考查双曲函数的单调性，选项D考查双曲正切的和公式.

2026年新高考全国2卷T19(3)
已知$f(x)=x\mathrm{e}^x-3x+1$，当$x>0$时，$f(k+x)+f(k-x)>2f(k)$，求$k$的取值范围.

带入化简得：$(k+x)\mathrm{e}^{k+x}+(k-x)\mathrm{e}^{k-x}>2k\mathrm{e}^k$，约去$\mathrm{e}^k$得：$k\mathrm{e}^{x}+x\mathrm{e}^{x}+k\mathrm{e}^{-x}-x\mathrm{e}^{-x}>2k$；

整理成双曲函数得形式得：$k\cosh x+x\sinh x>k$；

分离参数，因为$x>0$时$\cosh x>1$，所以$k>\frac{-x\sinh x}{\cosh x-1}$.

令$g(x)=\frac{-x\sinh x}{\cosh x-1}$，只需求$g(x)$的最大值.

$g'(x)=\frac{(-\sinh x-x\cosh x)(\cosh x-1)+x\sinh^2 x}{(\cosh x-1)^2}=\frac{x-\sinh x}{\cosh x -1}$，

令$h(x)=x-\sinh x$，$h'(x)=1-\cosh x<0$，所以$h(x)$单调递减，于是$x>0$时，$h(x)<h(0)=0$，即$g'(x)<0$，所以$g(x)$单调递减，但是$g(0)$无定义，用洛必达法则，得$g(x)<\displaystyle\lim_{x\rightarrow 0}g(x)=\displaystyle\lim_{x\rightarrow 0}\frac{-x\sinh x}{\cosh x-1}=\displaystyle\lim_{x\rightarrow 0}\frac{-\sinh x-x\cosh x}{\sinh x}=\displaystyle\lim_{x\rightarrow 0}\frac{-2\cosh x-x\sinh x}{\cosh x}=-2$，

所以$k\geq -2$.

2017全国中学生数学联赛一试T11(1)
设复数$z_{1}，z_{2}$满足$\mathrm{Re}(z_{1})>0,\mathrm{Re}(z_{2})>0$，$\mathrm{Re}(z_{1}^2)=\mathrm{Re}(z_{2}^2)=2$.求$\mathrm{Re}(z_{1}z_{2})$的最小值.
设$z_{i}=x_{i}+\mathrm{i}y_{i}$，有$x_{i}>0,x_{i}^2-y_{i}^2=2$，求$x_{1}x_{2}-y_{1}y_{2}$的最小值.
令$x_{i}=\sqrt{2}\cosh t_{i},y_{i}=\sqrt{ 2 }\sinh t_{i}$，$x_{1}x_{2}-y_{1}y_{2}=2\cosh t_{1}\cosh t_{2}-2\sinh t_{1}\sinh t_{2}=2\cosh(t_{1}-t_{2})\geq 2$.

## 双曲正弦与双曲正切函数的反函数

根据前面函数性质的分析，$y=\sinh x$是单调递增函数，因此是1-1对应的，存在反函数.反解$y=\frac{\mathrm{e}^x-\mathrm{e}^{-x}}{2}$，得到$\mathrm{e}^{2x}-2y\mathrm{e}^x-1=0$，解得$\mathrm{e}^x=y\pm\sqrt{y^2+1}$，因为$\mathrm{e}^x>0$，所以$x=\ln(y+\sqrt{y^2+1})$，反函数为$y=\ln(x+\sqrt{x^2+1})$，也是奇偶性判断里的常见函数.

$y=\tanh x$也是单调递增函数，也存在反函数，反解$y=\frac{\mathrm{e}^{2x}-1}{\mathrm{e}^{2x}+1}$，得到$y\mathrm{e}^{2x}+y=\mathrm{e}^{2x}-1$，$\mathrm{e}^{2x}=\frac{1+y}{1-y}$，$x=\frac{1}{2}\ln\frac{1+y}{1-y}$，反函数为$y=\frac{1}{2}\ln\frac{1+x}{1-x}$.也是奇偶性判断里的常见函数.
