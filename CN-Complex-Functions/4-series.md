#级数
##I. 复数项级数
###i. 复数列的极限
设 $\{\alpha_n\}(n=1,2,\cdots)$ 为一复数列, 其中 $\alpha_n=a_n+ib_n$, 又设 $\alpha=a+ib$ 为一确定的复数. 如果任意给定 $\varepsilon>0$, 相应地能找到一个正数 $N(\varepsilon)$, 使 $|\alpha_n-\alpha|<\varepsilon$ 在 $n>N$ 时成立, 那么成为复数列 $\{\alpha_n\}$ 当 $n\to\infty$ 时的 **极限**, 记作:
\[\lim_{n\to\infty}\alpha_n=\alpha\]
此时也称复数列 $\{a_n\}$ **收敛** 于 $\alpha$.
####1. 定理1
复数列 $\{a_n\}(n=1,2,\cdots)$ 收敛于 $\alpha$ 的充要条件为
\[\lim_{n\to\infty}a_n=a\quad\lim_{n\to\infty}b_n=b\]
### ii.级数概念
设 $\{a_n\}=\{a_n+ib_n\}(n=1,2,\cdots)$ 为一复数列, 表达式
\[\sum_{n=1}^\infty\alpha_n=\alpha_1+\alpha_2+\cdots+\alpha_n+\cdots\]
称为 **无穷级数**, 其最前面 $n$ 项的和
\[s_n=\alpha_1+\alpha_2+\cdots+\alpha_n\]
称为级数的 **部分和**.

如果部分和数列 $\{s_n\}$ 收敛, 那么级数 $\displaystyle\sum_{n=1}^\infty\alpha_n$ 称为 **收敛**, 并且极限 $\displaystyle\lim_{n\to\infty}s_n=s$ 称为级数的 **和**, 如果级数 $\{s_n\}$ 不收敛, 那么级数 $\displaystyle\sum_{n=1}^\infty\alpha_n$ **发散**.
####定理二
级数 $\displaystyle\sum_{n=1}^\infty\alpha_n$ 收敛的充要条件是级数 $\displaystyle\sum_{n=1}^\infty a_n$ 和 $\displaystyle\sum_{n=1}^\infty b_n$ 都 **收敛**.

复数项级数 $\displaystyle\sum_{n=1}^\infty\alpha_n$ 收敛的必要条件是 $\displaystyle\lim_{n\to\infty}\alpha_n$
####定理三
如果 $\displaystyle\sum_{n=1}^\infty\left|\alpha_n\right|$ 收敛, 那么 $\displaystyle\sum_{n=1}^\infty\alpha_n$ 也收敛, 且不等式 $\displaystyle\left|\sum_{n=1}^\infty\alpha_n\right|\le\sum_{n=1}^\infty\left|\alpha_n\right|$ 成立.

如果 $\displaystyle\sum_{n=1}^\infty\left|\alpha_n\right|$ 收敛, 那么称级数 $\displaystyle\sum_{n=1}^\infty\alpha_n$ 为 **绝对收敛**, 非绝对收敛的收敛级数称为 **条件收敛级数**.
##II.幂级数
###1.幂级数的概念
设 $\{f_n(z)\}(n=1,2,\cdots)$ 为一复变函数序列, 其中各项在区域 $D$ 内有定义. 表达式
\[\sum_{n=1}^\infty f_n(z)=f_1(z)+f_2(z)+\cdots+f_n(z)+\cdots\]
称为 **复变函数项级数**. 记作 $\displaystyle\sum_{n=1}^\infty f_n(z)$. 这级数最前面 $n$ 项的和
\[s_n(z)=f_1(z)+f_2(z)+\cdots+f_n(z)+\cdots\]
$s(z)$ 称为级数 $\displaystyle\sum_{n=1}^\infty f_n(z)$ 的 **和函数**

