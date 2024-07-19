---
layout: exercises
title: Spin Density Wave Order  - Exercises
dept: physics
course: qpt
unit: unit11
deptDisplay: Physics
courseDisplay: Quantum Phase Transitions
unitDisplay: Unit 11
---
<ol>
<li> <div class="exercise">  Compute the fourth order correction to the effective action by calculating \(\tr X^4\). 

<div class="answerBox"> 
 <button onclick="myFunction('answer3')" class="answerButton">Show Answer</button> 
 <div  id='answer3' class="answer" >
Now, the fourth power of \(X\) yields 

$$\begin{align}
\tr X^4 ={}& \frac{1}{(\beta N_s)^4}\sum_{\substack{k_1k_2k_3k_4 \\ q_1q_2q_3q_4}} \sum_{\ell_1\ell_2\ell_4\ell_4} \sum_{\substack{ \alpha_1\alpha_2\alpha_3\alpha_4 \\ \beta_1\beta_2\beta_3\beta_4}} \delta_{k_1q_4}\delta_{\alpha_1\beta_4}[m^{\ell_1}_{k_1-q_1}\sigma^{\ell_1}_{\alpha_1\beta_1}\mathcal{G}_0(k_1)] \delta_{q_1k_2}\delta_{\beta_1\alpha_2} \\
&\times [m^{\ell_2}_{k_2-q_2}\sigma^{\ell_2}_{\alpha_2\beta_2}\mathcal{G}_0(k_2)] \delta_{q_2k_3}\delta_{\beta_2\alpha_3} [m^{\ell_3}_{k_3-q_3}\sigma^{\ell_3}_{\alpha_3\beta_3}\mathcal{G}_0(k_3)] \delta_{q_3k_4}\delta_{\beta_3\alpha_4}[m^{\ell_4}_{k_4-q_4}\sigma^{\ell_4}_{\alpha_4\beta_4}\mathcal{G}_0(k_4)] \\
={}& \frac{1}{(\beta N_s)^4} \sum_{\substack{ k_1k_2k_3k_4 \\ \alpha_1\alpha_2\alpha_3\alpha_4 \\ \ell_1\ell_2\ell_4\ell_4}} m^{\ell_1}_{k_1-k_2}\sigma^{\ell_1}_{\alpha_1\alpha_2}\mathcal{G}_0(k_1)m^{\ell_2}_{k_2-k_3}\sigma^{\ell_2}_{\alpha_2\alpha_3}\mathcal{G}_0(k_2)m^{\ell_3}_{k_3-k_4}\sigma^{\ell_3}_{\alpha_3\alpha_4}\mathcal{G}_0(k_3)m^{\ell_4}_{k_4-k_1}\sigma^{\ell_4}_{\alpha_4\alpha_1}\mathcal{G}_0(k_4) \\
={}& \frac{1}{(\beta N_s)^4} \sum_{\substack{ k_1k_2k_3k_4 \\ \ell_1\ell_2\ell_4\ell_4}} m^{\ell_1}_{k_1-k_2}\mathcal{G}_0(k_1)m^{\ell_2}_{k_2-k_3}\mathcal{G}_0(k_2)m^{\ell_3}_{k_3-k_4}\mathcal{G}_0(k_3)m^{\ell_4}_{k_4-k_1}\mathcal{G}_0(k_4) \tr(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}\sigma^{\ell_4}) \\
\end{align}$$

The first thing we do is sum over the spin indices. We use the identity 

$$\begin{equation}
\sigma^a\sigma^b = \delta_{ab}\sigma^0 + i\epsilon_{abc}\sigma^c.
\end{equation}$$

Then, the trace simplifies down to

$$\begin{align}
\tr(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}\sigma^{\ell_4}) ={}& \tr([\delta_{\ell_1\ell_2}\sigma^0 + i\epsilon_{\ell_1\ell_2a}\sigma^a][\delta_{\ell_3\ell_4}\sigma^0 + i\epsilon_{\ell_3\ell_4b}\sigma^b]) \\
={}& \tr(\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4}\sigma^0 + i\delta_{\ell_1\ell_2}\epsilon_{\ell_3\ell_4 b}\sigma^b + i\delta_{\ell_3\ell_4}\epsilon_{\ell_1\ell_2}\sigma^a - \epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 b}\sigma^a\sigma^b) \\
={}& 2\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - \epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 b}\tr(\sigma^a\sigma^b) \\
={}& 2\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - 2\epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 b}\delta_{ab} \\
={}& 2\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - 2\epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 a}
\end{align}$$

Thus, we can rewrite 

$$\begin{align}
\sum_{\ell_1\ell_2\ell_3\ell_4} m^{\ell_1}_{k_1-k_2} m^{\ell_2}_{k_2-k_3} m^{\ell_3}_{k_3-k_4}m^{\ell_4}_{k_4-k_1}(\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - \epsilon_{\ell_1\ell_2\mu}\epsilon_{\ell_3\ell_4\mu}) ={}& (\mathbf{m}_{k_1-k_2}\cdot\mathbf{m}_{k_2-k_3})(\mathbf{m}_{k_3-k_4}\cdot\mathbf{m}_{k_4-k_1}) \\
&- (\mathbf{m}_{k_1-k_2}\times\mathbf{m}_{k_2-k_3})\cdot(\mathbf{m}_{k_3-k_4}\times\mathbf{m}_{k_4-k_1}) 
\end{align}$$

Thus, we have that \(\tr X^4\) becomes 
$$\begin{align}
\tr X^4 ={}& \frac{2}{(\beta N_s)^4} \sum_{k_1k_2k_3k_4} \mathcal{G}_0(k_1)\mathcal{G}_0(k_2)\mathcal{G}_0(k_3)\mathcal{G}_0(k_4)\left[ (\mathbf{m}_{k_1-k_2}\cdot\mathbf{m}_{k_2-k_3})(\mathbf{m}_{k_3-k_4}\cdot\mathbf{m}_{k_4-k_1}) \right. \\
&- \left.  (\mathbf{m}_{k_1-k_2}\times\mathbf{m}_{k_2-k_3})\cdot(\mathbf{m}_{k_3-k_4}\times\mathbf{m}_{k_4-k_1}) \right]
\end{align}$$

We now relabel the indices on the \(m\) fields. Let \(k_1-k_2 = q_1\), \(k_2-k_3 = q_2\), and \(k_3-k_4 = q_3\). Thus \(k_4-k_1 = -(q_1+q_2+q_3)\). Furthermore, \(k_1 = k_4+q_1+q_2+q_3\), \(k_2 = k_4 + q_2+q_3\), and \(k_3 = k_4+q_3\). We therefore rewrite as 

$$\begin{align}
\tr X^4 ={}& \frac{1}{(\beta N_s)^3} \sum_{q_1q_2q_3} u(q_1,q_2,q_3) \left[(\mathbf{m}_{q_1}\cdot\mathbf{m}_{q_2})(\mathbf{m}_{q_3}\cdot\mathbf{m}_{-q_1-q_2-q_3}) - (\mathbf{m}_{q_1}\times\mathbf{m}_{q_2})\cdot(\mathbf{m}_{q_3}\times\mathbf{m}_{-q_1-q_2-q_3}) \right]
\end{align}$$

where the coupling constant is given by 

$$\begin{align}
u(q_1,q_2,q_3) ={}& \frac{2}{\beta N_s}\sum_{k_4} \mathcal{G}_0(k_4+q_1+q_2+q_3)\mathcal{G}_0(k_4+q_2+q_3)\mathcal{G}_0(k_4+q_3)\mathcal{G}_0(k_4) 
\end{align}$$

We now make two approximations. We approximate \(u(q_1,q_2,q_3) = u = -\frac{v}{12}\rho"(E_F)\) to be a constant, and also remove the second term. The second term goes away if we assume that the coupling is independent of \(q\).
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  In this problem, we consider the third order correction to the action. Recall that  the matrix \(X\) is defined by 

$$\begin{equation}
X_{kq\alpha\beta} = \frac{1}{\beta N_s} \mathbf{m}_{k-q} \cdot \boldsymbol{\sigma} \mathcal{G}_0(k)
\end{equation}$$

FOR THIS, CHECK IF ANY SYMMETRIES OF THE ACTION ARE NOT RESPECTED, E.G. SWAPPING THE SI GN OF M (EQUAL ENERGY FOR DIFF CONFIGS??), OR TIME-REVESRAL

<ol type="a">
<li> Compute \(\tr X^3\), and thereby the third order correction to the action.
</li>
<li> In the case that the coupling constant is approximated to be independent of all momenta and Matsubara frequencies, show that the third order correction is zero.
</li>
<li> Determine the scaling of the cubic term, but considering the cases where \(\lambda\) is proportional to the \(\alpha\)th power of momentum and \(\beta\)th power of Matsubara frequency. 
</li>
<li> Evaluate the Matsubara sum in the coefficient.
</li>
<li> For the free electron gas dispersion relation, compute 

\(\)I = \frac{1}{N_s}\sum_{\k} \frac{1}{i\nu + \xi_{\k} - \xi_{\k+\q}} \frac{1}{i\omega + \xi_{\k} - \xi_{\k+\p}}\(\)
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer75')" class="answerButton">Show Answer</button> 
 <div  id='answer75' class="answer" >
<ol type="a">
<li> The trace yields 

$$\begin{align}
\tr X^3 ={}& \frac{1}{(\beta N_s)^3} \sum_{ \substack{ k_1k_2k_3 \\ q_1 q_2 q_3}} \sum_{\ell_1\ell_2\ell_3} \sum_{\substack{\alpha_1\alpha_2\alpha_3 \\ \beta_1 \beta_2 \beta_3}} \delta_{k_1q_3} \delta_{\alpha_1\beta_3} [m^{\ell_1}_{k_1-q_1}\sigma^{\ell_1}_{\alpha_1\beta_2}\mathcal{G}_0(k_1)] \delta_{q_1k_2}\delta_{\beta_1\alpha_2} \\
&\times [m^{\ell_2}_{k_2-q_2}\sigma^{\ell_2}_{\alpha_2\beta_2}\mathcal{G}_0(k_2)]\delta_{q_2k_3}\delta_{\beta_2\alpha_3}[m^{\ell_3}_{k_3-q_3}\sigma^{\ell_3}_{\alpha_3\beta_3}\mathcal{G}_0(k_3)] \\
={}& \frac{1}{(\beta N_s)^3} \sum_{ k_1k_2k_3 } \sum_{\ell_1\ell_2\ell_3} m^{\ell_1}_{k_1-k_2}\mathcal{G}_0(k_1) m^{\ell_2}_{k_2-k_3}\mathcal{G}_0(k_2) m^{\ell_3}_{k_3-k_1}\mathcal{G}_0(k_3)\tr(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}) 
\end{align}$$

We then use the well-known identity that \(\tr(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}) = 2i\epsilon_{\ell_1\ell_2\ell_3}\). This gives us 

$$\begin{align}
\tr X^3 ={}& \frac{2i}{(\beta N_s)^3} \sum_{ k_1k_2k_3 } \mathbf{m}_{k_1-k_2} \cdot (\mathbf{m}_{k_2-k_3} \times \mathbf{m}_{k_3-k_1})\mathcal{G}_0(k_1) \mathcal{G}_0(k_2) \mathcal{G}_0(k_3)
\end{align}$$

Then, we perform a shift of the momentum labels, by \(k_1-k_2 = q_1\), \(k_2-k_3 = q_2\), and therefore \(k_3-k_1 = -q_1-q_2\). Then, we find that 

