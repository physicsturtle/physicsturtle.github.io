---
layout: page
title: Quantum Harmonic Oscillator
course: test
unit: unit1
permalink: /test/quantum-harmonic-oscillator/
---

In this lesson, we will discuss the quantum mechanical analogue of the harmonic oscillator. In classical mechanics, we solved Newton's equation for the force $F(x) = -kx$, where $k$ is some spring constant. The corresponding potential energy is found by integrating up

$$\frac{dV}{dx} = -F(x),$$

which gives us the potential 

$$V(x) = \frac{1}{2}kx^2.$$

It is important that we have the potential because, in quantum mechanics, the fundamental equation is the Schrödinger equation. The Schrödinger equation does not have a force term, but rather the potential energy. This means that the appropriate (time independent) Schrödinger equation is

$$\left(-\frac{\hbar^2}{2m}\frac{d^2}{dx^2} + \frac{1}{2}kx^2\right)\psi = E\psi.$$

In quantum mechanics, there isn't an analogue of spring constant, so instead, we use the equation for the resonant frequency $\omega^2 = k/m$ to substitute in for $k$. This gives us the equation we actually want to solve:

<div class="result">
<p><b>Quantum Harmonic Oscillator Schrödinger Equation:</b></p>
For a quantum harmonic oscillator of frequency $\omega$, the Schrödinger equation is
$$\left(-\frac{\hbar^2}{2m}\frac{d^2}{dx^2} + \frac{1}{2}\omega^2m x^2\right)\psi = E\psi.$$
Since the wave function should decay at infinity (we want it to be normalizable!), we set the boundary conditions simply to be
$$\lim_{x\to\pm\infty} \psi(x) = 0.$$
</div> <br>

Now, let's actually solve this equation! There are two approaches that we will perform here. 
* The first is much less elegant, but it is also more concrete; it is solving the differential equation by brute force. 
* The second is defining some useful operators known as the raising and lowering operators, which allows us to simplify the differential equation substantially. 

### Brute Force Approach (Solving the Differential Equation)

#### Massaging the Differential Equation

For the brute force approach, we just need to solve the differential equation! This is however easier said than done! Before moving on to actually solving it, let's rewrite the equation in terms of a dimensionless (unitless) variable $\xi$. To determine what this variable should be, rewrite the equation 

$$\left(-\frac{\hbar}{m\omega}\frac{d^2\psi}{dx^2} + \frac{\omega m}{\hbar} x^2 \psi\right) = \frac{2E}{\hbar\omega}\psi.$$

Notice that on the left hand side of the equation, we have the expression $\omega m x^2/\hbar$ in the denominator of the first term, and the same expression in the numerator of the second term (I know it isn't technically in the denominator of the first term because it is $dx^2$, not $x^2$, but for variable changing purposes it doesn't matter). This suggests the substitution

$$\xi = \sqrt{\frac{\omega m}{\hbar}} x.$$

Making this substitution, as well as defining a modified eigenvalue $\lambda = 2E/m\omega$, we get 

$$-\frac{d^2\psi}{d\xi^2} + \xi^2\psi = \lambda\psi.$$

This is now the differential equation that we want to solve. However, you have not likely seen this equation in your differential equations courses! To solve it, we need to make a substitution. This substitution makes this problem much easier, but a priori, there is no way to know what it is! There are various arguments from asymptotic analysis that one can make, but I will simply show you what the substitution is. The substitution is 

$$\psi(\xi) = u(\xi)e^{-\xi^2/2}.$$

Note that the substitution $\psi(\xi) = u(\xi)e^{\xi^2/2}$ also substantially simplifies the equation, but we reject it because it doesn't decay to zero at infinity. We calculate the derivatives of our substitution to find 

