---
layout: lesson
title: Infinite square well 
dept: physics
course: qm-I
unit: unit3
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 3
---
Consider a particle confined to a box. The situation is depicted pictorially below. This scenario is highly idealized, and is not easily realizable in experiment. However,  it plays an important pedagogical role because it will allow us to develop some physical intuition without getting too bogged down with mathematical details. In the 1-dimensional Schrödinger equation, we use the following potential, in Eq.\eqref{eq:infinite_square_well}

<figure class="center">
<p><img src="figures/infinite_square_well.pdf" alt="Function" class="center" style="width:101.684px;height:131.85px;"> </p><figcaption class="center">Classical article moving in an infinite square well. In quantum mechanics, the position of the particle is no longer well-defined, but instead we have a <i>wave</i> which describes the position of the particle. We will come to a schematic of that after solving the corresponding quantum mechanical problem.</figcaption>
</figure>


$$\begin{equation}
V(x) = \begin{cases}
0 & 0 < x < a \\
\infty & \text{otherwise}
\end{cases}. \label{eq:infinite_square_well}
\end{equation}$$

This system should be thought of, classically, as a box of length \\(a\\) whose walls are infinitely tall, so a ball which you throw at the wall could never get out. Thus the classical probability of the particle being outside the box is zero. What this means in quantum mechanics is that the wave function, whose squared magnitude represents the probability (density) of a particle being at that point in space, is zero outside the box. This imposes the following boundary conditions on the wave function: \\(\psi(0) = \psi(a) = 0\\), because the wave function must be continuous.

Therefore, we can write down the Schrödinger equation inside the well (\\(0 < x < a\\)) and the appropriate boundary conditions to be:

$$\begin{equation}
\begin{cases}
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} = E\psi & 0 < x < a \\
\psi(0) = 0 & \psi(a) = 0
\end{cases}.
\end{equation}$$

To solve this boundary value problem, we rearrange it to a more familiar form:

$$\begin{equation}
\psi" + \frac{2mE}{\hbar^2}\psi = 0.
\end{equation}$$

In the case that \\(E > 0\\), we recognize this differential equation as that of a classical simple harmonic oscillator! If you want to consider the case where \\(E\leq 0\\), this is left to an example. The equation has the well-known solutions of sines and cosines:

$$\begin{equation}
\psi(x) = A\sin(kx) + B\cos(kx)
\end{equation}$$

where \\(k = \sqrt{2mE/\hbar^2}\\). The constants \\(A\\) and \\(B\\) are determined by the initial conditions for the classical harmonic oscillator case, but here they are determined by the boundary conditions and the normalization condition (normalization of wave functions must be 1). Let us first apply the boundary condition at \\(x=0\\). Doing this, we find \\(\psi(0) = A\sin(0) + B\cos(0) = B\\). This tells us that \\(B = 0\\). Thus our solution simplifies to \\(\psi(x) = A\sin(kx)\\).

Applying the second boundary condition, we have \\(\psi(a) = A\sin(ka) = 0\\). This leaves us with two choices. Either \\(A = 0\\), or \\(\sin(ka) = 0\\). Clearly, if we set \\(A = 0\\), then the entire wave function \\(\psi(x) \equiv 0\\). This is not a normalizable wave function and is unphysical. Instead, we let \\(A\neq 0\\), and set \\(\sin(ka) = 0\\), or in other words, \\(ak = n\pi\\). This gives a list of possible \\(k\\) values, enumerated by positive integers \\(n\\), namely \\(k_n = n\pi/a\\). This in turn yields the allowed energy eigenvalues 

$$\begin{align}
E_n ={}& \hbar^2k_n^2/2m \\
={}& \frac{n^2\pi^2\hbar^2}{2ma^2}.
\end{align}$$

This means that there are an infinite amount of solutions to the differential equation, indexed by integers \\(n\\):

$$\begin{equation}
\psi_n(x) = A_n\sin\left(\frac{n\pi}{a}\right)
\end{equation}$$

