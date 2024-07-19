---
layout: lesson
title: Derivatives of Polynomials 
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

In this section, we will learn start finding formulas for derivatives. The simplest formula to find is the one for polynomials. It is the following. 

<div class="result">
<b>Result:</b>
The derivative of a polynomial expression \(x^n\) is given by 
$$\begin{equation}
\frac{\d}{\d x}x^n = nx^{n-1}.
\end{equation}$$

</div>

To prove this result, we apply the definition of the derivative. 

<div class="proof">
<b>Proof:</b>
Let \(f(x) = x^n\), and apply the definition of the derivative
$$\begin{align}
f'(x) ={}& \lim_{x\to 0} \frac{f(x+h)-f(x)}{h}\\
={}& \lim_{x\to 0} \frac{(x+h)^n-x^n}{h}\\
={}& \lim_{x\to 0} \frac{(x^n + nx^{n-1}h + n(n-1)x^{n-2}h^2 + \cdots + n(n-1)\cdots 2 x h^{n-1} + n! h^n) - x^n}{h}\\
={}& \lim_{x\to 0} \frac{nx^{n-1}h + n(n-1)x^{n-2}h^2 + \cdots + n(n-1)\cdots 2 x h^{n-1} + n! h^n}{h}\\
={}& \lim_{x\to 0} nx^{n-1} + n(n-1)x^{n-2}h + \cdots + n(n-1)\cdots 2 x h^{n-2} + n! h^{n-1}\\
={}& nx^{n-1}
\end{align}$$

</div>

<div class="example">
<b>Example:</b>
Compute the derivative of each of the following functions:
<ol type="a">
<li> \(f(x) = x^2 - \frac{1}{x^2}\)
</li>
<li> \(f(x) = x^{5/2} - 3x^2\)
</li>
<li> \(f(x) = x^\pi\)
</li>
<li> \(f(x) = -2x^7 - \pi^e - 2x\)
</li></ol>


<b>Solution:</b>
<ol type="a">
<li> \(f'(x) = 2x + \frac{2}{x^3}\)
</li>
<li> \(f'(x) = \frac{5}{2}x^{3/2} - 6x\) 
</li>
<li> \(f'(x) = \pi x^{\pi-1}\) 
</li>
<li> \(f'(x) = -14x^6 - 2\)
</li></ol>

</div>


