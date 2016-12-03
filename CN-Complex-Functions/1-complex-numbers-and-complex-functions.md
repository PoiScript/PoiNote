#复数与复变函数
##I.复数基本理论
###i.复数与复数域
####1.复数
每个复数具有 $z=x+iy$ 的形式，其中 $x$ 和 $y$ 是实数，$i$ 是虚数单位(-1的平方根)

$x$ 和 $y$ 分别称为 **实部** 和 **虚部**，分别记作:
\[x=\Re z\quad y=\Im z\]
复数的 **共轭** 定义为:
\[\overline{z}=x-iy\]
1. 如果 $\Im z=0$，则 $z$ 可以看成一个 **实数**；
1. 如果 $\Im z$ 不等于零，那么称 $z$ 为 **虚数**；
1. 如果 $\Im z$ 不等于零，而 $\Re z=0$，则称 $z$ 为 **纯虚数**。

注意：
0即是实数也是纯虚数 $0=0+0i$

两个复数相等指它们的 **实部与虚部分别相等**。
####2.复数的四则运算
复数的 **四则运算定** 义为:
\[(a_i+ib_1)\pm(a_2+ib_2)=(a_1\pm a_2)+i(b_1\pm b_2)\]
\[(a_i+ib_1)(a_2+ib_2)=(a_1a_2-b_1b_2)+i(a_1b_2+a_2b_1)\]
\[\frac{(a_1+ib_1)}{(a_2+ib_2)}=\frac{a_1a_2+b_1b_2}{a^2_2+b^2_2}+i\frac{a_2b_1-a_1b_2}{a_2^2+b^2_2}\]
复数在四则运算这个 **代数结构** 下，构成一个复数域(对加、减、乘、除运算封闭)，记为 $C$。复数域可以看成 **实数域的扩张**。

容易验证:
\[\overline{\overline{z}}=z\quad\overline{z}z=x^2+y^2\\z+\overline{z}=2x=2\Re z\quad z-\overline{z}=2iy=2i\Im z\\\overline{z_1+z_2}=\overline{z_1}+\overline{z_2}\quad\overline{z_1z_2}=\overline{z_1}\,\overline{z_2}\quad\overline{\left(\frac{z_1}{z_2}\right)}=\frac{\overline{z_1}}{\overline{z_2}}\]
####3.复数的几何表示
在 **平移关系** 下

复数可以等同于平面中的向量等价类
####4.非零复数的三角表示
向量的长度称为复数的 **模**, 定义为：
\[\rho=|z|=\sqrt{a^2+b^2}\]
非零复数与实轴正向之间的夹角称为复数的 **辐角**，记为 **$\mathrm{Arg}z$**
\[\vec z=|z|(\cos\mathrm{Arg}z+i\sin\mathrm{Arg}z)=\rho(\cos\theta+\sin\theta)\]
注意：几个 **重要不等式**
1. $|z_1+z_2|\leq|z_1|+|z_2|$
1. $|z_1-z_2|\geq|z_1|-|z_2|$
1. $||z_1|-|z_2||\leq|z_1+z_2|\leq|z_1|+|z_2|$
1. $||z_1|-|z_2||\leq|z_1-z_2|\leq|z_1|+|z_2|$
1. $|\Re z|\leq|z|\quad|\Im z|\leq|z|$
\[\mathrm{Arg}z(z\neq0)=\begin{cases}\arctan\displaystyle\frac yx&x>0,y\gtreqqless0\\\displaystyle\pm\frac\pi2&x=0,y\gtrless0\\\displaystyle\arctan\frac yx\pm\pi&x<0,y\gtrless0\\\pi&x<0,y=0\end{cases}\\其中-\frac\pi2<\arctan\frac yx<\frac\pi2\]
1. 当 $z$ 落于第一四象限时，不变。
1. 当 $z$ 落于第二象限时，加 $\pi$。
1. 当 $z$ 落于第三象限时，减 $\pi$。
#####三角表示的乘除法
\[z_1=|z_1|(\cos \mathrm{Arg}z_1+i\sin \mathrm{Arg}z_1)\\z_2=|z_2|(\cos \mathrm{Arg}z_2+i\sin \mathrm{Arg}z_2)\]
\[z_1z_2=|z_1||z_2|\big[\cos(\mathrm{Arg}z_1+\mathrm{Arg}z_2)+i\sin(\mathrm{Arg}z_1+\mathrm{Arg}z_2)\big]\]
\[|z_1z_2|=|z_1||z_2|\quad\mathrm{Arg}(z_1z_2)=\mathrm{Arg}z_1+\mathrm{Arg}z_2\]
其中后一个式子应理解为 **集合相等**

