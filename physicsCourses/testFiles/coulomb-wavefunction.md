---
layout: page
title: Coulomb Wavefunction
course: test
unit: unit1
permalink: /test/coulomb-wavefunction/
---

Coulomb Wavefunctions are solutions to the hydrogenic system for positive energies. That is, unbound states of the hydrogenic system. Calculating these functions requires some heavy analysis, namely tools from contour integration. The differential equation that this leads to is (in atomic units)

$$-\frac{1}{2}\nabla^2\psi + \frac{Z}{r}\psi = E\psi$$

After separating variables, this leads to 

$$-\frac{1}{2}\frac{d^2}{dr^2}\psi + \frac{Z}{r}\psi + \frac{l(l+1)}{2r^2}\psi = E\psi.$$

The solutions to the Schrödinger equation have already been calculated for this, but for negative energies. It is possible to use these solutions as a template and from them build the solutions for positive energies. It will require us to do a new normalization, but it is better than trying to solve the differential equation from scratch again. 

The main difference between the solutions for positive energy and the solutions for negative energy is that the solutions for positive energy require an imaginary principal quantum number. Before, we had the formula (in atomic units)

$$E = -\frac{Z^2}{2n^2}$$

Now, for positive energies, we think of this as a continuous spectrum of possible states, and define 

$$E = \frac{k^2}{2}$$

which means that $n = -iZ/k$. (One could just have easily picked $n = -iZ/k$, it will not make a difference in the final result).

The solution to the hydrogenic equation is as follows: 

$$\psi_{nlm}(r,\theta,\varphi) = \sqrt{\left(\frac{2Z}{n_1a}\right)^3\frac{(n_1-l_1-1)!}{2n((n_1+l_1)!)^3}}\exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right)Y^{m_1}_{l_1}(\theta,\varphi).$$

We ditch the normalization factor, and focus only on the variable part. In order to adapt this solution, we need to extend the definition of the Laguerre polynomials to the case of complex indices. The Laguerre polynomials are defined as

$$ L_q(z) = e^z\left(\frac{d}{dz}\right)^q\left(e^{-z} z^q\right) $$

The $n$-fold differentiation of a product has various formulas for expressing it in a closed form. Recall the Cauchy integral formula:

\begin{equation}
f(z) = \frac{1}{2\pi i}\oint \frac{f(s)}{s-z} ds
\end{equation}

where the integral is taken counterclockwise over a simple closed curve, $f$ is holomorphic in an open set which fully contains the curve, and $z$ is a point inside the closed curve. Then we can differentiate the formula $n$ times with respect to $z$.

$$ f^{(n)}(z) = \frac{\Gamma(n+1)}{2\pi i}\oint \frac{f(s)}{(s-z)^{n+1}} ds $$

where $\Gamma$ is the gamma function. The gamma function is defined on the entire complex plane except at nonpositive integers, where it has poles. We will be working with it in a formal manner, and whenever a situation arises where it might be evaluated at a pole, we simply continue on symbolically. Thus we can express the $q$th Laguerre polynomial as 

$$L_q(z) = \frac{e^z \Gamma(q+1)}{2\pi i}\oint \frac{e^{-s} s^q}{(s-z)^{q+1}} ds $$

It is important that we keep track of the curve over which we integrate. In the above integral, this contour is still the one enclosing the point $z$.  Then we make the substitution $w = s-z$, so the contour becomes the counterclockwise one enclosing the origin in the $w$ plane.

$$ L_q(z) = \frac{\Gamma(q+1)}{2\pi i}\oint \frac{e^{-w}(z+w)^q}{w^{q+1}} dw $$

The associated Laguerre polynomials are defined in terms of the Laguerre polynomials like so:

$$ L^p_{q-p}(z) = (-1)^p\left(\frac{d}{dz}\right)^p L_q(z) $$

We can plug in the Laguerre polynomials into the formula for the associated Laguerre polynomials. Differentiating the formula $p$ times now gives us

$$ L^p_{q-p}(z) = (-1)^p \frac{(\Gamma(q+1))^2}{2\pi i \Gamma(q-p+1)}\oint \frac{e^{-w}(z+w)^{q-p}}{w^{q+1}} dw $$

For the case of the hydrogen atom, we use $p = 2l+1$ and $q = n+l$, so this gives us 

