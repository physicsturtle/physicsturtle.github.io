---
layout: lesson
title: GRADIENT VECTOR
course: calculus-III
unit: unit3
lessonID: gradient-vector
nextID: differential
---

The gradient vector of a function is the analogue of the normal derivative from single variable calculus. It encodes information about which direction the function increases in. The gradient vector is defined as 

$$\nabla f = \frac{\partial f}{\partial x}\hat{\textbf{x}} + \frac{\partial f}{\partial y}\hat{\textbf{y}}$$

### Geometric Interpretation
Consider the function \\(f\\) evaluated on a curve \\(\textbf{r}(t) = (x(t),y(t))\\). How does \\(f\\) change along this curve? If we differentiate with respect to \\(t\\), we can find how fast \\(f\\) changes along the curve. This is given by 

$$\begin{eqnarray}
f'(t) &=& f_x(x,y) x'(t) + f_y(x,y) y'(t)\\
&=& \nabla f\cdot \textbf{r}'(t) \\
&=& |\nabla f||\textbf{r}'(t)|\cos\theta
\end{eqnarray} $$

Suppose the curve \\(\textbf{r}(t)\\) is a level curve of \\(f\\). This would mean that \\(f'(t)\\) is zero along this curve. If neither \\(\nabla f\\) nor \\(\textbf{r}'(t)\\) are zero, then this means that \\(\cos\theta = 0\\), so \\(\theta = \pi/2\\). If instead we want to know the direction of greatest increase, we can consider a curve parallel to the gradient vector. This makes \\(\cos\theta = 1\\), which is then the maximum value of \\(f'(t)\\). Thus the gradient vector points in the direction of *fastest increase* of the function \\(f\\). In summary, the gradient vector is always *perpendicular* to level sets of the function. 




### Exercises

<ol>
<li> <div> Calculate the gradient vector of the function $$ f(x,y) = xy\cos(x^2)$$ </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>


<li> <div> Calculate the gradient vector of the function. $$f(x,y,z) = \sqrt{x^2+y^2+z^2\sin(xy)}$$ </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
