---
layout: exercises
title: Exponential Growth and Decay
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

\question[$*$] A culture of bacteria in a petri dish grows exponentially from an initial population of 5000 cells. Let $b(t)$ be the the number of bacteria after $t$ hours. Then $b(0) = 5000$. At $t = 10$ hours, scientists remove 4000 cells from the dish. At $t = 20$ hours, there are exactly 12000 cells in the dish. How many cells will be present in the dish at $t = 30$ hours?

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
Since we are told that it is exponential growth, we can construct the following model, value for $t < 10$:
\[b(t) = 5000e^{kt}\]
for some growth constant $k$. Then, we note that at $t = 10$, 4000 cells are taken away. This means that the number of bacteria \textit{just before} $t = 10$ is 
\[b(10^-) = 5000e^{10k}\]
and the number of cells in the dish \textit{just after} $t = 10$ is
\[b(10^+) = 5000e^{10k} - 4000\]
Now we can construct the following model for $b(t)$ for $t > 10$:
\[b(t) = (5000e^{10k} - 4000)e^{k(t-10)}\]
This means that in total, our model is 
\begin{displaymath}
b(t) = \left\{
\begin{array}{cc}
5000e^{kt}, &0 \leq t <10\\
(5000e^{10k} - 4000)e^{k(t-10)}, & t >10
\end{array}
\right.
\end{displaymath}
In order to find the unknown constant $k$, we evaluate $b$ at $t = 20$, because the number of bacteria is known at that time:
\[b(20) = 5000e^{20k} - 4000e^{10k} = 12000 \]
In order to solve for $k$, let $e^{10k} = x$, and rewrite the above equation as
\[5000x^2 - 4000x -12000 = 0\]
or, dividing by 1000, 
\[5x^2-4x-12 = 0\]
Solving for $x$: 
\[ x = \frac{4\pm\sqrt{16+60}}{10} = \frac{4\pm\sqrt{76}}{10} = \frac{2\pm\sqrt{19}}{5}\]
taking the positive value, we obtain
\[ k = \frac{\log\left( \frac{2+\sqrt{19}}{5}\right)}{10}\]
Now, for $t >10$, we can plug in the value for $k$ and $t = 30$ to obtain 
\[b(30) = 5000 \left(\frac{2+\sqrt{19}}{5}\right)^3 - 4000\left (\frac{2+\sqrt{19}}{5}\right)^2\]
\end{solution}






