---
layout: page
title: Quantum States
course: test
unit: unit1
permalink: /test/states/
---

There is no definition of state in quantum mechanics, but rather just pure state and mixed state. A pure state is the most precise piece of information that one can learn about a quantym system. 

<div class="definition">
<b>Definition:</b> Consider a quantum system with Hilbert space $\H$. Then, a pure state of this system is a linear operator
$$\rho_\psi = \frac{\ket{\psi}}{\bra{\psi}\ket{\psi}}\bra{\psi}$$
for any $\psi\in\H$. 
</div>

Note that in this definition $\rho_\psi = \rho_{\lambda\psi}$ for any $\lambda\in\C\setminus\\{0\\}$. This means that, when people refer to elements of $\H$ as the "pure states of the system", this is not a correct statement! One might even try to be more precise and say "the pure states of the system are the normalized elements of $\H$". This is also untrue, because one can multiply any $\psi$ by a complex phase $e^{i\alpha}$ and obtain another normalized state. 

This allows us to define the probability of finding the quantum system in some state $\rho_\varphi$. 

<div class="definition">
<b>Definition:</b> Let $E\subset\R$. Then, the probability of measuring the energy of the system to be an element of $E$ is given by 
$$\Tr(P_H(E)\rho_\varphi).$$
</div> <br>

Recall that $P_H$ is the projection operator. 

<div class="example">
<p><b>Example:</b> Calculate the probability that the energy of the harmonic oscillator is measured to be $E_k = \hbar\omega(k+1/2)$. </p>
<b>Solution:</b> Here we set the set $E = \{E_k\}$. Then, we wish to calculate the trace defined above. To calculate the trace, we need to pick a basis. Let $e_n$ be an orthonormal basis of the Hilbert space $\H$. 

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \sum_{n}\left< e_n, P_H(\{E_k\})\rho_\varphi(e_n)\right>.$$

Since the trace is independent of basis, the best choice of basis is the energy eigenstate basis. Thus, pick $e_n = \psi_n$. The sum then becomes 

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \sum_{n}\left< \psi_n, P_H(\{E_k\})\rho_\varphi(\psi_n)\right>.$$

Substituting in the definition of the state $\rho_\varphi$, note that $\psi_n$ is the argument of this operator to get

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \sum_{n}\left< \psi_n, P_H(\{E_k\})\frac{\varphi\left<\varphi,\psi_n\right>}{\left<\varphi,\varphi\right>}\right>.$$

The quotient of inner products is simply a scalar, so we pull it out and take $\varphi$ alone as the argument of the projection operator. 

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \sum_{n}\frac{\left<\varphi,\psi_n\right>}{\left<\varphi,\varphi\right>}\left< \psi_n, P_H(\{E_k\})\varphi\right>.$$

Applying the definition of the projection operator, we get 

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \sum_{n}\frac{\left<\varphi,\psi_n\right>}{\left<\varphi,\varphi\right>}\left< \psi_n, \sum_{\stackrel{m}{E_m\in\{E_k\}}} \psi_m\left<\psi_m,\varphi\right>\right>.$$

The sum over $m$ consists only of a single term, so we replace $m$ by $k$,

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \sum_{n}\frac{\left<\varphi,\psi_n\right>}{\left<\varphi,\varphi\right>}\left< \psi_n, \psi_k\left<\psi_k,\varphi\right>\right>.$$

Next we observed the inner product between $\psi_k$ and $\varphi$ is just a scalar, so we pull it out as well

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \sum_{n}\frac{\left<\varphi,\psi_n\right>\left<\psi_k,\varphi\right>}{\left<\varphi,\varphi\right>}\left< \psi_n, \psi_k\right>.$$

We observed next that $\left<\psi_n,\psi_k\right>$ is just the Kronecker delta and thus the sum evaluates to a single term 

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \frac{\left<\varphi,\psi_k\right>\left<\psi_k,\varphi\right>}{\left<\varphi,\varphi\right>}.$$

Finally, we simplify this expression to get 

$$\Tr(P_H(\{E_k\})\rho_\varphi) = \frac{|\left<\varphi,\psi_k\right>|^2}{\|\varphi\|^2} = \frac{\|P_k\varphi\|^2}{\|\varphi\|^2}.$$

Thus the probability of measuring energy $E_k$ when the system is in state $\rho_\varphi$ is given by 

$$\frac{\|P_k\varphi\|^2}{\|\varphi\|^2}.$$
</div>





