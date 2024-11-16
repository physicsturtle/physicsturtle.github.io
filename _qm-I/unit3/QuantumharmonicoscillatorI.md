---
layout: lesson
title: Quantum harmonic oscillator I 
dept: physics
course: qm-I
unit: unit3
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 3
---
In classical mechanics, a simple harmonic oscillator is a system consisting of a mass \\(m\\) which experiences a <i>harmonic potential</i>, namely a quadratic potential. Typically, the potential energy is produced by a spring, whose restoring force is \\(F(x) = -kx\\), where \\(k\\) is the spring constant. The The corresponding potential energy is found by integrating the following equation:

$$\begin{equation}
\frac{\d V}{\d x} = -F(x),
\end{equation}$$

which gives us the potential 

$$\begin{equation}
V(x) = \frac{1}{2}kx^2.
\end{equation}$$

It is important that we have the potential because, in quantum mechanics, the fundamental equation is the Schrödinger equation. The Schrödinger equation is not expressed in terms of forces, but rather in terms of energies. This means that the appropriate (time independent) Schrödinger equation is

$$\begin{equation}
\left(-\frac{\hbar^2}{2m}\frac{\d^2}{\d x^2} + \frac{1}{2}kx^2\right)\psi = E\psi.
\end{equation}$$

In quantum mechanics, there isn't an analogue of spring constant, so instead, we use the equation for the resonant frequency \\(\omega^2 = k/m\\) to substitute in for \\(k\\). This gives us a simple rewriting of the equation

$$\begin{equation}
\left(-\frac{\hbar^2}{2m}\frac{\d^2}{\d x^2} + \frac{1}{2}\omega^2m x^2\right)\psi = E\psi.
\end{equation}$$

Since the wave function should decay at infinity (we want it to be normalizable!), we set the boundary conditions to be

$$\begin{equation}
\lim_{x\to\pm\infty} \psi(x) = 0.
\end{equation}$$

Now, let's actually solve this equation! There are two approaches that we will perform here. The first is much less elegant, but it is also more concrete; it is solving the differential equation by brute force. We will do the brute force approach first, because you will never want to use it again after you learn the second method. The second is defining some useful operators known as the raising and lowering operators, which allows us to simplify the differential equation substantially. This will be done in the next section. 

For the brute force approach, we just need to solve the differential equation! This is easier said than done. Before moving on to actually solving it, let's rewrite the equation in terms of a dimensionless (unitless) variable \\(\xi\\). To determine what this variable should be, rewrite the equation 

$$\begin{equation}
\left(-\frac{\hbar}{m\omega}\frac{\d^2\psi}{\d x^2} + \frac{\omega m}{\hbar} x^2 \psi\right) = \frac{2E}{\hbar\omega}\psi.
\end{equation}$$

Notice that on the left hand side of the equation, we have the expression \\(\omega m x^2/\hbar\\) in the denominator of the first term, and the same expression in the numerator of the second term (I know it isn't technically in the denominator of the first term because it is \\(\d x^2\\), not \\(x^2\\), but for variable changing purposes it doesn't matter). This suggests the substitution

$$\begin{equation}
\xi = \sqrt{\frac{\omega m}{\hbar}} x.
\end{equation}$$

Making this substitution, as well as defining a modified eigenvalue \\(\lambda = 2E/m\omega\\), we get 

$$\begin{equation}
-\frac{\d^2\psi}{\d\xi^2} + \xi^2\psi = \lambda\psi.
\end{equation}$$

This is now the differential equation that we want to solve. However, you have not likely seen this equation in your differential equations courses! To solve it, we need to make a substitution. This substitution makes this problem much easier, but a priori, there is no way to know what it is! There are various arguments from asymptotic analysis that one can make, but I will simply show you what the substitution is. The substitution is 

$$\begin{equation}
\psi(\xi) = u(\xi)e^{-\xi^2/2}.
\end{equation}$$

Note that the substitution \\(\psi(\xi) = u(\xi)e^{\xi^2/2}\\) also substantially simplifies the equation, but we reject it because it doesn't decay to zero at infinity. We calculate the derivatives of our substitution to find 

$$\begin{equation}
\psi'(\xi) = (-\xi u + u')e^{-\xi^2/2},\qquad \psi"(\xi) = (-u + \xi^2 u - 2\xi u' + u")e^{-\xi^2/2}
\end{equation}$$

Plugging in the second derivative to the equation, we find that 