$$ \begin{eqnarray}
L^{2l+1}_{n-l+1}(z) &=& (-1)^{2l+1}\frac{(\Gamma(n+l+1))^2}{2\pi i\Gamma(n-l)}\oint \frac{e^{-w}(z+w)^{n-l-1}}{w^{n+l+1}}dw\\
&=& -\frac{(\Gamma(n+l+1))^2}{2\pi i\Gamma(n-l)}\oint \frac{e^{-w}(z+w)^{n-l-1}}{w^{n+l+1}}dw
\end{eqnarray}$$


<button onclick="myFunction('answer')" class="answerButton">Show Derivation</button>
<div  id="answer" class="answer">

To further simplify the formula, substitute $w = z(\xi - 1/2)$. Now the contour is around the point $\xi = 1/2$ in the $\xi$ plane. 

$$ \begin{eqnarray}
L^{2l+1}_{n-l+1}(z) &=& -\frac{(\Gamma(n+l+1))^2}{2\pi i\Gamma(n-l)}\oint \frac{e^{-z(\xi-1/2)}z^{n-l-1}(\xi + 1/2)^{n-l-1}}{z^{n+l-1}(\xi - 1/2)^{n+l+1}}z d\xi \\ 
&=& -\frac{(\Gamma(n+l+1))^2 e^{z/2}}{2\pi i z^{2l-1} \Gamma(n-l)}\oint \frac{e^{-z\xi}(\xi + 1/2)^{n-l-1}}{(\xi - 1/2)^{n+l+1}} d\xi \\ 
\end{eqnarray}$$

With the radial part of the solution being (with $z = 2rZ/na$, and $A$ a normalization constant),

$$R(z) = Ae^{-z} z^l L^{2l+1}_{n-l+1}(z)$$

we can then plug in our representation for the Laguerre polynomials:

$$R(z) = \frac{A(\Gamma(n+l+1))^2 e^{-z/2}}{2\pi i z^{l-1}\Gamma(n-l)}\oint \frac{e^{-z\xi}(\xi + 1/2)^{n-l-1}}{(\xi - 1/2)^{n+l+1}} d\xi $$

The last step is to evaluate the contour integral. Our principal quantum number $n$ is now imaginary, which means that we will have to navigate branch cuts. 
</div>

With these Laguerre polynomials, we now need to evaluate the contour integrals. Let's make a power series expansion of the integrand term $(z+w)^{n-l-1}$ in terms of decreasing powers of $w$:

$$(z+w)^{n-l-1} = \sum_{\gamma = 0}^\infty \binom{n-l-1}{\gamma} w^{n-l-1-\gamma}z^\gamma$$

Then plugging this into the integral, it is now possible to evaluate the integral around the contour surrounding the origin. 

$$\begin{eqnarray}
L^{2l+1}_{n-l+1}(z) &=& -\frac{(\Gamma(n+l+1))^2}{2\pi i\Gamma(n-l)}\sum_{\gamma = 0}^\infty \binom{n-l-1}{\gamma}z^{\gamma} \oint \frac{e^{-w} w^{n-l-1-\gamma}}{w^{n+l+1}}dw \\
&=& -\frac{(\Gamma(n+l+1))^2}{2\pi i\Gamma(n-l)}\sum_{\gamma = 0}^\infty \binom{n-l-1}{\gamma}z^{\gamma} \oint \frac{e^{-w}}{w^{2+2l+\gamma}}dw
\end{eqnarray}$$

The residue pole of order $2+2l+\gamma$ at the origin can be evaluated by the following:

$$\begin{eqnarray}
\oint \frac{e^{-w}}{w^{2+2l+\gamma}}dw &=& \oint \sum_{\beta = 0}^\infty \frac{(-1)^\beta w^\beta}{\beta!} \frac{1}{w^{2+2l+\gamma}}dw \\
&=& \sum_{\beta = 0}^\infty \frac{(-1)^\beta}{\beta!} \oint \frac{1}{w^{2+2l+\gamma-\beta}}dw \\
&=& \sum_{\beta = 0}^\infty \frac{(-1)^\beta}{\beta!} 2\pi i \delta_{0,1+2l+\gamma-\beta}\\
&=& \frac{(-1)^{1+2l+\gamma}}{(1+2l+\gamma)!} 2\pi i
\end{eqnarray}$$

