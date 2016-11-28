#波动光学
##I.光源 单色光 相干光
###i.光源(light source)
任何发光的物体都可以称为光源
####光源的分类
光谱：使光波中不同频率的光分开，形成光谱

按光谱分为: 线谱光源 连续谱光源

按发光机制分为 普通光源 新型光源
#####普通光源（自发辐射Spontaneous radiation）
1. **热辐射** 例如：太阳，白炽灯
1. **电致发光** 例如：闪电，霓虹灯，发光二极管等
1. **光致发光** 例如：日光灯，鳞光物质
1. **化学发光** 例如：燃烧，磷自燃，萤火虫
###ii.光波的相干叠加(superposition principle of light wave)
##VII.单缝的夫琅禾费衍射
###i.典型装置
$A,B\to P$ 的光程差 $\delta=AC=a\sin\varphi$ ($a$ 为缝 $AB$ 的宽度 )
###ii.菲涅耳半波带法
####1.衍射暗纹、明纹条件
\[a\sin\varphi=0,\varphi=0,\delta=0-中央明纹(中心)\]
$a\sin\varphi=2\displaystyle\frac\lambda2$ 此时缝分为两个“半波带”, $P$ 为暗纹。

两个“半波带”上发的光在 P 处干涉相消形成暗纹
#####暗纹条件
\[a\sin\varphi=\pm2k\frac\lambda2,k=1,2,3\cdots\]
$a\sin\varphi=3\displaystyle\frac\lambda2$ 此时缝分成三个“半波带”,$P$ 为明纹。
#####明纹条件
\[a\sin\varphi=\pm(2k+1)\frac\lambda2,k=1,2,3\cdots\]
半波带数目为非整数时，该点的光强介于明暗之间.
####2.衍射条纹的特点
1. 得到的暗纹和中央明纹位置精确,其它明纹位置只是近似
1. 衍射角越大，缝被分的半波带数越多，半波带面积越小，明纹的光强也越小。菲涅耳半波带法可以大致说明单缝衍射的光强分布
3. 单缝衍射和双缝干涉条纹比较:
    - 本质相同，都是光的相干叠加
    - 干涉：有限多的 **分立的** 光束的相干叠加
    - 衍射：无限多的 **连续的** 子波的相干叠加
    - 干涉和衍射 经常同时出现在某些光学现象中,比如 双缝干涉;两束光的干涉+每束光自身的衍射; 比如 **光栅**
####3.单缝衍射明纹角宽度和线宽度
#####角宽度
相邻两暗纹中心对应的衍射角之差
#####线宽度
观察屏上相邻两暗纹中心的间距
#####暗纹条件
\[a\sin\varphi=\pm2k\frac\lambda2,k=1,2,3\cdots\]
##IIX.圆孔的夫琅禾费衍射
###i.圆孔的夫琅禾费衍射
中央亮斑(爱里斑)(Airy disk)集中了约84%的衍射光能

经圆孔衍射后,一个点光源对应一个爱里斑

爱里斑的 **半角宽度** 为
\[\varphi_1\approx1.22\frac\lambda d\\
\left.\begin{array}{l}
d\uparrow\\\lambda\downarrow
\end{array}\right\}爱里斑变小\]
###ii.光学仪器的分辨本领
\[几何光学\quad物点\xrightarrow{一一对应}像点\\
波动光学\quad物点\xrightarrow{一一对应}像斑\]
光学仪器分辨本领(resolving power)
##IX.光栅衍射
###i.光栅衍射(grating diffraction)
####1.光栅(grating)
大量等宽等间距的平行狭缝(或反射面)构成的光学元件

