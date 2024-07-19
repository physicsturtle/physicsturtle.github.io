---
layout: exercises
title: Partial wave theory  - Exercises
dept: physics
course: qm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics III
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise">  Define the three-dimensional probability current by

$$\begin{equation}
<b>J</b> = \frac{i\hbar}{2m}(\Psi\nabla\Psi^* - \Psi^*\nabla\Psi)
\end{equation}$$

<ol type="a">
<li> Show that \(<b>J</b>\) satisfies the continuity equation

$$\begin{equation}
\nabla\cdot<b>J</b> = -\frac{\partial}{\partial t}|\Psi|^2
\end{equation}$$

which expresses local conservation of probability. It follows that 

$$\begin{equation}
\oint_{\partial \V} <b>J</b>\cdot\d<b>A</b> = -\frac{\d}{\d t}\int_{\V} |\Psi|^2 \d^3\x
\end{equation}$$

where \(\V\) is a (fixed) volume and \(\partial \V\) is its boundary surface. In words: the flow of probability out through the surface is equal to the decrease in probability of finding the particle in the volume. 

</li>
<li> Find \(<b>J</b>\) for hydrogen in the state \(n=2\), \(\ell = 1\), \(m = 1\). 

</li>
<li> If we interpret \(m<b>J</b>\) as the flow of mass, the angular momentum is 

$$\begin{equation}
<b>L</b> = m\int (\r\times<b>J</b>)\d^3\x
\end{equation}$$
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer31')" class="answerButton">Show Answer</button> 
 <div  id='answer31' class="answer" >
<ol type="a">
<li> The divergence of \(<b>J</b>\) is 

$$\begin{equation}
\nabla\cdot<b>J</b> = \frac{i\hbar}{2m}(\Psi\nabla^2\Psi^* - \Psi^*\nabla^2\Psi)
\end{equation}$$

The time derivative of \(|\Psi|^2\) is 

$$\begin{align}
\frac{\partial}{\partial t}|\Psi|^2 =& \left(\frac{\partial}{\partial t}\Psi\right)\Psi^* + \Psi\frac{\partial}{\partial t}\Psi^* \\
=& \frac{1}{i\hbar}\left(-\frac{\hbar^2\nabla^2\Psi}{2m} + V\Psi\right)\Psi^* + \Psi\frac{1}{-i\hbar}\left(-\frac{\hbar^2\nabla^2\Psi^*}{2m} + V\Psi^*\right) \\
=& \frac{i\hbar}{2m} (\nabla^2\Psi)\Psi^* - \frac{i\hbar}{2m}   \Psi(\nabla^2\Psi^*) \\
=& \frac{i\hbar}{2m}((\nabla^2\Psi)\Psi^* - \Psi(\nabla^2\Psi))
\end{align}$$

Clearly, this is the negative of \(\nabla\cdot<b>J</b>\). 

</li>
<li> Let us find the probability current for the state

$$\begin{equation}
\psi_{211}(\x,t) = -\frac{r\sin\theta}{8\sqrt{\pi a^5}}e^{-r/2a}e^{i\varphi}e^{-iE_2t/\hbar}
\end{equation}$$

We need the following formula for the gradient in spherical coordinates:

$$\begin{equation}
\nabla = \ehat_r \frac{\partial}{\partial r} + \ehat_\theta \frac{1}{r} \frac{\partial}{\partial \theta} + \ehat_\varphi \frac{1}{r\sin\theta} \frac{\partial}{\partial \varphi}
\end{equation}$$

Then, we take the derivative:

$$\begin{align}
\nabla\psi_{211} =& -\frac{e^{-iE_2t/\hbar}}{8\sqrt{\pi a^5}}\left[\left(e^{-2r/a} - \frac{r}{2a}e^{-2r/a}\right)\sin\theta e^{-i\varphi} \ehat_r + \frac{\cos\theta r}{r} e^{-r/2a} e^{-i\varphi} \ehat_\theta - \frac{ire^{-r/2a}\sin\theta}{r\sin\theta} e^{-i\varphi} \ehat_\varphi\right] \\
=& -\frac{e^{-iE_2t/\hbar}}{8\sqrt{\pi a^5}}\left[\left(1 - \frac{r}{2a}\right)\sin\theta \ehat_r + \cos\theta \ehat_\theta - i\ehat_\varphi\right] e^{-r/2a}e^{-i\varphi} \\
\end{align}$$

