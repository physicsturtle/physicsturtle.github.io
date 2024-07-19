---
layout: lesson
title: Differentiation of Integrals
dept: math
course: calculus-III
unit: unit3
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 3
---

Here we will derive a useful formula for differentiating integrals. Suppose I have a function \\(g\\):

$$g(x) = \int_a^b f(x,y) dy$$

How do we differentiate this (with respect to \\(x\\))? Well, let's apply the definition of the derivative. 

$$\begin{eqnarray}
g'(x) &=& \lim_{h\to 0} \frac{g(x+h) - g(x)}{h}\\
&=& \lim_{h\to 0} \frac{1}{h}\left(\int_a^b f(x+h,y) dy - \int_a^b f(x,y) dy\right)\\
&=& \lim_{h\to 0} \frac{1}{h}\int_a^b f(x+h,y) - f(x,y) dy\\
&=& \int_a^b \lim_{h\to 0} \frac{f(x+h,y) - f(x,y)}{h}dy\\
&=& \int_a^b \partial_x f(x,y)dy\\
\end{eqnarray}$$

so we see that the ordinary derivative becomes a partial derivative when it igoes inside the integral. 

Now we consider a more complicated case. For this case, we will need to use the chain rule.

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
