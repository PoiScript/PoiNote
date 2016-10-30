连续周期信号的频域分析
  周期信号的傅里叶级数展开
    1、周期信号
      f(t)=f(t+kT_0) (k=0,+-1,+-2,...)
    2 周期信号可以表示为三角波的线性组合
      f(t)=b_1\sin(\omega_0t)+b_2\sin(2\omega_0t)+b_3(3\omega_0t)+...
      = \sum^{\infty}_{n=0}b_n\sin(n\omega_0t) \omega_0=2\pi/T_0
      f(t)=\frac{a_0}{2}+\sum^{\infty}{n=1}[a_n\cos(n\omega_0t)+b_n\sin(n\omega_0t)]
    连续信号的分解
      1、连续信号分解为单位冲激信号的线性组合
        f(t)=\intf(\tau)\delta(t-\tau)d\tau
        利用单位冲激响应求解系统的输出信号
      2、连续信号分解为一系列不同频率的三角波信号或复指数信号的线性组合
        f(t)=\frac{a_0}{2}+\int[a_n\cos(n\omegat)+b_n\sin(n\omegat)]
        f(t)=\sum^{\infty}{n=-\infty}C_ne^{jn\omega_0t}
        利用频域特性求解系统的输出信号及系统函数
    频率和频域
      频率：物质在1秒内完成周期性变化的次数叫做频率。
      频域（frequency domain）即频率域，是指在对函数或信号进行分析时，分析其和频率有关部份，而不是和时间有关的部份。
      频域下的信号：信号在频域下的图形（一般称为频谱）可以显示信号分布在哪些频率及其比例。信号在时域下的图形可以显示信号如何随着时间变化 。
    连续周期信号的频域分析
      将信号表示为不同频率复指数分量的线性组合
      意义:
        从信号分析的角度，将信号表示为不同频率复指数分量的线性组合，为不同信号之间进行比较提供了途径。
        从系统分析角度，已知单频正弦信号激励下的响应，利用迭加特性可求得多个不同频率正弦信号同时激励下的总响应,而且每个正弦分量通过系统后的变化。
  傅里叶级数的基本性质
    1.1  周期信号的傅里叶级数展开
      1、傅里叶级数的引进
        法国数学家傅里叶发现，任何周期函数都可以用正弦函数和余弦函数构成的无穷级数来表示，后世称为傅里叶级数。
      2.信号分解为正交函数
        矢量正交与正交分解
        矢量正交：指矢量 $V_x=(V{x1},V_{x2},V_{x3})$ 与 $V_y=(V_{y1},V_{y2},V_{y3}) 的内积为0.
          V_XY_X^T = \sum^{3}_{i=1}v_{xi}v_{yi}=0
        正交矢量集：指由两两正交的矢量组成的矢量集合
          如三维空间中，以矢量vx=(2,0,0), vy=(0,2,0), vz=(0,0,2), 所组成的集合就是一个正交矢量集，且完备。d
        信号正交与正交函数集
          正交：指矢量 $\xi_1(t)$ 与 $\xi_2(t)$ 在(t1,t2)区间满足 $\int^{t_2}_{t_1}A(t)\Xi_2^*(t)dt=0$ 的内积为0.
            则称 $\xi_1(t)$ 和 $\xi_2(t)$ 在区间(t1,t2)内正交。
          正交函数集：若n个函数 $\xi_1(t),\xi_2(t),...,\xi_n(t)$
            构成一个函数的集，这些函数在区间(t1,t2)内满足 $\int^{t_2}_{t_1}A(t)\Xi_j^*(t)dt=
          完备正交函数集
            如果在正交函数集 {\xi_1(t),\xi_2(t),...,\xi_n(t)}  之外不存在函数 \xi(t) 满足
              \int^{t_2}_{t_1}A^*(t)\xi_i(t)dt=0（i=1,2,…,n）
            则称此函数为完备正交函数集。
              例如：三角函数集 {1, \cos(n\omega t), \sin(n\omega t), n=1,2,...}
              虚指数函数集 {e^{jn\omega t}, n=0,+-1,+-2,...}
              是典型的在区间 (t_0, t_0+T)(T=2\pi/\omega) 上的完备正交函数集。
              三角函数集 {1,\cos(n\omega t),\sin(n\omega t), } 在一个周期内是一个完备的正交函数集。
                \int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}\cos(n\omega t)\sin(m\omega t)dt = 0
                \int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}\cos(n\omega t)\sin(m\omega t)dt = \farc^{T}_{2}, m=n 0, m n
                \int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}\cos(n\omega t)\sin(m\omega t)dt = \farc^{T}_{2}, m=n 0, m n
      3、傅里叶级数-傅里叶级数的三角形式
        f(t)=\frac^{a_0}_{2}+\int^{}_{n=1}[a_n\cos(n\omega t)+b_n\sin(n\omega t)] \omega=2\pi/T
        \int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}f(t)\cos(k\omega k)dt=\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}(\frac^{a_0}_{2}+\sum^{\infty}_{n=1}[a_n\cos(n\omega t)+b_n\sin(n\omega t)])\cos(k\omega t)dt=\frac^{T}_{2}a_k
        a_n=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}f(t)\cos(n\omega t)dt
        a_0=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}f(t)dt

        \int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}f(t)\cos(k\omega k)dt=\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}(\frac^{a_0}_{2}+\sum^{\infty}_{n=1}[a_n\cos(n\omega t)+b_n\sin(n\omega t)])\sin(k\omega t)dt=\frac^{T}_{2}b_k
        b_n=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}f(t)\sin(n\omega t)dt
        b_0=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}f(t)dt
        f(t)=\frac^{a_0}{2}+\int^{}_{n=1}[a_n\cos(n\omega t)+b_n\sin(n\omega t)] \omega=2\pi/ 其中a_n a_b 为傅里叶系数
        a_n=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}\sin(n\omega t)dt a_n是n的偶函数
        b_n=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{-\frac^{T}_{2}}\cos(n\omega t)dt b_n是n的奇函数
        纯余弦形式傅里叶级数
          f(t)=\frac^{A_0}_{2}+\int^{}_{n=1}A_n\cos(n\omega t)+\xi_n
          周期信号可分解为直流分量和许多余弦分量
          A_0/2称为信号的直流分量，A_n\cos(n\omega_0 t+\xi_n) 称为信号的n次谐波分量。
         波形的对称性与谐波特性
          a_n=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{\frac^{T}_{2}}f(t)\cos(n\omega t)dt
          b_n=\frac^{2}_{T}\int^{\frac^{T}_{2}}_{\frac^{T}_{2}}f(t)\sin(n\omega t)dt
          (1) f(t)为偶函数 b_n=0，展开为余弦级数
          (2) f(t)为奇函数 a_n=0，展开为正弦级数
          (3) f(t)为半波镜像信号 f(t)=-f(t \frac^{T}_{2})
            此时傅里叶级数中只含奇次谐波分量 a_0=a_2=...=b_0=b_2=...=0
          (4) 半波重叠信号 f(t)=f(t \frac^{T}_{2})
            此时傅里叶级数中只含偶次谐波分量 a_1=a_3=...=b_1=b_3=...=0
      3、周期信号展开为傅里叶级数条件
        周期信号f (t)应满足Dirichlet条件，即：
        (1) 在一个周期内绝对可积，即满足 \int^{T_0+t_0}_{t_0}|f(t)|dt 为有限值。
        (2) 在一个周期内只有有限个不连续点；
        (3) 在一个周期内只有有限个极大值和极小值。
        注意：条件(1)为充分条件但不是必要条件 条件(2)(3)是必要条件但不是充分条件
      4、傅里叶级数的指数形式
        傅里叶级数的 阶谐波n 可以用指数形式表示。 a_n\cos(n\omega_0t)+b_n\sin(n\omega_0t) (n=1,2,...)
        \cos(n\omega_0t)=\frac{1}{2}(e^{jn\omega_0t}+e^{-jn\omega_0t})
        \sin(n\omega_0t)=-\frac{j}{2}(e^{jn\omega_0t}-e^{-jn\omega_0t})
        f(t)=\frac^{a_0}_{2}+\int^{}_{n=1}(a_n\cos(n\omega_0t)+b_n\sin(m\omega_0t))
        =\frac^{a_0}_{2}+\sum^{\infty}_{n=1}(\frac^{a_n-jb_n}_2e^{jn\omega_0t}+\frac^{a_n+jb_n}_2e^{-jn\omega_0t})
          C_0=\frac^{a_0}_2 C_n=\frac^{a_n-jb_n}_2 C_{-n}=\frac^{a_n+jb_n}_{2}
        f(t)=\sum^{\infty}{n=-\infty}C_ne^{jn\omega_0t} C_n为复傅里叶系数
        三角形式的傅里叶级数含义比较明确，但运算常感不便，因而经常采用指数形式的傅里叶级数
        连续时间周期信号可以用指数形式傅里叶级数表示为 f(t)=\sum^{\infty}{n=-\infty}C_ne^{jn\omega_0t} 其中 C_n=\frac^{1}_{T_0}\int
          n = 0 这一项是一个常数，称为信号的直流分量
          n = +-1 的基波频率为  \omega_0 ，两项合起来称为信号的基波分量
          n = +-2 的基波频率为2 \omega_0  ，两项合起来称为信号的2次谐波分量
          n = +-n 的基波频率为N \omega_0  ，两项合起来称为信号的N次谐波分量
        物理含义：
          周期信号f (t)可以分解为不同频率虚指数信号之和
    1.2  傅里叶级数的基本性质
       线性特性 
  周期信号的频谱及其特点
  周期信号的功率谱