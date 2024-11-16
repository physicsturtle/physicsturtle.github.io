---
layout: lesson
title: Conduction electron self energy (spin operators) 
dept: physics
course: kondo-physics
unit: unit4
deptDisplay: Physics
courseDisplay: Kondo and Heavy Fermion physics
unitDisplay: Unit 4
---
The Hamiltonian of consideration is 

$$\Hhat = \sum_{\k\sigma} \xi_{\k\sigma} \chat^\dagger_{\k\sigma} \chat_{\k\sigma} + J\sum_{\alpha\beta} \chat^\dagger_{0\alpha}\frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\chat_{0\beta} \cdot \Shat_0$$

The conduction electron self-energy is found by expanding the Green function, taking only the 1PI diagrams, and then stripping off the external legs. The Green function is given by 

$$\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') = -\langle T_\tau[\chat_{\k\sigma}(\tau)\chat^\dagger_{\k'\sigma}]\rangle = -\frac{\langle T_\tau[\Uhat_I(\beta,0)\chat_{\k\sigma,I}(\tau)\chat^\dagger_{\k'\sigma'}]\rangle_0}{\langle \Uhat_I(\beta,0) \rangle_0}$$

and the interaction picture time evolution operator is 

$$\Uhat_I(\beta,0) = T_\tau\exp\left(-\int_0^\beta J\sum_{\alpha\beta} \chat^\dagger_{0\alpha,I}(\tau) \frac{\boldsymbol{\sigma}_{\alpha\beta}}{2}\chat_{0\beta,I}(\tau) \cdot \Shat_0(\tau) \d\tau\right)$$

Note that the self-energy, which consists of connected 1PI diagrams, has a clear meaning even when there are spins. The connectedness refers to connectedness of the external lines to the internal vertices. The 1PI refers to not having a conduction electron line which can be cut. The Dyson equation defining the self-energy is given by (DO WE NEED DIVISION BY NUMBER OF SITES FOR THE MOMENTUM SUMS?)

$$\mathcal{G}(\k,\tau;\k';0) = \mathcal{G}_0(\k,\tau;\k',0) + \sum_{\k_1\k_2}\int_0^\beta\int_0^\beta \mathcal{G}_0(\k,\tau;\k_1,\tau_1) \Sigma(\k_1,\tau_1;\k_2,\tau_2)\mathcal{G}(\k_2,\tau_2,\k',0) \d\tau_1\d\tau_2$$

For the Kondo effect, we know that \\(\mathcal{G}\_0(\k,\tau;\k',\tau') = \delta\_{\k\k'}\mathcal{G}\_0(\k,\tau-\tau')\\), so the Dyson equation becomes 

$$\mathcal{G}(\k,\tau;\k') = \delta_{\k\k'}\mathcal{G}_0(\k,\tau) + \sum_{\k_2}\int_0^\beta\int_0^\beta \mathcal{G}_0(\k,\tau-\tau_1) \Sigma(\k,\tau_1-\tau_2;\k_2)\mathcal{G}(\k_2,\tau_2,\k',0) \d\tau_1\d\tau_2$$

At order 0, we have that 

$$\mathcal{G}(\k,\tau;\k') = -\langle T_\tau[\chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k\sigma}]\rangle_0 = \mathcal{G}_0(\k,\tau)$$

At order 1, we have that FILL THIS IN

$$\mathcal{G}(\k,\tau;\k') = -\langle T_\tau[\chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k\sigma}]\rangle_0 = \mathcal{G}_0(\k,\tau)$$


### Conduction electron self-energy: Second order


$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^2}{2}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2}\sum_{\alpha_1\beta_1} \sum_{\alpha_2\beta_2} \frac{\sigma^{\ell_1}_{\alpha_1\beta_1}}{2} \frac{\sigma^{\ell_2}_{\alpha_2\beta_2}}{2} \\
&\times\langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1) \chat_{0\beta_1,I}(\tau_1) \Shat^{\ell_1}_0(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2) \chat_{0\beta_2,I}(\tau_2) \Shat^{\ell_2}_0(\tau_2) \chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}]\rangle_{0,\text{conn},1PI} \d\tau_1\d\tau_2
\end{align}$$

The correlation functions are separated for the spins and the fermions. Thus, we can write this as 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^2}{2}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2} \sum_{\alpha_1\beta_1} \sum_{\alpha_2\beta_2} \frac{\sigma^{\ell_1}_{\alpha_1\beta_1}}{2} \frac{\sigma^{\ell_2}_{\alpha_2\beta_2}}{2} \langle T_\tau[\Shat^{\ell_1}_0(\tau_1) \Shat^{\ell_2}_0(\tau_2)]\rangle_0 \\
&\times\langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1) \chat_{0\beta_1,I}(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2) \chat_{0\beta_2,I}(\tau_2) \chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}]\rangle_{0,\text{conn},1PI} \d\tau_1\d\tau_2
\end{align}$$

Since \\(\Shat^{\ell\_1}\_0(\tau\_1)\Shat^{\ell\_2}\_0(\tau\_2)\\) is actually <i>independent of time</i> (because the free Hamiltonian does not time-evolve the spin operators, we just need to worry about the time-ordering. 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1) \Shat^{\ell_2}_0(\tau_2)]\rangle_0 ={}& \theta(\tau_1-\theta_2)\langle \Shat^{\ell_1}\Shat^{\ell_2}\rangle_0 + \theta(\tau_2-\tau_1)\langle \Shat^{\ell_2}\Shat^{\ell_1}\rangle_0 \\
={}& \frac{1}{2}[\theta(\tau_1-\theta_2)\tr(\Shat^{\ell_1}\Shat^{\ell_2}) + \theta(\tau_2-\tau_1) \tr(\Shat^{\ell_2}\Shat^{\ell_1})] \\
={}& \frac{1}{8}\tr(\sigma^{\ell_1}\sigma^{\ell_2}) \\
={}& \frac{1}{4}\delta_{\ell_1\ell_2}
\end{align}$$

