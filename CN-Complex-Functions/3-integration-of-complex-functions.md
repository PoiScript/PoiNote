#复变函数的积分
##I.复变函数积分的概念
###i.积分的定义
####1.有向曲线
设 $C$ 为平面上给定的一条光滑(或按段光滑)曲线. 如果设定 $C$ 的两个可能方向中的一个作为正方向(或正向), 那么我们就把 $C$ 理解为带方向的曲线, 称为 **有向曲线**.
####2.积分定义
设函数 $w=f(z)$ 定义在区域 $D$内，$C$ 为在区域 $D$ 内起点为 $A$ 终点为 $B$ 的一条光滑的有向曲线, 把曲线 $C$ 任意分成 $n$ 个弧段, 设分点为:
\[A=z_0,z_1,\cdots,z_{k-1},\cdots,z_n=B\]
在每个弧段 $\widehat{z_{k-1}z_k}(k=1,2,\cdots,n)$ 上任取一点 $\zeta_k$, 并作和式:
\[S_n=\sum^n_{k=1}f(\zeta_k)(z_k-z_{k-1})=\sum^n_{k=1}f(\zeta_k)\Delta z_k\]
这里 $\Delta z_k=z_k-z_{k-1}$. 记 $\Delta s_k=\widehat{z_{k-1}z_k}$ 的长度, $\delta=\displaystyle\underset{1\le k\le n}{\max}\{\Delta s_k\}$. 当 $n$ 无限增加, 且 $\delta$ 趋于零时, 如果不论对 $C$ 的分法及 $\zeta_k$ 的取法如何, $S_n$ 有唯一极限, 那么称这极限值为函数沿曲线 $C$ 的积分, 记作
\[\int_Cf(z)dz=\lim_{n\to\infty}\sum^n_{k=1}f(\zeta_k)\Delta z_k\]
如果 $C$ 为闭曲线，那么沿此闭曲线的积分记作　$\displaystyle\oint_Cf(z)dz$

当 $C$ 是 $x$ 轴上的区间 $a\le x\le b$, 而 $f(z)=u(x)$ 是, 这个积分定义就是一元实变函数定积分的定义.
####3.积分存在条件及其计算法
设光滑曲线 $C$ 由参数方程
\[z=z(t)=x(t)+iy(t),\alpha\le t\le\beta\tag 1\]
给出, 正方向为参数增加方向, 参数 $\alpha$ 及 $\beta$ 对应与起点 $A$ 及终点 $B$, 并且 $z'(t)\ne0,\alpha<t<\beta$

