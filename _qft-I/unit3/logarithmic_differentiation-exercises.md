---
layout: exercises
title: Logarithmic Differentiation - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

### Exercises
<ol>
<li> <div class="exercise> Differentiate the following function. $\displaystyle{y = (\tan x)^{1-x^2}}$

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer">
First take the logarithm of both sides:
\[\log(y) = \log(\tan(x))\cdot(1-x^2) \]
Differentiating both sides:
\begin{eqnarray*}
\frac{y'}{y} &=& [\log(\tan(x))\cdot(1-x^2)]' \\
&=& \left(\frac{\sec^2(x)}{\tan(x)}\right) (1-x^2) + (\log(\tan(x)))(-2x)
\end{eqnarray*}
Isolating $y'$:
\begin{eqnarray*}
y' &=& y\left(\frac{(1-x^2)\sec^2(x)}{\tan(x)} - 2x\log(\tan(x)) \right) \\
y' &=& (\tan(x))^{1-x^2} \left(\frac{(1-x^2)\sec^2(x)}{\tan(x)} - 2x\log(\tan(x)) \right)
\end{eqnarray*}
</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Differentiate the following function. $\displaystyle{y = (\arcsin 3x)^{\sqrt{e^{3x}+1}}}$

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
Taking the logarithm of both sides, and then differentiating:
\[\frac{y'}{y} = \frac{3\sqrt{e^{3x}+1}}{\arcsin(3x)\sqrt{1-9x^2}} + \log(\arcsin(3x))\frac{e^{3x}}{2\sqrt{e^{3x}+1}}\]
Isolating $y'$:
\[\frac{dy}{dx} = (\arcsin 3x)^{\sqrt{e^{3x}+1}}\cdot\left(\frac{3\sqrt{e^{3x}+1}}{\arcsin(3x)\sqrt{1-9x^2}} + \log(\arcsin(3x))\frac{3e^{3x}}{2\sqrt{e^{3x}+1}}\right)\]

</div> 
</div>
</div>
</li>

<li> <div class="exercise"> Compute a linear approximation to $f(x)$ at the point $x = \pi$.  \[f(x) = x^{x^{\sin x}}\]

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer">
Take the logarithm of both sides twice:
\[\log \log f = \sin x \log x + \log \log x.\]
Differentiating both sides: 
\[\frac{f'}{f\log f} = \frac{\sin x}{x} + \cos x \log x + \frac{1}{x\log x}\]
Solving for $f'$:
\[f' =x^{x^{\sin x}}\cdot(x^{\sin x}\log x)\cdot \left( \frac{\sin x}{x} + \cos x \log x + \frac{1}{x\log x}\right)\]
Now evaluating $f'(\pi)$:
\[f'(\pi) = 1-\pi(\log \pi)^2\]
Plugging that value into the linear approximation formula
\begin{eqnarray*}
L(x) &=& f(\pi) + f'(\pi)(x-\pi) \\
&=& \pi + ( 1-\pi(\log \pi)^2)(x-\pi)
\end{eqnarray*}

</div> 
</div>
</div>
</li>

</ol>

