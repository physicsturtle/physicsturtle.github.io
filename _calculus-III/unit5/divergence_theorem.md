---
layout: lesson
title: Divergence Theorem
dept: math
course: calculus-III
unit: unit5
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 5
---

The divergence theorem relates the flux of a vector field through a closed surface to the volume integral of the divergence of the vector field inside the surface. This makes some sense, because if the divergence is everywhere positive inside the closed surface, then that means the vector field is spreading out everywhere inside the surface. This would then imply that there should be a lot of flux coming out of the surface. Let's now make this a bit more formal. 


<div class="example">
Consider the region enclosed by the surfaces $z = a > 0$,  and $z = x^2 + y^2$. Find the outward flux of $\textbf{F} = \left<x,y,0\right>$ through the surface bounding this region
\begin{parts}
\part directly
\part using the Divergence theorem
\end{parts}

<div class="exampleSolution">
\begin{parts}
\part There are two surfaces to consider. The horizontal planar surface will have no outward flux because the unit normal is everywhere perpendicular to the surface. Thus we consider only the paraboloidal surface. The normal to the surface of the paraboloid is $\textbf{n} = \left< 2x, 2y, -1\right>$. If we parametrize the paraboloid by its natural coordinates $x,y$ (no need for $u,v$ here), then we just have $d\textbf{S} = \textbf{n} dx dy$. Finally, the region of integration is the circle centred at the origin of radius $\sqrt{a}$.  
$$\begin{eqnarray*}
\Phi &=& \iint \textbf{F}\cdot d\textbf{S} \\
&=& \iint \left<x,y,0\right>\cdot \left<2x,2y,-1\right> dx dy \\
&=& \iint 2(x^2+y^2) dx dy\\
&=& \int_0^{2\pi}\int_0^{\sqrt{a}} 2r^2 rdrd\theta\\
&=& \pi a^2
\end{eqnarray*}$$
\part When we use the divergence theorem, we will be calculating a volume integral inside this region of the divergence of the vector field. First, we have $\nabla\cdot \textbf{F} = 2$. Next, we need to calculate
$$\begin{eqnarray*}
\iint \textbf{F}\cdot d\textbf{S} &=& \iiint \nabla\cdot \textbf{F}dV \\
&=& \int_0^a \int_0^{2\pi} \int_0^{\sqrt{z}} 2 r dr d\theta dz\\
&=& \int_0^a\int_0^{2\pi} z d\theta dz\\
&=& 2\pi \frac{a^2}{2}\\
&=& \pi a^2
\end{eqnarray*}$$
\end{parts}
</div>
</div>


### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
