---
layout: lesson
title: GREEN'S THEOREM
course: calculus-III
unit: unit5
lessonID: green-theorem
nextID: divergence
---

Green's thoerem, as well as the divergence theorem and Stoke's theorem, which we will see later, is a generalization of integration by parts. Here we will define Green's theorem, prove it, as well as give some examples of its use. Green's theorem has two distinct formulations, with one corresponding to the divergence  theorem and the other to Stoke's theorem. 


In single variable calculus, we learned about the fundamental theorem of calculus. The fundamental theorem fo calculus allowed us to take the information about the derivative of a function inside the integral, and express it in terms of the function at the boundary. 
\[\underbrace{\int_a^b f'(x) dx}_\text{interior information} = \underbrace{f(b) - f(a)}_\text{boundary information}\]
Green's theorem is a generalization of this fact for integrals of functions of two variables. Green's theorem is as follows:

<div class="theorem">
<b> Theorem: </b> Suppose $C$ is a positively oriented, piecewise-smooth, simple closed curve in the plane. Let $D$ be the region bounded by $C$ (thus calling $C = \partial D$). If $P$ and $Q$ have continuous partial derivatives on an open region that contains $D$, then
\[\int_{\partial D} P dx + Q dy = \iint_D\left(\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}\right)dA.\]
</div>

This statement can be rewritten as 
\[\int_{\partial D} -Q dx + P dy= \iint_D\left(\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y}\right) dA\]

One may be able to recognize this as the flux integral around the curve $\partial D$ of the vector field $\left<P,Q\right>$. If we say $\textbf{F} = \left<P,Q\right>$, $d\textbf{r} = \left< dx, dy\right>$, and $d\textbf{n} = \left< dy,-dx\right>$, then this allows us to write these two expressions as 
\[\int_{\partial D} \textbf{F} \cdot d\textbf{r} = \iint_D \nabla\times\textbf{F} dA,\qquad \int_{\partial D} \textbf{F} \cdot d\textbf{n} = \iint_D \nabla\cdot\textbf{F} dA\]
%This statement can be rewritten as 
%\begin{eqnarray*}
%    \int_{\partial D} P dx + Q dy &=& \int_{\partial D} \left< P, Q\right> \cdot \left< dx, dy\right>\\
%    &=& \int_{\partial D} \left< P, Q\right> \cdot \underbrace{\left< \frac{dx}{dt}, \frac{dy}{dt}\right>}_{d\textbf{r}/dt} dt\\
%\end{eqnarray*}
In this form, Green's theorem is more easily memorized. 

 
<div class="example"> 
\begin{parts}
 \part Use Green's Theorem to evaluate the line integral 
 $$\oint_C y^2dx + xdy$$ whereby $C$ has the vector equation $\textbf{a}(t) = \left<2\cos t, 2\sin t\right>$, $t\in[0,2\pi]$ %$\textbf{a}(t) = \left<2\cos^3t, 2\sin^3t\right>$, $t\in[0,2\pi]$.
 \part Calculate the same integral directly.
 \end{parts}
 
 <div class="exampleSolution">
 \begin{parts}
 \part If we're going to use Green's theorem, then we need to calculate the region over which we're going to do the double integral. This is going to be the circle of radius 2. Thus let's change this to a double integral
 \begin{eqnarray*}
 \oint_C y^2dx + xdy &=& \iint \left(\frac{\partial x}{\partial x} - \frac{\partial y^2}{\partial y} \right)dA \\
 &=&  \iint \left(1-2y\right) dA \\
 &=& \int_0^{2\pi}\int_0^2 (1-2r\sin\theta)r dr d\theta\\
 &=& \int_0^{2\pi} \left(2 - \frac{16}{3}\sin\theta\right) d\theta\\
 &=& 4\pi
 \end{eqnarray*}
 \part To do the integral directly, we need to first find $\textbf{a}'(t) = \left<-2\sin t, 2\cos t\right>$. Then, we can write
 \begin{eqnarray*}
 \oint_C y^2dx + xdy &=& \int_0^{2\pi} (4\sin^2 t)(-2\sin t) dt + (2\cos t)(2\cos t) dt \\
 &=& \int_0^{2\pi} (-8\sin^3 t + 4\cos^2 t) dt\\
 &=& 4\pi
 \end{eqnarray*}
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
