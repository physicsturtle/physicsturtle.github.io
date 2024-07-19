---
layout: lesson
title: LAPLACIAN
course: calculus-III
unit: unit5
lessonID: laplacian
nextID: surface-integrals
---

- Definition of laplacian
- Meaning of laplacian
- analyzing functions with the laplacian

The Laplacian looks like fancy second derivative operator, but what parallels can we draw between it and the second derivative from single variable calculus? It, similar to how the second derivative in single variable calculus shows inflection points, contains information about the inflection points of a function.

The definition of the Laplacian is as follows

$$\nabla^2 f=  \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2}$$

You may recall the following approximation to the second derivative:

$$ f''(x) \approx \frac{f(x+\Delta x) - 2f(x) + f(x - \Delta x)}{\Delta x^2}$$

Using this expression in the definition of the Laplacian, and also saying that our step sizes in each direction are the same ($\Delta x = \Delta y = \Delta z = h$), we get

$$\begin{eqnarray}
\nabla^2 f &\approx&   \frac{f(x+\Delta x,y,z) - 2f(x,y,z) + f(x-\Delta x,y,z)}{\Delta x^2} \\
&+&  \frac{f(x,y+\Delta y,z) - 2f(x,y,z) + f(x,y-\Delta y,z)}{\Delta y^2}\\
&+& \frac{f(x,y,z+\Delta z) - 2f(x,y,z) + f(x,y,z-\Delta z)}{\Delta z^2} \\
&=& \frac{f(x+h,y,z) + f(x - h,y,z) + f(x,y+h,z) + f(x,y-h,z) f(x,y,z+h) + f(x,y,z-h)-6f(x,y,z)}{h^2} \\
&=& \frac{1}{6h^2}(\bar{f} - f(x,y,z))
\end{eqnarray}$$ 

This quantity $\bar{f}$ is the average of $f$ over all of its surrounding points. Thus the laplacian represents the difference between this average and the value at the centre. Now, how does this relate to concavity? If we have found a critical point of the function $f$, say, at $(x_0,y_0,z_0)$, then what does $\nabla^2 f(x_0,y_0,z_0)$ say about the behaviour of $f$ at this point? If the average of the function about the point $\bar{f}$ is greater than the value of the function $f_0$, then this means that the function is concave 



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
