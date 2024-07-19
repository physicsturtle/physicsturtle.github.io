---
layout: lesson
title: Spin Density Wave Order 
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
In this section, we will use the path integral formalism to study the possibility of spin density waves in the Fermi Hubbard model. We will find for example a spin-density wave with wave vector \\((\pi,\pi)\\), which corresponds to the special case of antiferromagnetism. The Hubbard-Stratonovich field which we will use in this section is actually a vector field instead of the simpler fields that have been discussed so far. In the next section, where we discuss charge density wave order, there is a single Hubbard-Stratonovich field, but an additional complication arises which is not present in the spin density wave section. 

We remind the reader that the Hubbard model in the operator language is given by 

$$\begin{equation}
\Hhat = -t\sum_{\langle i,j\rangle,\sigma}(\chat^\dagger_{i\sigma}\chat_{j\sigma} + \hc) + U\sum_i \chat^\dagger_{i\uparrow}\chat^\dagger_{i\downarrow}\chat_{i\downarrow}\chat_{i\uparrow} - \mu\sum_{i\sigma}\chat^\dagger_{i\sigma}\chat_{i\sigma}.
\end{equation}$$

We note that this is not the true Hamiltonian; the true Hamiltonian does not include the chemical potential. Since we are however working in the grand canonical ensemble, it is convenient to include the chemical potential at this stage. This indicates that the corresponding effective action for the path integral is

$$\begin{equation}
S = \int_0^\beta\left[ \sum_{i,\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} -t\sum_{\langle i,j\rangle,\sigma}(\bar{c}_{i\tau\sigma}c_{j\tau\sigma} + \bar{c}_{j\tau\sigma}c_{i\tau\sigma}) + U\sum_i \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow} - \mu\sum_{i\sigma}\bar{c}_{i\tau\sigma}c_{i\tau\sigma}\right] \d\tau
\end{equation}$$

We split up this action into two parts: a non-interacting part \\(S_0\\) and an interacting part \\(S_{\text{int}}\\):

$$\begin{align}
S_0 ={}& \int_0^\beta\left[ \sum_{i,\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} -t\sum_{\langle i,j\rangle,\sigma}(\bar{c}_{i\tau\sigma}c_{j\tau\sigma} + \bar{c}_{j\tau\sigma}c_{i\tau\sigma}) - \mu\sum_{i\sigma}\bar{c}_{i\tau\sigma}c_{i\tau\sigma}\right] \d\tau \\
S_{\text{int}} ={}& \int_0^\beta U\sum_i \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow} \d\tau.
\end{align}$$

The partition function is simply written as 

$$\begin{equation}
Z = \int e^{-S_0 - S_{\text{int}}}\D\bar{c}\D c
\end{equation}$$

and now we perform a Hubbard-Stratonovich transformation on the interaction. We are looking for spin density wave order, so we want the Hubbard-Stratonovich field to couple to the spin operator

$$\begin{equation}
\mathbf{S}_{i\tau} = \bar{c}_{i\tau\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{i\tau\beta} = (\bar{c}_{i\tau\alpha}\sigma^x_{\alpha\beta} c_{i\tau\beta}, \bar{c}_{i\tau\alpha}\sigma^y_{\alpha\beta} c_{i\tau\beta}, \bar{c}_{i\tau\alpha}\sigma^z_{\alpha\beta} c_{i\tau\beta})
\end{equation}$$

We will call the Hubbard-Stratonovich field \\(\mathbf{m}\\) to signify an (internal) magnetic field. If we then have 

$$\int e^{-a\|\mathbf{m}\|^2 - b\mathbf{m}\cdot \mathbf{S}}\d\mathbf{m} \propto e^{b^2\|\mathbf{S}\|^2/4a} = e^{-U\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}}$$

One can verify that 

$$\begin{align}
(S^x_{i\tau})^2 ={}& (\bar{c}_{i\tau\uparrow}c_{i\tau\downarrow} + \bar{c}_{i\tau\downarrow}c_{i\tau\uparrow})^2 \\
={}& 2\bar{c}_{i\tau\uparrow}c_{i\tau\downarrow}\bar{c}_{i\tau\downarrow}c_{i\tau\uparrow} \\
={}& -2\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}
\end{align}$$

$$\begin{align}
(S^y_{i\tau})^2 ={}& (-i\bar{c}_{i\tau\uparrow}c_{i\tau\downarrow} + i\bar{c}_{i\tau\downarrow}c_{i\tau\uparrow})^2 \\
={}& 2\bar{c}_{i\tau\uparrow}c_{i\tau\downarrow}\bar{c}_{i\tau\downarrow}c_{i\tau\uparrow} \\
={}& -2\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}
\end{align}$$

