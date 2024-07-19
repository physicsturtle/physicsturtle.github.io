---
layout: lesson
title: Non-Normalizable Wave Functions - Exercises
dept: physics
course: qm-I
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 2
---

<ol>
<li> <div class="exercise"> Let $\alpha$ be a real constant. Normalize the wave function $$\psi_k(x) = A\left(e^{ikx} + \alpha e^{-ikx}\right)$$ in the $k$ scale by finding the value of $A$.
<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
We recall the normalization condition 
$$\int_{-\infty}^\infty \psi^*_k(x) \int_{k - \Delta k}^{k + \Delta k} \psi_{k'}(x) dk' dx = 1.$$
First, we compute the inner integral by plugging in $\psi_{k'}(x) = A\left(e^{ik'x} + \alpha e^{-ik'x}\right)$:
\begin{eqnarray*}
\int_{k-\Delta k}^{k+\Delta k} A\left(e^{ik'x} + \alpha e^{-ik'x}\right) dk' &=& \frac{1}{ix}\left(e^{ik'x} - \alpha e^{-ik'x}\right)\bigg|^{k+\Delta k}_{k - \Delta k}\\
&=& \frac{A}{ix}\left(e^{i(k+\Delta k)x} - e^{i(k-\Delta k)x} - \alpha e^{-i(k+\Delta k)x} + \alpha e^{-i(k-\Delta k)x}\right)\\
&=& \frac{A}{ix}\left(e^{ikx}\left(e^{ix\Delta k} - e^{-ix\Delta k}\right) + \alpha e^{-ikx}\left(e^{ix\Delta k} - e^{-ix\Delta k}\right)\right)\\
&=& \frac{2A}{x}\left(e^{ikx}\sin(x\Delta k) + \alpha e^{-ikx}\sin(x\Delta k)\right)\\
&=& \frac{2A\sin(x\Delta k)}{x}\left(e^{ikx} + \alpha e^{-ikx}\right)
\end{eqnarray*}

With this formula, we can plug it into the normalization condition and evaluate

\begin{eqnarray*}
1 &=& \int_{-\infty}^\infty \psi^*_k(x)\left[\frac{2A\sin(x\Delta k)}{x}\left(e^{ikx} + \alpha e^{-ikx}\right)\right] dx \\
&=&  \int_{-\infty}^\infty A\left[e^{-ikx} + \alpha e^{ikx}\right]\left[\frac{2A\sin(x\Delta k)}{x}\left(e^{ikx} + \alpha e^{-ikx}\right)\right] dx \\
&=& A^2 \int_{-\infty}^\infty \frac{2\sin(x\Delta k)}{x}\left(1+\alpha \left(e^{2ikx} + e^{-2ikx}\right)+\alpha^2\right) dx \\
&=& 2A^2 \int_{-\infty}^\infty \frac{\sin(x\Delta k)}{x}\left(1+ 2\alpha \cos(2kx)+\alpha^2\right) dx \\
&=& 2A^2\left[ \int_{-\infty}^\infty \frac{(1+\alpha^2)\sin(x\Delta k)}{x}dx + \int_{-\infty}^\infty 2\alpha \frac{\sin(x\Delta k)\cos(2kx)}{x} dx \right]\\
&=& 2A^2\left[ (1+\alpha^2)\int_{-\infty}^\infty \frac{\sin(y)}{y}dy + 2\alpha\int_{-\infty}^\infty  \frac{\sin((\Delta k + 2k)x) + \sin((\Delta k - 2k)x)}{x} dx \right]\\
&=& 2A^2\left[ (1+\alpha^2)\pi + 2\alpha\left(\int_{-\infty}^\infty  \frac{\sin((\Delta k + 2k)x)}{x}dx + \int_{-\infty}^\infty \frac{\sin((\Delta k - 2k)x)}{x} dx\right) \right]\\
&=& 2A^2\left[ (1+\alpha^2)\pi + 2\alpha\left(\int_{-\infty}^\infty  \frac{\sin(y)}{y}dy + \int_{-\infty}^\infty \frac{\sin(y)}{y} dy\right) \right]\\
&=& 2A^2\left[ (1+\alpha^2)\pi + 2\alpha \pi \right]\\
&=& 2A^2\pi(1+2\alpha + \alpha^2)\\
1 &=& 2A^2(1+\alpha)^2
\end{eqnarray*}

Setting this to be equal to 1, we finally find that 

$$A = \frac{1}{\sqrt{2\pi}|1+\alpha|}.$$

Thus the normalized wave function is 

$$\psi_k(x) = \frac{1}{\sqrt{2\pi}|1+\alpha|} \left(e^{ikx} + \alpha e^{-ikx}\right).$$
</div>
</div>
</div>
</li>



<li> (find the tunneling wave function first) Normalize the wave function which has a continuum part and a tunneling part.


</li>

<li> 
asdf


</li>


</ol>
