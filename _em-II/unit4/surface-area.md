---
layout: lesson
title: SURFACE AREA
course: calculus-III
unit: unit4
lessonID: surface-area
nextID: triple-integral
---

- geometric derivation of surface area

We have already learned to calculate the length of a curve in the plane in the section on plane curves. This section on surface area however will be analogous to how we calculated the length of a curve in single variable calculus. 

### Explicitly Defined Surface

Consider a surface area element $dS$. When $dS$ is small, we can consider it as a part of a plane. Consider the corner above $(x,y)$ of $dS$. Along the $x$ axis, the corner above $x + \Delta x$ will be approximately a height $\partial f/\partial x \Delta x $ above the lower corner at $f(x,y)$. Along the $y$ axis, the corner above $y + \Delta y$ will be approximately a height $\partial f/\partial y \Delta y$ above the lower corner at $f(x,y)$. The area of a parallelogram can be calculate by a cross product. Our two vectors will be 

$$\textbf{a} = \left(\Delta x, 0 ,\partial_xf(x,y)\Delta x\right),\quad \textbf{b} = \left(0,\Delta y,\partial_y f(x,y)\Delta y\right)$$

Then we take the cross product 

$$\begin{eqnarray}
\textbf{a}\times\textbf{b} &=& \begin{vmatrix} \hat{\textbf{x}} & \hat{\textbf{y}} & \hat{\textbf{z}} \\  \Delta x &  0 & \partial_xf(x,y)\Delta x \\ 0 & \Delta y & \partial_y f(x,y)\Delta y \end{vmatrix} \\
&=& -(\partial_x f(x,y)\Delta x \Delta y)\hat{\textbf{x}} - (\partial_y f(x,y) \Delta x\Delta y)\hat{\textbf{y}} + \Delta x \Delta y \hat{\textbf{z}}  
\end{eqnarray}$$  

Then taking the magnitude of this, we get 

$$\begin{eqnarray}
|\textbf{a}\times\textbf{b}| &=&  \sqrt{f_x(x,y)^2\Delta x^2 \Delta y^2 + f_y(x,y)^2\Delta x^2\Delta y^2  + \Delta x^2 \Delta y^2 } \\
&=& \sqrt{f_x(x,y)^2 + f_y(x,y)^2 + 1} \Delta x \Delta y\\
&=& \sqrt{1+ |\nabla f|^2} \Delta x \Delta y
\end{eqnarray}$$

This gives the final formula for the surface area of the graph of the surface of $f$ above the region $R$ in the $xy$ plane.  

$$S(R) = \iint_R \sqrt{1+|\nabla f|^2} dx dy$$

### Parametrically Defined Surface

If we instead have the surface defined in terms of a parametrization, for example 

$$\textbf{r} = \textbf{r}(u,v)$$

the formula will be slightly different. This one the student should try to work through on her/his own, but we will provide some guidance here. We need to consider the element of the surface again. Two tangent vectors to the surface will be 

$$\frac{\partial \textbf{r}}{\partial u},\quad \frac{\partial \textbf{r}}{\partial v} $$



 






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
