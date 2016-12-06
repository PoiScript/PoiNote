#导数与微分
##I.导数的概念
###i.导数的定义
#####定义1.
设函数 $y=f(x)$ 在点 $x_0$ 的某邻域内有定义, 若 $\displaystyle\lim_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}=\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}$ 存在, 则称函数 $f(x)$ 在点 $x_0$ 处 **可导**, 并称此极限为 $y=f(x)$ 在点 $x_0$ 的 **导数**. 记作:
\[y'|_ {x=x_0}\quad f'(x_0)\quad\frac{dy}{dx}|_ {x=x_0}\quad\frac{df(x)}{dx}|_ {x=x_0}\]
即:
\[y'|_ {x=x_0}=f'(x_0)=\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}\\=\lim_{\Delta x\to0}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}=\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}h\]
若上述极限不存在, 就说函数 **在点 $x_0$ 不可导**.

若 $\displaystyle\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}=\infty$, 也称 $f(x)$ 在 $x_0$ 的导数为 **无穷大**.

若函数在开区间 $I$ 内每点都可导, 就称函数 **在 $I$ 内可导**. 此时导数值构成的新函数称为 **导函数**, 记作:
\[y'\quad f'(x)\quad\frac{dy}{dx}\quad\frac{df(x)}{dx}\]
注意:
\[f'(x_0)=f'(x)|_ {x=x_0}\neq\frac{df(x_0)}{dx}\]
###ii.导数的几何意义
曲线 $y=f(x)$ 在点 $(x_0,y_0)$ 的切线斜率为
\[\tan\alpha=f'(x_0)\]
#####切线方程:
\[y-y_0=f'(x_0)(x-x_0)\]
#####法线方程:
\[y-y_0=-\frac1{f'(x_0)}(x-x_0)(f'(x_0)\ne0)\]
1. 若 $f'(x_0)>0$, 曲线过 $(x_0,y_0)$ 上升;
1. 若 $f'(x_0)<0$, 曲线过 $(x_0,y_0)$ 下降;
1. 若 $f'(x_0)=0$, 切线与 $x$ 轴平行, 称驻点;
1. 若 $f'(x_0)=\infty$, 切线与 $x$ 轴垂直
###iii.函数的可导性与连续性的关系
#####定理1.
$f(x)$ 在点 $x$ 处可导, 则 $f(x)$ 在点 $x$ 处连续.
#####证:
1. 设 $y=f(x)$ 在点 $x$ 处可导, 即 $\displaystyle\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}=f'(x)$ 存在
2. 因此必有 $\displaystyle\frac{\Delta y}{\Delta x}=f'(x)+\alpha$, 其中 $\displaystyle\lim_{\Delta x\to0}\alpha=0$
3. 故 $\Delta y=f'(x)\Delta x+\alpha\Delta x\xrightarrow{\Delta x\to0}0$
4. 所以函数 $y=f(x)$, 在点 $x$ 连续.

注意: 函数在点 $x$ 连续未必可导.
###iv.单侧导数
#####定义2.
设函数 $y=f(x)$ 在点 $x_0$ 的某个右(左)领域内有定义, 若极限
\[\lim_{\substack{\Delta x\to0^+\\(\Delta x\to0^-)}}\frac{\Delta y}{\Delta x}=\lim_{\substack{\Delta x\to0^+\\(\Delta x\to0^-)}}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}\]
存在, 则称此极限值为 $f(x)$ 在 $x_0$ 处的右(左)导数, 记作 $f'_ +(x_0)(f'_ -(x_0))$

即 $\displaystyle f'_ \pm(x_0)=\lim_{\Delta x\to0^\pm}\frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$
#####定理2.
函数 $y=f(x)$ 在点 $x_0$ 可导的 **充分必要条件** 是 $f'_ +(x_0),f'_ -(x_0)$ 存在, 且 $f'_ +(x_0)=f'_ -(x_0)$
#####定理3.
函数 $f(x)$ 在点 $x_0$ 处右(左)导数存在, 则 $f(x)$ 在点 $x_0$ 必右(左)连续.

