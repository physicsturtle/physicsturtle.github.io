---
layout: page
title: Quantising the Electromagnetic Field
course: test
unit: unit1
permalink: /test/em-field-quantisation/
---

In the Coulomb gauge, the gauge of preference in quantum mechanics, the vector potential satisfies the following equation

$$\ddot{\textbf{A}} = \nabla^2\textbf{A}.$$

We thus look for a solution to the above equation that also satisfies the following two additional properties:

- $\nabla\cdot \textbf{A} = 0$
- $\textbf{A}$ is real

#### Fourier Transform
First, we write $\textbf{A}$ in terms of its Fourier components:

$$\textbf{A} = \frac{1}{(2\pi)^3} \int e^{i\textbf{k}\cdot \textbf{x}} \tilde{\textbf{A}} d^3 k$$

Substituting this Fourier representation of $\textbf{A}$ into the wave equation, we get

$$\begin{eqnarray*}
\frac{\partial^2}{\partial t^2}\frac{1}{(2\pi)^3} \int e^{i\textbf{k}\cdot \textbf{x}} \tilde{\textbf{A}} d^3 k &=& \nabla^2 \frac{1}{(2\pi)^3} \int  e^{i\textbf{k}\cdot \textbf{x}} \tilde{\textbf{A}} d^3 k \\
\frac{1}{(2\pi)^3} \int e^{i\textbf{k}\cdot \textbf{x}} \ddot{\tilde{\textbf{A}}} d^3 k &=& - \frac{1}{(2\pi)^3} \int |\textbf{k}|^2 e^{i\textbf{k}\cdot \textbf{x}} \tilde{\textbf{A}} d^3 k \\
\end{eqnarray*}$$

This equation implies the the following relationship for $\tilde{\textbf{A}}$:

$$\ddot{\tilde{\textbf{A}}} = -|\textbf{k}|^2\tilde{\textbf{A}} $$

Defining $\omega_\textbf{k} = \sqrt{\|\textbf{k}\|^2}$, we can write the solution 

$$\tilde{A}_i = \frac{1}{\sqrt{2\omega_\textbf{k}}}\left(e^{-i\omega_\textbf{k}t}\alpha_i(\textbf{k}) + e^{i\omega_\textbf{k}t}\beta_i(-\textbf{k})\right),\qquad i = 1,2,3,$$

where $\alpha_i$ and $\beta_i$ are arbitrary functions of $\textbf{k}$, and we have added the factor $1/\sqrt{2\omega_\textbf{k}}$ and the negative in the argument of $\beta_i$ both for notational convenience. Next, we take the inverse Fourier transform to get 

$$A_i = \int  \frac{e^{i\textbf{k}\cdot\textbf{x}}}{\sqrt{2\omega_\textbf{k}}}\left(e^{-i\omega_\textbf{k}t}\alpha_i(\textbf{k}) + e^{i\omega_\textbf{k}t}\beta_i(-\textbf{k})\right) \frac{d^3k}{(2\pi)^3}$$

We split this up into two integrals

$$A_i = \int  \frac{e^{i\textbf{k}\cdot\textbf{x}}}{\sqrt{2\omega_\textbf{k}}}e^{-i\omega_\textbf{k}t}\alpha_i(\textbf{k}) \frac{d^3k}{(2\pi)^3} + \int \frac{e^{i\textbf{k}\cdot\textbf{x}}}{\sqrt{2\omega_\textbf{k}}} e^{i\omega_\textbf{k}t}\beta_i(-\textbf{k}) \frac{d^3k}{(2\pi)^3}$$

In the second integral, we make the change of variables $\textbf{k}\mapsto \textbf{k}'$ and get 

