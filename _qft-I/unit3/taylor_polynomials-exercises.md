---
layout: exercises
title: Taylor Polynomials - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

<ol>
<li> <div class="exercise">
If the third degree Maclaurin polynomial for $g(x)$ is $g(x) \approx T_{3,g}(x) = 3 + 2x - 5x^2 + x^3/3$ (the subscript $g$ denotes it being the Maclaurin polynomial for $g(x)$), and $f(x) = (g(x))^3$, find the second degree Maclaurin polynomial for $f(x)$. 

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
First we identify the form of the Maclaurin polynomial for $g$. 
\begin{eqnarray*}
T_{3,g}(x) &=& 3 + 2x - 5x^2 + \frac{x^3}{3} \\
&=& g(0) + g'(0)x + \frac{g''(0)x^2}{2} + \frac{g'''(0)x^3}{6}
\end{eqnarray*}
Matching coefficients, we have
<ul>
<li>  $g(0) = 3$ </li>
<li> $g'(0) = 2$ </li>
<li> $g''(0) = -10$ </li>
<li>  $g'''(0) = 2$ </li>
</ul>
The Taylor polynomial for $f$ at $0$ will be in the form of
\[T_{2,f}(x) = f(0) + f'(0)x+\frac{f''(0)x^2}{2}\]
We can calculate the desired values of $f$ as follows.

First, we evaluate at $f$ at $x = 0$ in terms of $g(0)$:
\[f(0) = (g(0))^3 = 3^3 = 27\]

Next, we differentiate $f$ to express $f'(0)$ in terms of $g(0)$ and $g'(0)$:
\[f'(x) = 3(g(x))^2g'(x)\]
Then, we evaulate both sides at $x = 0$: \[f'(0) = 3(g(0))^2g'(0) = 54\]

Lastly, differentiate one more time to find $f''(x)$ in terms of $g$ and its derivatives:
[f''(x) = 6g(x)(g'(x))^2 + 3(g(x))^2g''(x)\]
Then evaluate both sides at $x = 0$:
\[f''(0) = 72 - 270 = -198\]

So then the second degree Maclaurin polynomial of $f(x)$ is \[T_{2,f} = 27 + 54x - 99x^2\]
</div>
</div>
</div>
</li>



<li> <div class="exercise"> 
If $11 - 9x + 2x^2$ is the second degree Taylor polynomial to $h(x)$ at $x = 3$, and $\displaystyle{f(x) = \frac{h(x)}{\sqrt{x+1}}}$, compute the second degree Taylor polynomial to $f(x)$ at $x = 3$.

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
First, note that the Taylor polynomial to $h(x)$ at $x = 3$ is \textit{not} in the form that we want! It looks like a polynomial that is centred about $x = 0$. In order to expand it in terms of $(x-3)$, we need to consider it as a separate function and find the Taylor approximation about $x = 3$. 

Define 
\[w(x) = 11 - 9x + 2x^2\]
Then the second degree approximation to $w(x)$ at $x = 3$ is 
\[w(3) + w'(3)(x-3) + \frac{w''(3)(x-3)^2}{2}\]
This gives
<ul>
<li> $w(3) = 2$ </li>
<li> $w'(3) = 3$ </li>
<li> $w''(x) = 4$ </li>
</ul>
Thus, \[w(x) = 2 + 3(x-3) + 2(x-3)^2\]
So the approximation to $h(x)$ at $x = 3$ is now in the form that we want. Now we can read off the values for:
<ul>
<li> $h(3) = 2$ </li>
<li> $h'(3) = 3$ </li>
<li> $h''(3) = 4$ </li>
</ul>
Now we can compute the Taylor approximation to $f(x)$ at $x = 3$.
Let $T_2(x)$ be the second order Taylor approximation to $f(x)$ at $x = 3$. Then, 
\[T_2(x) = f(3) + f'(3)(x-3) + \frac{f''(3)(x-3)^2}{2} \]
With \[f(x) = \frac{h(x)}{\sqrt{x+1}}\]
we can differentiate to find the values of $f$ in terms of $h$:
\[f'(x) = \frac{h'(x)}{\sqrt{x+1}} - \frac{h(x)}{2(x+1)^{3/2}}\]
\[f''(x) = \frac{h''(x)}{\sqrt{x+1}} - \frac{h'(x)}{(x+1)^{3/2}} + \frac{3h(x)}{4(x+1)^{5/2}}\]
Evaluating $f(3)$, $f'(3)$, and $f''(3)$, we find
<ul>
<li> $f(3) = 1$ </li>
<li> $f'(3) = 11/8$ </li>
<li> $f''(3) = 107/64$ </li>
</ul>
Now we plug the numbers into $T_2(x)$:
\[T_2(x) = 1 + \frac{11}{8}(x-3) + \frac{107}{128}(x-3)^2\]
</div>
</div>
</div>
</li>

</ol>