Thus, the quantities 

$$\begin{align}
\psi_{211}\nabla\psi_{211}^* =& -\frac{1}{64\pi a^5}\left[\left(1- \frac{r}{2a}\right)\sin\theta \ehat_r + \cos\theta \ehat_\theta - i\ehat_\varphi\right]\left(-r\sin\theta e^{-r/a}\right) \\
=& \frac{1}{64\pi a^5}\left[\left(1- \frac{r}{2a}\right)\sin\theta \ehat_r + \cos\theta \ehat_\theta - i\ehat_\varphi\right]r\sin\theta e^{-r/a}
\end{align}$$

Computing the difference \(\psi_{211}\nabla\psi^*_{211} - (\nabla\psi_{211})\psi^*_{211}\) removes the real part, and we get 

$$\begin{align}
\psi_{211}\nabla\psi^*_{211} - (\nabla\psi_{211})\psi^*_{211} =& \frac{1}{64\pi a^5}\left[ - 2i \ehat_\varphi\right]r\sin\theta e^{-r/a} \\
=& \frac{-i}{32\pi a^5}r\sin\theta e^{-r/a} \ehat_\varphi 
\end{align}$$

Finally, we find 

$$\begin{equation}
<b>J</b> = \frac{\hbar}{64m\pi a^5}r\sin\theta e^{-r/a} \ehat_\varphi
\end{equation}$$

We interpret this as a current going around the \(z\) axis, which makes since \(L_z = \hbar\) for this state. 

</li>
<li> The angular momentum is then found by computing 

$$\begin{equation}
<b>L</b> = m\int(<b>r</b>\times<b>J</b>)\d^3\x
\end{equation}$$

The position vector is \(<b>r</b> = r\ehat_r\), so computing \(\ehat_r\times\ehat_\varphi = -\ehat_\theta\), so we find (using \(\ehat_\theta = \cos\theta\cos\varphi\ehat_x + \cos\theta\sin\varphi\ehat_y -\sin\theta \ehat_z\))

$$\begin{align}
<b>L</b> =& -m\int \frac{\hbar}{64m\pi a^5}r^2\sin\theta e^{-r/a} \ehat_\theta \d^3\x \\
=& \frac{\hbar m}{64m\pi a^5}\int r^2\sin\theta e^{-r/a} \sin\theta \ehat_z \d^3\x \\
=& \frac{\hbar m}{64m\pi a^5} \int_0^\infty \int_0^\pi \int_0^{2\pi} r^2\sin\theta e^{-r/a} \sin\theta r^2\sin\theta \d\varphi \d\theta \d r \ehat_z\\
=& \frac{\hbar m}{64m\pi a^5} 2\pi \int_0^\infty r^4e^{-r/a} \d r \int_0^\pi \sin^3\theta \d\theta \ehat_z\\
=& \frac{\hbar m}{64m\pi a^5} 2\pi a^5 4! \frac{4}{3} \ehat_z\\
=& \hbar \ehat_z
\end{align}$$

This makes perfect sense! 

</li></ol>
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  We will often have an incoming particle. In quantum mechanics, an incoming particle is written as a plane wave. When the wave scatters off of some potential (big black dot), then we need to consider the different scattered components in terms of spherical waves. It is very inconvenient to describe the incoming wave in terms of a plane wave, but the outgoing wave in terms of a spherical wave. Thus, we need to <i>express the incoming plane wave in terms of spherical waves</i>. 

