---
layout: lesson
title: Pairing requires an attractive interaction 
dept: physics
course: superconductivity
unit: unit4
deptDisplay: Physics
courseDisplay: Superconductivity & Superfluidity
unitDisplay: Unit 4
---
To understand the origin and consequences of pairing correlation, consider a pair of electrons (2\\(e^-\\)) interacting. The other electrons (\\(N-2\\) of them) are noninteracting, and form the Fermi sea. We assume that we have a translationally invariant system and spin-independent interactions. The goal of this section is to derive a rewriting of the Schrödinger equation in momentum space, which will allow us to show that, to form a bound state, an attractive interaction is required in at least one angular momentum channel.

To start, we consider the Hamiltonian for these two electrons and a two electron wave function:

$$\begin{equation}
\Hhat\ket{\psi} = (\Hhat_0 + \Vhat)\ket{\psi}
\end{equation}$$

The orbital wave function and spin wave function are both included in \\(\ket{\psi}\\). The Schrödinger equation for this situation is given by

$$\begin{equation}
-\frac{\hbar^2}{2m}(\nabla_1^2 + \nabla_2^2)\Psi(\x_1,\x_2,\sigma_1,\sigma_2) + (V(\x_1-\x_2) - E)\Psi(\x_1,\x_2,\sigma_1,\sigma_2) = 0
\end{equation}$$

where \\(\Psi(\x\_1,\x\_2,\sigma\_1,\sigma\_2) = -\Psi(\x\_2,\x\_1,\sigma\_2,\sigma\_1)\\), as is required by fermion statistics. Because the potential only depends on the distance between the two electrons, we introduce the relative and centre of mass coordinates 

$$\begin{equation}
\x = \x_1 - \x_2,\quad \mathbf{X} = \frac{1}{2}(\x_1+\x_2)
\end{equation}$$

which defines the new masses \\(M = 2m\\) (total mass) and \\(\mu = m/2\\) (effective mass). Then, we have the new Schrödinger equation 

$$\begin{equation}
-\frac{\hbar^2}{2}\left(\frac{\nabla_{\mathbf{X}}^2}{M} + \frac{\nabla_{\x}^2}{\mu}\right)\Psi(\mathbf{X},\x,\sigma_1,\sigma_2) + (V(\r) - E)\Psi(\boldsymbol{R},\r,\sigma_1,\sigma_2) = 0
\end{equation}$$

The new condition on \\(\Psi\\), in terms of these new variables, is \\(\Psi(\mathbf{X},\x,\sigma\_1,\sigma\_2) = -\Psi(\mathbf{X},-\x,\sigma\_2,\sigma\_1)\\). We see that the potential is independent of \\(\mathbf{X}\\), which means that the \\(\hat{\mathbf{P}}\\) operator commutes with the Hamiltonian. Therefore, we can separate the wave function into the centre of mass motion part, the relative part, and the spin part:

$$\begin{equation}
\psi(\mathbf{X},\x,\sigma_1,\sigma_2) = e^{i\K\cdot\mathbf{X}}\psi(\x)\chi_{\sigma_1\sigma_2}.
\end{equation}$$

The next step is to substitute this simplification into the Schrödinger equation, which yields

$$\begin{equation}
-\frac{\hbar^2}{2}\left(-\frac{\K^2}{M} + \frac{\nabla_{\r}^2}{\mu}\right)\psi(\x)\chi_{\sigma_1\sigma_2} + (V(\x) - E)\psi(\x)\chi_{\sigma_1\sigma_2} = 0.
\end{equation}$$

We define \\(\tilde{E} = E - \frac{\hbar^2\K^2}{2M}\\) to be the energy shifted by the centre of mass kinetic energy. We see that \\(\mathbf{K} = 0\\) minimizes the energy, so we take it to be zero. Then, we get 

$$\begin{equation}
-\frac{\hbar^2}{2\mu}\nabla_{\x}^2\phi(\x)\chi_{\sigma_1\sigma_2} + (V(\x) - \tilde{E})\phi(\r)\chi_{\sigma_1\sigma_2} = 0
\end{equation}$$

