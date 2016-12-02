#连续周期信号的频域分析
##I.周期信号的傅里叶级数展开
1. 周期信号
\[f(t)=f(t+kT_0) (k=0,\pm1,\pm2,...)\]
满足上描述的最小 $T_0$ 为周期信号的 **基波周期** $\omega_0$ 为 **基波角频率**
2. 周期信号可以表示为 **三角波的线性组合**
\[f(t)=b_1\sin(\omega_0t)+b_2\sin(2\omega_0t)+b_3(3\omega_0t)+...\\=\sum^{\infty}_{n=0}b_n\sin(n\omega_0t)\quad\omega_0=2\pi/T_0\]
\[f(t)=\frac{a_0}{2}+\sum^{\infty}_{n=1}[a_n\cos(n\omega_0t)+b_n\sin(n\omega_0t)]\]
###连续信号的分解
####1.连续信号分解为 单位冲激信号 的线性组合
\[f(t)=\int^{\infty}_{-\infty}f(\tau)\delta(t-\tau)d\tau\]
利用单位冲激响应求解系统的输出信号
####2.连续信号分解为一系列 不同频率 的 三角波信号 或 复指数信号 的线性组合
\[f(t)=\frac{a_0}{2}+\sum^{\infty}_{n=1}[a_n\cos(n\omega t)+b_n\sin(n\omega t)]\]
\[f(t)=\sum^{\infty}_{n=-\infty}C_ne^{jn\omega_0t}\]
利用频域特性求解系统的输出信号及系统函数
###频率和频域
1. 频率: **物质** 在 **1秒** 内完成 **周期** 性变化的次数叫做频率。
1. 频域(frequency domain): 即 **频率域**，是指在对 **函数** 或 **信号** 进行分析时，分析其和频率有关部份，而不是和 **时间** 有关的部份。
1. 频域下的信号: 信号在频域下的图形（一般称为 **频谱** ）可以显示信号分布在哪些频率及其比例。信号在 **时域** 下的图形可以显示信号如何随着时间变化 。
###连续周期信号的频域分析
将信号表示为 **不同频率复指数分量** 的 **线性组合**

意义:
1. **从信号分析的角度** ，将信号表示为不同频率 **复指数分量** 的线性组合，为不同信号之间进行比较提供了途径。
1. **从系统分析角度** ，已知单频正弦信号激励下的响应，利用 **迭加特性** 可求得多个不同频率正弦信号同时激励下的总响应,而且每个正弦分量通过系统后的变化。
##II.傅里叶级数的基本性质
###i.周期信号的傅里叶级数展开
####1.傅里叶级数的引进
法国数学家 **傅里叶** 发现，任何周期函数都可以用 **正弦函数** 和 **余弦函数** 构成的无穷级数来表示，后世称为 **傅里叶级数**。

函数 $f(t)$ 可分解为无穷多项 **正交函数** 之和
####2.信号分解为正交函数
矢量正交与正交分解
#####矢量正交:
指矢量 $V_x=(V_{x1},V_{x2},V_{x3})$ 与 $V_y=(V_{y1},V_{y2},V_{y3})$ 的内积为0.
\[V_XY_X^T = \sum^{3}_{i=1}v_{xi}v_{yi}=0\]
#####正交矢量集:
指由 **两两正交的矢量** 组成的矢量集合

如 三维空间中，以矢量 $v_x=(2,0,0), v_y=(0,2,0), v_z=(0,0,2)$ 所组成的集合就是一个 **正交矢量集**，且完备。
#####信号正交与正交函数集:
1. **信号正交**:指矢量 $\phi_1(t)$ 与 $\phi_2(t)$ 在 $(t_1,t_2)$ 区间满足 $\displaystyle\int^{t_2}_{t_1}A(t)\phi_2^* (t)dt=0$ 则称 $\phi_1(t)$ 和 $\phi_2(t)$ 在区间 $(t_1,t_2)$ 内正交。
2. **正交函数集**：若n个函数 $\phi_1(t),\phi_2(t)\cdots\phi_n(t)$
构成一个函数的集，这些函数在区间 $(t_1,t_2)$ 内满足
\[\int^{t_2}_{t_1}\phi(t)\phi_j^* (t)dt=
   \begin{cases}
   0&i\neq j\\
   K\neq0&i=j\\
   \end{cases}\]
