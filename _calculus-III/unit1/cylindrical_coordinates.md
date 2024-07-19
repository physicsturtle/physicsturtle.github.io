---
layout: lesson
title: Cylindrical Coordinates
dept: math
course: calculus-III
unit: unit1
deptDisplay: Math
courseDisplay: Calculus III
unitDisplay: Unit 1
---

Here we will define cylindrical coordinates. If you have learned about polar coordinates in single variable calculus, then this discussion will be a direct extension of polar coordinates to three dimensions. In cylindrical coordinates, the three variables are
<ol>
<li> $r$, the distance from the $z$ axis </li>
<li> $\varphi$, the angle measured in the $xy$ plane from the postiive $x$ axis. </li>
<li> $z$ the height above the $xy$ plane. </li>
</ol>

The cylindrical coordinate system is shown in the figure below.

(insert figre here)

We will need to learn how to transform between the cylindrical coordinate system and the cartesian coordinate system. We will provide a few basic formulas here, but postpone the transformation of things like basis vectors to later. If we have a point $x,y,z$ in 3D space, then its corresponding cylindrical coordinates are 

$$\begin{cases}
r = \sqrt{x^2+y^2} \\
\varphi = \arctan\frac{y}{x} \\
z = z \end{cases}$$

A quick remark about the formula for $\varphi$. The above formula is not technically correct for all values of $\varphi$. If $x = y = -1$, then $y/x =1$, which is the same as when $x = y = 1$. Thus we get the same value for $\varphi = \pi/4$. However, we want to assign the value $\varphi = 5\pi/4$ when $x = y = -1$! Additionally, we restrict the output of $\arctan$ to always lie between $-\pi/2$ and $\pi/2$. To ammend this formula to give correct values for negative $x$, and to allow $\varphi$ to range between $-\pi$ and $\pi$, we can instead write 

$$\varphi = \begin{cases}
\arctan\frac{y}{x} & x > 0\\
\arctan\frac{y}{x} + \pi & x < 0, y\geq 0\\
\arctan\frac{y}{x} - \pi & x < 0, y\leq 0\\
\frac{\pi}{2} & x = 0, y > 0 \\
-\frac{\pi}{2} & x  = 0, y < 0 \\
\end{cases}$$

To transform back to cartesian from cylindrical, the formulas are

$$\begin{cases}
x = r\cos\varphi\\
y = r\sin\varphi \\
z = z \end{cases}$$
