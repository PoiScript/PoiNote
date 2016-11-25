#机械振动
##I.简谐运动
###i.简谐运动的特征及其表示式(谐振子)
####1.受力特点及动力学方程
线性恢复力
\[F=-kx\]
力和位移正比而反向
####2.运动学方程
动力学方程
\[F=-kx=ma=m\frac{d^2x}{d^2t}\]
运动学方程
\[\frac{d^2x}{d^2t}+\omega^2x=0\]
\[x(t)=A\cos(\omega t+\varphi_0)\]
其中 $\omega$ 为固有角 (圆) 频率
\[\omega=\sqrt\frac km\]
固有角频率决定于振动系统的内在性质
####3.速度和加速度
\[x(t)=A\cos(\omega t+\varphi_0)\]
\[V=\frac{dx}{dt}=-\omega A\cos(\omega t+\varphi_0)=-V_m\sin(\omega t+\varphi_0)\]
\[V=V_m\cos(\omega t+\varphi_0+\frac\pi2)\]
\[a=\frac{dv}{dt}=-\omega^2A\cos(\omega t+\varphi_0)=-a_m\cos(\omega t+\varphi_0)\]
####4.由初始条件求振幅和初相位
\[\begin{cases}x(t)=A\cos(\omega t+\varphi_0)\\
V=-\omega A\sin(\omega t+\varphi_0)\end{cases}
\xrightarrow{t=0}\begin{cases}x_0=A\cos\varphi_0\\
V_0=-\omega A\sin\varphi_0\end{cases}\]
\[A=\sqrt{x_0^2+\frac{v_0^2}{\omega^2}}\quad\varphi_0=\tan^{-1}\Big(-\frac{V_0}{\omega x_0}\Big)\]
###ii.描述简谐振动的特征量
**定义**: $x(t)=A\cos(\omega t+\varphi_0)$

$x$ 是描述位置的物理量,如 $x$ 或 $\theta$ 等.
####1.振幅(amplitude) $A$
最大位移的绝对值( $A$ 恒为 **正值**)
####2.周期(period) $T$ 和 频率(frequency) $ν$
反映振动的快慢
#####周期性:
\[x(t)=x(t+T)\]
\[\begin{cases}T=\frac{2\pi}\omega\\
\omega=\sqrt{\frac km}\end{cases}
\Rightarrow\begin{cases}T=2\pi\sqrt{\frac km}\\
v=\frac1T=\frac\omega{2\pi}=\frac1{2\pi}\sqrt{\frac km}\end{cases}\]
圆频率(角频率):
\[\omega=2\pi v\]
####3.相位
1. $(\omega t+\varphi_0)$ 是 $t$ 时刻的相位(phase)
1. $\varphi_0$ 是 $t=0$ 时刻的相位  ——  初相(initial phase) 初相 $\varphi_0$ 的数值决定于 **时间零点** 的选择
1. 相位的意义:
    - 相位确定了 $t$ 时刻振动的状态 $(x、υ、a)$
    - 相位每改变 $2\pi$ 振动重复一次.
    - 相位 $2\pi$ 范围内变化,状态不重复.
\[x(t)=A\cos(\omega t+\varphi_0)\]
\[\begin{cases}V=-\omega A\sin(\omega t+\varphi_0)\\
a=-\omega^2A\cos(\omega t+\varphi_0)\end{cases}\]
4. 相位差(phase difference)
\[x_1=A_1\cos(\omega_1t+\varphi_{10})\]
\[x_2=A_2\cos(\omega_2t+\varphi_{20})\]
\[\Delta\varphi=(\omega t+\varphi_{10})-(\omega t+\varphi_{20})=\varphi_{10}-\varphi_{20}\]
5. 同相和反相(同频率振动)<br>
当 $\Delta\varphi=\pm2k\pi,(k=0,1,2\cdots)$ 两振动步调相同,称 **同相**<br>
当 $\Delta\varphi=\pm(2k+1)\pi$ 两振动步调相反, 称 **反相**
6. 超前和落后<br>
若 $\Delta\varphi=\varphi2-\varphi1>0$, 则 $x_2$ 比 $x_1$ 早 $\Delta\varphi$ 达到正最大, 称 $x_2$ 比 $x_1$ 超前 $\Delta\varphi$(或 $x_1$ 比 $x_2$ 落后 $\Delta\varphi$)。<br>
**注意:** $|\Delta\varphi|>\pi$  例如: $\Delta\varphi=3/2\,\pi$，不说 $x_2$ 比 $x_1$ 超前 $3/2\,\pi$ ，而说 $x_2$ 比 $x_1$ 落后 $1/2\,\pi$ $(3/2\,\pi-2\pi=-1/2\,\pi)$
###iii.简谐振动的描述方法
####1.解析法
(由表达式 $x=A\cos(\omega t+\varphi_0)$ 出发)