The last step is to determine the constants \\(A_n\\). This is done by imposing the normalization condition

$$\begin{equation}
\int_0^a |\psi_n(x)|^2 \d x = 1.
\end{equation}$$

The integral is simply evaluated:

$$\begin{align}
1 ={}& \int_0^a |A_n|^2 \sin^2\left(\frac{n\pi x}{a}\right) \d x \\
={}& \frac{a}{2}|A_n|^2
\end{align}$$

which gives us \\(A_n = \sqrt{2/a}\\). Our final result is therefore a set of eigenfunction and eigenvalue pairs:

$$\begin{equation}
\psi_n(x) = \sqrt{\frac{2}{a}}\sin\left(\frac{n\pi}{a}\right),\quad E_n = \frac{n^2\pi^2\hbar^2}{2ma^2}.
\end{equation}$$

We note that the wave function is \\(\psi_n(x) \equiv 0\\) if the particle is outside of the well (\\(x < 0\\) or \\(x > a\\)).

<div class="example">
<b>Example:</b>
Consider the case of negative energy for the Schrödinger equation above. Determine whether or not solutions for \(E<0\) exist.

<b>Solution:</b>

When \(E<0\), we rewrite the Schrödinger equation as 

$$\begin{equation}
\psi" - \left(\frac{-2mE}{\hbar^2}\right)\psi = 0.
\end{equation}$$

