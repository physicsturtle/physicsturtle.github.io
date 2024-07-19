---
layout: page
title: Lagrangian for the Electromagnetic Field
course: test
unit: unit1
permalink: /test/em-lagrangian/
---

The Lagrangian density for the electromagnetic field is

$$\mathscr{L} = -\frac{1}{4}F_{\mu\nu} F^{\mu\nu},$$

where the Faraday tensor $F$ has components defined by 

$$F_{\mu \nu} = \partial_\mu A_\nu - \partial_\nu A_\mu.$$

From this, we can calculate an action $S$, which is given by 

$$S = \int-\frac{1}{4}F_{\mu\nu} F^{\mu\nu} d^4\textbf{x}.$$

There will be 4 coupled PDEs for this action! Let's see how calculating the Euler-Lagrange equations for this action can produce Maxwell's equations. 

The Euler-Lagrange equations are (for $\mu = 0,1,2,3$)

$$\frac{\partial\mathscr{L}}{\partial A_u} - \frac{\partial}{\partial x^\nu}\frac{\partial\mathscr{L}}{\partial(\partial_n A_\mu)} = 0.$$

There is no explicit dependent on the vector potential $A_\mu$ itself, but rather only on its derivatives. 









