---
layout: page
title: Hydrogen Photoionization
course: test
unit: unit1
permalink: /test/photoionization/
---

Photoionization is the problem where an electron in a bound state of an atom is released to an unbound state via some bath of radiation in which it sits. 

Eventually, this leads to integrals of the form 

$$\left<\psi_f\right|\textbf{r}\left|\psi_i\right>$$

with \\(\psi_i\\) and \\(\psi_f\\) denoting the initial and final states respectively. The initial states are the bound hydrogen states; we will use hydrogenic ones for generality. 

$$\psi_i = \sqrt{\left(\frac{2Z}{n_1a}\right)^3\frac{(n_1-l_1-1)!}{2n((n_1+l_1)!)^3}}\exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right)Y^{m_1}_{l_1}(\theta,\varphi)$$

The unbound wave-function is the coulomb wave-function. (show a derivation for this in another section)

$$\psi_f = \frac{(-1)^{l_2}2\sqrt{Z}}{\sqrt{1-e^{-2\pi n'}}}\left(\prod_{s=1}^{l_2}\sqrt{s^2+(n')^2}\right)\frac{Y^{m_2}_{l_2}(\theta,\varphi)}{2\pi(2kr)^{l_2+1}}\oint e^{2ikr\xi}\left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi $$

The next step is to calculate the inner product. This will be a very lengthy integral, so let's do each part separately. Since we can write \\(\textbf{r} = r\left(\sin\theta\cos\varphi \hat{\textbf{x}} + \sin\theta\sin\varphi \hat{\textbf{y}} + \cos\theta\hat{\textbf{z}}\right)\\), this factor of \\(r\\) can be separated out. This leaves us with three separate components:

The constant:

$$A = \sqrt{\left(\frac{2Z}{n_1a}\right)^3\frac{(n_1-l_1-1)!}{2n((n_1+l_1)!)^3}}\frac{(-1)^{l_2}2\sqrt{Z}}{2\pi\sqrt{1-e^{-2\pi n'}}}\left(\prod_{s=1}^{l_2}\sqrt{s^2+(n')^2}\right)$$

The radial integral:

$$R = \int_0^\infty \exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right) \frac{r}{(2kr)^{l_1+1}} \oint e^{2ikr\xi}\left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi r^2 dr$$

The angular integrals:

$$\int_0^{2\pi}\int_0^\pi Y^{m_1}_{l_1}(\theta,\varphi)^* \left(\sin\theta\cos\varphi \hat{\textbf{x}} + \sin\theta\sin\varphi \hat{\textbf{y}} + \cos\theta\hat{\textbf{z}}\right) Y^{m_2}_{l_2}(\theta,\varphi) d\theta d\varphi$$

### The Radial Integral

We now evaluate the radial integral. 

$$\begin{eqnarray}
R &=& \int_0^\infty \exp\left(-\frac{Zr}{n_1 a}\right)\left(\frac{2rZ}{n_1a}\right)^{l_1}L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right) \frac{r}{(2kr)^{l_1+1}} \oint e^{2ikr\xi}\left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi r^2 dr \\
&=& \left(\frac{2Z}{n_1a}\right)^{l_1}\frac{1}{(2k)^{l_1+1}}\int_0^\infty \oint\exp\left(-\frac{Zr}{n_1 a} + 2ikr\xi\right)L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right) \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} d\xi r^2 dr \\
&=& \left(\frac{2Z}{n_1a}\right)^{l_1}\frac{1}{(2k)^{l_1+1}} \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} \int_0^\infty \exp\left( 2ikr\xi -\frac{Zr}{n_1 a}\right)L^{2l_1+1}_{n_1-l_1+1}\left(\frac{2Zr}{n_1a}\right)  r^2 dr d\xi \\
\end{eqnarray}
$$

At this point, we have simplified some terms and swapped the order of integration. Now let's change the integration variable:

$$\frac{2Zr}{n_1a} = u$$

