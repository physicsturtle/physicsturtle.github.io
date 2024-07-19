---
layout: exercises
title: Schrodinger equation with spin-orbit coupling  - Exercises
dept: physics
course: cmp-I
unit: unit4
deptDisplay: Physics
courseDisplay: Condensed Matter Physics I
unitDisplay: Unit 4
---
<ol>
<li> <div class="exercise">  Consider the case when \(U(\x) = -\frac{e^2}{4\pi\epsilon_0\|\x\|}\), which is the Coulomb potential. Show that the spin-orbit coupling we find from the Dirac equation agrees with the one we often use in undergraduate quantum mechanics. 

<div class="answerBox"> 
 <button onclick="myFunction('answer3')" class="answerButton">Show Answer</button> 
 <div  id='answer3' class="answer" >
We compute 

\(\)\nabla U(\x) = \frac{e^2}{4\pi\epsilon_0 r^2}\rhat = \frac{e^2}{4\pi\epsilon_0 r^3}\x\(\)

Then, can use the fact that \(\hat{\mathbf{L}} = \hat{\x}\times\hat{\p}\), and then get that 

$$\begin{align}
\Hhat_\text{SOC} ={}& \frac{\hbar}{4m^2c^2}\boldsymbol{\sigma}\cdot\left(\frac{e^2}{4\pi\epsilon_0r^3}\hat{\mathbf{L}}\right) \\
={}& \frac{e^2}{8\pi m^2c^2\epsilon_0r^3} \hat{\mathbf{S}}\cdot\hat{\mathbf{L}}
\end{align}$$

where we have set \(\mathbf{S} = \hbar\boldsymbol{\sigma}/2\). This agrees with the standard expression from undergraduate quantum mechanics!
</div> 
 </div>

</div> </li></ol>

