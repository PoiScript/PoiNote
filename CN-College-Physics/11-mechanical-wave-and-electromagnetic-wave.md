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
###iii.波阵面和波射线(Wave surface & Line of wave)
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
##V. 惠更斯原理(Huygens’ principle)
###i.惠更斯原理
###ii.波的衍射(wave diffraction)
###iii.折射现象
###vi.反射现象
##VI.波的干涉(interference of waves)
###i.波的叠加原理 (superposition of waves)
####1.波传播的独立性
当几列波在传播过程中在某一区域相遇后再行分开，各波的传播情况与未相遇时一样，仍保持它们各自的频率、波长、振动方向等特性继续沿原来的传播方向前进。
####2.叠加原理
在波相遇区域内，任一质点的振动，为各波单独存在时所引起的振动的 **合振动。**
#####注意
波的叠加原理仅适用于 **线性波** (波动方程的线性决定了波服从叠加原理)
####3.波动方程的线性决定了波服从叠加原理
\[波的强度过大\to非线性波\to叠加原理不成立\]
对于小振幅的波
⇒ 媒质可看作线性媒质 (波引起的应变不大，应力∝应变，符合胡克定律)。
⇒波动方程是线性方程 (曾记否推导波 = ∂ t 2∂2ξ∂ x2∂2ξu2
动方程时用了胡克定律
∂2ξ
∂2ξ
u2
=
∂ t 2
∂ x2
一维齐次线性偏微分方程  ⇒  波动方程的线性决定了波服从叠加原理。
###ii.波的干涉条件
一般情况下，各个波的振动方向和频率均不同，相位关系
不确定，叠加的合成波较为复杂。
•
干涉现象 (interference of waves)
当两列（或多列）波叠加的结果，其合振幅 A 和合强
度 I 将在空间形成一种稳定的分布，即某些点上的振动始终
加强，某些点上的振动始终减弱。
—— 波的干涉现象
•
相干波
•
相干条件
满足相干条件的波
频率相同、振动方向相同、
相位差恒定。
•
相干波源
产生相干波的波源
###iii.干涉规律
S1
P
S2
P
根据叠加原理可知，P 点处振动方程为
• 合振动的振幅
• P 点处波的强度
空间任意点有确定的相位差和强度         空间不同点的强度分布是稳定的
• 空间点振动的情况分析
干涉相长
干涉相消
讨论
(1) 若           同相波源
干涉相长
干涉相消
(2) 若
干涉相长
干涉相消
从能量上看，当两个相干波发生干涉时，在两波交叠的区域，合成波在空间各处的强度并不等于两个分波强度之和，而是发生重新分布。这种新的强度分布是时间上稳定的、空间上强弱相间具有周期性的一种分布。
####iv.驻波(standing wave) ---- 干涉的特例
两列 **等振幅** 相干波沿 **相反方向** 传播时叠加形成 **驻波**
#####1.弦线上的驻波实验
完整驻波条件:
\[AB=L=n\frac\lambda2,n=1,2,3\cdots\]
####2.驻波波函数
\[y_1=A\cos2\pi\Big(\frac tT-\frac x\lambda\Big)\\y_2=A\cos2\pi\Big(\frac tT+\frac x\lambda\Big)\]
\[y=y_1+y_2\\=A\Big[\cos2\pi\Big(\frac tT-\frac x\lambda\Big)+\cos2\pi\Big(\frac tT+\frac x\lambda\Big)\Big]\\=\Big(2A\cos\frac{2\pi}\lambda x\Big)\cos\frac{2\pi}Tt\]
#####(1).频率特点:
各质元以同一频率作谐振动。
#####(2).振幅特点：
即驻波是各质点振幅按余弦分布的特殊谐振动;
######波腹 $(A′=A′_ {max})$:
\[x=k\frac\lambda2,k=0,\pm1,\pm2\cdots\]
######波节 $(A′=A′_ {min})$:
\[x=(2k+1)\frac\lambda4,k=0,\pm1,\pm2\cdots\]
######相邻两波腹之间的距离:
\[x_{k+1}-x_k=(k+1)\frac\lambda2-k\frac\lambda2=\frac\lambda2\]
######相邻两波节之间的距离:
\[x_{k+1}-x_k=\big[2(k+1)+1\big]\frac\lambda4-(2k+1)\frac\lambda4=\frac\lambda2\]
####3.相位特点
所有波节点将媒质划分为长 $\lambda/2$ 的许多段，每段中各质点的振动振幅不同，但 **相位皆相同**；而相邻段间各质点的振动 **相位相反**; 即驻波中 **不存在相位的传播**。
####4.能量特点
没有能量的 **定向传播**。能量只是在波节和波腹之间，进行动能和势能的转化。
####5.半波损失
反射点为波节，表明入射波与反射波在该点反相。
\[\Delta\varphi=\pi\Rightarrow\delta\frac\lambda{2\pi}\Delta\varphi=\frac\lambda2\]
相当于入射波与反射波之间附加了半个波长的波程差
1. $n_1<n_2$ 有半波损失(波节)
1. $n_1>n_2$ 无半波损失(波腹)

透射波没有半波损失
##VII.多普勒效应(Doppler effect)
波源振动的频率 $v_S$
波的频率(媒质质元) $v$
接收频率 $v_R$

波源和观察者 相对于 介质 **静止**:
\[u_S=u=u_R\]
由于观察者(接收器)或波源、或二者同时 **相对媒质运动**，而使观察者接收到的频率与波源发出的 **频率不同** 的现象，称为 **多普勒效应。**
\[u_S\neq u=\neq u_R\]
* 参照系：媒质
* 设 $S$ 和 $R$ 的运动沿二者连线
* 符号规定:  $S$ 和 $R$ 相互靠近时, $υ_S>0,υ_R>0$
###i.波源静止 观察者运动 $(v_S=0设v_R>0)$
\[v=v_S,但v_R\neq v\]
\[\nu_R=\frac{u+v_R}\lambda=\frac{u+v_R}{u/\nu_W}=\frac{u+v_R}u\nu_W\\\nu_R=(1+\frac{u_R}u)\nu_S\]
靠近 $v_R>0$ 远离 $v_R<0$
###ii.观察者静止 波源运动 $(v_R=0设v_S>0)$
\[v_R=v,但ν\neq v_S\\\lambda'=uT_S-v_ST_S=\frac{u-v_S}{\nu_S}\]
靠近 $v_S>0$ 远离 $v_S<0$
###iii.波源和观察者同时运动 $(设v_S,v_R均>0)$
\[\nu_R=\frac{u+v_R}u\nu\\\nu=\frac u{u-v_S}\nu_S\\\Rightarrow\nu_R=\frac{u+v_R}{u-v_S}\nu_S\]
符号正负的选择与上述相同
1. 当波源或观察者在二者联线 **垂直方向上** 运动时，**无多普勒效应**。机械波无 **横向** 多普勒效应 $ν_R=ν_S$
\[\nu_R=\frac{u+v_R\cos\theta_R}{u-v_S\cos\theta_S}\nu_S\]
2. $\mu_S>u$ 时，多普勒效应失去意义，此时形成冲击波.(Shock wave)

马赫角(Mach angle)
\[\sin\theta=\frac u{\nu_S}\]
##小结
1. 描述波的物理量
2. 波程差与相位差
\[\Delta\varphi=\frac{2\pi}\lambda\delta=\frac{2\pi}\lambda(r_1-r_2)\]
3. 平面简谐波的波函数
\[y(x,t)=A\cos\Big[\omega(t\pm\frac xu)+\varphi_0\Big]\]
4. 波的能量和能流
\[W_K=\frac12\mu\Delta xA^2\omega^2\sin^2\Big[\omega(t-\frac xu)+\varphi_0\Big]\\W_P=\frac12\mu\Delta xA^2\omega^2\sin^2\Big[\omega(t-\frac xu)+\varphi_0\Big]\]
\[平均能量密度:\overline{w}=\frac12\rho A^2\omega^2\\平均能流密度:I=\frac12\rho A^2\omega^2u\]
5. 波的干涉
\[\Delta\varphi=\varphi_{20}-\varphi_{10}-\frac{2\pi}\lambda(r_1-r_2)\\=\begin{cases}\pm2k\pi&干涉相长\\\pm(2k+1)\pi&干涉相消\end{cases}\]
6. 驻波
\[y=2A\cos2\pi\frac x\lambda\cos\omega t\\=\begin{cases}x=(2k+1)\frac\lambda4&波节\\x=k\frac\lambda2&波腹\end{cases}\]
7. 多普勒效应
\[\nu_R=\frac{u+v_R}{u-v_S}\nu_S\]
