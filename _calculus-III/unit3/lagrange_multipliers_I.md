---
layout: lesson
title: Lagrange Multipliers 1
dept: math
course: calculus-III
unit: unit3
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 3
---

The method of *Lagrange Multipliers*  is  mathematical tool for optimizing functions with respect to a constraint on the independent variables. This has many physical and mathematical applications. Suppose there is an irregularly shaped surface, and we want to find the point on that surface which is closest to the origin in \\(\mathbb{R}^3\\). This problem concerns minimizing the function \\(f(x,y,z) = x^2 + y^2 + z^2\\) (distance from the origin squared), when the point we're measuring the distance to is constrained to the surface given.

To begin the analysis, let's restrict ourselves to functions of only two variables. Suppose we have a function \\(z = f(x,y)\\) which we want to minimize or maximize, subject to the constraint \\( g(x,y) = c\\). Graphing \\(f\\) gives us a surface, and the constraint is actually a curve in the plane. This curve can be swept upwards, and since \\(g\\) is independent of \\(z\\), it holds at any point on the \\(z\\) axis. We then look at the curve of intersection between the surfaces \\(f\\) and \\(g\\). Flattening out this curve, we can see the problem we're trying to solve: find the minimum and maximum along this curve! 

\subsection{Analysis of the Problem}
This problem can be solved by creating contour plots of the function we need to optimize. The constraint \\(g\\) can be drawn as a curve in the \(\xy\\) plane. Suppose we want to optimize the function \\(f\\), whose level sets are shown. We want to find the level set of the smallest value of \\(f\\) for which \\(f\\) still satisfies the constraint. If we look at the level set for \(\f = 6\\), we see that there exist smaller values of \(f\) for which the constraint is still satisfied! We can then proceed to \\(f = 4\\), but then there are still further smaller values of \\(f\\) for which the constraint is satisfied! Continuing down until we are on the level set \(f = 2\), we see that if we continued for any smaller value of \(f\), we would no longer be able to satisfy the constraint. We therefore conclude that the level set of the function \\(f\\) must be tangent to the curve given by the constraint \(g\). An equivalent statement to this is that the normal vectors to the two curves are parallel, so \\(\nabla f = \lambda \nabla g\\) for some real number \\(\lambda\\). An identical argument can be applied if we wish to maximize the function \\(f\\) subject to a constraint \(g\). the scalar \(\\lambda\\) is called the \textit{Lagrange Multiplier}.

To find the minimum/maximum points of a function \(f\) with respect to a constraint \(g\), we need to solve the system of equations \(\nabla f = \lambda \nabla g\), and \(g = c\), for \(x,y,\lambda\). This may look like only two equations, but it is actually 3 equations, because the gradient is a vector equation.

$$
\begin{eqnarray}
f_x(x,y) &=& \lambda g_x(x,y)\\
f_y(x,y) &=& \lambda g_y(x,y)\\
g(x,y) &=& k
\end{eqnarray}  $$

Example1: Find the maximum and minimum values of the function \(f(x,y) = 2x^2 + 3y^2\) subject to \(xy = 1\)

\begin{solution}
We begin by identifying that constraint is \(g(x,y) = xy\). Then we compute the gradient of both functions:
\[\nabla f = \langle 4x , 6y \rangle \]
\[\nabla g = \langle y, x \rangle \]
Then setting up the Lagrange multipliers equation, we have 
\[\langle 4x, 6y = \lambda \langle y , x \rangle \]
Which gives us the three equations 
\begin{displaymath}
\left\{
\begin{array}{c}
4x= \lambda y\\
6y = \lambda x \\
xy = 1
\end{array}
\right.
\end{displaymath}
Assuming that \(\lambda \not= 0\), we can divide the first two equations to obtain
\[\frac{2x}{3y} = \frac{y}{x} \Rightarrow 2x^2 = 3y^2\]
Then multiplying the equation on both sides by \(y^2\), we have 
\[2x^2y^2 = 3y^4 = 2, \]
because we used the constraint \(xy = 1\). Thus we get \(y = \pm \sqrt{\frac{2}{3}}\), and \(x = \pm \sqrt{\frac{3}{2}}\), thus our two solutions are 
\[(x,y) = \left(\sqrt{\frac{3}{2}}, \sqrt{\frac{2}{3}}\right),\quad   \left(-\sqrt{\frac{3}{2}}, -\sqrt{\frac{2}{3}}\right)\]
We see the graphic to confirm that these solutions do indeed satisfy the condition of extremal points. Examining the level sets also confirms that they are tangent at these particular points. The level set of \(f\) that is tangent to \(g = 1\) happens to be the set \(f = 5\). This is obtained by plugging back our values into the function \(f\). 
\end{solution}

Example 2: Find the maximum and minimum values of the function \(f(x,y) =  \) on the unit disk \(x^2 + y^2 \leq 1\). 

\begin{solution}
To solve this problem, we will have to use optimization techniques learned before to find any extremal values inside the disk, and use Lagrange multipliers to find any extremal values on the edge of the disk. 
\end{solution}


### Exercises

<ol>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
<li> <div> Sketch all of the points such that \(y = 1\). </div>

<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer">
This is a plane that is parallel to the \(xz\) plane. 
</div> </li>
</ol>
