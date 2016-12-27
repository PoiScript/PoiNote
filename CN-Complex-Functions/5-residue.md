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
