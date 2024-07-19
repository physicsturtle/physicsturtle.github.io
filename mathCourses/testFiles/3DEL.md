---
layout: page
title: 3D Euler Lagrange?
course: test
unit: unit1
permalink: /test/3DEL
---

Since we want to consider a surface \\(u\\) as a function of \\(x, y\\) space coordinates and time \\(t\\), we will derive the Euler Lagrange equation for a problem in three general independent variables, \\(x^1,x^2,x^3\\).

We want to consider the problem of extremizing the functional 

$$\mathcal{S}[u] = \int_R \mathcal{L}(\textbf{x},u,\nabla u) d^3\textbf{x} $$

over all differentiable functions 

$$u : R\subset\mathbb{R}^3 \to \mathbb{R}$$

where \\(u(\partial R)\\) is given. Note that we will employ generalized coordinates in this section for ease of notation. Then consider the one parameter family of functions 

$$U(\textbf{x}) = u(\textbf{x}) + \epsilon \eta(\textbf{x})$$

with \\(\eta(\partial R) = 0\\). We note that \\(\left.\frac{d\mathcal{S}}{d\epsilon}\right|_{\epsilon = 0} = 0\\), and plug \\(U\\) into the functional \\(\mathcal{S}\\) to obtain

$$\mathcal{S}[U] = \int_R \mathcal{L}(\textbf{x},U,\nabla U) d^3\textbf{x}. $$

Then we need to differentiate with respect to $\epsilon$.

$$\begin{eqnarray*}
\frac{d}{d\epsilon} \mathcal{S}[U] &=& \frac{d}{d\epsilon} \int_R \mathcal{L}(\textbf{x},U,\nabla U) d^3\textbf{x}\\
&=& \int_R \left(\frac{\partial \mathcal{L}}{\partial U}\frac{dU}{d\epsilon} + \frac{\partial \mathcal{L}}{\partial U_{x^i}}\frac{dU_{x^i}}{d\epsilon}\right) d^3\textbf{x}\\
&=& \int_R \left(\frac{\partial \mathcal{L}}{\partial U}\eta + \frac{\partial \mathcal{L}}{\partial U_{x^i}}\frac{\eta}{x^i}\right) d^3\textbf{x}
\end{eqnarray*}$$

We can then set $\epsilon = 0$ and simplify, because \\(U = u\\) when \\(\epsilon = 0\\).

$$ \begin{eqnarray}
\left.\frac{d}{d\epsilon} \mathcal{S}[U]\right|_{\epsilon = 0} &=& \int_R \left(\frac{\mathcal{L}}{u}\eta + \frac{\mathcal{L}}{u_{x^i}}\frac{\eta}{x^i}\right) d^3\textbf{x} \notag \\
0 &=& \int_R \frac{\mathcal{L}}{u}\eta \,d^3\textbf{x} + \int_R \left(\frac{\mathcal{L}}{u_{x^i}}\frac{\eta}{x^i}\right) \, d^3\textbf{x} \notag \\
0 &=& \int_R \frac{\mathcal{L}}{u}\eta \,d^3\textbf{x} + \int_R \left(\frac{\mathcal{L}}{u_{x^1}}, \frac{\mathcal{L}}{u_{x^2}},\frac{\mathcal{L}}{u_{x^3}}\right)\cdot \nabla \eta \, d^3\textbf{x} \notag \\
0 &=& \int_R \frac{\mathcal{L}}{u}\eta \,d^3\textbf{x} + \cancelto{0}{\oint_{\partial R}\eta \left(\frac{\mathcal{L}}{u_{x^1}}, \frac{\mathcal{L}}{u_{x^2}},\frac{\mathcal{L}}{u_{x^3}}\right) \cdot \hat{\textbf{n}} dS} -  \int_R \eta \nabla\cdot \left(\frac{\mathcal{L}}{u_{x^1}}, \frac{\mathcal{L}}{u_{x^2}},\frac{\mathcal{L}}{u_{x^3}}\right)  d^3\textbf{x} \notag \\
0 &=& \int_R \eta\left( \frac{\mathcal{L}}{u} - \nabla\cdot \left(\frac{\mathcal{L}}{u_{x^1}}, \frac{\mathcal{L}}{u_{x^2}},\frac{\mathcal{L}}{u_{x^3}}\right)\right) d^3\textbf{x} \label{ELIntegral}
\end{eqnarray} $$

Since Equation \eqref{ELIntegral} must hold for \textit{all} $\eta$ for which $\eta(R) = 0$, we conclude that 
\begin{equation} \frac{\mathcal{L}}{u}- \nabla\cdot \left(\frac{\mathcal{L}}{u_{x^1}}, \frac{\mathcal{L}}{u_{x^2}},\frac{\mathcal{L}}{u_{x^3}}\right) = 0 \label{ELEq} \end{equation}
is the necessary condition for the functional $\mathcal{S}$ to be extremized.  