根据多缝衍射原理使光发生色散的光学元件
#####2.光栅常数d(~$10^{-6}$ 米)
\[d=a+b\]
光栅宽度为 $l$ 毫米，每毫米缝数为 m（可达 $10^3$，则 **总缝数**
\[N=m\times l\]
####3.每个缝的衍射图样相重叠
###ii.光栅方程(multiple-beam interference)
####1.五缝干涉
主极大角位置条件(缝间干涉)
\[d\sin\varphi=\pm k\lambda\\k=0,1,2\cdots k称为主极大级数\]
相邻两缝在 $P$ 点引起的光振动相位差为
\[\Delta\varphi=2\pi\frac{d\sin\varphi}\lambda=2k\pi\]
主极大的级数是有限的:
\[d\sin\varphi=\pm k\lambda\to k=\frac{(a+b)\sin\varphi}\lambda\\\sin\varphi\leq1\to k\leq\frac{(a+b)}\lambda\]
#####主极大强度
\[I_\varphi=A^2_\varphi=5^2(\Delta A_\varphi)^2\]
$\Delta A_\varphi$ 为主极大条件下单缝在 $P$ 点引起光的 **振动矢量** 的振幅
#####暗纹条件
各缝光振幅矢量:
\[\vec{A_1},\vec{A_2},\vec{A_3}\cdots\vec{A_5}\]
相邻矢量相位差:
\[\Delta\varphi=2\pi\frac{d\sin\varphi}\lambda\]
当这些 **同频率**、**同振动** 方向的矢量组成的多边形封闭时，合矢量为零，对应点为暗纹，则
\[暗纹条件:5\Delta\varphi=2m\pi\]
1. 对五缝干涉，相邻两主极大间有 **4** 个极小， **3** 个次极大。
1. 主极大光强是相应位置处单缝引起光强的 **$5^2$** 倍。
####2.N缝干涉(multiple-beam interference)
#####光栅方程
缝间干涉主极大就是光栅衍射主极大，其位置满足
\[d\sin\varphi=\pm k\lambda,k=0,1,2,3\cdots光栅方程\]
#####主极大强度
\[I_\varphi=A^2_\varphi=N^2\Delta I_\varphi\]
$\Delta I_\varphi=(\Delta A_\varphi)^2$ 单缝在 主极大位置处引起的光强。
#####暗纹条件
\[N\Delta\varphi=\pm2m\pi\]
\[Nd\sin\varphi=\pm m\lambda,m=1,2\cdots N-2,N-1,N,N+1\cdots\]
1. 对 N 缝干涉两主极大间有 N-1 个极小， N-2 个次极大。
1. 衍射屏上主极大的强度 $I\propto N^2$
1. 随着 N 的增大，强度向主极大集中，使条纹 **亮而窄**，便于观测。这正是多光束干涉较双缝干涉之优越处。
###iii.单缝衍射的调制作用(grating diffraction)
多缝干涉主极大光强受 **单缝衍射** 光强 **调制**，使得主极大光强大小不同，在单缝衍射光强极小处的主极大缺级。
\[\left.\begin{array}{r}
d\sin\varphi=\pm k\lambda\\a\sin\varphi=\pm k'\lambda
\end{array}\right\}=\sin\varphi=k'\lambda/a=k\lambda/d\\k=\pm k'\frac da\quad k'=1,2,3\cdots\]
##X.X射线在晶体上的衍射
//TBD
##XI.自然光和偏振光(Polarization of light)
###i.线偏振光(linearly polarized light)(平面偏振光)
####1.光的偏振态
光波在传播过程中，在垂直于传播方向的平面内可能有不同的振动状态，这种振动状态称为 **光的偏振态。**
####2.线偏振光
光矢量只在一个固定平面内沿一个固定方向振动的光叫线偏振光（平面偏振光）。光的偏振证明了光的 **横波性。**

光矢量只在一个方向上振动

偏振光的振动方向与传播方向组成的平面称为 **振动面**
#####线偏振光的表示法
光振动平行板面
\[++++++\to\]
光振动垂直板面
\[\cdots\cdots\cdots\to\]
#####线偏振光可沿两个相互垂直的方向分解
\[E_x=E\cos\alpha\quad E_y=E\sin\alpha\]
###ii.自然光(natural light)
自然光可用两个相互独立、没有固定相位关系、等振幅且振动方向相互垂直的线偏振光表示。

