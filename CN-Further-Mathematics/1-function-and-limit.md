#函数与极限
##I.映射与函数
###i.集合
####1.定义及表示法
#####(1).定义
1. 具有某种特定性质的事物的总体称为 **集合**.
1. 组成集合的事物称为 **元素**.
1. 不含任何元素的集合称为 **空集**,记作 $\varnothing$.
1. 元素 $a$ 属于集合 $M$, 记作 $a\in M$.
1. 元素 $a$ 不属于集合 $M$, 记作 $a\notin M$.

注: $M$ 为数集 $M^{* }$ 表示 $M$ 中排除 0 的集 ; $M^+$ 表示 $M$ 中排除 0 与负数的集 .
#####(2).表示法：
1. 列举法: 按某种方式列出集合中的全体元素.
1. 描述法: $M=\{x|所具有的特征\}$
1. 半开区间: $[a,b)=\{x|a\leq x<b\}$,$(a,b]=\{x|a<x\leq b\}$
1. 无限区间: $[a,+\infty)=\{x|a\leq x\}$,$(-\infty,b]=\{x|x\leq b\}$,$(-\infty,\infty)=\{x|x\in R\}$
1. 点的 $\delta$ 邻域: $\cup(a,\delta)=\{x|a-\delta<x<a+\delta\}=\{x||x-a|<\delta\}$
1. 去心 $\delta$ 邻域 $\cup(a,\delta)=\{x|0<|x-a|<\delta\}$ 其中, $a$ 称为邻域中心, $\delta$ 称为邻域半径.
1. 右 $\delta$ 邻域: $(a-\delta,a)$
1. 左 $\delta$ 邻域: $(a,a+\delta)$
####2.集合之间的关系及运算
设有集合 $A,B$, 若 $x\in A$, 必有 $x\in B$, 则称 $A$ 是 $B$ 的子集, 或称 $B$ 包含 $A$, 记作 $A\subset B$

若 $A\subset B$ 且 $B\subset A$, 则称 $A$ 与 $B$ 相等, 记作 $A=B$, 例如, $N\subset Z,Z\subset Q,Q\subset R$

显然有下列关系:
1. $A\subset A;A=A;\varnothing\subset A$
1. $A\subset B,B\subset C\Rightarrow A\subset C$

给定两个集合 $A,B$ 定义下列运算:
1. 并集: $A\cup B=\{x|x\in A或x\in B\}$
1. 交集: $A\cap B=\{x|x\in A且x\in B\}$
1. 差集: $A\setminus B=\{x|x\in A且x\notin B\}$
1. 余集: $B_A^c=A\setminus B(B\subset A)$
1. 直积: $A\times B=\{(x,y)|x\in A,y\in B\}$

特例: $R\times R\Rightarrow R^2$ 为平面上的全体点集
###ii.映射
####1.定义:
设 $X,Y$ 是两个非空集合, 若存在一个对应规则 $f$, 使得 $\forall x\in X$ 有唯一确定的 $y\in Y$ 与之对应，则称 $f$ 为从 $X$ 到 $Y$ 的映射, 记作 $f:Y\to X$

1. 元素 $y$ 称为元素 $x$ 在映射 $f$ 下的 **像**, 记作 $y=f(x)$
1. 元素 $x$ 称为元素 $y$ 在映射 $f$ 下的 **原像**.
1. 集合 $X$ 称为映射 $f$ 的定义域.
1. $Y$ 的子集 $f(X)=\{f(x)|x\in X\}$ 称为 $f$ 的 **值域**.

注意:
1. 映射的三要素: 定义域, 对应规则, 值域.
1. 元素 $x$ 的像 $y$ 是唯一的, 但 $y$ 的原像不一定唯一.

对映射 $f:X\to Y$, 若 $f(X)=Y$, 则称 $f$ 为 **满射**;

若 $\forall x_1,x_2\in X,x_1\neq x_2$, 有 $f(x_1)\neq f(x_2)$, 则称 $f$ 为 **单射**;

若 $f$ 既是满射又是单射,则称 $f$ 为 **双射** 或 **一一映射**.

