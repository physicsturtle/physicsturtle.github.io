---
layout: exercises
title: Quantum harmonic oscillator II  - Exercises
dept: physics
course: qm-I
unit: unit3
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  Find the most probable value of momentum \(p\) in the first excited state of the quantum harmonic oscillator 

$$\begin{equation}
\psi_1(x) = Axe^{-x^2/2a^2}
\end{equation}$$

where \(a = \sqrt{\hbar/m\omega}\) is the characteristic length and \(A = \sqrt{2/(a^3\pi^{1/2})}\).

<div class="answerBox"> 
 <button onclick="myFunction('answer9')" class="answerButton">Show Answer</button> 
 <div  id='answer9' class="answer" >
We need to compute the momentum space wave function. To do this, we compute 

$$\begin{align}
\phi(p,t) ={}& \frac{1}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty Axe^{-x^2/2a^2} e^{-ipx/\hbar} \d x \\
={}& \frac{A}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty x\exp\left(-\frac{1}{2a^2}\left(x^2 + \frac{2a^2 ipx}{\hbar}\right)\right)\d x \\
={}& \frac{A}{\sqrt{2\pi\hbar}}\int_{-\infty}^\infty x \exp\left(-\frac{1}{2a^2}\left[\left(x + \frac{a^2 ip}{\hbar}\right)^2 - \left(\frac{a^2 ip}{\hbar}\right)^2\right]\right) \d x \\
={}& \frac{A}{\sqrt{2\pi\hbar}} \exp\left(\frac{a^2}{2}\left(\frac{ip}{\hbar}\right)^2\right) \int_{-\infty}^\infty x \exp\left(-\frac{1}{2a^2}\left(x + \frac{a^2 ip}{\hbar}\right)^2 \right) \d x \\
={}& \frac{A}{\sqrt{2\pi \hbar}} \exp\left(-\frac{p^2a^2}{2\hbar^2}\right)\int_{-\infty}^\infty \left(x - \frac{a^2 ip}{\hbar}\right) \exp\left(-\frac{x^2}{2a^2}\right) \d x \\
={}& \frac{A}{\sqrt{2\pi\hbar}}\exp\left(-\frac{p^2a^2}{2\hbar^2}\right)\int_{-\infty}^\infty \left(-\frac{a^2 ip}{\hbar}\right)\exp\left(-\frac{x^2}{2a^2}\right) \d\left(\frac{x}{\sqrt{2}a}\right) \sqrt{2}a \\
={}& \frac{A}{\sqrt{2\pi\hbar}}\exp\left(-\frac{p^2a^2}{2\hbar^2}\right)\sqrt{\pi} \left(-\frac{a^2 ip}{\hbar}\right)  \sqrt{2}a \\
={}& \frac{Aa}{\sqrt{\hbar}}\exp\left(-\frac{p^2a^2}{2\hbar^2}\right) \left(-\frac{a^2 ip}{\hbar}\right) \\
\end{align}$$

The probability density is then given by 

$$\begin{align}
|\phi(p)|^2 ={}& \frac{A^2a^6p^2}{\hbar^3}\exp\left(-\frac{p^2a^2}{2\hbar^2}\right) \\
={}& \frac{2a^3p^2}{\sqrt{\pi}\hbar^3}\exp\left(-\frac{p^2a^2}{2\hbar^2}\right) \\
\end{align}$$

To find the most probable value of momentum, we take the derivative of this expression with respect to \(p\). This gives us 

$$\begin{align}
\frac{\d}{\d p}|\phi(p)|^2 \propto & \left(2p - \frac{p^3a^2}{\hbar^2}\right)e^{-p^2a^2/2\hbar^2} 
\end{align}$$

Setting this to zero, we have either \(p = 0\) or \(p = \pm \sqrt{2}\hbar/a\). The maximum is clearly at \(p = \pm\sqrt{2}\hbar/a\) because \(|\phi(p=0)|^2 = 0\), which is not the maximum.

</div> 
 </div>

</div> </li></ol>

