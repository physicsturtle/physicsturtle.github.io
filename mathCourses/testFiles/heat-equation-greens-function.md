---
layout: page
title: Green's Function for the Heat Equation
course: test
unit: unit1
permalink: /test/heat-equation-greens-function/
---

In this lesson, we will construct the Green's function for the problem

$$\begin{cases}
u_t = \alpha^2 \nabla^2 u + g(\textbf{x},t) \\
u(\partial\Omega) = f(\textbf{x},t) \\
u(\textbf{x},0) = u_0(\textbf{x})
\end{cases}$$

Let $Lu = \alpha^2\nabla^2 u - u_t$, and $L^*u = \alpha^2 \nabla^2 u + u_t$. Consider the space-time cylinder $C_T = \Omega\times[0,T]$. Integrate over this spacetime to get 

$$\int_{C_T} v(\alpha^2\nabla^{\prime 2} u - u_t) d\textbf{x}' dt' = \int_0^T \int_\Omega v\alpha^2\nabla^{\prime 2} u d\textbf{x}' dt' - \int_\Omega \int_0^T v u_{t'} dt' d\textbf{x}'$$
If we apply Green's second identity on the first term, we get 

$$ = \int_0^T \left( \int_{\partial\Omega}  ((\nabla' u) v - (\nabla' v) u )\cdot\hat{\textbf{n}} D dS' + \int_\Omega D(\nabla^{\prime 2} v) u d\textbf{x}'\right) dt' - \int_\Omega \left(vu\bigg|_0^T - \int_0^T v_{t'} u dt'\right) d\textbf{x}'$$

If we rewrite this in terms of the operator $L^*$ by rearranging terms, then we get 

$$= \int_{C_T} u L^* v d\textbf{x}' dt' + D\int_0^T\int_{\partial\Omega} ((\nabla' u) v - (\nabla' v)u) \cdot\hat{\textbf{n}} dS' dt' - \int_\Omega (vu)\bigg|_0^T d\textbf{x}'$$

If we set $v = 0$ on $\partial\Omega$, $v = 0$ for $t' > t$, and $L^* v = \delta(\textbf{x}' - \textbf{x}, t' - t)$ for $ 0 < t < T$, then many terms disappear:

$$= \int_{C_T} v(-g) d\textbf{x}' dt' = u(\textbf{x},t) + D\int_0^T\int_{\partial\Omega} -\frac{\partial v}{\partial n'} f d S' dt' + \int_\Omega v u_0(\textbf{x}') d\textbf{x}'$$

This leads to the following integral representation for $u$:

$$u(\textbf{x},t) = -\int_{C_T} vg d\textbf{x}' dt' + \int_0^T\int_{\partial\Omega} f\frac{\partial v}{\partial n'} dS' dt' - \int_\Omega v u_0 d\textbf{x}'$$

This can be related to the heat kernel $G$, which solves the problem (insert here) via $G(\textbf{x}';\textbf{x}, t-t') = v(\textbf{x}'; \textbf{x}, t')$. 




