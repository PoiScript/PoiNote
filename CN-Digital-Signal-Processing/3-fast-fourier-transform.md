# 离散 Fourier 变换快速算法

## I. 基 2 时间抽取 FFT 算法 (DIT)

### 1. 基 2 时间抽取 FFT 算法原理

$$X[m]=\sum^{N-1}_{k=0}x[k]W^{km}_N,m=0,1\cdots N-1$$

$$X[m]=\sum^{N/2-1}_{r=0}x[2r]W^{2rm}_N + \sum^{N/2-1}_{r=0}x[2r+1]W^{(2r+1)m}_N$$

令:

$$\,x[2r]=x_1[r],x[2r+1]=x_2[r]$$

$$X[m]=\sum^{N/2-1}_{r=0}x_1[r]W^{2rm}_N + W^m_N\sum^{N/2-1}_{r=0}x_2[r]W^{2rm}_N$$

旋转因子的可微性:

$$W^{2rm}_N=W^{rm}_{N/2}$$  

$$**X[m]=x_1[m]+W^m_Nx_2[m]**$$

旋转因子的对称性:

$$W^{mk+N/2}_N=-W^{mk}_N,(W^{mk}_N)^*=W^{-mk}_N$$

$$**X[m+\frac N2]=x_1[m+\frac N2]+W^{m+N/2}x_2[m+N/2]=x_1[m]-W^m_Nx_2[m]**$$

### 2. 基 2 时间抽取 FFT 算法复杂度

当 $N=2^M$ 时, 将分解成 $M$ 级, 每一级包含 $N/2$ 个蝶型, 共有 $\frac N2\times M=\frac N2\log_2N$ 个蝶性运算

每个蝶形运算需要 1 次复数乘法和 2 次复数加法, 共需要 $\frac N2\log_2N$ 次复数乘法, $N\log_2N$ 次复数加法.

### 3. 基 2 时间 FFT 算法结果特点

1. 原位运算

2. 序列倒序运算

3. 旋转因子分布规律:

- 第 1 级: 系数为 $W^0_N$, 节点距离为 1

- 第 2 级: 系数为 $W^0_N,W^{N/4}_N$, 节点距离为 2

- 第 3 级: 系数为 $W^0_N,W^{N/8}_N,W^{2N/8}_N,W^{3N/8}_N$, 节点距离为 4

- 第 M 级: 系数为 $W^0_N,W^1_N,\cdots,W^{(N/2-1)}_N$, 节点距离为 N/2

## II. 基 2 频率抽取的 FFT 算法 (DIF)

基 2 频率抽取 FFT 算法是将时域的序列以前后两部分按一定的方式组合后形成两个短序列,因此两个短序列的 DFT 合成的频域序列按奇偶顺序排列, 而不是按自然顺序排列.

DFT:

$$X[m]=\sum^{N-1}_{k=0}x[k]W^{km}_N,m=0,1\cdots N-1$$

自然顺序:

$$X[m]=\sum^{N/2-1}_{k=0}x[k]W^{km}_N+\sum^{N-1}_{k=N/2}x[k]W^{km}_Nx[k]W^{mk}_N$$

$$=\sum^{N/2-1}_{k=0}(x[k]+W^{mN/2}x[k+N/2])W^{mk}_N$$

$$\begin{cases}
X[2r]=\sum^{N/2-1}_{k=0}(x[k]+x[k+N/2])W^{rk}_N\\
X[2r+1]=\sum^{N/2-1}_{k=0}(x[k]-x[k+N/2])W^{rk}_N\cdot W^{rk}_N
\end{cases}\$$

$$x_1[k]=x[k]+x[k+N/2])W^{rk}_N,\,x_2[k]=x[k]-x[k+N/2])W^{rk}_N$$

$$
\begin{cases}
X[2r]=\sum^{N/2-1}_{k=0}x_1[k]\cdot W^{rk}_{N/2}\\X[2r+1]=\sum^{N/2-1}_{k=0}x_2[k]W^{rk}_{N/2}
\end{cases}$$

