---
layout: page
title: Simple Harmonic Oscillator
course: test
unit: unit1
permalink: /test/simple-harmonic-oscillator/
---

In this lesson, we will outline how the simple harmonic oscillator that was discussed in elementary quantum mechanics can be explained in a context appropriate for quantum field theory. We imagine a quantum particle moving in a potential given by 

$$V(x) = \frac{1}{2}\omega^2 m x^2.$$

This potential is the same as the one in classical mechanics for a particle on the end of a spring, and we of course need to work with energies instead of forces; we are doing quantum mechanics after all! The Schrödinger equation for the system is then simply 

$$\left(-\frac{\hbar^2}{2m}\frac{d^2}{dx^2} + \frac{1}{2}\omega^2 m x^2\right)\psi = E\psi.$$

If one solves this differential equation with the boundary conditions $\psi(\pm\infty) = 0$, then the (normalized) solutions turn out to be 

$$\psi_n(\xi) = \frac{1}{2^n n!}\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}H_n(\xi) e^{-\xi^2/2}.$$

where

* $H_n(\xi)$ is the Hermite polynomial of order $n$,
* $\xi = \sqrt{\frac{m\omega}{\hbar}}x$.




