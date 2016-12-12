#定积分
##I.定积分的概念与性质
###i.定积分的定义
####1.定义
设函数 $f(x)$ 在 $[a,b]$ 上有界, 在 $[a,b]$ 中任意插入若干个分点
\[a=x_0<x_1<x_2<\cdots<x_{n-1}<x_n=b\]
把区间 $[a,b]$ 分成 $n$ 个小区间
\[\left[x_0,x_1\right],\left[x_1,x_2\right],\cdots,\left[x_{n-1},x_n\right]\]
各个小区间的长度依次为
\[\Delta x_1=x_1-x_0,\Delta x_2=x_2-x_1,\cdots,\Delta x_n=x_n-x_{n-1}\]
在每个小区间 $\left[x_{i-1},x_i\right]$ 上任取一点 $\xi_i(x_{i-1}\le\xi_i\le x_i)$, 作函数值 $f(\xi_i)$ 与小区间长度 $\Delta x_i$ 的乘积 $f(\xi_i)\Delta x_i(i=1,2,\cdots,n)$, 并作出和
\[S=\sum_{i=1}^nf(\xi_i)\Delta x_i\]
记 $\lambda=\max\{\Delta x_1,\Delta x_2,\cdots,\Delta x_n\}$, 如果当 $\lambda\to0$ 时, 这和的极限总存在, 且于闭区间 $[a,b]$ 的分法及点 $\xi_i$ 的取法无关, 那么称这个极限 $I$ 为函数 $f(x)$ 在区间 $[a,b]$ 上的定积分(简称积分), 记作 $\displaystyle\int_a^bf(x)dx$, 即
\[\int^b_af(x)dx=I=\lim_{\lambda\to0}\sum_{i=1}^nf(\xi_i)\Delta x_i\]
其中 $f(x)$ 叫做 **被积函数**, $f(x)dx$ 叫做 **被积表达式**, $x$ 叫做 **积分变量**, $a$ 叫做 **积分下限**, $b$ 叫做 **积分上限**, $[a,b]$ 叫做 **积分区间**

**注意**: 当和式 $\displaystyle\sum^n_{n=1}f(\xi_i)\Delta x_i$ 的极限存在时, 其极限 $I$ 仅与被积函数 $f(x)$ 及积分区间 $[a,b]$ 有关.

和式 $\displaystyle\sum_{i=1}^nf(\xi_i)\Delta x_i$ 通常称为 $f(x)$ 的 **积分和**. 如果 $f(x)$ 在 $[a,b]$ 上的积分存在, 那么就说 $f(x)$ 在 $[a,b]$ 上 **可积**.
####2.定理1
设 $f(x)$ 在区间 $[a,b]$ 上连续, 则 $f(x)$ 在 $[a,b]$ 上可积
####3.定理2
设 $f(x)$ 在区间 $[a,b]$ 上有界, 且只有有限个间断点, 则 $f(x)$ 在 $[a,b]$ 上可积
###ii.定积分的性质
1. 当 $b=a$ 时, $\displaystyle\int_a^af(x)dx=0$
2. 当 $a>b$ 时, $\displaystyle\int_a^bf(x)dx=-\int_b^af(x)dx$