已知表达式 $\Rightarrow\,A,T,\varphi_0$
####2.旋转矢量法
**简谐振动** 和 **匀速圆周运动** 之间的简单关系:

匀速圆周运动质点在某一直径上的 **投影** 的运动就是简谐振动.

**特点**: 直观方便.
####3.振动曲线的画法
$\varphi_0$ 为非典型值时, 可用领先、落后的概念画出振动曲线。

欲画 $x=A\cos(\omega t+\varphi_0)$ 的曲线,
先画辅助曲线 $x_辅=A\cos\omega t$ 的曲线
将 $x_辅$ 曲线左(右)移即得 $x$ 的曲线,移动的距离为 $\Delta t=\frac{|\varphi_0|}{2\pi}T$
###iv.简谐振动的能量(以水平弹簧振子为例)
####1.动能
\[E_k=\frac12mV^2=\frac12kA^2\sin^2(\omega t+\varphi)\]
\[E_k=\frac1T\int^{t+T}_tE_kdt=\frac14kA^2\]
####2.势能
\[E_p=\frac12kx^2=\frac12kA^2\cos^2(\omega t+\varphi)\]
\[\overline E_p=\frac1T\int^{t+T}_tE_pdt=\frac14kA^2=\overline E_k\]
####3.机械能
\[E=E_k+E_p=\frac12kA^2\]
##II.阻尼振动(damped vibration)
**阻尼**: 消耗振动系统能量的原因
**阻尼种类**: 摩擦阻尼 辐射阻尼
###i.阻尼振动
\[f=-\gamma x=-\gamma\frac{dx}{dt}\]
(简谐振动系统机械能守恒)
###ii.阻尼振动的微分方程(以受阻弹簧振子为例)
\[m\frac{d^2x}{dt^2}=-kx-\gamma\frac{dx}{dt}\\
\Rightarrow\frac{d^2x}{dt^2}+2\delta\frac{dx}{dt}+\omega_0^2x=0\]
阻尼系数: $2\delta=\gamma/m$ 固有频率: $\omega_0=(k/m)^{1/2}$
###iii.表达式和振动曲线
####1.小阻尼 ($\delta<\omega_0$)
\[x=A_0e^{-\delta t}\cos\Big(\sqrt{\omega_0^2-\delta^2t}+\delta'_ 0\Big)\]
特点:
振动（ $A(t)=A_0e^{-\delta t}$ ）随时间指数衰减，振动能量不断损耗

不是简谐振动,也不是严格意义上的周期振动

位移相继两次达到极大值的时间间隔为(准周期)
\[T=\frac{2\pi}\omega=\frac{2\pi}{\sqrt{\omega_0^2-\delta^2}}>T_0(固有周期)\]
####2.过阻尼和临界阻尼
**临界阻尼**:
\[\delta=\omega_0\]
**过阻尼**:
\[\delta>\omega_0\]
**在过阻尼和临界阻尼时**, 无振动.

应用: 电表阻尼, 天平阻尼
实际的振动系统，阻力无法避免，怎样得到等幅振动？
##III.受迫振动 共振
###i.受迫振动
在外来驱动力作用下的振动
####1.系统受力
- 弹性力: $-kx$
- 阻尼力: $-\gamma x$
- 周期性驱动力: $F=F_0\cos(\omega_dt)$
####2.受迫振动的微分方程
\[m\frac{d^2x}{dt^2}=-kx-\gamma\frac{dx}{dt}+F_0\cos(\omega_dt)\]
\[\frac{d^2}{dt^2}+2\delta\frac{dx}{dt}+\omega_0^2x=\frac{F_0}m\cos(\omega_dt)\]
其中
\[\omega_0=\sqrt\frac km\quad2\delta=\frac\gamma m\quad f=\frac{F_0}m\]
####3.受迫振动微分方程的解(阻尼较小时)
\[x=\underbrace{A_0e^{-\delta t}\cos\Big(\sqrt{\omega_0^2-\delta^2}t+\varphi'_ 0\Big)}_{减幅振动，足够长时间后可以忽略}+\underbrace{A\cos(\omega_dt+\varphi)}_{稳定等幅振动}\]
稳态解为:
\[x=A\cos(\omega_dt+\varphi)\]
####4.特点
稳态时的受迫振动按简谐振动的规律变化
1. **频率**: 等于驱动力的频率 $\omega_d$
1. **振幅**: $A=\displaystyle\frac f{[(\omega_d^2-\omega_0^2)^2+4\delta^2\omega_d^2]^{1/2}}$
与 **起始条件** 无关。
1. **稳态受迫振动位移和驱动力的相位差**: $\tan\varphi=\displaystyle\frac{-2\delta\omega_d}{\omega_0^2-\omega_d^2}$ 与 **起始条件** 无关。
###ii.共振
####1.位移共振(振幅取极值)
\[\frac{dA}{d\omega_d}=0\Rightarrow\boxed{振幅出现极大值,振动剧烈的现象}\]
共振频率: $\omega_r=\sqrt{\omega_0^2-2\delta^2}$ 共振振幅: $A_r=\displaystyle\frac f{2\delta\sqrt{\omega_0^2-\delta^2}}$
####2.速度共振(速度振幅取极值)
\[V_m=A\omega_d=\frac{f\omega_d}{\sqrt{(\omega^2_d-\omega_0^2)^2+4\delta^2\omega^2_d}}\]
共振频率: $\omega_r=\omega_0$ 共振速度振幅: $V_m=\displaystyle\frac f{2\delta}$
\[v=\omega_dA\cos(\omega_dt+\varphi+\frac\pi2)\\\varphi=\arctan\frac{-2\delta\omega_d}{\omega_0^2-\omega_d^2}\\\xrightarrow{\omega_d=\omega_r=\omega_0}\varphi=-\frac\pi2\to\begin{cases}v=\omega_dA\cos(\omega_dt)\\F=F_0\cos(\omega_dt)\end{cases}\]
速度共振时，速度与策动力 **同相**，一周期内策动力总作 **正** 功，此时向系统输入的能量最大
##IV.电磁振荡
###i.LC电路的振荡
电路中电压和电流的周期性变化称为 **电磁振荡。**
LC振荡电路
        向左合上开关K，使电源给电容器充电，然后将开关K 接通LC 回路，出现电磁振荡效应。
##V.谐振动的合成
###i.同方向同频率的简谐振动的合成
####1.分振动:
\[\begin{cases}x_1=A_1\cos(\omega t+\varphi_{10})
\\x_2=A_2\cos(\omega t+\varphi_{20})\end{cases}\]
####2.合振动:
\[x=x_1+x_2=A_1\cos(\omega t+\varphi_{10})+A_2\cos(\omega t+\varphi_{20})\\=\underbrace{(A_1\cos\varphi_{10}+A_2\cos\varphi_{20})}_{A\cos\varphi_0}\cos\omega t-\underbrace{(A_1\sin\varphi_{10}+A_2\sin\varphi_{20})}_{A\sin\varphi_0}\sin\omega t\]
结论：合振动 $x$ 仍是 **简谐振动**
