---
layout: page
title: Helmholtz Equation Green's Function
course: test
unit: unit1
permalink: /test/helmholtz-greens-function/
---

We know that the free space Green's function for the operator $\nabla^2 - k^2$ is $G = -\frac{e^{-kr}}{4\pi r}$. We could simply substitute $k \mapsto ik$ and find the Green's function for the Helmhotlz operator, but we present here an alternate approach. (what about $k\mapsto -ik$?)

Consider the Helmholtz equation with point source
$$(\nabla^{2} + \lambda^2)u = \rho(\textbf{x}).$$
Note that normally, the Helmhltz equation is written with $k$ instead of $\lambda$, but we will be using $k$ for a different purpose later. 

We are interested in calculating the Green's function for this equation, where the Green's function satisfies the equation with delta function
$$(\nabla^{\prime 2} + \lambda^2)G = \delta(\textbf{x} - \textbf{x}')$$
where the Laplacian is taken with respect to the primed coordinates. In order to find the Green's function, we can apply the Fourier transform. Taking the three-dimensional Fourier transform of both sides, we get 

$$\int_{\mathbb{R}^3}e^{-i\textbf{k}\cdot\textbf{x}'}(\nabla^{\prime 2} + \lambda^2)G d^3\textbf{x}' = \int_{\mathbb{R}^3} e^{-i\textbf{k}\cdot\textbf{x}'}\delta(\textbf{x} - \textbf{x}') d^3\textbf{x}'$$

We can use Green's second identity on the term with the Laplacian and simplify, so that we get 

$$\begin{eqnarray*}
\frac{1}{(2\pi)^{3/2}}\int_{\mathbb{R}^3}\left[G \nabla^{\prime 2} e^{-i\textbf{k}\cdot\textbf{x}'} \right]d^3\textbf{x}' +  \lambda^2  \hat{G} &=& \frac{1}{(2\pi)^{3/2}}e^{-i\textbf{k}\cdot\textbf{x}} \\
-k^2\hat{G} + \lambda^2\hat{G} &=& \frac{1}{(2\pi)^{3/2}} e^{-i\textbf{k}\cdot\textbf{x}} 
\end{eqnarray*}$$

If we solve for $\hat{G}$, all we need to do is invert the Fourier transform. $\hat{G}$ is given by

$$\hat{G} = \frac{e^{-i\textbf{k}\cdot\textbf{x}}}{(2\pi)^{3/2}(\lambda^2 - k^2)}.$$

Thus the Green's function is 

$$G = \frac{1}{(2\pi)^3}\iiint \left(\frac{e^{-i\textbf{k}\cdot\textbf{x}}}{\lambda^2 - k^2}\right)e^{i\textbf{k}\cdot\textbf{x}'} d^3\textbf{k}$$

All that is left is evaluating this integral. Defining $r = \|\textbf{x} - \textbf{x}'\|$ and defining the $z$ axis for our integration by aligning it with $\textbf{x} - \textbf{x}'$ (this means that the angle between $\textbf{k}$ and $\textbf{x} - \textbf{x}'$ is the polar angle $\theta$), we evaluate the dot product and write explicitly the bounds of integration. 

$$G = \frac{1}{(2\pi)^3}\int_0^\infty \int_0^\pi \int_0^{2\pi} \left(\frac{e^{-ikr\cos\theta}}{\lambda^2 - k^2}\right) k^2 \sin\theta d\varphi d\theta dk$$

First, we evaluate the $\varphi$ integral, which simply contributes a factor of $2\pi$. 

$$G = \frac{1}{(2\pi)^2}\int_0^\infty \int_0^\pi \frac{k^2\sin\theta e^{-ikr\cos\theta}}{\lambda^2 - k^2}  d\theta dk$$

We can use a simple substitution to do the $\theta$ integral, which gives 

$$\begin{eqnarray*}
G &=& \frac{1}{(2\pi)^2ir}\int_0^\infty \frac{k e^{-ikr\cos\theta}}{\lambda^2 - k^2}\bigg|_{\theta = 0}^{\theta = \pi}  dk\\
&=&  \frac{1}{(2\pi)^2ir}\int_0^\infty \frac{k \left(e^{ikr} -e^{-ikr}\right) }{\lambda^2 - k^2} dk \\
&=& \frac{1}{2\pi^2r}\int_0^\infty \frac{k \sin(kr)}{\lambda^2 - k^2} dk \\
&=& \frac{1}{4\pi^2r}\int_{-\infty}^\infty \frac{k \sin(kr)}{\lambda^2 - k^2} dk
\end{eqnarray*}$$

where, in the last step, we have extended the range to be $\pm\infty$ because the integrand is even in $k$. The integrand has two poles at $k = \pm\lambda$ in the complex plane. To evaluate the integral, we consider its Cauchy principal value. It is useful to consider $k$ as a variable in the complex plane, for which we will turn the sine back into complex exponentials (we only turned it into a sine before so that it was obvious that the integrand is even).

$$G = \frac{1}{4\pi^2r}\int_{-\infty}^\infty \frac{k \sin(kr)}{\lambda^2 - k^2} dk = \frac{1}{8i\pi^2r}\left[\int_{-\infty}^\infty \frac{k e^{ikr} }{\lambda^2 - k^2} dk + \int_{-\infty}^\infty \frac{k e^{-ikr}}{\lambda^2 - k^2} dk\right].$$

and consider the following two contours in the $k$ plane. Call $I_1$ the contour in the upper half plane and $I_2$ the contour in the lower half plane. The first of the two integrals we evaluate along $I_1$ and the second along $I_2$. 

Upon evaluation (fill in details later), we obatin the Green's function 
$$G(r) = -\frac{e^{-ikr}}{4\pi r}$$
where $r = \|\textbf{x} - \textbf{x}'\|$.




QUESTION: can you use the method of images to find an appropriate green's function if we have a particle in the half space for example?