<figure class="center">
<p><img src="figures/incoming_plane_wave.pdf" alt="Function" class="center" style="width:151.42px;height:113.784px;"> </p><p><img src="figures/outgoing_spherical_wave.pdf" alt="Function" class="center" style="width:142.43px;height:114.382px;"> </p></figure>


Remark: First, what is a <i>spherical wave</i>? Well, we remind ourselves that a <i>plane wave</i> is a solution of the wave equation in Cartesian coordinates. A spherical wave is a solution of the wave equation in spherical coordinates. However, we know that these equations are actually the same, and the only difference is the coordinate system used to represent the solutions. Therefore, there should be a way to convert between the two. That is what we will discuss in this problem. Let us first review a couple things. We recall that:


We need to review the spherical harmonics first. 

<ul>
<li> The spherical harmonics are defined by 

$$\begin{equation}
Y^m_\ell(\theta,\varphi) = Ne^{im\varphi} P^m_\ell(\cos\theta)
\end{equation}$$

where \(N\) is a normalization constant and \(P^m_\ell\) are the associated Legendre polynomials. These polynomials are defined by 

$$\begin{equation}
P^m_\ell(u) = (-1)^m(1-u^2)^{m/2}\frac{\d^m}{\d u^m}P_\ell(u)
\end{equation}$$

where \(P_\ell(u)\) are the ordinary Legendre polynomials. However, if we are looking for azimuthally symmetric solutions (which we are), then there should be no \(\varphi\) dependence. Thus, \(m = 0\). Thus, we do not need to worry about the associated Legendre polynomials, and we will only consider the ordinary ones. Now let us remind ourselves about the ordinary Legendre polynomials.

</li>
<li> The Legendre polynomials are a system of complete and orthogonal polynomials on the interval \(x\in [-1,1]\). They are defined by

$$\begin{equation}
P_\ell(x) = \frac{1}{2^\ell \ell!} \frac{\d^\ell}{\d x^\ell}(x^2-1)^\ell
\end{equation}$$

They satisfy the following: 

$$\begin{equation}
\int_{-1}^1 P_m(x) P_n(x) \d x = \frac{2}{2n+1}\delta_{mn}
\end{equation}$$

Any (sufficiently nice) function \(f(x)\) can be expanded as 

$$\begin{equation}
f(x) = \sum_{\ell=0}^\infty a_\ell P_\ell(x),\qquad a_\ell = \frac{2\ell+1}{2}\int_{-1}^1 f(x) P_\ell(x) \d x
\end{equation}$$

Note: to find the coefficients \(a_\ell\), multiply the first equation by \(P_m(x)\) on both sides and then integrate, using the orthogonality relation.
</li>
<li> So far, we have just reviewed the angular solutions in spherical coordinates. What about the radial solutions? Well, in 3D, the radial solutions are related to something called ``spherical Bessel functions". The spherical Bessel functions are defined by 

$$\begin{equation}
j_\ell(x) = (-1)^\ell x^\ell \left(\frac{1}{x}\frac{\d}{\d x}\right)^\ell \frac{\sin x}{x}
\end{equation}$$

so the first few spherical Bessel functions are given by 

$$\begin{align}
j_0(x) ={}& \frac{\sin x}{x} \\
j_1(x) ={}& \frac{\sin x}{x^2} - \frac{\cos x}{x} \\
j_2(x) ={}& \left(\frac{3}{x^3} - \frac{1}{x}\right)\sin x - \frac{3}{x^2}\cos x
\end{align}$$

If we want to motivate where these come from, let us also recall that the spherical Bessel functions come from the wave equation (which includes the Laplacian) in 3 dimensions. We recall that the wave equation is 

$$\begin{equation}
\frac{\partial^2 \psi}{\partial t^2} = c^2 \nabla^2 \psi
\end{equation}$$

Then, the 

$$\begin{equation}
\nabla^2 \Psi = \left[\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial}{\partial\varphi^2}\right]\Psi
\end{equation}$$

To analyze the radial part of this, write that assume that \(\Psi = \psi(r,t)Y^m_\ell(\theta,\varphi)\), and then we have that 

