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
##II.连续时间系统的复频域分析
##III.连续时间系统函数与系统特性
##IV.连续时间系统的模拟