---
layout: page
title: empty
course: test
unit: unit1
permalink: /test/empty/
---








Now, we evaluate the angular integral. This can be done in various ways. One nice way is to consider 

$$\int e^{-r^2} d^d\r$$

and to evaluate it in two ways. In the first way, we write it in terms of an angular part and a radial part because we have a radially symmetric function. Let $\Omega_d$ be the solid angle of a $d-1$-dimensional sphere. So for $d = 2$, we consider a circle, $d=3$ a sphere, and so on. Then, let $\Omega_d(r)$ be the surface area of a $d-1$ dimensional sphere of radius $r$ (we expect $\Omega_2 = 2\pi$, $\Omega_2(r) = 2\pi r$, $\Omega_3 = 4\pi$, $\Omega_3(r) = 4\pi r^2$, and so on). These quantities relate to one another via $\Omega_d(r) = r^{d-1}\Omega_d$

\begin{align*}
\int e^{-r^2} d^d\r =& \int_0^\infty e^{-r^2}\Omega_d(r)  dr\\
=& \Omega_d \int_0^\infty e^{-r^2} r^{d-1} dr \\
=& \Omega_d \int_0^\infty e^{-y} y^{\frac{d-1}{2}} \frac{dy}{2\sqrt{y}} \\
=& \frac{\Omega_d}{2}\int_0^\infty y^{d/2-1}e^{-y}  dy\\
=& \frac{\Omega_d}{2}\Gamma(d/2-1).
\end{align*}

The other way to evaluate it is 

\begin{align*}
\int e^{-r^2} d\r =& \int_{-\infty}^\infty \cdots \int_{-\infty}^\infty e^{-x_1^2 - x_2^2 - \cdots - x_d^2} dx_1 dx_2 \cdots dx_d\\
=&  \sqrt{\pi}^d
\end{align*}

Thus, 

$$\Omega_d = \frac{2\pi^{d/2}}{\Gamma(d/2-1)}.$$
