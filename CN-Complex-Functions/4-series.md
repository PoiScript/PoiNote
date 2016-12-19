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
3. 既存在使级数收敛的正实数, 也存在使级数发散的正实数. 设 $z=\alpha(正实数)$ 时, 级数收敛, $z=\beta(正实数)$ 时, 级数发散, 那么在以原点为中心, $\alpha$ 为半径的圆周 $C_\alpha$ 内, 级数绝对收敛; 在以原点为中心, $\beta$ 为半径的圆周 $C_\beta$ 外, 级数发散. 显然 $\alpha<\beta$ 否则, 级数将在 $\alpha$ 处发散.
