---
layout: exercises
title: The Propagator  - Exercises
dept: physics
course: qm-V
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics V
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise">  For a free particle in one dimension, whose Hamiltonian is 

\(\)\Hhat = \frac{\phat^2}{2m}\(\)

compute the propagator \(K(x,t;x',0)\).

<div class="answerBox"> 
 <button onclick="myFunction('answer7')" class="answerButton">Show Answer</button> 
 <div  id='answer7' class="answer" >
We simply compute 

$$\begin{align}
\bra{x} e^{-i\phat t/2m\hbar} \ket{x'} =& \int_{-\infty}^\infty \bra{x} e^{-i\phat^2 t/2m\hbar} \ket{p}\bra{p} \ket{x'} \d p \\
=& \int_{-\infty}^\infty e^{-ip^2 t/2m\hbar}\bra{x}\ket{p}\bra{p}\ket{x'} \d p \\
=& \int_{-\infty}^\infty e^{-ip^2 t/2m\hbar} e^{ip(x-x')/\hbar} \frac{\d p}{2\pi\hbar}
\end{align}$$

Now, we complete the square. This allows us to evaluate the integral exactly 

$$\begin{align}
\bra{x} e^{-i\phat t/2m\hbar} \ket{x'} =& \int_{-\infty}^\infty \exp\left(-\frac{it}{2m\hbar}\left(p - m\frac{x-x'}{t}\right)^2\right) e^{im(x-x')^2/2m\hbar t} \frac{\d p}{2\pi\hbar} \\
=& e^{im(x-x')^2/2m\hbar t} \int_{-\infty}^\infty \exp\left(-\frac{it}{2m\hbar}p^2\right)  \frac{\d p}{2\pi\hbar} \\
=& \frac{e^{im(x-x')^2/2m\hbar t}}{2\pi\hbar} \sqrt{\frac{2m\hbar\pi}{it}} \\
=& e^{im(x-x')^2/2m\hbar t}\sqrt{\frac{m}{2\pi i\hbar t}}
\end{align}$$

</div> 
 </div>

</div> </li></ol>