若函数 $f(x)$ 在开区间 $(a,b)$ 内可导, 且 $f'_ +(a)$ 与 $f'_ -(b)$ 都存在, 则称 $f(x)$ 在闭区间 $[a,b]$ 上可导.

显然: $f(x)$ 在闭区间 $[a,b]$ 上可导, 则 $f(x)\in C[a,b]$
##II.函数的求导法则
###i.四则运算求导法则
#####定理1.
如果函数 $u=u(x)$ 及 $v=v(x)$ 都在点 $x$ 处具有导数, 那么它们的和、差、积、商 (除分母为 0的点外)都在点 $x$ 可导, 且
\[\begin{cases}\big[u(x)\pm v(x)\big]'=u'(x)\pm v'(x)
\\\big[u(x)v(x)\big]'=u'(x)v(x)+u(x)v'(x)
\\\bigg[\displaystyle\frac{u(x)}{v(x)}\bigg]'=\frac{u'(x)v(x)-u(x)v'(x)}{v^2(x)}(v(x)\neq0)\end{cases}\]
###ii.反函数的求导法则
#####定理2.
如果函数 $x=f(y)$ 在区间 $I_y$ 内单调可导且 $f'(y)\ne0$, 那么它的反函数 $y^{-1}(x)$ 在区间 $I_x=\{x|x=f(y),y\in I_y\}$ 内也可导, 且
\[[f^{-1}(x)]'=\frac1{f'(y)}或\frac{dy}{dx}=\frac1{\frac{dx}{dy}}\]
###iii.复合函数求导法则
#####定理3.
$u=g(x)$ 在点 $x$ 可导, $y=f(u)$ 在点 $u=g(x)$ 可导, 则复合函数 $y=f[g(x)]$ 在点 $x$ 可导,且
\[\frac{dy}{dx}=f'(u)g'(x)\]
**推广**: 此法则可推广到多个中间变量的情形.
\[\frac{dy}{dx}=\frac{dy}{du}\cdot\frac{du}{dv}\cdot\frac{dv}{dx}\]
###iv.初等函数的求导问题
####1.常数和基本初等函数的导数
\[\begin{array}{ll}
(C)'=0&(x^\mu)'=\mu x^{\mu-1}\\
(\sin x)'=\cos x&(\cos x)'=-\sin x\\
(\tan x)'=\sec^2x&(\cot x)'=-\csc^2x\\
(a^x)'=a^x\ln a&(e^x)'=e^x\\
(\log_ax)'=\frac1{x\ln a}&(\ln x)'=\frac1x\\
(\arcsin x)'=\frac1{\sqrt{1-x^2}}&(\arccos x)'=-\frac1{\sqrt{1-x^2}}\\
(\arctan x)'=\frac1{1+x^2}&(\mathrm{arccot}x)'=-\frac1{1+x^2}
\end{array}\]
####2.有限次四则运算的求导法则
\[\begin{array}{ll}
(u\pm v)'=u'\pm v'&(Cu)'=Cu'(C为常数)\\
(uv)'=u'v+uv'&\Big(\frac uv\Big)'=\frac{u'v-uv'}{v^2}(v\ne0)
\end{array}\]
####3.复合函数求导法则
\[y=f(u),u=\varphi(x)\\\frac{dy}{dx}=\frac{dy}{du}\cdot\frac{du}{dx}=f'(u)\cdot\varphi'(x)\]
####4.初等函数在定义区间内可导,且导数仍为初等函数
##III.高阶导数
###i.高阶导数的概念
定义.
若函数 $y=f(x)$ 的导数 $y'=f'(x)$ 可导, 则称 $f'(x)$ 的导数为 $f(x)$ 的 **二阶导数**, 记作 $y''$ 或 $\displaystyle\frac{d^2y}{dx^2}$ 即 $y''=(y')'$ 或 $\displaystyle\frac{d^2y}{dx^2}=\frac d{dx}\Big(\frac{dy}{dx}\Big)$