映射又称为 **算子**. 在不同数学分支中有不同的惯用名称. 例如,
\[X(\neq\varnothing)\xrightarrow{f}Y(数集),f称为X上的泛函\]
\[X(\neq\varnothing)\xrightarrow{f}X,f称为X上的变换\]
\[X(数集或点集)\xrightarrow{f}R,f称为定义在X上的为函数\]
####2.逆映射与复合映射
#####(1).逆映射
######定义
若映射 $f:D\to f(D)$ 为单射, 则存在一新映射 $f^{-1}:f(D)\to D$使 $\forall y\in f(D)$ 其中 $f(x)=y$ 称此映射 $f^{-1}$ 为 $f$ 的逆映射 .

习惯上, $y=f(x),x\in D$ 的逆映射记成 $y=f^{-1}(x),x\in f(D)$
#####(2).复合映射
######定义
设有映射链
\[\forall x\in D\xrightarrow{g}u=g(x)\in g(D)\\\forall u\in D_1\xrightarrow{f}y=f(u)\in Y=f(D_1)\]
则当 $g(D)\subset D_1$ 时, 由上述映射链可定义由 $D$ 到 $Y$ 的复合映射, 记作 $y=f[g(x)]$ 或 $$
######注意:
构成复合映射的条件 $g(D)\subset D_1$ 不可少.以上定义也可推广到多个映射的情形.
###iii.函数
####1.函数的概念
#####定义
设数集 $D\subset R$, 则称映射 $f:D\to R$ 为定义在 $D$ 上的函数, 记为
\[y=f(x),x\subset D\]
\[\forall x\in D\xrightarrow{f}y\in f(D)=\{y|y=f(x),x\in D\}\]
1. 定义域 $f:D\to R$ 使表达式及实际问题都有意义的自变量集合.
1. 自变量 $x$
1. 因变量 $y$
1. 值域 $f(D)$
1. 对应规则 $f$ 对应规律的表示方法:解析法、图象法、列表法
####2.函数的几种特性
设函数 $y=f(x),x\in D$, 且有区间 $I\in D$
#####(1).有界性
$\forall x\in D$, 使 $|f(x)|\leq M$, 称 $f(x)$ 为有界函数.或称 $f(x)$ 在 $D$ 上有界.

说明:  还可定义有上界、有下界、无界
#####(2).单调性
$\forall x_1,x_2\in I,x_1,x_2$ 时,

当 $f(x_1)<f(x_2)$ 称 $f(x)$ 为 $I$ 上的单调增函数;

当 $f(x_1)>f(x_2)$ 称 $f(x)$ 为 $I$ 上的单调减函数.统称单调函数。
#####(3).奇偶性
$\forall x\in D$ 且有 $-x\in D$,

若 $f(-x)=f(x)$, 则称 $f(x)$ 为偶函数;

若 $f(-x)=-f(x)$ 则称 $f(x)$ 为奇函数.

**说明**: 若 $f(x)$ 在 $x=0$ 有定义, 则当 $f(x)$ 为 **奇函数** 时, 必有 $f(0)=0$
#####(4).周期性
$\forall x\in D,\exists l>0$, 且 $x\pm l\in D$ 若 $f(x\pm l)=f(x)$, 则称 $f(x)$ 为 **周期函数**, 称 $l$ 为 **周期**(一般指 **最小正周期**).

注: 周期函数 **不一定** 存在最小正周期.
####3.反函数与复合函数
#####(1).反函数的概念及性质
若函数 $f:D\to f(D)$ 为单射, 则存在逆映射 $f^{-1}:f(D)\to D$
称此映射 $f^{-1}$ 为 $f$ 的 **反函数**.

习惯上, $y=f(x),x\in D$ 的反函数记成 $y=f^{-1}(x),x\in f(D)$
######性质:
其反函数
1. $y＝f(x)$ 单调递增(减) 其反函数 $y=f^{-1}(x)$ 且也单调递增(减).
2. 函数 $y=f(x)$ 与其反函数 $y=f^{-1}(x)$ 的图形关于直线 $y=x$ 对称.
#####(2).复合函数: 复合映射的特例
设有函数链
\[①:y=f(u),u\in D_1\\②:u=g(x),x\in D,g(D)\subset D_1\]
则
\[y=f[g(x)],x\in D\]
称为由①, ②确定的复合函数,$u$ 称为 **中间变量**.

