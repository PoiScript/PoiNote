#系统的频域分析及其应用
##I.连续时间系统的频率响应
###i.基本信号 $e^{j\omega t}(-\infty<t<\infty)$ 通过系统的零状态响应
\[y_f(t)=e^{j\omega t}* h(t)=\int^\infty_{-\infty}e^{j\omega(t-\tau)}h(\tau)d\tau
\\=e^{j\omega t}\int^\infty_{-\infty}e^{-j\omega t}h(\tau)d\tau=e^{j\omega t}H(j\omega)\]
\[其中 H(j\omega)=\int^\infty_{-\infty}e^{-j\omega\tau}h(\tau)d\tau,称为频率响应函数\]
系统的 **频率响应函数** $H(j\omega)$ 等于 **系统冲激响应** $h(t)$ 的Fourer变换

虚指数信号作用与LTI系统时,系统的零状态响应仍为同频率的虚指数信号,虚指数信号的幅度和相位由系统的响应函数 $H(h\omega)$ 确实,所以 $H(j\omega)$ 反映了连续LTI系统对不同频率信号的响应特性
###ii.任意非周期信号通过系统的零状态响应
若信号 $f(t)$ 的Fourier存在，则可由 **虚指数信号 $e^{j\omega t}(−∞<t<∞)$ 的线性组合表示** ，即
\[f(t)=\frac1{2\pi}\int^\infty_{-\infty}F(j\omega)e^{j\omega t}d\omega\]
由系统的 **线性时不变特性**，可推出信号 $f(t)$ 作用于系统的 **零状态响应** $y_f(t)$。
\[y_f(t)=T|f(t)|=\frac1{2\pi}\int^\infty_{-\infty}F(j\omega)H(j\omega)e^{j\omega}d\omega=\frac1{2\pi}\int^\infty_{-\infty}Y(j\omega)d\omega\]
用 $Y(j\omega)$ 表示系统响应 $y(t)$ 的频谱函数, $Y(j\omega)=F(j\omega)H(j\omega)$ 即信号 $f(t)$ 作用于系统的零状态响应的频谱的与激励信号的频谱乘以系统的频率响应
###iii.系统频响 $H(j\omega)$ 的定义与物理意义
####$H(j\omega)$ 称为 **系统的频率响应**，定义为
\[H(j\omega)=\int^\infty_{-\infty}e^{-j\omega\tau}h(\tau)d\tau或H(j\omega)=\frac{Y_f(j\omega)}{F(j\omega)}\]
\[H(j\omega)=|H(j\omega)|e^{j\theta(\omega)}\quad
|H(j\omega)|:系统的幅度响应\quad
\theta(\omega):系统的相位相应\]
####$H(j\omega)$ 的物理意义
$H(j\omega)$ 反映了系统对输入信号不同频率分量的传输特性。
###iv.$H(j\omega)$ 与 $h(t)$ 的关系
由 $H(j\omega)$ 的定义，显然有
\[H(j\omega)=\mathscr{F}[h(t)]\]
即 $H(j\omega)$ 等于系统冲激响应 $h(t)$ 的Fourier变换
###v.求$H(j\omega)$ 的方法
1. $H(j\omega)=\mathscr{F}[h(t)]$
1. $H(j\omega)=Y(j\omega)/F(j\omega)$
##II.连续信号通过系统响应的频域分析
###i.连续非周期信号通过系统响应的频域分析
####1. 已知描述系统的微分方程
线性时不变系统的数学模型(n阶常系数线性微分方程):
\[a_ny^{(n)}(t)+a_{n-1}y^{(n-1)}(t)+\cdots+a_1y(t)+a_0y(t)
\\=b_mf^{(m)}(t)+b_{m-1}f^{(m-1)}(t)+\cdots+b_1f(t)+b_0f(t)\]
方程两边进行 **Fourier变换**，并利用 **时域微分特性**，有
\[[a_n(j\omega)^n+a_{n-1}(j\omega)^{n-1}+\cdots+a_1(j\omega)+a_0]\cdot Y_f(j\omega)\\=[b_m(j\omega)^m+b_{m-1}(j\omega)^{m-1}+\cdots+b_1(j\omega)+b_0]\cdot F(j\omega)\]
解此代数方程即可求得零状态响应的频谱 $Y_f(j\omega)$。
\[Y_f(j\omega)=\frac{b_m(j\omega)^m+b_{m-1}(j\omega)^{m-1}+\cdots+b_1(j\omega)+b_0}{a_n(j\omega)^n+a_{n-1}(j\omega)^{n-1}+\cdots+a_1(j\omega)+a_0}F(j\omega)\]
####2. 已知系统的频域响应
\[Y_f(j\omega)=F(j\omega)H(j\omega)\]
对 $Y_f(j\omega)$ 进行Fourier反变换，可得
\[y_f(t)=F^{-1}[Y_f(j\omega)]\]
#####系统零状态响应频域分析方法与卷积积分法的关系:
1. 两种分析方法实质相同，只不过是采用单元信号不同。
1. 分析域不同，**卷积积分法** —— **时域**，**频域分析法** —— **频域**。