where we did not need to worry about the time-ordering after all, because the trace evaluates to the same thing in both cases. Also note the additional factor of 2 is from the partition function for spins, which is \\(Z = 2\\). Then, we get the simplification 

$$\begin{align}
\mathcal{G}(\k,\tau;\k') ={}& -\frac{(-J)^2}{8}\int_0^\beta\int_0^\beta \sum_{\ell} \sum_{\alpha_1\beta_1} \sum_{\alpha_2\beta_2} \frac{\sigma^{\ell}_{\alpha_1\beta_1}}{2} \frac{\sigma^{\ell}_{\alpha_2\beta_2}}{2}  \\
&\times\langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1) \chat_{0\beta_1,I}(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2) \chat_{0\beta_2,I}(\tau_2)  \chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}]\rangle_{0,\text{conn},1PI} \d\tau_1\d\tau_2
\end{align}$$

Since it is possible to interchange the two vertices, we can multiply the result by 2 and apply Wick's theorem. We get that one of the 2 options for the correlator is

$$\begin{align}
C ={}& \langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1) \chat_{0\beta_1,I}(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2) \chat_{0\beta_2,I}(\tau_2)  \chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}]\rangle_{0,\text{conn},1PI} \\
={}& -\langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1)\chat_{\k\sigma,I}(\tau)]\rangle_0 \langle T_\tau[\chat_{0\beta_1,I}(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2)]\rangle_0 \langle T_\tau[\chat_{0\beta_2,I}(\tau_2)\chat^\dagger_{\k'\sigma'}]\rangle_0 \\
={}& \frac{1}{N_s^2}\sum_{\k_1\k_2\k_3\k_4}\langle T_\tau[\chat_{\k\sigma,I}(\tau)\chat^\dagger_{\k_1\alpha_1,I}(\tau_1)]\rangle_0 \langle T_\tau[\chat_{\k_2\beta_1,I}(\tau_1) \chat^\dagger_{\k_3\alpha_2,I}(\tau_2)]\rangle_0 \langle T_\tau[\chat_{\k_4\beta_2,I}(\tau_2)\chat^\dagger_{\k'\sigma'}]\rangle_0 \\ 
={}& -\frac{1}{N_s^2}\sum_{\k_1\k_2\k_3\k_4}\mathcal{G}_0(\k,\tau-\tau_1)\delta_{\sigma\alpha_1}\delta_{\k\k_1} \mathcal{G}_0(\k_2,\tau_1-\tau_2)\delta_{\beta_1\alpha_2}\delta_{\k_2\k_3} \mathcal{G}_0(\k_4,\tau_2) \delta_{\beta_2\sigma'}\delta_{\k_4\k'} \\
={}& -\frac{1}{N_s^2}\sum_{\k_2}\mathcal{G}_0(\k,\tau-\tau_1)\delta_{\sigma\alpha_1} \mathcal{G}_0(\k_2,\tau_1-\tau_2)\delta_{\beta_1\alpha_2} \mathcal{G}_0(\k',\tau_2) \delta_{\beta_2\sigma'} 
\end{align}$$