自然光沿任何方向的分量的强度都等于总强度的一半：$I=1/2I_0$

在垂直于光传播方向的平面内沿各方向振动的光矢量呈对称分布

自然光的表示法:
\[+\cdot+\cdot+\cdot+\to\]
###iii.部分偏振光
部分偏振光可用两个相互独立、没有固定相位关系、不等振幅且振动方向相互垂直的线偏振光表示。

#####部分偏振光的表示法:
平行板面的光振动较强:
\[++\cdot++\cdot++\to\]
垂直板面的光振动较强:
\[\cdot\cdot+\cdot+\cdot\cdot\to\]
在垂直于光传播方向的平面内，各方向振动都有但振幅不相等
###iv.圆偏振光(circularly polarized light)椭圆偏振光(ellipticly polarized light)
#####迎着光传播方向观察：
在垂直于光传播方向的平面内，光矢量按一定频率旋转。

光矢量端点轨迹是一个圆→圆偏振光 椭圆→椭圆偏振光
\[E_x=A\cos(\omega t)\,\vec E顺时针旋转\quad左旋+\frac\pi2\]
\[E_y=A\cos(\omega t\pm\frac\pi2)\,\vec E逆时针旋转\quad右旋-\frac\pi2\]
###v.偏振度(degree of polarization)
部分偏振光可看成是自然光和线偏振光的混合,设部分偏振光的强度为 $I_i$, 其中自然光强度为 $I_n$，线偏振光的强度为 $I_p$, 则有
\[I_i=I_n+I_p\]
\[偏振度\quad p=\frac{I_p}{I_i}=\frac{I_p}{I_p+I_n}\\
\begin{cases}p=1&线偏振光\\0<p<1&部分偏振光\\p=0&自然光\end{cases}\]
###XII.起偏和检偏 马吕斯定律
###i.起偏和检偏
起偏：从自然光获得线偏振光的过程

起偏器：获得线偏振光的器件或装置(polarizer)(利用反射和折射；利用晶体的二向色性)
1. 所谓起偏，即将自然光转变为偏振光，而检验某束光是否是偏振光，即所谓检偏。用以转变自然光为偏振光的物体叫起偏器；用以判断某束光是否是偏振光的物体叫做检偏器。偏振片
2. 自然光经过起偏器后转变成线偏振光。
3. 在自然光的光路中插入检偏器，屏上光强减半。检偏器旋转，屏上亮暗无变化。
4. 对线偏振光，检偏器旋转一周，光强两亮两暗。
5. 对部分偏振光，检偏器旋转一周，屏上光强两亮两弱。

在 **自然光** 的光路中插入检偏器，屏上光强减半。检偏器旋转，屏上 **亮暗无变化**.

对 **线偏振光** ，检偏器旋转一周，光强 **两强两暗**