$$\psi'(\xi) = (-\xi u + u')e^{-\xi^2/2},\qquad \psi''(\xi) = (-u + \xi^2 u - 2\xi u' + u'')e^{-\xi^2/2}$$

Plugging in the second derivative to the equation, we find that 

$$-(-u + \xi^2 u - 2\xi u' + u'')e^{-\xi^2/2} + \xi^2 u e^{-\xi^2/2} = \lambda u e^{-\xi^2/2}$$

Cancelling all factors of $e^{-\xi^2/2}$ and simplifying, we get 

$$u + 2\xi u' - u'' = \lambda u.$$

Lastly, gathering like terms we get

$$u'' - 2\xi u' + (\lambda - 1)u =0.$$

#### Power Series Solution

Now, we need to solve this using a power series solution. The power series solution takes the form

$$u(\xi) = \sum_{n=0}^\infty a_n \xi^n = a_0 + a_1 \xi + a_2 \xi^2 + \cdots.$$

Substituting this into the differential equation, we get 

$$\sum_{n=2}^\infty n(n-1)a_n \xi^{n-2} -2\xi \sum_{n=1}^\infty na_n \xi^{n-1} + (\lambda-1) \sum_{n=0}^\infty a_n \xi^n = 0 $$

Next, we shift the indices of the first and second sums so that the powers of $\xi^n$ all match:

$$\sum_{n=0}^\infty(n+2)(n+1)a_{n+2} \xi^{n} -2\sum_{n=1}^\infty na_{n}\xi^{n} + (\lambda-1)\sum_{n=0}^\infty a_n \xi^n = 0$$

Now we peel off the $n=0$ terms from the first and third sums so that the sums all start at $n=1$.

$$\sum_{n=1}^\infty\left[(n+2)(n+1)a_{n+2}-2na_{n}+(\lambda-1) a_n \right]\xi^{n}+2a_{2}+(\lambda-1) a_{0} = 0$$

This gives us that $a_2 = -\frac{(\lambda-1) a_{0}}{2}$. The recurrence relation is: 

$$a_{n+2} = \frac{2n-(\lambda-1)}{(n+2)(n+1)}\cdot a_n,\qquad n\geq 2$$

Note that this also satisfies our extra condition $a_2 = -\frac{(\lambda-1) a_{0}}{2}$, so we can in fact define it for $n\geq 0$:

$$a_{n+2} = \frac{2n-(\lambda-1)}{(n+2)(n+1)}\cdot a_n,\qquad n\geq 0$$

This gives us two solutions. Set $a_0$ and $a_1$ arbitrary, then generate all further terms. Now, notice that for $n$ large, the recurrence relation is like 

$$a_{n+2}\sim \frac{2}{n}a_n,\qquad n\to\infty$$

the solution to which is $a_{n} \sim \frac{1}{(n/2)!}$, $n\to\infty$. This generates the coefficients for the power series 

$$e^{\xi^2} = \sum_{\stackrel{n=0}{n\,\text{even}}}^\infty \frac{\xi^{n}}{(n/2)!}$$

What this means for us, is that if we allow the recurrence relation to continue forever, we will get solutions like $u(\xi) \sim e^{\xi^2}$, which leads again to $\psi(\xi) = e^{\xi^2}e^{-\xi^2/2} = e^{\xi^2/2}$, which goes to infinity and is non-normalizable! Our conclusion is that our recurrence relation *must terminate*. The relation terminates if 

$$2n = \lambda - 1$$

for some $n$. This gives us the value for our eigenvalue $\lambda$. Thus, 

$$\lambda = 1 + 2n$$

Plugging back in our previous expression for $\lambda = 2E/\hbar\omega$, we finally get the energy eigenvalues for the system:

<div class="result">
  <b>Energy Eigenvalues for the Quantum Harmonic Oscillator:</b>
  $$E = \hbar\omega\left(\frac{1}{2} + n\right),\qquad n\geq 0$$
</div> <br>

The $n=0$ case is known as the *zero point energy* of the harmonic oscillator. Let's work now on the eigenfunctions of the system. The eigenfunctions corresponding to these eigenvalues are known as the Hermite polynomials, $H_n(\xi)$. If you want more information about the Hermite polynomials, consult a book on mathematical physics or special functions. 
