$$\begin{equation}
Y^m_\ell\frac{\partial^2 \psi}{\partial t^2} = c^2\left[\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) \psi - \frac{1}{r^2}\ell(\ell+1)\psi\right]Y^m_\ell
\end{equation}$$

Then letting \(\psi = R(r)T(t)\), we would have 

$$\begin{equation}
\frac{T"}{T} = \frac{c^2}{r^2R}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) - \frac{\ell(\ell+1)}{r^2} = -\omega^2 = -c^2k^2
\end{equation}$$

Then, this gives us 

$$\begin{equation}
\frac{1}{r^2R}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) - \frac{\ell(\ell+1)}{r^2} = -k^2
\end{equation}$$

Then letting \(\alpha = kr\), this changes to 

$$\begin{equation}
\frac{1}{\alpha^2 R}\frac{\partial}{\partial \alpha }\left(\alpha^2\frac{\partial R}{\partial \alpha}\right) - \frac{\ell(\ell+1)}{\alpha^2} = -1
\end{equation}$$

We can rearrange this to 

$$\begin{equation}
\alpha^2 \frac{\partial^2 R}{\partial\alpha^2} + 2\alpha\frac{\partial R}{\partial \alpha} + (\alpha^2 - \ell(\ell+1))R= 0
\end{equation}$$

This is the spherical Bessel function, with \(R = j_\ell(\alpha) = j_\ell(kr)\). Now that we know where the spherical Bessel functions came from, and we have some motivation for us to express the plane waves in terms of these radially symmetric functions.

</li></ul>

</div> </li>
<li> <div class="exercise">  Prove that 

$$\begin{equation}
e^{ikz} = \sum_{\ell=0}^\infty i^\ell (2\ell+1)j_\ell(kr) P_\ell(\cos\theta)
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer251')" class="answerButton">Show Answer</button> 
 <div  id='answer251' class="answer" >
In order to prove this, we have a function \(e^{ikz} = e^{ikr\cos\theta}\). Defining \(u = \cos\theta\), we want to use the above result to find the coefficients \(a_\ell\) in 

$$\begin{equation}
e^{ikru} = \sum_{\ell=0}^\infty a_\ell(kr)P_\ell(u)
\end{equation}$$
 
To find the coefficients, we compute 

$$\begin{equation}
a_\ell(kr) = \frac{2\ell+1}{2}\int_{-1}^1 e^{ikru}P_\ell(u) \d u
\end{equation}$$

Now, plugging in the form of \(P_\ell(u)\), we get 

$$\begin{align}
a_\ell(kr) ={}& \frac{2\ell+1}{2}\int_{-1}^1 e^{ikru} \frac{1}{2^\ell \ell!}\frac{\d^\ell}{\d u^\ell}(u^2-1)^\ell \d u \\
={}& \frac{2\ell+1}{2^{\ell+1}\ell!}\int_{-1}^1 e^{ikru}\frac{\d^\ell}{\d u^\ell}(u^2-1)^\ell \d u
\end{align}$$

We need to integrate by parts \(\ell\) times. If we do this, then we get 

$$\begin{align}
a_\ell(kr) ={}& \frac{2\ell+1}{2^{\ell+1}\ell!}\int_{-1}^1 (-1)^\ell \frac{\d^\ell}{\d u^\ell}(e^{ikru}) (u^2-1)^\ell \d u \\
={}& \frac{2\ell+1}{2^{\ell+1}\ell!} (-ikr)^\ell \int_{-1}^1 e^{ikru} (u^2-1)^\ell \d u
\end{align}$$

If we define \(\alpha = kr\), then we want to find the relationship between this integral and the spherical Bessel function

$$\begin{align}
\int_{-1}^1 e^{i\alpha u} (u^2-1)^n \d u
\end{align}$$

Well, let's calculate 

