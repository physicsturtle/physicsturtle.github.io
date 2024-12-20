---
layout: lesson
title: Coulomb's law for continuous charge distributions 
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---

What we have said about the superposition of electric fields due to a number of charges also applies for continuous charge distributions. For a continuous distribution, the electric field at a point \\(\x\\) due to the distribution \\(\rho\\) is given by

$$\begin{equation}
\mathbf{E}(\x) = \int_{V'}\frac{\rho(\x')(\x-\x')}{|\x-\x'|^3}\d^3\x'
\end{equation}$$

where \\(\rho\\) is the volume charge density and \\(V'\\) is the volume where the charge resides. There are analogous expressions for surface and line charge densities:

$$\begin{align}
\mathbf{E}(\x) ={}& \frac{1}{4\pi\epsilon_0}\int_{A'} \frac{\sigma(\x')(\x-\x')}{|\x-\x'|^3} \d^2\x' \\
\mathbf{E}(\x) ={}& \frac{1}{4\pi\epsilon_0}\int_{L'} \frac{\lambda(\x')(\x-\x')}{|\x-\x'|^3}\d\ell'.
\end{align}$$

These expressions have been written somewhat compactly. For clarity, if we expand out e.g. the volume formula, we get 

$$\begin{equation}
\mathbf{E}(\x) = \frac{1}{4\pi\epsilon_0}\int\frac{(x-',y-y',z-z')\rho(\x')}{[(x-x')^2+(y-y')^2+(z-z')^2]^{3/2}}\d x' \d y' \d z'.
\end{equation}$$


<div class="example">
<b>Example:</b>
Consider an infinite line of charge, with linear charge density \(\lambda\). Compute the electric field at all points in space. 




<b>Solution:</b> 
We suppose that the line of charge runs along the \(z\)-axis, and we will compute the electric field at a distance \(r\) away from the wire. By symmetry, we may as well compute the electric field at the point \((r,0,0)\). Furthermore, we note that the electric field should point radially outwards (assuming \(\lambda\) is positive), so we do not need to compute the other components of the field.

<figure class="center"><p><img src="figures/efield_infinite_wire_coulomb_law.pdf" alt="Function" class="center" style="width:232.827px;height:62.357px;"> </p></figure>

Then, we find that 

$$\begin{align}
E_x(r) ={}& \frac{1}{4\pi\epsilon_0} \int_{-\infty}^\infty \frac{\lambda\xhat\cdot((r,0,0) - (0,0,z'))}{|(r,0,0) - (0,0,z)|^3} \d z' \\
={}& \frac{1}{4\pi\epsilon_0} \int_{-\infty}^\infty \frac{\lambda r}{(r^2+z^2)^{3/2}} \d z' 
\end{align}$$

To evaluate the integral, we let \(z = r\tan\theta\), which gives us 

$$\begin{align}
E_x(r) ={}& \frac{\lambda}{4\pi\epsilon_0r} \int_{-\infty}^\infty \frac{\sec^2\theta}{(1+\tan^2\theta)^{3/2}} \d\theta \\
={}& \frac{\lambda}{4\pi\epsilon_0r} \int_{-\pi/2}^{\pi/2} \frac{\sec^2\theta}{(1+\tan^2\theta)^{3/2}} \d\theta \\
={}& \frac{\lambda}{4\pi\epsilon_0r} \int_{-\pi/2}^{\pi/2} \cos\theta \d\theta \\
={}& \frac{\lambda}{4\pi\epsilon_0r} \sin\theta\bigg|_{-\pi/2}^{\pi/2} \\
={}& \frac{\lambda}{2\pi\epsilon_0r}
\end{align}$$

Thus, we conclude that \(\mathbf{E} = \frac{\lambda}{2\pi\epsilon_0 r}\rhat\) anywhere in space. Note that, here, \(r = \sqrt{x^2+y^2}\) is the cylindrical radial coordinate, not the spherical one.


</div>

