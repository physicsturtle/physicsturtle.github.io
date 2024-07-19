---
layout: exercises
title: Intermediate Value Theorem - Exercises
dept: math
course: calculus-I
unit: unit2
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 2
---

<ol>
<li> <div class="exercise"> Show that there exist at least 2 real solutions to the equation $8\sin x = x^2+1$


<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
Define $f(x) = 8\sin x - x^2 -1$. First we will need the following inequality: Since \[-1 \leq \sin x \leq 1\] we can multiply both sides by 8 to obtain \[-8 \leq 8\sin x \leq 8 \]
We expect $f(\pi/2)$ to be positive, but we must prove that inequality. 
\[f(\pi/2) = 8 - \pi^2/4 - 1\] Since
\[ 3 < \pi < 4\] 
We can square the inequality
\[9 < \pi^2 < 16 < 28\] We can rewrite this as 
\[28 > \pi^2\] or 
\[4 \cdot 7 > \pi^2\]
Therefore
\[7 > \pi^2/4\]
which can be rewritten as 
\[8-\pi^2/4 - 1>0\] 
Thus, $f(\pi/2) > 0$.\\
Now we need to find some $x$ where $f$ is negative. 
\[f(10)  = 8\sin(10) - 100 - 1\]
Since 
\[8 \geq 8 \sin x \]
Subtract 101 from both sides to obtain
\[ 0 > -93 \geq 8\sin x - 101 = f(10)\]
So $f(10) < 0$
Now we find $f(-10)$. 
\[f(-10) = 8 \sin(-10) - 100 - 1\]
Again we use the inequality 
\[8 \geq 8 \sin x\]
which holds for all $x$. Then, in particular it holds for $x = -10$.
\[ 0 > -93 \geq 8\sin(-10)- 101 = f(-10)\]
so $f(-10)$ is also negative.\\
\\
Since $f(-10) < 0, f(0) > 0, f(-10) < 0$, and $f(x)$ is a continuous function for all real numbers due to it being composed of polynomials and trigonometric functions, and it changes sign twice in the interval $(-10,10)$, this means that, by the Intermediate Value Theorem, it must cross the $x$-axis at least twice in that interval. 
</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Show that there exist at least 2 real solutions to $x^4 = 3x^2 + 5$.

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>

<div  id="answer2" class="answer">
Let $f(x)=x^4-3x^2-5$
To show that there are two solutions we must use Intermediate Value Theorem twice.
\begin{itemize}
\item Plug in $x = -3$:
\[ f(-3)=81-9\cdot9-5=49\]
\item Plug in $x = 0$:
\[f(0)=0-3\cdot0-5=-5 \]
\item Plug in $x = 3$:
\[f(3)=81-3\cdot9-5=81-27-5=49\]
\end{itemize}

$f(x)$ is continuous on $\mathbb{R}$ as it is a polynomial. Since $f(-3)>0$ and $f(0)<0$, and $f(3)>0$, so the sign changes twice on the interval $[-3,3]$. Therefore the function must have at least two roots on that interval by Intermediate Value Theorem. Other values of $x$ may be used; as long as two sign changes are observed, the values work. 
</div> 
</div>
</div>
</li>



<li> <div class="exercise"> Show that there exists at least 1 real solution to $\cos x = \sqrt x$

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
Let $f(x)=\cos(x)-\sqrt{x}$. Apply the Intermediate Value Theorem
\begin{itemize}
\item Plug in $x = \pi/2$:
\[f(\pi/2)=\cos(\pi/2)-\sqrt{\pi/2}=-\sqrt{\pi/2}\]
\item Plug in $x = 0$:
\[ f(0)=\cos(0)-\sqrt{0}=1\]
\end{itemize}
We know that $f(x)$ is continuous for $x \in [0,\infty)$ as it is composed of a trigonometric function and the square root function, which is continuous on $x \in [0,\infty)$. Since $f(0)>0$ and $f(\pi/2)<0$, by Intermediate Value Theorem there must be at least one real solution. \\
</div> 
</div>
</div>
</li>
</ol>

