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