Plugging this back in and multiplying by 2, we find (using \\(\sum\_\alpha \sigma^\ell\_{\sigma\alpha}\sigma^\ell\_{\alpha\sigma'} = \sigma^0\_{\sigma\sigma'}\delta\_{\ell\ell} + i\epsilon\_{\ell\ell k} \sigma^k\_{\sigma\sigma'} = \delta\_{\sigma\sigma'}\\))

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& \frac{J^2}{4}\int_0^\beta\int_0^\beta \sum_{\ell} \sum_{\alpha_1\beta_1} \sum_{\alpha_2\beta_2} \frac{\sigma^{\ell}_{\alpha_1\beta_1}}{2} \frac{\sigma^{\ell}_{\alpha_2\beta_2}}{2} \frac{1}{N_s^2}\sum_{\k_2}\mathcal{G}_0(\k,\tau-\tau_1)\delta_{\sigma\alpha_1} \mathcal{G}_0(\k_2,\tau_1-\tau_2)\delta_{\beta_1\alpha_2} \mathcal{G}_0(\k',\tau_2) \delta_{\beta_2\sigma}  \d\tau_1\d\tau_2 \\
={}& \frac{J^2}{4}\int_0^\beta\int_0^\beta \sum_{\ell} \sum_{\alpha} \frac{\sigma^{\ell}_{\sigma\alpha}}{2} \frac{\sigma^{\ell}_{\alpha\sigma'}}{2} \frac{1}{N_s^2}\sum_{\k_2}\mathcal{G}_0(\k,\tau-\tau_1) \mathcal{G}_0(\k_2,\tau_1-\tau_2) \mathcal{G}_0(\k',\tau_2) \d\tau_1\d\tau_2 \\
={}& \frac{J^2}{16}\int_0^\beta\int_0^\beta \sum_{\ell} \delta_{\sigma\sigma'} \frac{1}{N_s^2}\sum_{\k_2}\mathcal{G}_0(\k,\tau-\tau_1) \mathcal{G}_0(\k_2,\tau_1-\tau_2) \mathcal{G}_0(\k',\tau_2) \d\tau_1\d\tau_2 \\
={}& \frac{3\delta_{\sigma\sigma'}J^2}{16}\int_0^\beta\int_0^\beta \frac{1}{N_s^2}\sum_{\k_2}\mathcal{G}_0(\k,\tau-\tau_1) \mathcal{G}_0(\k_2,\tau_1-\tau_2) \mathcal{G}_0(\k',\tau_2) \d\tau_1\d\tau_2
\end{align}$$

Next, we need to deal with the conduction electron part. Now, Fourier transforming each of the Green functions (and self-energy) according to 

$$\mathcal{G}_0(\k,\tau) = \frac{1}{\beta}\sum_{i\omega} e^{-i\omega \tau} \mathcal{G}_0(\k,i\omega), \qquad \Sigma(\k,\tau) = \frac{1}{\beta}\sum_{i\omega} e^{-i\omega \tau} \Sigma(\k,i\omega)$$

we get 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& \frac{3J^2\delta_{\sigma\sigma'}}{16}\int_0^\beta\int_0^\beta \frac{1}{N_s^2\beta^3} \sum_{i\omega_1,i\omega_2,i\omega_3}\sum_{\k_2}\mathcal{G}_0(\k,i\omega_1) \mathcal{G}_0(\k_2,i\omega_2) \mathcal{G}_0(\k,i\omega_3) e^{-i\omega_1(\tau-\tau_1)} e^{-i\omega_2(\tau_1-\tau_2)} e^{-i\omega_3\tau_2} \d\tau_1\d\tau_2 \\
={}& \frac{3J^2\delta_{\sigma\sigma'}}{16} \frac{1}{N_s^2\beta} \sum_{i\omega_1,i\omega_2,i\omega_3}\sum_{\k_2}\mathcal{G}_0(\k,i\omega_1) \mathcal{G}_0(\k_2,i\omega_2) \mathcal{G}_0(\k',i\omega_3) e^{-i\omega_1\tau} \delta_{\omega_2,\omega_3} \delta_{\omega_1,\omega_2} \\
\mathcal{G}_{\sigma\sigma'}(\k,i\omega;\k') ={}& \frac{3J^2\delta_{\sigma\sigma'}}{16} \frac{1}{N_s^2} \sum_{\k_2}\mathcal{G}_0(\k,i\omega) \mathcal{G}_0(\k_2,i\omega) \mathcal{G}_0(\k',i\omega)
\end{align}$$

Then, if we strip off the external lines, the self-energy becomes 

$$\begin{align}
\Sigma_{\sigma\sigma'}(\k,i\omega;\k') ={}& \frac{3J^2\delta_{\sigma\sigma'}}{16}\frac{1}{N_s^2}\sum_{\k_2} \frac{1}{i\omega - \xi_{\k_2}} \\
\Sigma_{\sigma\sigma'}(\k,\omega+i\eta;\k') ={}& \frac{3J^2\delta_{\sigma\sigma'}}{16}\frac{1}{N_s^2}\sum_{\k_2} \frac{1}{\omega - \xi_{\k_2} + i\eta} \\
\Sigma^R_{\sigma\sigma'}(\k,\omega;\k') ={}& \frac{3J^2\delta_{\sigma\sigma'}}{16}\frac{1}{N_s^2}\sum_{\k_2} \left[\mathcal{P}\frac{1}{\omega - \xi_{\k_2}} -i\pi\delta(\omega-\xi_{\k_2})\right]
\end{align}$$

The imaginary part of the retarded self-energy, to second order in \\(J^2\\) is 

$$\Sigma^R_{\sigma\sigma'}(\k,\omega;\k') = \frac{-3J^2\pi\rho(\omega)}{16N_s}$$

### Conduction electron self-energy: Third order

The third order contribution to the self-energy is given by 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^3}{3!}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2\ell_3}\sum_{\alpha_1\beta_1} \sum_{\alpha_2\beta_2} \sum_{\alpha_3\beta_3} \frac{\sigma^{\ell_1}_{\alpha_1\beta_1}}{2} \frac{\sigma^{\ell_2}_{\alpha_2\beta_2}}{2} \frac{\sigma^{\ell_3}_{\alpha_3\beta_3}}{2} \langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)]\rangle_0 \\
&\times\langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1) \chat_{0\beta_1,I}(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2) \chat_{0\beta_2,I}(\tau_2) \chat^\dagger_{0\alpha_3,I}(\tau_3) \chat_{0\beta_3,I}(\tau_3) \chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}]\rangle_{0,\text{conn},1PI} \d\tau_1\d\tau_2\d\tau_3
\end{align}$$

The correlation function of the spins now depends on the order of the three spins. We get then that 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)]\rangle_0 ={}& \theta(\tau_1-\tau_2)\theta(\tau_2-\tau_3) \langle \Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3) \rangle_0 \\
&+ \theta(\tau_1-\tau_3)\theta(\tau_3-\tau_2) \langle \Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_2}_0(\tau_2) \rangle_0 \\
&+ \theta(\tau_2-\tau_1)\theta(\tau_1-\tau_3) \langle \Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_3}_0(\tau_3) \rangle_0 \\
&+ \theta(\tau_2-\tau_3)\theta(\tau_3-\tau_1) \langle \Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_1}_0(\tau_1) \rangle_0 \\
&+ \theta(\tau_3-\tau_1)\theta(\tau_1-\tau_2) \langle \Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2) \rangle_0 \\
&+ \theta(\tau_3-\tau_2)\theta(\tau_2-\tau_1) \langle \Shat^{\ell_3}_0(\tau_3)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_1}_0(\tau_1) \rangle_0
\end{align}$$

