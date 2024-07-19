---
layout: exercises
title: Infinite square well  - Exercises
dept: physics
course: qm-I
unit: unit3
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  Consider the infinite square well on the interval \(-a\) to \(a\), which is defined by a potential

$$\begin{equation}
V(x) = \begin{cases}
0 & -a < x < a \\
\infty & \text{else}
\end{cases}.
\end{equation}$$

<ol type="a">
<li> Calculate the allowed energy levels and corresponding (normalized) wave functions.
</li>
<li> Show that the wave functions \(\psi_n(x)\) satisfy the relation
$$\begin{equation}
\int \psi_m^*(x) \psi_n(x) \d x = \delta_{mn}
\end{equation}$$
</li>
<li> Suppose a particle has wave function
$$\begin{equation}
\psi(x) = \begin{cases} 
A(a^2-x^2) & -a < x < a \\
0 & \text{else}
\end{cases}.
\end{equation}$$ 
<ol type="i">
<li> Normalize the wave function by calculating \(A\).
</li>
<li> If you measure the energy of the particle, what is the probability that you will find it in its \(n\)th energy eigenstate?
</li></ol>
</li></ol>

</div> </li>
<li> <div class="exercise">  Consider a particle in the \(n\)th energy eigenstate state of the infinite square well.
<ol type="a">
<li> Compute the momentum space eigenfunctions of 

$$\begin{equation}
\psi_n(x) = \sqrt{\frac{2}{a}}\sin\left(\frac{n\pi x}{a}\right)
\end{equation}$$

</li>
<li> Plot the probability distribution of a particle in the \(n\)th energy eigenstate in the infinite square well for \(n=1,2\) (using a computer).
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer40')" class="answerButton">Show Answer</button> 
 <div  id='answer40' class="answer" >
<ol type="a">
<li> 
We simply compute the Fourier transform 

$$\begin{align}
\psi_n(p) ={}& \int_{-\infty}^\infty \psi_n(x) e^{-ipx/\hbar} \frac{\d x}{\sqrt{2\pi\hbar}} \\
={}& \sqrt{\frac{2}{a}}\int_0^a e^{-ipx/\hbar}\frac{e^{in\pi x/a} - e^{-in\pi x/a}}{2i} \frac{\d x}{\sqrt{2\pi\hbar}} \\
={}& \frac{1}{2i\sqrt{\pi a\hbar}}\int_0^a\left(e^{ix(n\pi a/-p/\hbar)} - e^{-ix(n\pi/a+p/\hbar)}\right)\d x\\
={}& \frac{1}{2i\sqrt{\pi a\hbar}}\left(\frac{e^{ix(n\pi/a-p/\hbar)}}{i(n\pi/a-p/\hbar)}\bigg|_0^a + \frac{e^{-ix(n\pi/a+p/\hbar)}}{i(n\pi/a+p/\hbar)}\bigg|_0^a\right) \\
={}& \frac{1}{2i\sqrt{\pi a\hbar}}\left(\frac{e^{i(n\pi -pa/\hbar)}-1}{i(n\pi/a-p/\hbar)} + \frac{e^{-i(n\pi+pa/\hbar)}-1}{i(n\pi/a+p/\hbar)}\right) \\
={}& \frac{1}{2\sqrt{\pi a\hbar}}\left(\frac{1-(-1)^ne^{-ipa/\hbar}}{n\pi/a-p/\hbar} + \frac{1-(-1)^ne^{-ipa/\hbar}}{n\pi/a+p/\hbar}\right) \\
={}& \frac{1-(-1)^ne^{-ipa/\hbar}}{2\sqrt{\pi a\hbar}}\left(\frac{1}{n\pi/a-p/\hbar} + \frac{1}{n\pi/a+p/\hbar}\right) \\
={}& \frac{1-(-1)^ne^{-ipa/\hbar}}{2\sqrt{\pi a\hbar}}\frac{2n\pi/a}{(n\pi/a)^2-(p/\hbar)^2} \\
={}& \frac{1-(-1)^ne^{-ipa/\hbar}}{\sqrt{\pi a\hbar}}\frac{n\pi/a}{(n\pi/a)^2-(p/\hbar)^2} \\
={}& \frac{1-(-1)^ne^{-ipa/\hbar}}{(n\pi)^2-(pa/\hbar)^2}n\sqrt{\frac{\pi a}{\hbar}}
\end{align}$$

Then, we take the magnitude to find 

$$\begin{align}
|\psi_n(p)|^2 ={}& \frac{|1-(-1)^ne^{-ipa/\hbar}|^2}{((n\pi)^2-(pa/\hbar)^2)^2}\frac{\pi a n^2}{\hbar} \\
={}& \frac{2n^2\pi a/\hbar}{((n\pi)^2 - p^2a^2/\hbar^2)^2}(1-(-1)^n\cos(pa/\hbar))
\end{align}$$

</li>
<li> 
</li></ol>
</div> 
 </div>
</div> </li></ol>