#####完备正交函数集:
如果在正交函数集 ${\phi_1(t),\phi_2(t)\cdots\phi_n(t)}$ 之外不存在函数 $\phi(t)(\neq0)$ 满足
\[\int^{t_2}_{t_1}\phi^*(t)\phi_i(t)dt=0(i=1,2,…,n)\]
则称此函数为 **完备正交函数集**<br>
例如：**三角函数集** $\{1, \cos(n\omega t), \sin(n\omega t), n=1,2,...\}$ **虚指数函数集** $\{e^{jn\omega t}, n=0,+-1,+-2,...\}$ 是典型的在区间 $(t_0, t_0+T)(T=2\pi/\omega)$ 上的完备正交函数集。

三角函数集 $\{1,\cos(n\omega t),\sin(n\omega t), \}$ 在 **一个周期内** 是一个完备的正交函数集。
\[\int^{T/2}_{-T/2}\cos(n\omega t)\sin(m\omega t)dt=0\]
\[\int^{T/2}_{-T/2}\cos(n\omega t)\cos(m\omega t)dt =\begin{cases}\displaystyle\frac T2,m=n\\
   0,m\neq n\end{cases}\]
\[\int^{T/2}_{-T/2}\sin(n\omega t)\sin(m\omega t)dt =\begin{cases}\displaystyle\frac T2&m=n\\
   0&m\neq n\end{cases}\]
####3. 傅里叶级数的三角形式
\[f(t)=\frac{a_0}{2}+\sum^{\infty}_{n=1}[a_n\cos(n\omega t)+b_n\sin(n\omega t)],\omega=2\pi/T\]
---
\[\int^{T/2}_{-T/2}f(t)\cos(k\omega t)dt\\=\int^{T/2}_{-T/2}\Big(\frac{a_0}2+\sum^\infty_{n=1}\big[a_n\cos(n\omega t)+b_n\sin(n\omega t)\big]\Big)\cos(k\omega t)dt=\frac T2a_k\]
\[a_n=\frac2T\int^{T/2}_{-T/2}f(t)\cos(n\omega t)dt\quad a_0=\frac2T\int^{T/2}_{-T/2}f(t)dt\]
---
\[\int^{T/2}_{-T/2}f(t)\sin(k\omega t)dt\\=\int^{T/2}_{-T/2}\Big(\frac{a_0}2+\sum^\infty_{n=1}\big[a_n\cos(n\omega t)+b_n\sin(n\omega t)\big]\Big)\sin(k\omega t)dt=\frac T2b_k\]
\[b_n=\frac2T\int^{T/2}_{-T/2}f(t)\sin(n\omega t)dt\quad b_0=\frac2T\int^{T/2}_{-T/2}f(t)\sin(0t)dt=0\]
---
\[f(t)=\frac{a_0}2+\sum^\infty_{n=1}\big[a_n\cos(n\omega t)+b_n\sin(n\omega t)\big]\quad\omega=2\pi\quad其中a_n a_b为傅里叶系数\]
\[a_n=\frac2T\int^{T/2}_{-T/2}\sin(n\omega t)dt\quad a_n是n的偶函数\]
\[b_n=\frac2T\int^{T/2}_{-T/2}\cos(n\omega t)dt\quad b_n是n的奇函数\]
#####纯余弦形式傅里叶级数
\[f(t)=\frac{A_0}2+\sum^\infty_{n=1}A_n\cos(n\omega t)+\xi_n\]
$A_n=\sqrt{a^n+b^n}$(n的偶函数) $\varphi=\arctan\bigg(\displaystyle\frac{-b_n}{a_n}\bigg)$ $a_n=A_n\cos\varphi_n\quad b_n=-A_n\sin\varphi_n\quad n=1,2\cdots$

周期信号可分解为 **直流分量** 和许多 **余弦分量**