$$\begin{align}
(S^z_{i\tau})^2 ={}& (\bar{c}_{i\tau\uparrow}c_{i\tau\uparrow} - \bar{c}_{i\tau\downarrow}c_{i\tau\downarrow})^2 \\
={}& -2\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}
\end{align}$$

which tells us that 

$$\begin{equation}
\|\mathbf{S}_{i\tau}\|^2 = (S_{i\tau}^x)^2 + (S_{i\tau}^y)^2 + (S_{i\tau}^z)^2 = -6\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}.
\end{equation}$$

Thus, setting 

$$\begin{align}
-U\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow} ={}& \frac{b^2\|\mathbf{S}\|^2}{4a} \\
={}& \frac{-6b^2\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow}}{4a}
\end{align}$$

which means that \\(U = 3b^2/2a\\). We let \\(b=1\\) and \\(a = 3/2U\\). Thus, the interaction term of the effective action becomes 

$$S_{\text{int}} = \int_0^\beta \sum_i\left[\frac{3}{2U}\|\mathbf{m}_{i\tau}\|^2 + \sum_{\alpha\beta}\mathbf{m}_{i\tau} \cdot \bar{c}_{i\tau\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{i\tau\beta}\right]\d\tau$$

and we need to remember to integrate over \\(\mathbf{h}\\). Next, we will Fourier transform all of the fields in spacetime. We will apply the Fourier conventions 

$$\begin{equation}
c_{i\tau\sigma} = \frac{1}{\sqrt{N\beta}}\sum_k e^{-ik_0\tau + i\mathbf{R}_i\cdot\k} c_{k\sigma},\quad \bar{c}_{i\tau\sigma} = \frac{1}{\sqrt{N\beta}}\sum_k e^{ik_0\tau - i\mathbf{R}_i\cdot\k} \bar{c}_{k\sigma}, \quad \mathbf{m}_{i\tau} = \frac{1}{\beta N}\sum_k e^{-ik_0\tau + i\mathbf{R}_i\cdot\k}\mathbf{m}_k 
\end{equation}$$

which allows us to rewrite the two terms of the action as 

$$S_0 = \sum_{k\sigma}\bar{c}_{k\sigma}(-ik_0+\xi_{\k})c_{k\sigma},\quad S_{\text{int}} = \frac{3}{2U\beta N}\sum_k <b>m</b>_k \cdot<b>m</b>_{-k} + \frac{1}{\beta N}\sum_{kp\alpha\beta} <b>m</b>_k\cdot \bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}.$$

If we plug these expressions back in to the path integral representation of the partition function, we find that 

$$\begin{equation}
Z = \int e^{-S_0}\exp\left(-\frac{3}{2U\beta N}\sum_k<b>m</b>_k\cdot<b>m</b>_{-k}\right)\exp\left(-\frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>_{k}\cdot\bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}\right)\D\bar{c}\D c\D<b>m</b>
\end{equation}$$

We now regroup terms in this action to find that 

$$\begin{equation}
Z = \int \exp\left(-\frac{3}{2U\beta N}\sum_k<b>m</b>_k\cdot<b>m</b>_{-k}\right)\left[\int e^{-S_0}\exp\left(-\frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>\cdot\bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}\right)\D\bar{c}\D c \right]\D<b>m</b>
\end{equation}$$

and then rewrite the bracketed term as 

$$\begin{equation}
Z = \int \exp\left(-\frac{3}{2U\beta N}\sum_k<b>m</b>_k\cdot<b>m</b>_{-k}\right)Z_0 \left\langle \exp\left(-\frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>_k\cdot\bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}\right)\right\rangle_0 \D<b>m</b>
\end{equation}$$

and we now want to write 

$$\begin{equation}
Z = Z_0 \int e^{-S_{\text{eff}}[<b>m</b>]}\D<b>m</b>.
\end{equation}$$

where the effective action is given by 

$$\begin{equation}
S_{\text{eff}}[\mathbf{m}] = \frac{3}{2U\beta N}\sum_k<b>m</b>_k \cdot<b>m</b>_{-k} - \log\left\langle\exp\left(-\frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>_k\cdot\bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}\right)\right\rangle_0
\end{equation}$$

We will evaluate \\(S_{\text{eff}}\\) perturbatively in powers of \\(<b>m</b>\\). To do this, we apply the cumulant expansion. We define 

$$\begin{equation}
\Delta S_{\text{eff}} = -\log\left\langle\exp\left(-\frac{1}{\beta N}\sum_{k,p}<b>m</b>_k\cdot\bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta} c_{p\beta}\right)\right\rangle_0
\end{equation}$$