Thus the integral becomes

$$\begin{eqnarray}
R &=& \left(\frac{2Z}{n_1a}\right)^{l_1-3}\frac{1}{(2k)^{l_1+1}} \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} \int_0^\infty \exp\left(\underbrace{\left(\frac{ik\xi n_1 a}{Z} - \frac{1}{2}\right)}_{\beta}u\right)L^{2l_1+1}_{n_1-l_1+1}(u)  u^2 du d\xi \\
&=& \left(\frac{2Z}{n_1a}\right)^{l_1-3}\frac{1}{(2k)^{l_1+1}} \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1} \int_0^\infty e^{\beta u}L^{2l_1+1}_{n_1-l_1+1}(u)  u^2 du d\xi \\
\end{eqnarray}
$$

The integral in \\(u\\) can be evaluated to 

$$\int_0^\infty u^q e^{\beta u} L^\alpha_n(u) du = \sum_{k=1}^n\frac{(-1)^k}{k!(n-k)!}\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\frac{(q+k)!}{\beta^{q+k+1}}$$

<button onclick="myFunction('answer')" class="answerButton">Show Derivation</button>
<div  id="answer" class="answer">
The derivation of the above formula comes from using the Leibniz product rule for \(n\) times differentiating a product. The formula for the generalized Laguerre polynomials is 
$$L_n^\alpha(x) = \frac{e^x x^{-\alpha}}{n!}\frac{d^n}{dx^n}\left(e^{-x} x^{n+\alpha}\right)$$
and recall the Leibniz rule for differentiating a product:
$$\frac{d^n}{dx^n}\left(fg\right) = \sum_{k=0}^n f^{(k)}(x) g^{(n-k)}(x)\frac{n!}{k!(n-k)!}$$
This allows us to express the Laguerre polynomials in a sum: 
$$\begin{eqnarray}
L^\alpha_n(x) &=&  \frac{e^x x^{-\alpha}}{n!}\sum_{k=0}^n\frac{d^k}{dx^k}\left(e^{-x}\right)\frac{d^{n-k}}{dx^{n-k}}\left(x^{n+\alpha}\right)\frac{n!}{k!(n-k)!}\\
&=& \frac{e^x x^{-\alpha}}{n!}\sum_{k=0}^n(-1)^k e^{-x}\left(\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\right)x^{\alpha+k}\frac{n!}{k!(n-k)!}\\
&=& \sum_{k=0}^n(-1)^k \left(\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\right)\frac{x^k}{k!(n-k)!}\\
\end{eqnarray}$$

Now if we want to evaluate the given integral, we can substitute the sum representation of the Laguerre polynomials. 

$$\begin{eqnarray}
\int_0^\infty x^q e^{\beta x} L^\alpha_n(x) dx &=& \int_0^\infty  x^q e^{\beta x} \sum_{k=0}^n(-1)^k \left(\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\right)\frac{x^k}{k!(n-k)!}dx \\
&=& \sum_{k=0}^n \frac{(-1)^k}{k!(n-k)!}  \left(\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\right) \int_0^\infty  x^{q+k} e^{\beta x}dx \\
&=& \sum_{k=0}^n \frac{(-1)^k}{k!(n-k)!}  \left(\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\right) \int_0^\infty  x^{q+k} e^{\beta x}dx \\
\end{eqnarray}$$

Now looking at the integral itself, it is very similar the gamma function. For \(\beta\) in the left half plane, we get 

$$\begin{eqnarray}
\int_0^\infty  x^{q+k} e^{\beta x}dx &=& \frac{1}{\beta^{k+q+1}}\int_0^\infty y^{q+k} e^{\beta y} dy\\
&=& \frac{\Gamma(q+k+1)}{\beta^{k+q+1}}
\end{eqnarray}$$

Thus we are finally left with the evaluated integral:

