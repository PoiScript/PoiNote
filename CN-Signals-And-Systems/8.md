#离散时间信号与系统的Z域分析
##I.离散时间信号的Z域分析
###i.引言
信号与系统的分析方法有 **时域,变换域** 两种。
####1.时域分析法
1. 连续时间信号与系统: 信号的时域运算，时域分解，经典时域分析法，近代时域分析法，**卷积积分**。
1. 离散时间信号与系统: 序列的变换与运算，**卷积和**，差分方程的求解。
####2.变换域分析法
1. 连续时间信号与系统: 信号与系统的频域分析、复频域分析。
1. 离散时间信号与系统: Z变换，DFT(FFT)(数字信号处理)。Z变换可将差分方程转化为代数方程。

**Z变换方法** 可以看成是 **拉氏变换** 的离散化形式。它们的唯一的区别：**拉氏变换** 用于 **连续时间** 信号和系统，而Z变换用于 **离散时间** 信号与系统。因此，Z变换具有和拉氏变换同等的地位和作用。
\[f[k]=f_s(t)=f(t)\cdot\delta_{T_s}(t)=\sum^{\infty}_{n=-\infty}f(nT_s)\delta(t-nT_s)\]
\[连续时间f(t)\xrightarrow{Nyquist抽样}离散时间\]
\[连续信号恢复f[k]通过一个截止频率为ω_c，放大倍数为T_s的低通滤波器\]
\[f(t)=f_s(t)* \frac{2\omega_c}{\omega_s}Sa(\omega_ct)=\frac{2\omega_c}{\omega_s}\sum^\infty_{n=-\infty}[f(nT_s)Sa(\omega_c(t-nT_s))]\]
###ii.理想取样信号的拉普拉斯变换
\[f_s(t)=f(t)\sum^\infty_{k=-\infty}\delta(t-kT)=\sum^\infty_{k=-\infty}f(kT)\delta(t-kT)\]
\[F_s(s)=L[f_s(t)]=\sum^\infty_{k=-\infty}f(kT)e^{-ksT}\]
\[L\{f_s(t)\}=\sum^\infty_{k=-\infty}f[k]z^{-k}=F(z)\]
\[S域到Z域的映射关系:z=e^{sT}\]
###iii.S平面与Z平面对应关系
\[s=\sigma+j\omega\Rightarrow{}z=e^s=e^{\sigma+j\omega}\Rightarrow{}|z|=e^\sigma\quad{}arg(z)=\omega\quad{}jIm[z]\]
s平面 $(s=\sigma+jω)$|z平面 $(|z|=e^\sigma;arg(z)=ω)$
:--:|:--:
虚轴 $(\sigma=0)$|单位圆 $(|z|=1)$
平行于虚轴的直线 $(σ=\sigma_0)$|圆 $(|z|=e^{\sigma_0})$
左半开平面 $(\sigma<0)$|单位圆内区域 $(|z|<1)$
右半开平面 $(\sigma>0)$|单位圆内区域 $(|z|>1)$
平行于虚轴的两条直线围成的区域 $(σ_1<σ<σ_2)$|圆环 $(e^{\sigma_1}<|z|<e^{\sigma_2})$
###iv.Z变换定义
####1.双边Z变换:
\[F(z)=\sum^\infty_{k=-\infty}f[k]z^{-k}\]
####2.Z反变换:
\[f[k]=\frac1{2\pi{}j}\oint_cF(z)z^{k-1}dz\quad{}C为F(z) 的ROC中的一闭合曲线\]
####3.单边Z变换:
\[F(z)=\sum^\infty_{k=0}f[k]z^{-k}\]
####4.物理意义:
将离散信号分解为不同频率复指数 $e^{sTk}$ 的线性组合
###v.Z变换的收敛域(ROC,region of convergence)
// TBD
####1.有限长序列
\[ROC:0<|z|<\infty\]
####2.右边序列
\[ROC:|z|>R_-\]
####3.因果序列
\[f[k]=\left\{\begin{aligned}f[k],k\geq0\\0,k<0\end{aligned}\right.\]
\[ROC:R_{x^-}<|z|\]
**因果序列** 的z变换必在 $\infty$ 处收敛 在 $\infty$ 处收敛的z变换，其序列必为 **因果序列**
####4.左边序列
\[ROC:|z|<R_+\leq\infty\]
####5.双边序列
\[ROC:R_-<|z|<R_+\]
序列的收敛大致有以下几种情况：
1. 对于有限长的序列，其双边Z变换在整个平面。
1. 对因果序列，其Z变换收敛域在某个圆外区域。
1. 对反因果序列，其Z变换收敛域在某个圆内区域。
1. 对双边序列，其Z变换收敛域为环状序列。

注意：对双边Z变换必须表明收敛域,否则其对应的原序列将不唯一。
###vi.常用序列的Z变换
####1.单位脉冲序列 $\delta[k]$
\[\mathscr{Z}\{\delta[k]\}=1\quad|z|\geq0\]
####2.单位阶跃序列 $u[k]$
\[\mathscr{Z}\{u[k]\}=\frac1{1-z^{-1}}=\frac{z}{z-1}\quad|z|>1\]
####3.指数序列 $a^ku[k]$
\[\mathscr{Z}\{a^ku[k]\}=\frac1{1-az^{-1}}\quad|z|>|a|\]
####4.复指数序列 $e^{j\Omega_0k}u[k]$
\[\mathscr{Z}\{e^{j\Omega_0k}u[k]\}=frac1{1-e^{j\Omega_0}z^{-1}}\]
####5.正弦序列 $\cos\Omega_0ku[k]$ 和 $\sin\Omega_0ku[k]$
\[\cos(\Omega_0k)u[k]\xrightarrow{\mathscr{Z}}\frac{1-\cos\Omega_0z^{-1}}{1-2z^{-1}\cos\Omega_0+z^{-2}}\]
\[\sin(\Omega_0k)u[k]\xrightarrow{\mathscr{Z}}\frac{\sin\Omega_0z^{-1}}{1-2z^{-1}\cos\Omega_0+z^{-2}}\]
###vii.单边Z变换的性质
####1.线性特性
\[af_1[k]+bf_2[k]\longleftrightarrow{}aF_1(z)+bF_2(z)\quad{}|z|>\max(R_{f_1},R_{f_2})\]
####2.位移特性
#####因果序列右移
\[f[k-n]u[k-n]\longleftrightarrow{}z^{-n}F(z)\quad{}ROC=R_f\]
#####非因果序列位移
\[f[k-m]u[k-m]\longleftrightarrow{}z^{-m}F(z)\quad{}ROC=R_f\]
\[f[k-m]u[k]\longleftrightarrow{}z^{-m}[F(z)+\sum^{-1}_{k=-m}f[k]z^{-k}]\quad{}ROC=R_f\]
\[f[k+m]u[k]\longleftrightarrow{}z^m[F(z)-\sum^{m-1}_{k=0}f[k]z^{-k}]\quad{}ROC=R_f\]
####3.指数加权特性
\[a^kf[k]u[k]\longleftrightarrow{}F\bigg(\frac{z}a\bigg)\quad{}ROC:|z|>|a|R_f\]
\[u[k]\longleftrightarrow\frac1{1-z^{-1}}\quad{}ROC:|z|>1\]
\[a^ku[k]\longleftrightarrow\frac1{1-(\displaystyle\frac za)^{-1}}\quad{}ROC:|\frac za|>1\]
\[a^ku[k]\longleftrightarrow\frac1{1-az^{-1}}\quad{}ROC:|z|>|a|\]
####4.Z域微分特性
\[kf[k]u[k]\longleftrightarrow-z\frac{dF(z)}{dz}\quad{}ROC:|z|>R_f\]
\[ku[k]\longleftrightarrow\frac{z^{-1}}{(1-z^{-1})}=\frac z{(z-1)^2}\quad{}|z|>1\]
\[\frac{dF(z)}{dz}=(\frac z{z-1})'=\frac{z-1-z}{(z-1)^2}=\frac{-1}{(z-1)^2}\]
\[ku[k]\longleftrightarrow-z\frac{dF(z)}{dz}=\frac z{(z-1)^2}\]
####5.序列卷积
\[\sum^k_{i=0}f[i]\longleftrightarrow\frac1{1-z^{-1}}F(z)\quad{}ROC:|z|>\max(R_f,1)\]
####6.序列求和特性
####7.初值与终值定理
##II.离散时间系统的Z域分析
###Z反变换
\[f[k]\frac1{2\pi{}j}\oint_cF(z)z^{k-1}dz\quad{}C为F(z)的ROC中的一闭合曲线\\=\sum_iRe\,s\{F(z)z^{k-1}\}\quad{}z_i为F(z)z^{k−1}在C中的极点\]
计算方法：
1. 留数计算法
1. 幂级数展开法(长除法)
1. 部分分式展开
###留数法
\[f[k]\frac1{2\pi{}j}\oint_cF(z)z^{k-1}dz=\sum_iRe\,s\{F(z)z^{k-1}\}\]
若 $F(z)z^{k−1}$ 在 $z=p_i$ 处有一阶极点，则该极点的留数为:
\[\underset{z=p_i}{Re}s[F(z)z^{k-1}]=(z-z_i)F(z)z^{k-1}\mid_{z=z_i}\]
若 $F(z)z^{k−1}$ 在 $z=p$ 处有N阶极点，则该极点的留数为:
\[\underset{z=p}{Re}s[F(z)z^{k-1}]=\frac1{(n-1)!}\bigg[\frac{d^{n-1}(z-p)^nF(z)}{dz^{n-1}}\bigg]_ {z=p}\]
###幂级数展开法(长除法)
因为 $f[k]$ 的 z变换定义为 $z^{-1}$ 的幂级数，即：
\[F(z)=\sum^\infty_{k=0}f[k]z^{-k}=f[0]z^0+f[1]z^{-1}+\cdots+f[k]z^{-k}+\cdots\]
所以，把 $F(z)$ 按 $z^{-1}$ 展成幂级数（通常是使用长除法），那么其系数组成的序列 $f[k]$ 即为所求。<br>
$F(z)$ 的形式与它的收敛域，才能惟一确定序列 $f[k]$。
\[F(z)=\frac{N(z)}{D(z)}=\frac{\displaystyle\sum^K_{n=1}a_nz^n}{\displaystyle\sum^R_{m=1}b_mz^m}\]
关键在于分子分母多项式按 $z(z^{-1})$ 幂的排序。
\[当收敛域R_{x^-}<|z|时,右边序列=\frac{z降幂(z-1升幂)}{z降幂(z-1升幂))}\]
### 部分分式法
\[F(z)=\frac{B(z)}{A(z)}=\frac{b_0+b_1z^{-1}+\cdots+b_mz^{-m}}{1+a_1z^{-1}+\cdots+a_nz^{-n}}\]
1. m≤n，分母多项式无重根:
\[F(z)=\sum^n_{i=1}\frac{r_i}{1-p_iz^{-1}}\]
各部分分式的系数为
\[r_i=(1-p_iz^{-1})F(z)\mid_{z=p_i}\]
2. m≤n，分母多项式在z=u处有l阶重极点
\[F(z)=\sum^{n-1}_{i=1}\frac{r_i}{1-p_iz^{-1}}+\sum^l_{i=1}\frac{q_i}{(1-uz^{-1})^i}\]
\[q_i=\frac1{(-u)^{l-i}(l-i)!}\frac{d^{l-i}}{d(z^{-1})^{l-i}}=[(1-uz^{-1})^lF(z)]\mid_{z=u},i=1,\cdots,l\]
3. m>n
\[F(z)=\underbrace{\sum^{m-n}_{i=1}k_iz^{-1}}_{多项式}+\underbrace{\frac{B_1(z^{-1})}{A(z^{-1})}}_{按1,2情况展开}\]
##III.离散时间系统函数与系统特性
##IV.离散时间系统的模拟
