#机械波和电磁波
振动状态的传播就是 **波动**, 简称 **波**(wave), 激发波动的振动系统称为 **波源**. 通常波动分成两大类, 一类是机械振动在介质中的传播, 称为 **机械波**(mechanical wave); 另一类是变化电场和变化磁场在空间的传播,称为 **电磁波**(electromagnetic wave)
##I.机械波的产生和传播
###i.机械波产生的条件(Generation of mechanical wave)
####1.机械波:
机械振动以一定速度在弹性介质中由近及远地传播出去,就形成 **机械波**(Mechanical wave) 。
####2.条件
1. **波源**: 做机械振动的振动系统
1. **弹性介质**: 承担传播振动的物质质元之间以 **弹性力** 相联系
###ii.横波和纵波(Transversal wave & Longitudinal wave)
####1.横波:
介质质点的振动方向与波传播方向 **相互垂直** 的波；如柔绳上传播的波。
####2.纵波:
介质质点的振动方向和波传播方向 **相互平行** 的波,如声波。气体和液体内只能传播纵波,不能传播横波。

横波和纵波是波的两种基本类型, 有一些波既不是纯粹的横波, 也不是纯粹的纵波, 水面波就是一个例子.

结论
1. 波动中各质点并不随波前进；
1. 沿波的传播方向,各个质点的相位依次落后,波动是 **相位**(振动状态)的传播；

当波源做谐振动的时候,介质中各质点也做谐振动, 这时的波动称为 **简谐波**(simple harmonic wave)(余弦波或正弦波).简谐波是最简单而且重要的波
###iii.波阵面和波射线 Wave surface & Line of wave
####1.波面
在波传播过程中,任一时刻媒质中振动相位相同的点联结成的面。
####2.波线
沿波的传播方向作的有方向的线。
####3.波前
在某一时刻,波传播到的最前面的波面。

**注意** 在各向同性均匀媒质中,波线⊥波面。
###iv.波的特征物理量 波长 周期 频率 波速
####1.波长(Wavelength)$\lambda$
同一时刻同一波线上相邻两个相位差为 $2\pi$ 的质点之间的距离；即波源作一次完全振动,波前进的距离。

波长反映了波的 **空间周期性。**
####2.周期(Period)$T$
波前进一个波长距离所需的时间。

周期表征了波的 **时间周期性。**
####3.频率(Frequency)$v$
单位时间内,波前进距离中完整波的数目。

频率与周期的关系为
\[v=\frac1T\]
####4.波速(Wave velocity)$u$
振动状态在媒质中的传播速度。

波速与波长、周期和频率的关系为
\[u=\frac\lambda T=v\lambda\]
####5.说明
1. 波的周期和频率与媒质的性质无关；一般情况下,与 **波源** 振动的周期和频率相同。
1. 波速实质上是相位传播的速度,故称为 **相速度**; 其大小主要决定于 **媒质** 的性质(弹性和惯性),与波的频率无关。
##II.平面简谐波  Planar harmonic wave
####简谐波
介质传播的是简谐振动,即波所到之处,介质中各质点作同频率的简谐振动。
####平面简谐波
波面为平面的简谐波
####说明
1. **简谐波** 是一种最简单、最基本的行波,研究简谐波的波动规律是研究更复杂波的基础。
1. 本节主要讨论在 **无吸收**(即不吸收所传播的振动能量), **各向同性**, **均匀无限大** 媒质中传播的平面简谐波。
1. 同一波面上的点有相同的 **相位** 和 **位移**(离开平衡位置)所以只要研究和波面垂直的 **波线** 上波的传播。
###i.平面简谐波的波函数(Wave function)
**波函数**:   有波传播时 弹性媒质的运动函数;任意质元在任意时刻偏离平衡位置的位移

**一般波函数**: $y=f(x,t)$

**简谐振动**: $y=A\cos(\omega t+\varphi_0)$

**波函数**:
\[y(x,t)=A\cos\Big[\omega(t-\frac xu)+\varphi_0\Big]\]
波函数的其它形式
\[y(x,t)=A\cos\Big[2\pi(vt-\frac x\lambda)+\varphi_0\Big]
\\y(x,t)=A\cos\Big[2\pi(\frac tT-\frac x\lambda)+\varphi_0\Big]
\\y(x,t)=A\cos\Big[\frac{2\pi}\lambda(ut-x)+\varphi_0\Big]\]
1. 由波函数可知波的传播过程中任意两质点 $x_1$ 和 $x_2$ 振动的相位差为
 ($x2>x1,\Delta<0$,说明 $x_2$ 处质点振动的相位总 **落后** 于 $x_1$ 处质点的振动)
 \[\Delta=[\omega(t-\frac{x_2}u)+\varphi_0]-[\omega(t-\frac{x_1}u)+\varphi_0]\\=\frac\omega u(x_1-x_2)\]