$$\begin{align}
\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\int_{-1}^1 e^{i\alpha u} \d u ={}& \frac{1}{\alpha}\int_{-1}^1 e^{i\alpha u} iu \d u \\
={}& \frac{1}{2\alpha}\int_{-1}^1 e^{i\alpha u} i (u^2-1)'\d u \\
={}& \frac{i}{2\alpha}e^{i\alpha u}(u^2-1)\bigg|_{-1}^1 - \frac{i}{2\alpha} \int_{-1}^1 i\alpha e^{i\alpha u}(u^2-1)\d u \\
={}& \frac{1}{2} \int_{-1}^1 e^{i\alpha u}(u^2-1)\d u
\end{align}$$

If we generalize this, then we can find that 

$$\begin{align}
\frac{1}{\alpha}\frac{\partial}{\partial\alpha} \int_{-1}^1 e^{i\alpha u} (u^2-1)^n \d u ={}& \frac{1}{\alpha} \int_{-1}^1 iu e^{i\alpha u} (u^2-1)^n \d u \\
={}& \frac{1}{2\alpha(n+1)} \int_{-1}^1 ie^{i\alpha u} [(u^2-1)^{n+1}]' \d u \\
={}& \frac{i}{2\alpha(n+1)} e^{i\alpha u}(u^2-1)^{n+1}\bigg|_{-1}^1 - \frac{i}{2\alpha(n+1)}\int_{-1}^1 i\alpha e^{i\alpha u}(u^2-1)^{n+1} \d u \\
={}& \frac{1}{2(n+1)}\int_{-1}^1 e^{i\alpha u}(u^2-1)^{n+1} \d u 
\end{align}$$

We see now that we pick up a factor of \(1/2\) and \(1/(n+1)\) when we differentiate (and also divide by \(\alpha\)) \(\int_{-1}^1 e^{i\alpha u} (u^2-1)^n \d u\). Thus, if we want to differentiate (and divide by \(\alpha\))

\(\)\int_{-1}^1 e^{i\alpha u} \d u\(\)

\(\ell\) times, then we get 

$$\begin{equation}
\left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \int_{-1}^1 e^{i\alpha u} \d u = \frac{1}{2^\ell\ell!} \int_{-1}^1 e^{i\alpha u}(u^2-1)^\ell \d u
\end{equation}$$

Thus, we can use 

$$\begin{align}
a_\ell(kr) ={}& \frac{2\ell+1}{2^{\ell+1}\ell!} (-ikr)^\ell \int_{-1}^1 e^{ikru} (u^2-1)^\ell \d u \\
={}& \frac{2\ell+1}{2}(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \int_{-1}^1 e^{i\alpha u} \d u \\
={}& \frac{2\ell+1}{2}(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \frac{1}{i\alpha}e^{i\alpha u}\bigg|_{-1}^1 \\
={}& \frac{2\ell+1}{2}(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \frac{1}{i\alpha}(e^{i\alpha} - e^{-i\alpha}) \\
={}& (2\ell+1)(-i\alpha)^\ell \left(\frac{1}{\alpha}\frac{\partial}{\partial\alpha}\right)^\ell \frac{\sin\alpha}{\alpha}\\
={}& (2\ell+1)i^\ell j_\ell(\alpha)
\end{align}$$

Finally plugging back in \(\alpha = kr\), we get 

$$\begin{align}
a_\ell(kr) ={}& (2\ell+1)i^\ell j_\ell(kr)
\end{align}$$

Thus, we find that 

$$\begin{align}
e^{ikru} ={}& \sum_{\ell=0}^\infty a_\ell(kr)P_\ell(u) \\
={}& \sum_{\ell=0}^\infty (2\ell+1)i^\ell j_\ell(\alpha)P_\ell(u) 
\end{align}$$

and finally substituting back in \(u = \cos\theta\), we get 

$$\begin{align}
e^{ikz} = e^{ikr\cos\theta} ={}& \sum_{\ell=0}^\infty (2\ell+1)i^\ell j_\ell(\alpha)P_\ell(\cos\theta) 
\end{align}$$

</div> 
 </div>

</div> </li></ol>