当 $f_n(z)=c_{n-1}(z-a)^{n-1}$ 或 $f_n(z)=c_{n-1}z^{n-1}$ 时, 就得到函数项级数的特殊情况
\[\sum_{n=0}^\infty c_n(z-a)^n=c_0+c_1(z-a)+c_2(z-a)^2+\cdots+c_n(z-a)^n+\cdots\]
或
\[\sum_{n=0}^\infty c_nz^n=c_0+c_1z+c_2z^2+\cdots+c_nz^n+\cdots\]
这种级数称为 **幂级数**
####定理一(阿贝尔Abel定理)
如果级数 $\displaystyle\sum_{n=0}^\infty c_nz^n$ 在 $z=z_0(\ne0)$ 收敛, 那么对满足 $|z|<|z_0|$ 的 $z$, 级数必绝对收敛. 如果在 $z=z_0$ 级数发散, 那么对满足 $|z|>|z_0|$ 的 $z$, 级数必发散
###2.收敛圆与收敛半径
一个幂级数的收敛情况有3种:
1. 对所有的正实数都是收敛的, 这时, 根据阿贝尔定理可知级数在复平面内处处绝对收敛.
2. 对所有的正实数除 $z=0$ 外都是发散的, 这时, 级数在复平面内除原点外处处发散.
3. 既存在使级数收敛的正实数, 也存在使级数发散的正实数. 设 $z=\alpha(正实数)$ 时, 级数收敛, $z=\beta(正实数)$ 时, 级数发散, 那么在以原点为中心, $\alpha$ 为半径的圆周 $C_\alpha$ 内, 级数绝对收敛; 在以原点为中心, $\beta$ 为半径的圆周 $C_\beta$ 外, 级数发散. 显然 $\alpha<\beta$ 否则, 级数将在 $\alpha$ 处发散. 发散和收敛区域的边界的圆周 $C_R$ 称为幂级数的收敛圆. 在收敛圆的内部, 级数绝对收敛; 在收敛圆的外部, 级数发散. 收敛圆的的半径 $R$ 称为 收敛半径. 对幂级数来说, 它的收敛范围是以 $z=a$ 为中心的圆域. 在收敛圆的圆周上是收敛还是发散, 不能作出一般的结论, 要对具体级数进行具体分析.
###3.收敛半径的求法
####定理二(比值法)
如果 $\displaystyle\lim_{n\to\infty}\left|\frac{c_{n+1}}{c_n}\right|=\lambda\ne0$, 那么收敛半径 $R=\displaystyle\frac1\lambda$
####定理三(根值法)
如果 $\displaystyle\lim_{n\to\infty}\sqrt[n]{|c_n|}=\mu\ne0$, 那么收敛半径 $R=\displaystyle\frac1\mu$
###4.幂级数的运算和性质
像实变幂级数一样, 复变幂级数也能进行有理运算. 具体来说
\[f(z)=\sum_{n=0}^\infty a_nz^n,R=r_1,g(z)=\sum^\infty_{n=0}b_nz^n,R=r_2\]
那么在以原点为中心, $r_1,r_2$ 钟较小的一个为半径的院内的圆内, 这两个幂级数可以像多项式那样进行相加, 相减, 相乘与积. 在各种情况, 所得到的幂级数的收敛半径大于或等于 $r_1$ 与 $r_2$ 中较小的一个. 也就是
\[f(z)\pm g(z)=\sum^\infty_{n=0}a_nz^n\pm\sum^\infty_{n=0}b_nz^n=\sum^\infty_{n=0}(a_n\pm b_n)z^n,|z|<R\\f(z)g(z)=\left(\sum^\infty_{n=0}a_nz^n\right)\left(\sum^\infty_{n=0}b_nz^n\right)\\=\sum^\infty_{n=0}(a_nb_0+a_{n-1}b_1+a_{n-2}b_1+\cdots+a_0b_n)z^n,|z|<R\]
这里 $R=\max(r_1,r_2)$
####定理四
设幂级数 $\displaystyle\sum^\infty_{n=0}c_n(z-z_0)^n$ 的收敛半径为 $R$, 那么

**1**.它的和函数 $f(z)$, 即
\[f(z)=\sum^\infty_{n=0}c_n(z-a)^n\]
是收敛圆: $|z-a|<R$ 内的解析函数.

**2**.$f(z)$ 在收敛圆内的导数可将其幂级数逐项求导得到, 即
\[f'(z)=\sum^\infty_{n=1}nc_n(z-a)^{n-1}\]

**3**.$f(z)$ 在收敛圆内可以逐项积分, 即
\[\int_Cf(z)dz=\sum^\infty_{n=0}c_n\int_C(z-a)^ndz,C\in|z-a|<R\]
或
\[\int_a^zf(\xi)d\xi=\sum^\infty_{n=0}\frac{c_n}{n+1}(z-a)^{n+1}\]
