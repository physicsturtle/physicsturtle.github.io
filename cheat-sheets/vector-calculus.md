---
layout: page
title: Vector Calculus Formulas
permalink: /cheat-sheets/vector-calculus/
---
The formulas for gradient, divergence, curl, and Laplacian in cartesian coordinates are: 

## Cartesian

#### Gradient

\\[ \nabla f = \frac{\partial f}{\partial x}\hat{\textbf{x}} + \frac{\partial f}{\partial y}\hat{\textbf{y}} + \frac{\partial f}{\partial z}\hat{\textbf{z}} \\]

#### Divergence

\\[ \nabla\cdot\textbf{F} = \frac{\partial F_x}{\partial x} + \frac{\partial F_y}{\partial y} + \frac{\partial F_z}{\partial z} \\]

#### Curl

$$\nabla\times\textbf{F} = \begin{vmatrix} \hat{\textbf{x}} & \hat{\textbf{y}} & \hat{\textbf{z}} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ F_x & F_y & F_z \end{vmatrix} $$

which, after expanding, yields

$$\nabla\times\textbf{F} = \left(\frac{\partial F_z}{\partial y} - \frac{\partial F_y}{\partial z}\right)\hat{\textbf{x}} + \left(\frac{\partial F_x}{\partial z} - \frac{\partial F_z}{\partial x}\right)\hat{\textbf{y}} + \left(\frac{\partial F_y}{\partial x} - \frac{\partial F_x}{\partial y}\right)\hat{\textbf{z}} $$

#### Laplacian

$$\nabla^2 f = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2} $$

First we start with the transformations between Cartesian, cylindrical, and spherical coordinates.


## Cylindrical Coordinates