where $\delta_{ab}$ is the Kronecker delta. Plugging the result of this integral in, we get 

$$\begin{eqnarray}
L^{2l+1}_{n-l+1}(z) &=& -\frac{(\Gamma(n+l+1))^2}{2\pi i\Gamma(n-l)}\sum_{\gamma = 0}^\infty \binom{n-l-1}{\gamma}z^{\gamma} \frac{(-1)^{1+2l+\gamma}}{(1+2l+\gamma)!}2\pi i \\
&=& -\frac{(\Gamma(n+l+1))^2}{\Gamma(n-l)}\sum_{\gamma = 0}^\infty \frac{(n-l-1)!}{\gamma!(n-l-1-\gamma)!}\frac{z^{\gamma}(-1)^{1+2l+\gamma}}{(1+2l+\gamma)!} \\
&=& (\Gamma(n+l+1))^2\sum_{\gamma = 0}^\infty \frac{z^{\gamma}(-1)^{\gamma}}{\gamma!\Gamma(n-l-\gamma)}\frac{1}{\Gamma(2+2l+\gamma)} \\
\end{eqnarray}$$

Now using the following gamma function identity, 

$$\Gamma(a-b) = \frac{(-1)^{b-1}\Gamma(-a)\Gamma(1+a)}{\Gamma(b+1-a)}$$

we can rewrite the Laguerre polynomial 


$$\begin{eqnarray}
L^{2l+1}_{n-l+1}(z)  &=& (\Gamma(n+l+1))^2\sum_{\gamma = 0}^\infty \frac{z^{\gamma}(-1)^{\gamma}}{\gamma!}\frac{(-1)^{\gamma-1}\Gamma(\gamma+1+l-n)}{\Gamma(l-n)\Gamma(1+n-l)} \frac{\Gamma(2l+2)}{\Gamma(2l+2)\Gamma(2+2l+\gamma)} \\
&=& -\frac{(\Gamma(n+l+1))^2}{\Gamma(2l+2)\Gamma(l-n)\Gamma(1+n-l)}\underbrace{\sum_{\gamma = 0}^\infty \frac{z^{\gamma}}{\gamma!}\frac{\Gamma(\gamma+1+l-n)}{\Gamma(1+l-n)}\frac{\Gamma(2l+2)}{\Gamma(2+2l+\gamma)}}_{ {}_1F_1(1+l-n;2l+2;z)}\\
&=& \frac{\sin(\pi(n-l))(\Gamma(n+l+1))^2}{\Gamma(2l+2)\pi}{}_1F_1(1+l-n;2l+2;z)
\end{eqnarray}$$

where we have defined the following confluent hypergeometric function:

$${}_1F_1(\alpha;\beta; z) = \sum_{h = 0}^\infty \frac{z^h}{h!}\frac{\Gamma(\alpha+h)}{\Gamma(\alpha)}\frac{\Gamma(\beta)}{\Gamma(\beta+h)}.$$

Let us now plug this representation for the Laguerre polynomials into the formula for the wavefunction:

$$\begin{eqnarray}
R(z) &=& Ae^{-z/2} z^{l+1} L^{2l+1}_{n-l+1}(z) \\
&=& \underbrace{A \frac{\sin(\pi(n-l))(\Gamma(n+l+1))}{\pi}}_{B} e^{-z/2} z^{l+1} \frac{\Gamma(n+l+1)}{(2l+1)!}{}_1F_1(1+l-n;2l+2;z)
\end{eqnarray}$$

Now we can finally plug in the actual variable:

$$z = \frac{2Zr}{n}$$

Since we had $n = -iZ/k$, we then rewrite this as $z = 2ikr$. Thus 

$$\begin{eqnarray}
R(r) &=& B e^{-ikr} (2ikr)^{l+1}\frac{\Gamma(n+l+1)}{(2l+1)!}{}_1F_1(1+l-n;2l+2;2ikr)\\
&=& \underbrace{Bi^{l+1}}_{C} e^{-ikr} (kr)^{l+1}\frac{2^l\Gamma(n+l+1)}{(2l+1)!}{}_1F_1(1+l-n;2l+2;2ikr)
\end{eqnarray}$$

The last task is to determine the normalization constant $C$. 