Fourier变换的 **时域卷积定理** 是联系两者的桥梁。
###ii.连续周期信号通过系统响应的频域分析
####1.正弦信号通过系统的响应
\[f(t)=\sin(\omega t+\phi_n),-\infty<t<\infty\]
由 **Euler公式** 可得
\[f(t)=\frac1{2j}(e^{j(\omega t+\phi_n)}-e^{-j(\omega t+\phi_n)})\]
利用 **虚指数信号** $e^{j\omega t}$ 作用在系统上响应的特点及系统的 **线性特性**，可得 **零状态响应** $y_f(t)$ 为
\[y_f(t)=\frac1{2j}\Big[H(j\omega)e^{j(\omega t+\phi_m)}\Big]=|H(j\omega)|\sin(\omega t+\psi_n+\theta(\omega))\]
\[T\{\sin(\omega t+\psi_n)\}=|H(j\omega)|\sin(\omega t+\psi_n+\theta(\omega))\]
\[T\{\cos(\omega t+\psi_n)\}=|H(j\omega)|\cos(\omega t+\psi_n+\theta(\omega))\]
结论：正、余弦信号作用于线 **性时不变系统** 时，其输出的零状态响应 $y(t)$ 仍为同频率的正、余弦信号。
1. 输出信号的幅度 $y(t)$ 由系统的幅度响应 $|H(jω)|$ 确定
1. 输出信号的相位相对于输入信号偏移了 $\theta(\omega)$, 输出信号相对输入信号延迟了 $-\theta(\omega_0)/\omega_0$
####2.任意周期信号通过系统的响应
将周期为 $T_0$ 的周期信号 $f(t)$ 用Fourier级数展开为
\[f(t)=\sum_nC_ne^{jn\omega_0t}(\omega_0=2\pi/T_0)\]
利用 **虚指数信号** $e^{jωt}$ 作用在系统上响应的特点及 **线性特性** 可得系统的零状态响应为
\[y(t)=\sum^\infty_{n=-\infty}C_nT\{e^{jn\omega_0t}\}=\sum^\infty_{n=-\infty}C_nH(jn\omega_0)e^{jn\omega_0t}\]
若 $f(t)、h(t)$ 为 **实函数**，则有
\[y(t)=C_0H(j0)2+\sum^\infty_{n=1}Re\{C_nH(jn\omega_0)e^{jn\omega_0t}\}\]
##系统响应频域分析小结
###优点
求解系统的零状态响应时，可以直观地体现信号通过系统后信号频谱的改变，解释激励与响应时域波形的差异，物理概念清楚。
###不足
1. 只能求解系统的零状态响应，系统的零输入响应仍按时域方法求解。
1. 若激励信号不存在傅里叶变换，则无法利用频域分析法。
1. 频域分析法中，傅立叶反变换常较复杂。
###解决方法
采用 **拉普拉斯变换**
##III.无失真系统与理想低通
###i.无失真传输系统
####定义
输出信号和输入信号相比, 输出信号只在信号 **幅度因子** 上和 **出现时间** 上与输入信号有变化

