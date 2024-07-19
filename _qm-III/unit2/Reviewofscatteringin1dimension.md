---
layout: lesson
title: Review of scattering in 1 dimension 
dept: physics
course: qm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics III
unitDisplay: Unit 2
---
Let us consider the following scattering problem in 1 dimension, with potential

$$\begin{equation}
V(x) = \begin{cases} \pm V_0 & 0 < x < a \\ 0 & \text{else} \end{cases}
\end{equation}$$

where \\(V\_0 > 0\\). The Schrödinger equation to solve is 

$$\begin{equation}
\left[-\frac{\hbar^2}{2m}\frac{\d^2}{\d x^2} + V(x)\right]\psi = E\psi
\end{equation}$$

If \\(V\_0 > 0\\), this is a potential barrier, and if \\(V\_0 < 0\\), this is a potential well. For the case \\(V\_0 > 0\\), there are no bound states at all, and if \\(V\_0 < 0\\), there are bound states with negative energy, and scattering states with positive energy. We will solve both of these and contrast the solutions. 

  

### Potential well

Let us now turn to studying the potential well. The potential well is depicted below. The Schrödinger equation is given by

$$\begin{equation}
\begin{cases}
-\frac{\hbar^2}{2m}\psi" - V_0\psi = E\psi, & |x| < a \\
-\frac{\hbar^2}{2m}\psi" = E\psi, & |x| > a
\end{cases}
\end{equation}$$

<figure class="center">
<p><img src="figures/potential_well_1D.pdf" alt="Function" class="center" style="width:186.408px;height:129.982px;"> </p><figcaption class="center">Potential well with depth \(V_0\).</figcaption>
</figure>


To solve the problem, we solve the Schrödinger equation in each domain. If we are interested in scattering states, we only consider scattering states with \\(E > 0\\). Since \\(E > 0\\) means that the particle's energy is greater than the potential in each domain, they are sinusoidal in each region. The wave function can be defined in three different domains,

$$\begin{equation}
\psi(x) = \begin{cases} Ae^{ik_0x} + Be^{-ik_0x}, & x < -a \\ 
Ce^{ikx} + De^{-ikx}, & -a < x < a \\ 
Fe^{ik_0x}, & a < x 
\end{cases}
\end{equation}$$

Here, \\(k\_0 = \sqrt{2mE}/\hbar\\), and \\(k = \sqrt{2m(E+V\_0)}/\hbar\\). The relation between the constants is found by applying the boundary conditions. We have 4 equations:

$$\begin{align}
Ae^{-ik_0a} + Be^{ik_0a} ={}& Ce^{-ika} + De^{ika} \\
k_0(Ae^{-ik_0a}-Be^{ik_0a}) ={}& k(Ce^{-ika}-De^{ika}) \\
Ce^{ika} + De^{-ika} ={}& Fe^{ik_0a} \\
k(Ce^{ika} - De^{-ika}) ={}& k_0Fe^{ik_0a}
\end{align}$$

First, we eliminate either \\(C\\) or \\(D\\) from both equations to get 

$$\begin{align}
A(k+k_0)e^{-ik_0a} + B(k-k_0)e^{ik_0a} ={}& 2Cke^{-ika} \\
A(k-k_0)e^{-ik_0a} + B(k+k_0)e^{ik_0a} ={}& 2Dke^{ika} \\
2kCe^{ika}={}& (k+k_0)Fe^{ik_0a} \\
2kDe^{-ika}={}& (k-k_0)Fe^{ik_0a}
\end{align}$$

Then, we can rewrite these as 

$$\begin{align}
A(k+k_0)e^{i(k-k_0)a} + B(k-k_0)e^{i(k_0+k)a} ={}& 2kC \\
A(k-k_0)e^{-i(k_0+k)a} + B(k+k_0)e^{i(k_0-k)a} ={}& 2kD \\
2kC={}& (k_0+k)Fe^{i(k_0-k)a} \\
2kD={}& (k-k_0)Fe^{i(k_0+k)a}
\end{align}$$

and finally eliminate both \\(C\\) and \\(D\\),

$$\begin{align}
A(k+k_0)e^{i(k-k_0)a} + B(k-k_0)e^{i(k_0+k)a} ={}& (k_0+k)Fe^{i(k_0-k)a} \\
A(k-k_0)e^{-i(k_0+k)a} + B(k+k_0)e^{i(k_0-k)a} ={}& (k-k_0)Fe^{i(k_0+k)a}
\end{align}$$

Lastly, we need \\(B/A\\) and \\(F/A\\), which are found by solving 

$$\begin{equation}
\begin{pmatrix} (k_0-k)e^{i(k_0+k)a} & (k_0+k)e^{i(k_0-k)a} \\ -(k_0+k)e^{i(k_0-k)a} & (k-k_0)e^{i(k_0+k)a} \end{pmatrix} \begin{pmatrix} B/A \\ F/A \end{pmatrix} = \begin{pmatrix} (k+k_0)e^{i(k-k_0)a} \\ (k-k_0)e^{-i(k_0+k)a} \end{pmatrix}
\end{equation}$$

Thus, we get 

$$\begin{align}
\frac{B}{A} ={}& \frac{ie^{-2ik_0a}\sin(2ka)(k_0^2-k^2)/(2kk_0)}{\cos(2ka) - \frac{k_0^2+k^2}{2kk_0}i\sin(2ka)} \\
\frac{F}{A} ={}& \frac{-e^{-2ik_0a}}{\cos(2ka) - \frac{k_0^2+k^2}{2kk_0}i\sin(2ka)}
\end{align}$$

The transmission coefficient is 

$$\begin{align}
T^{-1} ={}& \bigg|\frac{A}{F}\bigg|^2 \\
={}& \cos^2(2ka) + \left(\frac{k_0^2+k^2}{2kk_0}\right)^2\sin^2(2ka) \\
={}& 1 + \left[\left(\frac{k_0^2+k^2}{2kk_0}\right)^2 - 1\right]\sin^2(2ka) \\
={}& 1 + \left(\frac{k_0^2-k^2}{2kk_0}\right)^2\sin^2(2ka)
\end{align}$$

Now plugging in the wave vectors

$$\begin{equation}
k_0 = \frac{\sqrt{2mE}}{\hbar}, \qquad k = \frac{\sqrt{2m(E+V_0)}}{\hbar}
\end{equation}$$

we find the transmission coefficient to be

$$\begin{align}
T^{-1} ={}& 1 + \frac{V_0^2}{4E(E+V_0)}\sin^2\left(\frac{2a}{\hbar}\sqrt{2m(E+V_0)}\right)
\end{align}$$

We see that \\(T^{-1}\\) is minimized to 1 (so \\(T\\) is maximized to 1) when the sine is zero, or, when \\(2ka = n\pi\\). When this occurs, the wave in the potential region is commensurate with the size of the well, namely \\(k = n\pi/2a\\) (\\(2a\\) is the width of the well). When the transmission is \\(T=1\\) for this particular wave vector, we call this a <i>resonance</i>. In general, the energy of the particles which pass unimpeded through the potential are 

$$\begin{equation}
E = -V_0 + \frac{\hbar^2}{2m} \left(\frac{n\pi}{2a}\right)^2
\end{equation}$$

Since scattering states have \\(E > 0\\), the first resonance occurs when \\(2a\sqrt{2mV\_0}/\hbar\pi = n\\). 

