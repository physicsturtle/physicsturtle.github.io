---
layout: page
title: Logarithms
course: test
unit: unit1
permalink: /test/logarithms/
---

Non-Local Contributions -- Logarithms

Suppose we have the integral 
$$I = \int_0^\infty f(x,\epsilon) dx$$

where the integrand has a special power dependence behaviour in the region $\epsilon \ll x \ll 1$.

$$f(x,\epsilon) = \left\{
\begin{array}{cc}
O(\epsilon^{-\alpha}) & \text{for}\, x = O(\epsilon)\\
O(x^{-\alpha}) & \text{for}\, \epsilon \ll x \ll 1\\
O(1) & \text{for}\,x = O(1)
\end{array}
\right. $$

For example, consider
$$f(x,\epsilon) = \frac{1}{(x+\epsilon)^\alpha(1+x)}$$

(reference hinch)

The case $\alpha = 1$ means that the dominant contribution is neither for $x = O(1)$ nor $x = O(\epsilon)$. Thus it is useful to split the integral up into three regions. Consider the integral

$$I = \int_0^\infty \frac{dx}{(x+\epsilon)(1+x)}.$$

Now, we want to split the integral up into three regions: $[0,\delta_1]$, $[\delta_1,\delta_2]$, and $[\delta_2,\infty)$, where $\delta_1 \ll \epsilon\ll 1 \ll \delta_2$. 

$$\begin{eqnarray}
I &=& \int_0^\infty  \frac{dx}{(x+\epsilon)(1+x)}\\
&=& \underbrace{\int_0^{\delta_1}  \frac{dx}{(x+\epsilon)(1+x)}}_{I_1} + \underbrace{\int_{\delta_1}^{\delta_2}  \frac{dx}{(x+\epsilon)(1+x)}}_{I_2}+ \underbrace{\int_{\delta_2}^\infty  \frac{dx}{(x+\epsilon)(1+x)}}_{I_3}\\
\end{eqnarray}$$

Let's start with $I_1$. This one requires a rescaling: $x = \epsilon X$. In this region, $x/\epsilon\ll 1$, so we can use a Taylor expansion. 

$$\begin{eqnarray}
I_1 &=& \int_0^{\delta_1}  \frac{dx}{(x+\epsilon)(1+x)} \\
&=&  \int_0^{\delta_1/\epsilon}  \frac{dX}{(X+1)(1+\epsilon X)} \\
&=&  \int_0^{\delta_1/\epsilon}  \frac{dX}{(X+1)(1+\epsilon X)} \\
&=&  \int_0^{\delta_1/\epsilon}  \frac{dX}{(X+1)}\left(1 - \epsilon X + \epsilon^2 X^2 +\cdots \right) \\
&=&  \int_0^{\delta_1/\epsilon}  \frac{dX}{(X+1)} - \epsilon \int_0^{\delta_1/\epsilon} \frac{XdX}{X+1}  + \cdots  \\
&=&  \left.\log(X+1)\right|^{\delta_1/\epsilon}_0 - \epsilon\left.\left(X - \log(X+1)\right)\right|^{\delta_1/\epsilon}_0 + \cdots  \\
&=&  \log(1+\delta_1/\epsilon) - \epsilon(\delta_1/\epsilon - \log(1+\delta_1/\epsilon)) + \cdots  \\
\end{eqnarray}$$

Now, we do $I_2$. In this region, $\epsilon \ll x \ll 1$. We Taylor expand both terms:

$$\begin{eqnarray}
I_2 &=& \int_{\delta_1}^{\delta_2} \frac{dx}{(x+\epsilon)(1+x)}\\
&=&  \int_{\delta_1}^{\delta_2} \frac{dx}{x(1+\epsilon/x)(1+x)}\\
&=&  \int_{\delta_1}^{\delta_2} \frac{dx}{x}\left(1-\frac{\epsilon}{x} + \frac{\epsilon^2}{x^2} + \cdots )\right)\left(1-x + x^2 + \cdots\right)\\
&=& 
\end{eqnarray}$$

Finally, we do $I_3$. In this region, $\epsilon/x \ll 1$. 

$$\begin{eqnarray}
I_3 &=& \int_{\delta_2}^\infty \frac{dx}{(x+\epsilon)(1+x)}\\
&=& \int_{\delta_2}^\infty \frac{dx}{x(1+\epsilon/x)(1+x)}\\
&=& \int_{\delta_2}^\infty \frac{dx}{x(1+x)}\left(1 - \frac{\epsilon}{x} + \frac{\epsilon^2}{x^2} + \cdots\right)\\
&=&  \int_{\delta_2}^\infty \frac{dx}{x(1+x)} - \epsilon\int_{\delta_2}^\infty  \frac{dx}{x^2 (1+x)}  + \cdots\\
&=&  \left.\log\left(\frac{x}{x+1}\right)\right|^\infty_{\delta_2} - \epsilon\left.\left[\log\left(\frac{x+1}{x}\right) -\frac{1}{x} \right]\right|^\infty_{\delta_2} + \cdots\\
\end{eqnarray}$$





Now consider the alternative integral as $\epsilon\to 0$:

$$I = \int_0^\infty \frac{dx}{\sqrt{\epsilon + x^2}(1+x^2)}$$

There are three regions of interest. $x\ll\sqrt{\epsilon}$, $\sqrt{\epsilon}\ll x \ll 1$, and $1 \ll x$. We will need to break the integral up into the contributions from these three regions. 




(put gross question from number 5 assignment 3)
N(z) = \frac{\sin z}{z} - \sin(1) + \text{Ci}(1) - \text{Ci}(z) - \epsilon\left[\frac{1}{3}\left(\frac{\sin z}{z^3} -\sin(1)\right) + \frac{1}{6}\left(\frac{\cos z}{z^2} - \cos(1)\right) + \frac{1}{6}\left(\frac{\sin z}{z} - \sin(1) + \text{Ci}(1) - \text{Ci}(z)\right)\right] for z = O(1)

and then for z < O(1), 

N(z) = 1 - \sin(1) + \text{Ci}(1) - \gamma - \log(\sqrt{z^2+\epsilon}) + \frac{z^2}{12} - \epsilon\left[\frac{\log(\sqrt{z^2+\epsilon})}{12} + \frac{\sin(1)}{6} + \frac{2}{3} + \cos(1) + \text{Ci}(1) - \gamma\right]
