---
layout: page
title: Classical Partition Function
course: test
unit: unit1
permalink: /test/classical-partition-function/
---

In classical statistical mechanics, the partition function is rather more difficult mathematically than in quantum statistical mechanics. In classical mechanics, there is a continuum of energies, while in quantum mechanics the energies are often discete. This means that when summing over states in classical statistical mechanics, we must actually calculate an integral as opposed to summing over discrete energies in quantum statistical mechanics. Let us take for example the classical harmonic oscillator.

<div class="definition">
<b>Definition:</b> Consider a classical system whose Hamiltonian is $H$. Then, the partition function is given by 
$$Z(\beta) = \int e^{-\beta H(\textbf{q},\textbf{p})} d\textbf{q}d\textbf{p}$$
</div>

<div class="example">
<p><b>Example:</b> Calculate the partition function of the classical harmonic oscillator with mass $m$ and angular frequency $\omega_0$. </p>
<b>Solution:</b> The Hamiltonian for the harmonic oscillator is 
$$H = \frac{p^2}{2m} + \frac{1}{2}m\omega_0^2 q^2.$$
Thus, the partition function is 
$$Z(\beta) = \int_{-\infty}^\infty \int_{-\infty}^\infty e^{-\beta(p^2/2m + m\omega_0^2 q^2/2)} dqdp$$
By the laws of exponentials and Fubini's theorem, this can be split up into two Gaussian integrals
$$Z(\beta) = \int_{-\infty}^\infty e^{-\beta p^2/2m} dp \int_{-\infty}^\infty e^{-\beta m \omega^2 q^2/2} dq$$
Each can be evaluated by use of the formula 
$$\int_{-\infty}^\infty e^{-ax^2} dx = \sqrt{\frac{\pi}{a}}.$$
Thus, the partition function is 
$$Z(\beta) = \sqrt{\frac{2\pi m}{\beta}}\sqrt{\frac{2\pi}{\beta m\omega_0^2}} = \frac{2\pi}{\beta\omega_0}.$$
</div>




















