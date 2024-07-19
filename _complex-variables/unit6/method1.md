---
layout: lesson
title: Integrals of Type I
dept: math
course: complex-variables
unit: unit6
deptDisplay: Math
courseDisplay: Complex Variables
unitDisplay: Unit VI
---

Here, we consider integrals of the form 

$$I = \int_{0}^{2\pi} f(\cos\theta,\sin\theta) d\theta.$$

To evaluate this integral, we note that the trigonometric functions can be written as

$$\cos\theta = \frac{e^{i\theta} + e^{-i\theta}}{2},\qquad \sin\theta = \frac{e^{i\theta} - e^{-i\theta}}{2i}.$$

Thus we make the variable substitution $z = e^{i\theta}$, $dz = i e^{i\theta} d\theta = izd\theta$ so that the integral becomes 

$$\begin{eqnarray*}
I &=& \int_{0}^{2\pi} f(\cos\theta,\sin\theta) d\theta \\
&=& \int_0^{2\pi} f\left(\frac{e^{i\theta} + e^{-i\theta}}{2}, \frac{e^{i\theta} - e^{-i\theta}}{2i}\right) d\theta \\
&=& \oint_C f\left(\frac{z + \frac{1}{z}}{2}, \frac{z - \frac{1}{z}}{2i}\right) \frac{dz}{iz}
\end{eqnarray*}$$

where the contour $C$ is the unit circle traversed counterclockwise. Following this, we can use Cauchy's integral theorem and calculate the residues at each of the poles. Let's do some examples.

<div class="example">
<p><b>Example:</b> Evaluate the integral 
$$I = \int_0^{2\pi} \frac{1}{2+\sin^2\theta} d\theta$$
</p>
<b>Solution:</b> To evaluate this integral, we apply the method outlined above. 

</div>
