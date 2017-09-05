# Direction Cosine

\[\vec{a_r}=\frac{\vec{r}}{r}=\frac{\vec{a_x}r\cos\alpha+\vec{a_y}r\cos\beta+\vec{a_z}r\cos\gamma}{r}=\vec{a_x}\cos\alpha+\vec{a_y}\cos\beta+\vec{a_z}\cos\gamma\]

# Dot Product
\[\vec{A}\cdot\vec{B}=|\vec{A}||\vec{B}|\cos\theta\]

\[\vec{A}\cdot(\vec{B}+\vec{C})=\vec{A}\cdot \vec{B}+\vec{A}\cdot\vec{C}\]

\[\begin{cases}
    \vec{a_{r}}=\vec{a_x}\cos\alpha+{a_y}\cos\beta+\vec{a_z}\cos\gamma\\
    \vec{r}=\vec{a_x}x+\vec{a_y}y+\vec{a_z}z
\end{cases}\]


# Cross Product

\[\vec{A}\times\vec{B}=|\vec{A}||\vec{B}|\sin\theta\]

# Triple Product

## Scalar Triple Product

\[\vec{C}\cdot\vec{A}\times\vec{B}=ABC\sin\theta\cos\varphi\]

## Vector Triple Product

\[\vec{C}\cdot(\vec{A}\times\vec{B})=\vec{B}\cdot(\vec{C}\times\vec{A})\vec{A}\cdot(\vec{B}\times\vec{C})\]

\[\vec{A}\times(\vec{B}\times\vec{C})=\vec{B}(\vec{A}\cdot\vec{C})-\vec{C}(\vec{A}\cdot \vec{B})\]

# Cartesian Coordinate System

\[\vec{a_x}\cdot\vec{a_{x}}=\vec{a_y}\cdot\vec{a_{y}}=\vec{a_z}\cdot\vec{a_{z}}=1\]

\[\vec{a_x}\cdot\vec{a_{y}}=\vec{a_y}\cdot\vec{a_{z}}=\vec{a_z}\cdot\vec{a_{x}}=0\]

\[\vec{a_x}\cdot\vec{a_{x}}=\vec{a_y}\cdot\vec{a_{y}}=\vec{a_z}\cdot\vec{a_{z}}=1\]

\[\begin{cases}
  \vec{a_x}\times\vec{a_y}=\vec{a_z}\\
  \vec{a_y}\times\vec{a_z}=\vec{a_x}\\
  \vec{a_z}\times\vec{a_x}=\vec{a_y}
\end{cases}\]

\[\begin{cases}
  \vec{A}=\vec{a_x}A_x+\vec{a_y}A_y+\vec{a_z}A_z\\
  \vec{B}=\vec{a_x}B_x+\vec{a_y}B_y+\vec{a_z}B_z
\end{cases}\]

\[|\vec{A}|=\sqrt{A_x^2+A_y^2+A_z^2}\]


\[\vec{A}\cdot\vec{B}=A_xB_x+A_yB_y+A_zB_z\]
\[\vec{A}\times\vec{B}=\vec{a_x}(A_yB_z-A_zB_y)+\vec{a_y}(A_zB_x-A_xB_z)+\vec{a_z}(A_xB_y-A_yB_x)=
\begin{vmatrix}
  \vec{a_x} & \vec{a_y} & \vec{a_z}\\
  A_x       & A_y       & A_z      \\
  B_x       & B_y       & B_z      \\
\end{vmatrix}\]

\[\vec{r}=\vec{a_x}x+\vec{a_y}y+\vec{a_z}z\]
\[d\vec{r}=d\vec{l}=\vec{a_x}dx+\vec{a_y}dy+\vec{a_z}dz\]
\[d\vec{S_x}=\vec{a_x}dzdy\]
\[d\vec{S_y}=\vec{a_y}dxdz\]
\[d\vec{S_z}=\vec{a_z}dxdy\]
\[d\tau=dxdydz\]

# Cylindrcal Coordinate System

\[\vec{a_{\rho}}\times\vec{a_{\rho}}=\vec{a_{\phi}}\times\vec{a_{\phi}}=\vec{a_z}\times\vec{a_z}=0\]

\[\vec{a_{\rho}}\times\vec{a_{\phi}}=\vec{a_z}\]
\[\vec{a_{\phi}}\times\vec{a_z}=\vec{a_{\rho}}\]
\[\vec{a_z}\times\vec{a_{\rho}}=\vec{a_{\phi}}\]

\[x=\rho\cos\phi\]
\[y=\rho\sin\phi\]
\[\rho=\sqrt{x^2+y^2}\]
\[\phi=\arctan\frac{y}{x}\]
\[\vec{r}=\vec{a_{\rho}}\rho+\vec{a_z}z\]
