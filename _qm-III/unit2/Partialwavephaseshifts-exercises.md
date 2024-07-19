---
layout: exercises
title: Partial wave phase shifts  - Exercises
dept: physics
course: qm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics III
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise">  Let us now consider the soft sphere potential

$$\begin{equation}
V(r) = \begin{cases} V_0 & r < a \\ 0 & r \geq a \end{cases}
\end{equation}$$

<ol type="a">
<li>  Consider the case \(E > V_0\) 
<ol type="i">
<li> Solve the Schrödinger equation in the scattering region for the two cases 
</li>
<li> Compute the partial wave phase shifts for each \(\ell\) in terms of Bessel functions
</li>
<li> Explicitly calculate the phase shift \(\delta_0\) for \(\ell = 0\)
</li>
<li> In the low-energy limit \(ka\ll 1\), compute the scattering cross section. Do this by taking only the \(\ell=0\) term. 
</li></ol>
</li>
<li> \(E < V_0\)
<ol type="i">
<li> Solve the Schrödinger equation in the scattering region for the two cases 
</li>
<li> Compute the partial wave phase shifts for each \(\ell\) in terms of Bessel functions
</li>
<li> Explicitly calculate the phase shift \(\delta_0\) for \(\ell = 0\)
</li>
<li> In the low-energy limit \(ka\ll 1\), compute the scattering cross section. Do this by taking only the \(\ell=0\) term. 
</li></ol>

</li>
<li> Compare the results from the two cases. 
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer26')" class="answerButton">Show Answer</button> 
 <div  id='answer26' class="answer" >
<ol type="a">

<li> 
<ol type="i">
<li> We need to solve the Schrödinger equation in the interior region. Unlike in the previous case, where the scattering region had oscillating states, we only have exponentially growing or decaying states in the interior region. The Schrödinger equation is given by 

\(\)-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + V_\text{eff}(r)R = ER\(\)

where 

\(\)V_\text{eff} = V(r) + \frac{\hbar^2\ell(\ell+1)}{2mr^2}\(\)

In the region \(r > a\), we have the typical wave function

\(\)\psi_\text{out} = A\sum_{\ell=0}^\infty i^\ell \frac{2\ell+1}{2}(h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr))P_\ell(\cos\theta)\(\)

whereas in the region \(r < a\), we will have an oscillatory solution because the energy is greater than the potential. In particular, the solution will have the form

\(\)\psi_\text{in} = B\sum_{\ell=0}^\infty i^\ell (2\ell+1)c_\ell j_\ell(k_0 r) P_\ell(\cos\theta)\(\)

Here, \(k_0 = \sqrt{2m(E-V_0)}/\hbar\). Since \(E > V_0\), this is an oscillatory solution. Thus, in the inner region the solution is 

$$\begin{equation}
\psi_\text{in} = B\sum_{\ell=0}^\infty  i^\ell (2\ell+1) c_\ell j_\ell(k_0 r) P_\ell(\cos\theta)
\end{equation}$$

</li>
<li> To compute the partial wave shifts, we need to stitch together the two solutions. We use continuity and continuity of the derivative, as before: 

$$\begin{equation}
e^{2i\delta_\ell} = -\frac{k_0 j'_\ell(k_0a) h^{(2)}_\ell(ka) - kj_\ell(k_0a) h^{(2)\prime}_\ell(ka)}{k_0 j'_\ell(k_0a)h^{(1)}_\ell(ka) - kj_\ell(k_0a)h^{(1)\prime}_\ell(ka) }
\end{equation}$$

</li>
<li> 

</li></ol>

</li>
<li> 

<ol type="i">
<li> In the intermediate region \(r > a\), the typical wave function is given by 

\(\)\psi_\text{out} = A\sum_{\ell=0}^\infty i^\ell \frac{2\ell+1}{2}(h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr))P_\ell(\cos\theta)\(\)

