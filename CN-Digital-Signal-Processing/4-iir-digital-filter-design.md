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

### i. Butterworth 模拟低通滤波器

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

### ii. Chebyshev 模拟低通滤波器

Butterworth 模拟低通滤波器的幅度响应, 无论在通带还是阻带都是随频率而单调变化, 设计出的滤波器的在通带和阻带内都存在许多裕量, 若能设计指标的精度均匀分布在通带或阻带内内, 或同时均匀分布在通带和阻带内, 则可以降低滤波器的阶数. 这种精度均匀分布的滤波器可以通过选择具有等纹波特性的逼近函数来完成.

Chebyshev 模拟低通滤波器幅度响应在一个频带中具有等波纹特性. Chebyshev I 型模拟低通滤波器的幅度响应在通带是等波纹的, 在阻带单调下降. Chebyshev II 型模拟低通滤波器的幅度响应在通带单调下降, 而在阻带是等波纹.

#### 1. Chebyshev I 型模拟低通滤波器

幅度响应的模方:

$$|H(j\omega)|^2=\frac1{1+\varepsilon^2C^2_N(\omega/\omega_c)}$$

$N$ : 滤波器阶数, $\varepsilon$ 和 $\omega_c$ : 滤波器参数, $C_N$ : N 阶 Chebyshev 多项式, 定义:

$$C_N(x)=\begin{cases}\cos[N\arccos(x)]&|x|\le1\\\cosh[N\text{arccosh}(x)]&|x|>1\end{cases}$$

##### 幅度响应特性:

1. $|H(j0)|^2$ 在 $\omega=0$ 时的值为 $|H(j0)|^2=\begin{cases}1&\text{N is odd}\\1/(1+\varepsilon^2)&\text{N is even}\end{cases}$

2. 当 $0\le\omega\le\omega_c$ 时, $|H(j\omega)|^2$ 在最小值 $1/(1+\varepsilon^2)$ 和最大值 1 之间等幅波动. 参数 $\varepsilon$ 控制了滤波器幅度响应在通带波动的大小.

3. 当 $\omega\ge\omega_c$ 时, $|H(j\omega)|^2$ 单调下降. N 越大, 下降速度越快. 所以 CB I 型模拟低通滤波器阻带衰减主要由 N 确定.

##### 设计步骤:

1. 由通带截频 $\omega_p$ 确定 $\omega_c$:

$$\omega_c=\omega_p$$

2. 由通带衰减 $A_p$ 确定 $\varepsilon$:

$$\varepsilon=\sqrt{10^{0.1A_p}-1}$$

3. 确定 $\omega_c$ 和 $\varepsilon$ 之后, 求出阶数 N:

$$N\ge\frac{\displaystyle\text{arccosh}(\frac1\varepsilon\sqrt{10^{0.1A_p}-1})}{\text{arrcosh}(\omega_s/\omega_p)}$$

4. 由模方 $|H(j\omega)|^2$ 求滤波器的极点:

$$s_k=\omega_c[-\sinh(\beta)\sin\frac{(2k-1)\pi}{2N}-j\cosh(\beta)\cos\frac{(2k-1)\pi}{2N}],k=1,2,\cdots,N$$

$$\beta=\frac{\text{arcsinh}(1/\varepsilon)}N$$

5. 由极点确定系统函数 $H(s)$:

$$H(s)=\prod^N_{k=1}\frac{H_0}{s-s_k}$$

$H_0$ 为设计滤波器的 $|H(j\omega)|^2$ 满足 $\omega=0$ 时的取值:

$$H_0=\begin{cases}\prod^N_{k=1}-s_k&\text{N is odd}\\\prod^N_{k=1}(-s_k)/\sqrt{1+\varepsilon^2}&\text{N is even}\end{cases}$$

#### 2. Chebyshev II 型模拟低通滤波器

幅度响应模方:

$$|H(j\omega)|^2=1-\frac1{1+\varepsilon^2C^2_N(\omega_c/\omega)}=\frac{\varepsilon^2C^2_N(\omega_c/\omega)}{1+\varepsilon^2C^2_N(\omega_c/\omega)}$$

特性:

1. 在 $|\omega|>\omega_c$ 时有:

$$0\le|H(j\omega)|^2\le\frac{\varepsilon^2}{1+\varepsilon^2}$$

参数 $\varepsilon$ 控制了滤波器幅度响应在阻带波动的大小

2. 对任意的 $N,\omega_c$ 和 $\varepsilon>0$, $|H(0)|=1$

3. 在通带 $0\le\omega\le\omega_c$ 时, $|H(j\omega)|^2$ 单调下降

