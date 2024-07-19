---
layout: lesson
title: Non-Normalizable Wave Functions
course: quantum-mechanics-I
unit: unit1
---

In this section, we discuss the concept of normalization of a wavefunction when the integral
$$\int_{-\infty}^\infty |\psi|^2 dx $$
does not actually converge. One may say that these are not physically realizable wave functions, but in fact many important problems involve wave functions which cannot be normalized. For example, if we have a free particle, then its wavefunction will not be normalizable! Let's consider the free particle as an example. 

### Normalization in the $k$ Scale
For a free particle, the Schrödinger equation is 

$$-frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} = E\psi$$

but this has no boundary conditions. It's solution is thus just complex exponentials expressed in terms of a wavenumber $k = \sqrt{2mE}/\hbar^2$. 

$$\psi_k(x) = Ae^{ikx} + Be^{-ikx}$$

Let's focus for now only on the rightward propagating wave and set $\psi_k(x) = Ae^{ikx}$. Immediately, we notice that 

$$\int_{-\infty}^\infty|\psi_k(x)|^2 dx A^2\int_{-\infty}^\infty 1 dx$$

which is a divergent integral; the integrand does not ever decay to zero. This leads us rethink our idea of orthonormality for continuum wave functions. In cases like the infinite square well, we had that 

$$\int_{-\infty}^\infty \psi_m^*(x)\psi_n(x) dx = \delta_{mn}$$

which meant that if we summed over $m$, then we would get 

$$\int_{-\infty}^\infty \psi_n^*(x)\psi_n(x) dx = 1$$

Let's use this approach of stepping back to the orthogonality relation to help us with the normalization of $\psi_k(x)$. The difference between the indices $k$ and $n$ is that $k$ is continuous while $n$ was discrete; $n$ needed to be an integer while $k$ can be any real number. For continuous indices, the analogue of the Kronecker delta function is the Dirac delta function. The appropriate orthonormality relation is 

$$\begin{equation} \label{continuousOrthonormality} \int_{-\infty}^\infty \psi_k^*(x)\psi_{k'}(x) dx = \delta(k-k'). \end{equation} $$

This orthonormality relation is quite difficult to derive because we're no longer dealing with functions but rather distributions (the Dirac delta function is not really a function). We can however still use this to calculate a normalization constant $A$. We consider integrating both sides of $\eqref{continuousOrthonormality}$ with respect to $k'$ over a range such that we enclose $k$. To do this, define $\Delta k = \|k-k'\|$, so 

$$\int_{k-\Delta k}^{k + \Delta k} \int_{-\infty}^\infty \psi_k^*(x)\psi_{k'}(x) dx dk' = 1.$$

We now consider swapping the order of integration so that we get 

$$\int_{-\infty}^\infty \psi_k^*(x)\int_{k-\Delta k}^{k + \Delta k} \psi_{k'}(x) dk' dx = 1.$$

Note that we can pull $\psi_k(x)$ outside of the $k'$ integral because it has no $k'$ in it. Let's apply this to the wave function that we defined before. First we evaluate the $k'$ integral. 

$$\begin{eqnarray*}
\int_{k - \Delta k}^{k + \Delta k} Ae^{ik'x} dk' &=& \frac{A}{ix} \left(e^{i(k - \Delta k)x} - e^{i(k+\Delta k)x}\right) \\
&=& \frac{2Ae^{ikx}}{x}\sin(x\Delta k)
\end{eqnarray*}$$

Now, we plug this into the $x$ integral

$$\begin{eqnarray*}
\int_{-\infty}^\infty A^*e^{-ikx} \frac{2Ae^{ikx}}{x}\sin(x\Delta k) dx &=& 1\\
2|A|^2 \int_{-\infty}^\infty \frac{1}{x}\sin(x\Delta k) dx &=& 1\\
2|A|^2 \int_{-\infty}^\infty \frac{\sin y}{y} dy &=& 1\\
2|A|^2 \pi &=& 1
\end{eqnarray*}$$

where we made a variable substitution $y = x\Delta k$, and recalled that

$$\int_{-\infty}^\infty \frac{\sin x}{x} dx = \pi.$$

Thus the normalization constant is 

$$A = \frac{1}{\sqrt{2\pi}}.$$

We note that we expect the normalization to be independent of $\Delta k$ because the normalization of $\phi_k(x)$ should depend only on $k$, and have nothing to do with the $k'$ of some other wave function. In this case it just so happens that the constant $A$ is also independent of $k$, but this need not always be the case. 



### Normalization in the $E$ scale
The normalization of a continuum wave function is not unique! It depends on 