whereas in the region \(r < a\), we will have an exponentially decaying solution. For this, let us look at the radial Schrödinger equation, which has the form 

\(\)-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left( r^2\frac{\partial R}{\partial r}\right)  + \left(\frac{\hbar^2\ell(\ell+1)}{2mr^2} + \frac{\hbar^2\kappa_0^2}{2m}\right)R = 0\(\)

whose solutions are the <i>modified Bessel functions</i> \(i_\ell(\kappa_0 r)\) and \(k_\ell(\kappa_0 r)\), rather than the typical ones. These two solutions are exponentially decaying and exponentially growing at large arugment. This doesn't really matter however, and what actually matters is the behaviour as \(r\to 0\). This tells us that we need \(i^{(1)}_\ell(\kappa r)\). Therefore, the wave function is 

\(\)\psi_\text{in} = B\sum_{\ell=0}^\infty i^\ell (2\ell+1) c_\ell i^{(1)}_\ell(\kappa r) P_\ell(\cos\theta)\(\)

Here, \(\kappa_0 = \sqrt{2m(V_0-E)}/\hbar\). 

</li>
<li> Now, we need to stitch together the two solutions. This gives us that the continuity condition is 

\(\)\frac{A}{2}(h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr)) = Bc_\ell i^{(1)}_\ell(\kappa_0 a)\(\)

and the continuity of the derivative is 

\(\)\frac{Ak}{2}(h^{(1)\prime}_\ell(kr) e^{2i\delta_\ell} + h^{(2)\prime}_\ell(kr)) = B\kappa c_\ell i^{(1)\prime}_\ell(\kappa_0 a)\(\)

Dividing the two equations, we find that 

\(\)k\frac{h^{(1)\prime}_\ell(kr) e^{2i\delta_\ell} + h^{(2)\prime}_\ell(kr)}{h^{(1)}_\ell(kr) e^{2i\delta_\ell} + h^{(2)}_\ell(kr)} = \frac{\kappa_0 i^{(1)\prime}_\ell(\kappa_0 a)}{i^{(1)}_\ell(\kappa_0 a)}\(\)

Thus, we can solve for \(e^{2i\delta_\ell}\) to get

\(\)e^{2i\delta_\ell} = -\frac{\kappa_0 i^{(1)\prime}_\ell(\kappa_0 a) h^{(2)}_\ell(ka) - k i^{(1)}_\ell(\kappa_0 a) h^{(2)\prime}_\ell(ka)}{\kappa_0 h^{(1)}_\ell(ka) i^{(1)\prime}_\ell(\kappa_0 a) - k h^{(1)\prime}_\ell(ka) i^{(1)}_\ell(\kappa_0 a)}\(\)

Then, the phase shifts can be found by noting that the numerator and denominator are complex conjugates are one another. Thus, we can write 

\(\)e^{2i\delta_\ell} = e^{i\pi} e^{-2i\varphi}\(\)

where 

\(\)\varphi = \Arg(\kappa_0 h^{(1)}_\ell(ka) i^{(1)\prime}_\ell(\kappa_0 a) - k h^{(1)\prime}_\ell(ka) i^{(1)}_\ell(\kappa_0 a))\(\)

Thus, 

\(\)2\delta_\ell = \pi - 2\varphi\(\)

Thus, we find 

\(\)\delta_\ell = \frac{\pi}{2} -  \Arg(\kappa_0 h^{(1)}_\ell(ka) i^{(1)\prime}_\ell(\kappa_0 a) - k h^{(1)\prime}_\ell(ka) i^{(1)}_\ell(\kappa_0 a))\(\)


</li>
<li> Now, we substitute in \(\ell=0\). This gives us 

$$\begin{align}
\delta_0 ={}& \frac{\pi}{2} - \Arg(\kappa_0 h^{(1)}_0(ka) i^{(1)\prime}_0(\kappa_0 a) - k h^{(1)\prime}_0(ka) i^{(1)}_0(\kappa_0 a)) 
\end{align}$$