$$\begin{align}
\tr X^3 ={}& \frac{2i}{(\beta N_s)^3} \sum_{q_1q_2k_3} \mathbf{m}_{q_1} \cdot (\mathbf{m}_{q_2} \times \mathbf{m}_{-q_1-q_2})\mathcal{G}_0(k_3+q_1+q_2) \mathcal{G}_0(k_3+q_2) \mathcal{G}_0(k_3)
\end{align}$$

This allows us to define a coupling 

\(\)\lambda(q_1,q_2) = \frac{2i}{\beta N_s}\sum_{k_3} \mathcal{G}_0(k_3+q_1+q_2)\mathcal{G}_0(k_3+q_2)\mathcal{G}_0(k_3)\(\)

Then, we find that 

$$\begin{align}
\tr X^3 ={}& \frac{1}{(\beta N_s)^2} \sum_{q_1q_2} \lambda(q_1,q_2) \mathbf{m}_{q_1} \cdot (\mathbf{m}_{q_2} \times \mathbf{m}_{-q_1-q_2}) 
\end{align}$$

This tells us that 

\(\)\Delta S^{(3)}_\text{eff} = \frac{i}{3(\beta N_s)^2}\sum_{q_1q_2}\lambda(q_1,q_2) \mathbf{m}_{q_1} \cdot (\mathbf{m}_{q_2} \times \mathbf{m}_{-q_1-q_2})\(\)

</li>
<li> If we approximate \(\lambda(q_1,q_2) = \lambda\), then we have that the correction to the action is given by 

\(\)\Delta S^{(3)}_\text{eff} = \frac{i\lambda}{3(\beta N_s)^2}\sum_{q_1q_2} \mathbf{m}_{q_1} \cdot (\mathbf{m}_{q_2} \times \mathbf{m}_{-q_1-q_2})\(\)

We can then Fourier transform back to position space, and find that 

\(\)\Delta S^{(3)}_\text{eff} = \frac{i\lambda}{3}\int_0^\beta \sum_{i} \mathbf{m}_{i\tau} \cdot (\mathbf{m}_{i\tau} \times \mathbf{m}_{i\tau}) \d\tau\(\)

This is clearly zero because we have a vector crossed with itself.

</li>
<li> The scaling of the quadratic term is \(k' = bk\) and \(\omega' = b^z\omega\). Then, the fields scale like \(m(k) = vm'(k')\), where \(v = b^{1 + (d+z)/2}\). The scaling of the term becomes \(v^3 b^{-\alpha} b^{-z\beta} b^{-2(d+z)} = b^{3-(d+z)/2 - \alpha - z\beta}\). In the case where \(\alpha=\beta=1\), we have that the scaling is \(b^{2-d/2-3z/2}\). If we have that \(z=3\), as is the case for a ferromagnetic quantum critical point, then the scaling is \(b^{-5/2-d/2}\). Comparing this to the quartic term, we note that the scaling on that term was \(b^{4-d-z} = b^{1-d}\). In this case, any \(d > 1\) leads to an irrelevant quartic interaction, whereas any \(d > 0\) leads to an irrelevant cubic interaction. If we instead have an antiferromagnetic QCP, then \(z=2\). The scaling of the cubic term is then \(b^{-1-d/2}\), and the scaling of the quartic term is \(b^{2-d}\). Then, any \(d > 0\) leads to an irrelevant cubic interaction, and \(d>2\) leads to an irrelevant quartic interaction. Lastly, if \(z=1\), then the cubic term scales as \(b^{1/2-d/2}\), and the quartic term as \(b^{3-d}\). In this case, the cubic interaction is irrelevant for any \(d > 1\), and the quartic interaction is irrelevant for any \(d > 3\). 

</li>
<li> The Matsubara sum for the coefficient is given by (setting \(k_3 = (i\omega,\k)\), \(q_1 = (i\omega_1,\q_1)\), and \(q_2 = (i\omega_2,\q_2)\))

$$\begin{align}
\lambda(q_1,q_2) ={}& \frac{2}{\beta N_s} \sum_{k_3}\mathcal{G}_0(k_3+q_1+q_2)\mathcal{G}_0(k_3+q_2)\mathcal{G}_0(k_3) \\
={}& \frac{2}{\beta N_s}\sum_{\k}\sum_{i\omega} \frac{1}{i\omega + i\omega_1 + i\omega_2 - \xi_{\k+\q_1+\q_2}} \frac{1}{i\omega + i\omega_2 - \xi_{\k+\q_2}} \frac{1}{i\omega - \xi_{\k}} \\
={}& \frac{2}{N_s}\sum_{\k}\left(\frac{1}{\xi_{\k+\q_1+\q_2} - i\omega_1 - \xi_{\k+\q_2}} \frac{1}{\xi_{\k+\q_1+\q_2} - i\omega_1 - i\omega_2 - \xi_{\k}} \right. \\
&+ \frac{1}{\xi_{\k+\q_2} + i\omega_1 - \xi_{\k+\q_1+\q_2}} \frac{1}{\xi_{\k+\q_2} - i\omega_2 - \xi_{\k}} \\
&\left. \frac{1}{i\omega_1 + i\omega_2 + \xi_{\k} - \xi_{\k+\q_1+\q_2}} \frac{1}{i\omega_2 + \xi_{\k} - \xi_{\k+\q_2}}\right)
\end{align}$$

</li>
<li> We then need to perform the integral over \(\k\). We will approximate this by solving it at zero temperature. First, we 

</li></ol>

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the Lindhard function in 3 dimensions.

\(\)\chi_0(k) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega}.\(\)

<div class="answerBox"> 
 <button onclick="myFunction('answer143')" class="answerButton">Show Answer</button> 
 <div  id='answer143' class="answer" >