交换定积分的上下限时, 定积分的绝对值不变而符号相反
####1.性质1
设 $\alpha$ 与 $\beta$ 均为常数, 则
\[\int_a^b\left[\alpha f(x)+\beta g(x)\right]dx=\alpha\int_a^bf(x)dx+\beta\int_a^bg(x)dx\]
对于有限个函数的线性组合也是成立的
####2.性质2
设 $a<b<c$, 则
\[\int_a^bf(x)dx=\int_a^cf(x)dx+\int_c^bf(x)dx\]
####3.性质3
如果在区间 $[a,b]$ 上 $f(x)\equiv1$, 那么
\[\int_a^b1dx=\int_a^bdx=b-a\]
####4.性质4
如果在区间 $[a,b]$ 上 $f(x)\ge0$, 那么
\[\int_a^bf(x)dx\ge0\quad(a<b)\]
####5.推论1
如果在区间 $[a,b]$ 上 $f(x)\le g(x)$, 那么
\[\int_a^bf(x)dx\le\int_a^bg(x)dx\quad(a<b)\]
####6.推论2
\[\left|\int_a^bf(x)dx\right|\le\int_a^b|f(x)|dx\quad(a<b)\]
####7.性质5
设 $M$ 及 $m$ 分别是函数 $f(x)$ 在区间 $[a,b]$ 上的最大值及最小值, 则
\[m(b-a)\le\int_a^bf(x)dx\le M(b-a)\quad(a<b)\]
####8.性质6(积分中值定理)
如果函数 $f(x)$ 在积分区间 $[a,b]$ 上连续, 那么在 $[a,b]$ 上至少存在一个点 $\xi$, 使下式成立:
\[\int_a^bf(x)dx=f(\xi)(b-a)\quad(a\le\xi\le b)\]
##II.微积分基本公式
###i.积分上限的函数及其导数
如果上限 $x$ 在区间 $[a,b]$ 上任意变动, 那么对于每一个取定的 $x$ 值, 定积分有一个对应值, 所以它在 $[a,b]$ 上定义了一个函数, 记作 $\Phi(x)$:
\[\Phi(x)=\int_a^xf(t)dt\quad(a\le x\le b)\]
####1.定理1
如果函数 $f(x)$ 在区间 $[a,b]$ 上连续, 那么积分上限的函数
\[\Phi(x)=\int_a^xf(t)dt\]
在 $[a,b]$ 上可导, 并且它的导数
\[\Phi'(x)=\frac d{dx}\int_a^xf(x)dt=f(x)\quad(a\le x\le b)\]
####2.定理2
如果函数 $f(x)$ 在区间 $[a,b]$ 上连续, 那么函数
\[\Phi(x)=\int_a^xf(t)dt\]
就是 $f(x)$ 在 $[a,b]$ 上的一个原函数
###ii.牛顿-莱不尼茨公式
####定理3(微积分基本定理)
如果函数 $F(x)$ 是连续函数 $f(x)$ 在区间 $[a,b]$ 上的一个原函数, 那么
\[\int_a^b=F(b)-F(a)\]
为了方便起见, 以后把 $F(b)-F(a)$ 记成 $[F(x)]_ a^b$, 可写成
\[\int_a^b=[F(x)]_ a^b\]
上式叫做 牛顿-莱不尼茨公式(Newton-Leibniz), 也做微积分基本公式. 它表明: 一个连续函数在区间 $[a,b]$ 上的定积分等于它的任一个原函数在区间 $[a,b]$ 上的增量.
###iii.定积分的换元法和分部积分法
####1.定积分的换元法
**定理**: 假设函数 $f(x)$ 在区间 $[a,b]$ 上连续, 函数 $x=\varphi(x)$ 满足条件:
1. $\varphi(\alpha)=a,\varphi(\beta)=b$
2. $\varphi(t)$ 在 $[\alpha,\beta]$ (或 $[\beta,\alpha]$) 上具有连续函数, 且其值域 $R_\varphi=[a,b]$,

则有
\[\int_a^bf(x)dx=\int_\alpha^\beta f[\varphi(t)]\varphi'(t)dt\]
上式成为定积分的 **换元公式**
####ii.定积分的分部积分法
依据不定积分的分部积分法, 可得
\[\int_a^bu(x)v'(x)dx=\left[\int u(x)v'(x)dx\right]_ a^b\\=\left[u(x)v(x)-\int v(x)u'(x)dx\right]_ a^b\\=\left[u(x)v(x)\right]_ a^b-\int_a^bv(x)u'(x)dx\]
简记作
\[\int_a^buv'dx=[uv]_ a^b-\int_a^bvu'dx\]
或
\[\int_a^budv=[uv]_ a^b-\int_a^bvdu\]
定积分的分部积分法公式, 公式表明原函数已经积出的部分可以先用上下限代入
##IV.反常积分
积分区间为无穷区间, 或者被积函数为无界函数的积分, 对定积分作如下两种推广, 从而形成反常积分
###i.无穷限的反常积分
设函数 $f(x)$ 在区间 $[a,\infty)$ 上连续, 任取 $t>a$, 作定积分 $\displaystyle\int_a^tf(x)dx$, 再求极限:
\[\lim_{t\to+\infty}\int_a^tf(x)dx\]
这个对变上限积分的算式称为 **函数 $f(x)$ 在无穷区间 $[a,+\infty)$ 上的反常积分**, 记作 $\displaystyle\int_a^{+\infty}f(x)dx$
####定义1
设函数 $f(x)$ 在区间 $[a,+\infty)$ 上连续, 如果上述极限存在, 那么称反常积分 $\displaystyle\int_a^{+\infty}f(x)dx$ **收敛**, 并称此为改反常积分的值; 如果极限不存在, 那么称反常积分 $\displaystyle\int_a^{+\infty}f(x)dx$ **发散**

---
类似地, 设函数 $f(x)$ 在区间 $(-\infty,b]$ 上连续, 任取 $t<b$
\[\lim_{t\to-\infty}\int_t^bf(x)dx\]
称为 **函数 $f(x)$ 在无穷区间 $(-\infty,b]$ 上的反常积分**, 记作 $\displaystyle\int_{-\infty}^bf(x)dx$
####定义2
设函数 $f(x)$ 在区间 $(-\infty,b]$ 上连续, 如果极限存在, 那么称反常积分 $\displaystyle\int_{-\infty}^bf(x)dx$ **收敛**, 并称此极限为该反常函数的值; 如果极限不存在, 那么称反常函数 $\displaystyle\int_{-\infty}^bf(x)dx$ **发散**

---
设函数 $f(x)$ 在区间 $(-\infty,+\infty)$ 上连续, 反常积分 $\displaystyle\int_{-\infty}^0f(x)dx$ 与 反常积分 $\displaystyle\int_0^{+\infty}f(x)dx$ 之和称为 函数 $f(x)$ 在无穷区间 $(-\infty,+\infty)$ 上的反常积分, 记为 $\displaystyle\int_{-\infty}^{+\infty}f(x)dx$, 即
\[\int_{-\infty}^{+\infty}f(x)dx=\int^0_{-\infty}f(x)dx+\int^{+\infty}_0f(x)dx\]
####定义3
设函数 $f(x)$ 在区间 $(-\infty,+\infty)$ 上连续, 如果反常积分 $\displaystyle\int_{-\infty}^0f(x)dx$ 与反常积分 $\displaystyle\int^{+\infty}_0f(x)dx$ 均收敛, 那么称反常积分 $\displaystyle\int_{-\infty}^{+\infty}f(x)dx$ **收敛**, 并称反常积分 设函数 $f(x)$ 在区间 $(-\infty,+\infty)$ 上连续, 如果反常积分 $\displaystyle\int_{-\infty}^0f(x)dx$ 的值与反常积分 $\displaystyle\int^{+\infty}_0f(x)dx$ 的值之和为反常积分 $\displaystyle\int_{-\infty}^{+\infty}f(x)dx$ 的值; 否则就称反常积分 $\displaystyle\int_{-\infty}^{+\infty}f(x)dx$ **发散**.

上述反常积分统称为 **无穷限的反常积分**.
