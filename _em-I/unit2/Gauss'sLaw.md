---
layout: lesson
title: Gauss's Law 
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---
In the last section, we discussed electric flux, which is the amount of electric field lines passing through some surface. Defined mathematically, the flux through a surface \\(S\\) is 

$$\begin{equation}
\Phi = \int_S \mathbf{E} \cdot \nhat \, \d A
\end{equation}$$

where \\(\nhat\\) is the normal vector to \\(S\\). In this equation, we see that if we increase the electric field strength \\(\mathbf{E}\\), then the flux would increase. Also, if we increase the surface area, then the flux would also increase. Practically, to increase the electric field strength, one can increase the charge producing the electric field strength. Are there any general relationships about the flux through a surface \\(S\\) and the charge producing the electric field? It turns out the answer is yes, but only for <i>closed surfaces</i>. 

Gauss's law makes a statement about the relationship between the total amount of electric flux passing through the surface and the total amount of charge enclosed by the surface. 

\begin{theorem_wrapper}
\begin{theorem}
(Gauss's law) If \\(S\\) is a closed surface, and \\(Q\\) is the amount of charge enclosed by \\(S\\), then the electric flux through the surface satisfies 

$$\begin{equation}
\oint_S \mathbf{E}\cdot\nhat \, \d A = \frac{Q}{\epsilon_0}
\end{equation}$$

where \\(\nhat\\) is the unit normal vector to the surface \\(S\\). This equation is known as <i>Gauss's law</i>. Since the flux of the electric field through a surface should be thought of as the ``amount" of electric field lines passing through that surface. Thus, Gauss's law is often stated in words as: ``The electric flux through a closed surface is equal to the amount of charge enclosed within the surface". 
\end{theorem}
\end{theorem_wrapper}


Before solving some physical problems with Gauss's law, we make a few remarks.
<ol>
<li> The surface \(S\) is an <i>imaginary surface</i>, called a Gaussian surface. You are free to choose the surface in whatever way is most convenient. The only restriction is that it is a closed surface. 
</li>
<li> Gauss's law is always true, but not always useful. In particular, it is not useful if the system does not have a high degree of symmetry.
</li>
<li> Gauss's law is normally used to find the electric field due to a particular charge distribution.
</li>
<li> Gauss's law can only be used in systems with spherical, cylindrical, or planar symmetry. This is because for each of these three cases, it is possible to construct a Gaussian surface on which the following properties hold:
<ul>
</li>
<li> The electric field has constant magnitude along the surface
</li>
<li> The electric field is always either normal or perpendicular to the surface's normal vector
</li></ul>
</li>
<li> There are some small exceptions to points 1 and 3. In particular, Gauss's law may be useful in systems where there is not as much symmetry, but only when certain subparts of the system have a high degree of symmetry (namely spherical, cylindrical, or planar). 
</li></ol>

We now proceed to some examples which help us to understand Gauss's law. The practical usage of Gauss's law will be reserved for the next section. 

<div class="example">
<b>Example:</b>
In this problem, we will show that Gauss's law is consistent with Coulomb's law. Consider a point charge \(q\) at the origin. Consider a Then, the right hand side of Gauss's law is \(q/\epsilon_0\).



<figure class="center"><p><img src="figures/point_charge_gauss.pdf" alt="Function" class="center" style="width:113.784px;height:113.784px;"> </p></figure>



</div>

<div class="example">
<b>Example:</b>
Consider the problem of finding the electric field due to a point charge without using Coulomb's law, but rather Gauss's law. Argue that the electric field must be exactly the one found by using Coulomb's law.

\noindent<b>Solution:</b> 



N

Now, this may seem like a very convoluted way to compute the electric field. The purpose of this problem is merely to demonstrate how to use Gauss's law, and the symmetry arguments that go along with it. The true power of Gauss's law will be demonstrated in the examples in the next section. 

</div>






<div class="example">
<b>Example:</b>
Compute the electric field due to a uniformly charged spherical shell of radius \(a\). 

<b>Solution:</b> First, we start with the example of the electric field due to a uniformly charged spherical shell. We get 

$$\begin{equation}
\mathbf{E} = \frac{1}{4\pi\epsilon_0}\int\frac{\sigma(\r-<b>a</b>)\d A}{|\r-<b>a</b>|^3}
\end{equation}$$

For simplicity, take \(\mathbf{E}\) on the \(z\)-axis. Then, by symmetry, we only need to calculate \(E_z = \mathbf{E}\cdot\hat{z}\), and now \(|\r-<b>a</b>| = (a^2+z^2-2az\cos\theta)^{1/2}\). Note that \(<b>a</b>\) is the integration variable here. This gives us the formula for the electric field at this particular point

$$\begin{equation}
E_z = \frac{1}{4\pi\epsilon_0}\int\frac{\sigma \d A(\r-<b>a</b>)\cdot\hat{z}}{(a^2+z^2-2az\cos\theta)^{3/2}}
\end{equation}$$

Since \(\d A = a^2\sin\theta\d\theta\d\phi = -a^2\d(\cos\theta)\d\phi\) and \((\r-<b>a</b>)\cdot\hat{a} = (z-a\cos\theta)\), we find that 

$$\begin{align}
 E_z ={}& -\frac{1}{4\pi\epsilon_0}\int\frac{\sigma a^2 \d(\cos\theta) \d\phi (z - a\cos\theta)}{(a^2+z^2-2az\cos\theta)^{3/2}} \\
={}& -\frac{2\pi\sigma a^2}{4\pi\epsilon_0}\int\frac{\d(\cos\theta)(z-a\cos\theta)}{(a^2+z^2-2az\cos\theta)^{3/2}} \\
={}& \frac{\sigma a^2}{2\epsilon_0}\int_{-1}^1 \frac{(z-au) \d u}{(a^2+z^2-2azu)^{3/2}} \\
={}& \frac{\sigma a^2}{2\epsilon_0}\left(\frac{1}{z^2}\frac{zu-a}{\sqrt{a^2+z^2-2azu}}\right)\bigg|_{-1}^1 \\
={}& \frac{\sigma a^2}{2z^2\epsilon_0}\left(\frac{z-a}{|z-a|} - \frac{-z-a}{|z+a|}\right)
\end{align}$$

which tells us that

$$\begin{equation}
E_z = \begin{cases}
\frac{q}{4\pi\epsilon_0}\frac{q}{z^2} & z > a \\
0 & z < a
\end{cases}
\end{equation}$$

</div>


<div class="example">
<b>Example:</b>
Calculate the field everywhere due to a uniformly charged sphere. In particular, obtain the field inside the sphere and outside. 

Solution: In general, for an arbitrary charge distribution, we have 

\(\)\mathbf{E}(\r) = \frac{1}{4\pi\epsilon_0}\int \frac{\rho(\r')(\r-\r')}{|\r-\r'|^3}\d V'\(\)

so outside the sphere, all charge is enclosed and 

\(\)\mathbf{E} = \frac{Q}{4\pi\epsilon_0 r^2}\hat{r}\(\)

whereas inside the sphere, we find all the charge up to radius \(r\)....

DO THE EXAMPLE WITH A TRIPLE INTEGRAL!!

</div>

Gauss's law:

The goal of Gauss's law is to relate the flux of \\(E\\) across a closed surface to the total charge enclosed. We consider a charge \\(Q\\) inside a closed surface \\(A\\) and the flux of \\(E\\) across \\(\d A\\). The flux is defined by 

$$\d\Phi = \mathbf{E} \cdot \d<b>A</b> = \frac{Q}{4\pi\epsilon_0}\frac{\hat{r}}{r^2}\d<b>A</b>$$

The dot product is evaluated simply as 

$$\begin{align}
\hat{r}\cdot\d<b>A</b> ={}& \hat{r}\cdot\hat{r}\d A_r \\
={}& r^2\sin\theta\d\theta\d\phi \\
={}& -r^2 \d(\cos\theta) \d\phi
\end{align}$$

Thus, we calculate 

$$\oint_A\mathbf{E}\cdot\d<b>A</b> = -\frac{Q}{4\pi\epsilon_0}\int_1^{-1}\d(\cos\theta)\int_0^{2\pi}\d\phi = \frac{Q}{\epsilon_0}.$$

Therefore we have Gauss's law in integral form:

$$\int_A \mathbf{E}\cdot\d<b>A</b> = 
\begin{cases}
\frac{Q}{\epsilon_0} & Q \in <b>A</b> \\
0 & Q \not\in<b>A</b>
\end{cases}.$$

If there is a volume charge density \\(\rho\\) but no surface charge, then

$$\int_A \mathbf{E}\cdot\d<b>A</b> = \frac{Q}{\epsilon_0} = \frac{1}{\epsilon_0}\int_V \rho \d V$$

Since this holds for any volume \\(V\\), we can use the divergence theorem to rewrite this as 

$$\int_V \nabla\cdot \mathbf{E}\cdot\d<b>A</b> = \frac{1}{\epsilon_0}\int_V \rho \d V$$

so that \\(\nabla\cdot\mathbf{E} = \frac{\rho}{\epsilon\_0}\\). 

<div class="faq">
<b>FAQ:</b>
<ul>
<li> Q: What is meant by a ``closed surface"? A: by a closed surface, we mean a surface which you must punch through in order to get from one side to another.
</li></ul>

</div>


