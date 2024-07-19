---
layout: exercises
title: Derivatives of Trigonometric Functions - Exercises
dept: math
course: calculus-I
unit: unit3
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 3
---

### Exercises

Finally, the last limit that we will compute is the derivative of $f(x) = \cos x$. 

$$\begin{eqnarray*}
\frac{d}{dx}\cos x &=& \lim_{h\to 0} \frac{\cos(x+h) - \cos x}{h} \\
&=& \lim_{h\to 0} \frac{\cos x \cos h - \sin x \sin h - \cos x}{h} \\
&=& \lim_{h\to 0} \frac{\cos x (\cos h - 1) - \sin x \sin h}{h} \\
&=& \lim_{h\to 0} \frac{\cos x (\cos h - 1)}{h}  - \lim_{h\to 0} \frac{\sin x \sin h}{h} \\
&=& \cos x\lim_{h\to 0} \frac{\cos h - 1}{h}  - \sin x\lim_{h\to 0} \frac{\sin h}{h} \\
&=& -\sin x
\end{eqnarray*}$$


