---
layout: lesson
title: Quantum harmonic oscillator II 
dept: physics
course: qm-I
unit: unit3
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 3
---
In this section, we will apply a much more elegant technique to find the eigenvalues and eigenstates of the harmonic oscillators. Starting from the classical Hamiltonian

$$\begin{equation}
H = \frac{p^2}{2m} + \frac{1}{2}m\omega^2x^2
\end{equation}$$

we promote \\(p\\) and \\(x\\) to operators, so the quantum Hamiltonian is given by

$$\begin{equation}
\hat{H} = \frac{\hat{p}^2}{2m} + \frac{1}{2}m\omega^2\hat{x}^2.
\end{equation}$$

We simplify the Hamiltonian by factoring it. Note that a usual factoring (as difference of squares) is not possible because \\([\hat{x},\hat{p}]\neq 0\\). Thus, we write the factoring, and add a correction term to account for the non-commutation:

$$\begin{align}
\hat{H} ={}& \frac{1}{2m}(\hat{p}^2+ m^2\omega^2 \hat{x}^2) \\
={}& \frac{1}{2m}\left((-i\hat{p} + m\omega \hat{x})(ip+m\omega\hat{x}) - m\omega\hat{x} i\hat{p} + i\hat{p}m\omega\hat{x}\right) \\
={}& \frac{1}{2m}((-i\hat{p} + m\omega\hat{x})(i\hat{p} + m\omega\hat{x}) - im\omega[\hat{x},\hat{p}]) \\
={}& \frac{1}{2m}((-i\hat{p} + m\omega\hat{x})(i\hat{p} + m\omega\hat{x}) + m\omega\hbar) \\
={}& \hbar\omega\left(\frac{(-i\hat{p} + m\omega\hat{x})(i\hat{p} + m\omega\hat{x})}{2\hbar\omega m} + \frac{1}{2}\right) \\
={}& \hbar\omega\left(\left(\frac{-i\hat{p} + m\omega\hat{x}}{\sqrt{2\hbar\omega m}}\right)\left(\frac{i\hat{p} + m\omega\hat{x}}{\sqrt{2\hbar\omega m}}\right) + \frac{1}{2}\right)
\end{align}$$

which leads us to define 

$$\begin{equation}
\ahat^\dagger = \frac{1}{\sqrt{2\hbar m\omega}}(-i\hat{p} + m\omega\hat{x}),\qquad \ahat = \frac{1}{\sqrt{2\hbar m\omega}}(i\hat{p} + m\omega\hat{x})
\end{equation}$$

Thus, the Hamiltonian is rewritten as 

$$\begin{equation}
\hat{H} = \hbar\omega\left(\ahat^\dagger\ahat+\frac{1}{2}\right).
\end{equation}$$

This tells us that \\(E\_n = \hbar\omega(n+1/2)\\). 

INSERT SOME DISCUSSION



We can invert the relations for the creation/annihilation operators to find that 

$$\begin{equation}
\xhat = \sqrt{\frac{\hbar}{2m\omega}}(\ahat+\ahat^\dagger),\quad \phat = i\sqrt{\frac{\hbar m\omega}{2}}(\ahat^\dagger-\ahat)
\end{equation}$$