2. $u$ 实际上是振动相位的传播速度。$t_1$ 时刻 $x_1$ 处的振动状态经 $\Delta t$ 时间传播到 $x_1+\Delta x$ 处,则
\[y(x_1+\Delta x,t_1+\Delta t)=y(x_1,t_1)\\
\omega(t_1-\frac{x_1}t)=\omega(t_1+\Delta t-\frac{x_1+\Delta x}u)
\\可得到:u\frac{\Delta x}{\Delta t}\]
3. 若波沿轴 **负向** 传播,沿 $x$ 正方向各质元振动的相位依次 **领先**, 同样可得到波函数:
\[y(x,t)=A\cos\Big[\omega(t\frac xu)+\varphi_0\Big]
\\其它形式\begin{cases}y(x,t)=A\cos\Big[2\pi(vt+\displaystyle\frac x\lambda)+\varphi_0\Big]
\\y(x,t)=A\cos\Big[2\pi(\displaystyle\frac tT+\frac x\lambda)+\varphi_0\Big]
\\y(x,t)=A\cos\Big[\displaystyle\frac{2\pi}\lambda(ut+x)+\varphi_0\Big]\end{cases}\]
###ii.波函数的物理意义
####1.振动状态的空间周期性
$y(x+\lambda,t)=y(x,t)$ 说明波线上振动状态的空间周期性
* 由 **质元** 看：相隔 $\lambda$ 的两点振动状态完全相同(同相点)。
* 由 **波形** 看：波形在空间以 $\lambda$ 为 “周期” 分布着。
####2.波形传播的时间周期性
$y(x,t+T)=y(x,t)$ 说明波形传播的时间周期性
* 由质元看：每个质元振动周期为T
* 由波形看：t时刻和  t+T 时刻的波形曲线完全重合。
####3.振动方程
$x$ 给定,$y=y(t)$ 是 $x$ 处振动方程
\[y(x_0,t)=A\cos\Big[\omega t-\omega\frac{x_0}u+\varphi_0\Big]\]
####4.波形图
$t$ 给定,$y=y(x)$ 表示 $t$ 时刻的波形图
\[y(x,t_0)=A\cos\Big[\omega t_0-\omega\frac xu+\varphi_0\Big]\]
####5.时空周期性
$x$ 和 $t$ 都在变化,表明波形传播和质点分布的 **时空周期性**

$y$ 给定, 设初相 $\phi_0=0$
 \[\displaystyle y(x_1,t_1)=A\cos[\omega(t_1-\frac{x_1}u)]\\
 =y(x_2,t_2)=A\cos\Big[\omega(t_1+\Delta t-\frac{x_1+\Delta x}u)\Big]
 \\\Rightarrow \Delta x=u\Delta t\]

振动状态 经过时间 $\Delta t$,传过了 $\Delta x=u\Delta t$ 的距离.在 $\Delta t$ 内,整个 **波形** 传播了 $\Delta t=u\Delta t$ 的距离。
####波动曲线与振动曲线的不同
1. 振动曲线反映 **某一质元** 的位移随 $t$ 的变化
1. 不同时刻对应有不同的波形曲线
1. 波形曲线能反映横波、纵波的位移情况
1. 波形曲线上必须标明 **时刻** $t$ 和波的 **传播方向**
###iii.平面简谐波的波动方程(Differential equation)
由
\[y(x,t)=A\cos\Big[\omega(t-\frac xu)+\varphi_0\Big]\]
知
\[\left.
\begin{array}{r}
\frac{\partial^2y}{\partial t^2}=-A\omega^2\cos\Big[\omega(t-\frac xu)+\varphi_0\Big]\\
\frac{\partial^2y}{\partial x^2}=-A\frac{\omega^2}{u^2}\cos\Big[\omega(t-\frac xu)+\varphi_0\Big]
\end{array}
\right\}\\
\frac{\partial^2y}{\partial x^2}=\frac1{u^2}\frac{\partial^2y}{\partial t^2}\]
1. 上式是 **一切平面波** 所满足的微分方程(**正、反传播**)
1. 不仅适用于机械波,也广泛地适用于电磁波、热传导、化学中的扩散等过程；
1. 若物理量是在 **三维** 空间中以波的形式传播,波动方程:
\[\frac{\partial^2\xi}{\partial x^2}+\frac{\partial^2\xi}{\partial y^2}+\frac{\partial^2\xi}{\partial z^2}=\frac1{u^2}\frac{\partial^2\xi}{\partial t^2}\]
##III.波的能量 波的强度
####波动过程
**波** 是振动状态(**相位**)的 **传播**