两个复数 **乘积的模** 等于它们的 **模相乘**，两个复数 **乘积的辐角** 等于它们的 **辐角相加**。

几何意义: 将复数 $z_1$ 按逆时针方向旋转一个角度 $\mathrm{Arg}z_2$，再将其伸缩到 $|z_2|$ 倍。

同理，对除法，也有：
\[z_1/z_2=|z_1|/|z_2|\big[\cos(\mathrm{Arg}z_1-\mathrm{Arg}z_2)+i\sin(\mathrm{Arg}z_1-\mathrm{Arg}z_2)\big]\]
即
\[|z_1/z_2|=|z_1|/|z_2|\quad\mathrm{Arg}(z_1/z_2)=\mathrm{Arg}z_1-\mathrm{Arg}z_2\]
其中后一个式子也应理解为 **集合相等**。

两个复数的 **商的模** 等于它们的 **模的商**，两个复数的 **商的辐角** 等于被除数与除数的 **辐角之差**。
#####三角表示的乘幂
\[z^n=|z|^n(\cos n\mathrm{Arg}z+i\sin n\mathrm{Arg}z)\]
\[z^{-n}=\frac1{z^n}\Rightarrow z^{-n}=|z|^{-n}\big[\cos(-n \mathrm{Arg}z)+i\sin(-n \mathrm{Arg}z)\big]\]
**棣模佛(De Moivre)公式**:
\[(\cos\theta+i\sin\theta)^n=\cos n\theta+i\sin n\theta\]
进一步，有:
\[z^{\frac1z}=\sqrt[n]{|z|}\big[\cos(\frac1n\mathrm{Arg}z)+i\sin(\frac1n\mathrm{Arg}z)\big]\\=\big[\cos(\frac1n\mathrm{arg}z+\frac{2\pi k}n)+i\sin(\frac1n\mathrm{arg}z+\frac{2\pi k}n)\big]\]
可以看到，$k=0,1,2,\cdots,n-1$ 时，可得n个不同的值，即 $z$ 有n个n次方根，其 **模相同**，**辐角相差一个常数**，**均匀分布** 于一个圆上。$k$ 取其它整数时，这些根又会 **重复出现**。
###ii.复球面与无穷大
####1.南极北极的定义
取一个与复平面切于原点 $z=0$ 的球面, 球面上的一点 $S$ 于原点重合, 通过 $S$ 作垂直于复平面的直线与球面相交与另一点 $N$, 我们称 $N$ 为北极, $S$ 为南极
####2.复球面的定义
对复平面内任一点 $P$ , 用直线将 $P$ 与 $N$ 相连, 与 **球面相交** 于 $Q$ 点(球极投影)

球面上的点，除去北极 $N$ 外，都和复平面上的点之间存在 **一一对应** 的关系。我们规定: 复数中有一个唯一的 **"无穷大"** 与复平面上的无穷远点相对应, 记作 $\infty$。**球面上的北极** $N$ 就是 **复数无穷大** $\infty$ 的 **几何表示**。

球面上的每一个点都有 **唯一的复数** 与之对应, 这样的球面称为 **复球面**
####3.扩充复平面的定义
**不包括** 无穷远点在内的复平面称为 **有限复平面**, 或简称 **复平面**，记作 $C$

包括无穷远点在内的复平面 $C\cup\{\infty\}$ 称为 **扩充复平面**，记作 $C_\infty$。
#####复球面的优越处:
能将扩充复平面的 **无穷远点** 明显地表示出来.

对于复数 $\infty$ 来说, 实部,虚部,辐角等概念均 **无意义**；模规定为 **正无穷大**，即 $|z|=+\infty$

与有限复数的基本运算为:
\[a\pm\infty=\infty\pm=\infty\\a\cdot\infty=\infty\cdot a=\infty(a\neq0)\\\frac a0=\infty(a\neq0)\quad\frac a\infty=0(a\neq0)\]
这些运算也无意义: $\infty\pm\infty,0,a\cdot\infty,\frac\infty\infty$
##II.复变函数
###i.复变函数的概念
设 $G$ 是一个复数的集合，$z=x+iy$。如果有一个 **确定的法** 则存在，使得按照这一法则，对于集合 $G$ 中的每一个复数 $z$，都有确定的（一个或几个）复数 $w=u+iv$ **与之对应**，则称复变数 $w$ 是复变数 $z$ 的 **函数**(简称 **复变函数**)，记作

集合 $G$ 称为 $f(z)$ 的 **定义域**, 对应于 $G$ 中所有 $z$ 对应的一切 $w$ 值所成的集合 $G^{* }$, 称为 **值域**。

