---
layout: lesson
title: Quotient Rule
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

In this section, we will derive the quotient rule. 

### Introduction
In this section, we will learn how to compute derivatives if there are two functions multiplied together, for example $f(x) = x\sin x$. The product rule is not as simple as the sum rule which we have seen so far, but is intuitive if one thinks about it the right way. We will start simply with what the product rule is, and then have a discussion on the intuition behind it later. 

### Theorem and Derivation

<div class="theorem">
<b>Theorem:</b> Let $f(x)$ and $g(x)$ each be differentiable functions. Then, the derivative of their quotient is 
$$\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x)g(x) - f(x)g'(x)}{g(x)^2}.$$
</div> <br>

To proceed with the proof we apply the definition of the derivative.

<div class="proof">
<b>Proof:</b> 
$$\begin{eqnarray*}
\frac{d}{dx}\frac{f(x)}{g(x)} &=& \lim_{h\to 0} \frac{\frac{f(x+h)}{g(x+h)} - \frac{f(x)}{g(x)}}{h}\\
&=& \lim_{h\to 0} \frac{f(x+h)g(x) - f(x)g(x+h)}{g(x+h)g(x)h}\\
&=& \lim_{h\to 0}\frac{f(x+h)g(x) - f(x) g(x) + f(x)g(x) - f(x)g(x+h)}{g(x+h)g(x)h}\\
&=& \frac{g(x)\lim_{h\to 0}\frac{f(x+h)-f(x)}{h} - f(x)\lim_{h\to 0}\frac{g(x+h) - g(x)}{h}}{\lim_{h\to 0}g(x)g(x+h)}\\
&=& \frac{f'(x)g(x) - f(x)g'(x)}{g(x)^2}
\end{eqnarray*}$$
</div>
