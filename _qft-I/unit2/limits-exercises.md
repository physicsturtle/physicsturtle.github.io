---
layout: exercises
title: Limits
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

### Introduction

In the last section, we introduced the idea of the tangent line to a curve, and how that can be calculated by using a limit. In this section, we will compute limits of functions and learn rules for simplifying limit calculations. There is a rigorous approach to limits, but we will not explore it in detail here; there will be an alternate limits lesson that you can read if you're interested.



### Idea of a Limit

Suppose we have a function $f(x) = x^2$. As $x$ approaches 2, it is clear that $f(x)$ approaches 4. 



<ol>
<li> <div> Evaluate the limit.  $$\lim_{x \to 2} \left(x^3 - 2x +1\right) $$ </div>

<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
$$\lim_{x \to 2}  \left(x^3 - 2x +1\right) = 2^3 - 2(2) + 1 = 3$$
</div> </li>

<li> <div> Evaluate the limit.  $$\lim_{x \to \frac{\pi}{2}} x\sin x$$ </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
$$\lim_{x \to \frac{\pi}{2}} x\sin x = \frac{\pi}{2}\sin\frac{\pi}{2} = \frac{\pi}{2}$$
</div> </li>


<li> <div> Evaluate the limit.  $$\lim_{x \to 0} \frac{3^x - 3^{-x}}{3^x + 3^{-x}}$$ </div>

<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
$$\begin{eqnarray*}
\lim_{x \to 0} \frac{3^x - 3^{-x}}{3^x + 3^{-x}} &=& \frac{3^0 - 3^{-0}}{3^0 + 3^{-0}}\\
&=& \frac{1-1}{1+1}\\
&=& \frac{0}{2}\\
&=& 0
\end{eqnarray*}$$
</div> </li>

</ol>
