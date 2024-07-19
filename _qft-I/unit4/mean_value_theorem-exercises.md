---
layout: exercises
title: Mean Value Theorem - Exercises
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

<ol> 
<li> <div class="exercise"> Let $f(x) = 1-x^{2/3}$. Show that $f(1) = f(-1) =0$, but that $f'(x)$ is never zero in the interval $[-1,1]$. Explain how this is possible in view of the Mean Value Theorem.

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
First, show that $f(1)=f(-1)=0$.
\begin{eqnarray*}
f(1) &=& 1-(1)^{\frac{2}{3}}\\
&=& 1-1 = 0\\
f(-1) &=& 1-(-1)^{\frac{2}{3}}\\
&=& 1-1 = 0
\end{eqnarray*}
The Mean Value Theorem states that if $f(x)$ is defined and continuous on the interval $[a,b]$ and differentiable on $(a,b)$, then there is at least one number $c$ in the interval $(a,b)$ (that is $a < c < b$) such that $f'(c)=\frac{f(b)-f(a)}{b-a}$.

According to this, there should be a horizontal slope in the interval $[-1,1]$. However, the function isn't differentiable at $x=0$ because $f'(x) = \frac{-2}{3x^{\frac{1}{3}}}$, so the theorem doesn't apply to this interval.

</div>
</div>
</div>
</li>

<li> <div class="exercise"> Show that $x^2 = x\sin x + \cos x$ for <i>exactly</i> two real values of $x$.

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
First we move everything over to one side to equate the difference of the left and right side to 0. Let $f(x) = x^2-x\sin x-\cos x = 0$
We must first show that there is at least two root by using three values and the Intermediate Value Theorem.
\begin{eqnarray*}
f(\pi) &=& (\pi)^2-(\pi)\sin(\pi) - \cos(\pi) = \pi^2+1 \Rightarrow +ve\\
f(0) &=& (0) - (0)\sin(0) - \cos(0) = -1 \Rightarrow -ve\\
f(-\pi) &=& (-\pi)^2-(-\pi)\sin(-\pi)-\cos(-\pi) = \pi^2+1 \Rightarrow +ve\\
\end{eqnarray*}
By the Intermediate Value Theorem, since f(x) is continuous on it's domain of $(-\infty,\infty)$, there must be two roots; one between $0<x<\pi$ and the other between $-\pi<x<0$.
Then, we assume that the function has 3 roots $f(a)=f(b)=f(c)=0$, by Rolle's Theorem, since the function is continuous, the first derivative must have two or more roots for this to be possible.
\begin{eqnarray*}
f(x) &=& x^2-x\sin(x)-\cos(x)\\
f'(x) &=& 2x-\sin(x)-x\cos(x)+\sin(x)=2x-x\cos(x) = x(2-\cos(x))\\
\end{eqnarray*}
We can see that the first derivative can only have a single root at $x=0$ because $-1\geq\cos(x)\geq1$.
Therefore, proving by contradiction that there cannot be three roots but have at least two, there is exactly two real roots.
</div>
</div>
</div>
</li>


<li> <div class="exercise"> Let $g(x) = \log(x^2 + 1) - \sin\left(e^{-x^2}\right)$. Show that there exists a real number $c$ such that $g'(c) = 0$.

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
Using Rolle's Theorem and the fact that the function is even ($f(-x)=f(x)$), any pair of $x=\pm a$ where $a\neq0$ would suffice for the theorem.

Now we need to test that the function is continuous and differentiable everywhere. $f(x)$ is continuous everywhere because it's a difference between a log function where the input is always positive and a continuous trigonometric function.

Taking the derivative of g(x):
\begin{eqnarray*}
\frac{d}{dx}(g(x)) = \frac{d}{dx}(\log(x^2+1)-\sin(e^{-x^2}) &=& \frac{2x}{x^2+1}-2xe^{-x^2}\cos(e^{-x^2}))\\
\end{eqnarray*}
Although there is a $-x^2$ within both the exponential and trigonometric functions, they are both always continuous on $(-\infty,\infty)$ no matter the input, so the derivative remains continuous throughout.
Thus, by Rolle's theorem there must exist a $g'(c)=0$ between any $x=\pm a$ or simply $x=0$.
or you could just take the derivative and notice that $g'(c)=0$ at $x=0$.
</div>
</div>
</div>
</li>

<li> <div class="exercise"> Let $h(x) = \sin x - x^2 + \pi x$. Show that there exists a real number $c$ such that $h'(c) = 0$.

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >
To prove that there exists a real number such that $h'(c)=0$ exists, we will use Rolle's theorem after finding two points such that $h(a)=h(b)$.

When confronted with trigonometric functions, the easiest choices to try values for which we can easily evaluate the trigonometric functions, such as $\pi$, such as $-\frac{\pi}{2}$, $0$, or $\pi$.

Analyzing the function, we can test points $x = 0$ and $x = \pi$.
\begin{eqnarray*}
h(0) &=& \sin(0)-(0)^2+\pi(0)=0\\
h(\pi) &=& \sin(\pi)-(\pi)^2+\pi(\pi)=0
\end{eqnarray*}
Since there are two values where $h(0)=h(\pi)=0$, the function is continuous on its domain, and the function is differentiable on it's domain, by Rolle's theorem there must be a point $x=c$ where $0<c<\pi$ such that $h'(c) = 0$.
</div>
</div>
</div>
</li>

</ol>
