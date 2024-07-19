---
layout: lesson
title: Relativistic effects 
dept: physics
course: cmp-I
unit: unit4
deptDisplay: Physics
courseDisplay: Condensed Matter Physics I
unitDisplay: Unit 4
---
So far, we have not considered the effect of spin-orbit coupling in a material. We will do this now. In undergraduate quantum mechanics, spin-orbit coupling, for example between an electron in hydrogon and the nucleus, is derived without explicit reference to special relativity. Instead, most authors choose to present a physical cartoon based on viewing the motion of the proton around the electron instead of the other way around. This cartoon is nice, but spin-orbit coupling arises very naturally from the Dirac equation for the electron. We will discuss this now. 

We recall that the Schrödinger equation 

$$\begin{equation}
i\hbar \frac{\partial}{\partial t} \ket{\psi} = \Hhat\ket{\psi}
\end{equation}$$

is Galilean invariant, but not Lorentz invariant, when \\(\Hhat\\) has the standard kinetic energy \\(E = \hat{\p}^2/2m\\). In special relativity, the standard relation \\(E^2 = (mc^2)^2 + (c\p)^2\\) holds instead. If one makes the prescription \\(E \to i\hbar \partial_t\\) and \\(\p \to -i\hbar\nabla\\), then letting the relativistic invariant equation act on a wave function gives us the <i>Klein-Gordon equation:</i>

$$\begin{equation}
-\hbar^2\partial_t^2 \psi = (mc^2)^2\psi - c^2\hbar^2\nabla^2\psi
\end{equation}$$

Then, the following \\(\psi(\x,t) = A\cos(\omega t) \cos(k_xx) \cos(k_yy) \cos(k_zz)\\) is a solution to the equation, whereby \\((\hbar\omega)^2 = (mc^2)^2 + (c\hbar \k)^2\\). This equation, although being relativistically invariant, admits a solution where \\(\psi(\x,t) = 0\\) for all \\(\x\\), if \\(\omega t = \pi(1/2 + n)\\) for any integer \\(n\\). This is a problem because it would mean that \\(\|\psi\|^2 = 0\\) at all points in space for some specific times, meaning the particle entirely disappears. This does not make sense on physical grounds, and it indicates that we should try to massage the equation into one in which there are only first derivatives in time, just like the ordinary Schrödinger equation. In this case, we would not get sines or cosines, but rather complex exponentials, and this ``vanishing of the probability density" issue would be solved. 

To solve this, the Klein-Gordon equation can be factored as 

$$\begin{equation}
E^2 - (mc^2)^2 - \|c\p\|^2 = (E + \alpha_0 mc^2 + c\boldsymbol{\alpha}\cdot\p)(E - \alpha_0 mc^2 - c\boldsymbol{\alpha}\cdot\p) = 0
\end{equation}$$

If we expand out the brackets, then we get that 

$$\begin{align}
0 ={}& E^2 - (mc^2)^2 \alpha_0^2 - \frac{1}{2}c^2\sum_{a,b=1}^3 \{\alpha_a,\alpha_b\}p_ap_b - \sum_{a=1}^3\{\alpha_0,\alpha_a\}p_a 
\end{align}$$

where we have symmetrized over \\(a,b\\) in the \\(\p^2\\) term at the cost of a factor of \\(1/2\\). This tells us that \\(\alpha_0^2 = \1\\), \\(\{\alpha_a,\alpha_b\} = 2\delta_{ab}\\), and \\(\{\alpha_0,\alpha_i\} = 0\\). A solution to this is 

$$\begin{equation}
\alpha_0 = \begin{pmatrix} \sigma^0 & 0 \\ 0 & -\sigma^0 \end{pmatrix}, \quad \alpha_a = \begin{pmatrix} 0 & \sigma^a \\ \sigma^a & 0 \end{pmatrix}
\end{equation}$$

Then, either of the two factors can be set to zero. In the following section, we will discuss the case when we set 

$$\begin{equation}
E - \alpha_0 mc^2 - c\boldsymbol{\alpha}\cdot\p = 0
\end{equation}$$

This is an equation which acts on a 4-component spinor, namely a Dirac spinor. Thus, we should read the equation as 

$$\begin{equation}
E\ket{\psi} = (\alpha_0 mc^2 - c\boldsymbol{\alpha}\cdot\p)\ket{\psi} 
\end{equation}$$

whereby

$$\begin{equation}
\ket{\psi} = \begin{pmatrix} 
\ket{\psi_{1\uparrow}} \\
\ket{\psi_{1\downarrow}} \\
\ket{\psi_{2\uparrow}} \\
\ket{\psi_{2\downarrow}}
\end{pmatrix}
\end{equation}$$

We can then write this as two separate equations, one for each two-component spinor \\(\ket{\psi_1}\\) and \\(\ket{\psi_2}\\). This gives us 

$$\begin{align}
E\ket{\psi_1} ={}& mc^2\ket{\psi_1} + c\boldsymbol{\sigma}\cdot\p\ket{\psi_2} + U(\x)\ket{\psi_1} \\
E\ket{\psi_2} ={}& -mc^2\ket{\psi_2} + c\boldsymbol{\sigma}\cdot\p\ket{\psi_1} + U(\x)\ket{\psi_2}
\end{align}$$

We will come to solving this in the next section.


<div class="faq">
<b>FAQ:</b> 
<ul>
<li> Q: In quantum field theory, we typically learn that the Klein-Gordon equation should be factorized as \((\gamma^0E + c\boldsymbol{\gamma}\cdot\p + mc^2)(\gamma^0E + c\boldsymbol{\gamma}\cdot\p - mc^2) = 0\). What is the relation between this factorization and the one discussed in this section? A: Well, we note that \(\gamma^0 = \alpha_0\). Well, we can rewrite the factorization as 

$$\begin{align}
E^2 - \|c\p\|^2 - (mc^2)^2 ={}& (\gamma^0E + c\boldsymbol{\gamma}\cdot\p + mc^2)(\gamma^0E + c\boldsymbol{\gamma}\cdot\p - mc^2)\\
={}& \gamma^0(E + c\gamma^0\boldsymbol{\gamma}\cdot\p + \gamma^0mc^2)(\gamma^0E + c\boldsymbol{\gamma}\cdot\p\gamma^0 - \gamma^0mc^2)\gamma^0
\end{align}$$

Then, we note that \(\gamma^0\gamma^a = \alpha_a\), and \(\gamma^a\gamma^0 = -\alpha_a\). Thus, we get that (removing the \(\gamma^0\) on the far left and far right of the equation)

$$\begin{align}
E^2 - \|c\p\|^2 - (mc^2)^2 ={}& (E + c\boldsymbol{\alpha}\cdot\p + \alpha^0mc^2)(\gamma^0E - c\boldsymbol{\alpha}\cdot\p - \alpha^0mc^2)
\end{align}$$

We therefore see that the factorization is equivalent to the one we have made in the text. We note that the factorization used above is quite common in condensed matter physics, because we are interested in creating Schrödinger type equations for an electron in a solid. That is, we want \(E\) to be by itself.
</li></ul>

</div>

