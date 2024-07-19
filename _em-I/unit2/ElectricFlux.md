---
layout: lesson
title: Electric Flux 
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---
In the section on Coulomb's law, we found one method of computing the electric field. Although it is very general, it is often quite cumbersome to evaluate the integrals. There are, thankfully, other methods to compute the electric field of a charge distribution. One of these methods is known as Gauss's law, which is one of the four Maxwell equations that we will meet throughout the notes. We will come to Gauss's law later, but we first need the idea of <i>electric flux</i>. 

In general, if we have some surface \\(S\\), we can define the flux \\(\Phi\\) through it by

$$\begin{equation}
\Phi = \int_{S} \mathbf{E}\cdot \d\mathbf{S}.
\end{equation}$$

Pictorially, we can imagine this integral as the sum of the fluxes through small infinitesimally small elements, as shown in the Figure. In the Figure, we have an electric field vector \\(\mathbf{E}\\). The normal vector to the surface is given by \\(\nhat\\), where \\(\d\mathbf{S} = \nhat \d S\\). The units of \\(\d \mathbf{S}\\) are area. Then, the integral represents the sum of the flux through all of the small area elements.

<figure class="center">
<p><img src="figures/flux_definition.pdf" alt="Function" class="center" style="width:165.866px;height:134.646px;"> </p><figcaption class="center">Illustration of the electric flux through a surface element \(\d S\)</figcaption> 
</figure>

<div class="example">
<b>Example:</b>
A point charge \(q\) is at the origin. Consider a circular surface of radius \(a\) that is normal to \(\zhat\), at a distance \(\ell\) from \(q\). The centre of the circular surface is directly above the origin. See the figure. What is the electric flux through the surface?

<figure class="center"><p><img src="figures/circular_surface_flux.pdf" alt="Function" class="center" style="width:145.42px;height:163.594px;"> </p></figure>


<b>Solution:</b> First, note that this is an <i>open</i> surface. This means that Gauss's law does not help us in this situation, because Gauss's law only applies to closed surfaces. This means that we have to proceed directly from the definition of the flux. 

Consider an annulus in the circle of radius differential \(\d r\). Let \(r^2 = x^2+y^2\). Thus, the <i>magnitude</i> of the electric field on this annulus is given by

$$\begin{equation}
E = \frac{q}{4\pi \epsilon_0 (r^2+\ell^2)}
\end{equation}$$


See the figure for an illustration of this annulus

<figure class="center"><p><img src="figures/circular_surface_flux_soln.pdf" alt="Function" class="center" style="width:145.42px;height:163.594px;"> </p></figure>

The flux through the surface is given by the sum of the fluxes through each of the little annuli,

$$\begin{equation}
\Phi = \int \mathbf{E}\cdot \nhat \d S = \int E\cos\theta \d S
\end{equation}$$

Since we're looking at small annuli, we have \(\d S = 2\pi r \d r\). Since the normal vector to the surface points directly upward, we have \(\cos\theta = \ell/\sqrt{r^2+\ell^2}\). Thus we have 

$$\begin{align}
\Phi ={}& \int_0^a E\cos\theta \d S \\
={}& \int_0^a \left(\frac{q}{4\pi \epsilon_0 (r^2+\ell^2)}\right)\left( \frac{\ell}{\sqrt{r^2+\ell^2}}\right) 2\pi r \d r \\
={}& \frac{q}{2\epsilon_0}\left(1-\frac{l}{\sqrt{a^2+\ell^2}}\right)
\end{align}$$

So the flux through the circular surface is 

$$\begin{equation}
\Phi =  \frac{q}{2\epsilon_0}\left(1-\frac{\ell}{\sqrt{a^2+\ell^2}}\right).
\end{equation}$$

As a sanity check, let us examine our result in a few different limits.

<ul>
<li> We see that, as \(a\to0\), we see that \(\Phi\to 0\), which makes sense because there would be no area for the electric field lines to penetrate through
</li>
<li> We see that, as \(a\to\infty\), the flux \(\Phi\to q/2\epsilon_0\). We will not necessarily be able to see why this makes sense until the next section on Gauss's law, so we encourage you to revisit this section after reading it. The total flux which would go through a closed surface surrounding charge \(q\) is \(q/\epsilon_0\). If \(a\to\infty\), then we would have an infinitely large disk, which would have half of the total flux going through it, because the other half would be going through a surface in the the \(-z\) half space.
</li></ul>


</div>

