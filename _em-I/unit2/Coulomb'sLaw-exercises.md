---
layout: exercises
title: Coulomb's Law  - Exercises
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise">  Consider 8 point charges, each of charge \(q\), at the vertices of a cube of side length \(2a\) centred at the origin. Calculate the electric field at a point \((0,0,z)\). 

<div class="answerBox"> 
 <button onclick="myFunction('answer3')" class="answerButton">Show Answer</button> 
 <div  id='answer3' class="answer" >
We can apply symmetry here. The \(x\) and \(y\) components of the electric fields will be zero, so we only need to calculate the \(z\) component. First, let's get the contribution from the charges at \((a,a,a),(-a,a,a),(a,-a,a),\) and \((-a,-a,a)\). The magnitude of electric field due to the charge at \((a,a,a)\) is 

$$\begin{equation}
E_\text{top} = \frac{q}{4\pi\epsilon_0r_\text{top}}
\end{equation}$$

and the unit vector is \(\rhat_\text{top} = (a,a,z-a)/\sqrt{2a^2+(z-a)^2}\). Thus, the electric field from both the top and bottom charges is (the bottom ones are easy to construct once the top contribution is done)

$$\begin{equation}
\mathbf{E} = \frac{q(z-a)\zhat}{\pi\epsilon_0(2a^2+(z-a)^2)^{3/2}} + \frac{q(z+a)\zhat}{\pi\epsilon_0(2a^2+(z+a)^2)^{3/2}}
\end{equation}$$

</div> 
 </div>


</div> </li></ol>