Then, using the fact that 

\(\)j_0(z) = \frac{\sin z}{z}, \quad h^{(1)}_0(z) = -i\frac{e^{iz}}{z}\(\)

we can use \(i^{(1)}_\ell(z) = i^{-\ell}j_\ell(iz)\) we get that \(i^{(1)}_0(z) = \sinh z/z\). Thus, we get that 

$$\begin{align}
\delta_0 ={}& \frac{\pi}{2} - \Arg\left[\kappa_0\left(-i\frac{e^{ika}}{ka}\right)\left(-\frac{\sinh(\kappa_0 a)}{(\kappa_0 a)^2} + \frac{\cosh(\kappa_0 a)}{\kappa_0 a}\right) - k\left(\frac{e^{ika}}{ka} + i\frac{e^{ika}}{(ka)^2}\right)\left(\frac{\sinh(\kappa_0 a)}{\kappa_0 a}\right)\right] \\
={}& \frac{\pi}{2} - \Arg\left[-i\kappa_0e^{ika}\left(-\frac{\sinh(\kappa_0 a)}{\kappa_0 a} + \cosh(\kappa_0 a)\right) - k\left(e^{ika} + i\frac{e^{ika}}{ka}\right)\sinh(\kappa_0 a)\right] \\
={}& \frac{\pi}{2} - \Arg\left[ ie^{ika}\frac{\sinh(\kappa_0 a)}{a} - i\kappa_0 e^{ika}\cosh(\kappa_0 a) - ke^{ika}\sinh(\kappa_0 a) - ik\frac{e^{ika}}{a}\sinh(\kappa_0 a)\right] \\
={}& \frac{\pi}{2} - \Arg\left[- i\kappa_0 e^{ika}\cosh(\kappa_0 a) - ke^{ika}\sinh(\kappa_0 a)\right] \\
={}& \frac{\pi}{2} - \Arg\left[-i\kappa_0\cosh(\kappa_0 a) - k\sinh(\kappa_0 a)\right] - ka \\
={}& \frac{\pi}{2} - \left[\arctan\left(\frac{\kappa_0\cosh(\kappa_0 a)}{k\sinh(\kappa_0 a)}\right) - \pi \right] - ka \\
={}& -\pi + \frac{\pi}{2} - \arctan\left(\frac{\kappa_0\cosh(\kappa_0 a)}{k\sinh(\kappa_0 a)}\right)  - ka \\
={}& -\pi + \arctan\left(\frac{k\tanh(\kappa_0 a)}{\kappa_0}\right)  - ka \\
\end{align}$$
 
We throw out the \(\pi\) because it doesn't matter for the final results since we have \(e^{2i\delta_0}\) and \(e^{2\pi i} = 1\). 

$$\begin{align}
\delta_0 ={}& \arctan\left(\frac{k \tanh(\kappa_0 a)}{\kappa_0}\right) - ka
\end{align}$$

</li>
<li> In the limit \(ka\ll 1\), we have 

$$\begin{align}
\delta_0 ={}& \arctan\left(\frac{ka \tanh(\kappa_0 a)}{\kappa_0a}\right) - ka \\
={}& \frac{ka \tanh(\kappa_0 a)}{\kappa_0a} - ka \\
={}& ka \left(\frac{\tanh(\kappa_0 a)}{\kappa_0a} - 1\right) \\
\end{align}$$

Thus the cross section is 

$$\begin{align}
\sigma ={}& \frac{4\pi}{k^2}\sin^2\left[ka \left(\frac{\tanh(\kappa_0 a)}{\kappa_0a} - 1\right) \right] \\
={}& 4\pi a^2\left(\frac{\tanh(\kappa_0 a)}{\kappa_0a} - 1\right)^2 \\
\end{align}$$


</li></ol>

</li>
<li> 
</li></ol>
</div> 
 </div>

</div> </li></ol>