$$\begin{equation}
-(-u + \xi^2 u - 2\xi u' + u")e^{-\xi^2/2} + \xi^2 u e^{-\xi^2/2} = \lambda u e^{-\xi^2/2}
\end{equation}$$

Cancelling all factors of \\(e^{-\xi^2/2}\\) and simplifying, we get 

$$\begin{equation}
u + 2\xi u' - u" = \lambda u.
\end{equation}$$

Lastly, gathering like terms we get

$$\begin{equation}
u" - 2\xi u' + (\lambda - 1)u =0.
\end{equation}$$

The standard technique for solving ordinary differential equations with constant coefficients (by trying the Ansatz \\(e^{rx}\\)) is not applicable here because there is a \\(\xi\\) coefficient on the \\(u'\\) term. However, we can solve such differential equations by using a <i>power series solution</i>. This technique involves substituting a power series with unknown coefficients into the differential equation, and then solving for the coefficients order by order. This will then yield a solution to the equation. The power series solution takes the form

$$\begin{equation}
u(\xi) = \sum_{n=0}^\infty a_n \xi^n = a_0 + a_1 \xi + a_2 \xi^2 + \cdots.
\end{equation}$$

Substituting this into the differential equation, we get 

$$\begin{equation}
\sum_{n=2}^\infty n(n-1)a_n \xi^{n-2} -2\xi \sum_{n=1}^\infty na_n \xi^{n-1} + (\lambda-1) \sum_{n=0}^\infty a_n \xi^n = 0.
\end{equation}$$

Next, we shift the indices of the first and second sums so that the powers of \\(\xi^n\\) all match:

$$\begin{equation}
\sum_{n=0}^\infty(n+2)(n+1)a_{n+2} \xi^{n} -2\sum_{n=1}^\infty na_{n}\xi^{n} + (\lambda-1)\sum_{n=0}^\infty a_n \xi^n = 0.
\end{equation}$$

Now we peel off the \\(n=0\\) terms from the first and third sums so that the sums all start at \\(n=1\\):

$$\begin{equation}
\sum_{n=1}^\infty\left[(n+2)(n+1)a_{n+2}-2na_{n}+(\lambda-1) a_n \right]\xi^{n}+2a_{2}+(\lambda-1) a_{0} = 0.
\end{equation}$$

This gives us that \\(a\_2 = -\frac{(\lambda-1) a\_{0}}{2}\\). The recurrence relation is: 

$$\begin{equation}
a_{n+2} = \frac{2n-(\lambda-1)}{(n+2)(n+1)}\cdot a_n,\qquad n\geq 1.
\end{equation}$$

Note that this also satisfies our extra condition \\(a\_2 = -\frac{(\lambda-1) a\_{0}}{2}\\), so we can in fact define it for \\(n\geq 0\\):

$$\begin{equation}
a_{n+2} = \frac{2n-(\lambda-1)}{(n+2)(n+1)} a_n,\qquad n\geq 0.
\end{equation}$$

This gives us two solutions. Set \\(a\_0\\) and \\(a\_1\\) arbitrary, then generate all further terms. Now, notice that for \\(n\\) large, the recurrence relation is like 

$$\begin{equation}
a_{n+2}\sim \frac{2}{n}a_n,\qquad n\to\infty
\end{equation}$$

the solution to which is \\(a\_{n} \sim \frac{1}{(n/2)!}\\), as \\(n\to\infty\\). This generates the coefficients for the power series 

$$\begin{equation}
e^{\xi^2} = \sum_{\substack{n=0 \\ n\,\text{even}}}^\infty \frac{\xi^{n}}{(n/2)!}
\end{equation}$$

What this means for us, is that if we allow the recurrence relation to continue forever, we will get solutions like \\(u(\xi) \sim e^{\xi^2}\\), which leads again to \\(\psi(\xi) = e^{\xi^2}e^{-\xi^2/2} = e^{\xi^2/2}\\), which goes to infinity and is non-normalizable! Our conclusion is that our recurrence relation <i>must terminate</i>. The relation terminates if \\(2n = \lambda - 1\\), for some \\(n\\). This gives us the value for our eigenvalue \\(\lambda\\). Thus, 

$$\begin{equation}
\lambda = 1 + 2n
\end{equation}$$

Plugging back in our previous expression for \\(\lambda = 2E/\hbar\omega\\), we finally get the energy eigenvalues for the system:

$$\begin{equation}
E = \hbar\omega\left(\frac{1}{2} + n\right),\qquad n\geq 0
\end{equation}$$

The \\(n=0\\) case is known as the <i>zero point energy</i> of the harmonic oscillator. Let's work now on the eigenfunctions of the system. The eigenfunctions corresponding to these eigenvalues are known as the Hermite polynomials, \\(H\_n(\xi)\\). If you want more information about the Hermite polynomials, consult a book on mathematical physics or special functions. 