对 **部分偏振光** ，检偏器旋转一周，屏上光强 **两强两弱**
###ii.马吕斯定律（Malus law)
它是关于偏振光强度变化的定量定律.
\[I\propto E^2\quad I'\propto E'^2=E^2\cos\alpha\]
\[I'=I\cos^2\alpha\quad马吕斯定律\]
\[当\alpha=0,I=I_{\text{max}}=I_0\\
当\alpha=\frac\pi2,I=0\Rightarrow\overset{extinction}{消光}\]
##XIII.反射和折射时光的偏振
###i.反射和折射产生的偏振
自然光反射和折射后产生部分偏振光
###ii.布儒斯特定律(Brewster Law)
1812，布儒斯特发现: 反射光的偏振化程度和入射角有关

$ib+γ=90^o$ 时，反射光为线偏振光

$i_B$ — **布儒斯特角** 或 **起偏角** (Brewster angle)
\[n_1\sin i_b=n_2\sin\gamma=n_2\cos i_b\\\tan i_b=\frac{n_2}{n_1}=n_{21}\]
* 布儒斯特角决定于介质的折射率
* 自然光以布儒斯特角入射，反射出线偏振光 -- **反射起偏法**

##XIV.光的双折射
光在各向异性介质中的传播
###i.寻常光和非常光
####1.双折射(double refraction)
#####双折射现象
一束光入射到各向异性的介质后出现两束折射光线的现象。
####2.寻常光和非寻常光
两折射光线中有一条始终在入射面内，并遵从折射定律，称为 **寻常光**, 简称 **o光** (ordinary light)

另一条光一般不在入射面内，不遵从折射定律，称 **非常光**，简称 **e光** (extraordinary light)

两束光的特点:
* 两束光是光矢量振动方向不同的线偏振光
* 垂直入射时，以入射光为轴旋转晶体， **o光** 不动， **e光** 旋转
###ii.光轴  主平面
####1.晶体的光轴(optical axis of crystal)
当光在晶体内沿某个特殊方向传播时 **不发生双折射**，该方向称为晶体的 **光轴**。

**光轴是一特殊的方向**,凡平行于此方向的直线均为光轴。
1. **单轴晶体**: 只有一个光轴的晶体冰洲石、石英、红宝石、冰...
1. **双轴晶体**: 有两个光轴的晶体云母、蓝宝石、橄榄石、硫磺...
####2.主平面(principal plane)
**主平面** 晶体中 **光的传播** 方向与晶体 **光轴** 构成的平面.

**o光** 振动垂直主平面 **e光** 振动在主平面内
#####双折射光的偏振
**o光** 和 **e光** 都是偏振光, 并且偏振方向互相垂直

**光轴在入射面** 时, **o光** 主平面和 **e光** 主平面重合,此时 **o光** 振动和 **e光** 振动相互垂直。一般情况下，两个主平面夹角很小，故可认为 **o光** 振动和 **e光** 振动仍然相互垂直。
###iii.单轴晶体的子波波阵面
####o光:
\[n_o=\frac c{V_o}(o光主折射率)\]
各个方向光速相同波面为球面
####e光:
\[n_e=\frac c{V_e}(e光主折射率)\]
各个方向光速不同波面为椭球面
####正晶体(positive crystal):
石英、冰等
\[\begin{cases}V_o>V_e\\n_o<n_e\end{cases}\]
####负晶体(negative crystal):
\[\begin{cases}V_o<V_e\\n_o>n_e\end{cases}\]
方解石、红宝石等
###iv.偏振光的干涉
####1.实验现象
* 单色光入射，波片厚度均匀，屏上光强均匀分布。
* 白光入射，屏上出现彩色，转动偏振片或波片，色彩变化。
* 波片厚度不均匀时，出现干涉条纹。
####2.偏振光干涉的分析
光轴平行晶体表面，垂直入射

o光 和 e光 传播方向相同，但速度不同。

o光 和 e光 通过波片后产生的相位差为：
\[\left|\Delta\varphi_c\right|=\frac{2\pi d}\lambda\left|n_o-n_e\right|\]
1. $n_o$: $o$ 光主折射率
1. $n_e$: $e$ 光主折射率

o光和e光振动方向垂直，不能产生干涉！利用偏振片2将光振动引到一个方向上来。
\[A_{o2}=A_o\sin\beta=A_1\sin\theta\sin\beta\\A_{e2}=A_e\cos\beta=A_1\cos\theta\cos\beta\]
####3.光强分析 $P_1\bot P_2$
\[A_o=A_1\sin\theta\\A_e=A_1\cos\theta\\A_{o2}=A_1\cos\theta=A_1\sin\theta\cos\theta\\A_{e2}=A_e\sin\theta=A_1\sin\theta\cos\theta\]
$\pi$ 为投影引入的附加相位
\[\left|\Delta\varphi\right|=\left|\Delta\varphi_c\right|+\pi\\=\frac{2\pi d}\lambda\left|n_o-n_e\right|+\pi\]
o光 和 e光 经过 偏振片2 后，振动方向平行，振动频率相同，相位差恒定，满足干涉条件。
#####合振动强度为:
\[I_2=A^2_{o2}+A^2_{e2}+2A_{o2}A_{e2}\cos\Delta\varphi\\=\frac12A_1^2\sin^22\theta(1+\cos\Delta\varphi)\]
\[\left|\Delta\varphi\right|=\frac{2\pi d}\lambda\left|n_o-n_e\right|+\pi=2k\pi\,干涉相长\\\left|\Delta\varphi\right|=\frac{2\pi d}\lambda\left|n_o-n_e\right|+\pi=(2k+1)\pi\,干涉相消\]
1. 波片厚度相同时，各处相位差相同，单色光 照射时屏上光强均匀分布。
2. 波片厚度不均匀时，各处相位差不同，单色光入射出现等厚干涉条纹。
3. **白光** 照射时，屏上由于某种颜色干涉相消, 而呈现它的 **互补色(complementary colors)**，这叫 **(显)色偏振(chromatic polarization)**
\[\left|\Delta\varphi\right|=\frac{2\pi d}\lambda\left|n_o-n_e\right|+\pi=(2k+1)\pi\\]
4. 旋转偏振片，使两偏振片偏振化方向平行， 相位差产生π 的变化，屏上颜色发生变化。偏光显微镜广泛用于地质、冶金工业中矿石鉴别、晶体结构分析.
###iv.单轴晶体中的波面 (惠更斯作图法($v_e>v_o$))
\\TBD
###v.晶体偏振器
####1.尼科耳棱镜
尼科耳棱镜(W.Nicol,1828) **应用最为广泛的双折射偏振器件**
将方解石晶体沿特定方向切成两半，再用加拿大树胶粘合，即制成尼科耳棱镜

**要求**: 入射角小于 $14^0$, 否则 O光不能发生全反射。

**缺点**: 加拿大树胶吸收紫外线，所以，对短波段不适用。这时，可以使用渥拉斯顿棱镜
####2. 渥拉斯顿棱镜(Wollaston prism)
由两块直角方解石棱镜拼成。两块棱镜的光轴互相垂直

上述两种棱镜得到的偏振光质量非常好，但棱镜本身价格很高，因而使用较少。
####3.波晶片
（光轴平行于表面且厚度均匀的晶体）
自然光垂直入射波晶片后，o 光, e 光传播速度不同，产生的相位不同 。
波晶片
出射 o光 e光 的相差为
\[\Delta\varphi=\frac{2\pi}\lambda(n_o-n_e)d\]
波晶片分类
\[\begin{array}{llc}(n_o-n_e)d=\lambda/4&\Delta\varphi=\pi/2&\overset{quarter-wave plate}{1/4波片}\\
(n_o-n_e)d=\lambda/2&\Delta\varphi=\pi&\overset{halfwave plate}{半波片}\\
(n_o-n_e)d=\lambda&\Delta\varphi=2\pi&全波片\end{array}\]
说明: 一定的波晶片是针对某一特定波长而言的.

出射后 o光 e光 合成:
\[\begin{cases}E_e=A_e\cos(\omega t)\\E_o=A_o\cos(\omega t+\Delta\varphi)\end{cases}\]
1. $\Delta\varphi=k\pi$
\[E_o=\pm\frac{A_o}{A_e}E_e\quad线偏振光\]
2. $\Delta\varphi=\pm\displaystyle\frac\pi2$
\[\frac{E_e^2}{A_e^2}+\frac{E_o^2}{A_o^2}=1\quad椭圆偏振光
\\A_e=A_o\quad圆偏振光\]
