---
layout: lesson
title: Euler-Lagrange equation 
dept: physics
course: cm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 2
---
In this lesson, we will derive the Euler-Lagrange equation for the basic problem in the calculus of variations. The problem is to minimize the integral

$$S[x] = \int_a^b \mathcal{L}(t,x,\dot{x}) \d t $$

over differentiable functions \\(x\\), where \\(x(a)\\) and \\(x(b)\\) are given. To do this, we assume that we have found a function \\(x_{*}\\) which minimizes the integral. Then, we consider a general function \\(x = x_{*} + \epsilon\eta\\), where \\(\eta\\) is a any function satisfying \\(\eta(a) = \eta(b) = 0\\); recall that we are only considering functions which satisfy the boundary conditions so we cannot have any extra contributions at \\(t = a\\) and \\(t = b\\). Thus, \\(\epsilon\eta\\) is a small perturbing funciton. We note that for \\(\epsilon = 0\\), \\(y\\) becomes the minimizer of the integral. This means that 

$$\begin{equation}
\frac{\d}{\d\epsilon} S[x]\bigg|_{\epsilon = 0} = 0.
\end{equation}$$

Armed with this condition, we compute the derivative of \\(S\\) with respect to \\(\epsilon\\). 

$$\begin{align}
\frac{\d}{\d\epsilon}S[x] ={}& \frac{d}{d\epsilon} \int_a^b \mathcal{L}(t,x,\dot{x}) \d t\\
={}& \int_a^b\left(\frac{\partial\mathcal{L}}{\partial x}\frac{\d x}{d\epsilon} + \frac{\partial\mathcal{L}}{\partial \dot{x}} \frac{d\dot{x}}{d\epsilon}\right) \d t \\
={}& \int_a^b\left(\frac{\partial\mathcal{L}}{\partial x}\eta + \frac{\partial\mathcal{L}}{\partial \dot{x}} \dot{\eta} \right) \d t \\
={}&  \int_a^b\left(\frac{\partial\mathcal{L}}{\partial x}\eta \right) \d t +  \int_a^b\left(\frac{\partial\mathcal{L}}{\partial \dot{x}} \dot{\eta} \right) \d t \\
={}&  \int_a^b\left(\frac{\partial\mathcal{L}}{\partial x}\eta \right) \d t +  \left(\frac{\partial\mathcal{L}}{\partial \dot{x}} \eta\right)\bigg|_a^b - \int_a^b \frac{d}{\d t}\left(\frac{\partial\mathcal{L}}{\partial \dot{x}} \right)\eta \d t \\
={}&  \int_a^b\left[\frac{\partial\mathcal{L}}{\partial x}- \frac{d}{\d t}\left(\frac{\partial\mathcal{L}}{\partial \dot{x}} \right)\right]\eta \d t 
\\
={}& 0
\end{align}$$

Since this integral is 0 for all \\(\eta\\), we conclude that the object multiplying it is zero, or, 

$$\frac{\partial\mathcal{L}}{\partial x}- \frac{d}{\d t}\left(\frac{\partial\mathcal{L}}{\partial \dot{x}}\right)  = 0$$

This is known as the Euler-Lagrange equation. 

<div class="result">
<b>Result:</b> If the function \\(x(t)\\) is a stationary point of the functional 
\(\)S[x] = \int_a^b \mathcal{L}(t,x,\dot{x}) \d t,\(\)
then it must satisfy the <i>Euler Lagrange equation</i>
\(\)\frac{\partial\mathcal{L}}{\partial x}- \frac{d}{\d t}\left(\frac{\partial\mathcal{L}}{\partial \dot{x}}\right)  = 0.\(\)

</div>

Note that in this derivation, we have \\(t\\) as the independent variable and \\(x = x(t)\\) as the dependent variable. The Euler Lagrange equation works equally well if we simply relabel the variables; some problems have \\(x\\) as the independent variable and \\(y = y(x)\\) as the dependent variable. In these cases we have \\(\L = \L(x,y,y')\\) and the Euler Lagrange equation is 

$$\frac{\partial\L}{\partial y} = \frac{d}{\d x}\frac{\partial\L}{\partial y'}.$$

Examples
To get a feel for how this works, let us now find the Euler Lagrange equation for certain Lagrangians. 

<div class="example">
<b>Example:</b>
Find the Euler Lagrange equation for the Lagrangian
\(\)\L(x,\dot{x}) = \frac{1}{2}m\dot{x}^2 - V(x),\(\)
where \(m\) is a constant. Does the resulting equation look familiar? 

\noindent<b>Solution:</b>


</div>

<div class="example">
<b>Example:</b>
<ol type="a">
<li> Find the Euler Lagrange equation for the Lagrangian corresponding to the shortest path between two points:
\(\)\L(y,y') = \sqrt{1+(y')^2}\(\)
</li>
<li> Solve the differential equation subject to boundary conditions \(y(x_1) = y_1\) and \(y(x_2) = y_2\).
</li></ol>


<b>Solution:</b>

<ol type="a">
<li> 
</li>
<li> 
</li></ol>

</div>

<div class="example">
<b>Example:</b>
Find the Euler Lagrange equation for the Lagrangian 
\(\)\L(y,y') = y\sqrt{1+(y')^2},\(\)
which you may recognize as the one from the minimal lateral surface area problem from the introduction page. You do not need to solve the resulting differential equation. </p>
<b>Solution:</b> The Euler Lagrange equation for us is (consider \(x\) the independent variable and \(y\) the dependent variable)
\(\)\frac{d}{\d x}\left(\frac{\partial\mathcal{L}}{\partial y'}\right) = \frac{\partial\mathcal{L}}{\partial y}.\(\)

If we plug this in, we find that the partial derivatives of \(\L\) with respect to \(y\) and \(y'\) are, respectively,

\(\)\frac{\partial \L}{\partial y} = \sqrt{1+(y')^2} ,\qquad \frac{\partial\L}{\partial y'} = \frac{yy'}{\sqrt{1+(y')^2}}.\(\)

If we plug these into the Euler Lagrange equation, we get 

\(\) \frac{d}{\d x}\left(\frac{yy'}{\sqrt{1+(y')^2}}\right) = \sqrt{1+(y')^2}.\(\)

If we expand out all the terms, then we get 

\(\)\frac{(y')^2}{\sqrt{1+(y')^2}} +  \frac{yy"}{\sqrt{1+(y')^2}} - \frac{y(y')^2y"}{(1+(y')^2)^{3/2}}= \sqrt{1+(y')^2}\(\)

If we simplify the terms and cancel, then we get 

\(\)\frac{yy"}{1+(y')^2} = 1.\(\)

If we solve this differential equation for \(y\), then we will find a function which provides a stationary point of the integral and thus minimizes the surface area.

</div>