Then, we can remove the time arguments of the spin operators:

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)]\rangle_0 ={}& \theta(\tau_1-\tau_2)\theta(\tau_2-\tau_3) \langle \Shat^{\ell_1}_0\Shat^{\ell_2}_0\Shat^{\ell_3}_0 \rangle_0 + \theta(\tau_1-\tau_3)\theta(\tau_3-\tau_2) \langle \Shat^{\ell_1}_0\Shat^{\ell_3}_0\Shat^{\ell_2}_0 \rangle_0 \\
&+ \theta(\tau_2-\tau_1)\theta(\tau_1-\tau_3) \langle \Shat^{\ell_2}_0\Shat^{\ell_1}_0\Shat^{\ell_3}_0 \rangle_0 + \theta(\tau_2-\tau_3)\theta(\tau_3-\tau_1) \langle \Shat^{\ell_2}_0\Shat^{\ell_3}_0\Shat^{\ell_1}_0 \rangle_0 \\
&+ \theta(\tau_3-\tau_1)\theta(\tau_1-\tau_2) \langle \Shat^{\ell_3}_0\Shat^{\ell_1}_0\Shat^{\ell_2}_0 \rangle_0 + \theta(\tau_3-\tau_2)\theta(\tau_2-\tau_1) \langle \Shat^{\ell_3}_0\Shat^{\ell_2}_0\Shat^{\ell_1}_0 \rangle_0
\end{align}$$

Then, we have that the trace can shuffle around the operators, and we can combine a few terms together: 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)]\rangle_0 ={}& [\theta(\tau_1-\tau_2)\theta(\tau_2-\tau_3) + \theta(\tau_2-\tau_3)\theta(\tau_3-\tau_1) + \theta(\tau_3-\tau_1)\theta(\tau_1-\tau_2)]\langle \Shat^{\ell_1}_0\Shat^{\ell_2}_0\Shat^{\ell_3}_0 \rangle_0 \\
&+ [\theta(\tau_1-\tau_3)\theta(\tau_3-\tau_2) + \theta(\tau_2-\tau_1)\theta(\tau_1-\tau_3) + \theta(\tau_3-\tau_2)\theta(\tau_2-\tau_1)]\langle \Shat^{\ell_1}_0\Shat^{\ell_3}_0\Shat^{\ell_2}_0 \rangle_0
\end{align}$$

Then, the combinations of spin operators become 

$$\begin{align}
\langle \Shat^{\ell_1}_0\Shat^{\ell_2}_0\Shat^{\ell_3}_0 \rangle_0 ={}& \frac{1}{2}\tr(\Shat^{\ell_1}_0 \Shat^{\ell_2}_0 \Shat^{\ell_3}_0) \\
={}& \frac{1}{16}\tr(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}) \\
={}& \frac{1}{8}i\epsilon_{\ell_1\ell_2\ell_3}
\end{align}$$

$$\begin{align}
\langle \Shat^{\ell_1}_0\Shat^{\ell_3}_0\Shat^{\ell_2}_0 \rangle_0 ={}& \frac{1}{8}i\epsilon_{\ell_1\ell_3\ell_2}
\end{align}$$

Plugging these in, we get 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)]\rangle_0 ={}& \frac{i}{8}[\theta(\tau_1-\tau_2)\theta(\tau_2-\tau_3) + \theta(\tau_2-\tau_3)\theta(\tau_3-\tau_1) + \theta(\tau_3-\tau_1)\theta(\tau_1-\tau_2)]\epsilon_{\ell_1\ell_2\ell_3} \\
&+ \frac{i}{8}[\theta(\tau_1-\tau_3)\theta(\tau_3-\tau_2) + \theta(\tau_2-\tau_1)\theta(\tau_1-\tau_3) + \theta(\tau_3-\tau_2)\theta(\tau_2-\tau_1)]\epsilon_{\ell_1\ell_3\ell_2}
\end{align}$$

Then using the fact that \\(\theta(x) = 1 - \theta(-x)\\), we can simplify this to 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)]\rangle_0 ={}& \frac{i\epsilon_{\ell_1\ell_2\ell_3}}{8}[\theta(\tau_1 - \tau_2) - \theta(\tau_3 - \tau_2) + \theta(\tau_2 - \tau_3) - \theta(\tau_1 - \tau_3) + \theta(\tau_3 - \tau_1) - \theta(\tau_2 - \tau_1)] 
\end{align}$$

Then using the fact that \\(\theta(x) - \theta(-x) = \sgn(x)\\), this becomes 

$$\begin{align}
\langle T_\tau[\Shat^{\ell_1}_0(\tau_1)\Shat^{\ell_2}_0(\tau_2)\Shat^{\ell_3}_0(\tau_3)]\rangle_0 ={}& \frac{i\epsilon_{\ell_1\ell_2\ell_3}}{8}[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)] 
\end{align}$$

Now, let's plug this in to the Green function calculation. The Green function is given by (plugging in our result for the spin correlation functions) 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^3}{3!}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2\ell_3}\sum_{\alpha_1\beta_1} \sum_{\alpha_2\beta_2} \sum_{\alpha_3\beta_3} \frac{\sigma^{\ell_1}_{\alpha_1\beta_1}}{2} \frac{\sigma^{\ell_2}_{\alpha_2\beta_2}}{2} \frac{\sigma^{\ell_3}_{\alpha_3\beta_3}}{2} \frac{i\epsilon_{\ell_1\ell_2\ell_3}}{8}[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1) \chat_{0\beta_1,I}(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2) \chat_{0\beta_2,I}(\tau_2) \chat^\dagger_{0\alpha_3,I}(\tau_3) \chat_{0\beta_3,I}(\tau_3) \chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}]\rangle_{0,\text{conn},1PI} \d\tau_1\d\tau_2\d\tau_3
\end{align}$$

I was unable to find a nice way to evaluate the sums over \\(\ell\_1,\ell\_2,\ell\_3\\), so let's just evaluate the Wick's theorem for conduction electrons first. There are 3 options for contracting with \\(\chat\_{\k\sigma,I}(\tau)\\), and therefore 2 options for contracting with \\(\chat^\dagger\_{\k'\sigma'}\\). For the remaining operators, they can be contracted amongst themselves in only one way. All of these diagrams are topologically equivalent. We therefore multiply by 6, and select just one of them. We find 

