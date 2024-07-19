---
layout: lesson
title: Introduction to the problem 
dept: physics
course: cm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Classical Mechanics III
unitDisplay: Unit 2
---
The problem that we are interested in solving is finding the stationary points of the integral

$$\begin{equation} 
 S[x] = \int_a^b \L(t,x,\dot{x}) \d t \label{eq:functional}
\end{equation}$$

over all functions \\(x\\). The function \\(\L\\) is called the <i>Lagrangian</i>, and \\(S\\) is called a <i>functional</i>. A function takes as input a function (in our case, \\(x\\) is the function), and spits out a real number (in our case, the value of the integral). To help you understand what the problem is, let's calculate \\(S\\) for some various functions \\(x\\). 

<div class="example">
<b>Example:</b>
Let \(S\) be defined by 
$$\begin{equation}
S[x] = \int_0^1 \left(tx^2 - \dot{x}^3\right )\d t
\end{equation}$$
Calculate \(S\) for the following functions of \(t\). Give the answer in terms of a decimal; feel free to use a computer to evaluate the integral. Which gives the smallest value of \(S\)?
<ol type="a">
<li> \(x(t) = t^2\)
</li>
<li> \(x(t) = \sin(\pi t)\)
</li>
<li> \(x(t) = e^t\)
</li></ol>


<b>Solution:</b>
<ol type="a">
<li> For the case \(x(t) = t^2\), the Lagrangian becomes 

$$\begin{equation}
L = t^5 - 8t^3.
\end{equation}$$

The integral is then 

$$\begin{equation}
S = \int_0^1 \left(t^5 - 8t^3\right) \d t.
\end{equation}$$

The value of the integral is \(-1.833\)
</li>
<li> For the case of \(x(t) = \sin(\pi t)\), the Lagrangian becomes

$$\begin{equation}
L = t\sin^2(\pi t) - \pi^3 \cos^3(\pi t).
\end{equation}$$

The integral is then 

$$\begin{equation}
S = \int_0^1 \left(t\sin^2(\pi t) - \pi^3 \cos^3(\pi t)\right) \d t.
\end{equation}$$

The value of the integral is \(0.25\)
</li>
<li> For the case of \(x(t) = e^t\), the Lagrangian becomes

$$\begin{equation}
L = t e^{2t} - e^{3t}
\end{equation}$$

The integral is then 

$$\begin{equation}
S = \int_0^1 \left(t e^{2t} - e^{3t}\right) \d t.
\end{equation}$$

The value of the integral is \(-4.264\)
</li></ol>
The smallest value of \(S\) was for the case \(x(t) = e^t\).

</div>

As we have seen in this example, depending on the form of \\(x(t)\\), we get a different value for \\(S[x]\\). It will be our goal to find functions \\(x\\) which give the <i>smallest possible value of</i> \\(S\\). Later, we will introduce boundary conditions, by which I mean we will only consider functions \\(x\\) which satisfy \\(x(a) = A\\) and \\(x(b) = B\\), where \\(a,b,A,B\\) are all given. 

### Examples

Let's now conclude the lesson by giving some examples of problems which lead to the optimization of a functional of the form \\(\eqref{eq:functional}\\). You are not expected to understand how we came up with these functionals, but rather just recognize that we are presenting problems in the calculus of variations. 

<div class="example">
<b>Example:</b> 
Consider two points \((x_{1},y_{1})\) and \((x_{2},y_{2})\) in the \(xy\)  plane. If one connects these two points by a curve \(y = y(x)\), then one can calculate the length of this curve. What curve gives the shortest distance between the two points? The length \(\ell\) (nothing to do with the Lagrangian that we mentioned before) of a curve \(y = y(x)\) is 

$$\begin{equation}
L[y] = \int_{x_1}^{x_2}\sqrt{1+(y')^2} \d x.
\end{equation}$$

You will not be surprised to find out that the function minimizing this function is a straight line.

</div>

<div class="example">
<b>Example:</b>
<i>The Brachistochrone Problem</i>. Consider rolling a ball without friction down a (possibly curved)
incline which connects two points. Which shape of incline minimizes the time it takes to roll from the top to the bottom? This is known as the brachistochrone problem. The time \(T\) that it takes to traverse an incline of shape \(y = y(x)\) is given by 
$$\begin{equation}
T[y] = \int_0^L \sqrt{\frac{1+(y')^2}{2gy}}\d x.
\end{equation}$$

</div>

<div class="example">
<b>Example:</b>
Suppose we are interested in finding the surface area of a solid of revolution whose radii at the top and bottom are \(y_1\) and \(y_2\), respectively. What curve defining the boundary will cause the lateral surface area of the solid to be minimized? The surface area \(S\) of such a solid is given by 
$$\begin{equation}
S[y] =  2\pi\int_{x_1}^{x_2} y\sqrt{1+(y')^2} \d x.
\end{equation}$$
We are thus interested in finding a function \(y\) which causes \(S\) to be a minimum, such that \(y(x_1) = y_1\) and \(y(x_2) = y_2\). 

</div>

<div class="example">
<b>Example:</b> The following is an example of contrained optimization, analogous to the study of Lagrange multipliers from multivariable calculus. If one lets a rope (length \\(L\\)) of uniform mass density \\(\mu\\) hang between two points (separated in the \\(x\\) direction by a distance \\(a\\)), what is the shape that it makes? For a given shape of rope \\(y = y(x)\\), the potential energy \\(V\\) of the rope is
$$\begin{equation}
V[y] = g\mu \int_0^a \left(y\sqrt{1+(y')^2} \right) \d x
\end{equation}$$
where we pick the heights of the endpoints by only allowing functions such that \(y(0) = h_1\) and \(y(a) = h_2\). An additional constraint that we must place on the function \(y\) is that it must satisfy
$$\begin{equation}
L = \int_0^a \sqrt{1+(y')^2} \d x,
\end{equation}$$
where \(L > a\). This is the constraint that the length of the curve \(y(x)\) indeed matches the length \(L\) of the given rope. The function \(y\) (satisfying the boundary conditions) which minimizes the <i>potential energy</i> \(V\) subject to the constraint of being length \(L\) and satisfying the boundary conditions \(y(0) = h_1\) and \(y(a) = h_2\) is the shape that the rope will actually take. 

</div>

<div class="remark">
<b>Remark:</b>
1. We usually use square brackets around the argument of a functional; we would write \(S[x]\) instead of \(S(x)\).

</div>