若输入信号为 $f(t)$，则无失真传输系统的输出信号 $y(t)$ 应为
\[y(t)=K\cdot f(t-t_d)\]
$K$ 为常数，$t_d$ 是输入信号通过系统后的延迟时间。
####频率响应
\[\because Y(j\omega)=KF(j\omega)e^{-j\omega t_d}\\
\therefore H(j\omega)=\frac{Y(j\omega)}{F(j\omega)}=Ke^{-j\omega t_d}\]
####幅度响应 相位响应
\[|H(j\omega)|=K\quad \theta(\omega)=-\omega t_d\]
####无失真传输系统应满足两个条件:
1. 系统的幅频响应 $|H(jω)|$ 在整个频率范围内应为常数 $K$ ，即系统的带宽为无穷大；
1. 系统的相位响应 $\theta(\omega)$ 在整个频率范围内应与 $ω$ 成正比。
####线性系统引起的信号失真
1. 幅度失真:各频率分量幅度产生不同程度的衰减；(系统的幅频响应 $|H(jω)|$ 不为常数)
1. 相位失真:各频率分量产生的相移不与频率成正比，使响应的各频率分量在时间轴上的相对位置发生变化。(系统的相位响应 $\theta(\omega)$ 不是 $\omega$ 的线性函数)
1. 线性系统的失真: 幅度、相位变化，不产生新的频率成分。
1. 非线性系统产生非线性失真: 产生新的频率成分
###ii.理想滤波器
滤波器是指能使信号的一部分频率通过，而使另一部分频率通过很少的系统。实际应用中 根据允许通过的频率成分划分, 滤波器可以分为 **低通 $|H_{LP}(j\omega)|$**, **高通 $|H_{HP}(j\omega)|$**, **带通 $|H_{BP}(j\omega)|$**, **带阻 $|H_{BS}(j\omega)|$**
###iii.理想低通滤波器
理想低通滤波器的幅度响应:
\[H(j\omega)=\left\{\begin{aligned}e^{-j\omega t_d}\,|\omega|\leq\omega_c\\0\,|\omega|>\omega_c\end{aligned}\right.=p_{2\omega_c}(\omega)e^{-j\omega t_d}\]
**幅频响应** $|H(j\omega)|$ 在通带 $0\sim\omega_c$ 恒为1，在通带之外为0。**相频响应** $φ(\omega)$ 在通带内与 $\omega$ 成线性关系

由于理想低通滤波器的通频带不是无穷大而是有限值, 故也称 **带限系统** 信号通过带限系统后会失真 失真一方面取决于 **带限系统的通频带的宽度** 另一方面取决于 **输入信号的频带宽度**
####1.冲激响应
系统的冲激响应 $h(t)$ 就是当系统输入激励为单位冲激响应 $\delta(t)$ 时产生的输出响应 而且系统的冲激响应 $h(t)$ 与系统函数 $H(j\omega)$ 是一对Fourier变换对
\[h(t)=\frac1{2\pi}\int^\infty_{-\infty}H(j\omega)e^{j\omega t}dt=\frac1{2\pi}\int^{\omega_c}_{-\omega_c}e^{-j\omega t_d}e^{j\omega t}\\=\frac1{2\pi}\int^{\omega_c}_{-\omega_c}e^{-j\omega(t-t_d)}=\frac{\omega_c}{\pi}Sa[\omega_c(t-t_d)]\]
#####分析:
1. $h(t)$ 的波形是一个抽样函数，不同于输入信号 $\delta(t)$ 的波形，有失真。<br>
原因：**理想低通滤波器** 是一个带限系统，而冲激信号 $\delta(t)$ 的频带宽度为无穷大。<br>
减小失真方法：增加理想低通截频 $\omega_c$。 $h(t)$ 的主瓣宽度为 $2\pi/\omega_c$，$\omega_c$ 越小，失真越大。当 $ω_c\to\infty$ 时，理想低通变为 **无失真传输系统**， $h(t)$ 也变为冲激函数。
1. $h(t)$ 主峰出现时刻 $t=t_d$ 比输入信号 $\delta(t)$ 作用时刻 $t=0$ 延迟了一段时间 $t_d$ 。$t_d$ 是理想低通滤波器 **相位特性的斜率**。
1. $h(t)$ 在 $t<0$ 的区间也存在输出，可见理想低通滤波器是一个 **非因果系统**，因而它是一个 **物理不可实现** 的系统。
####2.阶跃响应
如果理想低通滤波器的输入是一个单位阶跃信号, 则系统的输出响应成为 **阶跃响应**,以符号 $g(t)$ 表示, 由于单位阶跃信号是单位冲激信号的积分 根据线性时不变系统的特性 系统阶跃信号相应应是系统冲激响应的积分:
\[g(t)=h^{-1}(t)=\int^t_{-\infty}h(\tau)d\tau\\=
\frac{\omega_c}{\pi}\int^t_{-\infty}Sa[\omega_c(\tau-t_d)]d\tau=\frac12+\frac1\pi\int^{\omega_c(t-t_d)}_0Sa(x)dx\]
####分析:
1. **阶跃响应** $g(t)$ 比输入 **阶跃信号** $u(t)$ 延迟 $t_d$ 。$t_d$ 是理想低通滤波器 **相位特性的斜率**。
1. 阶跃响应的建立需要一段时间。阶跃响应从 **最小值上升到最大值** 所需时间称为阶跃响应的 **上升时间** $t_r$。$t_r=2\pi/\omega_c$，即上升时间 $t_r$ 与理想低通 **截频** $\omega_c$ 成反比。$\omega_c$ 越大，上升时间就越短，当 $\omega_c\to\infty$ 时，$t_r\to0$。
1. 存在 **Gibbs现象** 即在间断点的前后出现了振荡，其振荡的最大峰值约为阶跃突变值的 **9%** 左右，且 **不随滤波器带宽的增加而减小**。
####结论
1. 输出响应的 **延迟时间** 取决于理想低通滤波器的 **相位特性的斜率** 。
1. 输入信号在通过理想低通滤波器后，输出响应在 **输入信号不连续点** 处产生逐渐上升或下降的波形，上升或下降的时间 **与理想低通滤波器的通频带宽度成反比**。
1. 理想低通滤波器的通带宽度与输入信号的带宽 **不相匹配** 时，输出就会失真。系统的通带宽度越大于信号的带宽，则失真越小，反之，则失真越大。
##IV.抽样与抽样定理
为了用离散信号处理方法处理连续时间信号 可以对连续时间信号 $f(t)$ 进行等间隔抽样 从而获得离散时间序列 $f(kT),k=0,\pm1,\pm2,\cdots$ T为抽样间隔或抽样周期

抽样后的离散时间序列是否包括原连续信号的全部信息, 抽样定理给出了抽样后的信号包含原连续信号全部信息的条件 可以说 抽样定理在连续时间信号和离散时间信号之间架起了一座桥
###i.信号抽样的理论分析
我们将抽样后的离散时间信号以连续时间信号表示:
\[f_s(t)=\sum^\infty_{k=-\infty}f(kT)\delta(t-kT)\]
其中 **$T$ 为抽样周期, $f_s=1/T$ 为抽样频率, $\omega_s=2\pi/T$ 为抽样角频率**

抽样信号等价为:
\[f_s(t)=f(t)\cdot\delta_T(t)\]
若连续信号 $f(t)$ 的频谱函数为 $F(j\omega)$，则为:
\[F_s(j\omega)=\frac1{2\pi}F(j\omega)*
\omega_s\sum^{+\infty}_{n=-\infty}\delta(\omega-n\omega_s)\\\xrightarrow{冲激信号卷积特性}\frac{\omega_s}{2\pi}\sum^{+\infty}_{n=-\infty}F[j(\omega-n\omega_s)]\quad \omega_s=\frac{2\pi}T\]
有理想抽样信号的频谱是周期的, 其周期为 $\omega_s$ 对连续信号的频谱位移 **整数倍**, 再对所有这些频谱求和即可得出理想抽样信号的频谱

设实信号 $f(t)$ 是带限的, 即在 $|\omega|>\omega_m$ 时信号的频谱为零 成 $\omega_m$ 为信号的最高角频率 记 $F_n(j\omega)=F(j(\omega-n\omega_s))$ 随着角频率的降低 相邻的 $F_n(j\omega)$ 之间的间隔将会减小 这就使得 **相邻部分的 $F_n(j\omega)$ 有可能发生重叠** 导致抽样信号频谱失真 这种由 **非零值重叠引起的失真称为混叠(Aliasing)**
####过抽样 $\omega_s>2\omega_m$
抽样信号 $f_s(t)$ 包括了原信号 $f(t)$ 所有的信息 可以从抽样信号恢复原信号
####临界抽样 $\omega_s=2\omega_m$
抽样信号频谱没有发生混叠 但是再降低抽频率 抽样信号的频谱将发生混叠
####混叠 $\omega_s<2\omega_m$
相邻的 $F_n(j\omega)$ 的非零部分发生了重叠 使抽样信号发生了混叠 这意味着抽样信号 $f_s(t)$ 丢失了原信号 $f(t)$ 中的部分信息 这时不可能从抽样信号恢复原信号
###ii.时域抽样定理
若带限信号 $f(t)$ 的最高角频率为 $\omega_m$，则信号 $f(t)$ 可以用 **等间隔的抽样值** 唯一地表示。而抽样间隔 $T$ 需不大于 $1/2f_m$，或最低抽样频率 $f_s$ 不小于 $2f_m$。

若从抽样信号 $f_s(t)$ 中恢复原信号 $f(t)$，需满足两个条件：
1. $f(t)$ 是 **带限信号**，即其频谱函数在 $|\omega|>\omega_m$ 各处为零；
1. 抽样间隔 $T$ 需满足， 或抽样频率 $f_s$ 需满足 $fs\geq2f_m(或\omega_s\geq2ω m)$。**$f_s=2f_m$** 为使信号不发生混叠的 **最小抽样频率**，称为Nyquist 频率. **$T=1/(2f_m)$** 是使信号不发生混叠的 **最大抽样间隔**, 成为Nyquist 间隔.
###iii.抽样定理的工程应用
许多实际工程信号不满足带限条件
\[f(t)\to\underbrace{抗混低通滤波器}_{h(t)}\to f_1(t)\]
###iv.实际应用举例
利用离散系统处理连续时间信号
\[f(t)\to[A/D]\xrightarrow{f[k]}H(z)\xrightarrow{y[k]}[D/A]\to y(t)\]
1. 生物医学信号处理
1. 铁路控制信号识别
###v.信号重建
信号的重建指从抽样信号 $f_s(t)$ 中恢复原信号 $f(t)$ 的过程

要从抽样信号 $f_s(t)$ 中恢复原信号 $f(t)$ 可用一个 **理想低通滤波器** 对抽样信号 $f_s(t)$ 进行滤波 理想低通滤波器的 **幅度响应** 在通频带内为常数 $T$ 理想低通滤波器的 **截止角频率** 为 $\omega_c(\omega_m<\omega_c\leq\omega_s/2)$ 即:
\[H_r(j\omega)=\begin{cases}T&|\omega|<\omega_c\\0&|\omega|>\omega_c\end{cases}\]
抽样信号 $f_s(t)$ 通过该理想低通滤波器即可恢复原信号 $f(t)$
####分析
取 **$\omega_c=\omega_s/2$** 得理想重建滤波器的冲激响应为
\[h_r(t)=\mathscr{F}^{-1}[H_r(j\omega)]=Sa(\frac{\omega_st}2)\]
在取样点上 即 $t=kT$ 时, 有:
\[h_r(kT)=Sa(\frac{\omega_skT}2)=Sa(\pi k)=\delta[k]\]
即 $h_r(t)$ 除了在 $t=0$ 时, 在其他抽样点上的值均为0, 当将抽样信号 $f_s(t)$ 加到系统 $h_r(t)$ 的输入端 系统输出为 $f(t)$ $f_s(t)$ 的每一个冲激经过系统后将产生一个幅度等于冲激强度的抽样脉冲信号 对所有的抽样脉冲信号求和即得 $f(t)$ $f_s(t)$ 的第k个冲激为 $f(kT)\delta(t-kT)$ 该冲激通过滤波器产生的脉冲为 $f(kT)h_r(t-kT)$ 由 **系统的线性特性** 得 $f_s(t)$ 通过滤波器的输出为 $f(t)$ 为:
\[f(t)=\sum_kf(kT)h_r(t-kT)=\sum_kf(kT)Sa(\omega_s(t-kT)/2)\\
=\sum_kf(kT)Sa(\omega_st/2-\pi k)\]
上式为内插公式 即在满足抽样定理的条件下 可由信号在抽样点的值进行内插来恢复原信号 $f(t)$
##V.调制与解调
//TBD
##VI.离散时间系统的频域分析
##VII.离散信号通过系统的响应
###i.离散系统的频率响应
离散系统的频率响应定义为
\[DTFT\{h[k]\}=H(e^{j\Omega})=|H(e^{j\Omega})|e^{j\phi(\Omega)}\]
DTFT = Discrete-time Fourier Transform 离散时间傅里叶变换

幅度响应: $|H(e^{j\Omega})|$ 相位响应: $\phi(\Omega)$ 群延迟: $\tau(\Omega)=-\displaystyle\frac{d\phi(\Omega)}{d\Omega}$
###ii.$e^{j\Omega k}$ 通过LTI系统的稳态响应
设离散LTI系统的单体脉冲响应为 $h[k]$, 但系统输入的是角频率为 $\Omega$ 的虚指数信号 零状态响应可以通过 $e^{j\Omega k}$ 和 $h[k]$ 卷积和来求出 即
\[y[k]=e^{j\Omega k}* h[k]=\sum_ne^{j\Omega(k-n)}h[n]\\=e^{j\Omega k}\sum_ne^{j\Omega n}h[n]=e^{j\Omega k}H(e^{j\Omega})\]
\[e^{j\Omega k}\to H(e^{j\Omega})\to e^{j\Omega k}H(e^{j\Omega})\]
###iii.任意信号通过系统的响应
\[f[k]=\frac1{2\pi}\int^\pi_{-\pi}F(e^{j\Omega})e^{j\Omega k}d\Omega\]
\[T\{f[k]\}=\frac1{2\pi}\int^\pi_{-\pi}F(e^{j\Omega})T\{e^{j\Omega k}\}d\Omega\\=\frac1{2\pi}\int^\pi_{-\pi}F(e^{j\Omega})H(e^{j\Omega})e^{j\Omega k}d\Omega\]
\[F(e^{j\Omega k})\to H(e^{j\Omega})\to H(e^{j\Omega})F(e^{j\Omega k})\]
###iv.信号通过线性相位系统的响应
\[H(e^{j\Omega})=|H(e^{j\Omega})|e^{j\phi(\Omega)}\]
**线性相位** 系统: $\phi(\Omega)=-\Omega_0k_0$ <br>
**线性相位** 系统的群延迟: $\tau(\Omega)=k_0$ <br>
$\displaystyle f[k]=\sum^{N-1}_{m=0}F[m]e^{j\Omega_mk}$, 通过线性相位系统的响应为
\[y[k]=\sum^{N-1}_{m=0}F[m]|H(e^{j\Omega_m})|e^{-j\Omega_mk_0}e^{j\Omega_mk}\]
\[y[k]=\sum^{N-1}_{m=0}F[m]|H(e^{j\Omega_m})|e^{-j\Omega_m(k-k_0)}\]
###v.理想数字滤波器
**理想低通 $|H_{LP}(j\omega)|$**, **理想高通 $|H_{HP}(j\omega)|$**, **理想带通 $|H_{BP}(j\omega)|$**, **理想带阻 $|H_{BS}(j\omega)|$**
