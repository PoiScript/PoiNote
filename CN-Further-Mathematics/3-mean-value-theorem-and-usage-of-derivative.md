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
1. 当 $n=0$ 时, 公式(3) 变成拉格朗日中值公式 $f(x)=f(x_0)+f'(\xi)(x-x_0)(\xi在x_0与x之间)$
1. 公式(4) 称为 **拉格郎日余项**.
