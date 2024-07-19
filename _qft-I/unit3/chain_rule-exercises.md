---
layout: exercises
title: Chain Rule
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

<ol>
<li> <div class="exercise"> Prove that if $f$ is an invertible, differentiable function, then
\[(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))}\]
Hint: Recall that $f(f^{-1}(x)) = x$. Try differentiating both sides of that. 

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
Consider the expression
\[f(f^{-1}(x)) = x\]
and differentiate both sides with respect to $x$.
\[f'(f^{-1}(x))(f^{-1})'(x) = 1\]
Then rearranging, we have
\[(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))}\]

</div>
</div>
</div>
</li>

<li> <div class="exercise">
Suppose $h$ is a function such that $h'(x) = \sin^2(\sin(x+1))$, and $h(0) = 3$. Find
<ol type = "a">
<li> $(h^{-1})'(3)$. </li>
<li> $(\beta^{-1})'(3)$, where $\beta(x) = h(x+1)$. </li>
</ol>

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
<ol type="a">
<li> From the formula derived above, 
\[(h^{-1})'(x) = \frac{1}{h'(h^{-1}(x))}\]
Plugging in $x = 3$ to both sides, 
\[(h^{-1})'(3) = \frac{1}{h'(h^{-1}(3))}\]
and since $h(0) = 3$, we know that $h^{-1}(3) = 0$.
Thus 
\[(h^{-1})'(3) = \frac{1}{h'(h^{-1}(3))} = \frac{1}{h'(0)} =  \frac{1}{\sin^2(\sin(1))}\]
</li>
<li> Since $\beta(x) = h(x+1)$, we know that $x = \beta^{-1}(h(x+1))$. Differentiating both sides:
\[(\beta^{-1})'(h(x+1))\cdot h'(x+1) = 1\]
Rearranging:
\[(\beta^{-1})'(h(x+1))  = \frac{1}{h'(x+1)}\]
Plugging in $x = -1$ to both sides:
\[(\beta^{-1})'(h(0))  = \frac{1}{h'(0)}\]
\[(\beta^{-1})'(3)  = \frac{1}{\sin^2(\sin(1))}\]
</li>
</ol>
</div>
</div>
</div>
</li>

<li> <div class="exercise">
Find a formula for $(f^{-1})''(x)$.

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
Given \[(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))},\]
we can differentiate both sides with respect to $x$.
\begin{eqnarray*}
((f^{-1})'(x))' &=& \left(\frac{1}{f'(f^{-1}(x))}\right)'\\
(f^{-1})''(x) &=& \frac{-(f'(f^{-1}(x)))'}{(f'(f^{-1}(x)))^2}\\
&=& -\frac{1}{(f'(f^{-1}(x)))^2}\cdot f''(f^{-1}(x))\cdot (f^{-1})'(x)\\
\end{eqnarray*}
Plugging in the previous formula for $(f^{-1})'$, we have
\[(f^{-1})''(x) = -\frac{ f''(f^{-1}(x))}{(f'(f^{-1}(x)))^3}\]

</div>
</div>
</div>
</li>

<li> <div class="exercise">
Suppose that $f$ is a differentiable and invertible function, and that $f = F'$. Let 
\[G(x) = xf^{-1}(x) - F(f^{-1}(x)).\] Show that $G'(x) = f^{-1}(x)$.

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >
Differentiating both sides:
\begin{eqnarray*}
G'(x) &=& f^{-1}(x) + x(f^{-1})'(x) - F'(f^{-1}(x))\cdot (f^{-1})'(x)\\
&=& f^{-1}(x) + x(f^{-1})'(x) - f(f^{-1}(x))\cdot (f^{-1})'(x)\\
&=& f^{-1}(x) + x(f^{-1})'(x) - x(f^{-1})'(x)\\
&=& f^{-1}(x)
\end{eqnarray*}


</div>
</div>
</div>
</li>

</ol>