如果 $z$ 的一个值对应着 $w$ 的一个值, 则函数 $f(z)$ 是 **单值** 的；否则就是 **多值** 的

在以后的讨论中, 定义集合 $G$ 常常是一个 **平面区域**,称之为 **定义域**, 并且, 如无特别声明, 所讨论的函数均为 **单值函数**。
#####与实变函数的关系:
一个复变函数相当于 **一对** **二元** 实变函数
\[u=u(x,y)\quad v=v(x,y)\]
###ii.复变函数的极限
####定义
设函数 $w=f(z)$ 定义在 $z_0$ 的 **去心邻域** $0<|z-z_0|<p$ 内 如果有一确定的数 $A$ 存在, 对于任意给定的 $\varepsilon>0$ 相应地必有一正数 $\delta(\varepsilon)(0<\delta\leq p)$ 使得当 $0<|z-z_0|<\delta$ 时有
\[|f(z)-A|<\varepsilon\]
那么称 $A$ 为 $f(z)$ **当 $z$ 趋近于 $z_0$ 时的极限**, 记作 $\displaystyle\lim_{z\to z_0}f(z)=A$ 或者记作当 $z\to z_0$ 时 $f(z)\to A$

应当注意, 定义中 $z$ 趋向于 的方式时 **任意的**, 就是说, 无论 $z$ 从什么方向 以何种方式趋向于 $z_0$, $f(z)$ 都是要趋向于 **同一个常数** $A$ 这比一元实变函数的极限定义要求 **苛刻** 得多
####几何意义
当变点 $z$ 一旦进入 $z_0$ 的充分小的 $\delta$ 去心邻域时 它的象点 $f(z)$ 就落入 $A$ 的预先给定的 $\varepsilon$ 邻域中, 跟一元实变函数的极限的几何意义相比十分类似 只是这里用 **圆形** 的邻域代替了那里的邻区
####定理
1. 设 $f(z)=u(x,y)+iv(x,y),\,A=u_0+iv_0,\,z_0=x_0+iy_0$ 那么 $\displaystyle\lim_{z\to z_0}f(z)=A$ 的 **充分条件是**
\[\lim_{x\to x_0,y\to y_0}u(x,y)=u_0,\lim_{x\to x_0,y\to y_0}v(x,y)=v_0\]
2. 如果 $\displaystyle\lim_{z\to z_0}f(z)=A,\lim_{z\to z_0}g(z)=B$
\[\lim_{z\to z_0}\big[f(z)\pm g(z)\big]=A\pm B\]
\[\lim_{z\to z_0}\big[f(z)g(z)\big]=AB\]
\[\lim_{z\to z_0}\bigg[\frac{f(z)}{g(z)}\bigg]=\frac AB(B\neq0)\]
###iii.复变函数的连续性
####定义
如果 $\displaystyle\lim_{z\to z_0}f(z)=f(z_0)$ 那么我们就说 $f(z)$ 在 $z_0$ 处 **连续**, 如果 $f(z)$ 在区域 $D$ 内 **处处连续** 我们说 $f(z)$ 在 $D$ 内连续
####定理
1. 函数 $f(z)=u(x,y)+iv(x,y)$ 在 $z_0=x_0+iy_0$ 处连续的充要条件是 $u(x,y)$ 和 $v(x,y)$ 在 $(x_0,y_0)$ 处连续
1. 在 $z_0$ 连续的两个函数 $f(z)$ 与 $g(x)$ 的和, 差, 积, 商(分号在 $z_0$ 不为零)在 $z_0$ 处仍连续
1. 如果函数 $h=g(z)$ 在 $z_0$ 连续, 函数 $w=f(h)$ 在 $h_0=g(z_0)$ 连续,那么复合函数 $w=f[g(z)]$ 在 $z_0$ 连续

从上面的定理中, 我们可以推得有理整函数(多项式)
\[w=P(z)=a_0+a_1z+a_2z^2+\cdots+a_nz^n\]
对复平面所有的 $z$ 都是连续的, 而有理分式函数
\[w=\frac{P(z)}{Q(z)}\]
其中 $P(z)$ 和 $Q(z)$ 都是多项式, 在复平面内使分母不为零的点也是连续的.

函数 $f(z)$ 在曲线 $C$ 上 $z_0$ 点处连续的意义是指
\[\lim_{z\to z_0}f(z)=f(z_0),z\in C\]
在闭曲线或包括闭曲线端点在内的曲线段上连续的函数 $f(z)$, 在闭曲线上是有界的, 即存在一正整数 $M$, 在曲线上恒有
\[|f(z)|\leq M\]