We approximate the Fermi-Dirac functions as \(n_F(\xi) = \theta(-\xi)\), where \(\xi_{\k} = \epsilon_{\k} - \epsilon_F\), and \(\epsilon_{\k} = \k^2/2m\). In this case, after changing to continuous space, we have 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int \frac{\theta(-\xi_{\q}) - \theta(-\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega} \frac{\d\q}{(2\pi)^3} .\(\)

Now shifting the integration variable of the second term, we can rewrite this as 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int \theta(-\xi_{\q})\left(\frac{1}{\xi_{\q} - \xi_{\k+\q} + i\omega} - \frac{1}{\xi_{\q-\k} - \xi_{\q} + i\omega}\right) \frac{\d\q}{(2\pi)^3} .\(\)

Then, noting that 

\(\)\theta(-\xi_{\q}) = \begin{cases} 1, & |\q| < k_F \\ 0, & |\q| > k_F \end{cases}\(\)

we can integrate the entire occupied region to get 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int_0^{k_F}\int_0^\pi \left(\frac{1}{\xi_{\q} - \xi_{\k+\q} + i\omega} - \frac{1}{\xi_{\q-\k} - \xi_{\q} + i\omega}\right) \frac{q^2\sin\theta \d\theta\d q}{(2\pi)^2} .\(\)

where we have used the fact that the dispersion is spherically symmetric. Next, we will integrate over the angle \(\theta\). First, we need to introduce \(\theta\) through \(\q\cdot\k = qk\cos\theta\), so 

$$\begin{align}
\chi_0(k) ={}& -2\frac{\V}{N_s}\int_0^{k_F}\int_0^\pi \left(\frac{1}{\frac{1}{2m}(-k^2-2kq\cos\theta) + i\omega} - \frac{1}{\frac{1}{2m}(k^2-2kq\cos\theta) + i\omega}\right) \frac{q^2\sin\theta \d\theta\d q}{(2\pi)^2} \\
={}& -2\frac{\V}{N_s}\int_0^{k_F}\int_0^\pi \left(\frac{1}{- \epsilon_{\k}-kq\cos\theta/m + i\omega} - \frac{1}{\epsilon_{\k} - kq\cos\theta/m + i\omega}\right) \frac{q^2\sin\theta \d\theta\d q}{(2\pi)^2}
\end{align}$$

To make notation a big nicer, we rescale \(q = k_Fu\) and get 

$$\begin{align}
\chi_0(k) ={}& -2\frac{\V}{N_s}\int_0^{1}\int_0^\pi \left(\frac{1}{- \epsilon_{\k}-kv_Fu\cos\theta + i\omega} - \frac{1}{\epsilon_{\k} - kuv_F\cos\theta + i\omega}\right) \frac{k_F^3u^2\sin\theta \d\theta\d u}{(2\pi)^2}
\end{align}$$

We use the standard integral 

\(\)\int_0^\pi \frac{\sin\theta}{a - b\cos\theta} \d\theta = -\frac{1}{b}\log\left(\frac{a-b}{a+b}\right)\(\)

and this gives us (where \(v_F = k_F/m\))

\(\)\chi_0(k) = \frac{2\V k_F^3}{N_s}\int_0^{1} \left(\frac{1}{kuv_F} \log\left(\frac{-\epsilon_{\k} + i\omega - kuv_F}{-\epsilon_{\k} + i\omega + kuv_F}\right) - \frac{1}{kuv_F\hbar} \log\left(\frac{\epsilon_{\k} + i\omega - kuv_F}{\epsilon_{\k} + i\omega + kuv_F} \right)\right) \frac{u^2\d u}{(2\pi)^2} .\(\)

We perform some small simplification, including setting \(v = \V/N_s\) to be the volume of the primitive unit cell

\(\)\chi_0(k) = \frac{2vk_F^3}{kv_F(2\pi)^2}\int_0^{1} \left(\log\left(\frac{-\epsilon_{\k} + i\omega - kuv_F}{-\epsilon_{\k} + i\omega + kuv_F}\right) - \log\left(\frac{\epsilon_{\k} + i\omega - kuv_F}{\epsilon_{\k} + i\omega + kuv_F} \right)\right) u\d u.\(\)

Now, we evaluate the final integral. To make our lives easier, we note that 

\(\)\int_0^1\log\left(\frac{a-bu}{a+bu}\right)u\d u = \int_{-1}^1 \log(a-bu)u \d u\(\)

which allows us to rewrite the integral as

\(\)\chi_0(k) = -\frac{2vk_F^2m}{k(2\pi)^2}\int_{-1}^{1}\log\left(\frac{\epsilon_{\k} + i\omega - kuv_F}{-\epsilon_{\k} + i\omega - kuv_F}\right) u\d u.\(\)

Finally, using the result

$$\begin{align}
\int_{-1}^1 u\log(a-bu) \d u ={}& \frac{a-bu}{b^2}\left( \frac{a-bu}{2}\left(\log(a-bu) - \frac{1}{2}\right) - a(\log(a-bu) - 1)\right)\bigg|_{-1}^1 \\
={}& - \frac{a}{b} + \frac{b^2-a^2}{2b^2}\log\left(\frac{a-b}{a+b}\right)
\end{align}$$

We can then evaluate this with \(a_+ = \epsilon_{\k} + i\omega\), \(a_- = -\epsilon_{\k} + i\omega\), and \(b = kv_F\)

\(\)\chi_0(k) = -\frac{2vk_F^3}{kv_F\hbar(2\pi)^2}\left[-\frac{a_+}{b} + \frac{1}{2}\left(1 - \frac{a_+^2}{b^2}\right)\log\left(\frac{a_+-b}{a_++b}\right)  + \frac{a_-}{b}- \frac{1}{2}\left(1 - \frac{a_-^2}{b^2}\right)\log\left(\frac{a_--b}{a_-+b}\right)\right].\(\)

We rearrange this a little bit to find

\(\)\chi_0(k) = \frac{2vk_F^3}{kv_F\hbar(2\pi)^2}\left[\frac{a_+-a_-}{b}+ \frac{1}{2}\left(1 - \frac{a_+^2}{b^2}\right)\log\left(\frac{a_++b}{a_+-b}\right)  + \frac{1}{2}\left(1 - \frac{a_-^2}{b^2}\right)\log\left(\frac{a_--b}{a_-+b}\right)\right].\(\)

Now substituting in the values, we get

\(\)\chi_0(k) = \frac{2vk_Fm}{\hbar(2\pi)^2}\frac{k_F}{k}\left[\frac{k}{k_F} + \frac{1}{2}(1 - x_+^2)\log\left(\frac{\epsilon_{\k} + i\omega + kv_F}{\epsilon_{\k} + i\omega - kv_F}\right) + \frac{1}{2}(1-x_-^2)\log\left(\frac{-\epsilon_{\k} + i\omega - kv_F}{-\epsilon_{\k} + i\omega + kv_F}\right) \right]\(\)

Then, we use ASSUMING THAT \(k < 2k_F\), IS THIS ALWAYS TRUE?? IT IS FOR US, SINCE IS THIE IS THE SMALL \(k\) limit, BUT IS IT TRUE IN GENERAL?

$$\begin{align}
\log\left(\frac{\epsilon_{\k} + i\omega + kv_F\hbar}{\epsilon_{\k} + i\omega - kv_F\hbar}\right) ={}& \log\left(\frac{1 + i\omega/kv_F + k/2k_F}{-1 + i\omega/kv_F + k/2k_F}\right) \\
={}& -i\pi\sgn(\omega) + \log\left(\frac{1 + i\omega/kv_F + k/2k_F}{1 - i\omega/kv_F - k/2k_F}\right) 
\end{align}$$

$$\begin{align}
\log\left(\frac{-\epsilon_{\k} + i\omega - kv_F\hbar}{-\epsilon_{\k} + i\omega + kv_F\hbar}\right) ={}& \log\left(\frac{-1 + i\omega/kv_F - k/2k_F}{1 + i\omega/kv_F - k/2k_F}\right) \\
={}& i\pi\sgn(\omega) + \log\left(\frac{1 - i\omega/kv_F + k/2k_F}{1 + i\omega/kv_F - k/2k_F}\right)
\end{align}$$

Plugging these representations in, we find that 

$$\begin{align}
\chi_0(k) ={}& \frac{2vk_Fm}{(2\pi)^2}\frac{k_F}{k}\left[\frac{k}{k_F} + \frac{1}{2}(1 - x_+^2)\log\left(\frac{1 + \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 - \frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right)  + \frac{1}{2}(1-x_-^2)\log\left(\frac{1 - \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 + \frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right) \right. \\
&\left. -\frac{i\pi}{2}\sgn(\omega)(x_-^2-x_+^2) \right] 
\end{align}$$

Finally, using the fact that \(\rho(E_F) = vk_Fm/\pi^2\)

$$\begin{align}
\chi_0(k) ={}& \frac{\rho(E_F)}{2} \left[1 + \frac{k_F}{2k}(1 - x_+^2)\log\left(\frac{1 + \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 - \frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right)  \right. \\
&\left. + \frac{k_F}{2k}(1-x_-^2)\log\left(\frac{1 - \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 + i\frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right)  + i\frac{\pi k_F}{2k}\sgn(\omega)(x_+^2-x_-^2) \right] 
\end{align}$$

whereby \(x_+ = \frac{k}{2k_F} + \frac{i\omega}{kv_F}\), and \(x_- = -\frac{k}{2k_F} + \frac{i\omega}{kv_F}\)
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the answer of the previous question in the limit 

$$\begin{align}
\chi_0(k) ={}& \frac{\rho(E_F)}{2} \left[1 + \frac{k_F}{2k}(1 - x_+^2)\log\left(\frac{1 + \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 - \frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right)  + \frac{k_F}{2k}(1-x_-^2)\log\left(\frac{1 - \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 + i\frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right) \right. \\
&\left. +i\frac{\pi k_F}{2k}\sgn(\omega)(x_+^2-x_-^2) \right] 
\end{align}$$


<div class="answerBox"> 
 <button onclick="myFunction('answer249')" class="answerButton">Show Answer</button> 
 <div  id='answer249' class="answer" >
<ol type="a">
<li> Now, we use the Taylor expansion

\(\)\log\left(\frac{1+a}{1-a}\right) = 2\left(a + \frac{a^3}{3} + \frac{a^5}{5} + \cdots\right)\(\)

to simplify these logarithms. We find that (with \(x_+ = \frac{k}{2k_F} + \frac{i\omega}{kv_F}\), and \(x_- = -\frac{k}{2k_F} + \frac{i\omega}{kv_F}\)),

$$\begin{align}
\chi_0(k) ={}& \frac{\rho(E_F)}{2} \left[1 + \frac{k_F}{2k}(1 - x_+^2)\log\left(\frac{1 + x_+}{1 - x_+}\right) + \frac{k_F}{2k}(1-x_-^2)\log\left(\frac{1 - x_-}{1 + x_-}\right) \right. \\
&\left. +i\frac{\pi k_F}{2k}\sgn(\omega)(x_+^2-x_-^2) \right] 
\end{align}$$

Taylor expanding, and truncating at order \(k^2\) and \(\omega/k\), we find that 

$$\begin{align}
\chi_0(k) ={}& \frac{\rho(E_F)}{2} \left[1 + \frac{k_F}{k}(1 - x_+^2)\left(x_+ + \frac{x_+^3}{3}\right) - \frac{k_F}{k}(1-x_-^2)\left(x_- + \frac{x_-^3}{3}\right) \right. \\
&\left. + i\frac{\pi k_F}{2k}\sgn(\omega)(x_+^2-x_-^2) \right] 
\end{align}$$

There are substantial simplifications, yielding

$$\begin{align}
\chi_0(k) ={}& \frac{\rho(E_F)}{2} \left[1 + \frac{k_F}{k}\left(\frac{k}{k_F} + \frac{2}{3}\left(-\frac{2k^3}{8k_F^3}\right) \right) - \frac{\pi|\omega|}{kv_F}\right] \\
={}& \frac{\rho(E_F)}{2} \left[1 + 1- \frac{k^2}{6k_F^2} - \frac{\pi|\omega|}{kv_F}\right] \\
={}& \rho(E_F)\left[1 - \frac{1}{3}\left(\frac{k}{2k_F}\right)^2 - \frac{\pi|\omega|}{2kv_F}\right]
\end{align}$$

Not that the Landau damping term \(\pi|\omega|/2qv_F\) makes sense because the damping term should be \(\pi/k\), which is half of the wavelength of the plasmon osccilation, and then dividing the wavelength by \(v_F\) gives the relaxation time, and then the 2 is cancelled by the total density of states, because the \(\rho(E_F)\) is just the density of states per unit spin. 

</li>
<li> What happens if instead we are interested in fluctuations about a nonzero \(k\) wavevector? This time, we expand about \(<b>Q</b>\), so \(|\k-<b>Q</b>| \ll k_F\). We also expand for \(|\omega|/v_FQ \ll 1\). Thus, our Taylor expansion will need to be modified slightly. We have 

$$\begin{align}
\frac{k}{k_F} ={}& \frac{Q}{k_F}\sqrt{1 + \frac{2q\cos\theta}{Q} + \frac{q^2}{Q^2}} \\
={}& \frac{Q}{k_F}\left(1 - \right)
\end{align}$$



</li></ol>

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the coupling constant \(u(q_1,q_2,q_3)\) for the case when it is evaluated at \(q_1=q_2=q_3=0\).
$$\begin{align}
u(q_1,q_2,q_3) ={}& \frac{2}{\beta N_s}\sum_{k} \mathcal{G}_0(k+q_1+q_2+q_3)\mathcal{G}_0(k+q_2+q_3)\mathcal{G}_0(k+q_3)\mathcal{G}_0(k) 
\end{align}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer297')" class="answerButton">Show Answer</button> 
 <div  id='answer297' class="answer" >
We find that 

$$\begin{align}
u(0,0,0) ={}& \frac{2}{\beta N_s}\sum_{k} [\mathcal{G}_0(k)]^4 \\
={}& \frac{2}{12N_s} \sum_{\k} n_F"'(\xi_{\k}) \\
={}& -\frac{2\V}{12N_s} \int (-n_F'(\xi_{\k}))" \frac{\d^3\k}{(2\pi)^3} \\
={}& -\frac{\V}{12N_s}\rho"(\mu)
\end{align}$$

Since, for a 3D electron gas the DOS's second derivative is negative, we have the \(u > 0\). Note that 

\(\)\rho(E) = v\left(\frac{2m}{\hbar^2}\right)^{3/2}\frac{\sqrt{E}}{2}\(\)

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the Lindhard function in two dimensions 

\(\)\chi_0(k) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega}\(\)

<div class="answerBox"> 
 <button onclick="myFunction('answer317')" class="answerButton">Show Answer</button> 
 <div  id='answer317' class="answer" >
We approximate the Fermi-Dirac functions as \(n_F(\xi) = \theta(-\xi)\), where \(\xi_{\k} = \epsilon_{\k} - \mu\), and \(\epsilon_{\k} = \k^2/2m\). We also move to the thermodynamic limit to get 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int \frac{\theta(-\xi_{\q}) - \theta(-\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega} \frac{\d\q}{(2\pi)^2}\(\)

where \(\V\) is actually an area, but we use \(\V\) for consistency. After shifting the integration variable in the second term, we can rewrite this as 

\(\)\chi_0(k) = -\frac{2\V}{N_s}\int \theta(-\xi_{\q})\left(\frac{1}{\xi_{\q} - \xi_{\k+\q} + i\omega} - \frac{1}{\xi_{\q-\k} - \xi_{\q} + i\omega}\right) \frac{\d\q}{(2\pi)^2}\(\)

We integrate over the entire occupied region to get 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int_0^{k_F}\int_0^{2\pi} \left(\frac{1}{\xi_{\q} - \xi_{\k+\q} + i\omega} - \frac{1}{\xi_{\q-\k} - \xi_{\q} + i\omega}\right) \frac{q \d\theta \d q}{(2\pi)^2}\(\)

We are using the fact that the dispersion is spherically symmetric in order to write this. First, we integrate over the angle \(\theta\). To do this, we need to introduce \(\theta\) via \(\q\cdot\k = qk\cos\theta\), so that 

$$\begin{align}
\chi_0(k) ={}& -2\frac{\V}{N_s}\int_0^{k_F}\int_0^{2\pi}\left(\frac{1}{\frac{1}{2m}(-k^2 - 2kq\cos\theta) + i\omega} - \frac{1}{\frac{1}{2m}(k^2 - 2kq\cos\theta) + i\omega}\right) \frac{q\d\theta\d q}{(2\pi)^2} \\
={}& -2\frac{\V}{N_s}\int_0^{k_F}\int_0^{2\pi} \left(\frac{1}{-\epsilon_{\k} - kq\cos\theta/m + i\omega} - \frac{1}{\epsilon_{\k} - kq\cos\theta/m + i\omega}\right) \frac{q \d \theta \d q}{(2\pi)^2}
\end{align}$$

To ease the notation a little bit, rescale as \(q = k_Fu\) to get 

$$\begin{align}
\chi_0(k) ={}& -2\frac{\V}{N_s}\int_0^1 \int_0^{2\pi}\left(\frac{1}{-\epsilon_{\k} - kv_Fu\cos\theta + i\omega} - \frac{1}{\epsilon_{\k} - kv_F u\cos\theta + i\omega}\right) \frac{k_F^2 u \d\theta \d u}{(2\pi)^2}
\end{align}$$

where \(v_F = k_F/m\). To make this integral easier, we note that we can make the substitution \(\theta = \theta' + \pi\) in the second integral to get 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int_0^1\left[ \int_0^{2\pi}\frac{1}{-\epsilon_{\k} - kv_Fu\cos\theta + i\omega} \d\theta - \int_{-\pi}^\pi \frac{1}{\epsilon_{\k} + kv_F u\cos\theta' + i\omega}\d\theta'\right] \frac{k_F^2 u\d u}{(2\pi)^2}\(\)

but since it is a periodic function we can just rewrite it as 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int_0^1\left[ \int_0^{2\pi}\frac{1}{-\epsilon_{\k} - kv_Fu\cos\theta + i\omega} \d\theta - \int_{0}^{2\pi} \frac{1}{\epsilon_{\k} + kv_F u\cos\theta + i\omega}\d\theta\right] \frac{k_F^2 u\d u}{(2\pi)^2}\(\)

and now combining the two together, we get 

\(\)\chi_0(k) = 2\frac{\V}{N_s}\int_0^1 \int_0^{2\pi} \left[ \frac{1}{\epsilon_{\k} + kv_Fu\cos\theta - i\omega} + \frac{1}{\epsilon_{\k} + kv_F u\cos\theta + i\omega}\right]\d\theta \frac{k_F^2 u\d u}{(2\pi)^2}\(\)

This allows us to make the observation that the integral should be entirely real (the integrand is a complex number plus its complex conjugate!). This will serve as a sanity check later. Now, we return to the previous integral and perform a Weierstrass substitution. This gives us 

\(\)\int \frac{1}{a - b\cos\theta} \d\theta = \frac{2}{\sqrt{a^2-b^2}}\arctan\left(\tan\left(\frac{\theta}{2}\right) \sqrt{\frac{a+b}{a-b}}\right)\(\)

Then, we need to evaluate this carefully. This gives us 

$$\begin{align}
\int_{-\pi}^\pi \frac{1}{\epsilon_{\k} - i\omega + kv_Fu\cos\theta} ={}& -\frac{2}{\sqrt{(i\omega - \epsilon_{\k})^2 - k^2v_F^2u^2}}\arctan\left(\tan\left(\frac{\theta}{2}\right)\sqrt{\frac{\epsilon_{\k} - i\omega - kv_Fu}{\epsilon_{\k} - i\omega + kv_Fu}}\right)\bigg|_{-\pi}^\pi
\end{align}$$

To evaluate the limit, we note that we can rewrite 

\(\)\frac{\epsilon_{\k} - i\omega - kv_Fu}{\epsilon_{\k} - i\omega + kv_Fu} = re^{i\varphi}\(\)

Here, 

$$\begin{align}
\varphi ={}& \Arg\left(\frac{\epsilon_{\k} - i\omega - kv_Fu}{\epsilon_{\k} - i\omega + kv_Fu}\right)
\end{align}$$

We will need to evaluate the limit as \(\theta\to\pi/2\). Thus, we note that if we have \(\arctan(re^{i\varphi})\) where \(r\to\infty\), we get:

\(\)\lim_{r\to\infty} \arctan(re^{i\xi}) = \frac{\pi}{2}\sgn(\Re(\cos\xi))\(\)

Thus, we need to compute \(\sgn(\cos(\varphi/2))\). Since \(\varphi\in(-\pi,\pi]\), we have that \(\varphi/2 \in (-\pi/2,\pi/2]\) and therefore is always positive. Thus, 

$$\begin{align}
\int_{-\pi}^\pi \frac{1}{i\omega - \epsilon_{\k} - kv_Fu\cos\theta} ={}& \frac{2\pi}{\sqrt{(i\omega - \epsilon_{\k})^2 - k^2v_F^2u^2}}
\end{align}$$

We perform a similar operation for the other integral to get that 

$$\begin{align}
\int_{-\pi}^\pi \frac{1}{\epsilon_{\k} - kv_Fu\cos\theta + i\omega} ={}& \frac{2}{\sqrt{(i\omega + \epsilon_{\k})^2 - k^2v_F^2u^2}}\arctan\left(\tan\left(\frac{\theta}{2}\right)\sqrt{\frac{i\omega + \epsilon_{\k} + kv_Fu}{i\omega  + \epsilon_{\k} - kv_Fu}}\right)\bigg|_{-\pi}^\pi \\
={}& \frac{2\pi}{\sqrt{(i\omega + \epsilon_{\k})^2 - k^2v_F^2u^2}}
\end{align}$$

DEFINE

\(\)Q^1_\pm = \bigg| \frac{\epsilon_{\k} + i\omega \pm \sqrt{(\epsilon_{\k} + i\omega)^2 - (kv_Fu)^2}}{kv_Fu}\bigg|, \qquad Q^2_\pm = \bigg| \frac{\epsilon_{\k} - i\omega \pm \sqrt{(\epsilon_{\k} - i\omega)^2 - (kv_Fu)^2}}{kv_Fu}\bigg|\(\)

where the square roots are the principal branch. Then, we have that 

\(\)\int_{-\pi}^\pi \frac{\d\theta}{\epsilon_{\k} + i\omega + kv_Fu\cos\theta} = \begin{cases} 
0, & Q^1_+ > 1, Q^1_- > 1 \\ 
0, & Q^1_+ < 1, Q^1_- < 1 \\ 
\frac{2\pi}{\sqrt{(\epsilon_{\k}+i\omega)^2 - (kv_Fu)^2}}, & Q^1_+ > 1, Q^1_- < 1 \\
-\frac{2\pi}{\sqrt{(\epsilon_{\k}+i\omega)^2 - (kv_Fu)^2}}, & Q^1_+ < 1, Q^1_- > 1 
\end{cases}\(\)

\(\)\int_{-\pi}^\pi \frac{\d\theta}{\epsilon_{\k} - i\omega + kv_Fu\cos\theta} = \begin{cases} 
0, & Q^2_+ > 1, Q^2_- > 1 \\ 
0, & Q^2_+ < 1, Q^2_- < 1 \\ 
\frac{2\pi}{\sqrt{(\epsilon_{\k}-i\omega)^2 - (kv_Fu)^2}}, & Q^2_+ > 1, Q^2_- < 1 \\
-\frac{2\pi}{\sqrt{(\epsilon_{\k}-i\omega)^2 - (kv_Fu)^2}}, & Q^2_+ < 1, Q^2_- > 1 
\end{cases}\(\)

How can we simplify this situation? Well, we start by noting that the interior of the absolute values for \(Q^1_+, Q^2_+\) are complex conjugates of one another, which means that \(Q^1_+ = Q^2_+\). The same can be said about \(Q^1_- = Q^2_-\). Thus, we remove the superscripts 1,2:

\(\)\int_{-\pi}^\pi \frac{\d\theta}{\epsilon_{\k} + i\omega + kv_Fu\cos\theta} = \begin{cases} 
0, & Q_+ > 1, Q_- > 1 \\ 
0, & Q_+ < 1, Q_- < 1 \\ 
\frac{2\pi}{\sqrt{(\epsilon_{\k}+i\omega)^2 - (kv_Fu)^2}}, & Q_+ > 1, Q_- < 1 \\
-\frac{2\pi}{\sqrt{(\epsilon_{\k}+i\omega)^2 - (kv_Fu)^2}}, & Q_+ < 1, Q_- > 1 
\end{cases}\(\)

\(\)\int_{-\pi}^\pi \frac{\d\theta}{\epsilon_{\k} - i\omega + kv_Fu\cos\theta} = \begin{cases} 
0, & Q_+ > 1, Q_- > 1 \\ 
0, & Q_+ < 1, Q_- < 1 \\ 
\frac{2\pi}{\sqrt{(\epsilon_{\k}-i\omega)^2 - (kv_Fu)^2}}, & Q_+ > 1, Q_- < 1 \\
-\frac{2\pi}{\sqrt{(\epsilon_{\k}-i\omega)^2 - (kv_Fu)^2}}, & Q_+ < 1, Q_- > 1 
\end{cases}\(\)

We now want to solve the inequalities for \(u\), so that we know what bounds we can place on it. The fundamental thing that we are concerned with is the behaviour of the function

\(\)f_\pm(z) = z \pm \sqrt{z^2-1}\(\)

where here, \(z = \alpha + i\beta\), where \(\alpha = k/2k_F\) and \(\beta = \omega/v_Fk\). When is this function greater (in magnitude) than 1? Note that the square root is taken in the principal branch. The branch cut extends from 1 out on the positive real axis (we choose this!)




First, we see that 

\(\)\lim_{u\to 0}Q_+ = \infty, \qquad \lim_{u\to 0} Q_- = 0\(\)

Next, we want to find the bounds and we do this for the case \(k/2k_F \ll 1\), and \(\omega/kv_F\ll 1\). In this case, then we have that 

$$\begin{align}
Q_+ ={}& \bigg| \frac{k}{2k_F} + \frac{i\omega}{kv_F} + i\sqrt{1 - \left(\frac{k}{2k_F} + \frac{i\omega}{kv_F}\right)^2}\bigg| \\
={}& \bigg| \frac{k}{2k_F} + \frac{i\omega}{kv_F} + i\left(1 - \frac{1}{2}\left(\frac{k}{2k_F} + \frac{i\omega}{kv_F}\right)^2\right)\bigg|
\end{align}$$

Then, the imaginary part is greater than 1 so \(Q_+ > 1\). Thus since \(Q_+>1\) for both \(u\to 0\) and \(u\to 1\). For \(Q_-\), we have that 

$$\begin{align}
Q_- ={}& \bigg| \frac{k}{2k_F} + \frac{i\omega}{kv_F} - i\sqrt{1 - \left(\frac{k}{2k_F} + \frac{i\omega}{kv_F}\right)^2}\bigg| \\
={}& \bigg| \frac{k}{2k_F} + \frac{i\omega}{kv_F} - i\left(1 - \frac{1}{2}\left(\frac{k}{2k_F} + \frac{i\omega}{kv_F}\right)^2\right)\bigg|
\end{align}$$

and for this, we have that \(\omega/v_Fk - 1\) is less than 1 (in magnitude), and so is \(k/2k_F\), so \(Q_- < 1\) for both \(u\to 0\) and \(u\to 1\). Thus, we have the case 

\(\)\int_{-\pi}^\pi \frac{\d\theta}{\epsilon_{\k} + i\omega + kv_Fu\cos\theta} = \frac{2\pi}{\sqrt{(\epsilon_{\k}+i\omega)^2 - (kv_Fu)^2}}\(\)

\(\)\int_{-\pi}^\pi \frac{\d\theta}{\epsilon_{\k} - i\omega + kv_Fu\cos\theta} = 
\frac{2\pi}{\sqrt{(\epsilon_{\k}-i\omega)^2 - (kv_Fu)^2}}\(\)

Therefore, there are no modifications to the bounds of the integral. Thus, we have that 

$$\begin{align}
\chi_0(k) ={}& 2\frac{\V}{N_s}\int_0^1 \left[\frac{2\pi}{\sqrt{(\epsilon_{\k} + i\omega)^2 - (kv_Fu)^2}} + \frac{2\pi}{\sqrt{(\epsilon_{\k} - i\omega)^2 - (kv_Fu)^2}}\right] \frac{k_F^2 u \d u}{(2\pi)^2} \\
={}& 2\frac{\V}{N_s}\int_0^1 \left[\frac{1}{\sqrt{(\epsilon_{\k} + i\omega)^2 - (kv_Fu)^2}} + \frac{1}{\sqrt{(\epsilon_{\k} - i\omega)^2 - (kv_Fu)^2}}\right] \frac{k_F^2 u \d u}{2\pi} \\
\end{align}$$

The final integrals are easy, and we get 

$$\begin{align}
\chi_0(k) ={}& -\frac{\V k_F^2}{\pi N_sk^2 v_F^2}\left(\sqrt{(\epsilon_{\k} + i\omega)^2 - k^2 v_F^2 u^2}\bigg|_0^1 + \sqrt{(\epsilon_{\k} - i\omega)^2 - k^2 v_F^2 u^2}\bigg|_0^1 \right)
\end{align}$$

Then, to take the square root properly, we set each square root to be 

\(\)x + iy = \sqrt{(\epsilon_{\k} + i\omega)^2 - k^2 v_F^2 u^2}\(\)

which gives us 

\(\)x(u) = \sqrt{\frac{\epsilon_{\k}^2 - \omega^2 - (v_Fku)^2 + \sqrt{(\epsilon_{\k}^2 - \omega^2 - (v_Fku)^2)^2 + 4\omega^2\epsilon_{\k}^2}}{2}}\(\)
\(\)y(u) = \sqrt{\frac{-(\epsilon_{\k}^2 - \omega^2 - (v_Fku)^2) + \sqrt{(\epsilon_{\k}^2 - \omega^2 - (v_Fku)^2)^2 + 4\omega^2\epsilon_{\k}^2}}{2}}\(\)

so then 

$$\begin{align}
\chi_0(k) ={}& -\frac{\V k_F^2}{\pi N_sk^2 v_F^2}\left((x(u) + iy(u)) \bigg|_0^1 + (x(u) - iy(u))\bigg|_0^1 \right) \\
={}& -\frac{2\V k_F^2}{\pi N_sk^2 v_F^2}x(u) \bigg|_0^1 \\
={}& -\frac{2\V k_F^2}{\pi N_sk^2 v_F^2}\left[\sqrt{\frac{\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2 + \sqrt{(\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2)^2 + 4\omega^2\epsilon_{\k}^2}}{2}} - \sqrt{\frac{\epsilon_{\k}^2 - \omega^2 + \sqrt{(\epsilon_{\k}^2 - \omega^2 )^2 + 4\omega^2\epsilon_{\k}^2}}{2}}\right] \\
={}& -\frac{2\V m^2}{\pi N_sk^2}\left[\sqrt{\frac{\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2 + \sqrt{(\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2)^2 + 4\omega^2\epsilon_{\k}^2}}{2}} - \sqrt{\frac{\epsilon_{\k}^2 - \omega^2 + \sqrt{(\epsilon_{\k}^2 + \omega^2 )^2}}{2}}\right] \\
={}& -\frac{2\V m^2}{\pi N_sk^2}\left[\sqrt{\frac{\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2 + \sqrt{(\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2)^2 + 4\omega^2\epsilon_{\k}^2}}{2}} - \sqrt{\frac{\epsilon_{\k}^2 - \omega^2 + \epsilon_{\k}^2 + \omega^2}{2}}\right] \\
={}& \frac{2\V m^2}{\pi N_sk^2}\left[\epsilon_{\k} - \sqrt{\frac{\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2 + \sqrt{(\epsilon_{\k}^2 - \omega^2 - (v_Fk)^2)^2 + 4\omega^2\epsilon_{\k}^2}}{2}}  \right] \\
={}& \frac{2\V m^2v_F}{\pi N_sk}\left[\frac{\epsilon_{\k}}{v_Fk} - \sqrt{\frac{\epsilon_{\k}^2/(v_Fk)^2 - \omega^2/(v_Fk)^2 - 1 + \sqrt{(1 - \epsilon_{\k}^2/(v_Fk)^2 + \omega^2/(v_Fk)^2)^2 + 4\omega^2\epsilon_{\k}^2/(v_Fk)^4}}{2}}  \right]
\end{align}$$

Then, letting \(\alpha = k/2k_F\) and \(\beta =\omega/v_Fk\), we see that \(\epsilon_{\k}/v_Fk = k/2k_F\) (use the fact that \(k_F = v_Fm\)), we Taylor expand the square roots. Thus we rewrite it as

$$\begin{align}
\chi_0(k) ={}& \frac{\V m}{\pi N_s\alpha}\left[\alpha - \sqrt{\frac{\alpha^2 - \beta^2 - 1 + \sqrt{(1 - \alpha^2 + \beta^2)^2 + 4\alpha^2\beta^2}}{2}}  \right] \\
={}& \frac{\rho(\epsilon_F)}{\alpha}\left[\alpha - \sqrt{\frac{\alpha^2 - \beta^2 - 1 + \sqrt{(1 - \alpha^2 + \beta^2)^2 + 4\alpha^2\beta^2}}{2}}  \right]
\end{align}$$

where \(\rho(\epsilon_F) = m\V/\pi N_s\) is the total density of states (includes spin up and down).

Let us use the fact that 

\(\)\sqrt{1 + x} = 1 + \frac{x}{2} - \frac{x^2}{8} + \frac{x^3}{16} - \frac{5x^4}{128} + \cdots\(\)

which tells us that 

$$\begin{align}
S ={}& \sqrt{(1 - \alpha^2 + \beta^2)^2 + 4\alpha^2\beta^2} - 1 + \alpha^2 - \beta^2 \\
={}& \sqrt{1 + 2(\beta^2-\alpha^2) + (\beta^2 + \alpha^2)^2} - 1 + \alpha^2 - \beta^2 \\
={}& \alpha^2 - \beta^2 + (\beta^2-\alpha^2) + \frac{1}{2}(\beta^2 + \alpha^2)^2 - \frac{1}{8}[2(\beta^2-\alpha^2) + (\beta^2 + \alpha^2)^2]^2 \\
&+ \frac{1}{16}[2(\beta^2-\alpha^2) + (\beta^2 + \alpha^2)^2]^3 - \frac{5[2(\beta^2-\alpha^2) + (\beta^2 + \alpha^2)^2]^4}{128} \\
={}& 2\alpha^2\beta^2 + 2(\alpha^2 - \beta^2)\alpha^2\beta^2 + 2\alpha^2\beta^2(\alpha^4 - 3\alpha^2\beta^2 + \beta^4) + \cdots \\
={}& 2\alpha^2\beta^2(1 + \alpha^2 - \beta^2 + (\alpha^4 - 3\alpha^2\beta^2 + \beta^4) + \cdots) 
\end{align}$$

Plugging this in, we get 

\(\)\chi_0(k) = \rho(\epsilon_F)\left[1 - \beta - \frac{1}{2}\beta\alpha^2 + \cdots \right]\(\)

The interesting thing is that at zero frequency this is independent of the wave vector!! 

\(\)\chi_0(k) = \rho(\epsilon_F)\left[1 - \frac{|\omega|}{qv_F} - \frac{1}{2}\frac{|\omega|}{qv_F}\frac{q^2}{4k_F^2} + \cdots \right]\(\)

</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Evaluate the Lindhard function in 3 dimensions.

\(\)\chi_0(k) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega}.\(\)

<div class="answerBox"> 
 <button onclick="myFunction('answer535')" class="answerButton">Show Answer</button> 
 <div  id='answer535' class="answer" >
We approximate the Fermi-Dirac functions as \(n_F(\xi) = \theta(-\xi)\), where \(\xi_{\k} = \epsilon_{\k} - \epsilon_F\), and \(\epsilon_{\k} = \k^2/2m\). In this case, after changing to continuous space, we have 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int \frac{\theta(-\xi_{\q}) - \theta(-\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega} \frac{\d\q}{(2\pi)^3} .\(\)

Now shifting the integration variable of the second term, we can rewrite this as 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int \theta(-\xi_{\q})\left(\frac{1}{\xi_{\q} - \xi_{\k+\q} + i\omega} - \frac{1}{\xi_{\q-\k} - \xi_{\q} + i\omega}\right) \frac{\d\q}{(2\pi)^3} .\(\)

Then, noting that 

\(\)\theta(-\xi_{\q}) = \begin{cases} 1, & |\q| < k_F \\ 0, & |\q| > k_F \end{cases}\(\)

we can integrate the entire occupied region to get 

\(\)\chi_0(k) = -2\frac{\V}{N_s}\int_0^{k_F}\int_0^\pi \left(\frac{1}{\xi_{\q} - \xi_{\k+\q} + i\omega} - \frac{1}{\xi_{\q-\k} - \xi_{\q} + i\omega}\right) \frac{q^2\sin\theta \d\theta\d q}{(2\pi)^2} .\(\)

where we have used the fact that the dispersion is spherically symmetric. Next, we will integrate over the angle \(\theta\). First, we need to introduce \(\theta\) through \(\q\cdot\k = qk\cos\theta\), so 

$$\begin{align}
\chi_0(k) ={}& -2\frac{\V}{N_s}\int_0^{k_F}\int_0^\pi \left(\frac{1}{\frac{1}{2m}(-k^2-2kq\cos\theta) + i\omega} - \frac{1}{\frac{1}{2m}(k^2-2kq\cos\theta) + i\omega}\right) \frac{q^2\sin\theta \d\theta\d q}{(2\pi)^2} \\
={}& -2\frac{\V}{N_s}\int_0^{k_F}\int_0^\pi \left(\frac{1}{- \epsilon_{\k}-kq\cos\theta/m + i\omega} - \frac{1}{\epsilon_{\k} - kq\cos\theta/m + i\omega}\right) \frac{q^2\sin\theta \d\theta\d q}{(2\pi)^2}
\end{align}$$

To make notation a big nicer, we rescale \(q = k_Fu\) and get 

$$\begin{align}
\chi_0(k) ={}& -2\frac{\V}{N_s}\int_0^{1}\int_0^\pi \left(\frac{1}{- \epsilon_{\k}-kv_Fu\cos\theta + i\omega} - \frac{1}{\epsilon_{\k} - kuv_F\cos\theta + i\omega}\right) \frac{k_F^3u^2\sin\theta \d\theta\d u}{(2\pi)^2}
\end{align}$$

Let us note that, by making the substitution \(\theta' = \theta - \pi\), we have 

\(\)\int_0^\pi \frac{\sin\theta}{a - b\cos\theta} = -\int_{-\pi}^0 \frac{\sin\theta'}{a+b\cos\theta} \d\theta' = -\int_\pi^0 \frac{\sin\theta}{a+b\cos\theta}\d\theta = \int_0^\pi \frac{\sin\theta}{a+b\cos\theta}\d\theta\(\)

Taking advantage of this fact, we can rewrite the second term as

$$\begin{align}
\chi_0(k) ={}& -2\frac{\V}{N_s}\int_0^{1}\int_0^\pi \left(\frac{1}{- \epsilon_{\k}-kv_Fu\cos\theta + i\omega} - \frac{1}{\epsilon_{\k} + kuv_F\cos\theta + i\omega}\right) \frac{k_F^3u^2\sin\theta \d\theta\d u}{(2\pi)^2} \\
={}& 2\frac{\V}{N_s}\int_0^{1}\int_0^\pi \left(\frac{1}{\epsilon_{\k}+kv_Fu\cos\theta - i\omega} + \frac{1}{\epsilon_{\k} + kuv_F\cos\theta + i\omega}\right) \frac{k_F^3u^2\sin\theta \d\theta\d u}{(2\pi)^2} \\
={}& 4\frac{\V}{N_s}\int_0^{1}\int_0^\pi \frac{\epsilon_{\k} + kv_Fu\cos\theta}{(\epsilon_{\k}+kv_Fu\cos\theta)^2 +\omega^2}\frac{k_F^3u^2\sin\theta \d\theta\d u}{(2\pi)^2}
\end{align}$$

Thus the Lindhard function is entirely real! Let us continue integrating. Define \(x = \cos\theta\) to get 

$$\begin{align}
\chi_0(k) ={}& 4\frac{\V}{N_s}\int_0^{1}\int_{-1}^1 \frac{\epsilon_{\k} + kv_Fux}{(\epsilon_{\k}+kv_Fux)^2 +\omega^2}\frac{k_F^3u^2 \d x\d u}{(2\pi)^2} \\
={}& 4\frac{\V}{N_s}\int_0^{1}\frac{1}{2kv_Fu}\log((\epsilon_{\k}+kv_Fux)^2 +\omega^2)\bigg|_{-1}^1 \frac{k_F^3u^2\d u}{(2\pi)^2} \\
={}& 2\frac{\V}{N_skv_F}\int_0^{1}\log\left[\frac{(\epsilon_{\k} + kv_Fu)^2 +\omega^2}{(\epsilon_{\k} - kv_Fu)^2 +\omega^2}\right] \frac{k_F^3u\d u}{(2\pi)^2}
\end{align}$$

Finally, we need to do the \(u\) integral. This one is the most challenging one! IS THERE AN EASY WAY TO DO THIS???



and this gives us (where \(v_F = k_F/m\))

\(\)\chi_0(k) = \frac{2\V k_F^3}{N_s}\int_0^{1} \left(\frac{1}{kuv_F} \log\left(\frac{-\epsilon_{\k} + i\omega - kuv_F}{-\epsilon_{\k} + i\omega + kuv_F}\right) - \frac{1}{kuv_F\hbar} \log\left(\frac{\epsilon_{\k} + i\omega - kuv_F}{\epsilon_{\k} + i\omega + kuv_F} \right)\right) \frac{u^2\d u}{(2\pi)^2} .\(\)

We perform some small simplification, including setting \(v = \V/N_s\) to be the volume of the primitive unit cell

\(\)\chi_0(k) = \frac{2vk_F^3}{kv_F(2\pi)^2}\int_0^{1} \left(\log\left(\frac{-\epsilon_{\k} + i\omega - kuv_F}{-\epsilon_{\k} + i\omega + kuv_F}\right) - \log\left(\frac{\epsilon_{\k} + i\omega - kuv_F}{\epsilon_{\k} + i\omega + kuv_F} \right)\right) u\d u.\(\)

Now, we evaluate the final integral. To make our lives easier, we note that 

\(\)\int_0^1\log\left(\frac{a-bu}{a+bu}\right)u\d u = \int_{-1}^1 \log(a-bu)u \d u\(\)

which allows us to rewrite the integral as

\(\)\chi_0(k) = -\frac{2vk_F^2m}{k(2\pi)^2}\int_{-1}^{1}\log\left(\frac{\epsilon_{\k} + i\omega - kuv_F}{-\epsilon_{\k} + i\omega - kuv_F}\right) u\d u.\(\)

Finally, using the result

$$\begin{align}
\int_{-1}^1 u\log(a-bu) \d u ={}& \frac{a-bu}{b^2}\left( \frac{a-bu}{2}\left(\log(a-bu) - \frac{1}{2}\right) - a(\log(a-bu) - 1)\right)\bigg|_{-1}^1 \\
={}& - \frac{a}{b} + \frac{b^2-a^2}{2b^2}\log\left(\frac{a-b}{a+b}\right)
\end{align}$$

We can then evaluate this with \(a_+ = \epsilon_{\k} + i\omega\), \(a_- = -\epsilon_{\k} + i\omega\), and \(b = kv_F\)

\(\)\chi_0(k) = -\frac{2vk_F^3}{kv_F\hbar(2\pi)^2}\left[-\frac{a_+}{b} + \frac{1}{2}\left(1 - \frac{a_+^2}{b^2}\right)\log\left(\frac{a_+-b}{a_++b}\right)  + \frac{a_-}{b}- \frac{1}{2}\left(1 - \frac{a_-^2}{b^2}\right)\log\left(\frac{a_--b}{a_-+b}\right)\right].\(\)

We rearrange this a little bit to find

\(\)\chi_0(k) = \frac{2vk_F^3}{kv_F\hbar(2\pi)^2}\left[\frac{a_+-a_-}{b}+ \frac{1}{2}\left(1 - \frac{a_+^2}{b^2}\right)\log\left(\frac{a_++b}{a_+-b}\right)  + \frac{1}{2}\left(1 - \frac{a_-^2}{b^2}\right)\log\left(\frac{a_--b}{a_-+b}\right)\right].\(\)

Now substituting in the values, we get

\(\)\chi_0(k) = \frac{2vk_Fm}{\hbar(2\pi)^2}\frac{k_F}{k}\left[\frac{k}{k_F} + \frac{1}{2}(1 - x_+^2)\log\left(\frac{\epsilon_{\k} + i\omega + kv_F}{\epsilon_{\k} + i\omega - kv_F}\right) + \frac{1}{2}(1-x_-^2)\log\left(\frac{-\epsilon_{\k} + i\omega - kv_F}{-\epsilon_{\k} + i\omega + kv_F}\right) \right]\(\)

Then, we use ASSUMING THAT \(k < 2k_F\), IS THIS ALWAYS TRUE?? IT IS FOR US, SINCE IS THIE IS THE SMALL \(k\) limit, BUT IS IT TRUE IN GENERAL?

$$\begin{align}
\log\left(\frac{\epsilon_{\k} + i\omega + kv_F\hbar}{\epsilon_{\k} + i\omega - kv_F\hbar}\right) ={}& \log\left(\frac{1 + i\omega/kv_F + k/2k_F}{-1 + i\omega/kv_F + k/2k_F}\right) \\
={}& -i\pi\sgn(\omega) + \log\left(\frac{1 + i\omega/kv_F + k/2k_F}{1 - i\omega/kv_F - k/2k_F}\right) 
\end{align}$$

$$\begin{align}
\log\left(\frac{-\epsilon_{\k} + i\omega - kv_F\hbar}{-\epsilon_{\k} + i\omega + kv_F\hbar}\right) ={}& \log\left(\frac{-1 + i\omega/kv_F - k/2k_F}{1 + i\omega/kv_F - k/2k_F}\right) \\
={}& i\pi\sgn(\omega) + \log\left(\frac{1 - i\omega/kv_F + k/2k_F}{1 + i\omega/kv_F - k/2k_F}\right)
\end{align}$$

Plugging these representations in, we find that 

$$\begin{align}
\chi_0(k) ={}& \frac{2vk_Fm}{(2\pi)^2}\frac{k_F}{k}\left[\frac{k}{k_F} + \frac{1}{2}(1 - x_+^2)\log\left(\frac{1 + \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 - \frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right)  + \frac{1}{2}(1-x_-^2)\log\left(\frac{1 - \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 + \frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right) \right. \\
&\left. -\frac{i\pi}{2}\sgn(\omega)(x_-^2-x_+^2) \right] 
\end{align}$$

Finally, using the fact that \(\rho(E_F) = vk_Fm/\pi^2\)

$$\begin{align}
\chi_0(k) ={}& \frac{\rho(E_F)}{2} \left[1 + \frac{k_F}{2k}(1 - x_+^2)\log\left(\frac{1 + \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 - \frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right)  \right. \\
&\left. + \frac{k_F}{2k}(1-x_-^2)\log\left(\frac{1 - \frac{i\omega}{kv_F} + \frac{k}{2k_F}}{1 + i\frac{i\omega}{kv_F} - \frac{k}{2k_F}}\right)  + i\frac{\pi k_F}{2k}\sgn(\omega)(x_+^2-x_-^2) \right] 
\end{align}$$

whereby \(x_+ = \frac{k}{2k_F} + \frac{i\omega}{kv_F}\), and \(x_- = -\frac{k}{2k_F} + \frac{i\omega}{kv_F}\)
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  Evaluate the Lindhard function in general dimensions (is this possible???) 

</div> </li>
<li> <div class="exercise">  Consider the Lindhard function for a general dispersion in \(d\)-dimensions:

\(\)\chi_0(k) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega}.\(\)

<ol type="a">
<li> For \(\k = 0\) and \(\omega = 0\), show that \(\chi_0(\k=0,i\omega=0) = \rho(\epsilon_F)\), where \(\rho\) is the density of states (including or not including spin)
</li>
<li> 
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer665')" class="answerButton">Show Answer</button> 
 <div  id='answer665' class="answer" >
<ol type="a">
<li> 
</li>
<li> 
</li>
<li> 
</li>
<li> 
</li></ol>
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  The Lindhard function can be Taylor expanded for any dispersion relation, in any number of dimensions. For the case of \(\q=0\) order, we want to expand around small Matsubara frequency and around \(\q=0\). 

<ol type="a">
<li> Consider \(\chi_0(0)\).
<ol type="i">
<li> Show that \(\chi_0(0) = \rho(\epsilon_F)\), where \(\rho(\epsilon_F)\) is the density of states (including spin).
</li>
<li> Compute \(\rho(\epsilon_F)\) for \(\epsilon_{\k} = \k^2/2m\) in 3 dimensions.
</li></ol>
</li>
<li> Assume that the dispersion relation satisfies \(\xi_{\k} = \xi_{-\k}\) (it is invariant under spatial inversion).
<ol type="i">
<li> Show that \(\chi(\q,i\omega) = \chi(-\q,i\omega)\). 
</li>
<li> What does this imply about terms linear in \(q\) in the Taylor expansion? 
</li>
<li> Explicitly show that there are no terms linear in \(q\) in the Taylor expansion. 
</li></ol>
</li>
<li> Consider the Taylor expansion \(\chi(\q,0) = \const + \sum_{ij} \alpha_{ij} q^i q^j\). 
<ol type="i">
<li> Compute the coefficients \(\alpha_{ij}\). Write your answer in terms of an integral over the Fermi surface. 
</li>
<li> Compute the coefficient for the dispersion \(\epsilon_{\k} = \k^2/2m\) in \(d=3\).
</li>
<li> Compute the coefficient for the dispersion \(\epsilon_{\k} = \k^2/2m\) in \(d=2\). 
</li>
<li> Compute the coefficient for the dispersion \(\epsilon_{\k} = -2t(\cos(k_xa) + \cos(k_ya))\). Does your answer differ from (c) iii.?
</li></ol>
</li>
<li> Consider the Taylor expansion \(\chi(\k,i\omega) = \const + \sum_{ij} \alpha_{ij} k^i k^j + c\frac{|\omega|}{f(\k)}\). Here, the \(f(\k)\) is sometimes just \(f(\k) = |\k|\), but may not be.
 <ol type="i">
<li> Compute the coefficient \(c\) and the function \(f(\k)\). Write your answer in terms of an integral over the Fermi surface. 
</li>
<li> Compute the coefficient \(c\) and function \(f(\k)\) for the dispersion \(\epsilon_{\k} = \k^2/2m\) in \(d=3\).
</li>
<li> Compute the coefficient \(c\) and function \(f(\k)\) for the dispersion \(\epsilon_{\k} = \k^2/2m\) in \(d=2\). 
</li>
<li> Compute the coefficient \(c\) and function \(f(\k)\) for the dispersion \(\epsilon_{\k} = -2t(\cos(k_xa) + \cos(k_ya))\). Does your answer differ from (d) iii.?
</li></ol>
</li></ol>

Thus, prove that 

\(\)\chi(\q,i\omega) \approx \(\)

<div class="answerBox"> 
 <button onclick="myFunction('answer708')" class="answerButton">Show Answer</button> 
 <div  id='answer708' class="answer" >
The definition of the Lindhard function is 

\(\)\chi_0(k) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega}\(\)

<ol type="a">
<li> The 
<ol type="i">
<li> When \(k = (\k,i\omega) \to 0\), we can easily set \(\omega = 0\) to get 

\(\)\chi_0(\k,0) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q}}\(\)

Now to set \(\k\to 0\), we need to take the limit because we have a 0/0 form. For this, we let \(\xi_{\q} = \xi_{\k+\q} + \eta\), where \(\eta\) is some small number. This gives us 

$$\begin{align}
\chi_0(\k\to0,0) ={}& -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q+\k} + \eta) - n_F(\xi_{\k+\q})}{\eta} \\
={}& -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q+\k}) + n_F'(\xi_{\q+\k})\eta - n_F(\xi_{\k+\q})}{\eta} \\
={}& -\frac{2}{N_s}\sum_{\q} n_F'(\xi_{\q+\k}) \\
={}& -\frac{2}{N_s}\sum_{\q} (-\delta(\xi_{\q+\k})) \\
={}& \frac{2}{N_s}\sum_{\q} \delta(\xi_{\q}) \\
={}& \frac{2}{N_s}\sum_{\q} \delta(\epsilon_{\q} - \epsilon_F) 
\end{align}$$

which is the definition of the density of states at the chemical potential (including the factor of 2 for spin). 


</li>
<li> Doing this gives us 

\(\)\rho(\epsilon) = \frac{\V}{N_s\pi^2} \frac{(2m)^{3/2}}{2}\sqrt{\epsilon}\(\)
</li></ol>

</li>
<li> 

<ol type="i">
<li> For this first part, we simply have 

\(\)\chi_0(-\k,i\omega) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{-\k+\q})}{\xi_{\q} - \xi_{-\k+\q} + i\omega}\(\)

Then, we swap the sign of \(\q\), which is ok because this is a dummy variable summing over the Brillouin zone:

\(\)\chi_0(-\k,i\omega) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{-\q}) - n_F(\xi_{-\k-\q})}{\xi_{-\q} - \xi_{-\k-\q} + i\omega}\(\)

