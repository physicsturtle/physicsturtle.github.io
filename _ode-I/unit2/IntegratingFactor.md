---
layout: lesson
title: Integrating Factor 
dept: math
course: ode-I
unit: unit2
deptDisplay: Math
courseDisplay: Ordinary Differential Equations I
unitDisplay: Unit 2
---

The integrating factor is a very useful and general technique for solving many kinds of linear, nonlinear, ordinary, and partial differential equations. In this section, we will apply the technique to the simplest case, which is that of a first order linear inhomogeneous equation. We aim to find a solution to the equation of the form

$$\begin{align}
y' + p(x)y = q(x).
\end{align}$$

The idea of the integrating factor is to write the left hand side as the derivative of something, thus putting all the \\(y\\)'s together. This would allow us to simply integrate both sides. Let's now focus on the left hand side. We multiply the left hand side by \\(\mu(x)\\), and then impose the condition that the result can be written as the derivative of a product.

$$\begin{align}
\mu(x)(y'+p(x)y) = (\mu(x)y)'
\end{align}$$

If we expand out the right hand side with the product rule, we get

$$\begin{align}
\mu(x)y' + \mu(x)p(x)y = \mu(x)y' + \mu'(x)y
\end{align}$$

we can cancel \\(\mu(x)y'\\) from both sides, and get 

$$\begin{align}
\mu(x)p(x)y = \mu'(x)y
\end{align}$$

and then cancel out \\(y\\) from both sides to find a differential equation for \\(\mu\\), which is

$$\begin{align}
\frac{\mu'(x)}{\mu(x)} = p(x).
\end{align}$$

<div class="result">
<b>Result:</b>
To solve the differential equation 

$$\begin{align}
y' + p(x)y = q(x),
\end{align}$$

<ol>
<li> Multiply both sides by the integrating factor \(\mu(x) = e^{\int p(x) \d x}\)
</li>
<li> Rewrite the left hand side as a product \((\mu(x)y)'\).
</li>
<li> Integrate both sides
</li>
<li> Solve for \(y\) by dividing both sides by the integrating factor
</li>
<li> If there is an initial condition given, plug it in to solve for the arbitrary constant.
</li></ol>

</div>



