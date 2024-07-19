---
layout: exercises
title: Introductory Problems  - Exercises
dept: physics
course: cm-III
unit: unit3
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 3
---
<ol>
<li> <div class="exercise">  Consider the spherical pendulum, which consists of a massless rod of length \(\ell\) attached to a fixed point at \((0,0,0)\), and at the end of the rod is a mass \(m\). Determine the Lagrangian for this system.

<div class="answerBox"> 
 <button onclick="myFunction('answer3')" class="answerButton">Show Answer</button> 
 <div  id='answer3' class="answer" >
We can parameterize the coordinates of the particle by two variables, the angles \(\varphi\) and \(\theta\). This takes the form 

$$\begin{equation}
\begin{cases}
x = \ell \sin\theta \cos\varphi \\
y = \ell \sin\theta \sin\varphi \\
z = \ell \cos\theta
\end{cases}
\end{equation}$$

Thus, the time derivatives of each of these are 

$$\begin{equation}
\begin{cases}
\dot{x} = \ell(\dot{\theta}\cos\theta\cos\varphi - \dot{\varphi}\sin\theta\sin\varphi) \\
\dot{y} = \ell(\dot{\theta}\cos\theta\sin\varphi + \dot{\varphi}\sin\theta\cos\varphi) \\
\dot{z} = -\ell\dot{\theta}\sin\theta
\end{cases}
\end{equation}$$

Thus, the kinetic energy is given by 

$$\begin{align}
T ={}& \frac{m}{2}(\dot{x}^2 + \dot{y}^2 + \dot{z}^2) \\
={}& \frac{m}{2}\ell^2(\dot{\theta}^2\cos^2\theta\cos^2\varphi + \dot{\varphi}^2\sin^2\theta\sin^2\varphi + \dot{\theta}^2\cos^2\theta\sin^2\varphi + \dot{\varphi}^2\sin^2\theta\cos^2\varphi + \dot{\theta}^2\sin^2\theta) \\
={}& \frac{m}{2}\ell^2(\dot{\theta}^2\cos^2\theta + \dot{\theta}^2\sin^2\theta + \dot{\varphi}^2\sin^2\theta) \\
={}& \frac{1}{2}m\ell^2(\dot{\theta}^2 + \dot{\varphi}^2\sin^2\theta)
\end{align}$$

The potential energy is \(V = mgz\), and since \(z = \ell \cos\theta\), we have that \(V = mg\ell\cos\theta\). Thus, the Lagrangian is given by 

\(\)\L = \frac{1}{2}m\ell^2(\dot{\theta}^2 + \dot{\varphi}^2\sin^2\theta) - mg\ell\cos\theta\(\)

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  A bead of mass \(m\) slides on a straight wire of length \(L\) at an angle \(\theta\) with respect to the vertical. The wire rotates counterclockwise around the vertical with angular frequency \(\omega\).

<ol type="a">
<li> Find the equations of motion for this system
</li>
<li> The bead is initially at a position \(L/2\) from the bottom of the wire and has zero velocity. Solve for the motion of the bead.
</li>
<li> Under what conditions will the bead remain stationary at \(L/2\)?
</li></ol>

</div> </li>
<li> <div class="exercise">  A cylinder of radius \(R\) and mass \(m\) rolls without slipping on an incline of angle \(\theta\) and mass \(M\), which sits on a frictionless surface. Initially, the incline is at rest. The cylinder is released with its centre of mass at a height \(h\) from the frictionless surface.

<ol type="a">
<li> Find the Lagrangian for this system
</li>
<li> Find the Euler-Lagrange equations for this system
</li>
<li> Solve for the momentum of the cylinder when its centre of mass is a height \(h/2\) from the frictionless surface. What is the momentum of the incline at that time?
</li>
<li> What is the minimum coefficient of friction \(\mu\) needed on the incline surface so that the cylinder rolls without slipping?
</li></ol> 
 


</div> </li></ol>