Because the potential is independent of spin, we can factor it out. Thus, we get the spatial Schrödinger equation for only the relative wave function:

$$\begin{equation}
-\frac{\hbar^2}{2\mu}\nabla_{\x}^2\phi(\x) + (V(\x) - \tilde{E})\phi(\x) = 0.
\end{equation}$$

Since we are working in a large box with periodic boundary conditions, the Fourier transform of the wave function is given by

$$\begin{equation}
\phi(\x) = \frac{1}{\sqrt{\V}}\sum_{\k} e^{i\k\cdot\x} \phi_{\k}
\end{equation}$$

which gives us 

$$\begin{equation}
\frac{1}{\sqrt{\V}}\sum_{\k}e^{i\k\cdot\x}\left[\frac{\hbar^2\k^2}{2\mu}\phi_{\k} + (V(\x) - \tilde{E})\phi_{\k}\right] = 0
\end{equation}$$

Then, multiplying by \\(e^{-i\k'\cdot\x}\\) on both sides and integrating, we get 

$$\begin{align}
\int \sum_{\k}e^{i(\k-\k')\cdot\x}\left[\frac{\hbar^2\k^2}{2\mu}\phi_{\k} + (V(\x) - \tilde{E})\phi_{\k}\right] \d^3\x = 0 \\
\sum_{\k}\left[2\epsilon_{\k}\phi_{\k}\V\delta_{\k\k'} + (V(\k'-\k) - \tilde{E}\V\delta_{\k\k'})\phi_{\k}\right] = 0
\end{align}$$

where \\(\V\\) is the volume of the system, and we have defined 

$$\begin{equation}
V(\k'-\k) = \int e^{i(\k-\k')\cdot\x} V(\x) \d^3\x
\end{equation}$$

The equation can then be rewritten by swapping \\(\k,\k'\\) to get 

$$\begin{align}
2\epsilon_{\k}\phi_{\k} + \frac{1}{\V}\sum_{\k'}V(\k-\k')\phi_{\k'} - \tilde{E}\phi_{\k} ={}& 0 \\
(2\epsilon_{\k} - \tilde{E})\phi_{\k} ={}& -\frac{1}{\V}\sum_{\k'} V(\k-\k') \phi_{\k'}
\end{align}$$

Based on the definition of \\(V(\k-\k')\\), we observe that it can only depend on the lengths of \\(\k,\k'\\), as well as the angle between them. We can expand it in partial waves by recalling the formula 

$$\begin{equation}
e^{ikr\cos\theta} = \sum_{\ell=0}^\infty i^\ell (2\ell+1)j_\ell(kr) P_\ell(\cos\theta)
\end{equation}$$

where \\(j\_\ell\\) is the spherical Bessel function of order \\(\ell\\) and \\(P\_\ell\\) is the Legendre polynomial of order \\(\ell\\). Then, if we orient the \\(\x\\) coordinate system so that its \\(z\\) axis lies along \\(\k\\), then we have that \\(\k = k\zhat\\). Thus, the above identity applies identically. For the \\(e^{i\k'\cdot\x}\\), this is a bit more difficult. We of course have \\(\x = r(\cos\varphi\sin\theta,\sin\varphi\sin\theta,\cos\theta)\\), and we also write \\(\k'\\) in spherical coordinates as \\(\k' = k'(\cos\varphi'\sin\theta',\sin\varphi'\sin\theta',\cos\theta')\\). Then, we have that 

$$\begin{equation}
\x\cdot\k' = k'r[\cos(\varphi-\varphi') \sin\theta\sin\theta' + \cos\theta\cos\theta']
\end{equation}$$

This means that 

$$\begin{align}
e^{-i\k'\cdot\x} ={}& e^{-ik'r(\cos(\varphi-\varphi') \sin\theta\sin\theta' + \cos\theta\cos\theta')} \\
={}& \sum_{\ell'=0}^\infty (-i)^{\ell'}(2\ell'+1) j_{\ell'}(k'r) P_{\ell'}(\cos(\varphi-\varphi') \sin\theta\sin\theta' + \cos\theta\cos\theta')
\end{align}$$

Substituting this in to the potential integral, we get 

$$\begin{align}
V(\k' - \k) ={}& \sum_{\ell,\ell'=0}^\infty \int_0^{2\pi} \int_0^\pi \int_0^\infty i^\ell (2\ell+1)j_\ell(kr) P_\ell(\cos\theta) \\
&\times (-i)^{\ell'}(2\ell'+1) j_{\ell'}(k'r) P_{\ell'}(\cos(\varphi-\varphi') \sin\theta\sin\theta' + \cos\theta\cos\theta') V(r) r^2\sin\theta \d r \d\theta \d\varphi
\end{align}$$

We can then use the identity

$$\begin{equation}
P_{\ell}(\cos(\varphi-\varphi') \sin\theta\sin\theta' + \cos\theta\cos\theta') = \sum_{m=-\ell}^\ell (-1)^m P^{-m}_\ell(\cos\theta) P^m_n(\cos\theta') \cos(m(\varphi-\varphi'))
\end{equation}$$

and then, since 

$$\begin{equation}
\int_0^{2\pi} \cos(m\varphi) \d\varphi = 2\pi \delta_{m,0}
\end{equation}$$

we get that

$$\begin{align}
\int_0^{2\pi} P_{\ell}(\cos(\varphi-\varphi') \sin\theta\sin\theta' + \cos\theta\cos\theta') \d\varphi ={}& \sum_{m=-\ell}^\ell (-1)^m P^{-m}_\ell(\cos\theta) P^m_n(\cos\theta') \int_0^{2\pi} \cos(m(\varphi-\varphi')) \d\varphi \\
={}& 2\pi\sum_{m=-\ell}^\ell (-1)^m P^{-m}_\ell(\cos\theta_1) P^m_n(\cos\theta_2) \delta_{m,0} \\
={}& 2\pi P^0_\ell(\cos\theta)P^0_\ell(\cos\theta') \\
={}& 2\pi P_\ell(\cos\theta)P_\ell(\cos\theta')
\end{align}$$

Thus, we have a vast simplification, and find that 

$$\begin{align}
V(\k' - \k) ={}& 2\pi \sum_{\ell,\ell'=0}^\infty \int_0^\pi \int_0^\infty i^\ell (2\ell+1)j_\ell(kr) P_\ell(\cos\theta) (-i)^{\ell'}(2\ell'+1) j_{\ell'}(k'r) V(r) P_{\ell'}(\cos\theta)P_{\ell'}(\cos\theta') r^2\sin\theta \d r \d\theta
\end{align}$$

Then, through the orthogonality relation of Legendre polynomials, which is 

$$\begin{equation}
\int_0^\pi P_\ell(\cos\theta) P_{\ell'}(\cos\theta)\sin\theta \d\theta = \frac{2\delta_{\ell\ell'}}{2\ell+1}
\end{equation}$$

we find that 

$$\begin{align}
V(\k' - \k) ={}& \sum_{\ell=0}^\infty \int_0^\infty (2\ell+1)j_\ell(kr) j_{\ell}(k'r) V(r) P_{\ell}(\cos\theta') r^2 \d r
\end{align}$$

Since \\(\cos\theta'\\) is the angle between \\(\k\\) and \\(\k'\\), we write \\(\cos\theta' = \khat\cdot\khat'\\), and thus 

$$\begin{align}
V(\k' - \k) ={}& \sum_{\ell=0}^\infty (2\ell+1) P_{\ell}(\khat\cdot\khat') V_\ell(k,k') 
\end{align}$$

whereby the partial wave component is given by

$$\begin{equation}
V_\ell(k,k') = 4\pi \int_0^\infty j_\ell(kr) j_{\ell}(k'r) V(r) r^2 \d r
\end{equation}$$

Now that we have expanded the potential in partial waves, we can do the same thing for the wave function. The wave function can be written as 

$$\begin{equation}
\phi(\k) = \sum_{\ell=0}^\infty \sum_{m=-\ell}^\ell \phi_{\ell m}(k) Y^m_\ell(\khat).
\end{equation}$$

Plugging in the expanded form of the wave function as well as the expanded form of the potential, we find 

$$\begin{align}
(2\epsilon_{\k} - \tilde{E})\sum_{\ell=0}^\infty \sum_{m=-\ell}^\ell \phi_{\ell m}(k) Y^m_\ell(\khat) = -\frac{1}{\V}\sum_{\k'}\sum_{\ell=0}^\infty (2\ell+1)V_{\ell}(k,k')P_{\ell}(\cos\theta)\sum_{\ell'=0}^\infty\sum_{m'=-\ell'}^{\ell'} \phi_{\ell' m'}(k') Y^{m'}_{\ell'}(\khat')
\end{align}$$

Then, we plug in the addition theorem for spherical harmonics:

$$\begin{equation}
P_\ell(\cos(\khat\cdot\khat')) = \frac{4\pi}{2\ell+1}\sum_{m=-\ell}^\ell Y^m_\ell(\khat)[Y^m_\ell]^*(\khat')
\end{equation}$$

which gives us 

$$\begin{align}
(2\epsilon_{\k} - \tilde{E})\sum_{\ell m} \phi_{\ell m}(k) Y^m_\ell(\khat) = -\frac{1}{\V}\sum_{\k'}\sum_{\ell m \ell' m'} 4\pi V_{\ell}(k,k') Y^m_\ell(\khat) [Y^m_\ell]^*(\khat') \phi_{\ell' m'}(k') Y^{m'}_{\ell'}(\khat')
\end{align}$$

The next step is to evaluate the sum (integral) over the angular part of \\(\k'\\), which gives us (using \\(\int Y^{m\*}\_\ell(\khat') Y^{m'}\_{\ell'}(\khat')\d\Omega' = \delta\_{\ell\ell'}\delta\_{mm'}\\))

$$\begin{align}
(2\epsilon_{\k} - \tilde{E})\sum_{\ell m} \phi_{\ell m}(k) Y^m_\ell(\khat) ={}& -\frac{1}{(2\pi)^3}\int \sum_{\ell m \ell' m'} 4\pi V_{\ell}(k,k') Y^m_\ell(\khat) [Y^m_\ell]^*(\khat') \phi_{\ell' m'}(k') Y^{m'}_{\ell'}(\khat') k^{\prime 2} \d k' \d\Omega' \\
={}& -\frac{(4\pi)}{(2\pi)^3}\int \sum_{\ell m \ell' m'} \delta_{\ell\ell'}\delta_{mm'} V_{\ell}(k,k') Y^m_\ell(\khat) \phi_{\ell' m'}(k') k^{\prime 2} \d k' \\
={}& -\frac{(4\pi)}{(2\pi)^3}\int \sum_{\ell m} V_{\ell}(k,k') Y^m_\ell(\khat) \phi_{\ell m}(k') k^{\prime 2} \d k'
\end{align}$$

Thus, we find that, taking the components of each side to be equal to one another (equivalent to multiplying both sides by \\(Y^{m'}\_{\ell'}(\khat)\\) and then integrating over \\(\d\Omega\\)) gives us

$$\begin{equation}
(2\epsilon_k - \tilde{E})\phi_{\ell m}(k) = -\frac{1}{(2\pi)^3}\int V_\ell(k,k') \phi_{\ell m}(k') (4\pi) k^{\prime 2} \d k'
\end{equation}$$

The point of this, is that if we want a bound state for the system, then the energy eigenvalue \\(\tilde{E}\\) should satisfy \\(\tilde{E} < 2\epsilon\_F\\). This is because the energy of the bound state must be less than just the kinetic energies of the two electrons comprising it. We see from this that if \\(\tilde{E}<2\epsilon\_F\\), then this implies that \\(V\_\ell < 0\\) when \\(\phi\_{\ell m} \neq 0\\). Thus, a bound state requires an effective <i>attraction</i>. 