类似地, 二阶导数的导数称为三阶导数, 依次类推, $n-1$ 阶导数的导数称为 $n$ 阶导数, 分别记作 $y''',y^{(4)}\cdots y^{(n)}$ 或 $\displaystyle\frac{d^3y}{dx^3},\frac{d^4y}{dx^4}\cdots\frac{d^ny}{dx^n}$
###ii.高阶导数的运算法则
设函数 $u=u(x)$ 及 $v=v(x)$ 都有 $n$ 阶导数, 则
\[\begin{array}{ll}
1.&(u\pm v)^{(n)}=u^{(n)}\pm v^{(n)}\\
2.&(Cu)^{(n)}=Cu^{(n)}(C为常数)\\
3.&(uv)^{(n)}=u^{(n)}+nu^{(n-1)}v'+\frac{n(n-1)}{2!}u^{(n-2)}v''+\\
&+\cdots+\frac{n(n-1)\cdots(n-k+1)}{k!}u^{(n-k)}v^{(k)}\\
&+\cdots+uv^{(n)}\,\text{莱布尼兹(Leibniz)公式}
\end{array}\]
##IV.隐函数和参数方程求导
###i.隐函数的导数
若由方程 $F(x,y)=0$, 可确定 $y$ 是 $x$ 的函数, 则称该函数为 **隐函数**.

由 $y=f(x)$ 表示的函数, 称为 **显函数**.
可确定显函数

隐函数 **求导方法**: $F(x,y)=0$ 两边对 $x$ 求导, 得到含导数 $y$ 的方程 $\displaystyle\frac d{dx}F(x,y)=0$
###ii.由参数方程确定的函数的导数
若参数方程 $\displaystyle\begin{cases}x=\varphi(t)\\y=\psi(t)\end{cases}$ 可确定一个 $y$ 与 $x$ 之间的函数关系, $\varphi(t),\psi(t)$ 可导, 且 $[\varphi'(t)]^2+[\psi'(t)]^2\ne0$, 则 $\varphi'(t)\ne0$ 时, 有
\[\frac{dy}{dx}=\frac{dy}{dt}\cdot\frac{dt}{dx}=\frac{dy}{dt}\cdot\frac1{\frac{dx}{dt}}=\frac{\psi'(t)}{\varphi'(t)}\]
$\psi'(t)$ 时, 有
\[\frac{dx}{dy}=\frac{dx}{dt}\cdot\frac{dt}{dy}=\frac{dx}{dt}\frac1{\frac{dy}{dt}}=\frac{\varphi'(t)}{\psi'(t)}\]
(此时看成 $x$ 是 $y$ 的函数 )

若上述参数方程中 $\varphi(t),\psi(t)$ 二阶可导, 且 $\varphi'(t)\ne0$, 则由它确定的函数 $y=f(x)$ 可求二阶导数. 利用新的参数方程 $\displaystyle\begin{cases}x=\varphi(t)\\\displaystyle\frac{dy}{dx}=\frac{\psi'(t)}{\varphi'(t)}\end{cases}$, 可得
\[\frac{d^2y}{dx^2}=\frac d{dx}\left(\frac{dy}{dx}\right)=\frac d{dt}\left(\frac{\psi'(t)}{\varphi'(t)}\right)\cdot\frac{dt}{dx}\\=\frac{\psi''(t)\varphi'(t)-\psi'(t)\varphi''(t)}{\varphi'^2(t)}\cdot\frac1{\varphi'(t)}\]
即:
\[\frac{d^2y}{dx^2}=\frac{\psi''(t)\varphi'(t)-\psi'(t)\varphi''(t)}{\varphi'^3(t)}\]
**注意**: $\displaystyle\frac{dy}{dx}=\frac{\psi'(t)}{\varphi'(t)},\frac{d^2y}{dx^2}\ne\left(\frac{\psi'(t)}{\varphi'(t)}\right)'$
###iii.相关变化率
$x=x(t),y=y(t)$ 为两可导函数, $x,y$ 之间有联系, 则 $\displaystyle\frac{dx}{dt},\frac{dy}{dt}$ 之间也有联系, 称为 **相关变化率**

相关变化率问题解法:
1. 找出相关变量的关系式
1. 对 $t$ 求导
1. 得相关变化率之间的关系式
1. 求出未知的相关变化率
##V.函数的微分
###i.微分的概念
定义: 若函数 $y=f(x)$ 在点 $x_0$ 的增量可表示为
\[\Delta y=f(x_0+\Delta x)-f(x_0)=A\Delta x+o(\Delta x),A为不依赖于\Delta x的常数\]
则称函数 $y=f(x)$ 在点 $x_0$ **可微**, 而 $A\Delta x$ 称为 $f(x)$ 在 $x_0$ 的微分, 记作 $dy$, 即
\[dy=A\Delta x\]
**定理**: 函数 $y=f(x)$ 在点 $x_0$ 可微的充要条件是 $y=f(x)$ 在点 $x_0$ 处可导, 且 $A=f'(x_0)$, 即 $dy=f'(x_0)\Delta x$

**说明**: $\Delta y=f'(x_0)\Delta x+o(\Delta x)\quad dy=f'(x_0)\Delta x$ 当 $f'(x_0)\ne0$ 时,
\[\lim_{\Delta x\to0}\frac{\Delta y}{dy}=\lim_{\Delta x\to0}\frac{\Delta y}{f'(x_0)\Delta x}\\=\frac1{f'(x_0)}\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x}=1\]
所以 $\Delta x\to0$ 时 $\Delta y$ 与 $dy$ 是等价无穷小, 故当 $|\Delta x|$
很小时, 有近似公式 $\Delta y\approx dy$

###ii.微分运算法则
设 $u(x),v(x)$ 均可微, 则
\[\begin{array}{ll}
1.d(u\pm v)=du\pm dv&2.d(Cu)=Cdu(C为常数)\\
3.d(uv)=vdu+udv&4.d(\frac uv)=\frac{vdu-udv}{v^2}(v\ne0)
\end{array}\]
**复合函数的微分**: $y=f(u),u=\varphi(x)$ 分别可微, 则复合函数 $y=f[\varphi(x)]$ 的微分为 $dy=y'_ xdx=f'(u)\underbrace{\varphi'(x)dx}_{du\,微分形式不变},dy=f'(u)du$
###iii.微分在近似计算中的应用
\[\Delta y=f'(x_0)\Delta x+o(\Delta x)\]
当 $\Delta x$ 很小时, 得近似等式:
\[\Delta y=f(x_0+\Delta x)-f(x_0)\approx f'(x_0)\Delta x\\f(x_0+\Delta x)\approx f(x_0)+f'(x_0)\Delta x\xrightarrow{x=x_0+\Delta x}\\f(x)\approx f(x_0)+f'(x_0)(x-x_0)\]
###iv.微分在估计误差中的应用
某量的精确值为 $A$, 其近似值为 $a$, $A-a$ 称为 $a$ 的 **绝对误差**, $\displaystyle\frac{|A-a|}{|a|}$ 称为 $a$ 的 **相对误差**

若 $|A-a|\le\delta_A$, $\delta_A$ 称为测量 $A$ 的 **绝对误差限**, $\displaystyle\frac{\delta_A}{|a|}$ 称为测量 $A$ 的 **相对误差限**

**误差传递公式**: 若直接测量某量得 $x$, 已知测量误差限为 $\delta_x$ 按公式 $y=f(x)$ 计算 $y$ 值时的误差
\[|\Delta y|\approx|dy|=|f'(x)|\cdot|\Delta x|\le|f'(x)|\cdot\delta_x\]
故 $y$ 的绝对误差限约为 $\delta_y\approx|f'(x)|\cdot\delta_x$, 相对误差限约为 $\displaystyle\frac{\delta_y}{|y|}\approx\left|\frac{f'(x)}{f(x)}\right|\cdot\delta_x$
