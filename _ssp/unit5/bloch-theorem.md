---
layout: lesson
title: Bloch's Theorem
dept: physics
course: ssp
unit: unit5
deptDisplay: Physics
courseDisplay: Solid State Physics
unitDisplay: Unit 5
---

In this section, we will derive one of the most important results in solid state physics. It places a strong restriction on the type of wave functions that electrons are allowed to have in solids. Consider the Schrödinger equation for a single electron (the electron does not interact with other electrons in the solid). The electron moves in the presence of a periodic potential $V(\r)$ created by the atoms. This means that, for any lattice vector $\textbf{R}$, we have $V(\r+\textbf{R}) = V(\r)$. We know from Fourier theory that any periodic function can be expanded in terms of complex exponentials. The expansion looks like

$$V(\r) = \sum_{\k} V_\k e^{i\k\cdot\r}$$

where the coefficients $V_\k$ are given by 

$$V_\k = \frac{1}{V} \int_V V(\r) e^{-i\k\cdot\r} d^3\r$$

and the integral is taken over the unit cell. 