$$\begin{cases}
x_1[k]=x[k]+x[k+N/2]\\
x_2[k]=\{x[k]-x[k+N/2]\}W^k_N
\end{cases}$$

## III. 实序列的 DFT 计算

### 1. 利用 N 点复序列的 FFT 算法同时计算两个 N 点实序列 DFT

$x[k], h[k]$ 为 N 点实序列, $X[m], H[m]$ 分别为对应的 DFT.

$$y[k]=x[k]+jh[k]$$

$$\begin{cases}
x[k]=\frac12\{y[k]+y^*[k]\}\\
h[k]=\frac1{2j}\{y[k]-y^*[k]\}
\end{cases}$$

$$DFT\{y^*[k]\}=Y^*[(-m)_N]$$

$$\begin{cases}
X[m]=\frac12\{Y[m]+Y^*[(-m)_N]\}\\
H[m]=\frac1{2j}\{Y[m]-Y^*[(-m)_N]\}
\end{cases}$$

### 2. 利用 N 点复序列的 FFT 算法计算 2N 点序列 DFT

$y[k]$ 为一个长度为 2n 的序列

$$\begin{cases}
x_1[k]=y[2k]&0\le k \le N-1\\
x_2[k]=y[2k+1]&0\le k \le N-1
\end{cases}$$

$$\begin{cases}
Y[m]=X_1[m]+W^{m}_{2N}X_2[m]\\
Y[m+N]=X_1[m]-W^{m}_{2N}X_2[m]
\end{cases}$$

## IV. IDFT 的快速运算

$$x[k]=IDFT\{X[m]\}=\frac1N\sum^{N-1}_{m=0}X[m]W^{-mk}_N$$

$$X[m]=DFT\{x[k]\}=\sum^{N-1}_{k=0}x[k]W^{mk}_N$$

只要把 FFT 中的每个系数 $W^p_N$ 换成 $W^{-p}_N$, 并且在最后一级乘以 N/2 则时间抽取或频域抽取的 FFT 流图都可以用来实现 IDFT.

把频率抽取 FFT 流图转变为 IFFT 流图时, 应改称为按时间抽取 IFFT 流图.
把时间抽取 FFT 流图转变为 IFFT 流图时, 应改称为按频率抽取 IFFT 流图.

可以利用 DFT 于 IDFT 定义的对称性, 直接用 FFT 计算 IFFT:

$$x[k]=IDFT\{X[m]\}=\frac1N\sum^{N-1}_{m=0}X[m]W^{-mk}_N$$

$$=\frac1N(\sum^{N-1}_{m=0}X^*[m]W^{mk}_N)^*=\frac1N(DFT\{X^*[m]\})^*$$

$$X[m]\nRightarrow{\{\}^*}X^*[m]\nRightarrow{FFT}Nx^*[k]\nRightarrow{\{\}^*}Nx[k]\nRightarrow{1/N}x[k]$$

## VI. 混合基 FFT 算法

根据序列长度决定每次分解短序列的长度

若 $x[k]$ 长度为 $pg$ 则分解为 $p$ 个长度为 $q$ 的序列

$$X[m]=X_1[m]+W^m_NX_2[m]+W^{2m}_NX_3[m]+\cdots+W^{(p-1)m}_NX_p[m]$$

$$X[m+q]=X_1[m]+W^{(m+q)}_NX_2[m]+W^{2(m+q)}_NX_3[m]+\cdots+W^{(p-1)(m+q)}_NX_3[m]$$

$$X[m+(p-1)+q]=X_1[m]+W^{(m+pq-q)}_NX_2[m]+W^{2(m+pq-q)}_NX_3[m]$$
$$+\cdots+W^{(p-1)(m+pq-q)}_NX_3[m]$$

基 2 时间抽取 FFT 算法和基 4 时间抽取 FFT 算法是混合基算法的特例, 他们每级分解的基必须相同.