Then, since the dispersion is even, we get 

\(\)\chi_0(-\k,i\omega) = -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega}\(\)

Thus \(\chi_0\) is even in \(\k\).

</li>
<li> This implies that there should be no linear terms. This is because ....

</li>
<li> To explicitly verify this, we compute the coefficient in the Taylor series. To do this, we could in principle evaluate the sum over the Brillouin zone exactly, and then Taylor expand. This is impossible in general, because although the Fermi functions simplify (we always take the zero temperature limit and replace them by Heaviside functions), it is still impossible to perform the integral because there are generically some horrible sine and cosine functions in the dispersion (at least for tight binding models). To get the coefficient, we therefore compute the derivative and then set \(\k=0\) and \(\omega = 0\). This gives us 

\(\)\frac{\partial}{\partial k_i} \chi(\k,i\omega) = -\frac{2}{N_s}\sum_{\q} \left[\frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{(\xi_{\q} - \xi_{\k+\q} + i\omega)^2} (\partial_i \xi)_{\k+\q} - \frac{n_F'(\xi_{\k+\q})(\partial_i \xi)_{\k+\q}}{\xi_{\q} - \xi_{\k+\q} + i\omega}\right]\(\)

Then, we set \(\omega = 0\). We also set \(\xi_{\q} = \xi_{\k+\q} + \eta\). Note that \(\eta\) is quite small here! This gives us 

$$\begin{align}
\frac{\partial}{\partial k_i} \chi(\k,0) ={}& -\frac{2}{N_s}\sum_{\q} \left[\frac{n_F(\xi_{\k+\q} + \eta) - n_F(\xi_{\k+\q})}{\eta^2} (\partial_i \xi)_{\k+\q} - \frac{n_F'(\xi_{\k+\q})(\partial_i \xi)_{\k+\q}}{\eta}\right] \\
={}& -\frac{2}{N_s}\sum_{\q} \left[\frac{n_F(\xi_{\k+\q}) + \eta n_F'(\xi_{\k+\q}) + \frac{\eta^2}{2} n_F"(\xi_{\k+\q}) - n_F(\xi_{\k+\q})}{\eta^2} - \frac{n_F'(\xi_{\k+\q})}{\eta}\right](\partial_i \xi)_{\k+\q} \\
={}& -\frac{2}{N_s}\sum_{\q} \left[\frac{n_F'(\xi_{\k+\q}) + \frac{\eta}{2} n_F"(\xi_{\k+\q})}{\eta} - \frac{n_F'(\xi_{\k+\q})}{\eta}\right](\partial_i \xi)_{\k+\q} \\
={}& -\frac{2}{N_s}\sum_{\q} \frac{1}{2} n_F"(\xi_{\k+\q})(\partial_i \xi)_{\k+\q}
\end{align}$$

Now we can take \(\k=0\) to get 

$$\begin{align}
\frac{\partial}{\partial k_i} \chi(0,0) ={}& -\frac{2}{N_s}\sum_{\q} \frac{1}{2} n_F"(\xi_{\q})(\partial_i \xi)_{\q}
\end{align}$$

Since \(\xi_{\q}\) is even, \((\partial_i \xi)_{\q}\) is odd. Thus, we can wrrite 

$$\begin{align}
\frac{\partial}{\partial k_i} \chi(0,0) ={}& -\frac{1}{2N_s}\sum_{\q} (n_F"(\xi_{\q})(\partial_i \xi)_{\q} + n_F"(\xi_{-\q})(\partial_i \xi)_{-\q}) \\
={}& -\frac{1}{2N_s}\sum_{\q} (n_F"(\xi_{\q})(\partial_i \xi)_{\q} - n_F"(\xi_{\q})(\partial_i \xi)_{\q}) \\
={}& 0
\end{align}$$

</li></ol>

</li>
<li> For this part, we will need to compute the second derivative of the Lindhard function. We get 

$$\begin{align}
\frac{\partial}{\partial k_i}\frac{\partial}{\partial k_j}\chi_0(\k,i\omega) ={}& -\frac{2}{N_s}\sum_{\q}\left[2\frac{n_F(\xi_{\q}) - n_F(\xi_{\q+\k})}{(\xi_{\q} - \xi_{\q+\k} + i\omega)^3} (\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k} - \frac{n_F'(\xi_{\k+\q})(\partial_i\xi)_{\q+\k}(\partial_j\xi)_{\q+\k}}{(\xi_{\q} - \xi_{\q+\k} + i\omega)^2} \right. \\
&+ \frac{n_F(\xi_{\q}) - n_F(\xi_{\q+\k})}{(\xi_{\q} - \xi_{\q+\k} + i\omega)^2}(\partial_i\partial_j\xi)_{\q+\k} - \frac{n_F'(\xi_{\q+\k})(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k}}{(\xi_{\q} - \xi_{\q+\k} + i\omega)^2} \\
&\left. - \frac{n_F"(\xi_{\q+\k})(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k}}{\xi_{\q} - \xi_{\q+\k} + i\omega} - \frac{n_F'(\xi_{\q+\k})(\partial_i \partial_j \xi)_{\q+\k}}{\xi_{\q} - \xi_{\q+\k} + i\omega}\right]
\end{align}$$

This simplifies a tiny but because two of the terms are the same; 

$$\begin{align}
\frac{\partial}{\partial k_i}\frac{\partial}{\partial k_j}\chi_0(\k,i\omega) ={}& -\frac{2}{N_s}\sum_{\q}\left[\left(\frac{n_F(\xi_{\q}) - n_F(\xi_{\q+\k})}{(\xi_{\q} - \xi_{\q+\k} + i\omega)^2} - \frac{n_F'(\xi_{\q+\k})}{\xi_{\q} - \xi_{\q+\k} + i\omega}\right)(\partial_i \partial_j \xi)_{\q+\k} \right. \\
&+ \left(2\frac{n_F(\xi_{\q}) - n_F(\xi_{\q+\k})}{(\xi_{\q} - \xi_{\q+\k} + i\omega)^3} - 2\frac{n_F'(\xi_{\q+\k})}{(\xi_{\q} - \xi_{\q+\k} + i\omega)^2} \right. \\
&\left. \left. - \frac{n_F"(\xi_{\q+\k})}{\xi_{\q} - \xi_{\q+\k} + i\omega} \right)(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k} \right]
\end{align}$$

<ol type="i">
<li> Now, to set \(\k\to 0\), we again let \(\xi_{\q} = \xi_{\q+\k} + \eta\). We also let \(\omega = 0\). This gives us 

$$\begin{align}
\frac{\partial}{\partial k_i}\frac{\partial}{\partial k_j}\chi_0(\k,i\omega) ={}& -\frac{2}{N_s}\sum_{\q}\left[\left(\frac{n_F(\xi_{\q+\k}) + \eta n_F'(\xi_{\q+\k}) + \frac{\eta^2}{2}n_F"(\xi_{\q+\k}) - n_F(\xi_{\q+\k})}{\eta^2} - \frac{n_F'(\xi_{\q+\k})}{\eta}\right)(\partial_i \partial_j \xi)_{\q+\k} \right. \\
&+ \left(2\frac{n_F(\xi_{\q+\k}) + \eta n_F'(\xi_{\q+\k}) + \frac{\eta^2}{2} n_F"(\xi_{\q+\k}) + \frac{\eta^3}{6} n_F"'(\xi_{\q+\k}) - n_F(\xi_{\q+\k})}{\eta^3}\right. \\
&\left. \left. - 2\frac{n_F'(\xi_{\q+\k})}{\eta^2} - \frac{n_F"(\xi_{\q+\k})}{\eta} \right)(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k} \right] \\
={}& -\frac{2}{N_s}\sum_{\q}\left[\left(\frac{n_F'(\xi_{\q+\k}) + \frac{\eta}{2}n_F"(\xi_{\q+\k})}{\eta} - \frac{n_F'(\xi_{\q+\k})}{\eta}\right)(\partial_i \partial_j \xi)_{\q+\k} \right. \\
&+ \left(2\frac{n_F'(\xi_{\q+\k}) + \frac{\eta}{2} n_F"(\xi_{\q+\k}) + \frac{\eta^2}{6} n_F"'(\xi_{\q+\k})}{\eta^2}\right. \\
&\left. \left. - 2\frac{n_F'(\xi_{\q+\k})}{\eta^2} - \frac{n_F"(\xi_{\q+\k})}{\eta} \right)(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k} \right] \\
={}& -\frac{2}{N_s}\sum_{\q}\left[\frac{1}{2}n_F"(\xi_{\q+\k})(\partial_i \partial_j \xi)_{\q+\k} \right. \\
&+ \left(\frac{n_F"(\xi_{\q+\k}) + \frac{\eta}{3} n_F"'(\xi_{\q+\k})}{\eta} \left. - \frac{n_F"(\xi_{\q+\k})}{\eta} \right)(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k} \right] \\
={}& -\frac{2}{N_s}\sum_{\q}\left[\frac{1}{2}n_F"(\xi_{\q+\k})(\partial_i \partial_j \xi)_{\q+\k} \right. \\
&+ \left. \left(\frac{\frac{\eta}{3} n_F"'(\xi_{\q+\k})}{\eta} \right)(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k} \right] \\
={}& -\frac{2}{N_s}\sum_{\q}\left[\frac{1}{2}n_F"(\xi_{\q+\k})(\partial_i \partial_j \xi)_{\q+\k} +\frac{1}{3} n_F"'(\xi_{\q+\k})(\partial_i \xi)_{\q+\k} (\partial_j \xi)_{\q+\k} \right]
\end{align}$$

We can finally set \(\k = 0\) to get 

$$\begin{align}
\frac{\partial}{\partial k_i}\frac{\partial}{\partial k_j}\chi_0(0,0) ={}& -\frac{2}{N_s}\sum_{\q}\left[\frac{1}{2}n_F"(\xi_{\q})(\partial_i \partial_j \xi)_{\q} +\frac{1}{3} n_F"'(\xi_{\q})(\partial_i \xi)_{\q} (\partial_j \xi)_{\q} \right]
\end{align}$$

This tells us that

\(\)\alpha_{ij} = -\frac{1}{N_s}\sum_{\q}\left[\frac{1}{2}n_F"(\xi_{\q})(\partial_i \partial_j \xi)_{\q} +\frac{1}{3} n_F"'(\xi_{\q})(\partial_i \xi)_{\q} (\partial_j \xi)_{\q} \right]\(\)

where we have an additional factor of 1/2 because of the Taylor expansion formula. Next, to write this in terms of a single derivative of the Fermi function, we have that 

\(\)\lim_{\beta\to\infty} n_F'(x) = -\delta(x)\(\)

then we simply get 

\(\)\lim_{\beta\to\infty} n_F"(x) = -\delta'(x), \quad \lim_{\beta\to\infty} n_F"'(x) = -\delta"(x)\(\)

Plugging this in, we find 

\(\)\alpha_{ij} = \frac{1}{N_s}\sum_{\q}\left[\frac{1}{2}\delta'(\xi_{\q})(\partial_i \partial_j \xi)_{\q} +\frac{1}{3} \delta"(\xi_{\q})(\partial_i \xi)_{\q} (\partial_j \xi)_{\q} \right]\(\)

To write this as an integral over the Fermi surface, we change the sum to an integral:

\(\)\alpha_{ij} = \frac{\V}{N_s}\int\left[\frac{1}{2}\delta'(\xi_{\q})(\partial_i \partial_j \xi)_{\q} +\frac{1}{3} \delta"(\xi_{\q})(\partial_i \xi)_{\q} (\partial_j \xi)_{\q} \right]\frac{\d^d\q}{(2\pi)^d}\(\)

Using the typical formula 

\(\)\d^d\q = \d q_\perp \d S = \frac{\d\xi_{\q}}{|\nabla\xi_{\q}|} \d S\(\)

we get 

$$\begin{align}
\alpha_{ij} ={}& \frac{\V}{N_s}\int\left[\frac{1}{2}\delta'(\xi_{\q})(\partial_i \partial_j \xi)_{\q} +\frac{1}{3} \delta"(\xi_{\q})(\partial_i \xi)_{\q} (\partial_j \xi)_{\q} \right]\frac{\d \xi_{\q} \d S}{|\nabla\xi_{\q}|(2\pi)^d} \\
={}& \frac{\V}{N_s}\int_\text{FS}\left[-\frac{1}{2}\frac{\partial}{\partial \xi_{\q}}\left(\frac{(\partial_i \partial_j \xi)_{\q}}{|\nabla\xi_{\q}|}\right) +\frac{1}{3}\frac{\partial^2}{\partial \xi_{\q}^2}\left(\frac{(\partial_i \xi)_{\q} (\partial_j \xi)_{\q}}{|\nabla\xi_{\q}|}\right) \right]\frac{\d S}{(2\pi)^d}
\end{align}$$

</li>
<li> To evaluate this for the spherical Fermi surface, we have 

\(\)\partial_i \partial_j \xi_{\q} = \frac{\delta_{ij}}{m}, \quad \partial_i \xi_{\q} \partial_j \xi_{\q} = \frac{q_i q_j}{m^2}, \quad \nabla \xi_{\q} = \frac{\q}{m}, \quad |\nabla \xi_{\q}| = \frac{q}{m}\(\)

$$\begin{align}
\alpha_{ij} ={}& \frac{\V}{N_s}\int_\text{FS}\left[-\frac{1}{2}\frac{\partial}{\partial \xi_{\q}}\left(\frac{\delta_{ij}/m}{q/m}\right) +\frac{1}{3}\frac{\partial^2}{\partial \xi_{\q}^2}\left(\frac{q_i q_j/m^2}{q/m}\right) \right]\frac{\d S}{(2\pi)^3} \\
={}& \frac{\V}{N_s}\int_\text{FS}\left[-\frac{1}{2}\frac{\partial}{\partial \xi_{\q}}\left(\frac{\delta_{ij}}{q}\right) +\frac{1}{3}\frac{\partial^2}{\partial \xi_{\q}^2}\left(\frac{q_i q_j}{mq}\right) \right]\frac{\d S}{(2\pi)^3}
\end{align}$$

Now, we write \(q_1 = q\cos\varphi\sin\theta\), \(q_2 = q\sin\varphi\sin\theta\), and \(q_3 = q\cos\theta\), which can be summarized as \(q_i = q n_i\). We also note that, since \(\epsilon_{\q} = q^2/2m\), we can compute \(q\) derivatives instead of energy ones:

\(\)\frac{\partial}{\partial\epsilon_{\q}} = \frac{\partial q}{\partial\epsilon_{\q}} \frac{\partial}{\partial q} = \frac{m}{q}\frac{\partial}{\partial q}\(\)

$$\begin{align}
\alpha_{ij} ={}& \frac{\V}{N_s}\int_\text{FS}\left[-\frac{m}{2q}\frac{\partial}{\partial q}\left(\frac{\delta_{ij}}{q}\right) +\frac{1}{3}\frac{m}{q}\frac{\partial}{\partial q}\left(\frac{m}{q}\frac{\partial}{\partial q}\right)\left(\frac{q n_i n_j}{m}\right) \right]\frac{\d S}{(2\pi)^3} \\
={}& \frac{\V}{N_s}\int_\text{FS}\left[\frac{m}{2q}\left(\frac{\delta_{ij}}{q^2}\right) +\frac{1}{3}\frac{m}{q}\frac{\partial}{\partial q}\left(\frac{n_i n_j}{q}\right) \right]\frac{\d S}{(2\pi)^3} \\
={}& \frac{\V}{N_s}\int_\text{FS}\left[\frac{m}{2q}\left(\frac{\delta_{ij}}{q^2}\right) - \frac{1}{3}\frac{m}{q}\left(\frac{n_i n_j}{q^2}\right) \right]\frac{\d S}{(2\pi)^3} \\
={}& \frac{\V}{N_s}\int_\text{FS}\frac{m}{q^3}\left[\frac{1}{2}\delta_{ij} - \frac{1}{3}n_i n_j \right]\frac{\d S}{(2\pi)^3}
\end{align}$$

Then we can evaluate the integral to get 
$$\begin{align}
\alpha_{ij} ={}& \frac{\V}{N_s}\frac{m}{k_F^3}\left(\frac{1}{2}(4\pi k_F^2) - \frac{1}{3}\frac{4\pi k_F^2}{3}\right)\frac{1}{(2\pi)^3} \\
={}& \frac{\pi^2 \rho(\epsilon_F)}{mk_F}\frac{m}{k_F^3}\left(\frac{1}{2}(4\pi k_F^2) - \frac{1}{3}\frac{4\pi k_F^2}{3}\right)\frac{1}{(2\pi)^3} \\
={}& \frac{\rho(\epsilon_F)}{mk_F^2}\frac{m}{3}\frac{1}{6} \\
\end{align}$$

</li>
<li> 
</li>
<li> For the tight-binding model, we compute the derivatives to be:

$$\begin{align}
\partial_i \epsilon_{\k} ={}& 2ta\sin(k_ia) \\
\partial_i \partial_j \epsilon_{\k} ={}& -2ta^2\delta_{ij}\cos(k_ia) \\
|\nabla\epsilon_{\k}| ={}& 2ta\sqrt{\sin^2(k_xa) + \sin^2(k_ya)}
\end{align}$$

We need to later compute derivatives of these with respect to \(\epsilon_{\q}\). This is somewhat difficult! 

$$\begin{align}
\frac{\partial}{\partial \epsilon_{\k}} f(k_x,k_y) ={}& \frac{\partial f}{\partial k_x} \left(\frac{\partial k_x}{\partial \epsilon_{\k}}\right)_{k_y} + \frac{\partial f}{\partial k_y} \left(\frac{\partial k_y}{\partial \epsilon_{\k}}\right)_{k_x} \\
={}& \frac{1}{2ta\sin(k_xa)}\frac{\partial f}{\partial k_x} + \frac{1}{2ta\sin(k_ya)}\frac{\partial f}{\partial k_y} 
\end{align}$$

Thus, 

\(\)\frac{\partial}{\partial \epsilon_{\k}} = \frac{1}{2ta\sin(k_xa)}\frac{\partial}{\partial k_x} + \frac{1}{2ta\sin(k_ya)}\frac{\partial}{\partial k_y}\(\)

The functions we need to differentiate of are 

$$\begin{align}
\frac{(\partial_i \partial_j \xi)_{\q}}{|\nabla\xi_{\q}|} ={}& \frac{-2ta^2\delta_{ij}\cos(q_ia)}{2ta\sqrt{\sin^2(q_xa) + \sin^2(q_ya)}} \\
={}& \frac{-a\delta_{ij}\cos(q_ia)}{\sqrt{\sin^2(q_xa) + \sin^2(q_ya)}} \\
\frac{(\partial_i \xi)_{\q} (\partial_j \xi)_{\q}}{|\nabla\xi_{\q}|} ={}& \frac{4t^2a^2\sin(k_ia)\sin(k_ja)}{2ta\sqrt{\sin^2(k_xa) + \sin^2(k_ya)}} \\
={}& \frac{2ta\sin(k_ia)\sin(k_ja)}{\sqrt{\sin^2(k_xa) + \sin^2(k_ya)}}
\end{align}$$

The derivatives are 

$$\begin{align}
\frac{\partial}{\partial \epsilon_{\k}}\frac{(\partial_i \partial_j \xi)_{\q}}{|\nabla\xi_{\q}|} ={}& \frac{a\delta_{ij}}{2t}\left(\frac{1}{\sqrt{\sin^2(q_xa) + \sin^2(q_ya)}} - \frac{\cos(q_ia)\epsilon_{\q}}{2t(\sin^2(q_xa) + \sin^2(q_ya))^{3/2}}\right) \\
={}& 
\end{align}$$

Plugging this in, we get 

$$\begin{align}
\alpha_{ij} ={}& \frac{\V}{N_s}\int_\text{FS}\left[-\frac{1}{2}\frac{\partial}{\partial \xi_{\q}}\left(\frac{(\partial_i \partial_j \xi)_{\q}}{|\nabla\xi_{\q}|}\right) +\frac{1}{3}\frac{\partial^2}{\partial \xi_{\q}^2}\left(\frac{(\partial_i \xi)_{\q} (\partial_j \xi)_{\q}}{|\nabla\xi_{\q}|}\right) \right]\frac{\d S}{(2\pi)^2}
\end{align}$$

FILL IN STEPS

Now that this integrand is in terms of \(k_x, k_y\), we need to figure out a way to rewrite the differential element, such that we parameterize the Fermi surface. Parameterizing the Fermi surface is not so easy. One way to parameterize the Fermi surface is through some angle. 

Can WE WRITE THIS LIKE SOME KIND OF LINE INTEGRALLLL?? 
</li></ol>
</li></ol>








</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Evaluate the Lindhard function for a simple cubic lattice, 

\(\)\xi_{\k} = -2t(\cos(k_xa) + \cos(k_ya) + \cos(k_za)) - \mu\(\)

in the limit of small \(k\), and small \(|\omega|/|k|\). 

<div class="answerBox"> 
 <button onclick="myFunction('answer949')" class="answerButton">Show Answer</button> 
 <div  id='answer949' class="answer" >


</div> 
 </div>


</div> </li></ol>