CB I 型和 CB II 型的区别是 CB I 型在通带等波纹波动, 参数 $\varepsilon$ 控制通带波动; CB II 型在阻带等波纹波动, 参数 $\varepsilon$ 控制阻带波动.

CB II 型模拟低通滤波器既有零点, 也有极点, 设计于 CB I 型类似:

1. 由通带截断 $\omega_s$ 确定 $\omega_c$

$$\omega_s=\omega_c$$

2. 由阻带衰减 $A_s$ 确定 $\varepsilon$:

$$\varepsilon=\frac1{\sqrt{10^{0.1A_s}-1}}$$

3. 确定 $\omega_c$ 和 $\varepsilon$ 后, 根据通带衰减 $A_p$, 可求出阶数 N:

$$N\ge\frac{\text{arccosh}\left(\displaystyle\frac1{\varepsilon\sqrt{10^{0.1A_p-1}}}\right)}{\text{arccosh}(\omega_s/\omega_p)}$$

4. 由 $N,\varepsilon,\omega_c$ 查表获得 CB II 型模拟低通滤波器的系统函数 $H(s)$

### 几种模拟低通滤波器的对比

![](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/Filters_order5.svg/540px-Filters_order5.svg.png)

## II. 模拟域频率变换

若要设计高通, 带通, 带阻, 可以通过频率变换的方法实现:

1. 通过频率变换将模拟非低通滤波器技术指标转换为模拟低通滤波器(称为原型低通滤波器)

2. 通过 BW 型, CW 型和椭圆模拟低通滤波器设计原型低通滤波器

3. 通过(复)频率变换将原型低通滤波器的系统函数转换为对应的模拟滤波器的系统函数

原型模拟低通滤波器系统函数 $H_L(\bar s)$, 通带截频 $\overline{\omega_p}$ 阻带截频 $\overline{\omega_s}$, 频率响应 $H_L(j\overline\omega)$; 设计出的高通, 带通, 带阻滤波器分别为 $H_{HP}(s)$, $H_{BP}(s)$, $H_{BS}(s)$

1. 若原型低通滤波器的 $H_L(\bar s)$ 为有理函数, 则变换之后模拟滤波器 $H(s)$ 为有理函数

2. 变换后的模拟滤波器仍是稳定的, 即 $\bar s$ 的左半平面必须映射到 $s$ 的左半平面, 右半平面, 虚轴同理

### 频率变换

1. 原型低通到高通的变换:

$$\bar s=\frac{\omega_0}s,\overline\omega=\frac{\omega_0}\omega$$

变换的高通滤波器 $H_{HP}(s)$ 和原型低通滤波器 $H_L(\bar s)$ 具有相同的阶数

原型低通的通带变换到高通的阻带, 原型低通的阻带变换到高通的通带

2. 原型低通到带通的变换:

$$\bar s=\frac{s^2+\omega_0^2}{Bs},\overline\omega=\frac{\omega^2-\omega^2_0}{B\omega}$$

$\omega_0$ 是一正参数, 通常取 1

变换后的带通滤波器 $H_{HP}(s)$ 阶数是原型滤波器 $H_L(\bar s)$ 阶数的 2 倍

通带宽度 $B=\omega_{p2}-\omega_{p1}$ 中心频率 $\omega_0^2=\omega_{p1}\omega_{p2}$

3. 原型低通到带阻的变换:

$$\bar s=\frac{Bs}{s^2+\omega_0^2},\overline\omega=\frac{B\omega}{-\omega^2+\omega_0^2}$$

阻带宽度 $B=\omega_{s2}-\omega_{s1}$, 中心频率 $\omega_0^2=\omega_{s1}\omega_{s2}$

## III. 脉冲响应不变法

在将模拟滤波器 $H(s)$ 转换为数字滤波器 $H(z)$ 时, 要求模拟域到数字域的映射满足下列两个条件:

1. 两者的频率特性不变,$s$ 平面的虚轴必须映射到 $z$ 平面的单位圆上

2. 变换后的滤波器仍是稳定的, 即 $s$ 的左半平面必须映射到 $z$ 平面的单位圆内

### i. 基本原理

通过对模拟滤波器的单位冲击响应 $h(t)$ 等间隔转换来获得对应数字滤波器的单位脉冲响应 $h[k]$:

$$h[k]=h(t)|_{t=kT}=h(kT)$$

$T$ 为抽样间隔

1. 先对模拟滤波器的系统函数 $H(s)$ 进行 Laplace 你变换获得 $h(t)$

2. 再对 $h(t)$ 等间隔抽样得到 $h[k]$

3. 最后计算 $h[k]$ 的 $z$ 变换得到 $H(z)$
