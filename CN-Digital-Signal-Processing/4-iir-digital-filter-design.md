数字滤波器是一个离散系统, 其系统函数一般可表示为 $z^{-1}$ 的有理多项式形式, 即:

$$H(z)=\frac{\displaystyle\sum_{j=0}^Mb_jz^{-j}}{1+\displaystyle\sum_{i=1}^Na_iz^{-i}}=\frac{b_0+b_1z^{-i}+\cdots+b_Nz^{-1}}{1+a_0+a_1z^{-1}+\cdots+b_Mz^{-1}}$$

- $M\ge1$, $M$ 为 IIR(Infinite-Implues Response) 滤波器阶数, 反馈环个数. 有反馈环, 无限脉冲响应.

- $A(z)=1$, 脉冲响应长度 $N+1$, FIR(Finite-Implues Response) 滤波器.

#### IIR 数字滤波器:

- 优点: 直接利用模拟滤波器设计成果.

- 缺点: 存在反馈, 不稳定, 数字运算可能溢出.

#### FIR 数字滤波器:

- 优点: 不存在极点, 绝对稳定, 有线性位移, 实现简单.

- 缺点: 性能不如 IIR 滤波器.

数字滤波器的衰减响应:

$$A(\Omega)=-10\lg|H(j\omega)|^2=-20\lg|H(j\omega)|\text{dB}$$

数字滤波器的增益响应:

$$G(\Omega)=-A(\Omega)=10\lg|H(j\omega)|^2\text{dB}$$

由于模拟滤波器设计技术已经非常成熟, 且可得闭合形式的解, 因此在设计 IIR 滤波器时, 一般是通过模拟滤波器来设计数字滤波器.

1. 待设计数字滤波器指标 (频率转换)

2. 模拟滤波器指标 (设计模拟滤波器) 比较常见的模拟低通滤波器有 Butterworth 和 Chebyshev 等

3. 模拟滤波器 $H(s)$ (s 到 z 域转换) 主要方法有脉冲响应不变法和双线性变换法

4. 数字滤波器 $H(z)$

模拟滤波器的设计是基础, 模拟滤波器到数字滤波器的转换是核心.

# IIR 数字滤波器的设计

模拟滤波器的设计指标和数字滤波器类似, 有通带截频 $\{\omega_p(\text{rad/s})\}$, 通带最大衰减 $A_p$, 阻带截频 $\{\omega_s(\text{rad/s})\}$, 阻带最大衰减 $A_s$.

设计模拟滤波器的时候, 先将待设计的模拟滤波器的技术指标转换为模拟低通滤波器的技术指标, 然后设计模拟低通滤波器, 再通过频率变换将模拟低通滤波器转换为所需的滤波器.

## I. 模拟低通滤波器设计

### 1. Butterworth 模拟低通滤波器

幅度响应的模方

$$|H(j\Omega)|^2=\frac1{1+(\omega/\omega_c)^{2N}}$$

$N$ 为滤波器阶数, $\omega_c$ 为 3dB 截止频率, 即 $A(\omega_c)=-20\lg|H(j\omega_c)|\approx3\text{dB}$.

当 $\omega_c=1$ 时, Butterworth 模拟低通滤波器称为归一化的 Butterworth 模拟低通滤波器.

#### 特性:

1. $|H(j0)|^2=1$, $|H(j\infty)|^2=0$

2. $\displaystyle\frac{d|H(j\omega)|^2}{d\omega}=-\frac{2N(\omega/\omega_c)^{2N-1}}{(1+(\omega/\omega_c)^{2N})^2}<0$, 所以幅度响应随着 $\omega$ 的增加而单调递减

3. $|H(j\omega)|^2$ 在 $\omega=0$ 处从 1 到 $2N-1$ 阶导数为 0, 即在 $\omega=0$ 具有最大的平坦性. Butterworth 也称为在 $\omega=0$ 处具有最大的平坦性的滤波器.

#### 设计步骤:

##### 1. 由滤波器指标 $\omega_p,\omega_s,A_p,A_s$ 确定滤波器的阶数 $N$:

$$1+\left(\frac{\omega_p}{\omega_c}\right)^{2N}=10^{0.1A_p}$$

$$1+\left(\frac{\omega_s}{\omega_c}\right)^{2N}=10^{0.1A_s}$$

滤波器阶数 $N$ 为:

$$N\ge\frac{\displaystyle\lg\left(\frac{10^{0.1A_s}}{10^{0.1A_p}}\right)}{\displaystyle2\lg(\omega_s/\omega_p)}$$

##### 2. 确定 $\omega_c$:

$$\frac{\omega_p}{(10^{0.1A_p}-1)^{1/2N}}\le\omega_c\le\frac{\omega_s}{(10^{0.1A_s}-1)^{1/2N}}$$

##### 3. 计算 $s$ 左半平面的 N 个极点.

$$|H(j\omega)|^2=H(j\omega)H^*(j\omega)=H(j\omega)H(-j\omega)=H(s)H(-s)|_{s=j\omega}$$

故有:

$$H(s)H(-s)=\frac1{1+\left(-j\displaystyle\frac s{\omega_c}\right)^{2N}}$$

Butterworth 模拟低通滤波器只有极点, 没有零点, 是全极点系统. $H(s)$ 和 $H(-s)$ 的极点为:

$$s_k=(-1)^{1/N}j\omega_c=\{e^{-j\pi+2\pi k}\}^{1/2N}j\omega_c=\omega_ce^{j\pi\left(\frac12+\frac{2k-1}{2N}\right)},k=1,2,\cdots,2N$$

为了保证滤波器的稳定, 必须选取 $s$ 左半面的 N 个极点构成系统函数 $H(-s)$, 即:

$$s_k=\omega_ce^{j\pi\left(\frac12+\frac{2k-1}{2N}\right)},k=1,2,\cdots,2N$$


##### 4. 确定滤波器的系统函数 $H(s)$
$$H(s)=\prod^N_{k=1}\frac{-s}{s-s_k}$$
