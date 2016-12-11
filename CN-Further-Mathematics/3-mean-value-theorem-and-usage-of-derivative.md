#微分中值定理与导数的应用
##I.中值定理
###i.罗尔(Rolle)定理
####1.费马(Fermat)引理
设函数 $f(x)$ 在点 $x_0$ 的某邻域 $U(x_0)$ 内有定义, 并且在 $x_0$ 处可导, 如果对任意的 $x\in U(x_0)$, 有:
\[f(x)\le f(x_0)(或f(x)\ge f(x_0))\]
那么 $f'(x_0)=0$
#####证:
1. 设 $\forall x_0+\Delta x\in U(x_0), f(x_0+\Delta x)\le f(x_0)$
1. $f'(x_0)=\displaystyle\lim_{\Delta x\to0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$
1. $\displaystyle\begin{cases}f'_ -(x_0)\ge0(\Delta\to0^-)\\f'_ +(x_0)\le0(\Delta\to0^+)\end{cases}\Rightarrow f'(x_0)=0$
####2.罗尔(Rolle)定理
$f(x)$ 满足:
1. 在区间 $[a,b]$ 上连续
1. 在区间 $(a,b)$ 内可导
1. $f(a)=f(b)$

则, 在 $(a,b)$ 内至少存在一点 $\xi$ 使 $f'(\xi)=0$
#####证:
由于 $f(x)$ 在闭区间 $[a,b]$ 上连续, 故在 $[a,b]$ 上取得最大值 $M$ 和最小值 $m$.
1. 若 $M=m$, 则 $f(x)\equiv M,x\in[a,b]$, 因此 $\forall\xi\in(a,b),f'(\xi)=0$
1. 若 $M>m$, 则 $M$ 和 $m$ 中至少有一个与端点值不等, 不妨设 $M\ne f(a)$, 则至少存在一点 $\xi\in(a,b)$, 使 $f(\xi)=M$, 则由费马引理得 $f'(\xi)=0$
#####注意:
1. 定理条件条件不全具备, 结论不一定成立.
2) 定理条件只是充分的.本定理可推广为:
\[y=f(x)在(a,b)内可导,且\lim_{x\to a^+}f(x)=\lim_{x\to b^-}f(x)\\\Rightarrow在(a,b)内至少存在一点\xi,使f'(\xi)=0\]
###ii.拉格朗日中值定理
$y=f(x)$ 满足:
1. 在区间 $[a,b]$ 上连续
1. 在区间 $(a,b)$ 内可导

则至少存在一点 $\xi\in(a,b)$, 使 $f'(\xi)=\displaystyle\frac{f(b)-f(a)}{b-a}$
####证明:
1. 问题转化为证 $\displaystyle f'(\xi)-\frac{f(b)-f(a)}{b-a}=0$
1. 作辅助函数 $\displaystyle\varphi(x)=f(x)-\frac{f(b)-f(a)}{b-a}$
1. 显然 $\displaystyle\varphi(a)=\frac{bf(a)-af(b)}{b-a}=\varphi(b)$, 由罗尔定理知至少存在一点 $\xi\in(a,b)$, 即 $\varphi'(\xi)=0$
1. 即定理结论成立 .

####拉格朗日中值定理的有限增量形式:
令 $a=x_0,b=x_0+\Delta x$, 则 $\Delta y=f'(\underbrace{x_0+\theta\Delta x}_{\xi})\Delta x(0<\theta<1)$
####推论:
若函数 $f(x)$ 在区间 $I$ 上满足 $f'(x)=0$, 则 $f(x)$ 在 $I$ 上 **必为常数**.
#####证:
在 $I$ 上任取两点 $x_1,x_2(x_1<x_2)$, 由拉格郎日中值公式, 得 $f(x_2)-f(x_1)=f'(\xi)(x_2-x_1)=0(x_1<\xi<x_2)$, 有 $f(x_2)=f(x_1)$,由 $x_1,x_2$ 的任意性知, $f(x)$ 在 $I$ 上为常数.
###iii.柯西(Cauchy)中值定理
$f(x)$ 及 $F(x)$ 满足:
1. 在闭区间 $[a,b]$ 上连续
1. 在开区间 $(a,b)$ 内可导
1. 在开区间 $(a,b)$ 内 $F'(x)\ne0$

则至少存在一点 $\xi\in(a,b)$, 使 $\displaystyle\frac{f(b)-f(a)}{F(b)-F(a)}=\frac{f'(\xi)}{F'(xi)}$
####分析:
$F(b)-F(a)=F'(\eta)(b-a)\ne0(a<\eta<b)$, 要证 $\displaystyle\underbrace{\frac{f(b)-f(a)}{F(b)-F(a)}F'(\xi)-f'(\xi)}_{\varphi'(\xi)}=0$

