---
layout: exercises
title: Cooper instability  - Exercises
dept: physics
course: superconductivity
unit: unit4
deptDisplay: Physics
courseDisplay: Superconductivity & Superfluidity
unitDisplay: Unit 4
---
<ol>
<li> <div class="exercise">  Consider the two-particle Hamiltonian:

$$\begin{equation}
\Hhat = -\frac{\hbar^2}{2m_e}\nabla_{\r_1}^2 - \frac{\hbar^2}{2m_e}\nabla_{\r_2}^2 - \left[2\mathbf{S}_1 \cdot \mathbf{S}_2 + \frac{1}{2}\right] V(\r_1 - \r_2).
\end{equation}$$

<ol type="a">
<li> Show that 

$$\begin{equation}
(2\epsilon_{\k} - \tilde{E})\phi_{\ell m}(k) = -\frac{(-1)^\ell}{(2\pi)^3}\int V_\ell(k,k') \phi_{\ell m}(k') 4\pi k^{\prime 2} \d k'
\end{equation}$$

where \(V_\ell(k,k')\) is defined as it was in the previous section. Remember what the total spin should be for an even parity (singlet) vs. odd parity (triplet) wave function. What condition on \(V_\ell(k_F,k_F)\) is required such that a bound state exists? (a bound state will have energy \(\tilde{E} < 2\epsilon_F\) because the energy must be lower than the kinetic energy of the 2 electrons comprising the pair)

</li>
<li> Next, show that, for a nontrivial solution for \(\phi_{\ell m}\) to exist, we require

$$\begin{equation}
1 = -(-1)^\ell\int \frac{V_\ell(k,k')}{2\epsilon_{\k'} - \tilde{E}} \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3}
\end{equation}$$

Recall that \(\phi_{\ell m}(k) = 0\) for \(k < k_F\), due to the Fermi surface.

</li>
<li> Defining \(\Delta = 2\epsilon_F - \tilde{E}\), and assuming a high-energy cutoff \(D\), show that there is a bound state with binding energy 

$$\begin{equation}
\Delta \approx 2D e^{-2/\lambda_\ell \rho}
\end{equation}$$

where \(\rho\) is the density of states at the Fermi energy, and \(\lambda_\ell = -(-1)^\ell V_\ell(k,k')\) is the approximate value of the potential in the \(\ell\) angular momentum channel on the Fermi surface (\(k,k'=k_F\)). 

</li>
<li> Suppose the potential is given by \(V(r) = \alpha\frac{j_1(2k_Fr)}{k_Fr^2}\), where \(\alpha\) is a positive constant, and \(j_1(x)\) is the spherical Bessel function of order 1:

$$\begin{equation}
j_1(x) = \frac{\sin x}{x^2} - \frac{\cos x}{x}
\end{equation}$$

If this potential seems very weird (e.g. how can we have an oscillating potential?), please recall that an oscillating potential is possible due to electron-electron overscreening (this was called Friedel oscillations). For \(\ell=0,1,2,3\) plot \((-1)^\ell V_\ell(k,k')\) for \(0 < k,k' < 2k_F\). You should write a short program to do this (these integrals are possible to calculate analytically, but this is a waste of your time). For \(k,k'\) on the Fermi surface, what can you say about the sign of \((-1)^\ell V_\ell(k,k')\) as a function of \(\ell\)? Which value of \(\ell\) gives the leading attractive interaction? Does this yield a spin-singlet or spin-triplet solution?
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer41')" class="answerButton">Show Answer</button> 
 <div  id='answer41' class="answer" >
<ol type="a">
<li> 
</li>
<li> 
</li></ol>
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Show that we still need a threshold if we have no Fermi surface

<div class="answerBox"> 
 <button onclick="myFunction('answer50')" class="answerButton">Show Answer</button> 
 <div  id='answer50' class="answer" >
<ol type="a">
<li> If we instead had a lower bound of 0 instead of \(\epsilon_F\), then if \(\rho(\epsilon) = c\sqrt{\epsilon}\), the integral would be

$$\begin{align}
1 ={}& N_sV_\ell c \int_{\epsilon_L}^{\epsilon_F + D} \frac{\sqrt{\epsilon}}{2\epsilon - \tilde{E}} \d\epsilon \\
={}& N_s V_\ell c \left(\sqrt{\epsilon} + \frac{\sqrt{\tilde{E}}}{2\sqrt{2}}\log\left|\frac{\sqrt{2\epsilon} - \sqrt{\tilde{E}}}{\sqrt{2\epsilon} + \sqrt{\tilde{E}}}\right| \right)\bigg|_{\epsilon_L}^{\epsilon_F+D} \\
={}& N_s V_\ell c \left(\sqrt{\epsilon_F+D} + \frac{\sqrt{\tilde{E}}}{2\sqrt{2}}\log\left|\frac{\sqrt{2\epsilon_F+2D} - \sqrt{\tilde{E}}}{\sqrt{2\epsilon_F+2D} + \sqrt{\tilde{E}}}\right|  - \sqrt{\epsilon_L} - \frac{\sqrt{\tilde{E}}}{2\sqrt{2}}\log\left|\frac{\sqrt{2\epsilon_L} - \sqrt{\tilde{E}}}{\sqrt{2\epsilon_L} + \sqrt{\tilde{E}}}\right|\right)
\end{align}$$

If we look now for a solution \(\tilde{E} < 2\epsilon_F\), one can see by plotting software (define \(z = \tilde{E}/2\epsilon_F\) and \(a = \sqrt{1 + D/\epsilon_F} > 1\)) that we need to solve the equation

$$\begin{align}
1 ={}& N_s V_\ell c \sqrt{\epsilon_F}\left(a + \frac{\sqrt{z}}{2}\log\left|\frac{a - \sqrt{z}}{a + \sqrt{z}}\right| \right)
\end{align}$$

If we look for a solution for \(z < 1\), (which is equivalent to saying \(\tilde{E} < 2\epsilon_F\))
</li></ol>
</div> 
 </div>

 
  
 
 
 
 
     
 

 

</div> </li></ol>