and the resulting cumulant expansion gives terms at each power of \\(<b>m</b>\\). The first order term is given by

$$\begin{align}
\Delta S_{\text{eff}}^{(1)} ={}& \frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>_k \cdot \langle\bar{c}_{k+p,\alpha} \boldsymbol{\sigma}_{\alpha\beta} c_{p\beta}\rangle_0 
\end{align}$$

Since we have that \\(\langle \bar{c}_{k+p,\alpha} c_{p\beta}\rangle_0 \propto \delta_{\alpha\beta}\\), the sums over \\(\alpha,\beta\\) will give zero because the Pauli matrices are traceless. Thus \\(\Delta S^{(1)}_{\text{eff}} = 0\\). The second order contribution is then given by 

$$\begin{align}
\Delta S_{\text{eff}}^{(2)} ={}& -\frac{1}{2}\left[\left\langle\left(-\frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>_k\cdot\bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}\right)^2\right\rangle_0 - \left\langle-\frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>_k\cdot\bar{c}_{k+p,\alpha}\sigma_{\alpha\beta}c_{p\beta}\right\rangle_0^2\right]
\end{align}$$

We note that the second term is simply 0, because it is just the first order contribution to the effective action (which was 0). Thus we will focus on the first of the two terms. We will evaluate it in detail. 

$$\begin{align}
\Delta S_{\text{eff}}^{(2)} ={}& -\frac{1}{2}\left\langle\left(-\frac{1}{\beta N}\sum_{kp\alpha\beta}<b>m</b>_k\cdot\bar{c}_{k+p,\alpha}\boldsymbol{\sigma}_{\alpha\beta}c_{p\beta}\right)^2\right\rangle_0 \\
={}& -\frac{1}{2(\beta N)^2}\left\langle\left(\sum_{k,p}m^\ell_k \bar{c}_{k+p,\alpha}\sigma^\ell_{\alpha\beta}c_{p\beta}\right)^2\right\rangle_0 \\
={}& -\frac{1}{2(\beta N)^2}\sum_{\substack{kp\alpha\beta \\ k'p'\alpha'\beta'}} m^\ell_k m^{\ell'}_{k'}\sigma^\ell_{\alpha\beta} \sigma^{\ell'}_{\alpha'\beta'}\langle\bar{c}_{k+p,\alpha}c_{p\beta}\bar{c}_{k'+p',\alpha'}c_{p'\beta'}\rangle_0
\end{align}$$

We now evaluate the four-point correlation function by using Wick's theorem. It gives us 