如果 $f(z)=u(x,y)+iv(x,y)$ 在 $D$ 内处处连续, 那么 $u(x,y)$ 及 $v(x,y)$ 均为 $D$ 内的连续函数, 设 $\zeta_k=\xi_k+i\eta_k$, 由于
\[\Delta z_k=z_k-z_{k-1}=x_k+iy_k-(x_{k-1}+iy_{k-1})\\=(x_k-x_{k-1})+i(y_k-y_{k-1})=\Delta x_k+i\Delta y_k\]
所以:
\[\sum^n_{k=1}f(\zeta_k)\Delta z_k=\sum^n_{k=1}[u(\xi_k,\eta_k)+iv(\xi_k,\eta_k)](\Delta x_k+i\Delta y_k)\\=\sum^n_{k=1}[u(\xi_k,\eta_k)\Delta x_k-v(\xi_k,\eta_k)\Delta y]+i\sum^n_{k=1}[v(\xi_k,\eta_k)\Delta x_k+u(\xi_k,\eta_k)\Delta y_k\]
由于 $u,v$ 都是连续函数, 根据线积分的存在定理, 当 $n$ 无限增大而弧段长度的最大值趋于零时, 不论对 $C$ 的分法如何, 点 $(\xi_k,\eta_k)$ 的取法如何, 上式右端的两个和式的极限都是存在的 因此有
\[\int_Cf(z)dz=\int_Cudx-vdy+i\int_Cvdx+udy\]
上式可以看作: $f(z)=u+iv$ 与 $dz=dx+idy$ 的乘积求积分得到
1. 当 $f(z)$ 是连续函数而 $C$ 时光滑曲线时, 积分 $\int_Cf(z)dz$ 是一定存在的
1. $\int_Cf(z)dz$ 可以通过两个二元实变函数的线积分来计算
####4.积分的性质
1. $\displaystyle\int_Cf(z)dz=-\int_{C^-}f(z)dz$

1. $\displaystyle\int_Ckf(z)dz=k\int_Cf(z)dz(k为常数)$

1. $\displaystyle\int_C\left[f(z)\pm g(z)\right]dz=\int_Cf(z)dz\pm\int_Cg(z)dz$

1. 设曲线 $C$ 的长度为 $L$, 函数 $f(z)$ 在 $C$ 上满足 $|f(z)|\le M$, 那么
\[\left|\int_Cf(z)dz\right|\le\int_C\left|f(z)\right|ds\le ML\]
##II.柯西-古萨(Cauchy-Goursat)定理
如果函数 $f(z)$ 在单连通域 $B$ 内处处解析，那么函数 $f(z)$ 沿 $B$ 内的任一封闭曲线 $C$ 的积分为零:
\[\oint_Cf(z)dz=0\]
##III.基本定理的推广--复合闭路定理
设 $C$ 为多连通域 $D$ 内的一条简单闭曲线, $C_1,C_2,\cdots,C_n$ 是在 $C$ 内部的简单闭曲线, 它们互不包含也互不相交, 并且以 $C,C_1,C_2\cdots,C_n$ 为边界的区域全含于 $D$. 如果 $f(z)$ 在 $D$ 内解析, 那么
\[\oint_Cf(z)dz=\sum^n_{k=1}\oint_{C_k}f(z)dz\]
其中 $C$ 及 $C_k$ 均取正方向:
\[\oint_\Gamma f(z)dz=0\]
这里 $\Gamma$ 为由 $C$ 及 $C_k(k=1,2,\cdots,n)$ 所组成的复合闭路(其方向是: $C$ 按逆时针进行, $C_k^n$ 按顺时针进行)
##IV.原函数与不定积分
###i.定理一
如果函数 $f(z)$ 在单连通域 $B$ 内处处解析, 那么积分 $\displaystyle\int_Cf(z)dz$ 与连结起点及终点的路线 $C$ 无关.
###ii.定理二
如果 $f(z)$ 在单连通域 $B$ 内, 处处解析, 那么函数 $F(z)$ 比为 $B$ 内的一个解析函数, 并且 $F'(z)=f(z)$
###iii.定义
如果函数 $\varphi(z)$ 在区域 $B$ 内的导数等于 $f(z)$, 即 $\varphi'(z)=f(z)$ 那么称 $\varphi(z)$ 为 $f(z)$ 在区域 $B$ 内的原函数.

$f(z)$ 的原函数的一般表达式 $F(z)+c$(其中 $c$ 为任意常数) 为 $f(z)$ 的不定积分, 记作
\[\int f(z)dz=F(z)+c\]
###iv.定理三
如果 $f(z)$ 在单连通域 $B$ 内处处解析, $G(z)$ 为 $f(z)$ 的一个原函数, 那么
\[\int_{z_0}^{z_1}f(z)dz=G(z_1)-G(z_0)\]
这里的 $z_0,z_1$ 为域 $B$ 内的两点
##V.柯西积分公式
###i.定理
如果 $f(z)$ 在区域 $D$ 内处处解析, $C$ 为 $D$ 内的任何一条正向简单闭曲线, 它的内部完全含于 $D$, $z_0$ 为 $C$ 内任一点, 那么
\[f(z_0)=\frac1{2\pi i}\oint_C\frac{f(z)}{z-z_0}dz\]
如果 $f(z)$ 在区域边界上的值一经确定, 那么他在区域内部任一点处处的值也就确定.柯西积分公式不但提供了计算某些复变函数沿闭路积分的一种方法, 而且给出了解析函数的一个积分表达式

如果 $C$ 是圆周 $z=z_0+Re^{i\theta}$, 那么有
\[f(z_0)=\frac1{2\pi}\int_0^{2\pi}f(z_0+Re^{i\theta})d\theta\]
这就是说, 一个解析函数在圆心处的值等于他在圆周上的平均值
##VI.解析函数的高阶导数
###i.定理
解析函数 $f(z)$ 的导数任为解析函数, 它的 $n$ 阶导数为:
\[f^{(n)}(z_0)=\frac{n!}{2\pi i}\oint_C\frac{f(z)}{(z-z_0)^{n+1}}dz(n=1,2,\cdots)\]
其中 $C$ 为在函数 $f(z)$ 解析区域 $D$ 内围绕 $z_0$ 的任何一条正向简单闭曲线, 并且它的内部全含于 $D$

上式相当于把柯西积分公式的两边对 $z_0$ 求 $n$ 阶导数, 右边求导在积分号下进行, 求导时把被积函数看作是 $z_0$ 的函数, 而把 $z$ 看作常数

高阶导数公式的作用, 不在于通过积分来求导, 而在于通过求导来求积分
##VII.解析函数于调和函数的关系
###i.定义
如果二元实变函数 $\varphi(x,y)$ 在区域 $D$ 内具有二阶连续偏导数并且满足拉普拉斯方程
\[\frac{\partial^2\varphi}{\partial x^2}+\frac{\partial^2\varphi}{\partial y^2}=0\]
那么称 $\varphi(x,y)$ 为区域 $D$ 内的调和函数
###ii.定理
任何在区域 $D$ 内解析的函数, 它的实部和虚部都是 $D$ 内的调和函数

设 $u(x,y)$ 为区域 $D$ 内给定的调和函数, 把使 $u+iv$ 在 $D$ 内构成解析函数的调和函数 $v(x,y)$ 称为 $u(x,y)$ 的共轭调和函数, 即在 $D$ 内满足柯西黎曼方程
\[\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y},\frac{\partial v}{\partial x}=-\frac{\partial u}{\partial y}\]