$$\int_0^\infty x^q e^{\beta x} L^\alpha_n(x) dx =  \sum_{k=0}^n \frac{(-1)^k}{k!(n-k)!}  \left(\frac{\Gamma(n+\alpha+1)}{\Gamma(k+\alpha+1)}\right)  \frac{(q+k)!}{\beta^{k+q+1}}.$$

</div>

With the integral in \\(u\\) now evaluated, this leaves only the integral in \\(\xi\\). To avoid confusion with the wave-vector \\(k\\), we change the index of the sum from \\(k\\) to \\(p\\).

$$\begin{eqnarray}
R &=& \left(\frac{2Z}{n_1a}\right)^{l_1-3}\frac{1}{(2k)^{l_1+1}} \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1}  \sum_{p=0}^n \frac{(-1)^p}{p!(n-p)!}  \left(\frac{\Gamma(n+\alpha+1)}{\Gamma(p+\alpha+1)}\right)  \frac{(q+p)!}{\beta^{p+q+1}} d\xi \\
&=&  \left(\frac{2Z}{n_1a}\right)^{l_1-3} \sum_{p=0}^n\frac{(-1)^k(q+p)!}{(2k)^{l_1+1}p!(n-p)!}  \left(\frac{\Gamma(n+\alpha+1)}{\Gamma(p+\alpha+1)}\right)  \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1}  \left(\frac{ik\xi n_1 a}{Z} - \frac{1}{2}\right)^{-p-q-1} d\xi \\
\end{eqnarray}$$

The only pole is where 

$$\frac{ik\xi n_1 a}{Z} - \frac{1}{2} = 0$$

and the other two points of interest, \\(\xi = \pm 1/2\\), are simply branch points. Considering only the contour integral, which has a pole of oder \\(p+q+1\\) at \\(\xi = -iZ/2kna\\), we get 

$$\begin{eqnarray}
I &=& \oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1}  \left(\frac{ik\xi n_1 a}{Z} - \frac{1}{2}\right)^{-p-q-1} d\xi  \\
&=& \left(\frac{Z}{ikn_1a}\right)^{p+q+1}\oint \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1}  \left(\xi + \frac{iZ}{2kn_1a}\right)^{-p-q-1} d\xi \\
&=& \left(\frac{Z}{ikn_1a}\right)^{p+q+1} \left. \frac{d^{p+q+1}}{d\xi^{p+q+1}}\left( \left(\xi + \frac{1}{2}\right)^{-in'-l_2-1}\left(\xi - \frac{1}{2}\right)^{in'-l_2-1}  \right) \right|_{\xi =-iZ/2kna} \\
\end{eqnarray}$$

We evaluate the residue at \\(\xi = -iZ/2kna\\), 

$$\begin{eqnarray}
I &=& \left(\frac{Z}{ikn_1a}\right)^{p+q+1} \left. \sum_{\sigma = 0}^{p+q+1} \frac{\Gamma(-in'-l_2)}{\Gamma(-in'-l_2 - \sigma)}\left(\xi + \frac{1}{2}\right)^{-in'-l_2-1-\sigma}\frac{\Gamma(in'-l_2)}{\Gamma(in'-l_2 + \sigma - (p+q+1))}\left(\xi - \frac{1}{2}\right)^{in'-l_2 - 1 - (p+q+1) + \sigma} \right|_{\xi =-iZ/2kna} \\
&=& \left(\frac{Z}{ikn_1a}\right)^{p+q+1} \sum_{\sigma = 0}^{p+q+1} \frac{\Gamma(-in'-l_2)}{\Gamma(-in'-l_2 - \sigma)}\left(-\frac{iZ}{2kna} + \frac{1}{2}\right)^{-in'-l_2-1-\sigma}\frac{\Gamma(in'-l_2)}{\Gamma(in'-l_2 + \sigma - (p+q+1))}\left(-\frac{iZ}{2kna}- \frac{1}{2}\right)^{in'-l_2 -1 - (p+q+1) + \sigma} \\
\end{eqnarray}$$


