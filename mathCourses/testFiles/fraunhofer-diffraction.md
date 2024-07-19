---
layout: page
title: Fraunhofer Diffraction
course: test
unit: unit1
permalink: /test/fraunhofer-diffraction/
---

In this section, we will consider Fraunhofer diffraction. Suppose we have a monochromatic wave incident on a mask with mask function $f(x',y')$. Then, the electric field at a point $(x,y,z)$ will be 

$$E = \frac{E_0}{4\pi r}\int_{-\infty}^\infty \int_{-\infty}^\infty e^{ikr}f(x',y') dx' dy' $$

This formula is quite unwieldly as is, so we can make an approximation of $r$ to make it easier to evaluate. Defining $R = \sqrt{x^2+y^2+z^2}$, we have
$$\begin{eqnarray*}
r &=& \sqrt{z^2+(x-x')^2 + (y-y')^2} \\
&\sim & \sqrt{z^2+x^2 - 2xx' + y^2 - 2yy'} \\
&=& \sqrt{R^2 - 2xx' - 2yy'} \\
&=& R\sqrt{1 - \frac{2xx' + 2yy'}{R^2}}\\
&=& R - \frac{xx' + yy'}{R}
\end{eqnarray*}$$

Plugging this into our fomula for the electric field, we can produce the wave amplitude in the Fraunhofer approximation, which is 

$$\begin{eqnarray*}
E &=& \frac{E_0}{4\pi r}\int_{-\infty}^\infty \int_{-\infty}^\infty e^{ik\left(R - \frac{xx'+yy'}{R}\right)}f(x',y') dx' dy'\\
&=& \frac{E_0 e^{ikR}}{4\pi R}\int_{-\infty}^\infty \int_{-\infty}^\infty e^{-ik\left(\frac{xx'+yy'}{R}\right)}f(x',y') dx' dy'
\end{eqnarray*}$$



<div class="example">
For a Gaussian mask (rectangular), 

\begin{eqnarray*}
E &=& \frac{E_0 e^{ikR}}{4\pi R}\int_{-\infty}^\infty e^{-x^{\prime 2}/2\sigma^2}e^{-ikx'} dx'\\
&=& \frac{E_0 e^{ikR}{4\pi R}\sqrt{\frac{\pi\sigma^2}{2}} e^{-\pi^2 k_x^2 \sigma^2/2}}\\
&=& \frac{E_0 \sigma e^{ikR}{4\pi R}\sqrt{\frac{\pi}{2}} e^{-\pi^2 k_x^2 \sigma^2/2}}\\
\end{eqnarray*}
where $k_x = kx/R = k\theta$. 

</div>


