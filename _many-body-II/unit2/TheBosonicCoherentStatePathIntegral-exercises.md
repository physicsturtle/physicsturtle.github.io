---
layout: exercises
title: The Bosonic Coherent State Path Integral  - Exercises
dept: physics
course: many-body-II
unit: unit2
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise">  In this problem, we will derive the expression for the coherent state for bosons. This state is an eigenstate of the boson annihilation operator, and so satisfies

\(\)\bhat\ket{z} = z\ket{z}.\(\)

It must also satisfy that \(\bra{z}\ket{z} = 1\). Using these two properties, derive an expression for the boson coherent state in terms of the basis \(\ket{n}\) signifying \(n\) particles in a particular state. 

<div class="answerBox"> 
 <button onclick="myFunction('answer7')" class="answerButton">Show Answer</button> 
 <div  id='answer7' class="answer" >
As a first step, we will write
\(\)\ket{z} = \sum_{n=0}^\infty a_{nz}\ket{n}.\(\)
Our goal is to calculate \(a_{nz}\) such that \(\ket{z}\) satisfies the above two conditions. Our first step is to recast the two conditions into constraints on the coefficients \(a_{nz}\). Using the eigenstate condition, we find that 

$$\begin{align}
\bhat\ket{z} ={}& \bhat\sum_{n=0}^\infty a_{nz}\ket{n} \\
={}& \sum_{n=0}^\infty a_{nz}\sqrt{n}\ket{n-1} \\
={}& \sum_{n=1}^\infty a_{nz}\sqrt{n}\ket{n-1} \\
z\sum_{n=0}^\infty a_{nz}\ket{n} ={}& \sum_{n=0}^\infty a_{n+1,z}\sqrt{n+1}\ket{n}
\end{align}$$

and by matching coefficients, we find that 

\(\)za_{nz} = \sqrt{n+1}a_{n+1,z}\(\)

which gives us a recursion relation capturing the first constraint on our coefficients: 

\(\)\frac{a_{n+1,z}}{a_{nz}} = \frac{z}{\sqrt{n+1}}.\(\)

The second constraint of normalization simply yields that 

\(\)\sum_{n=0}^\infty \|a_{nz}\|^2 = 1.\(\)

Equipped with these constraints, we start by solving the recursion relation, which gives 

\(\)a_{nz} = \frac{z^n}{\sqrt{n!}}a_{0z}.\(\)

Now plugging this into the normalization condition, we find that 

\(\)\sum_{n=0}^\infty \frac{\|z\|^{2n}}{n!}\|a_{0z}\|^2 = 1 = e^{\|z\|^2}\(\)

and find that 

\(\)a_{0z} = e^{-\|z\|^2/2}.\(\)

Lastly, we write 

$$\begin{align}
\ket{z} ={}& e^{-\|z\|^2/2} \sum_{n=0}^\infty \frac{z^n}{\sqrt{n!}}\ket{n} \\
={}& e^{-\|z\|^2/2}\sum_{n=0}^\infty \frac{z^n}{n!} \sqrt{n!}\ket{n} \\
={}& e^{-\|z\|^2/2}\sum_{n=0}^\infty \frac{z^n}{n!} (\bhat^\dagger)^n \ket{0} \\
={}& e^{-\|z\|^2/2} e^{z\bhat^\dagger}\ket{0}
\end{align}$$

</div> 
 </div>

</div> </li></ol>

