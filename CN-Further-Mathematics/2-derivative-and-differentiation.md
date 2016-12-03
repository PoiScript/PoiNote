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