and then set \(\kappa = \sqrt{-2mE}/\hbar\), and since \(E<0\), the square root is of a positive number. This allows us wrote the Schrödinger equation as \(\psi" - \kappa^2\psi = 0\). The general solution to this equation can be either written in terms of \(e^{\kappa x}\) and \(e^{-\kappa x}\), or in terms of \(\sinh(\kappa x) = \frac{e^{\kappa x} - e^{-\kappa x}}{2}\) and \(\cosh(\kappa x) = \frac{e^{\kappa x} + e^{-\kappa x}}{2}\). We pick the hyperbolic sine and cosine for convenience. Thus the general solution is

$$\begin{equation}
\psi(x) = A\sinh(\kappa x) +B\cosh(\kappa x).
\end{equation}$$

Now, we impose the condition \(\psi(0) = 0\). Plugging in \(x=0\) gives us \(\psi(0) = B\), so \(B=0\). Thus \(\psi(x) = A\sinh(\kappa x)\). Now, we impose the condition \(\psi(a) = 0\). This gives us that \(A\sinh(\kappa a) = 0\). However, since \(\sinh(z) \) is zero only when \(z=0\), we see that we require \(A=0\). (there is technically another case to consider, where \(E=0\), but perhaps you can try this on your own). Since \(A=0\), we find that \(\psi(x) = 0\). Since wave functions cannot be identically zero, we see that there are <i>no solutions</i> to the equation if we assume that \(E<0\). We therefore consider the other case.


</div>

There are a few general features of wave functions that are exemplified here (as they must be). The following are generally true about solutions to the Schrödinger equation:

<ol>
<li> Energy eigenstates (eigenfunctions) corresponding to different eigenvalues are orthogonal to one another
</li>
<li> The number of nodes (zeros) of the wave function increases by 1 as \(n\) increases by 1. For example, there are no zeros of \(\psi_1(x)\), there is one zero (at the centre) of \(\psi_2(x)\), and so on.
</li>
<li> The energy eigenstates form a complete set, meaning that any wave function can be expanded in a linear combination of the energy eigenstates
</li>
<li> The wave functions are either even or odd with respect to \(x=a/2\), which is a symptom of the fact that our potential is even with respect to \(a/2\). 
</li></ol>

We want to show that the eigenfunctions are orthogonal. We have already shown that they are normalized (we didn't show this, but rather we imposed it and chose the \\(A_n\\) coefficients accordingly). When we say orthogonal, this means that we want to show that the inner product (generalization of dot product) is zero between any two wave functions with different \\(n\\). Thus, we want to show that, if \\(n\neq m\\), the following inner product vanishes:

$$\begin{equation}
\int \psi^*_m(x) \psi_n(x) \d x = 0.
\end{equation}$$

To do this, we simply integrate.

$$\begin{align}
\int \psi^*_m(x) \psi_n(x) \d x ={}& \int_0^a \sqrt{\frac{2}{a}}\sin\left(\frac{m\pi x}{a}\right) \sqrt{\frac{2}{a}}\sin\left(\frac{n\pi x}{a}\right) \d x\\
={}& \frac{2}{a}\int_0^a \sin\left(\frac{m\pi x}{a}\right)\sin\left(\frac{n\pi x}{a}\right) \d x \\
={}& \frac{2}{a}\int_0^a\frac{1}{2}\left[\cos\left(\frac{(m-n)\pi x}{a}\right) - \cos\left(\frac{(m+n)\pi x}{a}\right)\right] \d x \\
={}& \frac{1}{a}\left[\frac{a}{(m-n)\pi}\sin\left(\frac{(m-n)\pi x}{a}\right)\bigg|_0^a - \frac{a}{(m+n)\pi}\sin\left(\frac{(m+n)\pi x}{a}\right)\bigg|_0^a \right] \\
={}& \left[\frac{1}{(m-n)\pi}\sin\left(\frac{(m-n)\pi a}{a}\right) - \frac{1}{(m+n)\pi}\sin\left(\frac{(m+n)\pi a}{a}\right) \right] \\
={}& \frac{1}{(m-n)\pi}\sin\left((m-n)\pi\right) - \frac{1}{(m+n)\pi}\sin\left((m+n)\pi\right) \\
={}& 0
\end{align}$$

because know that \\(\sin(\text{integer}\times\pi) = 0\\) for any integer. This calculation, combined with the normalization we worked out in part (a), tells us that

$$\begin{equation}
\int \psi^*_m(x) \psi_n(x) \d x = \delta_{mn}.
\end{equation}$$

<div class="example">
<b>Example:</b>
Suppose a particle in this infinite square well has wave function
$$\begin{equation}
\psi(x) = \begin{cases}
Ax & 0 < x < a/2 \\
A(a-x) & a/2 < x < a \\
0 & \text{else}
\end{cases}.
\end{equation}$$
<ol type="a">
<li> Normalize the wave function by calculating \(A\).
</li>
<li> If you measure the energy of the particle, what is the probability that you will find it in its \(n\)th energy eigenstate?
</li>
<li> Given the fact that 

$$\begin{equation}
\sum_{n=1}^\infty \frac{1}{(2n-1)^4} = \frac{\pi^4}{96},
\end{equation}$$
show that the sum of probabilities for finding the particle in any of the energy eigenstates indeed adds up to 1.
</li></ol>

<b>Solution:</b>

<ol type="a">
<li> We calculate the integral of the wave function squared to find \(A\):
$$\begin{align}
\int |\psi(x)|^2 \d x ={}& \int_0^{a/2} A^2x^2\d x + \int_{a/2}^a A^2(a-x)^2 \d x \\
={}& A^2\left[\frac{x^3}{3}\bigg|_0^{a/2} + \frac{(x-a)^3}{3}\bigg|_{a/2}^a \right] \\
={}& \frac{A^3}{3}\left[\frac{a^3}{8} - \left(\frac{-a}{2}\right)^3\right] \\
={}& \frac{A^2a^3}{12}
\end{align}$$

Imposing the normalization condition that \(\int |\psi(x)|^2 \d x = 1\), we find that 

$$\begin{equation} 
A = \left(\frac{12}{a^3}\right)^{1/2}.
\end{equation}$$

The normalized wave function is then 
$$\begin{equation}
\psi(x) = \left(\frac{12}{a^3}\right)^{1/2}\begin{cases} 
x & 0 < x < a/2 \\
(a-x) & a/2 < x < a \\
0 & \text{else}.
\end{cases} 
\end{equation}$$

</li>
<li> In order to find the probability of measuring a particular energy, we need to expand our wave function \(\psi\) in terms of a linear combination of energy eigenstates. This will allow us to find out ``how much" of each energy eigenstate is contained within the wave function \(\psi\). That is, we want to write 

$$\begin{equation}
\psi(x) = \sum_{n=1}^\infty c_n\psi_n(x).
\end{equation}$$

where the \(\psi_n\) are the energy eigenstates we calculated in part (a). The problem now becomes one of solving for the coefficients \(c_n\). You may recognize this as a Fourier series problem! To calculate a formula for \(c_n\), we first multiply both sides of the equation by \(\psi^*_m(x)\). This gives us 

$$\begin{equation}
\psi_m^*(x)\psi(x) = \sum_{n=1}^\infty c_n\psi^*_m(x)\psi_n(x).
\end{equation}$$

Now, we integrate both sides over the interval \(0<x<a\). 

$$\begin{align}
\int_0^a \psi_m^*(x)\psi(x)\d x ={}& \int_0^a\sum_{n=1}^\infty c_n\psi^*_m(x)\psi_n(x) \d x \\
={}& \sum_{n=1}^\infty c_n\int_0^a \psi^*_m(x)\psi_n(x) \d x 
\end{align}$$

What we showed in part (b) was that 

$$\begin{equation}
\int_0^a \psi^*_m(x)\psi_n(x) \d x = \delta_{mn},
\end{equation}$$

so substituting this in to the above expression, we find that 

$$\begin{equation}
\int_0^a \psi^*_m(x) \psi(x) \d x = \sum_{n=1}^\infty c_n \delta_{mn}.
\end{equation}$$

The delta function simplifies the sum to just 

$$\begin{equation}
c_m = \int_0^a \psi^*_m(x) \psi(x) \d x .
\end{equation}$$

Now we plug in the expressions 

$$\begin{equation}
\psi^*_m(x) = \sqrt{\frac{2}{a}}\sin\left(\frac{n\pi x}{a}\right),\qquad \psi(x) = \sqrt{\frac{12}{a^3}}\begin{cases} 
x & 0 < x < a/2 \\
(a-x) & a/2 < x < a \\
0 & \text{else}.
\end{cases} 
\end{equation}$$

This means that we split up the integral: (note that the \(m\) here is an index, and has nothing to do with the mass of the particle)

$$\begin{align}
c_m ={}& \int_0^a \psi^*_m(x) \psi(x) \d x \\
={}& \int_0^{a/2} \sqrt{\frac{2}{a}}\sin\left(\frac{m\pi x}{a}\right) \sqrt{\frac{12}{a^3}} x \d x + \int_{a/2}^a \sqrt{\frac{2}{a}}\sin\left(\frac{m\pi x}{a}\right) \sqrt{\frac{12}{a^3}} (a-x) \d x \\
={}& \frac{2\sqrt{6}}{a^2}\left[\int_0^{a/2} x\sin\left(\frac{m\pi x}{a}\right) \d x + \int_{a/2}^a (a-x)\sin\left(\frac{m\pi x}{a}\right) \d x\right] 
\end{align}$$

Now we examine the two integrals separately. First, 

$$\begin{align}
\int_0^{a/2} x\sin\left(\frac{m\pi x}{a}\right) \d x ={}& -\frac{xa}{m\pi}\cos\left(\frac{m\pi x}{a}\right) \bigg|_0^{a/2} + \frac{a}{m\pi}\int_0^{a/2} \cos\left(\frac{m\pi x}{a}\right) \d x \\
={}& -\frac{a^2}{2m\pi}\cos\left(\frac{m\pi}{2}\right) + \frac{a^2}{m^2\pi^2}\sin\left(\frac{m\pi x}{a}\right)\bigg|_0^{a/2} \\
={}& -\frac{a^2}{2m\pi}\cos\left(\frac{m\pi}{2}\right) + \frac{a^2}{m^2\pi^2}\sin\left(\frac{m\pi}{2}\right) 
\end{align}$$

Next, we do the other integral. 

$$\begin{align}
 \int_{a/2}^a (a-x)\sin\left(\frac{m\pi x}{a}\right) \d x ={}& -\frac{a(a-x)}{m\pi}\cos\left(\frac{m\pi x}{a}\right)\bigg|_{a/2}^a - \frac{a}{m\pi}\int_{a/2}^a \cos\left(\frac{m\pi x}{a}\right) \d x \\
={}& \frac{a(a-a/2)}{m\pi}\cos\left(\frac{m\pi }{2}\right) - \frac{a^2}{m^2\pi^2} \sin\left(\frac{m\pi x}{a}\right)\bigg|_{a/2}^a  \\
={}& \frac{a^2}{2m\pi}\cos\left(\frac{m\pi }{2}\right) + \frac{a^2}{m^2\pi^2} \sin\left(\frac{m\pi }{2}\right) 
\end{align}$$

Now substituting both of these expressions back into the expression for \(c_m\), we find that 

$$\begin{align}
c_m ={}& \frac{2\sqrt{6}}{a^2}\left[\int_0^{a/2}x\sin\left(\frac{m\pi x}{a}\right) \d x + \int_{a/2}^a(a-x)\sin\left(\frac{m\pi x}{a}\right) \d x \right] \\
={}& \frac{2\sqrt{6}}{a^2}\left[ -\frac{a^2}{2m\pi}\cos\left(\frac{m\pi}{2}\right) + \frac{a^2}{m^2\pi^2}\sin\left(\frac{m\pi}{2}\right) + \frac{a^2}{2m\pi}\cos\left(\frac{m\pi }{2}\right) + \frac{a^2}{m^2\pi^2} \sin\left(\frac{m\pi }{2}\right) \right] \\
={}& \frac{2\sqrt{6}}{a^2}\frac{2a^2}{m^2\pi^2}\sin\left(\frac{m\pi}{2}\right) \\
={}& \frac{4\sqrt{6}}{m^2\pi^2}\sin\left(\frac{m\pi}{2}\right) 
\end{align}$$

What this tells us that (relabelling the index \(m\) back to \(n\))

$$\begin{equation}
c_n = \frac{4\sqrt{6}}{n^2\pi^2}\sin\left(\frac{n\pi}{2}\right).
\end{equation}$$

$$\begin{equation}
c_n = \begin{cases}
\frac{4\sqrt{6}}{n^2\pi^2}(-1)^{(n-1)/2} & n\,\text{odd} \\
0 & n\,\text{even}
\end{cases}
\end{equation}$$

Thus, the probability that we measure \(\psi\) in the state \(\psi_n\) is given by 

$$\begin{equation}
\text{prob}(n) = |c_n|^2 =  \begin{cases}
\frac{96}{n^4\pi^4} & n\,\text{odd} \\
0 & n\,\text{even}
\end{cases}.
\end{equation}$$

</li>
<li> We sum the probabilities that the wave function will be measured in the \(n\)th eigenstate:

$$\begin{equation}
\sum_{n=1}^\infty |c_n|^2 = \sum_{n=1}^\infty |c_{2n-1}|^2 
\end{equation}$$

where we can do that rewriting because we want to skip all the even \(n\) since \(c_n=0\) anyways for \(n\) even. Thus, we want to sum

$$\begin{equation}
\sum_{n=1}^\infty \frac{96}{(2n-1)^4\pi^4} = \frac{96}{\pi^4}\sum_{n=1}^\infty \frac{1}{(2n-1)^4} = \frac{96}{\pi^4}\frac{\pi^4}{96} = 1,
\end{equation}$$
so the result is 1, as desired.

</li></ol>


</div>