注意: 构成复合函数的条件 $g(D)\subset D_1$ 不可少.

两个以上函数也可构成复合函数.
####4.初等函数
#####(1).基本初等函数
幂函数, 指数函数, 对数函数, 三角函数, 反三角函数
#####(2).初等函数
由常数及基本初等函数经过有限次四则运算和复合步骤所构成,并可用一个式子表示的函数,称为 **初等函数**. 否则称为 **非初等函数**.
######非初等函数举例:
1. 符号函数
\[y=\text{sgn}x=\begin{cases}1&当x>0\\0&当x=0\\-1&当x<0\end{cases}\]
2. 取整函数
\[y=[x]=n,当n\leq x<n+1,n\in Z\]
##II.数列的极限
###i.数列极限的定义
定义:
自变量取正整数的函数称为 **数列**, 记作 $x_n=f(n)$ 或 $\{x_n\}$. $x_n$ 称为 **通项**(一般项).

若数列 $\{x_n\}$ 及常数 $a$ 有下列关系:
$\forall\varepsilon>0,\exists n\in N,当n>N时,总有|x_n-a|<\varepsilon$
则称该数列 $\{x_n\}$ 的极限为 $a$, 记作 $\displaystyle\lim_{n\to\infty}x_n=a$ 或 $x_n\to a(n\to\infty)$

此时也称数列 **收敛**, 否则称数列 **发散**.
###ii.收敛数列的性质
####1.收敛数列的极限唯一
**证**:用反证法.
1. 假设 $\displaystyle\lim_{n\to\infty}x_n=a$ 及 $\displaystyle\lim_{n\to\infty}x_n=b$, 且 $a<b$
2. 取 $\displaystyle\varepsilon=\frac{b-a}2$, 因 $\displaystyle\lim_{n\to\infty}x_n=a$, 故存在 $N_1$, 使当 $n>N_1$ 时, $|x_n-a|<\displaystyle\frac{a+b}2$, 从而 $x_n<\displaystyle\frac{a+b}2$
3. 同理, 因 $\displaystyle\lim_{n\to\infty}x_n=b$,故存在 $N_2$, 使当 $n>N_2$ 时, 有 $|x_n-b|<\displaystyle\frac{b-a}2$, 从而 $x_n>\displaystyle\frac{a+b}2$
4. $N=\max\{N_1,N_2\}$ 则当 $n>N$ 时, $x_n$ 满足的不等式矛盾.
5. 故假设不真! 因此收敛数列的极限必唯一.
####2.收敛数列一定有界.
**证**:
1. 设 $\displaystyle\lim_{n\to\infty}x_n=a$, 取 $\varepsilon=1$, 则 $\exists N$, 当 $n>N$ 时, 有 $|x_n-a|<1$
2. 从而有 $|x_n|=|(x_n-a)+a|\leq|x_n-a|+|a|<1+|a|$
3. 取 $M=\max\{|x_1|,|x_2|\cdots|x_n|,1+|a|\}$
4. 则有 $|x_n|\leq M(n=1,2\cdots)$
5. 由此证明收敛数列必有界.

**说明**: 此性质反过来不一定成立. 例如, 数列 $\{(-1)^{n+1}\}$ 虽有界但不收敛.
####3.收敛数列的保号性.
若 $\displaystyle\lim_{n\to\infty}x_n=a$, 且 $a>0(<0), \exists N\in N^+, n>N$ 时, 有 $x_n>0(<0)$

**证**:
1. 对 $a>0$, 取 $\varepsilon=\displaystyle\frac a2,\exists N\in N^+,n>N$
2. $|x_n-a|<\displaystyle\frac a2\Rightarrow x_n>a-\frac a2>0$

