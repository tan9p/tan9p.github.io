---
title: 分成两个函数证明不等式
layout: post
tags: 导数 不等式
categories: 初等数学
---

# 证明：$\ln x\leq x^2\mathrm{e}^x-1(x>0)$
采用分成两个函数的方法，要$\mathrm{e}^x$项有最小值，想到需给它除掉一个东西，等价于证明$$\frac{\ln x + 1}{x^3}\leq\frac{\mathrm{e}^x}{x}.$$
令$f(x)=\frac{\ln x + 1}{x^3},g(x)=\frac{\mathrm{e}^x}{x}$.
对$f(x)$，$f'(x)=\frac{-3\ln x-2}{x^4}$，所以$f_max(x)=f(\mathrm{e}^{-\frac{2}{3}})=\frac{\mathrm{e}^2}{3}$.
对$g(x)$，$g'(x)=\frac{\mathrm{e}^x(x-1)}{x^2}$，所以$g_min(x)=g(1)=\mathrm{e}$.
所以$\frac{\ln x + 1}{x^3}\leq\mathrm{e}<\frac{\mathrm{e}^2}{3}\leq\frac{\mathrm{e}^x}{x}$.