**波动过程** 是能量的 **传播过程**

质元由静止开始振动 质元也发生形变

振动动能 形变势能 = 波的能量
###i.弹性波的能量
####1.能量
以绳索上传播的横波为例: 设波沿 $x$ 方向传播,取线元
\[\Delta m=\mu\Delta x\]
线元的动能为
\[W_k=\frac12\Delta mV^2=\frac12\Delta m(\frac{\partial y}{\partial t})^2\]
线元的势能(原长为势能零点) 伸长过程中张力作的功 为
\[W_p=F(\Delta l-\Delta x)\]
其中
\[\Delta l=\sqrt{(\Delta x)^2+(\Delta y)^2}=\Delta x[1+\Big(\frac{\Delta y}{\Delta x}\Big)^2]^{1/2}\\\approx\Delta x[1+\Big(\frac{\partial y}{\partial x}\Big)^2]^{1/2}\approx\Delta x[1+\frac12\Big(\frac{\partial y}{\partial x}\Big)^2]\\W_p\approx\frac12F\Delta x\Big(\frac{\partial y}{\partial x}\Big)^2\]
线元的机械能为
\[W=W_k+W_p\]
\[\because F=u(弦线中横波速度)^2+\mu(线密度)\\y=A\cos\big[\omega(t-\frac xu)+\varphi_0\big]\]
\[\therefore W_k=\frac12\mu\Delta x(\frac{\partial y}{\partial t})^2=\frac12\mu\Delta xA^2\omega^2\sin^2\big[\omega(t-\frac xu)+\varphi_0\big]\\W_p=\frac12F\Delta x(\frac{\partial y}{\partial x})^2=\frac12\mu\Delta xA^2\omega^2\sin^2\big[\omega(t-\frac xu)+\varphi_0\big]\]
机械能
\[W=W_k+W_p=\mu\Delta xA^2\omega^2\sin^2\big[\omega(t-\frac xu)+\varphi_0\big]\]
1. 在波的传播过程中,**媒质中任一质元的动能和势能是同步变化的**,即 $W_k=W_p$,与简谐弹簧振子的振动能量变化规律是不同的；此时能量是“一堆一堆”地集中于位移为零的那些质元处。随着波形的传播,能量也向前传播,其传播速度也是u (波速)。
1. 质元机械能随时空周期性变化,表明质元在波传播过程中不断吸收和放出能量；因此,**波动过程是能量的传播过程。**
####2.能量密度
设绳子的横截面为 $S$ ,体密度为 $\rho$,则 **线元单位体积** 中的机械能(**能量密度**) 为:
\[w=\frac W{S\Delta x}=\rho A^2\omega^2\sin^2\big[\omega(t-\frac xu)+\varphi_0\big]=w(x,t)\]
* **平均能量密度**
\[w=\frac1T\int^T_0wdt=\frac12\rho A^2\omega^2\]
###ii.波的强度
####1.能流
在单位时间内通过一定截面的波动能量为 **能流**
\[P=\frac{wudtS}{dt}=wuS\]
在一个周期中的 **平均能流** 为
\[P=\frac1T\int_0^TPdt=\overline{w}uS\]
####2.能流密度
垂直通过单位截面积的能流。
#####大小:
\[J=\frac{dP}{dS}=wu\]
#####方向:
波的传播方向
#####矢量表示式
\[\vec{J}=w\vec{u}\]
####3.波的强度(平均能流密度)
一个周期内能流密度大小的平均值。
\[I=\overline{J}=\frac1T\int^T_0Jdt=\frac uT\int^T_0wdt\\=u\overline{w}=\frac12\rho A^2\omega^2u\propto A^2\]
###iii.平面波和球面波的振幅(不吸收能量)
####1.平面波
\[\overline{P}_1=\overline{w}_1uS_1=\frac12\rho A_1^2\omega^2uS_1\]
\[\overline{P}_2=\overline{w}_2uS_2=\frac12\rho A_2^2\omega^2uS_2\]
由 $\overline{P}_1=\overline{P}_2$ 平面波: $S_1=S_2\Rightarrow A_1=A_2$

