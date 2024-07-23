---
title: 数学归纳法在代数中的应用
layout: post
tags: 代数 数学归纳法
categories: 数学竞赛
---

时间：2024-7-22

# 1
设$x_i>0,y_i>0(1\leq i\leq n)$，$n>1$，且$\sum\limits_{i=1}^n x_i = \sum\limits_{i=1}^n y_i=\pi$，求证

$$
\sum\limits_{i=1}^n\frac{\cos y_i}{\sin x_i}\leq\sum\limits_{i=1}^n\cot x_i.
$$

**从简单出发**

$n=2$时，条件：$x_1+x_2=y_1+y_2=\pi$，要证：$\frac{\cos y_1}{\sin x_1}+\frac{\cos y_2}{\sin x_2}\leq\cot x_1+\cot x_2$  
$LHS=0=RHS$，得证.

$n=3$时，条件$x_1+x_2+x_3=y_1+y_2+y_3=\pi$（联想三角形）  
要证：$\frac{\cos y_1}{\sin x_1}+\frac{\cos y_2}{\sin x_2}+\frac{\cos y_3}{\sin x_3}\leq\cot x_1+\cot x_2+\cot x_3$.  
关于$\cot x_1+\cot x_2+\cot x_3$的结论：  
在$\triangle ABC$中，$\cot x_1+\cot x_2+\cot x_3=\sum\frac{\cos x_i}{\sin x_i}=\sum\frac{\frac{a^2+b^2-c^2}{2ab}}{\sin x_i}=\sum\frac{a^2+b^2-c^2}{2ab\sin x_1}=\frac{a^2+b^2+c^2}{4S}$.  
即证：$\frac{\cos y_1}{\sin x_1}+\frac{\cos y_2}{\sin x_2}+\frac{\cos y_3}{\sin x_3}\leq\frac{a^2+b^2+c^2}{4S}\Leftrightarrow\frac{\cos y_1}{\frac{\sin x_1}{4S}}+\frac{\cos y_2}{\frac{\sin x_2}{4S}}+\frac{\cos y_3}{\frac{\sin x_3}{4S}}\leq a^2+b^2+c^2$  
等价于证：$2ab\cos y_1+2bc\cos y_2+2ca\cos y_3\leq a^2+b^2+c^2$.  
这就是[嵌入不等式](#%E5%B5%8C%E5%85%A5%E4%B8%8D%E7%AD%89%E5%BC%8F)

$n=4$时，条件$x_1+x_2+x_3+x_4=y_1+y_2+y_3+y_4=\pi$，  
要证：$\sum\frac{\cos y_i}{\sin x_i}\leq\sum\cot x_i$  
想利用$n=3$时的结论，可以考虑合并$x_3+x_4$和$y_3+y_4$，利用$n=3$的结论，有  
$\frac{\cos y_1}{\sin x_1}+\frac{\cos y_2}{\sin x_2}+\frac{\cos (y_3+y_4)}{\sin (x_3+x_4)}\leq\cot x_1+\cot x_2+\cot(x_3+x_4)$  
只需证：  
$\frac{\cos y_3}{\sin x_3}+\frac{\cos y_4}{\sin x_4}-\frac{\cos (y_3+y_4)}{\sin (x_3+x_4)}\leq\cot x_3+\cot x_4-\cot(x_3+x_4)$.**（待证-已证=需证，不变号）**  
利用诱导公式，等价于证：$\frac{\cos y_3}{\sin x_3}+\frac{\cos y_4}{\sin x_4}+\frac{\cos (\pi-(y_3+y_4))}{\sin (\pi-(x_3+x_4))}\leq\cot x_3+\cot x_4+\cot(\pi-(x_3+x_4))$，这就又是$n=3$时证明过的结论.  
以后的$n$，都可以用同样的方法，将其转化为$n-1$的情形和$n=3$的情形，可以用数学归纳法证明.

<span style="color: lightblue;">总结：什么样的题目适合数学归纳法？
形如$\sum f(x_i) \geq(\leq)\sum g(x_i)$的题目
可以两项看作一项，达到递推的目的.</span>

# 2
设$a,b,c>0$，且一元二次方程$ax^2+bx+c=0$有两个不相等的实数根.数列$\{a_n\},\{b_n\}$满足
$$b_0=ca_0>0,b_1=ca_1-ba_0>0,b_n=aa_{n-2}-ba_{n-1}+ca_n,n\geq 2.$$
若$b_n>0$,则是否有$a_n>0$，并证明你的结论.

解：是.
有两个不等的实根，$\Delta=b^2-4ac>0$，即$\frac{ac}{b^2}<\frac{1}{4}$.
$b_0=ca_0>0$，所以$a_0>0$；
$b_1=ca_1-ba_0>0$，所以$ca_1>ba_0>0$，所以$a_1>0$；
有$a_0<\frac{c}{b}a_1$；
$b_2=aa_0-ba_1+ca_2>0$，
所以$ca_2>ba_1-aa_0>ba_1-a(\frac{c}{b}a_1)=ba_1(1-\frac{ac}{b^2})>\frac{3}{4}ba_1>0$.
有$a_1<\frac{4}{3}\frac{c}{b}a_2$；
$b_3=aa_1-ba_2+ca_3>0$，
所以$ca_3>ba_2-aa_1>ba_2-a\frac{4c}{3b}a_2=ba_2(1-\frac{4ac}{3b^2})>\frac{2}{3}ba_2>0$
$a_2<\frac{3c}{2b}a_3$
$b_4=aa_2-ba_3+ca_4>0$，$ca_4>ba_3-aa_2>ba_3-a\frac{3c}{2b}a_3=ba_3(1-\frac{3ac}{2b^2})>\frac{5}{8}ba_2>0$
归纳猜想：$ca_n>\frac{n+1}{2n}ba_{n-1}$.
上式对$n=2$成立.
假设上式对$n$成立，下证其对$n+1$成立.
$b_{n+1}=aa_{n-1}-ba_n+ca_{n+1}>0$
所以$ca_{n+1}>ba_n-aa_{n-1}>ba_n-a\frac{2n}{n+1}\cdot\frac{c}{b}a_n=ba_n(1-\frac{2n}{n+1}\cdot\frac{ac}{b^2})>ba_n(1-\frac{2n}{n+1}\cdot\frac{1}{4})=\frac{n+2}{2(n+1)}ba_n$.

# 3
设实数$a_1\leq a_2\leq\cdots\leq a_n$，满足$a_1+2a_2+\cdots+na_n=0$.证明：对任意实数$x$，有
$$a_1[x]+a_2[2x]+\cdots+a_n[nx]\geq 0.$$

几个取整函数的性质：
(1) $x-1<[x]\leq x$
(2) $[x+y]-1<[x]+[y]\leq[x+y]$

$n=1$时，$a_1=0$，$a_1[x]=0\geq 0$；
$n=2$时，$a_1\leq a_2,a_1+2a_2=0$，得$a_2\geq 0$.
证$a_1[x]+a_2[2x]\geq 0$，换掉$a_1$，即证：
$-2a_2[x]+a_2[2x]=a_2([2x]-2[x])\geq 0$.
因$[2x]-2[x]\geq0,a_2\geq0$成立.
$n=3$时，换$a_1$的方法不再成立；换$a_2$可以解决$n=3$，但推广不到$n=4$以后.
思考：该如何将$n=3$的情况划归成$n=2$的情况？
把$a_3$分给$a_1,a_2$：$a_1+2a_2+3a_3=(a_1+xa_3)+2(a_2+xa_3)$，解得$x=1$，即$(a_1+a_3)+2(a_2+a_3)=0$，由已证，得：
$(a_1+a_3)[x]+(a_2+a_3)[2x]\geq 0$.
待证：$a_1[x]+a_2[2x]+a_3[3x]\geq 0$
只需证：$a_3[3x]-a_3[2x]-a_3[x]\geq 0$.
由$a_3\geq 0,[3x]-[2x]-[x]\geq 0$，得证.
下面用归纳法：
$n=1,2$，成立；
假设对$n$成立，考虑$n+1$的情况.
条件$a_1+2a_2+\cdot+na_n+(n+1)a_{n+1}=0$
变成$n$的情形：$(a_1+xa_{n+1})+2(a_2+xa_{n+1})+\cdots+n(a_n+xa_{n+1})=a_1+2a_2+\cdots+na_n+\frac{n(n+1)}{2}\cdot xa_{n+1}$，所以$x=\frac{2}{n}$.
待证：$a_1[x]+a_2[2x]+\cdots+a_n[nx]+a_{n+1}[(n+1)x]\geq 0$
已证：$(a_1+\frac{2}{n}a_{n+1})[x]+(a_2++\frac{2}{n}a_{n+1})[2x]+\cdots+(a_n++\frac{2}{n}a_{n+1})[nx]\geq 0$
需证：$a_{n+1}[(n+1)x]-\frac{2a_{n+1}}{n}([x]+[2x]+\cdots+[nx])\geq 0$.
只需证$a_{n+1}[(n+1)x]\geq\frac{2a_{n+1}}{n}([x]+[2x]+\cdots+[nx])$，
易证：$a_{n+1}\geq 0$，只需证：$n[(n+1)x]\geq2([x]+[2x]+\cdots+[nx])$，
由倒叙相加：$[x]+[nx]\geq[(n+1)x],\cdots,[nx]+[x]\geq[(n+1)x]$可得.

变式：
1. 把$a_i$看成是$x_i-y_i$，条件就变成$x_1\leq x_2\leq\cdots \leq x_n$，$y_1\geq y_2\geq\cdots\geq y_n$，且$\sum\limits_{i=1}^n ix_i=\sum\limits_{i=1}^n iy_i$,证明：对任意的$x\in \mathbb{R}$，有
$$\sum\limits_{i=1}^n x_i[ix]\geq\sum\limits_{i=1}^n y_i[ix]$$
2. 取$a_1=-1,a_2=-\frac{1}{2},\cdots,a_{n-1}=-\frac{1}{n-1},a_n=\frac{n-1}{n}$.
上述结论即为$-[x]-\frac{[2x]}{2}-\cdots-\frac{[(n-1)x]}{n-1}+\frac{n-1}{n}[nx]\geq 0$，即
$[x]+\frac{[2x]}{2}+\cdots+\frac{[nx]}{n}\leq[nx]$.

# 嵌入不等式
$\triangle ABC$的三个内角分别为$A,B,C$，则对任意的实数$x,y,z$满足：$x^2+y^2+z^2-2yz\cos A-2zx\cos B-2xy\cos C\geq 0$.
证明方法：
求最值的题目.


# 离散傅里叶变换(Discrete Fourier Transform)
设$\omega$是$n$次本原单位根，$\omega=\mathrm{e}^{\frac{2\pi i}{n}}$,
若$x_1,x_2,\cdots,x_n\in \mathbb{R}$，定义变换：$y_j=\frac{1}{\sqrt{n}}\sum\limits_{k=1}^n x_k\omega^{-kj}$.
该变换有以下性质：
1. $x_j=\frac{1}{\sqrt{n}}\sum\limits_{k=1}^n y_k\omega^{kj}$
2. $\sum\limits_{k=1}^n x_kx_{k+t}=\sum\limits_{k=1}^n(y_k)^2\cos\frac{2k\pi t}{n}$，$t=0,1,2,\cdots,n$，下标$(k+t)$取除$n$的余数.

# 樊畿不等式(Ky-fan inequality)
离散情形：
设$x_1,x_2,\cdots,x_n$且$x_1+x_2+\cdots+x_n=0$，则有$(\sum\limits_{i=1}^n x_i^2)\cos\frac{2\pi}{n}\geq x_1x_2+x_2x_3+\cdots+x_{n-1}x_n+x_nx_1$.
当且仅当：$x_k=a\cos\frac{2k\pi}{n}+b\sin\frac{2k\pi}{n}$时取等.