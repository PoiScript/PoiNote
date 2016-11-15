#连续时间信号与系统的S域分析
##I.连续时间信号的复频域分析
###n.傅里叶变换的缺陷
1. 某些信号不存在Fourier变换，无法利用频域分析方法
1. 频域分析方法只能求解系统的零状态响应，而不能求解零输入响应
1. 频域分析方法中，Fourier反变换一般比较复杂
###i.从傅立叶变换到拉普拉斯变换
####1.推导:
\[f(t)=e^{αt}u(t)(\alpha>0)傅里叶变换\to不存在\]
\[将f(t)乘以衰减因子e^{-σt}\]
\[F[f(t)e^{-\sigma{}t}]=\int^{\infty}_{\infty}f(t)e^{-\sigma{}t}e^{-j\omega{}t}dt=\int^{\infty}_{\infty}f(t)e^{-(\sigma+j\omega )t}dt\]
\[令s=\sigma+j\omega\quad\int^{\infty}_{-\infty}f(t)e^{-st}dt=F(s)\]
####2.定义:
\[拉普拉斯正变换:\quad{}F(s)=\int^{\infty}_{-\infty}f(t)e^{-st}dt\]
####3.对 $f(t)e^{-\sigma{}t}$ 求傅里叶反变换可推出:
\[拉普拉斯反变换:\quad{}f(s)=\frac1{2\pi{}j}\int^{\sigma+j\omega}_{\sigma-j\omega}F(t)e^{st}dt\]
####4.拉普拉斯变换符号表示及物理含义:
#####符号表示:
\[F(s)=L[f(t)]\quad{}f(t)=L^{-1}[F(s)]\quad{}f(t)\xrightarrow{L}F(s)\]
#####物理含义:
信号 $f(t)$ 可分解成复指数 $e^{st}$ 的线性组合<br>
$F(s)$ 为单位带宽内各谐波的合成振幅，是密度函数。<br>
$s$ 是复数称为复频率，$F(s)$ 称复频谱。
###ii.单边拉普拉斯变换及其存在的条件
####1.单边拉普拉斯变换
\[F(s)=\int^{\infty}_{0^-}f(t)e^{-st}dt\\f(s)=\frac1{2\pi{}j}\int^{\sigma+j\omega}_{\sigma-j\omega}F(t)e^{st}dt\]
#####关于积分下限的说明:
1. 积分下限定义为 **零的左极限** ，目的在于分析和计算时可以直接利用起始给定的 $0^-$ 状态。
1. 一般把积分下限简写为 0 ，含义与 $0^-$ 相同。
####2.单边拉普拉斯变换存在的条件
\[充分条件为:\quad{}\int^{\infty}_{-\infty}|f(t)e^{-\sigma{}t}|dt<\infty,\sigma\in{}R\]
对任意信号 $f(t)$ ，若满足上式，则 $f(t)$ 应满足:
\[\lim_{t\to\infty}f(t)e^{-\sigma{}t}=0,(\sigma\cdot\sigma_0)\]
###iii.常用信号的拉普拉斯变换
####1.指数型函数 $e^{\lambda{}t}u(t)$
\[L[e^{\lambda{}t}u(t)]=\int^{\infty}_{0^-}e^{\lambda{}t}e^{-st}dt=\frac1{s-\lambda}\quad\sigma>\lambda\]
\[e^{-\lambda{}t}u(t)\xrightarrow{L}\frac1{s-\lambda}\quad\sigma>-\lambda\]
\[e^{j\omega_0t}u(t)\xrightarrow{L}\frac1{s-j\omega_0}\quad\sigma>0\]
\[e^{(\sigma_0+j\omega_0)t}u(t)\xrightarrow{L}\frac1{s-(\sigma_0+j\omega_0)}\quad\sigma>\sigma_0\]
#####正弦信号
\[\cos(\omega_0t)u(t)=\frac{e^{j\omega_0t}+e^{-j\omega_0t}}2u(t)\xrightarrow{L}\frac1{2}(\frac1{s-j\omega_0}+\frac1{s+j\omega_0})=\frac{s}{s^2+\omega^2_0},\sigma>0\]
\[\sin(\omega_0t)u(t)=\frac{e^{j\omega_0t}-e^{-j\omega_0t}}2u(t)\xrightarrow{L}\frac1{2}(\frac1{s-j\omega_0}-\frac1{s+j\omega_0})=\frac{\omega_0}{s^2+\omega^2_0},\sigma>0\]
####2.阶跃函数 $u(t)$
\[L[u(t)]=\lim_{\lambda\to0}L[e^{\lambda{}t}u(t)]=\frac1s,\sigma>0,Re(s)>0\]
####3.冲激信号 $\delta(t)\quad\delta^{(n)}(t)$
\[L[\delta(t)]=\int^{\infty}_{0^-}\delta(r)e^{-st}dt=1,Re(s)>-\infty\]
\[L[\delta'(t)]=\int^{\infty}_{0^-}\delta'(t)e^{-st}dt=-\frac{d}{ds}(e^{-st})|_{t=0}=s\]
\[L[\delta^{(n)}(t)]=\int^{\infty}_{0^-}\delta^{(n)}(t)e^{-st}dt=(-1)^{(n)}\frac{d^n}{ds^n}(e^{-st})|_{t=0}=s^n\]
####4. t 的正幂函数 $t_n$，n为正整数，t>0
\[L[t^n]=\int^{\infty}_{0^-}(t^n)e^{-st}=-\frac{t^n}s(e^{-st})|^{\infty}_{0^-}t^{n-1}e^{-st}dt\\=\frac{n}s\int^{\infty}_{0^-}t^{n-1}e^{-st}dt=\frac{n}sL[t^{n-1}]\]
根据以上推理:
\[t^n\xrightarrow{L}\frac{n!}{s^{s+1}},Re(s)>0\]
###iv.拉普拉斯变换与傅里叶变化的关系
###v.拉普拉斯变换的性质
###vi.拉普拉斯变换反变换
####1.计算拉普拉斯反变换方法
1. 利用复变函数中的 **留数定理** => 直接由Laplace反变换
\[f(t)=\frac1{2\pi{}j}\int^{\sigma+j\omega}_{\sigma-j\omega}F(s)e^{st}ds\]
2. 采用 **部分分式展开法** => 分解成简单表示式之和，然后得到原信号
####2.留数法
\[f(t)=\frac1{2\pi{}j}\int^{\sigma+j\omega}_{\sigma-j\omega}F(s)e^{st}ds\]
上述积分式等于围线中被积函数 $F(s)e^{st}ds$ 所有极点的留数之和。<br>
设在极点 $s=p_i$ 处的留数为 $r_i$ ，并设 $F(s)e^{st}ds$ 在围线中共有n个极点。
#####计算留数的方法:
1. 若极点 $s=p_i$ 为 $F(s)e^{st}ds$ 的单极点:
\[r_i=[(s-p_i)F(s)e^{st}]_{s=p_i}\]
2. 若极点 $s=p_i$ 为 $F(s)e^{st}ds$ 的k阶极点:
\[r_i=\frac1{(k-1)!}[\frac{d^{k-1}}{ds^{k-1}}(s-p_i)^kF(s)e^{st}]_{s=p_i}\]
####3.部分分式展开法
归纳
\[F(s)=\frac{N(s)}{D(s)}=\frac{b_ms^m+b_{m-1}s^{m-1}+\cdots+b_1s+b_0}{s^n+a_{n-1}s^{n-1}+\cdots+a_1s+a_0}\]
1. F(s) 为有理真分式 (m<n)，极点为一阶极点, F(s) 可分解为:
\[F(s)=\frac{N(s)}{D(s)}=\frac{N(s)}{(s-p_1)(s-p_2)\cdots(s-p_n)}=\frac{k_1}{s-p_1}+\frac{k_2}{s-p_2}+\cdots+\frac{k_n}{s-p_n}\]
\[\therefore{}k_i=(s-p_i)F(s)|_{s=p_i}\quad{}i=1,2,\cdots,n\]
\[\therefore{}f(t)=(k_1e^{p_1t}+k_2e^{p_2t}+\cdots+k_ne^{p_nt})u(t)\]
2. F(s) 为有理真分式 (m<n)，极点为r重阶极点, F(s) 可分解为:
\[F(s)=\frac{N(s)}{D(s)}=\frac{N(s)}{(s-p_1)^r(s-p_{r+1})\cdots(s-p_n)}=\\\frac{k_1}{s-p_1}+\frac{k_1}{(s-p_1)^2}+\cdots+\frac{k_1}{(s-p_1)^r}+\frac{k_{r+1}}{s-p_{r+1}}+\cdots\frac{k_n}{s-p_n}\]
3. F(s)为有理假分式 (m≥n), 将 F(s) 分解为 s 的多项式与有理真分式两部分, 即:
\[F(s)=\frac{N(s)}{D(s)}=B_0+B_1s+\cdots+B_{m-n}s^{m-n}+\frac{N_1(s)}{D(s)}\]
式中, $\frac{N(s)}{D(s)}$ 为真分式, 可根据极点情况按 1/2 展开 多项式部分对应冲激和冲激的高阶导数,即:
\[B_0\xrightarrow{L}B_0\delta(s)\quad{}B_1s\xrightarrow{L}B_1\delta'(t)\quad{}B_{m-n}s^{m-n}\xrightarrow{L}B_{m-n}\delta^{(m-n)}(t)\]
####4.总结
1. 从以上分析可以看出，当F(s)为有理分式时，可利用部分分式分解和查表的方法求得逆变换，无需引用留数定理。
1. 如果F(s)表达式为有理分式与e-st相乘时，可再借助延时定理得出逆变换。
1. 当F(s)分母为二次多项式时，可进行配方。
1. 当F(s)为无理函数时，需利用留数定理求逆变换，然而，这种情况在电路分析问题中几乎不会遇到。
1. 信号的复频域分析实质是将信号分解为 **复指数信号的线性组合**。
1. 信号的复频域分析使用的数学工具是 **拉普拉斯变换**。
1. 利用基本信号的复频谱和拉普拉斯变换的性质可对任意信号进行复频域分析。
1. 复频域分析主要用于 **线性系统** 的分析。
##II.连续时间系统的复频域分析
###i.微分方程描述系统的S域分析
时域微分方程 -解微分方程-> 时域响应y(t) =拉氏变换=> S域代数方程 -解代数方程-> S域响应Y(s)<br>
描述n阶线性时不变连续时间系统的微分方程为:
\[a_ny^{(n)}(t)+a_{n-1}y^{(n-1)}(t)+\cdots+a_1y'(t)+a_0y(t)=b_mf^{(m)}(t)+b_{m-1}f^{(m-1)}(t)+\cdots+b_1f'(t)+b_0f(t)\\\Rightarrow\sum^n_{i=0}a_iy^{(i)}(t)=\sum^m_{j=0}b_jf^{(j)}(t)\]
根据时域微分特性,有:
\[L[y^{(i)}(t)]=s^iY(s)-s^{s-1}y(0^-)-s^{i-2}y'(0^-)-\cdots-y^{(i-1)}(0^-)\Rightarrow{}L[f^{(j)}(t)]=s^jF(s)\]
原方程的单边Laplace变换式为:
\[\sum^n_{i=1}a_i[s^iY(s)-s^{i-1}y(0^-)-s^{i-2}y(0^-)-\cdots-y^{(i-1)}(0^-)]+a_0Y(s)=\sum^m_{j=0}b_js^{j}F(s)\\Y(s)=\frac{\displaystyle\sum^n_{i=1}a_i[s^{i-1}y(0^-)+s^{i-2}y'(0^-)+\cdots+y^{(i-1)}(0^-)]}{\displaystyle\sum^n_{i=0}a_is^i}+\frac{\displaystyle\sum^m_{j=0}b_js^j}{\displaystyle\sum^n_{i=0}a_is^i}F(s)\]
零输入响应的s域表达式为:
\[Y_x(s)=\frac{\displaystyle\sum^n_{i=1}a_i[s^{i-1}y(0^-)+s^{i-2}y'(0^-)+\cdots+y^{(i-1)}(0^-)]}{\displaystyle\sum^n_{i=0}a_is^i}\]
零状态响应的s域表达式为:
\[Y_f(s)=\frac{\displaystyle\sum^m_{j=0}b_js^j}{\displaystyle\sum^n_{i=0}a_is^i}F(s)\]
对 $Y_x(s)$ 和 $Y_f(s)$ 进行 Laplace反变换, 可得零输入响应和零状态响应的时域表达式,即:
\[y_x(t)+L^{-1}[Y_x(s)]\quad{}y_f(t)=L^{-1}[Y_f(s)]\]
####二阶系统响应的S域求解
\[\frac{d^2y(t)}{dt^2}+a_1\frac{dy(t)}{dt}+a_2y(t)=b_0\frac{d^2f(t)}{dt^2}+b_1\frac{df(t)}{dt}+b_2f(t)\]
已知 $f(t),y(0^-),y'(0^-)$ 求 y(t)<br>
求解过程:
1. 经 **拉氏变换** 将域微分方程变换为s域代数方程
1. 求解s域代数方程，求出 $Y_x(s),Y_f(s)$
1. **拉氏反变换**，求出响应的时域表示式
\[\underbrace{[s^2Y(s)-sy(0^-)-y'(0^-)]}_{f''(t)}+\underbrace{a_1[sY(s)-y(0^-)]}_{a_1y'(t)}+\underbrace{a_2Y(s)}_{a_2y(t)}=b_0s^2F(s)+b_1sF(s)+b_2\underbrace{F(s)}_{b_0f''(t)+b_1f'(t)+b_2f(t)}\]
\[Y(s)=\underbrace{\frac{sy(0^-)+y'(0^-)+a_1y(0^-)}{s^2+a_1s+a_2}}_{Y_x(s)}+\underbrace{\frac{b_0s^2+b_1s+b_2}{s^2+a_1s+a_0}F(s)}_{Y_f(s)}\]
\[y(t)=y_f(t)+y_x(t)=L^{-1}\{Y_f(s)+Y_x(s)\}\]
###ii.电路的S域模型
|时域|复频域|
|--|--|
|$\displaystyle v_R(t)=Ri_R(T)$|$\displaystyle V_R(s)=RI_R(s)$|
|$\displaystyle v_L(t)=L\frac{di_L(t)}{dt}$|$\displaystyle V_L(s)=sLI_L(s)-Li_L(0)$|
|$\displaystyle v_c(t)=\frac1C\int^t_{-\infty}i_c(\tau)d\tau$|$\displaystyle V_c(s)=\frac1{sC}I_c(s)+\frac1sv_c(0^-)$|
##III.连续时间系统函数 $H(s)$ 与系统特性
###i.系统函数 $H(s)$
####1.定义
系统在零状态条件下，输出的拉氏变换式与输入的拉式变换式之比，记为 $H(s)$。
\[H(s)=\frac{L[y_f(t)]}{L[f(t)]}=\frac{Y_f(s)}{F(s)}\]
####2. $H(s)$ 与 $h(t)$ 的关系
\[\because{}y_f(t)=F(s)L[h(t)]\\\therefore{}H(s)=\frac{Y_f(s)}{F(s)}=L[h(t)]\]
系统函数 $H(t)$ 是该系统冲激响应 $h(t)$ 的Laplace变换
####3.S域求零状态响应
\[f(t)\to{}h(t)\to{}y_f(t)=f(t)* h(t)\\F(s)\to{}H(s)\to{}Y_f(s)=F(s)H(s)\]
####4.求 $H(s)$ 的方法
1. 由系统的冲激响应求解：$H(s)=L[h(t)]$
1. 由定义式 $H(s)=\displaystyle\frac{L[y_f(t)]}{L[f(t)]}$
1. 由系统的微分方程写出 $H(s)$
###ii.零极点与系统时域特性
####1.零极点分布:
\[H(s)=\frac{b_ms^m+b_{m-1}s^{m-1}+\cdots+b_1s+b_0}{s^n+a_{n-1}s^{n-1}+\cdots+a_1s+a_0}\\=b_m\frac{(s-r_1)(s-r_2)\cdots(s-r_m)}{(s-s_1)(s-s_2)\cdots(s-s_n)}\]
####2. $H(s)$ 与 $h(t)$ 的关系
1. 位于σ 轴的单极点

H(s)|零极点|h(t)
:--:|:--:|:--:
$\displaystyle\frac1{s+1}$|(-1,0)|$e^{-t}u(t)$
$\displaystyle\frac1s$|(0,0)|$u(t)$
$\displaystyle\frac1{s-1}$|(1,0)|$e^tu(t)$
2. 共轭单极点

H(s)|零极点|h(t)
:--:|:--:|:--:
$\displaystyle\frac1{(s+1+j)(s+1-j)}$|(-1,1)(-1,-1)|$\sin(t)e^{-t}u(t)$
$\displaystyle\frac1{(s+j)(s-j)}$|(0,1)(0,-1)|$\sin(t)u(t)$
$\displaystyle\frac1{(s-1+j)(s-1-j)}$|(1,1)(1,-1)|$\sin(t)e^tu(t)$
###iii.零极点与系统频响特性
###连续系统的稳定性
##IV.连续时间系统的模拟
