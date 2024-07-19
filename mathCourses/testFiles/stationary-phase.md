---
layout: page
title: Stationary Phase
course: test
unit: unit1
permalink: /test/stationary-phase/
---

In this section, we will show how to evaluate integrals by the method of stationary phase. Consider the integral 

$$I = \int_{-\infty}^\infty e^{iz\phi(t)} f(t) dt,\qquad z\gg 1.$$

If $z \gg 1$, then if $\phi$ changes by even a little bit, then $z\phi$ changes by a lot, so that there are rapid oscillations in $e^{iz\phi}$. These rapid oscillations cause cancellations in the integral, so, as long as $\phi'(t)$ is not too small, there is a near zero contribution to the integral. Thus, we will only consider the integral in the neighbourhood of $t_\*$, where $\phi'(t_\*) = 0$. This is where the phase is stationary, hence, *stationary phase*. 

The integral is then approximated by Taylor expanding $\phi$ about $t_\*$. The function $f$ is evaluated at the point $t_\*$. For ease of notation, define $f_\* = f(t_\*)$, $\phi_\* = \phi(t_\*)$, and $\phi''_\* = \phi''(t_\*)$. The leading order approximation to the integral is thus 

$$I \sim \int_{-\infty}^\infty f(t_*)e^{iz[\phi(t_*) + (t-t_*)^2\phi''(t_*)/2]} dt$$

If we factor out the terms not depending on $t$, then we are left with a Fresnel type integral. To evaluate it, make the substitution $u = (t-t_\*)\sqrt{\|z\phi''_\*\|/2}$. This gives us 

$$I \sim f(t_*) e^{i\phi_*}\int_{-\infty}^\infty e^{i\sgn(\phi''_*)u^2}\sqrt{\frac{2}{z|\phi''_*|}} du $$

We now rewrite the complex exponential using Euler's identity so that we can see the Fresnel integrals. 

$$I \sim f(t_*) e^{i\phi_*}\sqrt{\frac{2}{z|\phi''_*|}} \left( \int_{-\infty}^\infty \cos(u^2) du + \sgn(\phi''_*)\int_{-\infty}^\infty \sin(u^2) du \right)$$

The integrals are famously (show derivation here) each equal to $\sqrt{\pi/2}$, 

$$\int_{-\infty}^\infty \cos(u^2) du = \int_{-\infty}^\infty \sin(u^2) du = \sqrt{\frac{\pi}{2}}.$$

This yields the following leading order approximation to the integral. 

$$I \sim f(t_*) e^{i\phi_*}\sqrt{\frac{2\pi }{z|\phi''_*|}} \left(\frac{1}{\sqrt{2}} + i\frac{\sgn(\phi''_*)}{\sqrt{2}}\right)$$

If we rewrite this with complex exponential form, we get a phase shift. 

$$I \sim f(t_*) e^{i\phi_* + i\sgn(\phi''_*)\pi/4}\sqrt{\frac{2\pi }{z|\phi''_*|}}.$$

### Examples

