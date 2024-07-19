---
layout: page
title: Thermodynamics
course: test
unit: unit1
permalink: /test/thermodynamics/
---

The first law of thermodynamics is 

$$dU = TdS - PdV + \mu dN.$$

In general, if one has a function $f(x,y)$ of two variables, $x$ and $y$, its differential is 

$$df = \frac{\partial f}{\partial x}\bigg|_ydx + \frac{\partial f}{\partial y}\bigg_x dy

where the subscripts on the partial derivatives are written to make clear which variables are being held constant. This tells us three things about the internal energy $U$. 

1 $U$ is a function of $S$ and $V$.

2 $\frac{\partial U}{\partial S}\bigg|_{V,N} = T$.

3 $\frac{\partial U}{\partial V}\bigg|_{S,N} = -P$. 

4 $\frac{\partial U}{\partial N}\bigg_{S,V} = \mu$. 

<div class="example">
<p><b>Example:</b> Calclulate the temperature of the system with internal energy and thereby express the internal energy in terms of temperature. $C$ is a constant. 
$$U = C\left(\frac{e^{S/nR}}{V}\right)^{2/3}$$ </p>
The temperature is given by 
$$T = \frac{\partial U}{\partial S}\bigg_V = \frac{2}{3}\frac{C}{nR}\left(\frac{e^{S/nR}}{V}\right)^{2/3} = \frac{2U}{3nR}$$
Thus, the internal energy in terms of temperature is 
$$U = \frac{3nRT}{2}$$
</div>