### Coordinate Transformations
$$\left\{\begin{eqnarray}
x &=& \rho \cos\varphi \\
y &=& \rho \sin\varphi \\
z &=& z
\end{eqnarray}\right. $$

$$\left\{\begin{eqnarray}
\rho &=& \sqrt{x^2+y^2}\\
\varphi &=& \arctan\left(\frac{y}{x}\right) \\
z &=& z
\end{eqnarray}\right. $$

$$\left\{\begin{eqnarray}
\hat{\textbf{x}} &=& \cos\varphi\hat{\boldsymbol{\rho}} - \sin\varphi \hat{\boldsymbol{\varphi}}\\
\hat{\textbf{y}} &=& \sin\varphi\hat{\boldsymbol{\rho}}  + \cos\varphi\hat{\boldsymbol{\varphi}} \\
\hat{\textbf{z}} &=& \hat{\textbf{z}}
\end{eqnarray}\right. $$

$$\left\{\begin{eqnarray}
\hat{\boldsymbol{\rho}} &=& \cos\varphi\hat{\textbf{x}} + \sin\varphi\hat{\textbf{y}}\\
\hat{\boldsymbol{\varphi}} &=& = -\sin\varphi\hat{\textbf{x}} + \cos\varphi\hat{\textbf{y}}\\
\hat{\textbf{z}} &=& \hat{\textbf{z}}
\end{eqnarray}\right. $$

#### Gradient

\\[ \nabla f = \frac{\partial f}{\partial \rho}\hat{\boldsymbol{\rho}} + \frac{1}{\rho}\frac{\partial f}{\partial \varphi}\hat{\boldsymbol{\varphi}} + \frac{\partial f}{\partial z}\hat{\textbf{z}} \\]

#### Divergence

\\[ \nabla\cdot\textbf{F} = \frac{1}{\rho}\frac{\partial}{\partial \rho}\left(\rho F_\rho \right) + \frac{1}{\rho}\frac{\partial F_\varphi}{\partial \varphi} + \frac{\partial F_z}{\partial z} \\]

#### Curl

$$\nabla\times\textbf{F} = \left(\frac{1}{\rho}\frac{\partial F_z}{\partial\varphi} - \frac{\partial_\varphi}{\partial z}\right)\hat{\boldsymbol{\rho}} + \left(\frac{\partial F_\rho}{\partial z} - \frac{\partial F_z}{\partial\rho}\right)\hat{\boldsymbol{\varphi}} + \frac{1}{\rho}\left(\frac{\partial}{\partial \rho}\left(\rho F_\varphi\right) - \frac{\partial F_\rho}{\partial\varphi}\right)\hat{\textbf{z}}$$

#### Laplacian

$$\nabla^2 f = \frac{1}{\rho}\frac{\partial}{\partial\rho}\left(\rho\frac{\partial f}{\partial \rho}\right) + \frac{1}{\rho^2}\frac{\partial^2 f}{\partial \varphi^2} + \frac{\partial^2 f}{\partial z^2} $$


## Spherical Coordinates

$$\left\{\begin{eqnarray}
x &=& r\sin\theta\cos\varphi\\
y &=& r\sin\theta\sin\varphi\\
z &=& r\cos\theta
\end{eqnarray}\right.$$

$$\left\{\begin{eqnarray}
r &=& \sqrt{x^2+y^2+z^2}\\
\theta &=& \arctan\left(\frac{\sqrt{x^2+y^2}}{z}\right)\\
\varphi&=& \arctan\left(\frac{y}{x}\right)
\end{eqnarray}\right.$$

$$\left\{\begin{eqnarray}
\hat{\textbf{x}} &=& \sin\theta\cos\varphi\hat{\textbf{r}} + \cos\theta\cos\varphi\hat{\boldsymbol{\theta}} - \sin\varphi\hat{\boldsymbol{\varphi}}\\
\hat{\textbf{y}} &=& \sin\theta\sin\varphi\hat{\textbf{r}} + \cos\theta\sin\varphi\hat{\boldsymbol{\theta}} + \cos\varphi\hat{\boldsymbol{\varphi}} 
\\\
\hat{\textbf{z}} &=& \cos\theta\hat{\textbf{r}} - \sin\theta \, \hat{\boldsymbol{\theta}}
\end{eqnarray}\right.$$

$$\left\{\begin{eqnarray}
\hat{\textbf{r}} &=& \sin\theta\cos\varphi\hat{\textbf{x}} + \sin\theta\sin\varphi\hat{\textbf{y}} + \cos\theta\hat{\textbf{z}}\\
\hat{\boldsymbol{\theta}} &=& \cos\theta\cos\varphi\hat{\textbf{x}} + \cos\theta\sin\varphi\hat{\textbf{y}} - \sin\theta\hat{\textbf{z}} \\
\hat{\boldsymbol{\varphi}} &=& -\sin\varphi\hat{\textbf{x}} + \cos\varphi\hat{\textbf{y}}
\end{eqnarray}\right.$$


#### Gradient 

\\[ \nabla f = \frac{\partial f}{\partial r}\hat{\textbf{r}} + \frac{1}{r}\frac{\partial f}{\partial \theta}\hat{\boldsymbol{\theta}} + \frac{1}{r\sin\theta}\frac{\partial f}{\partial\varphi} \hat{\boldsymbol{\varphi}} \\]

#### Divergence

\\[ \nabla\cdot\textbf{F} = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2 F_r\right) + \frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta F_\theta \right) + \frac{1}{r\sin\theta}\frac{\partial F_\varphi}{\partial\varphi} \\]

#### Curl

$$\nabla\times\textbf{F} = \frac{1}{r\sin\theta}\left(\frac{\partial}{\partial\theta}\left(\sin\theta F_\varphi\right) - \frac{\partial F_\theta}{\partial \varphi}\right)\hat{\textbf{r}} + \frac{1}{r}\left(\frac{1}{\sin\theta}\frac{\partial F_r}{\partial\varphi} - \frac{\partial}{\partial r}\left(r F_\varphi\right)\right)\hat{\boldsymbol{\theta}} + \frac{1}{r}\left(\frac{\partial}{\partial r}\left(r F_\theta\right) - \frac{\partial F_r}{\partial \theta}\right)\hat{\boldsymbol{\varphi}}$$

#### Laplacian

$$\nabla^2 f = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial f}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial f}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2 f}{\partial\varphi^2}$$


