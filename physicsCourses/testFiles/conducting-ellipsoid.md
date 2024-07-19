---
layout: page
title: Conducting Ellipsoid
course: test
unit: unit1
permalink: /test/conducting-ellipsoid/
---

Here, let's study the conducting ellipsoid. 


The charge density is then 
$$\sigma = \frac{Q}{4\pi abc}\left(\frac{x^2}{a^4} + \frac{y^2}{b^4} + \frac{z^2}{c^4}\right)^{-1/2}$$

Exercise: Confirm that the charge density integrates to $Q$. 

We are interested in evaluating the surface integral
$$\iint_S \sigma dS$$
over the surface 
$$\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1.$$

To do this, let's first parametrize our surface by writing $x = ua$, $y = vb$, and $z = c\sqrt{1-u^2-v^2}$: 
$$\textbf{r} = \left<au,bv,c\sqrt{1-u^2-v^2}\right>$$
Next, we need to find the area element. 
$$\textbf{r}_u = \left<a,0,\frac{-cu}{\sqrt{1-u^2-v^2}}\right>,\qquad \textbf{r}_u = \left<0,b,\frac{-cv}{\sqrt{1-u^2-v^2}}\right>$$

Then, our area element can be written as 

$$d\textbf{S} = |\textbf{r}_u\times\textbf{r}_v| dudv = \left<\frac{bcu}{\sqrt{1-u^2-v^2}}, \frac{-acv}{\sqrt{1-u^2-v^2}}, 0\right>$$

and the scalar area element is 

$$\nabla f = \left< \frac{-xc}{a^2\sqrt{1 - \frac{x^2}{a^2} - \frac{y^2}{c^2}}}, \frac{-yc}{b^2\sqrt{1 - \frac{x^2}{a^2} - \frac{y^2}{c^2}}}\right>$$

$$\begin{eqnarray}
dS &=& \sqrt{1 + |\nabla f|^2} dxdy \\
&=& \sqrt{1 + \frac{x^2c^2}{a^4\left(1-\frac{x^2}{a^2} - \frac{y^2}{b^2}\right)} +  \frac{y^2c^2}{b^4\left(1-\frac{x^2}{a^2} - \frac{y^2}{b^2}\right)}} dxdy\\
&=& \sqrt{1 - \frac{x^2}{a^2} - \frac{y^2}{b^2} + \frac{x^2c^2}{a^4} +  \frac{y^2c^2}{b^4}}\left(1 - \frac{x^2}{a^2} - \frac{y^2}{b^2}\right)^{-1/2} dxdy\\
&=& c\sqrt{\frac{z^2}{c^4}+ \frac{x^2}{a^4} +  \frac{y^2}{b^4}}\left(1 - \frac{x^2}{a^2} - \frac{y^2}{b^2}\right)^{-1/2} dxdy\\
\end{eqnarray} $$

When plugging this into the integral, we get

$$\begin{eqnarray}
\iint\sigma ds &=& \iint \frac{Q}{4\pi abc}\left(\frac{x^2}{a^4} + \frac{y^2}{b^4} + \frac{z^2}{c^4}\right)^{-1/2} c\sqrt{\frac{z^2}{c^4}+ \frac{x^2}{a^4} +  \frac{y^2}{b^4}}\left(1 - \frac{x^2}{a^2} - \frac{y^2}{b^2}\right)^{-1/2}  dxdy\\
&=& \iint \frac{Q}{4\pi ab}\left(1 - \frac{x^2}{a^2} - \frac{y^2}{b^2}\right)^{-1/2}  dxdy\\
&=& \frac{Q}{4\pi} \iint \sqrt{1-u^2-v^2} dudv\\
&=& Q
\end{eqnarray}$$

Exercise: Find the potential created by this ellipsoid. 

Now we are interested in evaluating the integral

$$V(\textbf{x}) = \frac{1}{4\pi\epsilon_0} \iint \frac{\sigma(\textbf{x}')}{|\textbf{x} - \textbf{x}'|} dS$$

Through a similar procedure to above, we can calculate: 

$$\begin{eqnarray}
V(\textbf{x}) &=& \frac{Q}{4\pi ab} \frac{1}{4\pi\epsilon_0} \iint \frac{1}{\sqrt{(x-x')^2 + (y-y')^2 + (z-z')^2}} \sqrt{1 - \frac{x^2}{a^2} - \frac{y^2}{b^2}}dxdy\\
&=& 


\end{eqnarray}$$