**推论**:
若数列从某项起 $x_n\geq0(\leq0),\displaystyle\lim_{n\to\infty}x_n=a,a\geq0(\leq0)$(用反证法证明)
####4.收敛数列的任一子数列收敛于同一极限.
**证**:
1. 设数列 $\{x_{n_k}\}$ 是数列 $\{x_n\}$ 的任一子数列.
2. 若 $\displaystyle\lim_{n\to\infty}x_n=a$ 则 $\forall\varepsilon>0,\exists N$, 当 $n>N$ 时, 有 $|x_n-a|<\varepsilon$
3. 现取正整数 $K$ , 使 $n_K\geq N$, 于是当 $k>K$ 时, 有 $n_k>n_K>N$
4. 从而有 $\displaystyle\left|x_{n_k}-a\right|<\varepsilon$, 由此证明 $\displaystyle\lim_{k\to\infty}x_{n_k}=a$

**说明**: 由此性质可知, 若数列有两个子数列收敛于不同的极限, 则原数列一定发散.

例如，$x_n=(-1)^{n+1}(n=1,2\cdots)$ 发散! $\displaystyle\lim_{k\to\infty}x_{2k-1}=1;\lim_{k\to\infty}x_{2k}=-1$
###iii.极限存在准则
####1.夹逼准则
\[\begin{cases}y_n\leq x_n\leq z_n(n=1,2\cdots)\\\displaystyle\lim_{n\to\infty}y_n=\lim_{n\to\infty}z_n=a\end{cases}\\\Rightarrow\lim_{n\to\infty}x_n=a\]
####2.单调有界准则
\[x_1\leq x_2\leq\cdots\leq x_n\leq x_{n+1}\leq\cdots\leq M\Rightarrow\lim_{n\to\infty}x_n=a(\leq M)\]
\[x_1\geq x_2\geq\cdots\geq x_n\geq x_{n+1}\geq\cdots\geq m\Rightarrow\lim_{n\to\infty}x_n=b(\geq m)\]
####3.柯西审敛准则(柯西审敛原理)
数列 $\{x_n\}$ 极限存在的充要条件是:
\[\forall\varepsilon>0,使当存在正整数N,使当m>N,n<N时,有|x_n-x_m|<\varepsilon\]
##III.函数的极限
###i.自变量趋于有限值时函数的极限
####1. $x\to x_0$ 时函数极限的定义
定义1.设函数 $f(x)$ 在点 $x_0$ 的某去心邻域内有定义, 若 $\forall\varepsilon>0,\exists\delta>0$, 当 $0<|x-x_0|<\delta$ 时, 有 $|f(x)-A|<\delta$，则称常数 $A$ 为函数时的极限, 记作:
\[\lim_{x\to x_0}f(x)=A或f(x)\to A(当x\to x_0)\]
即 $\displaystyle\lim_{x\to x_0}f(x)=A\leftrightarrow\forall\varepsilon>0,\exists\delta>0当x\in\mathring{U}(x_0,\delta)时,有|f(x)-A|<\varepsilon$
####2.保号性定理
#####定理1:
若 $\displaystyle\lim_{x\to x_0}f(x)=A$, 且 $A>0(A<0)$ 则存在常数 $\delta>0$, 使得当 $0<|x-x_0|<\delta$ 时, 有 $f(x)>0(或f(x)<0)$
#####推论:
若 $\displaystyle\lim_{x\to x_0}f(x)=A\neq0$, 则存在 $\mathring{U}(x_0,\delta)$, 使当 $x\in\mathring{U}(x_0,\delta)$ 时, 有 $|f(x)|>\displaystyle\frac{|A|}2$
#####定理2:
若在 $x_0$ 的某去心邻域内 $f(x)\geq0(f(x)\leq0)$, 且 $\displaystyle\lim_{x\to x_0}f(x)=A$, 则 $A\geq0(A\leq0)$
####3.左极限与右极限
#####左极限:
\[f(x_0^-)=\lim_{x\to x_0^-}f(x)=A\leftrightarrow\\\forall\varepsilon>0,\exists\delta>0当x\in(x_0-\delta,x_0)时,有|f(x)-A|<\varepsilon\]
#####右极限:
\[f(x_0^+)=\lim_{x\to x_0^+}f(x)=A\leftrightarrow\\\forall\varepsilon>0,\exists\delta>0当x\in(x_0,x_0+\delta)时,有|f(x)-A|<\varepsilon\]
#####定理3:
\[\lim_{x\to x_0}f(x)=A\leftrightarrow\lim_{x\to x_0^+}f(x)=\lim_{x\to x_0^-}f(x)=A\]
###ii.自变量趋于无穷大时函数的极限
#####定义2:
设函数 $f(x)$ 当 $|x|$ 大于某一正数时有定义，若 $\forall\varepsilon>0,\exists X>0使得当x满足不等式|x|>X时,对应的函数值f(x)都满足不等式|f(x)-A|<\varepsilon$ 则称常数 $A$ 为函数 $f(x)$ 当 $x\to\infty$ 的极限, 记作:
\[\lim_{x\to\infty}f(x)=A或f(x)\to A(当x\to\infty)\]
#####两种特殊情况:
\[\lim_{x\to+\infty}f(x)=A\leftrightarrow\\\forall\varepsilon>0,\exists X>当0,当x>X时,有|f(x)-A|<\varepsilon\]
\[\lim_{x\to-\infty}f(x)=A\leftrightarrow\\\forall\varepsilon>0,\exists X>当0,当x<-X时,有|f(x)-A|<\varepsilon\]
##IV.无穷小与无穷大
###i.无穷小
#####定义1
若 $x\to x_0(x\to\infty)$ 时, 函数 $f(x)\to0$ 则称函数 $f(x)$ 为 $x\to x_0(x\to\infty)$ 时的无穷小.

