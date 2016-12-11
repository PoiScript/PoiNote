#不定积分
##I. 不定积分的概念与性质
###i. 原函数与不定积分的概念
####1. 定义1:
若在区间 $I$ 上定义的两个函数  $F(x)$ 及 $f(x)$ 满足
\[F'(x)=f(x)或dF(x)=f(x)dx\]
则称 $F(x)$ 为 $f(x)$ 在区间 $I$ 上的一个 **原函数**.
####2. 原函数存在定理
如果函数 $f(x)$ 在区间 $I$ 上连续, 那么在区间 $I$ 上存在可导函数 $F(x)$, 使任一 $x\in I$ 都有
\[F'(x)=f(x)\]
简单来说就是, 连续函数一定有原函数
####3. 定义2
$f(x)$ 在区间 $I$ 上的原函数全体称为 $f(x)$ 在 $I$ 上的不定积分, 记作
\[\int f(x)dx\]
**其中**:
1. $f(x)$— 被积函数;

1. $\int$— 积分号;
1. $f(x)dx$— 被积表达式.
1. $x$— 积分变量;

若 $F'(x)=f(x)$, 则
\[\int f(x)dx=F(x)+C\quad(C为任意常数)\]
$C$ 称为积分常数

从不定积分定义可知:
1. $\displaystyle\frac d{dx}[\int f(x)dx]=f(x)$ 或 $\displaystyle d[\int f(x)dx]=f(x)dx$

1. $\displaystyle\int F'(x)dx=F(x)+C$ 或 $\displaystyle\int dF(x)=F(x)+C$
###ii.基本积分表
\[\begin{array}{ll}
1.\int kdx=kx+C(k为常数)&2.\int x^\mu dx=\frac{x^{\mu+1}}{\mu+1}+C\\
3.\int\frac{dx}x=\ln|x|+C&4.\int\frac{dx}{1+x^2}=\arctan x+C\\
5.\int\frac{dx}{\sqrt{1-x^2}}=\arcsin x+C&6.\int\cos xdx=\sin x+C\\
7.\int\sin xdx=-\cos x+C&8.\int\frac{dx}{\cos^2x}=\sec^2xdx=\tan x+C\\
9.\int\frac{dx}{\sin^2x}=\int\csc^2xdx=-\cot x+C&10.\int\sec x\tan xdx=\sec x+C\\
11.\int\csc x\cot xdx=-\csc x+C&12.\int e^xdx=e^x+C\\
13.\int a^x=dx=\frac{a^x}{\ln a}+C
\end{array}\]
###iii.不定积分的性质
####1.性质1
设函数 $f(x)$ 及 $g(x)$ 的原函数存在, 则
\[\int\left[f(x)+g(x)\right]dx=\int f(x)dx+\int g(x)dx\]
####2.性质2
设函数 $f(x)$ 的原函数存在, $k$ 为非零常数, 则
\[\int kf(x)dx=k\int f(x)dx\]
##II.换元积分法
通过复合函数的微分法反过来用于求不定积分, 利用中间变量的代换, 得到复合函数的积分法, 称为 **换元积分法**, 简称 **换元法**
###i.第一类换元法(配元法)
####1.定理1
设函数 $f(u)$ 具有原函数, $u=\varphi(x)$ 可导, 则有换元公式
\[\int f\left[\varphi(x)\right]\varphi'(x)dx=\left[\int f(u)du\right]_ {u=\varphi(x)}\]
由定理可见, 虽然 $\displaystyle\int f\left[\varphi(x)\right]\varphi'(x)$ 是一个整体的记号, 但从形式上看, 被积表达式中的 $dx$ 也可当作变量 $x$ 的微分来对待, 从而微分等式 $\varphi'(x)dx=du$ 可以方便地应用到被积表达式中来
####常用的几种配元形式:
\[\begin{array}{l}
1.\int f(ax+b)dx=\frac1a\int f(ax+b)d(ax+b)\\
2.\int f(x^n)x^{n-1}dx=\frac1n\int f(x^n)dx^n\\
3.\int f(x^n)\frac1xdx=\frac1n\int f(x^n)\frac1{x^n}dx^n\\
4.\int f(\sin x)\cos xdx=\int f(\sin x)d\sin x\\
5.\int f(\cos x)\sin xdx=-\int f(\cos x)d\cos x\\
6.\int f(\tan x)\sec^2xdx=\int f(\tan x)d\tan x\\
7.\int f(e^x)e^xdx=\int f(e^x)de^x\\
8.\int f(\ln x)\frac1xdx=\int f(\ln x)d\ln x
\end{array}\]
##III.分部积分法
利用两个函数乘积的求导法则, 来推得求积分的一个基本方法 **分部积分法**

设函数 $u=u(x)$ 及 $v=v(x)$ 具有连续导数, 则两个函数乘积的导数公式为
\[(uv)'=u'v+uv'\]
移项, 得
\[uv'=(uv)'-u'v\]
对这个等式两边求不定积分, 得
\[\int uv'dx=uv-\int u'vdx\tag 1\]
公式 (1), 称为 **分部积分分式**. 如果求 $\displaystyle\int uv'dx$ 有困难, 而求 $\displaystyle\int u'vdx$ 比较容易时, 分部积分公式就发挥作用了, 为便利起见, 公式 (1) 也可写作以下形式
\[\int udv=uv-\int vdu\]
##IV.有理函数的积分
###i.有理函数的积分
**有理函数**:
\[R(x)=\frac{P(x)}{Q(x)}=\frac{a_0x^n+a_1x^{n-1}+\cdots+a_n}{b_0x^m+b_1x^{m-1}+\cdots+b_m}\]
$m\le n$ 时, $R(x)$ 为 **假分式**; $m>n$ 时, 为 **真分式**

对于真分式 $\displaystyle\frac{P(x)}{Q(x)}$, 如果分母可分解成两个多项式乘积
\[Q(x)=Q_1(x)Q_2(x)\]
且 $Q_1(x)$ 与 $Q_2(x)$ 没有公因式, 那么它可分拆成两个真分式之和
\[\frac{P(x)}{Q(x)}=\frac{P_1(x)}{Q_1(x)}+\frac{P_2(x)}{Q_2(x)}\]
上述步骤称为把真分式化为 **部分分式** 之和, 如果 $Q_1(x)$ 或 $Q_2(x)$ 还能再分解成两个没有公因式的多项式的乘积, 那么就更简单的部分分式. 最后有理函数的分解式中出现多项式, $\displaystyle\frac{P_1(x)}{(x-a)^k}$, $\displaystyle\frac{P_2(x)}{(x^2+px+q)}$ 等三类函数(这里 $p^2-4q<0$, $P_1(x)$ 为小于 $k$ 次的多项式, $P_2(x)$ 为小于 $2l$ 次的多项式)
####四种典型部分分式的积分:
\[\begin{array}{l}
1.\int\frac A{x-a}dx=A\ln|x-a|+C\\
2.\int\frac A{(x-a)^n}dx=\frac A{1-n}(x-a)^{1-n}+C(n\ne1)\\
3.\int\frac{Mx+N}{x^2+px+q}dx\quad变分子为\frac M2(2x+p)+N-\frac{Mp}2再分项积分\\
4.\int\frac{Mx+N}{(x^2+px+q)^n}dx(p^2-4q<0,n\ne1)
\end{array}\]
###ii.可化为有理函数的积分举例
####1.三角函数有理式的积分
设 $R(\sin x,\cos x)$ 表示三角函数有理式, 则
\[\int R(\sin x,\cos x)dx\xrightarrow[万能代换]{\displaystyle t=\tan\frac x2}t的有理函数的积分\]
####2.简单无理函数的积分
被积函数为简单根式的有理式, 可通过根式代换化为有理函数的积分. 例如:
\[\begin{array}{ll}
\int R\left(x,\sqrt[n]{ax+b}\right)dx&令t=\sqrt[n]{ax+b}\\
\int R\left(x,\sqrt[n]{\frac{ax+b}{cx+d}}\right)dx&令t=\sqrt[n]{\frac{ax+b}{cx+d}}\\
\int R\left(x,\sqrt[n]{ax+b},\sqrt[m]{ax+b}\right)dx&令t=\sqrt[p]{ax+b}
\end{array}\]
