---
layout: exercises
title: Path Integral for a Fermionic Field Theory  - Exercises
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  The grand potential is defined by

\(\)\Omega = -\frac{1}{\beta}\log \mathcal{Z}\(\)

For the Hamiltonian 

\(\)\Hhat = \sum_{\k\sigma} \xi_{\k}\chat^\dagger_{\k\sigma} \chat_{\k\sigma}\(\)

<ol type="a">
<li> Compute the grand partition function by the standard way
</li>
<li> Compute the grand partition function with the path integral
</li>
<li> Use this information to get the normalization constant in the path integral. 
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer15')" class="answerButton">Show Answer</button> 
 <div  id='answer15' class="answer" >
<ol type="a">
<li> The grand partition function is (note that the Hamiltonian already includes the chemical potential in it here, so we do not need to add it in the definition of the grand partition function)

\(\)\mathcal{Z} = \tr e^{-\beta \Hhat}\(\)

We can rewrite this as 

$$\begin{align}
\mathcal{Z} ={}& \prod_{\k\sigma} \left(\sum_{n_{\k\sigma}=0,1} e^{-\beta n_{\k\sigma} \xi_{\k}}\right) \\
={}& \prod_{\k\sigma} (1 + e^{-\beta \xi_{\k}})
\end{align}$$

</li>
<li> The grand partition function in the path integral is given by 

\(\)\mathcal{Z} = \int e^{-S}\D[\bar{c},c]\(\)

the action can be written as 

\(\)S = \sum_{k\sigma} (-i\omega + \xi_{\k})\bar{c}_{k\sigma} c_{k\sigma}\(\)

where we pick up a Jacobian \(J\) when transforming to Matsubara frequency space. Then, we get 

$$\begin{align}
\mathcal{Z} ={}& J\prod_{\k\sigma} \int e^{(i\omega - \xi_{\k})\bar{c}_{k\sigma}c_{k\sigma}} \d \bar{c}_{k\sigma} \d c_{k\sigma} \\
={}& J\prod_{k\sigma} \int (1 + (i\omega - \xi_{\k})\bar{c}_{k\sigma}c_{k\sigma}) \d \bar{c}_{k\sigma} \d c_{k\sigma} \\
={}& J\prod_{k\sigma} (-i\omega + \xi_{\k})
\end{align}$$

Next, we need to evaluate the product over Matsubara frequencies. This gives us 

\(\)\prod_{i\omega}(-i\omega + \xi_{\k}) = \prod_{i\omega}(-i\omega)\left(1 - \frac{\xi_{\k}}{i\omega}\right)\(\)

We recall the infinite product identity 

\(\)\cos x = \prod_{n=1}^\infty \left[1-\frac{4x^2}{\pi^2(2n-1)^2)}\right]\(\)

then plugging in \(\omega_n = (2n-1)\pi/\beta\), we get 

$$\begin{align}
\prod_{i\omega}(-i\omega + \xi_{\k}) ={}& \prod_{n=1}^\infty\left(\frac{(2n-1)\pi}{\beta}\right)^2\prod_{n=1}^\infty\left(1 - \frac{i\beta\xi_{\k}}{\pi(2n-1)}\right)\left(1 + \frac{i\beta\xi_{\k}}{\pi(2n-1)}\right) \\
={}& \prod_{n=1}^\infty\left(\frac{(2n-1)\pi}{\beta}\right)^2\prod_{n=1}^\infty\left(1 - \frac{i^2\beta^2\xi_{\k}^2}{\pi^2(2n-1)^2}\right)
\end{align}$$

The second infinite product is \(\cos(i\beta \xi_{\k}/2) = \cosh(\beta\xi_{\k}/2)\). Thus, we get 

$$\begin{align}
\prod_{i\omega}(-i\omega + \xi_{\k}) ={}& \cosh\left(\frac{\beta\xi_{\k}}{2}\right)\prod_{n=1}^\infty\left(\frac{(2n-1)\pi}{\beta}\right)^2
\end{align}$$



</li>
<li> 
</li></ol>
</div> 
 </div>

</div> </li></ol>