**说明**: 除 0 以外任何很小的常数都不是无穷小!
#####定理1(无穷小与函数极限的关系):
\[\lim_{x\to x_0}f(x)=A\leftrightarrow\\f(x)=A+\alpha,其中\alpha为x\to x_0时的无穷小量\]
###ii.无穷大
#####定义2
若任给 $M>0$, $\delta>0(正数X)$, 使对一切满足不等式 $0<|x-x_0|<\delta(|a|>X)$ 的 $x$, 总有 $|f(x)|>M$, 则称函数 $f(x)$ 当 $x\to x_0(x\to\infty)$ 时为无穷大, 记作
\[\lim_{x\to x_0}f(x)=\infty\Big(\lim_{x\to\infty}f(x)=\infty\Big)\]
若在定义中将 $|f(x)|>M$ 式改为 $f(x)>M(f(x)<-M)$, 则记作
\[\lim_{\substack{x\to x_0\\(x\to\infty)}}f(x)=+\infty\big(\lim_{\substack{x\to x_0\\(x\to\infty)}}f(x)=-\infty\big)\]
#####注意:
1. 无穷大不是很大的数, 它是描述函数的一种状态.
2. 函数为无穷大, 必定无界. 但反之不真!
###iii.无穷小与无穷大的关系
#####定理2:
在自变量的同一变化过程中

若 $f(x)$ 为无穷大, 则 $\displaystyle\frac1{f(x)}$ 为无穷小;

若 $f(x)$ 为无穷大, 且 $f(x)\neq0$, 则 $\displaystyle\frac1{f(x)}$ 为无穷小

**说明**: 据此定理, 关于无穷大的问题都可转化为无穷小来讨论.
##V.极限运算法则
###i.无穷小运算法则
#####定理1.
有限个无穷小的和还是无穷小.

**说明**: 无限个无穷小之和不一定是无穷小!
#####定理2.
有界函数与无穷小的乘积是无穷小.

**推论1**. 常数与无穷小的乘积是无穷小 .

**推论2**. 有限个无穷小的乘积是无穷小 .
###ii.极限的四则运算法则
#####定理3:
若 $\lim f(x)=A,\lim g(x)=B$, 则有
\[\lim[f(x)\pm g(x)]=\lim f(x)\pm\lim g(x)=A\pm B\]
**推论**: 若 $\lim f(x)=A,\lim g(x)=B$, 且 $f(x)\geq g(x)$, 则 $A\geq B$

**说明**: 定理 3 可推广到有限个函数相加、减的情形.
#####定理4:
若 $\lim f(x)=A,\lim g(x)=B$, 则有
\[\lim[f(x)g(x)]=\lim f(x)\lim g(x)=AB\]
**说明**: 定理 4 可推广到有限个函数相乘的情形.

**推论1**. $\lim[Cf(x)]=C\lim f(x)$ ($C$ 为常数)

