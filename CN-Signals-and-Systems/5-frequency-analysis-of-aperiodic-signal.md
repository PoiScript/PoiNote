#非周期信号的频域分析
##I.连续非周期信号的频谱
###i.从傅里叶级数到傅里叶变换
周期为 $T_0$ 的周期信号的Fourier级数和Fourier系数 $C_n$ 分别为:
\[f_{T_0}(t)=\sum^\infty_{n=-\infty}C_ne^{jn\omega_0t}\quad
C_n=\frac1{T_0}\int^{T_0/2}_{-T_0/2}f_{T_0}(t)e^{-jn\omega_0t}dt\]
当 $T_0\to\infty$ 时, 周期信号就变成了 **非周期信号**,即:
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
####6.单位阶跃信号 $u(t)$
\[u(t)=\frac12+\frac1{j\omega}sgn(t)\]
\[\mathscr{F}[u(t)]=\pi\delta(\omega)+\frac1{j\omega}\]
###ii.常见周期信号的频谱密度
####1.虚指数信号 $e^{j\omega_0t}(-\infty<t<\infty)$
\[\mathscr{F}[e^{j\omega_0t}]=\int^\infty_{-\infty}e^{-j(\omega-\omega_0)t}dt=2\pi\delta(\omega-\omega_0)\]
虚指数信号的频谱只有在 $\omega=\omega_0$ 处有一个冲激, 故称虚指数信号为 **单频信号**
####2.正弦型信号
\[\cos\omega_0t=\frac12(e^{j\omega_0t}+e^{-j\omega_0t})\xrightarrow{\mathscr{F}}\pi[\delta(\omega-\omega_0)+\delta(\omega+\omega_0)]\]
\[\sin\omega_0t=\frac1{2j}(e^{j\omega_0t}-e^{-j\omega_0t})\xrightarrow{\mathscr{F}}-j\pi[\delta(\omega-\omega_0)+\delta(\omega+\omega_0)]\]
####3.一般周期信号
\[f(t)=\sum^\infty_{n=-\infty}C_ne^{jn\omega_0t},\omega=\frac{2\pi}{T_0}\\两边进行Fourier变换\to
F(j\omega)=\mathscr{F}[\sum^{+\infty}_{n=-\infty}C_ne^{jn\omega_0t}]=\sum^{+\infty}_{n=-\infty}C_n\mathscr{F}[e^{jn\omega_0t}]\\
F(j\omega)=2\pi\sum^{+\infty}_{n=-\infty}C_n\delta(\omega-n\omega_0)\]
####4.单位冲激串 $\delta_{T_0}(t)$
定义:
\[\delta_{T_0}(t)=\sum^{+\infty}_{n=-\infty}\delta(t-nT_0),n\in Z\]
\[\delta_{T_0}=\sum^{+\infty}_{n=-\infty}\delta(t-nT_0)=\frac1{T_0}\sum^{+\infty}_{n=-\infty}e^{jn\omega_0t},\omega_0=2\pi/T_0\\两边进行Fourier变换\to F(j\omega)=\frac1{T_0}\sum^{+\infty}_{n=-\infty}2\pi\delta(\omega-n\omega_0)=\omega_0\sum^{+\infty}_{n=-\infty}\delta(\omega-n\omega_0)\]
##III.连续时间Fourier变换的性质
###i.线性特性
\[f_1(t)=\xrightarrow{\mathscr{F}}F_1(j\omega),f_2(t)=\xrightarrow{\mathscr{F}}F_2(j\omega)\\\Rightarrow{}af_1(t)+bf_2(t)\xrightarrow{\mathscr{F}}aF_1(j\omega)+bF_2(j\omega)\]
###ii.共轭对称特性
\[f(t)=\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}f^* (t)\xrightarrow{\mathscr{F}}F^* (-j\omega)\quad f^* (-t)\xrightarrow{\mathscr{F}}F^* (j\omega)\]
###iii.对称互易特性
\[f(t)=\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}F(jt)\xrightarrow{\mathscr{F}}2\pi{}f(-\omega)\]
对称互易特性表明信号的时域波形与其频谱函数具有对称互易关系,从Fourier正反变换的公式也可以发现他们的差别就是幅度相差 $2\pi$ 且积分项内差一个负号
###iv.展缩特性
\[f(t)=\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}f(at)\xrightarrow{\mathscr{F}}\frac1{|a|}F(j\frac\omega{a})\]
时域波形的压缩(|a|>1),则对应其频谱函数扩展,反之则压缩 由此可见,信号的持续时间与其有效带宽成反比 在通信技术中,常需要增加通信速度,这就要求相应的扩展通讯设备的有效带宽
###v.时移特性
\[f(t)=\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}f(t-t_0)\xrightarrow{\mathscr{F}}F(j\omega)e^{-j\omega t_0}\]
信号在时域中的 **时移**，对应频谱函数在频域中产生的 **附加相移**，而 **幅度频谱保持不变**。
###vi.频移特性(调制定理)
\[f(t)=\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}f(t)e^{j\omega_0t}\xrightarrow{\mathscr{F}}F(j(\omega-\omega_0))\]
信号号在时域的时移,对应频谱函数在频域的频移
\[\mathscr{F}[f(t)\cos\omega_0t]=\frac12\mathscr{F}[f(t)e^{j\omega_0t}]+\frac12\mathscr{F}[f(t)e^{-j\omega_0t}]=\frac12\mathscr{F}[j(\omega-\omega_0)]+\frac12\mathscr{F}[j(\omega+\omega_0)]\]
信号 $f(t)$ 与余弦信号 $\cos\omega_0t$ 相乘后，其频谱是将原来信号频谱向左右搬移 $ω_0$，幅度减半。
###vii.时域卷积特性
\[f_1(t)\xrightarrow{\mathscr{F}}F_1(j\omega),f_2(t)=\xrightarrow{\mathscr{F}}F_2(j\omega)\\\Rightarrow{}f_1(t)* f_2(t)\xrightarrow{\mathscr{F}}F_1(j\omega)F_2(j\omega)\]
Fourier变换可以将时域的卷积运算转换成频域中的乘法运算
###iix.频域卷积特性
\[f_1(t)\xrightarrow{\mathscr{F}}F_1(j\omega),f_2(t)=\xrightarrow{\mathscr{F}}F_2(j\omega)\\\Rightarrow{}f_1(t)f_2(t)\xrightarrow{\mathscr{F}}\frac1{2\pi}[F_1(j\omega)* F_2(j\omega)]\]
两信号在时域的乘积运算,可以转换为两信号在频谱的卷积运算
###ix.时域微分特性
\[f(t)\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}f(t)'\xrightarrow{\mathscr{F}}(j\omega)F(j\omega)\quad f^{(n)}\xrightarrow{\mathscr{F}}(j\omega)^{(n)}F(j\omega)\]
####修正的时域微分特性
\[f(t)\xrightarrow{\mathscr{F}}F(j\omega)\quad f(t)'\xrightarrow{\mathscr{F}}F_1(j\omega)\\\Rightarrow{}F(j\omega)=\pi(f(\infty)+f(-\infty))\delta(\omega)+\frac{F_1(j\omega)}{j\omega}\]
###x.积分特性
\[f(t)\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}\int^t_{-\infty}f(\tau)d\tau\xrightarrow{\mathscr{F}}\frac1{j\omega}F(j\omega)+\pi F(0)\delta(\omega)\]
###xi.频域微分特性
\[f(t)\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}tf(t)\xrightarrow{\mathscr{F}}j\frac{dF(j\omega)}{d\omega}\]
###xii.能量定理(Parseval定理)
\[f(t)\xrightarrow{\mathscr{F}}F(j\omega)\\\Rightarrow{}E_f=\int^\infty_{-\infty}|f(t)|^2dt=\frac1{2\pi}\int^\infty_{-\infty}|F(j\omega)|^2d\omega\]
非周期能量信号不但可以从信号的时域描述 $f(t)$ 进行计算, 也可以从信号的频域描述 $F(j\omega)$ 进行计算(由 $|F(jω)|^2$ 在整个频率范围的积分乘以 $1/2π$ 来计算)

物理意义：非周期能量信号的归一化能量在 **时域中与在频域** 中相等，保持 **能量守恒**。

定义单位角频率的信号能量为 **能量频谱密度函数**，简称 **能量谱** $G(j\omega)$。
\[G(j\omega)=\frac1{2\pi}|F(j\omega)|^2\]
可见,信号的能量谱 $G(j\omega)$ 是 $\omega$ 的偶函数, 它只决定与频谱函数的幅度特性,而与相位特性无关
##非周期信号的频域分析小结
* 重要概念: **非周期信号的频谱**
  1. 非周期信号的频谱与周期信号的频谱的区别
  1. 非周期信号 **频谱的物理意义**
  1. 非周期信号频谱的分析方法: 应用 **常用基本信号的频谱** 与 **傅里叶变换的性质**
* 分析问题使用的数学工具: **傅里叶变换**
* 工程应用: 调制 解调 频分复用
##IV.离散周期信号的频域分析
//TBD
##V.离散非周期信号的频域分析
//TBD
