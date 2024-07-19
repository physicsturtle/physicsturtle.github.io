---
layout: lesson
title: Logarithmic Differentiation
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

### Method
So far, we have learned how to differentiate functions like $f(x) = x^n$ as well as functions like $f(x) = e^x$. The case of polynomial functions has the variable in the base and a constant in the exponent. The case of the exponential function has the constant in the base and the variable in the exponent. What happens if we allow both the base and exponent to vary? The method of logarithmic differentiation is best illustrated with an example. 

<div class="example">
<p><b>Example:</b> Differentiate the function $y = x^x$. </p>
<b>Solution:</b> We take the logarithm of both sides to get 
$$\log y = \log x^x = x\log x.$$
Now, we differentiate both sides with respect to $x$. Use the chain rule on the left side and the product rule on the right side.
$$\frac{y'}{x} = x\frac{1}{x} + 1\log x$$
Now multiply both sides by $y$:
$$y' = y(1+\log x).$$
Substitute back our expression for $y$ in terms of $x$:
$$y' = x^x(1+\log x).$$
</div>

To summarize the method, 
1. Take the logarithm of both sides
2. Differentiate both sides
3. Multiply both sides by the original function

Now, we do several examples to further illustrate the method.

### Examples

<div class="example">
<p><b>Example:</b> Differentiate the function (similar example to the first one)</p>
<b>Solution:</b> 
</div> <br>

<div class="example">
<p><b>Example:</b> Differentiate the function (product of a bunch of stuff). </p>
<b>Solution:</b> 
</div> <br>

<div class="example">
<p><b>Example:</b> Find a general formula for the derivative of $y = [f(x)]^{g(x)}$. </p>
<b>Solution:</b> First, we take the logarithm of both sides:
$$\log y = \log\left( [f(x)]^{g(x)}\right) = g(x)\log f(x).$$
Next, we differrentiate both sides with respect to $x$:
$$\frac{y'}{y} = g'(x)\log f(x) + g(x)\frac{f'(x)}{f(x)}.$$
Multiplying both sides by $y$, we get 
$$y' = y\left(g'(x)\log f(x) + g(x)\frac{f'(x)}{f(x)}\right).$$
Finally, substituting back in our original expression for $y$, 
$$y' = [f(x)]^{g(x)}\left(g'(x)\log f(x) + g(x)\frac{f'(x)}{f(x)}\right).$$
</div> <br>

### Discussion
Let's spend a moment thinking about the example for the derivative of $y = [f(x)]^{g(x)}$. If we pretend that $g$ is a constant, then we would get $y_f' = [f(x)]^{g-1}f'(x)g$. If we pretend that $f$ is a constant, then we would get $y_g' = \log(f)[f]^{g(x)}g'(x)$. Adding these two contributions together, 

$$y' =  [f(x)]^{g-1}f'(x)g + \log(f)[f]^{g(x)}g'(x).$$

If we factor $[f(x)]^{g(x)}$ out of this expression then it becomes the familiar one from the example:

$$y' = [f(x)]^{g(x)}\left(g'(x)\log f(x) + g(x)\frac{f'(x)}{f(x)}\right).$$