**推论2**. $\lim[f(x)]^n=[\lim f(x)]^n$ ($n$ 为正整数)
#####定理5.
若 $\lim f(x)=A,\lim g(x)=B$, 且 $B\neq0$, 则有
\[\lim\frac{f(x)}{g(x)}=\frac{\lim f(x)}{\lim g(x)}=\frac AB\]
#####定理6.
若 $\displaystyle\lim_{n\to\infty}x_n=A,\lim_{n\to\infty}y_n=B$, 则有
\[\begin{cases}\displaystyle\lim_{n\to\infty}(x_n\pm y_n)=A\pm B
\\\displaystyle\lim_{n\to\infty}x_ny_n=AB
\\\displaystyle如果y_n\neq0,B\neq0,\lim_{n\to\infty}\frac{x_n}{y_n}=\frac AB\end{cases}\]
因为数列是一种特殊的函数, 故此定理 可由 定理3, 4, 5 直接得出结论 .

一般有如下结果:
\[\lim_{x\to\infty}=\frac{a_0x^m+a_1x^{m-1}+\cdots+a_m}{b_0x^m+b_1x^{n-1}+\cdots+b_n}(a_0b_0\neq0,m,n为非负常数)\\=
\begin{cases}\displaystyle\frac{a_0}{b_0}&n=m
\\0&n>m\\\infty&n<m\end{cases}\]
###iii.复合函数的极限运算法则
#####定理7.
设 $\displaystyle\lim_{x\to x_0}\phi(x)=a$, 且 $x$ 满足 $a<|x-x_0|<\delta_1$ 时, $\phi(x)\neq a$, 又 $\displaystyle\lim_{u\to a}f(u)=A$, 则有
\[\lim_{x\to x_0}f[\phi(x)]=\lim_{u\to a}f(u)=A\]
**说明**: 若定理中 $\displaystyle\lim_{x\to x_0}\phi(x)=\infty$ 则类似可得
\[\lim_{x\to x_0}f[\phi(x)]=\lim_{u\to\infty}f(u)=A\]
##VI.极限存在准则及两个重要极限
###i.函数极限与数列极限的关系及夹逼准则
####1.函数极限与数列极限的关系
#####定理1.
$\displaystyle\lim_{\substack{x\to x_0\\(x\to\infty)}}f(x)=A\leftrightarrow\forall\{x_n\}:x_n\neq x_0$, $f(x)$ 有定义, 且 $\underset{(x\to\infty)}{x_n\to x_0}$, 有 $\displaystyle\lim_{n\to\infty}f(x_n)=A$

