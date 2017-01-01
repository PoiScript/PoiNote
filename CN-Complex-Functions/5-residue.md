#留数
##I.留数概念及基本定理
###i.留数概念
由柯西积分定理, 如果 $z_0$ 是 $f(z)$ 的解析点, 围线 $\Gamma$ 包围点 $z_0$ 且全含于 $z_0$ 的某邻域内, 且 $f(z)$ 在该邻域解析, 则
\[\int_\Gamma f(z)dz=0\]
如果 $z_0$ 是函数 $f(z)$ 的孤立奇点, 同样围线 $\Gamma$ 包围 $z_0$ 且全含于 $z_0$ 的某去心邻域内, $f(z)$ 在该去心邻域内解析, 那么积分 $\displaystyle\int_\Gamma f(z)dz$ 不一定为 0 , 但是利用洛朗系数公式可将这个积分值计算出来.

设 $z_0$ 是 $f(z)$ 的一个有限孤立奇点, 即 $f(z)$ 在点 $z_0$ 的去心邻域 $0<|z-z_0|<r$ 内解析, 于是 $f(z)$ 在 $z_0$ 的洛朗展式是 :
\[f(z)=\cdots+\frac{a_{-m}}{(z-z_0)^m}+\frac{a_{-(m-1)}}{(z-z_0)^{(m-1)}}+\cdots+\frac{a_{-1}}{z-z_0}\\+a_0+a_1(z-z_0)+a_2(z-z_0)^2+\cdots,0<|z-z_0|<r\]
将此式两边同时沿 $\displaystyle\Gamma_\rho:|z-z_0|=\rho,0<|z-z_0|<r$ 积分且对等
号右端逐项积分, 有
\[\int_{\Gamma_\rho}f(z)dz=\cdots+\int_{\Gamma_\rho}\frac{a_{-m}}{(z-z_0)^m}dz+\int_{\Gamma_\rho}\frac{a_{-(m-1)}}{(z-z_0)^{m-1}}dz+\cdots+\int_{\Gamma_\rho}\frac{a_{-1}}{z-z_0}dz+\int_{\Gamma_\rho}a_0dz+\cdots\tag 1\]
我们已熟知
\[\int_{\Gamma_\rho}\frac{dz}{(z-z_0)^m}=
\begin{cases}2\pi i&(n=1)\\
0&(n\ne0,n为整数)\end{cases}\]
由此, (1) 式右端诸积分除 $\displaystyle\int_{\Gamma_\rho}\frac{a_{-1}}{z-z_0}dz$ 外均为 0, 即
\[\int_{\Gamma_\rho}f(z)dz=\int_{\Gamma_\rho}\frac{a_{-1}}{z-z_0}dz=2\pi ia_{-1}\]
从而
\[a_{-1}=\frac1{2\pi i}\int_{\Gamma_\rho}f(z)dz\]
####1.定义1
设 $z_0$ 是解析函数 $f(z)$ 的 **有限孤立奇点**, 我们称 $f(z)$ 在 $z_0$ 处的洛朗展式 $\displaystyle f(z)=\sum^\infty_{n=-\infty}a_n(z-z_0)^n$ 中负一次幂项系数 $a_{-1}$ 为 $f(z)$ 在点 $z_0$ 的留数或残数, 记作 $\displaystyle\mathrm{Res}_{z=z_0}=a_{-1}$

由上面的讨论知,
\[\mathrm{Res}_{z=z_0}f(z)=a_{-1}=\frac1{2\pi i}\int_{\Gamma_\rho}f(z)dz\]
其中 $\Gamma_\rho:|z-z_0|=\rho(0<\rho<r)$, $\Gamma_\rho$ 也可以是 $z_0$ 的去心邻域 $0<|z-z_0|<r$ 内绕 $z_0$ 的任意正向简单闭路.

当有限点 $z_0$ 是函数 $f(z)$ 的可去奇点时, 其洛朗展式的主要部分为零, 因而的 $\displaystyle\frac1{z-z_0}$ 系数 $a_{-1}=0$. 所以, 函数在有限可去奇点的留数为零 .
###ii.留数定理
####定理1(留数定理)
设函数 $f(z)$ 在正向简单围线 (或复围线) $\Gamma$ 所范围的有界区域 $D$ 内除去有限个奇点 $z_1,z_2,...,z_n$ 外解析, 在闭域 $D=D+\Gamma$ 上除 $z_1,z_2,...,z_n$ 外连续, 则 $\displaystyle\int_\Gamma f(z)dz=2\pi i\sum^n_{k=1}\mathrm{Res}_{z=z_k}f(z)$

从留数定理可以看出, 当函数在围线内只有有个孤立奇点时, 函数沿此围线积分的计算可转化成 围线内 部各个奇 点处的 留数的计算 , 也就是说 , 留数定理 把整体问 题转化 成了局 部问题 .留数定理是本章的中心问题及实际应用的理论根据 .

###iii. 留数的计算
####1.利用留数定义求留数
利用留数定义求留数, 可以考虑两个途径:
1. 将函数展成洛朗级数, 找出负一次幂项系数 $a_{-1}$
2. 直接计算积分 $\displaystyle\frac1{2\pi i}\int_\Gamma f(z)dz$

从留数定理可以 看出积 分与 留 数的 关系 ,
利用积分可以计算 留数 ; 反之 , 利用留数 也可以 计算积 分 .函数 沿
内部有有限 奇点的围 线的积 分可由多 种方法来 计算 , 但 利用留 数
计算也是一种较好的选择 .
####2.极点处的留数
函数在 有限可去 奇点的 留数 为零 .因 此, 只考虑孤立奇点是极点和本性奇点的情形的留数求法 .一般说来 只要将函数 在孤立奇 点展成 洛朗展式 , 立即就 可以找出 该点的 留数 .但是有时计算洛朗展式非常繁杂 , 必须另寻更简便的
方法.

设 $z_0$ 是 $f(z)$ 的 $n$ 级极点, 有
\[f(z)=\frac{\Phi(z)}{(z-z_0)^n}\tag 1\]
即
\[\Phi(z)=(z-z_0)^nf(z)\]
其中 $\Phi(z)$ 在点 $z_0$ 解析, 且 $\Phi(z_0)\ne0$ (或 $\Phi(z)$ 以 $z_0$ 为可去奇点, 且 $\displaystyle\lim_{z\to z_0}\Phi(z)=\alpha\ne0$, 此时可同样处理, 把 $\Phi(z_0)$ 定义成 $\alpha$ 即可).

对 (1) 式两边积分, 得
\[\int_\Gamma f(z)dz=\int_\Gamma\frac{\Phi(z)}{(z-z_0)^n}dz\]
或
\[\frac1{2\pi i}\int_\Gamma f(z)dz=\frac1{(n-1)!}\frac{(n-1)!}{2\pi i}\int_\Gamma\frac{\Phi(z)}{(z-z_0)^{(n-1)+1}}dz\]
于是
\[\mathrm{Res}_{z=z_0}f(z)=\frac{\Phi^{(n-1)}(z_0)}{(n-1)!}\]
定理 2
若 $z_0$ 是 $f(z)$ 的 $n$ 级极点, 则
\[\mathrm{Res}_{z=z_0}f(z)=\frac{\Phi^{(n-1)}(z_0)}{(n-1)!},\tag 2\]
其中 $\Phi(z)=(z-z_0)^nf(z)$
PoiquoteJS