$A_0/2$ 称为信号的 **直流分量**，$A_n\cos(n\omega_0 t+\varphi_n)$ 称为信号的 **n次谐波分量**
#####波形的对称性与谐波特性
\[a_n=\frac2T\int^{T/2}_{-T/2}f(t)\cos(n\omega t)dt\]
\[b_n=\frac2T\int^{T/2}_{-T/2}f(t)\sin(n\omega t)dt\]
1. $f(t)$ 为 **偶函数** $b_n=0$，展开式中 **只有直流项和余弦项**
1. $f(t)$ 为 **奇函数** $a_n=0$，展开式中 **只有正弦项**
1. $f(t)$ 为 **半波镜像信号** $f(t)=-f(t\pm T_0/2)$ 此时傅里叶级数中只含 **奇次谐波分量** $a_0=a_2=\cdots=b_0=b_2=\cdots=0$
1. $f(t)$ 为 **半波重叠信号** $f(t)=f(t\pm T_0/2)$ 此时傅里叶级数中只含 **偶次谐波分量** $a_1=a_3=\cdots=b_1=b_3=\cdots=0$
####4. 周期信号展开为傅里叶级数条件
周期信号 $f(t)$ 应满足 **Dirichlet条件**，即：
1. 在一个周期内 **绝对可积**，即满足 $\displaystyle\int^{T_0+t_0}_{t_0}|f(t)|dt$ 为有限值。
1. 在一个周期内只有 **有限个不连续点**；
1. 在一个周期内只有 **有限个极大值和极小值**。

注意：条件1为 **充分条件但不是必要** 条件 条件2,3是 **必要条件但不是充分** 条件
####5. 傅里叶级数的指数形式
傅里叶级数的n阶谐波 $a_n\cos(n\omega_0t)+b_n\sin(n\omega_0t)(n=1,2\cdots)$ 可以用指数形式表示:
\[\cos(n\omega_0t)=\frac12(e^{jn\omega_0t}+e^{-jn\omega_0t})\quad\sin(n\omega_0t)=-\frac j2(e^{jn\omega_0t}-e^{-jn\omega_0t})\]
\[f(t)=\frac{a_0}2+\sum^\infty_{n=1}\big[a_n\cos(n\omega_0t)+b_n\sin(m\omega_0t)\big]\]
\[=\frac{a_0}2+\sum^{\infty}_{n=1}(\frac{a_n-jb_n}2e^{jn\omega_0t}+\frac{a_n+jb_n}2e^{-jn\omega_0t})\]
\[C_0=\frac{a_0}2\quad C_n=\frac{a_n-jb_n}2\quad C_{-n}=\frac{a_n+jb_n}2\]
\[f(t)=\sum^\infty_{n=-\infty}C_ne^{jn\omega_0t}\quad C_n为复傅里叶系数\]
**三角形式** 的傅里叶级数含义比较明确，但运算常感不便，因而经常采用 **指数形式** 的傅里叶级数