这表明平面波在媒质不吸收的情况下, 振幅不变。
####2.球面波
由
\[\frac12\rho A_1^2\omega^2uS_1=\frac12\rho A_2^2\omega^2uS_2\]
得
\[A_1^2\cdot4\pi r_1^2=A_2^2\cdot4\pi r_2^2\\A_1r_1=A_2r_2\]
令 $Ar=a$ ($a$ 为离原点 (波源) 单位距离处波的振幅)则球面简谐波的波函数为
\[y(r,t)=\frac ar\cos\big[\omega(t-\frac ru)+\varphi_0\big],r>0\]
球面波的振幅在媒质不吸收的情况下,随 $r$ 增大而减小.
###iv.波的吸收
实验表明
\[dA=-aAdx\\A=A_0e^{-ax}\\I=I_0e^{-2ax}\]
$a$ 为介质 **吸收系数**,与介质的性质、温度、及波的频率有关。
###v.声强级
####1.正常人听声范围
\[20<ν<20000\text{Hz}\]
\[I_{下(听觉阀)}<I<I_{上(痛觉阀)}\]
####2.声强级
以 $1000\text{Hz}$ 时的 $I_下$ 作为基准声强 $I_0$,
\[I_L=10\log_{10}\Big(\frac I{I_0}\Big)\,单位:分贝(\text{db})\]
引起痛觉：120 db；繁忙街道：70 db；正常谈话：60 db；
耳语：20 db； 树叶沙沙响：10 db。
##IV.电磁波（Electromagnetic wave ）
###i.麦克斯韦的理论预言
\[\begin{array}{rcl}
\oint_S\vec D\cdot d\vec S=0&高斯定理&\nabla\cdot\vec E=0
\\\oint_S\vec B\cdot d\vec S=0&磁通连续性原理&\nabla\cdot\vec B=0
\\\oint_L\vec E\cdot d\vec l=-\int_S\frac{\partial\vec B}{\partial t}&法拉第电磁感应定律&\nabla\times\vec E=-\mu_0\frac{\partial\vec E}{\partial t}
\\\oint_L\vec H\cdot d\vec l=\int_S\frac{\partial\vec D}{\partial t}\cdot d\vec S&全电流安培环路定理&\nabla\times\vec H=\varepsilon_0\frac{\partial\vec E}{\partial t}
\end{array}\]
####1.预言电磁波的存在。
无源区时变电磁场是有旋无散的。电场线与磁场线相互交链，自行闭合，从而在空间形成 **电磁波。**

麦克斯韦电磁场理论 **波动方程**:
\[\begin{cases}\nabla^2\vec E=\varepsilon_0\mu_0\displaystyle\frac{\partial^2\vec E}{\partial t^2}
\\\nabla^2\vec H=\varepsilon_0\mu_0\displaystyle\frac{\partial^2\vec H}{\partial t^2}\end{cases}\\
\boxed{变化的电场}\Leftrightarrow\boxed{变化的磁场}\]
对沿 $x$ 方向传播的电磁场(波) 有
\[\frac{\partial^2E}{\partial x^2}=\mu_0\varepsilon_0\frac{\partial^2E}{\partial t^2}\\
\frac{\partial^2H}{\partial x^2}=\mu_0\varepsilon_0\frac{\partial^2H}{\partial t^2}\]
####2.电磁波的波速恰好等于光速，预言光也是电磁波
#####红外线
在微波和可见光之间的一个广阔波段范围(波长在600微米-- 0.76微米之间)的电磁波，叫做红外线。它在电磁波谱中位于可见光的红光部分之外，人眼看不见，波长比红光更长。
红外线是由炽热物体辐射出来的，人体就是一个红外线源。红外线的显著特性是热效应大，能透过浓雾或较厚大气层而不易被吸收。所谓热辐射，主要就是指红外线辐射。
#####可见光
在电磁波谱中，可见光只占很小的一部分波段，即波长范围在400～760nm之间，这些电磁波能使人眼产生光的感觉，所以叫做光波。人眼所看见的不同颜色的光，实际上是不同波长的电磁波，白光则是各种颜色(红、橙、黄、绿、青、蓝、紫)的可见光的混合。
#####紫外线
波长范围在40nm～400nm的电磁波，叫做紫外线。它是比可见光中的紫光波长更短的一种射线，人眼也看不见。炽热物体的温度很高(例如太阳)时，就会辐射紫外线。
#####无线电波
在电磁波谱中，波长最长的是无线电波。一般将频率低于 的电磁波统称为无线电波。无线电波通常是由电磁振荡电路通过天线发射出去的。无线电波按波长的不同又被分为长波、中波、短波、超短波、微波等波段。其中，长波的波长在3km以上，微波的波长小到0.1mm 。
#####X射线
X射线又称伦琴射线 （俗称X光），是波长比紫外线更短的电磁波，其波长范围在                   之间。它一般是由伦琴射线管产生的，也可由高速电子流轰击金属靶产生，它是由原子中的内层电子发射的。X射线具有很强的穿透能力，能使照相底片感光、使荧光屏发光。这种性质，在医疗上广泛用于透视和病理检查；工业上是工业探伤等无损检测的必要手段。由于X射线的波长与晶体中原子间距的线度相当，也常被用来分析晶体结构。
#####γ射线
γ射线是一种比X射线波长更短的电磁波，它的波长在0.3nm以下，频率在                    以上，。它来自宇宙射线或是由某些放射性元素在衰变过程中放射出来的。γ射线的能量极高，穿透能力比X射线更强，也可用于金属探伤等。通过对γ射线的研究，还可帮助了解原子核的结构。此外，原子武器爆炸时，有大量γ射线放出，它是原子武器主要杀伤因素之一。γ射线也是人类研究天体，认识宇宙的强有力的武器。
###ii.电磁波的辐射和传播
凡做加速运动的电荷都是电磁波的波源