$$A_i = \int  \frac{e^{i\textbf{k}\cdot\textbf{x}}}{\sqrt{2\omega_\textbf{k}}}e^{-i\omega_\textbf{k}t}\alpha_i(\textbf{k}) \frac{d^3k}{(2\pi)^3} + \int \frac{e^{-i\textbf{k}'\cdot\textbf{x}}}{\sqrt{2\omega_{\textbf{k}'}}} e^{i\omega_{\textbf{k}'}t}\beta_i(\textbf{k}') \frac{d^3k'}{(2\pi)^3}$$

Note that the sign of the differential brings an overall minus sign, but each of the three integrals' bounds also got flipped from $-\infty \to \infty$ to $\infty \to -\infty$. If we change all these back to $-\infty\to\infty$, then this brings three more overall minus signs, which cancel with the one produced by the differential. Since $\textbf{k}'$ was a dummy variable, we just rename it to be $\textbf{k}$. Now, we put the two integrals back together 

$$A_i = \int  \frac{e^{i\textbf{k}\cdot\textbf{x}-i\omega_\textbf{k}t}\alpha_i(\textbf{k}) + e^{-i\textbf{k}\cdot\textbf{x}+i\omega_\textbf{k}t}\beta_i(\textbf{k}) }{\sqrt{2\omega_\textbf{k}}} \frac{d^3k}{(2\pi)^3}$$

We now impose that $A_i$ is real. Setting the integrand to be real, we find that $\beta_i(\textbf{k}) = \alpha^*_i(\textbf{k})$, so 

$$A_i = \int  \frac{e^{i\textbf{k}\cdot\textbf{x}-i\omega_\textbf{k}t}\alpha_i(\textbf{k}) + e^{-i\textbf{k}\cdot\textbf{x}+i\omega_\textbf{k}t}\alpha^*_i(\textbf{k}) }{\sqrt{2\omega_\textbf{k}}} \frac{d^3k}{(2\pi)^3}.$$

Lastly, we need to impose the condition 

$$\nabla\cdot\textbf{A} = \frac{\partial A_1}{\partial x^1} + \frac{\partial A_2}{\partial x^2} + \frac{\partial A_3}{\partial x^3} =0.$$ 

Since 

$$\frac{\partial A_j}{\partial x^j} = \int\frac{ ik_je^{i\textbf{k}\cdot\textbf{x} - i\omega_\textbf{k}t} \alpha_j(\textbf{k}) - ik_j e^{-i\textbf{k}\cdot\textbf{x} + i\omega_\textbf{k}t}\alpha^*_j(\textbf{k})}{\sqrt{2\omega_\textbf{k}}} \frac{d^3k}{(2\pi)^3},$$

we conclude that 

$$\sum_{j=1}^3 k_j \alpha_j(\textbf{k}) = \textbf{k}\cdot\boldsymbol{\alpha}(\textbf{k}) = 0$$

Thus, $\textbf{k}$ is perpendicular to $\boldsymbol{\alpha}$ at every point in space. This means that $\boldsymbol{\alpha}$ always lies in a plane perpendicular to $\textbf{k}$. We can thus define a basis $\\{\hat{\textbf{e}}_1(\textbf{k}), \hat{\textbf{e}}_2(\textbf{k})\\}$, in which every $\boldsymbol{\alpha}$ can be described. Note that this basis is a function of $\textbf{k}$! We thus write 

$$\boldsymbol{\alpha}(\textbf{k}) = \sum_{n=1}^2 a_n(\textbf{k}) \hat{\textbf{e}}_n(\textbf{k}).$$

Componentwise (components with respect to Cartesian basis), this equation becomes 

$$\alpha_i(\textbf{k}) = \sum_{n=1}^2 a_n(\textbf{k}) e_{in}(\textbf{k}).$$

Finally substituting this into our expression for the vector potential, we get 

$$A_i = \int  \left(e^{i\textbf{k}\cdot\textbf{x}-i\omega_\textbf{k}t} \sum_{n=1}^2 a_n(\textbf{k}) e_{in}(\textbf{k})+ e^{-i\textbf{k}\cdot\textbf{x}+i\omega_\textbf{k}t}\sum_{n=1}^2 a_n^*(\textbf{k}) e_{in}(\textbf{k})\right)\frac{1}{\sqrt{2\omega_\textbf{k}}} \frac{d^3k}{(2\pi)^3}.$$

From now on, we leave the sum over $n$ implicit and write 

$$A_i = \int  \left(e^{i\textbf{k}\cdot\textbf{x}-i\omega_\textbf{k}t} a_n(\textbf{k}) e_{in}(\textbf{k})+ e^{-i\textbf{k}\cdot\textbf{x}+i\omega_\textbf{k}t} a_n^*(\textbf{k}) e_{in}(\textbf{k})\right)\frac{1}{\sqrt{2\omega_\textbf{k}}} \frac{d^3k}{(2\pi)^3}.$$

We observe at this point that $A_i$ is made up of two independent harmonic oscillators: one in the $\hat{\textbf{e}}_1$ direction and one in the $\hat{\textbf{e}}_2$ direction. To quantize, we replace the coefficients $a$ and $a^*$ with $\hat{a}$ and $\hat{a}^\dagger$ respectively: 

<div class="result">
<b> Vector Potential Operators </b>
$$\hat{A}_i(\textbf{x},t) = \int  \left(e^{i\textbf{k}\cdot\textbf{x}-i\omega_\textbf{k}t} e_{in}(\textbf{k}) \hat{a}_n(\textbf{k}) + e^{-i\textbf{k}\cdot\textbf{x}+i\omega_\textbf{k}t} e_{in}(\textbf{k}) \hat{a}^\dagger_n(\textbf{k}) \right)\frac{1}{\sqrt{2\omega_\textbf{k}}} \frac{d^3k}{(2\pi)^3}.$$
</div>