$$\begin{align}
\langle\bar{c}_{k+p,\alpha}c_{p\beta}\bar{c}_{k'+p',\alpha'}c_{p'\beta'}\rangle_0 ={}& \langle\wick{\c1{\bar{c}}_{k+p,\alpha}\c1{c}_{p\beta}\c1{\bar{c}}_{k'+p',\alpha'}\c1{c}_{p'\beta'}} \rangle_0 + \langle\wick{\c2{\bar{c}}_{k+p,\alpha}\c1{c}_{p\beta}\c1{\bar{c}}_{k'+p',\alpha'}\c2{c}_{p'\beta'}}\rangle_0 \\
={}& \langle\bar{c}_{k+p,\alpha}c_{p\beta}\rangle_0\langle\bar{c}_{k'+p',\alpha'}c_{p'\beta'}\rangle_0 + \langle\bar{c}_{k+p,\alpha}c_{p'\beta'}\rangle_0\langle c_{p,\beta}\bar{c}_{k'+p',\alpha'}\rangle_0 \\
={}& \mathcal{G}_0(p)\delta_{k,0}\delta_{\alpha\beta}\mathcal{G}_0(p')\delta_{k',0}\delta_{\alpha'\beta'} - \mathcal{G}_0(p')\delta_{k+p,p'}\delta_{\alpha\beta'} \mathcal{G}_0(p)\delta_{p,k'+p'}\delta_{\alpha'\beta}
\end{align}$$

Plugging this in to our expression for \\(\Delta S^{(2)}_{\text{eff}}\\), we find that 

$$\begin{align}
\Delta S_{\text{eff}}^{(2)} ={}& -\frac{1}{2(\beta N)^2}\sum_{k,p,k',p'} h^\ell_k h^{\ell'}_{k'}\sigma^\ell_{\alpha\beta} \sigma^{\ell'}_{\alpha'\beta'}\left( \mathcal{G}_0(p)\delta_{k,0}\delta_{\alpha\beta}\mathcal{G}_0(p')\delta_{k',0}\delta_{\alpha'\beta'} - \mathcal{G}_0(p')\delta_{k+p,p'}\delta_{\alpha\beta'} \mathcal{G}_0(p)\delta_{p,k'+p'}\delta_{\alpha'\beta}\right) \\
={}& -\frac{1}{2(\beta N)^2}\sum_{k,p,k',p'} h^\ell_k h^{\ell'}_{k'}\left( \mathcal{G}_0(p)\delta_{k,0}\mathcal{G}_0(p')\delta_{k',0}\sigma^\ell_{\alpha\alpha}\sigma^{\ell'}_{\alpha'\alpha'} - \mathcal{G}_0(p')\delta_{k+p,p'} \mathcal{G}_0(p)\delta_{p,k'+p'} \sigma^\ell_{\beta'\beta}\sigma^{\ell}_{\beta\beta'} \right)
\end{align}$$

We can write the remaining sums over Pauli matrices indices as traces: 

$$\begin{align}
\sigma^\ell_{\alpha\alpha} = \tr(\sigma^\ell) = 0\\
\sigma^\ell_{\alpha'\alpha'} = \tr(\sigma^{\ell'}) = 0\\
\sigma^\ell_{\beta'\beta}\sigma^{\ell'}_{\beta\beta'} = \tr(\sigma^\ell\sigma^{\ell'}) = 2\delta_{\ell\ell'}
\end{align}$$

This gives us 

$$\begin{align}
\Delta S_{\text{eff}}^{(2)} ={}& -\frac{1}{2(\beta N)^2}\sum_{k,p,k',p'} h^\ell_k h^{\ell'}_{k'}\left( - \mathcal{G}_0(p')\delta_{k+p,p'} \mathcal{G}_0(p)\delta_{p,k'+p'} 2\delta_{\ell\ell'} \right) \\
={}& \frac{1}{(\beta N)^2}\sum_{k,p,k',p'} h^\ell_k h^\ell_{k'}\mathcal{G}_0(p')\delta_{k+p,p'} \mathcal{G}_0(p)\delta_{p,k'+p'} \\
={}& \frac{1}{(\beta N)^2}\sum_{k,p,k'} h^\ell_k h^\ell_{k'}\mathcal{G}_0(k+p)\mathcal{G}_0(p)\delta_{p,k'+k+p}
\end{align}$$

Since \\(\delta_{p,k'+k+p} = \delta_{k+k',0} = \delta_{k',-k}\\), we can evaluate another sum:

$$\begin{align}
\Delta S_{\text{eff}}^{(2)} ={}& \frac{1}{(\beta N)^2}\sum_{k,p,k'} h^\ell_k h^\ell_{k'}\mathcal{G}_0(k+p)\mathcal{G}_0(p)\delta_{k',-k} \\
={}& \frac{1}{(\beta N)^2}\sum_{k,p} h^\ell_k h^\ell_{-k}\mathcal{G}_0(k+p)\mathcal{G}_0(p)\\
={}& \frac{1}{\beta N}\sum_k<b>h</b>_k\cdot<b>h</b>_{-k}\left(\frac{1}{\beta N}\sum_p \mathcal{G}_0(k+p)\mathcal{G}_0(p) \right) \\
={}& \frac{1}{\beta N}\sum_k<b>h</b>_k\cdot<b>h</b>_{-k}\left(\frac{1}{N}\sum_{\p} \frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}}\right) 
\end{align}$$

Now, we finally write down the whole effective action to \\(O(h^2)\\). We find that 

$$\begin{align}
S_{\text{eff}} ={}& \frac{3}{2U\beta N} \sum_k<b>h</b>_k\cdot<b>h</b>_{-k} + \Delta S^{(2)}_{\text{eff}} \\
={}& \frac{3}{2U\beta N} \sum_k<b>h</b>_k\cdot<b>h</b>_{-k} + \frac{1}{\beta N}\sum_k<b>h</b>_k\cdot<b>h</b>_{-k}\left(\frac{1}{N}\sum_{\p} \frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}}\right) \\
={}& \frac{1}{2\beta N}\sum_k<b>h</b>_k\cdot<b>h</b>_{-k}\left[\frac{3}{U} + \frac{2}{N}\sum_{\p}\frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}}\right]
\end{align}$$

This result for the effective action describes an effective Gaussian theory for \\(<b>h</b>\\). The theory converges if the factor is positive, whereas it diverges if the factor is negative. Thus, when the factor is zero, this signifies an instability in the theory. This will allow us to find, as a function of frequency \\(k_0\\) and wave vector \\(\k\\), the transition temperature for such an ordering by solving the equation 

$$\frac{3}{U} + \frac{2}{N}\sum_{\p}\frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}} = 0.$$

We note that temperature enters in through the Fermi-Dirac distribution.

