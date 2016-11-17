#非周期信号的频域分析
##I.连续非周期信号的频谱
###i.从傅里叶级数到傅里叶变换
周期为 $T_0$ 的周期信号的Fourier级数和Fourier系数 $C_n$ 分别为:
\[f_{T_0}(t)=\sum^\infty_{n=-\infty}C_ne^{jn\omega_0t}\quad
C_n=\frac1{T_0}\int^{T_0/2}_{-T_0/2}f_{T_0}(t)e^{-jn\omega_0t}dt\]
当 $T_0\to\infty$ 时, 周期信号就变成了非周期信号,即:
\[\lim_{T_0\to\infty}f_{T_0}(t)=f(t)\]
为防止 $T_0\to\infty$ 时, $C_n\to0$, 将原式定义为:
\[f(t)=\sum^\infty_{n=\infty}\frac{D_0}{T_0}e^{jn\omega_0t}\quad
D_0=\int^{T_0/2}_{-T_0/2}f(t)e^{-jn\omega_0t}dt(\omega_0=\frac{2\pi}{T_0})\]
**实例:** 周期为T宽度为τ 的周期矩形脉冲的Fourier系数为:
\[C_n=\frac{\tau A}TSa\Big(\frac{n\omega_0\tau}2\Big)\]
\[\therefore D_n=T_0C_n=\tau ASa(n\omega_0\tau/2)=\tau ASa(\omega\tau/2)\mid_{\omega=n\omega_0}\]
**谱线间隔** $\omega_0=2\pi/T_0$: 信号的周期 $T_0$ 越大, 其基谱 $\omega_0$ 就越小, 谱线则越密 反之 则越疏 当 **周期趋于无穷大** 时, **周期信号变为非周期信号**, 此时信号的谱线 **间隔趋于零**, 即 **离散频谱变为连续频谱**, 记 $\omega=n\omega_0$ 则 宽度为 $\tau$ 的非周期矩阵脉冲信号的频谱为:
\[F(j\omega)=\lim_{T_0\to\infty}D_n=\lim_{T_0\to\infty}T_0C_n=\tau ASa(\omega\tau/2)\]
对于任意的周期信号, 当 $T_0\to\infty,\Delta\omega=(n+1)\omega_0-n\omega_0=\omega_0=2\pi/T_0\to0,n\omega_0$成为连续变量, 用 $\omega$ 表示
\[傅里叶变换:F(j\omega)=\lim_{T_0\to\infty}D_n=\lim_{T_0\to\infty}\int^{T_0/2}_{-T_0/2}f(t)e^{-j\omega t}=\int^\infty_{-\infty}f(t)e^{-j\omega t}dt\]
**物理意义:** $F(jω)$ 是单位频率所具有的信号频谱，称之为非周期信号的 **频谱密度函数** ，简称 **频谱函数** 。
\[傅里叶反变换:f(t)=\lim_{T\to\infty}f_T(t)=\lim_{T\to\infty}\sum^\infty_{n=-\infty}C_ne^{jn\omega_0t}=\\\lim_{T\to\infty}\sum^\infty_{n=-\infty}\frac{2F(j\omega)\omega_0}{2\pi}e^{jn\omega_0t}=\frac1{2\pi}\int^\infty_{-\infty}F(j\omega)e^{j\omega t}d\omega\]
**物理意义:** 非周期信号可以分解为无数个频率为 $\omega$，复振幅为 $[F(j\omega)/2\pi]d\omega$ 的 **虚指数信号** $e^{j\omega t}$ 的线性组合。
###ii.周期和非周期信号频谱函数的区别
1. 周期信号的频谱为 **离散** 频谱，非周期信号的频谱为 **连续** 频谱。
1. 周期信号的频谱为 $C_n$ 的分布，表示每个谐波分量的 **复振幅**；非周期信号的频谱为 $F(j\omega)$ 的分布，$(F(j\omega)/2\pi)d\omega$ 表示合成谐波分量的复振幅, 所以也将 $F(j\omega)$ 称为 **频谱密度函数**
####两者关系:
\[F(j\omega)=\lim_{T_0\to\infty}T_0C_n\quad
C_n=\frac{F(j\omega)}{T_0}\mid_{\omega=n\omega_0}\]
###iii.狄里赫莱条件
狄里赫莱条件是充分不必要条件
1. 非周期信号在无限区间上 **绝对可积**
\[\int^\infty_{-\infty}|f(t)|dt<\infty\]
2. 在任意有限区间内，信号只有 **有限个最大值和最小值**。
2. 在任意有限区间内，信号仅有 **有限个不连续点**，且这些点必须是有限值。
###iv.非周期矩形脉冲信号的频谱分析
1. 非周期矩形脉冲信号的频谱是 **连续频谱**，其形状与周期矩形脉冲信号离散频谱的包络线相似。
1. 周期信号的 **离散频谱** 可以通过对非周期信号的 **连续频谱** 等间隔取样求得
1. 信号在 **时域有限**，则在频域将 **无限延续**。
1. 信号的频谱分量主要集中在 **零频到第一个过零点之间**，工程中往往将此宽度作为 **有效带宽**。
1. 脉冲宽度τ越窄，有限带宽越宽，高频分量越多。即信号信息量大、传输速度快，传送信号所占用的频带越宽。
##II.常见连续时间信号的频谱
###i.常见非周期信号的频谱(频谱密度)
####1.单边指数信号 $e^{-at}u(t),a>0$
\[F(j\omega)=\int^\infty_{-\infty}f(t)e^{-j\omega t}dt=\int^\infty_0e^{-at}e^{-j\omega t}dt=\frac1{a+j\omega}\]
\[幅度频谱:|F(j\omega)|=\frac1{\sqrt{a^2+\omega^2}}\quad
相位频谱:\phi(\omega)=-\arctan(\frac\omega{a})\]
####2.双边指数信号 $e^{-a|t|}$
\[F(j\omega)=\int^0_{-\infty}e^{-at}e^{-j\omega{}t}dt+\int^\infty_0e^{-at}e^{-j\omega{}t}dt=\frac1{a-j\omega}+\frac1{a+j\omega}=\frac{2a}{a^2+\omega^2}\]
\[幅度频谱:|F(j\omega)|=\frac{2a}{a^2+\omega^2}\quad
相位频谱:\phi(\omega)=0\]
####3.单位冲激信号 $\delta(t)$
根据取样特性有:
\[\mathscr{F}[\delta]=\int^\infty_{-\infty}f(t)e^{-j\omega t}dt=\int^\infty_{-\infty}\delta(t)e^{-j\omega t}dt=1\]
####4.直流信号 $f(t)=1,-\infty<t<\infty$
\[\because\delta(t)=\frac1{2\pi}\int^\infty_{-\infty}e^{j\omega t}d\omega\]
\[\mathscr{F}[1]=\int^\infty_{-\infty}1e^{-j\omega t}dt=2\pi\delta(\omega)\]
对照 **冲激、直流** 时频曲线可看出:
1. 时域持续越宽的信号，其频域的频谱越窄；
1. 时域持续越窄的信号，其频域的频谱越宽。
####5.符号函数信号 $sgn(t)$
符号函数定义:
\[sgn(t)=\begin{cases}-1,t<0\\0,t=0\\1,t>0\end{cases}\]
\[\mathscr{F}\Big[sgn(t)e^{-\sigma|t|}\Big]=\int^0_{-\infty}(-1)e^{at}\]
####6.单位阶跃信号u(t)
###ii.常见周期信号的频谱密度
####1.虚指数信号
####2.正弦型信号
####3.单位冲激串
##III.连续时间Fourier变换的性质
##IV.离散周期信号的频域分析
##V.离散非周期信号的频域分析