$$\begin{align}
Wick ={}& \langle T_\tau[\chat^\dagger_{0\alpha_1,I}(\tau_1) \chat_{0\beta_1,I}(\tau_1) \chat^\dagger_{0\alpha_2,I}(\tau_2) \chat_{0\beta_2,I}(\tau_2) \chat^\dagger_{0\alpha_3,I}(\tau_3) \chat_{0\beta_3,I}(\tau_3) \chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}]\rangle_{0,\text{conn},1PI} \\
={}& 6\langle T_\tau[\chat_{\k\sigma,I}(\tau)\chat^\dagger_{0\alpha_1,I}(\tau_1)]\rangle_0 \langle T_\tau[\chat_{0\beta_1,I}(\tau_1)\chat^\dagger_{0\alpha_2,I}(\tau_2)]\rangle_0 \langle T_\tau[\chat_{0\beta_2,I}(\tau_2)\chat^\dagger_{0\alpha_3,I}(\tau_3)]\rangle_0 \langle T_\tau[\chat_{0\beta_3,I}(\tau_3)\chat^\dagger_{\k'\sigma',I}]\rangle_0 \\
\end{align}$$

The noninteracting Green function is quite straightforward, and is given by 

$$\langle T_\tau[\chat_{\k\sigma,I}(\tau) \chat^\dagger_{\k'\sigma'}(\tau')]\rangle = (\theta(\tau-\tau') - n_F(\xi_{\k})) e^{-(\tau-\tau')\xi_{\k}} \delta_{\k\k'}\delta_{\sigma\sigma'}$$

To actually write this, we need to take all of the operators and Fourier transform them into momentum space: 

$$\begin{align}
wick ={}& \frac{6}{N_s^3}\sum_{\substack{\k_1\q_1\k_2 \\ \q_2\k_3\q_3}} \langle T_\tau[\chat_{\k\sigma,I}(\tau)\chat^\dagger_{\k_1\alpha_1,I}(\tau_1)]\rangle_0 \langle T_\tau[\chat_{\q_1\beta_1,I}(\tau_1)\chat^\dagger_{\k_2\alpha_2,I}(\tau_2)]\rangle_0 \langle T_\tau[\chat_{\q_2\beta_2,I}(\tau_2)\chat^\dagger_{\k_3\alpha_3,I}(\tau_3)]\rangle_0 \langle T_\tau[\chat_{\q_3\beta_3,I}(\tau_3)\chat^\dagger_{\k'\sigma',I}]\rangle_0 \\
={}& \frac{6}{N_s^3}\sum_{\substack{\k_1\q_1\k_2 \\ \q_2\k_3\q_3}} \delta_{\k\k_1}\delta_{\q_1\k_2}\delta_{\q_2\k_3}\delta_{\q_3\k'} \delta_{\sigma\alpha_1}\delta_{\beta_1\alpha_2}\delta_{\beta_2\alpha_3}\delta_{\beta_3\sigma'} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\q_3,\tau_3)
\end{align}$$

Then, we  can perform the sums over \\(\k\_1,\k\_2,\k\_3\\), and \\(\q\_3\\). This is easy, because of the delta functions. 

$$\begin{align}
wick ={}& \frac{6}{N_s^3}\sum_{\q_1\q_2} \delta_{\sigma\alpha_1}\delta_{\beta_1\alpha_2}\delta_{\beta_2\alpha_3}\delta_{\beta_3\sigma'} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3)
\end{align}$$

Now plugging this in to the Green function, we find 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^3}{3!}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2\ell_3}\sum_{\alpha_1\beta_1} \sum_{\alpha_2\beta_2} \sum_{\alpha_3\beta_3} \frac{\sigma^{\ell_1}_{\alpha_1\beta_1}}{2} \frac{\sigma^{\ell_2}_{\alpha_2\beta_2}}{2} \frac{\sigma^{\ell_3}_{\alpha_3\beta_3}}{2} \frac{i\epsilon_{\ell_1\ell_2\ell_3}}{8}[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{6}{N_s^3}\sum_{\q_1\q_2} \delta_{\sigma\alpha_1}\delta_{\beta_1\alpha_2}\delta_{\beta_2\alpha_3}\delta_{\beta_3\sigma'} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3) \d\tau_1\d\tau_2\d\tau_3
\end{align}$$

Now we evaluate the sums over \\(\alpha\_1,\alpha\_2,\alpha\_3,\beta\_3\\), which gives us 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^3}{3!}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2\ell_3}\sum_{\beta_1\beta_2}  \frac{\sigma^{\ell_1}_{\sigma\beta_1}}{2} \frac{\sigma^{\ell_2}_{\beta_1\beta_2}}{2} \frac{\sigma^{\ell_3}_{\beta_2\sigma'}}{2} \frac{i\epsilon_{\ell_1\ell_2\ell_3}}{8}[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{6}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3) \d\tau_1\d\tau_2\d\tau_3
\end{align}$$

Next, we use \\(\sum\_{\beta\_1} \sigma^{\ell\_1}\_{\sigma\beta\_1} \sigma^{\ell\_2}\_{\beta\_1\beta\_2} = \delta\_{\ell\_1\ell\_2}\sigma^0\_{\sigma\beta\_2} + i\epsilon\_{\ell\_1\ell\_2 r}\sigma^r\_{\sigma\beta\_2}\\):

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^3}{2^6}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2\ell_3}\sum_{\beta_2}  (\delta_{\ell_1\ell_2}\sigma^0_{\sigma\beta_2} + \sum_r i\epsilon_{\ell_1\ell_2 r}\sigma^r_{\sigma\beta_2}) \sigma^{\ell_3}_{\beta_2\sigma'} i\epsilon_{\ell_1\ell_2\ell_3}[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3) \d\tau_1\d\tau_2\d\tau_3 \\
={}& -\frac{(-J)^3}{2^6}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2\ell_3r}\sum_{\beta_2}  i\epsilon_{\ell_1\ell_2 r}\sigma^r_{\sigma\beta_2} \sigma^{\ell_3}_{\beta_2\sigma'} i\epsilon_{\ell_1\ell_2\ell_3}[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3) \d\tau_1\d\tau_2\d\tau_3 
\end{align}$$

Next, we use \\(\sum\_{\beta\_2} \sigma^{r}\_{\sigma\beta\_2} \sigma^{\ell\_3}\_{\beta\_2\sigma'} = \delta\_{r\ell\_3}\sigma^0\_{\sigma\sigma'} + i\epsilon\_{r\ell\_3s}\sigma^s\_{\sigma\sigma'}\\):

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^3}{2^6}\int_0^\beta\int_0^\beta \sum_{\ell_1\ell_2\ell_3r} i\epsilon_{\ell_1\ell_2 r}(\delta_{r\ell_3}\sigma^0_{\sigma\sigma'} + \sum_s i\epsilon_{r\ell_3s}\sigma^s_{\sigma\sigma'})i\epsilon_{\ell_1\ell_2\ell_3}[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3) \d\tau_1\d\tau_2\d\tau_3 
\end{align}$$

Then, there are two sums that we need to evaluate are 

$$\sum_{\ell_1\ell_2\ell_3r}\epsilon_{\ell_1\ell_2r}\delta_{r\ell_3}\epsilon_{\ell_1\ell_2\ell_3} = 6$$
$$\sum_{\ell_1\ell_2\ell_3r}\epsilon_{\ell_1\ell_2r}\epsilon_{r\ell_3s}\epsilon_{\ell_1\ell_2\ell_3} = \sum_{\ell_1\ell_2\ell_3} (\delta_{\ell_1\ell_3}\delta_{\ell_2s} - \delta_{\ell_1s} \delta_{\ell_2\ell_3})\epsilon_{\ell_1\ell_2\ell_3} = 0$$

Then, we find that 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& -\frac{(-J)^3\delta_{\sigma\sigma'}}{2^6}\int_0^\beta\int_0^\beta\int_0^\beta 6i^2[\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3) \d\tau_1\d\tau_2\d\tau_3 \\
={}& \frac{3(-J)^3\delta_{\sigma\sigma'}}{2^5}\int_0^\beta\int_0^\beta\int_0^\beta [\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,\tau-\tau_1)\mathcal{G}_0(\q_1,\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3)\mathcal{G}_0(\k',\tau_3) \d\tau_1\d\tau_2\d\tau_3
\end{align}$$

To evaluate the integrals over \\(\tau\_1,\tau\_2,\tau\_3\\), we plug in the Green function

$$\mathcal{G}_0(\k,\tau) = -(\theta(\tau) - n_F(\xi_{\k}))e^{-\tau\xi_{\k}}$$

Plugging it in gives us 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& \frac{3(-J)^3\delta_{\sigma\sigma'}}{2^5}\int_0^\beta\int_0^\beta\int_0^\beta [\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} (\theta(\tau-\tau_1) - n_F(\xi_{\k}))e^{-(\tau-\tau_1)\xi_{\k}} (\theta(\tau_1-\tau_2) - n_F(\xi_{\q_1}))e^{-(\tau_1-\tau_2)\xi_{\q_1}} \\
&\times (\theta(\tau_2-\tau_3) - n_F(\xi_{\q_2}))e^{-(\tau_2-\tau_3)\xi_{\q_2}} (\theta(\tau_3) - n_F(\xi_{\k'}))e^{-\tau_3\xi_{\k'}}\d\tau_1\d\tau_2\d\tau_3
\end{align}$$

Matching this with the definition of the self-energy, we have that 

$$\Sigma(\k,\tau_1-\tau_3;\k_2) = \frac{1}{N_s^3}\sum_{\q_1\q_2}\int_0^\beta \mathcal{G}_0(\q_1(\tau_1-\tau_2)\mathcal{G}_0(\q_2,\tau_2-\tau_3) [\sgn(\tau_1-\tau_2) + \sgn(\tau_2-\tau_3) + \sgn(\tau_3-\tau_1)]\d\tau_2$$

To match with the definition of the self-energy, we need to perform the integral over \\(\tau\_2\\). Some useful identities are:

$$\begin{align}
\theta(x) - n_F(\xi) ={}& \sgn(x)n_F(-\sgn(x)\xi) \\
\sgn(x)(\theta(x) - n_F(\xi)) ={}& n_F(-\sgn(x)\xi) \\
={}& 
\end{align}$$


This gives us 

\begin{align*}
I_1 ={}& \int_0^\beta \sgn(\tau_1-\tau_2) (\theta(\tau_1-\tau_2) - n_F(\xi_{\q_1}))e^{\tau_2(\xi_{\q_1} - \xi_{\q_2})} (\theta(\tau_2-\tau_3) - n_F(\xi_{\q_2})) \d\tau_2 \\
={}& \int_0^\beta  n_F(\sgn(\tau_2-\tau_1)\xi_{\q_1}))e^{\tau_2(\xi_{\q_1} - \xi_{\q_2})}\sgn(\tau_2-\tau_3) n_F(\sgn(\tau_3-\tau_2)\xi_{\q_2})) \d\tau_2 \\
={}& \begin{cases} 
[\int_0^{\tau_3} + \int_{\tau_3}^{\tau_1} + \int_{\tau_1}^\beta][n_F(\sgn(\tau_2-\tau_1)\xi_{\q_1}))e^{\tau_2(\xi_{\q_1} - \xi_{\q_2})}\sgn(\tau_2-\tau_3) n_F(\sgn(\tau_3-\tau_2)\xi_{\q_2})) \d\tau_2] & \tau_1 > \tau_3 \\
[\int_0^{\tau_1} + \int_{\tau_1}^{\tau_3} + \int_{\tau_3}^\beta][n_F(\sgn(\tau_2-\tau_1)\xi_{\q_1}))e^{\tau_2(\xi_{\q_1} - \xi_{\q_2})}\sgn(\tau_2-\tau_3) n_F(\sgn(\tau_3-\tau_2)\xi_{\q_2})) \d\tau_2] & \tau_1 < \tau_3
\end{cases}
\end{align*}

$$\begin{align}
I_2 ={}& \int_0^\beta \sgn(\tau_2-\tau_3) (\theta(\tau_1-\tau_2) - n_F(\xi_{\q_1}))e^{\tau_2(\xi_{\q_1} - \xi_{\q_2})} (\theta(\tau_2-\tau_3) - n_F(\xi_{\q_2})) \d\tau_2 \\
={}& \int_0^\beta  \sgn(\tau_1-\tau_2)n_F(\sgn(\tau_2-\tau_1)\xi_{\q_1}))e^{\tau_2(\xi_{\q_1} - \xi_{\q_2})} n_F(\sgn(\tau_3-\tau_2)\xi_{\q_2})) \d\tau_2 \\
\end{align}$$

$$\int_0^\beta \sgn(\tau_3-\tau_1) (\theta(\tau_1-\tau_2) - n_F(\xi_{\q_1}))e^{\tau_2(\xi_{\q_1} - \xi_{\q_2})} (\theta(\tau_2-\tau_3) - n_F(\xi_{\q_2})) \d\tau_2 = $$ 







Before we evaluate the integrals over \\(\tau\_1,\tau\_2,\tau\_3\\), let's transform the Green functions into Matsubara space: 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& \frac{3(-J)^3\delta_{\sigma\sigma'}}{2^5\beta^4}\sum_{\omega,\omega_1,\omega_2,\omega_3} \int_0^\beta\int_0^\beta [\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]  \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,i\omega) e^{-i\omega(\tau-\tau_1)}\mathcal{G}_0(\q_1,i\omega_1) e^{-i\omega_1(\tau_1-\tau_2)}\mathcal{G}_0(\q_2,i\omega_2) e^{-i\omega_2(\tau_2-\tau_3)}\mathcal{G}_0(\k',i\omega_3) e^{-i\omega_3\tau_3} \d\tau_1\d\tau_2\d\tau_3
\end{align}$$

Then, we perform the time integrals. For the first term, we integrate over \\(\tau\_3\\) first, for the second term, we integrate over \\(\tau\_1\\) first, and for the third term, we integrate over \\(\tau\_2\\) first. This gives us 

$$\begin{align}
I ={}& \int_0^\beta\int_0^\beta\int_0^\beta [\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]e^{-i\omega\tau} e^{i\tau_1(\omega-\omega_1)}e^{i\tau_2(\omega_1-\omega_2)} e^{i\tau_3(\omega_2-\omega_3)} \d\tau_1\d\tau_2\d\tau_3 \\
={}& \beta\int_0^\beta\int_0^\beta \sgn(\tau_1 - \tau_2)\delta_{\omega_2\omega_3}e^{-i\omega\tau} e^{i\tau_1(\omega-\omega_1)}e^{i\tau_2(\omega_1-\omega_2)} \d\tau_1\d\tau_2 \\
&+ \beta\int_0^\beta\int_0^\beta\sgn(\tau_2-\tau_3)e^{-i\omega\tau}\delta_{\omega\omega_1}e^{i\tau_2(\omega_1-\omega_2)}e^{i\tau_3(\omega_2-\omega_3)} \d\tau_2\d\tau_3\\
&+ \beta\int_0^\beta\int_0^\beta\delta_{\omega_1\omega_2}\sgn(\tau_3-\tau_1)e^{-i\omega\tau}e^{i\tau_1(\omega-\omega_1)}e^{i\tau_3(\omega_2-\omega_3)}\d\tau_1\d\tau_3 
\end{align}$$

Now, for the first term we evaluate the integral over \\(\tau\_2\\), for the second one we evaluate the integral over \\(\tau\_3\\), and for the third term we evaluate the integral over \\(\tau\_1\\). This gives us 

$$\begin{align}
I ={}& \beta\int_0^\beta \delta_{\omega_2\omega_3}e^{-i\omega\tau} e^{i\tau_1(\omega-\omega_1)}\frac{e^{i\tau_1(\omega_1-\omega_2)}-1}{i(\omega_1-\omega_2)} \d\tau_1 + \beta\int_0^\beta e^{-i\omega\tau}\delta_{\omega\omega_1}e^{i\tau_2(\omega_1-\omega_2)} \frac{e^{i\tau_2(\omega_2-\omega_3)}-1}{i(\omega_2-\omega_3)} \d\tau_2 \\
&+ \beta\int_0^\beta\delta_{\omega_1\omega_2}e^{-i\omega\tau} \frac{e^{i\tau_3(\omega-\omega_1)}-1}{i(\omega-\omega_1)} e^{i\tau_3(\omega_2-\omega_3)} \d\tau_3 
\end{align}$$

Now, we integrate over \\(\tau\_1\\), \\(\tau\_2\\), and \\(\tau\_3\\) for the first, second, and third terms, respectively. We find 

$$\begin{align}
I ={}& \beta^2 \delta_{\omega_2\omega_3}e^{-i\omega\tau} \frac{\delta_{\omega\omega_2} - \delta_{\omega\omega_1}}{i(\omega_1-\omega_2)} + \beta^2 e^{-i\omega\tau}\delta_{\omega\omega_1} \frac{\delta_{\omega_1\omega_3} - \delta_{\omega_1\omega_2}}{i(\omega_2-\omega_3)} + \beta^2\delta_{\omega_1\omega_2}e^{-i\omega\tau} \frac{\delta_{\omega\omega_3} - \delta_{\omega_2\omega_3}}{i(\omega-\omega_1)} 
\end{align}$$



 


$$\begin{align}
I ={}& \int_0^\beta\int_0^\beta\int_0^\beta [\sgn(\tau_1 - \tau_2) + \sgn(\tau_2 - \tau_3) + \sgn(\tau_3 - \tau_1)]e^{-i\omega\tau} e^{i\tau_1(\omega-\omega_1)}e^{i\tau_2(\omega_1-\omega_2)} e^{i\tau_3(\omega_2-\omega_3)} \d\tau_1\d\tau_2\d\tau_3 \\
={}& \int_0^\beta\int_0^\beta \left[\sgn(\tau_1 - \tau_2)\beta\delta_{\omega_2\omega_3} + 2\frac{e^{i\tau_2(\omega_2-\omega_3)}-1}{i(\omega_2-\omega_3)} + 2\frac{1 - e^{i\tau_1(\omega_2-\omega_3)}}{i(\omega_2-\omega_3)}\right]e^{-i\omega\tau} e^{i\tau_1(\omega-\omega_1)}e^{i\tau_2(\omega_1-\omega_2)} \d\tau_1\d\tau_2 \\
={}& \int_0^\beta\int_0^\beta \left[\sgn(\tau_1 - \tau_2)\beta\delta_{\omega_2\omega_3} + 2\frac{e^{i\tau_2(\omega_2-\omega_3)}-e^{i\tau_1(\omega_2-\omega_3)}}{i(\omega_2-\omega_3)}\right]e^{-i\omega\tau} e^{i\tau_1(\omega-\omega_1)}e^{i\tau_2(\omega_1-\omega_2)} \d\tau_1\d\tau_2
\end{align}$$

Now, we evaluate the integral over \\(\tau\_2\\). This gives us 

$$\begin{align}
I ={}& \int_0^\beta \left[2\frac{e^{i\tau_1(\omega_1-\omega_2)}-1}{i(\omega_1-\omega_2)}\beta\delta_{\omega_2\omega_3} + 2\frac{\beta\delta_{\omega_1\omega_3}-e^{i\tau_1(\omega_2-\omega_3)}\beta\delta_{\omega_1\omega_2}}{i(\omega_2-\omega_3)}\right]e^{-i\omega\tau} e^{i\tau_1(\omega-\omega_1)} \d\tau_1
\end{align}$$

Finally, we do the integral over \\(\tau\_1\\), which gives us 

$$\begin{align}
I ={}& \beta^2\left[2\frac{\delta_{\omega\omega_2}-\delta_{\omega\omega_1}}{i(\omega_1-\omega_2)}\delta_{\omega_2\omega_3} + 2\frac{\delta_{\omega\omega_1}\delta_{\omega_1\omega_3}-\delta_{\omega,\omega_1+\omega_3-\omega_2}\delta_{\omega_1\omega_2}}{i(\omega_2-\omega_3)}\right]e^{-i\omega\tau} \\
={}& 2\beta^2\left[\frac{\delta_{\omega\omega_2}-\delta_{\omega\omega_1}}{i(\omega_1-\omega_2)}\delta_{\omega_2\omega_3} + \frac{\delta_{\omega\omega_1}\delta_{\omega_1\omega_3}-\delta_{\omega\omega_3}\delta_{\omega_1\omega_2}}{i(\omega_2-\omega_3)}\right]e^{-i\omega\tau} \\
\end{align}$$

Plugging this back in, we find 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& \frac{3(-J)^3}{2^4\beta^2}\sum_{\omega,\omega_1,\omega_2,\omega_3} \left[\frac{\delta_{\omega\omega_2}-\delta_{\omega\omega_1}}{i(\omega_1-\omega_2)}\delta_{\omega_2\omega_3} + \frac{\delta_{\omega\omega_1}\delta_{\omega_1\omega_3}-\delta_{\omega\omega_3}\delta_{\omega_1\omega_2}}{i(\omega_2-\omega_3)}\right]e^{-i\omega\tau} \\
&\times\frac{1}{N_s^3}\sum_{\q_1\q_2} \mathcal{G}_0(\k,i\omega) \mathcal{G}_0(\q_1,i\omega_1) \mathcal{G}_0(\q_2,i\omega_2)\mathcal{G}_0(\k',i\omega_3)
\end{align}$$

Next, we simplify using the delta functions: 

$$\begin{align}
\mathcal{G}_{\sigma\sigma'}(\k,\tau;\k') ={}& \frac{3(-J)^3}{2^4\beta^2N_s^3}\sum_{\q_1\q_2}\sum_{\omega,\omega_1} e^{-i\omega\tau}\left[\frac{\mathcal{G}_0(\k,i\omega) \mathcal{G}_0(\q_1,i\omega_1) \mathcal{G}_0(\q_2,i\omega)\mathcal{G}_0(\k',i\omega)}{i(\omega_1-\omega)} - \frac{\mathcal{G}_0(\k,i\omega) \mathcal{G}_0(\q_1,i\omega) \mathcal{G}_0(\q_2,i\omega_1)\mathcal{G}_0(\k',i\omega_1)}{i(\omega-\omega_1)} \right. \\
&\left. +\frac{\mathcal{G}_0(\k,i\omega) \mathcal{G}_0(\q_1,i\omega) \mathcal{G}_0(\q_2,i\omega_1)\mathcal{G}_0(\k',i\omega)}{i(\omega_1-\omega)}-\frac{\mathcal{G}_0(\k,i\omega) \mathcal{G}_0(\q_1,i\omega_1) \mathcal{G}_0(\q_2,i\omega_1)\mathcal{G}_0(\k',i\omega)}{i(\omega_1-\omega)}\right] 
\end{align}$$

The first two terms are identical, which can be seen explicitly by swapping \\(\q\_1\\) and \\(\q\_2\\). The last two terms however require some additional massaging. 

