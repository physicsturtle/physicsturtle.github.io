---
layout: lesson
title: Using Gauss's Law 
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---
In this section, we will solve some simple physical problems by using Gauss's law. 

There are 3 prototypical examples of systems to which we can apply Gauss's law. We will go through each of them in detail. 


Let's now provide another derivation of Gauss's law in differential form. 

$$\mathbf{E} = \frac{1}{4\pi\epsilon_0}\int\frac{\hat{R}}{R^2}\rho(\r')\d V'$$

with \\(<b>R</b> = \r - \r'\\). Thus 

$$\nabla\cdot\mathbf{E} = \frac{1}{4\pi\epsilon_0}\int\nabla\cdot\frac{\hat{R}}{R^2}\rho(\r')\d V'$$

but 

$$\nabla\cdot\frac{\hat{R}}{R^2} = 4\pi\delta(\r-\r')$$

which tells us that 

$$\nabla\cdot\mathbf{E} = \frac{1}{4\pi\epsilon_0}\int\nabla\cdot 4\pi\delta(\r-\r') \rho(\r')\d V' = \frac{1}{\epsilon_0}\rho(\r)$$


Gauss's law becomes useful when the magnitude of the electric field on a particular Gaussian surface is constant, and is always parallel or perpendicular to the normal vector of the surface. 

<div class="example">
<b>Example:</b>
Consider a uniformly charged sphere of radius \(a\). Find the electric field inside and outside the sphere. 

By symmetry, \(\mathbf{E}\) is radially outward. Thus \(\mathbf{E} = E(r)\hat{r}\). We consider a Gaussian surface of radius \(r\). We get 

\(\)\oint\mathbf{E}\cdot\d<b>A</b> = E4\pi r^2\(\)

and inside the sphere we have that 

\(\)Q_\text{enc} = \frac{\rho r}{3\epsilon_0}\(\)

whereas the enclosed charge if you're outside of the sphere is just \(Q\). Thus

LIST ELECTRIC FIELD HERE


</div>


<div class="example">
<b>Example:</b>
Consider an infinite plane uniformly charged. Find the electric field everywhere. 

We pick a Gaussian pillbox, and get

\(\)\mathbf{E} = \frac{\sigma}{2\epsilon_0}\hat{n}.\(\)

</div>

<div class="example">
<b>Example:</b>
Consider an infinitely long charged wire, with uniform linear charge density \(\lambda\). Compute the electric field everywhere using Gauss's law.

\noindent<b>Solution:</b>


</div>