有 $\displaystyle\varphi(x)=\frac{f(b)-f(a)}{F(b)-F(a)}F(x)-f(x)$
####证:
作辅助函数 $\displaystyle\varphi(x)=\frac{f(b)-f(a)}{F(b)-F(a)}F(x)-f(x)$
显然, $\varphi(x)$ 在闭区间 $[a,b]$ 上连续, 在开区间 $(a,b)$ 内可导, 且
\[\varphi(a)=\varphi(b)=\frac{F(b)f(a)-F(a)f(b)}{F(b)-F(a)}\]
故 $\varphi(x)$ 适合罗尔定理的条件, 因此在 $(a,b)$ 内至少有一点 $\xi$, 使
\[\varphi'(\xi)=f'(\xi)-\frac{f(b)-f(a)}{F(b)-F(a)}F'(\xi)=0\]
因此得
\[\frac{f(b)-f(a)}{F(b)-F(a)}=\frac{f'(\xi)}{F'(\xi)}\]
####柯西定理的几何意义:
\[\underbrace{\frac{f(b)-f(a)}{F(b)-F(a)}}_{弦的斜率}=\underbrace{\frac{f'(\xi)}{F'(\xi)}}_{切线斜率}\]
###iv.微分中值定理的条件、结论及关系
\[费马引理\to罗尔定理\\罗尔定理\xrightarrow{f(b)=f(a)}拉格朗日中值定理\\柯西中值定理\xrightarrow{F(x)}拉格朗日中值定理\\罗尔定理\xrightarrow{f(b)=f(a),F(x)}柯西中值定理\]
##II.洛必达法则
###i. $\frac00$型未定式
####定理1
1. $\displaystyle\lim_{x\to a}f(x)=\lim_{x\to a}F(x)=0$
1. 在点 $a$ 的某去心邻域内, $f'(x)$ 及 $F'(x)$ 都存在, 且 $F'(x)\ne0$
1. $\displaystyle\frac{f'(x)}{F'(x)}$ 存在或为无穷大
则
\[\lim_{x\to a}\frac{f(x)}{F(x)}=\lim_{x\to a}\frac{f'(x)}{F'(x)}\]
####证明
无妨假设 $f(a)=F(a)=0$, 指出的邻域内任取 $x\ne a$, 则 $f(x),F(x)$ 在以 $x,a$ 为端点的区间上满足柯西定理条件, 故
\[\frac{f(x)}{F(x)}=\frac{f(x)-f(a)}{F(x)-F(a)}=\frac{f'(\xi)}{F'(\xi)}(ξ在x,a之间)\\\therefore\lim_{x\to a}\frac{f(x)}{F(x)}=\lim_{x\to a}\frac{f'(\xi)}{F'(\xi)}=\lim_{x\to a}\frac{f'(x)}{F'(x)}\]
####推论1
定理1 中 $x\to a$ 换为 $x\to a^+,x\to a^-,x\to\infty,x\to+\infty,x\to-\infty$
之一, 条件 2) 作相应的修改, 定理 1 仍然成立.
###ii. $\frac\infty\infty$ 型未定式
####定理2
1. $\displaystyle\lim_{x\to a}\left|f(x)\right|=\lim_{x\to a}\left|F(x)\right|=\infty$
1. 当 $|x|>N$ 时, $f'(x)$ 及 $F'(x)$ 都存在, 且 $F'(x)\ne0$
1. $\displaystyle\lim_{x\to\infty}\frac{f'(x)}{F'(x)}$ 存在(或为无穷大)
###iii.其他未定式: $0\cdot\infty,\infty-\infty,0^0,1^\infty,\infty^0$
####解决方法:
\[\infty-\infty\xrightarrow{通分转化}\begin{cases}0/0\\\infty/\infty\end{cases}\\\begin{cases}0^0\\1^\infty\\\infty^0\end{cases}\xrightarrow{取对数转化}0\cdot\infty\xrightarrow{取倒数转化}\begin{cases}0/0\\\infty/\infty\end{cases}\]
##III.泰勒(Taylor)公式
###i.泰勒公式的建立
在微分应用中已知近似公式:
\[f(x)\approx\underbrace{f(x_0)+f'(x_0)(x-x_0)}_{p_1(x)\quad x的一次多项式}\]
**特点**: $p_1(x_0)=f(x_0),p_1'(x_0)=f'(x_0)$
###ii.泰勒中值定理:
####定理1:
如果函数 $f(x)$ 在 $x_0$ 处, 具有 $n$ 阶的导数, 那么存在 $x_0$ 的一个邻域, 对于该邻域的任一 $x$, 有
\[f(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2\\+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+R_n(x)\tag 1\]
其中
\[R_n(x)=o((x-x_0)^n)\tag 2\]
1. 公式(1) 称为 $f(x)$ 的 **$n$ 阶泰勒公式**.
1. 公式(2) 称为 $n$ 阶泰勒公式的 **佩亚诺余项**.
####定理2:
如果函数 $f(x)$ 在 $x_0$ 的某个邻域 $U(x_0)$ 内具有 $(n+1)$ 阶导数, 那么任一 $x\in U(x_0)$, 有
\[f(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2\\+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+R_n(x)\tag 3\]
其中
\[R_n(x)=\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}\tag 4\]
这里的 $\xi$ 是 $x_0$ 与 $x$ 之间的某个值
1. 当 $n=0$ 时, 公式(3) 变成拉格朗日中值公式: $f(x)=f(x_0)+f'(\xi)(x-x_0)(\xi在x_0与x之间)$
1. 公式(4) 称为 **拉格郎日余项**.
####麦克劳林公式:
在泰勒公式中若取 $x_0=0,\xi=\theta x(0<\theta<1)$ 则有
\[f(x)=f(0)+f'(0)x+\frac{f''(0)}{2!}+\cdots+\frac{f^{(n)}}{n!}x^n+\frac{f^{(n+1)}(\theta x)}{(n+1)!}x^{n+1}\]
称为 **麦克劳林(Maclaurin)公式**. 由此得近似公式
\[f(x)\approx f(0)+f'(0)x+\frac{f''(0)}{2!}x^2+\cdots+\frac{f^{(n)}(0)}{n!}x^n\]
若在公式成立的区间上 $\left|f^{(n+1)}(x)\right|\le M$, 则有误差估计式
\[\left|R_n(x)\right|\le\frac M{(n+1)!}\left|x\right|^{n+1}\]
####几个初等函数的麦克劳林公式
#####(1).$f(x)=e^x$
\[\because f^{(k)}(x)=e^x,f^{(k)}(0)=1(k=1,2,\cdots)\\\therefore e^x=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\cdots+\frac{x^n}{n!}+R_n(x)\]
**其中**: $\displaystyle R_n(x)=\frac{e^{\theta x}}{(n+1)!}(0<\theta<1)$
#####(2).$f(x)=\sin x$
\[\because f^{(k)}(x)=\sin(x+k\cdot\frac\pi2)\\f^{(k)}(0)=\sin\frac\pi2=\begin{cases}0&k=2m\\(-1)^{m-1}&k=2m-1\end{cases}(m=1,2\cdots)\\\therefore\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}+\cdots+(-1)^{m-1}\frac{x^{2m-1}}{(2m-1)!}+R_{2m}(x)\]
**其中**: $\displaystyle R_{2m}(x)=\frac{(-1)^m\cos(\theta x)}{(2m+1)!}x^{2m+1}(0<\theta<1)$
#####(3).$f(x)=\cos x$
**类似可得**:
\[\cos x=1-\frac{x^2}{2!}+\frac{x^4}{4!}+\cdots+(-1)^m\frac{x^{2m}}{(2m)!}+R_{2m+1}(x)\]
**其中**: $\displaystyle R_{2m+1}(x)=\frac{(-1)^{m+1}\cos(\theta x)}{(2m+2)!}x^{2m+2}(0<\theta<1)$
#####(4).$f(x)=(1+x)^{a}(x>-1)$
\[\because f^{(k)}=a(a-1)\cdots(a-k+1)(1+x)^{a-k}\\f^{(k)}(0)=a(a-1)\cdots(a-k+1)(k=1,2\cdots)\\\therefore(1+x)^a=1+ax+\frac{a(a-1)}{2!}+\cdots+\frac{a(a-1)\cdots(a-n+1)}{n!}x^n+R_n(x)\]
**其中**: $\displaystyle R_n(x)=\frac{a(a-1)\cdots(a-n)}{(n+1)!}(1+\theta x)^{a-n-1}x^{n+1}(0<\theta<1)$
#####(5).$f(x)=\ln(1+x)(x>-1)$
已知
\[f^{(k)}(x)=(-1)^{k-1}\frac{(k-1)!}{(1+x)^k}(k=1,2\cdots)\]
类似可得
\[\ln(1+x)=x-\frac{x^2}2+\frac{x^3}3+\cdots+(-1)^{n-1}\frac{x^n}n+R_n(x)\]
**其中**: $\displaystyle R_n(x)=\frac{(-1)^n}{n+1}\frac{x^{n+1}}{(1+\theta x)^{n+1}}(0<\theta<1)$
###iii.泰勒公式的应用
####1.在近似计算中的应用
\[f(x)\approx f(0)+f'(0)+\frac{f''(0)}{2!}+\cdots+\frac{f^{(n)}}{n!}x^n\]
**误差**: $\left|R_n(x)\right|\le\displaystyle\frac M{(n+1)!}|x|^{n+1}$

$M$ 为 $|f^{(n+1)}(x)|$ 在包含 $0,x$ 的某区间上的上界.

**需解问题的类型**:
1. 已知 x 和误差限 , 要求确定项数 n ;
1. 已知项数 n 和 x , 计算近似值并估计误差;
1. 已知项数 n 和误差限 , 确定公式中 x 的适用范围.
####2.利用泰勒公式求极限
####3.利用泰勒公式证明不等式
##IV.函数的单调性与曲线的凹凸性
###i.函数单调性的判定法
导数是图形上切线的斜率，当斜率为正时，曲线上升；当斜率为负时，曲线下降。

**定理1**: 设 $y=f(x)$ 在区间 $I=[a,b]$ 上连续，在 $(a,b)$ 内可导，则
1. $f'(x)>0$ 时 $f(x)$ 在区间 $[a,b]$ 上 **单调增加**
1. $f'(x)<0$ 时 $f(x)$ 在区间 $[a,b]$ 上 **单调减少**

**证**: 无妨设 $f'(x)>0,x\in I$, 任取 $x_1,x_2\in(x_1<x_2)$, 由拉格朗日中值定理得
\[f(x_2)-f(x_1)=f'(\xi)(x_2-x_1)>0,\xi\in(x_1,x_2)\subset I\]
故 $f(x_1)<f(x_2)$, 这说明 $f(x)$ 在 $I$ 内单调递增.

**说明**:
1. 单调区间的分界点除驻点外,也可是导数不存在的点.
1. 如果函数在某驻点两边导数同号, 则不改变函数的单调性 .
###ii.曲线的凹凸与拐点
####1.凹凸性的定义
**定义**: 设函数 $f(x)$ 在区间 $I$ 上连续, $\forall x_1,x_2\in I$
1. 若恒有 $\displaystyle f(\frac{x_1+x_2}2)<\frac{f(x_1)+f(x_2)}2$ 则称图形是 **凹** 的;
1. 若恒有 $\displaystyle f(\frac{x_1+x_2}2)>\frac{f(x_1)+f(x_2)}2$ 则称图形是 **凸** 的.

连续曲线上有切线的凹凸分界点称为 **拐点**.

**性质**:
1. 凹弧在其切线上方，凸弧在其切线下方。
1. 凹弧切线的斜率递增，凸弧切线的斜率递减。

定理2.(凹凸判定法)
设函数 $f(x)$ 在区间 $I$ 上有二阶导数
1. 在 $I$ 内 $f''(x)>0$, 则 $f(x)$ 在 $I$ 内图形是凹的;
1. 在 $I$ 内 $f''(x)<0$, 则 $f(x)$ 在 $I$ 内图形是凸的.

**证**:
$\forall x_1,x_2\in I$ 利用一阶泰勒公式可得
\[f(x_1)=f\left(\frac{x_1+x_2}2\right)+f'\left(\frac{x_1+x_2}2\right)\left(x_1-\frac{x_1+x_2}2\right)\\+\frac{f''(\xi_1)}{2!}\left(x_1-\frac{x_1+x_2}2\right)^2\\f(x_2)=f\left(\frac{x_1+x_2}2\right)+f'\left(\frac{x_1+x_2}2\right)\left(x_2-\frac{x_1+x_2}2\right)\\+\frac{f''(\xi_2)}{2!}\left(x_2-\frac{x_1+x_2}2\right)^2\]
两式相加
\[f(x_1)+f(x_2)=2f\left(\frac{x_1+x_2}2\right)+\frac1{2!}\left(\frac{x_2-x_1}2\right)^2\left[f''(\xi_1)+f''(\xi_2)\right]\]
当 $f''(x)\lessgtr0$ 时, $\displaystyle\frac{f(x_1)+f(x_2)}2\lessgtr f\left(\frac{x_1+x_2}2\right)$

**说明**:
1. 若在某点二阶导数为0, 在其两侧二阶导数不变号, 则曲线的凹凸性不变.
1. 拐点的判别法: 设曲线 $f(x)$, $f''(x_0)=0)$ 或不存在, 但 $f''(x)$ 在 $x_0$ 两侧异号, 则点 $(x_0,f(x_0))$ 是曲线 $y=f(x)$ 的一个拐点.
##V.函数的极值与最大值最小值
###i.函数的极值及其求法
####1.定义:
设函数 $f(x)$ 在点 $x_0$ 的某个邻域 $U(x_0)$ 内有定义, 如果对于去心邻域 $\mathring U(x_0)$ 内的任一 $x$, 有
\[f(x)<f(x_0)(或f(x)>f(x_0))\]
那么称 $f(x_0)$ 时函数 $f(x)$ 的一个极大值(或极小值)
1. 极大值 极小值统称为 **极值**, 使函数取得极值的点 $x_0$ 称为 **极值点**
1. 极值点一定是区间的内点
1. 极值是局部概念，是局部的最值
####2.必要条件:定理(费马定理)
若 $f(x)$ 在其极值点 $x_0$ 可导, 则 $f'(x_0)=0$
1. 导数为零的点称为函数的驻点
1. 极值点一定是驻点或不可导点
1. 驻点或不可导点不一定是极值点
####3.第一充分条件
设函数 $f(x)$ 在 $x_0$ 处连续, 且在 $x_0$ 的某去心邻域 $\mathring{U}(x_0,\delta)$ 内可导
1. 若 $x\in(x_0-\delta,x_0)$ 时, $f'(x)>0$, 而 $x\in(x_0,x_0+\delta)$ 时, $f'(x)<0$, 则 $f(x)$ 在 $x_0$ 处取得极大值
1. 若 $x\in(x_0-\delta,x_0)$ 时, $f'(x)<0$, 而 $x\in(x_0,x_0+\delta)$ 时, $f'(x)>0$, 则 $f(x)$ 在 $x_0$ 处取得极小值
1. 若 $x\in\mathring{U}(x_0,\delta)$ 时, $f'(x)$ 的符号保持不变, 则 $f(x)$ 在 $x_0$ 处没有极值
####4.第二充分条件
设函数 $f(x)$ 在 $x_0$ 处具有二阶导数且 $f'(x_0)=0$, $f''(x_0)\ne0$, 则
1. 当 $f''(x_0)<0$ 时, 函数 $f(x)$ 在 $x_0$ 处取得极大值
2. 当 $f''(x_0)>0$ 时, 函数 $f(x)$ 在 $x_0$ 处取得极小值
###ii.最大值与最小值问题
可用如下方法求 $f(x)$ 在 $[a,b]$ 上的最大值和最小值
1. 求出 $f(x)$ 在 $(a,b)$ 内的驻点及不可导点
2. 计算 $f(x)$ 在上述驻点, 不可导点处的函数值及 $f(a),f(b)$
3. 比较 (2) 中诸值的大小, 其中最大的便是 $f(x)$ 在 $[a,b]$ 上的最大值, 最小的便是 $f(x)$ 在 $[a,b]$ 上的最小值

**特别**:
1. 当 $f(x)$ 在 $[a,b]$ 内只有 **一个** 极值可疑点时, 若在此点取极大(小)值 , 则也是最大(小)值.
1. 当 $f(x)$ 在 $[a,b]$ 上 **单调** 时, 最值必在端点处达到.
1. 对应用问题, 有时可根据实际意义判别求出的可疑点是否为最大值点或最小值点 .
##VI.函数图形的描绘
###i.曲线的渐近线
####定义
若曲线 $C$ 上的点 $M$ 沿着曲线无限地远离原点时, 点 $M$ 与某一直线 $L$ 的距离(或为“纵坐标差”)趋于 0, 则称直线 $L$ 为曲线 $C$ 的 **渐近线**.
####1.水平与铅直渐近线
若 $\displaystyle\lim_{x\to+\infty}f(x)=b$ 则曲线 $y=f(x)$ 有水平渐近线 $y=b(当x\to-\infty)$

若 $\displaystyle\lim_{x\to-\infty}f(x)=\infty$ 则曲线 $y=f(x)$ 有垂直渐近线 $x=x_0(当x\to x^-_ 0)$
####2.斜渐近线
若 $\displaystyle\lim_{x\to+\infty}[f(x)-f(kx+b)]=0$, 则曲线 $y=f(x)$ 有斜渐近线 $y=kx+b$
###ii.函数图形的描绘
**步骤**:
1. 确定函数 $y=f(x)$ 的定义域, 并考察其对称性及周期性;
2. 求 $f'(x),f''(x)$, 并求出 $f'(x)$ 及 $f''(x)$ 为 0 和不存在的点;
3. 列表判别增减及凹凸区间, 求出极值和拐点;
4. 求渐近线;
5. 确定某些特殊点, 描绘函数图形.
##VII.平面曲线的曲率
###i.弧微分
设 $f(x)$ 在 $(x,x+\Delta x)$ 内有连续导数, 其图形为 $\stackrel{\Large\frown}{MM'}$, 于是
\[\left(\frac{\Delta s}{\Delta x}\right)^2=\left(\frac{\stackrel{\Large\frown}{MM'}}{\Delta x}\right)^2\cdot\frac{|MM'|^2}{(\Delta x)^2}=\left(\frac{\stackrel{\Large\frown}{MM'}}{\Delta x}\right)^2\cdot\frac{(\Delta x)^2+(\Delta y)^2}{(\Delta x)^2}\\=\left(\frac{\stackrel{\Large\frown}{MM'}}{\Delta x}\right)^2\cdot\left[1+\left(\frac{\Delta y}{\Delta x}\right)^2\right]\]
\[\frac{\Delta s}{\Delta x}=\pm\sqrt{\left(\frac{\stackrel{\Large\frown}{MM'}}{\Delta x}\right)^2\cdot\left[1+\left(\frac{\Delta y}{\Delta x}\right)^2\right]}\]
当 $\Delta x\to0$ 时, $M\to M'$, 弧的长度于弦的长度之比的极限等于1, 即
\[\lim_{M\to M'}\frac{|\stackrel{\Large\frown}{MM'}|}{|MM'|}=1\]
又
\[\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}=y'\]
因此得
\[\frac{ds}{dx}=\pm\sqrt{1+y'^2}\]
由于 $s=s(x)$ 是单调函数, 从而根号前应取正号, 于是有
\[ds=\sqrt{1+y'^2}dx\]
这就是 **弧微分公式**
###ii.曲率及其计算公式
####定义
在光滑弧上自点 $M$ 开始取弧段, 其长为 $\Delta s$ 对应切线转角为 $\Delta\alpha$, 定义

弧段 $\Delta s$ 上的平均曲率
\[K=\left|\frac{\Delta\alpha}{\Delta s}\right|\]
点 $M$ 处的曲率
\[K=\lim_{\Delta s\to0}\left|\frac{\Delta\alpha}{\Delta s}\right|=\left|\frac{d\alpha}{ds}\right|\]
**注意**: 直线上任意点处的曲率为 **0** !
####曲率 $K$ 的计算公式
设曲线弧 $y=f(x)$ 二阶可导, 则由
\[\tan\alpha=y'(-\frac\pi2<\alpha<\frac\pi2)\\\because\alpha=\arctan y'\\d\alpha=(\arctan y')'dx=\frac{y''}{1+y'^2}dx\]
\[又ds=\sqrt{1+y'^2}dx\]
故曲率计算公式为
\[K=\frac{|y''|}{(1+y'^2)^{3/2}}\]
$\because|y'|\ll1$, 有曲率近似计算公式 $K\approx|y''|$
###iii.曲率圆与曲率半径
设 $M$ 为曲线 $C$ 上任一点, 在点 $M$ 处作曲线的切线和法线, 在曲线的凹向一侧法线上取点 $D$ 使
\[|DM|=R=\frac1K\]
把以 $D$ 为中心, $R$ 为半径的圆叫做曲线在点 $M$ 处的 **曲率圆**(密切圆), $R$ 叫做 **曲率半径**, $D$ 叫做 **曲率中心**.

在点 $M$ 处曲率圆与曲线有下列密切关系:
1. 有公切线 2. 凹向一致 3. 曲率相同

设曲线方程为 $y=f(x)$, 且 $y''\ne0$, 求曲线上点 $M$ 处的曲率半径及曲率中心 $D(\alpha,\beta)$ 的坐标公式.

设点 $M$ 处的曲率圆方程为
\[(\xi-\alpha)^2+(\eta-\beta)^2=R^2\]
故曲率半径公式为
\[R=\frac1K=\frac{(1+y'^2)^{3/2}}{|y''|}\]
$\alpha,\beta$ 满足方程组
\[\begin{cases}(x-\alpha)^2+(y-\beta)^2=R^2\\y'=-\displaystyle\frac{x-\alpha}{y-\beta}&(DM\bot MT)\end{cases}\]
由此可得曲率中心公式
\[\begin{cases}\alpha=x-\displaystyle\frac{y'(1+y'^2)}{y''}\\\beta=y+\displaystyle\frac{1+y'^2}{y''}\end{cases}\]
当点 $M(x,y)$ 沿曲线 $y=f(x)$ 移动时, 相应的曲率中心的轨迹 $G$ 称为曲线 $C$ 的 **渐屈线**, 曲线 $C$ 称为曲线 $G$ 的 **渐伸线**.

曲率中心公式可看成渐屈线的参数方程(参数为 $x$).
##IIX.方程的近似解
求方程的近似解, 可分成两步来做:
1. 确定根的大致范围, 集体来说就是确定一个区间, 使得所求跟是位于这个区间的唯一实根. 这一步叫做 **根的隔离**, 区间叫做 **隔离区间**.
2. 以根的隔离区间的端点作为根的初始近似值, 逐步改善根的近似值的精度值, 直至求得满足精确度要求的近似值.
###1.二分法
###2.切线法
###3.割线法
