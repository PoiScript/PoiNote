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
\[\sum^n_{k=1}f(\zeta_k)\Delta z_k=\sum^n_{k=1}[u(\xi_k,\eta_k)]\]
