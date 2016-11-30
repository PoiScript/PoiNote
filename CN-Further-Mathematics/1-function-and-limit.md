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
#####(1).逆映射的定义
###iii.函数