例如：天线中的振荡电流 分子或原子中电荷的振动
\[\boxed{变化的电场}\to\boxed{变化的磁场}\to\boxed{变化的电场}\]

变化的电场和变化的磁场由近及远的传播出去，就形成了电磁波
###iii.平面电磁波的性质 (plane electromagnetic wave)
真空或绝缘介质:
\[\vec E=\vec E_0\cos\Big[\omega(t-\frac ru)+\varphi_0\Big]
\\\vec H=\vec H_0\cos\Big[\omega(t-\frac ru)+\varphi_0\Big]\]
1. 电磁波是 **横波** $\vec E\times\vec H\parallel\vec u$
1. 电磁波具有偏振性
1. $\vec E$ 和 $\vec H$ 互相垂直 **同相位** **同速度**
1. 任一时刻任一点，量值上 $\sqrt\varepsilon=\sqrt\mu H,E=\mu B$, $\varepsilon$ 和 $\mu$ **随介质变化**
1. 波速 $u=\sqrt{\displaystyle\frac1{\varepsilon\mu}}$ 真空中 $c=\sqrt{\displaystyle\frac1{\varepsilon_0\mu_0}}=2.9979\times10^8m\cdot s^{-1}$
1. 电磁波具有波的共性 —— **在介质分界面处有反射和折射**
\[n=\displaystyle\frac cu=\sqrt{\frac{\varepsilon\mu}{\varepsilon_0\mu_0}}=\sqrt{\varepsilon_r\mu_r}\approx\sqrt{\varepsilon_r}\leftarrow非铁磁性介质\]
###iv.电磁波的能量(electromagnetic energy)
####1.能量密度
\[w=\frac12(ED+BH)\frac12\big(\varepsilon E^2+\frac{B^2}\mu\big)\]
\[w=\varepsilon E^2=\frac{B^2}\mu\]
####2.能流密度矢量 — 坡印庭(Poynting)矢量
\[S=\frac{dA\cdot udt\cdot w}{dA\cdot dt}=wu\\
=u\varepsilon E^2=u^2\varepsilon E\frac Eu=\frac1\mu EB=EH\]
随时间周期变化
\[\vec S=\vec E\times\vec H=\vec E_0\times\vec H_0\cos^2\Big[\omega(r-\frac ru)+\varphi_0\Big]\]
波的强度 $I$:
\[I=\vec S=<S>=\frac1T\int^{t+T}_tSdt=\\
\frac1T\int^{t+T}_tE_0H_0\cos^2[\omega(t-\frac ru)+\varphi_0]dt=\frac12\sqrt\frac\varepsilon\mu E_0^2\]
####3.电磁波的动量密度
#####能量密度 $w$:
\[w^2=p^2u^2\]
#####动量密度 $p$:
\[p=\frac wu=\frac S{u^2}\]
\[\vec p=\frac{\vec S}{u^2}=\frac{\vec E\times\vec H}{u^2}\]