**说明**: 此定理常用于判断函数极限不存在.
1. 找一个数列 $\{x_n\}:x_n\neq x_0,当x_n\to x_0(n\to\infty)时,\displaystyle\lim_{n\to\infty}f(x_n)不存在$
2. 找两个趋于 $x_0$ 的不同数列 $\{x_n\}$ 及 $\{x_n'\}$ 使 $\displaystyle\lim_{n\to\infty}f(x_n)\neq\lim_{n\to\infty}f(x_n')$
####2.函数极限存在的夹逼准则
#####定理2.
$当x\in\mathring{U}(x_0,\delta)时$, $g(x)\leq f(x)\leq h(x),(|x|>X>0)$ 且 $\displaystyle\lim_{\substack{x\to x_0\\(x\to\infty)}}g(x)=\lim_{\substack{x\to x_0\\(x\to\infty)}}h(x)=A$有:
\[\lim_{\substack{x\to x_0\\(x\to\infty)}}f(x)=A\]
###ii.两个重要极限
####1.$\displaystyle\lim_{x\to0}\frac{\sin x}x=1$
####2.$\displaystyle\lim_{x\to\infty}(1+\frac1x)^x=e$
说明: 此极限也可写为 $\displaystyle\lim_{z\to0}(1+z)^\frac1z=e$
##VII.无穷小的比较
####定义
设 $\alpha,\beta$ 是自变量同一变化过程中的无穷小,
1. 若 $\displaystyle\lim\frac\beta\alpha=0$, 则称 $\beta$ 是比 $\alpha$ **高阶** 的无穷小, 记作  $\beta=o(\alpha)$
1. 若 $\displaystyle\lim\frac\beta\alpha=\infty$, 则称 $\beta$ 是比 $\alpha$ **低阶** 的无穷小;
1. 若 $\displaystyle\lim\frac\beta\alpha=C\neq0$, 则称 $\beta$ 是 $\alpha$ 的 **同阶** 无穷小;
1. 若 $\displaystyle\lim\frac\beta{\alpha^k}=C\neq0$, 则称 $\beta$ 是关于 $\alpha$ 的 **$k$ 阶** 无穷小;
1. 若 $\displaystyle\lim\frac\beta\alpha=1$, 则称 $\beta$ 是 $\alpha$ **的等价** 无穷小, 记作 $\alpha\sim\beta$ 或 $\beta\sim\alpha$
####定理1
\[\alpha\sim\beta\leftrightarrow\beta=\alpha+o(\alpha)\]
证:
\[\alpha\sim\beta\Rightarrow\lim\frac\beta\alpha=1\\\Rightarrow\lim(\frac\beta\alpha-1)=0,即\lim\frac{\beta-\alpha}\alpha=0\\\Rightarrow\beta-\alpha=o(\alpha),即\beta=\alpha+o(\alpha)\]
####定理2
设 $\alpha\sim\alpha',\beta\sim\beta'$, 且 $\displaystyle\lim\frac{\beta'}{\alpha'}$ 存在, 则
\[\lim\frac\beta\alpha=\lim\frac{\beta'}{\alpha'}\]
证:
\[\lim\frac\beta\alpha=\lim(\frac\beta{\beta'}\frac{\beta'}{\alpha'}\frac{\alpha'}\alpha)\\=\lim\frac\beta{\beta'}\lim\frac{\beta'}{\alpha'}\lim\frac{\beta'}{\alpha'}=\lim\frac{\beta'}{\alpha'}\]
####说明:
设对同一变化过程, $\alpha,\beta$ 为无穷小, 由等价无穷小的性质, 可得简化某些极限运算的下述规则.
1. **和差取大规则**: 若 $\beta=o(\alpha)$, 有 $\alpha\pm\beta\sim\alpha$
2. **和差代替规则**: $\alpha\sim\alpha',\beta\sim\beta'\Rightarrow\alpha-\beta\sim\alpha'-\beta',\displaystyle\lim\frac{\alpha-\beta}\gamma=\lim\frac{\alpha'-\beta'}\gamma$
3. **因式代替规则**: $\alpha\sim\beta,\phi(x)存在或有界,则\lim\alpha\phi(x)=\lim\beta\phi(x)$
##IIX.函数的连续性与间断点
###i.函数连续性的定义
#####定义:
设函数 $y=f(x)$ 在 $x_0$ 的某邻域内有定义, 且 $\displaystyle\lim_{x\to x_0}f(x)=f(x_0)$ 则称函数 $f(x_0)$ 在 $x_0$ 连续

可见, 函数 $f(x)$ 在点 $x_0$ 连续必须具备下列条件:
1. $f(x)$ 在点 $x_0$ 有定义, 即 $f(x_0)$ 存在;
2. 极限 $\displaystyle\lim_{x\to x_0}=f(x)$ 存在;
3. $\displaystyle\lim_{x\to x_0}f(x)=f(x_0)$

若 $f(x)$ 在某区间上每一点都连续, 则称它在该区间上连续, 或称它为该区间上的 **连续函数** .

在闭区间 $[a,b]$ 上的连续函数的集合记作 $C[a,b]$.

对自变量的增量 $\Delta x=x-x_0$, 有 **函数的增量**
\[\Delta y=f(x)-f(x_0)=f(x_0+\Delta x)-f(x_0)\]
函数 $f(x)$ 在点 $x_0$ 连续有下列 **等价命题**:
\[\lim_{x\to x_0}f(x)=f(x_0)\Rightarrow\lim_{\Delta x\to0}f(x_0+\Delta x)=f(x_0)\\\Rightarrow\lim_{\Delta x\to0}\Delta y=0\Rightarrow\rlap{\overbrace{\phantom{f(x_0^-)=f(x_0)}}^{左连续}}f(x_0^-)=\underbrace{f(x_0)=f(x_0^+)}_{右连续}\\\Rightarrow\forall\varepsilon>0,\exists\delta>0,当|x-x_0|=|\Delta x|<\delta时,有|f(x)-f(x_0)|=|\Delta y|<\varepsilon\]
###ii.函数的间断点
设 $f(x)$ 在点 $x_0$ 的某去心邻域内有定义, 则下列情形之一时, 函数 $f(x)$ 在点 $x_0$ 不连续:
1. 函数 $f(x)$ 在 $x_0$ **无定义**;
2. 函数 $f(x)$ 在 $x_0$ 虽有定义, 但 $\displaystyle\lim_{x\to x_0}f(x)$ **不存在**;
3. 函数 $f(x)$ 在 $x_0$ 虽有定义, 且 $\displaystyle\lim_{x\to x_0}f(x)$ 存在, 但 $\displaystyle\lim_{x\to x_0}f(x)\neq f(x_0)$ 这样的点称为 **间断点**.
#####间断点分类:
######第一类间断点:
$f(x_0^-)$ 及 $f(x_0^+)$ 均存在,
1. 若 $f(x_0^-)=f(x_0^+)$, 称 $x_0$ 为 **可去间断点**.
2. 若 $f(x_0^-)\neq f(x_0^+)$, 称 $x_0$ 为 **跳跃间断点**.
######第二类间断点:
$f(x_0^-)$ 及 $f(x_0^+)$ 中至少一个不存在,
1. 若其中有一个为 $\infty$, 称 $x_0$ 为 **无穷间断点**.
2. 若其中有一个为振荡, 称 $x_0$ 为 **振荡间断点**.
##IX.连续函数的运算与初等函数的连续性
###i.连续函数的运算法则
#####定理1.
在某点连续的有限个函数经有限次和, 差, 积,商(分母不为0) 运算,结果仍是一个在该点连续的函数.(利用极限的四则运算法则证明)
#####定理2.
连续单调递增(递减)函数的反函数, 也连续单调递增(递减).
#####定理3.
连续函数的复合函数是连续的.
###ii.初等函数的连续性
1. 基本初等函数在定义区间内连续
2. 连续函数经四则运算仍连续
3. 连续函数的复合函数连续

一切初等函数在定义区间内都连续
##X.闭区间上连续函数的性质
###i.最值定理
#####定理1.
在 **闭区间** 上连续的函数,在该区间上一定有最大值和最小值.

即: 设 $f(x)\in C[a,b]$, 则 $\exists\xi_1,\xi_2\in[a,b]$ 使
\[f(\xi_1)=\min_{a\le x\le b}f(x)\\f(\xi_2)=\max_{a\le x\le b}f(x)\]
**注意**: 若函数在 **开区间** 上连续, 或在闭区间内有 **间断点**, 结论不一定成立.

**推论**: 在闭区间上连续的函数在该区间上有界.
###ii.介值定理
#####定理2(零点定理)
$f(x)\in C[a,b]$ 且 $f(a)f(b)<0$ 则至少有一点 $\xi\in(a,b)$, 使 $f(\xi)=0$
#####定理3(介值定理)
设 $f(x)\in C[a,b]$ 且 $f(a)=A,f(b)=B,A\ne B$, 则对 $A$ 与 $B$ 之间的任一数 $C$, 至少有一点 $\xi\in(a,b)$ 使 $f(\xi)=C$

**推论**: 在闭区间上的连续函数必取得介于最小值与最大值之间的任何值.
###iii.一致连续性
**定义**: 设函数 $f(x)$ 在区间 $I$ 上有定义, 如果对于任意给定的正数 $\varepsilon$, 总存在正数 $\delta$, 使得对于区间 $I$ 上任意两点 $x_1,x_2$, 当 $|x_1-x_2|<\delta$ 时, 有:
\[|f(x_1)-f(x_2)|<\delta\]
那么称函数 $f(x)$ 在区间 $I$ 上一致连续.

如果函数 $f(x)$ 在区间 $I$ 上一致连续, 那么 $f(x)$ 在区间 $I$ 上也是连续的.但放过来不一定成立.

**定理**: 如果函数 $f(x)$ 在闭区间 $[a,b]$ 上连续, 那么他在该区间上一定一致连续
