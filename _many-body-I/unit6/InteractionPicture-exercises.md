---
layout: exercises
title: Interaction Picture  - Exercises
dept: physics
course: many-body-I
unit: unit6
deptDisplay: Physics
courseDisplay: Many Body Physics I
unitDisplay: Unit 6
---
<ol>
<li> <div class="exercise">  Consider the fermionic Hamiltonian
\(\)\hat{H}_0 = \sum_{\k\sigma} \xi_{\k} \chat^\dagger_{\k\sigma} \chat_{\k\sigma}.\(\)

Explicitly calculate the interaction picture operator \(\chat_{\k\sigma,I}(t)\).

<div class="answerBox"> 
 <button onclick="myFunction('answer6')" class="answerButton">Show Answer</button> 
 <div  id='answer6' class="answer" >
To do this, we first consider the definition of the interaction picture operator, which is 

\(\)\chat_{\k\sigma,I}(t) = e^{i\hat{H}_0t/\hbar} \chat_{\k\sigma} e^{-i\hat{H}_0t/\hbar}.\(\)

We now apply the Baker-Campbell-Hausdorff formula to get 

\(\)\chat_{\k\sigma,I}(t) = \chat_{\k\sigma} + \frac{it}{\hbar}[\hat{H}_0, \chat_{\k\sigma}] + \frac{1}{2} \left(\frac{it}{\hbar}\right)^2[\hat{H}_0,[\hat{H}_0,\chat_{\k\sigma}]] + \cdots\(\)

Let's first calculate the commutator \([\hat{H}_0,\chat_{\k\sigma}]\). 

$$\begin{align}
[\hat{H}_0,\chat_{\k\sigma}] ={}& \left[\sum_{\k'\sigma'}\xi_{\k'} \chat^\dagger_{\k'\sigma'} \chat_{\k'\sigma'}, \chat_{\k\sigma}\right] \\
={}& \sum_{\k'\sigma'}\xi_{\k'}\left[ \chat^\dagger_{\k'\sigma'} \chat_{\k'\sigma'}, \chat_{\k\sigma}\right] \\
={}&  \sum_{\k'\sigma'}\xi_{\k'}\left( \chat^\dagger_{\k'\sigma'} \chat_{\k'\sigma'} \chat_{\k\sigma} - \chat_{\k\sigma} \chat^\dagger_{\k'\sigma'} \chat_{\k'\sigma'}\right) \\
={}& \sum_{\k'\sigma'}\xi_{\k'}\left(\chat^\dagger_{\k'\sigma'}\chat_{\k'\sigma'}\chat_{\k\sigma} - \left(-\chat^\dagger_{\k'\sigma'} \chat_{\k\sigma} + \delta_{\k\k'}\delta_{\sigma\sigma'}\right)\chat_{\k'\sigma'}\right)\\
={}&  \sum_{\k'\sigma'}\xi_{\k'}\left(\chat^\dagger_{\k'\sigma'}\left\{\chat_{\k'\sigma'}, \chat_{\k\sigma}\right\} - \delta_{\k\k'}\delta_{\sigma\sigma'}\chat_{\k'\sigma'}\right) \\
={}& -\xi_{\k} \chat_{\k\sigma}
\end{align}$$

This means it is actually easy to evaluate the series completely! This is so because if we have \(n\) nested commutators, for example, if \(n=2\), 

$$\begin{align}
[\hat{H}_0, [\hat{H}_0, \chat_{\k\sigma}]] ={}& [\hat{H}_0, -\xi_{\k} \chat_{\k\sigma} ]\\
={}& -\xi_{\k} [\hat{H}_0,\chat_{\k\sigma}] \\
={}& (-\xi_{\k})^2 \chat_{\k\sigma}
\end{align}$$

Thus, the series becomes 

$$\begin{align}
\chat_{\k\sigma,I}(t) ={}& \chat_{\k\sigma} + \frac{it}{\hbar}(-\xi_{\k})\chat_{\k\sigma} + \frac{1}{2}\left(\frac{it}{\hbar}\right)^2 (-\xi_{\k})^2 \chat_{\k\sigma} + \cdots \\
={}&  \chat_{\k\sigma}\sum_{n=0}^\infty \frac{1}{n!}\left(\frac{-it\xi_{\k}}{\hbar}\right)^n \\
={}& e^{-it\xi_{\k}/\hbar} \chat_{\k\sigma}
\end{align}$$


Similarly, one can show that 

\(\)\chat^\dagger_{\k\sigma,I}(t) = e^{it\xi_{\k}/\hbar} \chat^\dagger_{\k\sigma},\(\)

either by taking the Hermitian conjugate of our previous result, or by direct computation.
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Consider the following free bosonic Hamiltonian 

\(\)\hat{H}_0 = \sum_{\k} \xi_{\k} \bhat^\dagger_{\k} \bhat_{\k}.\(\)

Explicitly calculate the interaction picture operator \(\bhat_{\k,I}(t)\). 

<div class="answerBox"> 
 <button onclick="myFunction('answer56')" class="answerButton">Show Answer</button> 
 <div  id='answer56' class="answer" >
To do this, we first consider the definition of the interaction picture operator, which is 

\(\)\bhat_{\k,I}(t) = e^{i\Hhat_0 t/\hbar} \bhat_{\k} e^{-i\Hhat_0 t/\hbar}\(\)

We now apply the Baker-Campbell-Hausdorff formula to get 

\(\)\bhat_{\k,I}(t) = \bhat_{\k} + \frac{it}{\hbar}[\Hhat_0,\bhat_{\k}] + \frac{1}{2}\left(\frac{it}{\hbar}\right)^2[\Hhat_0,[\Hhat_0,\bhat_{\k}]] + \cdots\(\)

Let's first compute the commutator \([\Hhat_0, \bhat_{\k}]\). We find 

$$\begin{align}
[\Hhat_0, \bhat_{\k}] ={}& \left[\sum_{\k'} \xi_{\k'} \bhat^\dagger_{\k'}\bhat_{\k'}, \bhat_{\k}\right] \\
={}& \sum_{\k'} \xi_{\k'} [\bhat^\dagger_{\k'}, \bhat_{\k}]\bhat_{\k'} \\
={}& \sum_{\k'} \xi_{\k'} (-\delta_{\k\k'}) \bhat_{\k'} \\
={}& -\xi_{\k} \bhat_{\k}
\end{align}$$

Thus we see that 

$$\begin{align}
\bhat_{\k,I}(t) ={}& \bhat_{\k}  \frac{it\xi_{\k}}{\hbar}\bhat_{\k} + \frac{1}{2}\left(\frac{-\xi_{\k} it}{\hbar}\right)^2\bhat_{\k}+ \cdots \\
={}& \sum_{n=0}^\infty \frac{1}{n!}\left(-\frac{it\xi_{\k}}{\hbar}\right)^n \bhat_{\k} \\
={}& e^{-it\xi_{\k}/\hbar} \bhat_{\k}
\end{align}$$

From this, we also see that 

\(\)\bhat^\dagger_{\k,I}(t) = e^{it\xi_{\k}/\hbar} \bhat^\dagger_{\k}.\(\)

</div> 
 </div>


</div> </li></ol>

