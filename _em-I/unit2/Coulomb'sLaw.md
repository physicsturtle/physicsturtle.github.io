---
layout: lesson
title: Coulomb's Law 
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---
Electrostatics is the study of electric charges at rest (hence ``statics"). At the centre of this is <i>Coulomb's law</i>. Coulomb's law is the statement that the force of \\(q_a\\) on \\(q_b\\) is given by 

$$\begin{equation}
\mathbf{F}_{ab} = \frac{q_aq_b}{4\pi\epsilon_0 r^2}\hat{r}_{ab},
\end{equation}$$

where \\(\hat{r}_{ab}\\) is the unit vector which points from \\(q_a\\) to \\(q_b\\). The constant \\(\epsilon_0 = 8.85\times 10^{-12}\text{C}^2/\text{N}\text{m}^2\\) is called the <i>permittivity of free space</i>. Coulomb's law is known to very high precision. It goes as \\(1/r^n\\), where \\(n\\) has been measured experimentally to be very close to 2, in fact \\( \|n-2\| < 10^{-16}\\). 

<figure class="center">
<p><img src="figures/coulomb_law.pdf" alt="Function" class="center" style="width:192.252px;height:33.886px;"> </p><figcaption class="center">Schematic of Coulomb's law for the case where \(q_a\) and \(q_b\) are like charges. Because the two charges are like, they repel one another.</figcaption>
</figure>


Surrounding a point charge is the <i>electric field</i>, and the electric field due to an isolated charge \\(Q\\) is given by 

$$\begin{equation}
\mathbf{E} = \frac{Q}{4\pi\epsilon_0 r^2}\hat{r}.
\end{equation}$$

<figure class="center">
<p><img src="figures/electric_field_schematic.pdf" alt="Function" class="center" style="width:411.422px;height:184.65px;"> </p><figcaption class="center">Schematic of the electric field surrounding a point charge \(Q\). Note that the field lines are not drawn to scale. In reality, they should decay much faster and therefore the ones far from the charge should be much shorter. Left: This is for the case \(Q > 0\), where the field lines point away from the charge. Right: This is for the case \(Q < 0\), where the field lines point toward the charge.</figcaption>
</figure>

Regardless of what produces the electric field, we can find the force due to this electric field \\(\mathbf{E}\\) on some charge \\(q\\) placed in it. The force on a test charge \\(q\\) is given by \\(\mathbf{F} = q\mathbf{E}\\). Before moving on to some examples, let's note that, in these notes, we will be using SI units. Important values in these units are 

<ul>
<li> The mass of the electron \(m_e = 9.1\times 10^{-31}\text{kg}\)
</li>
<li> The mass of the proton: \(m_p = 1826m_e\)
</li>
<li> The charge of the proton: \(e = 1.6\times10^{-19}\text{C}\). This is also called the <i>elementary charge</i>. 
</li>
<li> The speed of light: \(c = 2.9979\times10^8\text{m}/\text{s}\). 
</li></ul>

A further important fact, which may seem trivial, is the law of superposition of electric fields. This states that, the electric field due to multiple charges is the sum of the electric fields of each individual charge. To see this, we can use the fact that <i>forces can be added together</i>. Suppose we have \\(n\\) point charges \\(q_1,q_2,\dots,q_n\\). The force on a charge \\(q\\) is given by

$$\begin{equation}
\mathbf{F} = \sum_{i=1}^n \frac{qq_i}{4\pi\epsilon_0 r_i^2}\hat{r}_i
\end{equation}$$

Factoring out \\(q\\), we use the relation between force on a charge \\(q\\) and the electric field it sites in: \\(\mathbf{F} = q\mathbf{E}\\). This allows us to conclude that

$$\begin{equation}
\mathbf{E} =  \sum_{i=1}^n \frac{q_i}{4\pi\epsilon_0 r_i^2}\hat{r}_i.
\end{equation}$$

So we have derived superposition of electric fields from superposition of forces.

<div class="example">
<b>Example:</b>
Let us use the fact of superposition of electric fields to do the following problem. Suppose we have two point charges \(Q_1\) and \(Q_2\) at \(x = - a\) and \(x = a\), respectively. Calculate the electric field at \((x,y)\) in space.

<figure class="center"><p><img src="figures/two_charge_example.pdf" alt="Function" class="center" style="width:176.445px;height:109.129px;"> </p></figure>


<b>Solution:</b> The magnitude of the electric field due to charge 1 is given by 

$$\begin{equation}
E_1 = \frac{Q_1}{4\pi\epsilon_0 r_1^2} = \frac{Q_1}{4\pi\epsilon_0[(a+x)^2 + y^2]}
\end{equation}$$

and, now putting in the unit vector which points from \((-a,0)\) to \((x,a)\)

$$\begin{equation}
\mathbf{E}_1 = E_1(\cos\theta_1\xhat + \sin\theta_1\yhat) = E_1\left(\frac{a+x}{r_1}\xhat + \frac{y}{r_1}\yhat\right)
\end{equation}$$

where \(r_1 = \sqrt{(x+a)^2 + y^2}\), and similarly, 

$$\begin{equation}
E_2 = \frac{Q_2}{4\pi\epsilon_0 r_2^2} = \frac{Q_2}{4\pi\epsilon_0[(x-a)^2 + y^2]}
\end{equation}$$

and, adding the unit vector of the direction, we get

$$\begin{equation}
\mathbf{E}_2 = E_2(\cos\theta_2\xhat + \sin\theta_2\yhat) = E_2\left(\frac{x-a}{r_2}\xhat + \frac{y}{r_2}\yhat\right)
\end{equation}$$

where \(r_2 = \sqrt{(x-a)^2 + y^2}\). By the principle of superposition, \(\mathbf{E} = \mathbf{E}_1 + \mathbf{E}_2\), and the final answer is, for the special case \(Q_1 = Q_2\) (also write for \(Q_1\neq Q_2\))

$$\begin{equation}
\mathbf{E} = \frac{Q}{4\pi\epsilon_0}\left\{\left[\frac{x+a}{[(x+a)^2 + y^2]^{3/2}} + \frac{x-a}{[(x-a)^2+y^2]^{3/2}}\right]\hat{x} + \left[\frac{y}{[(x+a)^2+y^2]^{3/2}} + \frac{y}{[(x-a)^2+y^2]^{3/2}}\right]\hat{y}\right\}
\end{equation}$$


</div>

What we have said about the superposition of electric fields due to a number of charges also applies for continuous charge distributions. For a continuous distribution, 

$$\begin{equation}
\mathbf{E} = \int_{V'}\frac{\rho(\x')(\x-\x')}{\|\x-\x'\|^3}\d^3\x'
\end{equation}$$

where \\(\rho\\) is the volume charge density and \\(V'\\) is the volume where the charge resides. There are analogous expressions for surface and line charge densities:

$$\begin{align}
\mathbf{E} ={}& \frac{1}{4\pi\epsilon_0}\int_{A'} \frac{\sigma(\x')(\x-\x')}{\|\x-\x'\|^3} \d^2\x' \\
\mathbf{E} ={}& \frac{1}{4\pi\epsilon_0}\int_{L'} \frac{\lambda(\x')(\x-\x')}{\|\x-\x'\|^3}\d\ell'.
\end{align}$$

These expressions have been written somewhat compactly. For clarity, if we expand out e.g. the volume formula, we get 

$$\begin{equation}
\mathbf{E}(\x) = \frac{1}{4\pi\epsilon_0}\int\frac{(x-',y-y',z-z')\rho(\x')}{[(x-x')^2+(y-y')^2+(z-z')^2]^{3/2}}\d x' \d y' \d z'.
\end{equation}$$

<div class="example">
<b>Example:</b>
Consider an infinite line of charge, with linear charge density \(\lambda\). Compute the electric field at all points in space. 

</div>


