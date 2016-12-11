#力学
##I.质点运动的描述
###i.质点运动学的基本概念
####1.质点(particle)
有质量而无形状和大小的几何点 突出了 **质量** 和 **位置**

**质点系**: 若干质点的集合
####2.参考系 坐标系(frame of reference)
**参照物**：为了描述物体运动而选作参考的物体或物体系

**参考系**：参照物 + 坐标系 + 时钟
1. 运动学中参考系可任选。
1. 参照物选定后，坐标系可任选。坐标系是参考系的数学抽象 (coordinate system)  (reference system)
1. 常用坐标系:直角坐标系 $(x,y,x)$ 球坐标系 $(r,\theta,\phi)$ 柱坐标系 $(\rho,\theta,\phi)$ 自然坐标系 $(s)$
####3. 空间和时间 时空观
**空间**: 物质的广延性，与体积位置变化相联系

**时间**: 物理事件的顺序性和持续性
###ii.运动学方程(运动函数)(function of motion)
直角坐标下 $x=x(t),y=y(x),z(t)$

**意义**: 已知运动学方程，可求质点运动轨迹、速度和加速度
###iii.位矢  (position vector)
质点某时刻位置 $P(x,y,z)$ 由 **位矢** $\vec r$ 表示。
\[\vec r=x\vec i+y\vec j+z\vec k\]
位矢的方向用方向余弦表示，则有:
\[\cos\alpha=\frac xr\quad\cos\beta=\frac yr\quad\cos\gamma=\frac zr\]
###iv.位移(displacement)
位移矢量反映了物体运动中位置(距离与方位)的变化。
####1.定义
\[\Delta\vec r=\vec r(t+\Delta t)-\vec r(t)\]
1. 位移是矢量(有大小,有方向), 位移不同于路程
1. 位移与参照系位置的变化无关
1. 分清 $|\Delta\vec r|$ 与 $\Delta r$ 的区别
\[|\Delta\vec r|=|\vec r(t+\Delta t)-\vec r(t)|\\\Delta r=|\vec r(t+\Delta t)|-|\vec r(t)|\]
####2.用直角坐标表示位移
\[\vec{r_1}=x_1\vec i+y_1\vec j+z_1\vec k\\\vec{r_2}=x_2\vec i+y_2\vec j+z_2\vec k\\\Delta\vec r=\Delta x\vec i+\Delta y\vec j+\Delta z\vec k\\=(x_2-x_1)\vec i+(y_2-y_1)\vec j+(z_2-z_1)\vec k\]
###v.速度(velocity)
描述物体运动状态的物理量
####1.定义
#####平均速度 (average velocity)
\[\left\langle\vec v\right\rangle=\frac{\Delta\vec r}{\Delta t}=\frac{\vec r(t+\Delta t)-\vec r(t)}{\Delta t}\]
#####瞬时速度 (instantaneous velocity)
\[\vec v=\lim_{\Delta t\to0}\frac{\vec r(t+\Delta t)-\vec r(t)}{\Delta t}=\frac{d\vec r}{dt}\]
1. 速度的矢量性、瞬时性和相对性。
1. 注意速度与速率（speed）的区别
\[\vec v=\frac{d\vec r}{dt}\quad v=|\vec v|=\left|\frac{d\vec r}{dt}\right|=\left|\frac{ds}{dt}\right|\ne\frac{dr}{dt}\]
####2.用直角坐标表示速度
#####平均速度
\[\left\langle\vec v\right\rangle=\frac{\Delta\vec r}{\Delta t}=\frac{\Delta x}{\Delta t}\vec i+\frac{\Delta y}{\Delta t}\vec j+\frac{\Delta z}{\Delta t}\vec k\]
#####瞬时速度
\[\vec v=\frac{d\vec r}{dt}\vec i=\frac{dx}{dt}\vec i+\frac{dy}{dt}+\vec j+\frac{dz}{dt}\vec k\\=v_x\vec i+v_y+\vec j+v_z\vec k\]
速度的大小为
\[v=\sqrt{v_x^2+v_y^2+v_z^2}\]
速度的方向用方向余弦表示为
\[\cos\alpha'=\frac{v_x}{|\vec v|}\quad\cos\beta'=\frac{v_y}{|\vec v|}\quad\cos\gamma'=\frac{v_z}{|\vec v|}\]
###vi.加速度(acceleration)
####1.定义
#####平均加速度
\[\left\langle\vec\alpha\right\rangle=\frac{\Delta\vec v}{\Delta t}=\frac{\vec v(t+\Delta t)-\vec v(t)}{\Delta t}\]
#####瞬时加速度
\[\vec\alpha=\lim_{\Delta t\to0}\frac{\vec v(t+\Delta t)-\vec v(t)}{\Delta t}=\frac{d\vec v}{dt}=\frac{d^2\vec r}{dt^2}\]
1. 加速度反映速度的变化(大小和方向)情况
1. 加速度的方向总是指向轨迹曲线凹的一面
####2.用直角坐标表示加速度
\[\vec\alpha=\frac{d\vec v}{dt}=\frac{dv_x}{dt}\vec i+\frac{dv_y}{dt}\vec j+\frac{dv_z}{dt}\vec k=\frac{d^2x}{dt^2}\vec i+\frac{d^2y}{dt^2}\vec j+\frac{d^2z}{dt^2}\vec k\]
大小为
\[|\vec\alpha|=\sqrt{\alpha_x^2+\alpha^2_y+\alpha_z^2}=\sqrt{\left(\frac{dv_x}{dt}\right)^2+\left(\frac{dv_y}{dt}\right)^2+\left(\frac{dv_z}{dt}\right)^2}\]
方向用方向余弦表示为
\[\cos\alpha''=\frac{\alpha_x}{|\vec\alpha|}\quad\cos\beta''=\frac{\alpha_y}{|\vec\alpha|}\quad\cos\gamma''=\frac{\alpha_z}{|\vec\alpha|}\]
###vii.运动学的二类问题
####1.第一类问题
已知运动学方程，求 $\vec v,\vec\alpha$
####2.第二类问题
已知加速度和初始条件，求 $\vec v,\vec r$
##II.圆周运动和平面曲线运动(plane curvilinear motion)
###i.平面曲线运动
####1.速度
\[\Delta s=s(t+\Delta t)-s(t)\\\vec v=\lim_{\Delta t\to0}\frac{\Delta\vec r}{\Delta t}=\lim_{\Delta t\to0}\left(\frac{\Delta\vec t}{\Delta s}\frac{\Delta s}{\Delta t}\right)\\=\left(\lim_{\Delta t\to0}\frac{\Delta\vec r}{\Delta s}\right)\left(\lim_{\Delta t\to0}\frac{\Delta s}{\Delta t}\right)=\left(\lim_{\Delta t\to0}\frac{\Delta\vec r}{\Delta s}\right)\frac{ds}{dt}\\=\left(\lim_{\Delta t\to0}\frac{|\Delta\vec r|}{\Delta s}\vec\tau\right)\frac{ds}{dt}=\frac{ds}{dt}\vec\tau=v\vec\tau\]
速度矢量在切线上的投影
####2.加速度
\[\vec v=v\vec\tau\quad\vec\alpha\frac{d\vec v}{dt}=\frac d{dt}(v\vec\tau)=\frac{dv}{dt}\vec\tau+v\frac{d\vec\tau}{}\]
第一项: $\displaystyle\frac{dv}{dt}\vec\tau$ 叫 **切向加速度**(tangential acceleration)
1. 大小为 $\frac{dv}{dt}\vec\tau$, 方向为 $\vec\tau$
1. 意义: 反映速度大小变化的快慢 (与速度同向的力或加速度只能改变速度大小)

第二项: $\displaystyle v\frac{d\vec\tau}{dt}$ 叫 **法向加速度**(normal acceleration)
\[\Delta\vec\tau=\vec\tau(t+\Delta t)-\vec\tau(t)\]