连续时间周期信号可以用指数形式傅里叶级数表示为
\[f(t)=\sum^\infty_{n=-\infty}C_ne^{jn\omega_0t}\quad其中 C_n=\frac1{T_0}\int^{T_0}_0f(t)e^{-jn\omega_0t}dt\]
1. $n=0$ 这一项是一个常数，称为信号的 **直流分量**
1. $n=\pm1$ 的基波频率为  $\omega_0$，两项合起来称为信号的 **基波分量**
1. $n=\pm2$ 的基波频率为 $2\omega_0$，两项合起来称为信号的 **2次谐波分量**
1. $n=\pm n$ 的基波频率为 $N\omega_0$，两项合起来称为信号的 **N次谐波分量**
#####物理含义：
周期信号 $f(t)$ 可以分解为 **不同频率虚指数信号** 之和
###ii.傅里叶级数的基本性质
###1.线性特性
\[f_1(t)\to C_{1n}\quad f_2(t)\to C_{2n}\]
\[\Rightarrow a_1f_1(t)+a_2f_2(t)\to a_1C_{1n}+a_2C_{2n}\]
###2.时移特性
\[f(t)\to C_n\]
\[\Rightarrow f(t-t_0)\to e^{-jn\omega_0t_0}C_n\]
###3.卷积特性
$f1(t)$ 和 $f2(t)$ 均是周期为 $T_0$ 的周期信号，且
\[f_1(t)\to C_n\quad f_2(t)\to C_{2n}\]
\[\Rightarrow f_1(t)* f_2(t)\to T_0C_{1n}C_{2n}\]
###4.微分特性
\[f(t)\to C_n\Rightarrow f'(t)\to jn\omega_0C_n\]
##III.周期信号的频谱及其特点
###i.频谱的概念
从广义上说，信号的某种特征量(幅值、相位)随信号频率变化的关系，称为 **信号的频谱**，所画出的图形称为信号的频谱图。
###ii.周期信号的频谱
**周期信号的频谱** 是指周期信号中各次谐波幅值、相位随频率变化的关系，即<br>
将 $A_n\sim\omega$ 和 $\phi_n\sim\omega$ 的关系分别画在以 $\omega$ 为横坐标的平面上得到的两个图

分别称为 **幅度频谱图** 和 **相位频谱图**

因为 $n\geq0$，所以称这种频谱为 **单边谱**。

周期信号 $f(t)$ 可以分解为 **不同频率虚指数信号** 之和:
\[f(t) = \sum^{\infty}_{n=-\infty}C_ne^{jn\omega_0t}\]
不同的时域信号，只是 **傅里叶级数的系数** $C_n$ 不同，因此通过研究傅里叶级数的系数来研究信号的特性。<br>
$Cn$ 是频率的函数，它反映了组成信号各次谐波的幅度和相位随频率变化的规律，称 **频谱函数**。<br>
直接画出信号各次谐波对应的Cn线状分布图形，这种图形称为信号的 **频谱图** 。能够说明信号的频域特性。
#####双边频谱:
\[C_n=|C_n|e^{j\xi_n},C_n\to幅度频谱 j\omega_n\to相位频谱\]
#####单边频谱:
\[f(t)=\frac{A_0}{2}+\sum^{}_{n=1}A_n\cos(n\omega t)+\phi_n,幅度频谱\to A_n相位频谱\to\phi_n\]
###iii.频谱的特性
####1.离散频谱特性
周期信号的频谱是由 **间隔为 $\omega_0$** 的谱线组成的<br>
信号周期 $T$ 越大，$\omega_0$ 就越小，则谱线越密，谱线幅度降低，但对振幅收敛性无影响。反之，$T$ 越小，$\omega_0$ 越大，谱线则越疏
####2 幅度衰减特性(收敛性)
一般当周期信号的幅度频谱随着 **谐波 $n\omega_0$ 增大** ，幅度频谱 **$|C_n|$ 不断衰减** ，并最终趋于零<br>
谱线与波形参数之间的关系：
1. $T$ 一定，$\tau$ 变小，此时谱线间隔 $\omega_0$ 不变，两零点之间的谱线数目: $\omega/\omega_0 = (2\pi/\tau)/(2\pi/T)=T/\tau$ 增多。
1. $\tau$ 一定，$T$ 增大，间隔 $\omega_0$ 减小，频谱变密，幅度减小。
1. $T$ 趋于无穷大时，间隔趋于0，频谱变为连续谱。
####3.信号的有效带宽
$0\sim2\pi/\tau$ 这段频率范围称为周期矩形脉冲信号的 **有效频带宽度** ,即
\[\omega_B=\frac{2\pi}\tau\]
信号的有效带宽与信号时域的持续时间成反比。<br>
即  越大，其 $\omega_B$ 越小；反之， 越小，其 $\omega_B$ 越大。<br>
信号的有效带宽有多种定义方式。
#####物理意义:
在信号的有效带宽内，集中了信号绝大部分谐波分量。若信号丢失有效带宽以外的谐波成分，不会对信号产生明显影响。

说明：当信号通过系统时，信号与系统的有效带宽必须“匹配”。
##IV.周期信号的功率谱
###i.周期信号的功率谱
####帕什瓦尔(Parseval)功率守恒定理:
\[P=\frac{1}{T}\]
####物理意义:
任意周期信号的 **平均功率** 等于信号所包含的直流和n次谐波分量在1欧电阻上消耗的 **平均功率之和**。
####周期信号的功率频谱:
$|C_n|^2$ 随 $n\omega_0$ 分布情况称为周期信号的功率频谱，简称 **功率谱**<br>
###ii. 吉伯斯（Gibbs）现象
用有限次谐波分量来近似原信号，在不连续点出现过冲，过冲峰值 **不随谐波分量增加而减少**，且 为跳变值的 **9%**。
####吉伯斯现象产生原因
时间信号存在跳变破坏了信号的 **收敛性**，使得在间断点傅里叶级数出现 **非一致收敛**。
##V.总结:
分析问题使用的数学工具为 **傅里叶级数**

最重要概念：**频谱函数**

要点
1. 频谱的定义、物理意义
2. 频谱的特点
3. 频谱的性质，应用性质分析复杂信号的频谱
4. 功率谱的概念
