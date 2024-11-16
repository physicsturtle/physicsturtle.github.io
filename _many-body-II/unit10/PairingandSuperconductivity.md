---
layout: lesson
title: Pairing and Superconductivity 
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
In this section, we will perform another kind of Hubbard-Stratonovich calculation which allows us to investigate the propensity of a model of interacting electrons, interacting via an attractive interaction (as opposed to a repulsive interaction, as usual) to form a superconducting state. How electrons can attract each other is, at this point, abstracted away. The various microscopic mechanisms which can lead to attraction could be due to phonons, electron-electron overscreening, antiferromagnetism, or more. These will not be discussed in this section. 

The Hamiltonian for the attractive Hubbard model is given by 

$$\begin{equation}
\Hhat = -t\sum_{\langle i,j\rangle,\sigma}(\chat^\dagger_{i\sigma}\chat_{j\sigma} + \hc) - U\sum_i \chat^\dagger_{i\uparrow} \chat^\dagger_{i\downarrow} \chat_{i\downarrow} \chat_{i\uparrow} - \mu\sum_{i\sigma} \chat^\dagger_{i\sigma}\chat_{i\sigma}
\end{equation}$$

which leads to the effective action

$$\begin{equation}
S = \int_0^\beta \left[\sum_{i\sigma}\bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} - t\sum_{\langle i,j\rangle,\sigma}(\bar{c}_{i\tau\sigma} c_{j\tau\sigma} + \bar{c}_{j\tau\sigma} c_{i\tau\sigma}) - U\sum_i \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow} c_{i\tau\downarrow} c_{i\tau\uparrow} - \mu\sum_{i\sigma} \bar{c}_{i\tau\sigma} c_{i\tau\sigma}\right]\d\tau
\end{equation}$$

We split the action into two parts: a noninteracting part \\(S\_0\\) and an interacting part \\(S\_{\text{int}}\\):

$$\begin{align}
S_0 ={}& \int_0^\beta\left[ \sum_{i,\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} -t\sum_{\langle i,j\rangle,\sigma}(\bar{c}_{i\tau\sigma}c_{j\tau\sigma} + \bar{c}_{j\tau\sigma}c_{i\tau\sigma}) - \mu\sum_{i\sigma}\bar{c}_{i\tau\sigma}c_{i\tau\sigma}\right] \d\tau \\
S_{\text{int}} ={}& -\int_0^\beta U\sum_i \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow}c_{i\tau\downarrow}c_{i\tau\uparrow} \d\tau.
\end{align}$$

We will decompose the interacting part via a Hubbard-Stratonovich transformation. It is simply verified that 

$$\begin{equation}
\int \exp\left(-\frac{1}{U}\Delta^{*}\Delta - \Delta \bar{c}_{i\uparrow}\bar{c}_{i\downarrow} - \Delta^{*} c_{i\downarrow} c_{i\uparrow}\right)\d\Delta^{*}\d\Delta = e^{U\bar{c}_{i\uparrow}\bar{c}_{i\downarrow}c_{i\downarrow}c_{i\uparrow}}
\end{equation}$$

so then we write 

$$\begin{equation}
\exp\left(\int_0^\beta U\sum_i \bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow} c_{i\tau\downarrow} c_{i\tau\uparrow} \d\tau\right) = \exp\left(-\int_0^\beta \sum_i\left[ \frac{1}{U}|\Delta_{i\tau}|^2 + \Delta_{i\tau} \bar{c}_{i\tau\uparrow} \bar{c}_{i\tau\downarrow} + \Delta_{i\tau}^{*} c_{i\tau\downarrow} c_{i\tau\uparrow}\right]\d\tau \right)
\end{equation}$$

Then, we write the partition function as 

$$\begin{equation}
Z = \int e^{-S_0} \exp\left(-\int_0^\beta \sum_i\left[ \frac{1}{U}|\Delta_{i\tau}|^2 + \Delta_{i\tau} \bar{c}_{i\tau\uparrow} \bar{c}_{i\tau\downarrow} + \Delta_{i\tau}^{*} c_{i\tau\downarrow} c_{i\tau\uparrow}\right]\d\tau \right)\D\bar{c}\D c\D\Delta^{*}\D\Delta
\end{equation}$$

we rewrite the action as 

$$\begin{equation}
Z = \int \exp\left(-\int_0^\beta\sum_i \frac{1}{U}|\Delta_{i\tau}|^2\d\tau\right) \left(\int e^{-S_0}\exp\left(-\int_0^\beta \sum_i \left[\Delta_{i\tau}\bar{c}_{i\tau\uparrow} \bar{c}_{i\tau\downarrow} + \Delta^{*}_{i\tau} c_{i\tau\downarrow} c_{i\tau\uparrow}\right] \d\tau\right) \D\bar{c}\D c\right)\D\Delta^{*}\D\Delta
\end{equation}$$

and then rewrite the bracketed quantity in terms of an expectation value:

$$\begin{equation}
Z = \int \exp\left(-\int_0^\beta\sum_i \frac{1}{U}|\Delta_{i\tau}|^2\d\tau\right) Z_0\langle\exp\left(-\int_0^\beta \sum_i \left[\Delta_{i\tau}\bar{c}_{i\tau\uparrow} \bar{c}_{i\tau\downarrow} + \Delta^{*}_{i\tau} c_{i\tau\downarrow} c_{i\tau\uparrow}\right] \d\tau\right) \rangle_0\D\Delta^{*}\D\Delta
\end{equation}$$

We see now that everything is written in terms of a path integral involving \\(\Delta^{*}\\) and \\(\Delta\\) fields. We define the effective action to be 

$$\begin{equation}
S_{\text{eff}}[\Delta^{*},\Delta] = \int_0^\beta \sum_i \frac{1}{U}|\Delta_{i\tau}|^2\d\tau - \log\langle\exp\left(-\int_0^\beta\sum_i \left(\Delta_{i\tau}\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow} + \Delta^{*}_{i\tau} c_{i\tau\downarrow} c_{i\tau\uparrow}\right)\d\tau\right)\rangle_0
\end{equation}$$

We will now calculate the effective action perturbatively. We start by Fourier transforming the action according to the following Fourier transform conventions: 

$$\begin{equation}
c_{i\tau\sigma} = \frac{1}{\sqrt{N_s\beta}} \sum_k e^{-ik_0\tau + i\mathbf{R}_i\cdot\k}c_{k\sigma}, \quad \bar{c}_{i\tau\sigma} = \frac{1}{\sqrt{N_s\beta}}\sum_k e^{ik_0-i\mathbf{R}_i\cdot\k}\bar{c}_{k\sigma},\quad \Delta_{i\tau} = \frac{1}{\beta N_s}\sum_k e^{-ik_0\tau + i\mathbf{R}_i\cdot\k}\Delta_k
\end{equation}$$

Then, we Fourier transform parts of this to find 

$$\begin{align}
\int_0^\beta \sum_i |\Delta_{i\tau}|^2 \d\tau ={}& \int_0^\beta \sum_i \Delta^{*}_{i\tau} \Delta_{i\tau} \d\tau \\
={}& \int_0^\beta\sum_i \frac{1}{(\beta N_s)^2}\sum_{k,k'} e^{ik_0\tau - i\mathbf{R}_i\cdot\k} e^{-ik_0' + i\mathbf{R}_i\cdot\k'} \Delta^{*}_{k}\Delta_{k'} \d\tau \\
={}& \frac{1}{\beta N_s}\sum_{k,k'} \Delta^{*}_{k}\Delta_{k'}\delta_{k,k'} \\
={}& \frac{1}{\beta N_s}\sum_{k} \Delta^{*}_{k}\Delta_{k} \\
\end{align}$$

The other part is given by 

$$\begin{align}
S' ={}& \int_0^\beta\sum_i\left(\Delta_{i\tau}\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow} + \Delta^{*}_{i\tau} c_{i\tau\downarrow} c_{i\tau\uparrow}\right) \d\tau \\
={}& \int_0^\beta\sum_i\left[\frac{1}{(\beta N_s)^2}\sum_{k,p,q} e^{-ik_0\tau + i\mathbf{R}_i\cdot\k} e^{ip_0\tau - i\mathbf{R}_i\cdot\p} e^{iq_0\tau - i\mathbf{R}_i\cdot\q} \Delta_k \bar{c}_{p\uparrow} \bar{c}_{q\downarrow} \right. \\
&+ \left. \frac{1}{(\beta N_s)^2}\sum_{k,p,q} e^{ik_0\tau - i\mathbf{R}_i\cdot\k} e^{-ip_0\tau + i\mathbf{R}_i\cdot\p} e^{-iq_0\tau + i\mathbf{R}_i\cdot\q}\Delta^{*}_k c_{p\downarrow} c_{q\uparrow}\right] \d\tau \\
={}& \frac{1}{\beta N_s} \left[\sum_{k,p,q} \delta_{p+q,k} \Delta_k \bar{c}_{p\uparrow} \bar{c}_{q\downarrow} +\sum_{k,p,q} \delta_{p+q,k} \Delta^{*}_k c_{p\downarrow} c_{q\uparrow}\right] \\
={}& \frac{1}{\beta N_s}\sum_{k,p} \left( \Delta_k \bar{c}_{k-p,\uparrow} \bar{c}_{p\downarrow} + \Delta^{*}_k c_{k-p,\downarrow} c_{p\uparrow}\right)
\end{align}$$

Then, we can start evaluating the effective action. We get

$$\begin{equation}
\Delta S_{\text{eff}} = -\log\langle\exp\left(-\frac{1}{\beta N_s}\sum_{k,p}\left(\Delta_k \bar{c}_{k-p,\uparrow} \bar{c}_{p\downarrow} + \Delta^{*}_k c_{k-p,\downarrow} c_{p\uparrow}\right)\right)\rangle_0
\end{equation}$$

It is clear that \\(\Delta S^{(1)}\_{\text{eff}} = 0\\). We now evaluate the second order correction: 

$$\begin{align}
\Delta S^{(2)}_{\text{eff}} = -\frac{1}{2}\left[\langle\frac{1}{(\beta N_s)^2}\sum_{k,p,k',p'}\left(\Delta_k \bar{c}_{k-p,\uparrow} \bar{c}_{p\downarrow} + \Delta^{*}_k c_{k-p,\downarrow} c_{p\uparrow}\right) \left(\Delta_{k'} \bar{c}_{k'-p',\uparrow} \bar{c}_{p'\downarrow} + \Delta^{*}_{k'} c_{k'-p',\downarrow} c_{p'\uparrow}\right) \rangle_0\right]
\end{align}$$

Note that there is technically another term in \\(\Delta S^{(2)}\_{\text{eff}}\\), because 

$$\begin{equation}
\Delta S^{(2)}_{\text{eff}} = -\frac{1}{2}\left[ \langle(S')^2\rangle_0 - \langle S'\rangle_0^2\right]
\end{equation}$$

but \\(\langle S'\rangle = 0\\). Now continuing with the evaluation of \\(\Delta S^{(2)}\_{\text{eff}}\\), 

$$\begin{align}
\Delta S^{(2)}_{\text{eff}} ={}& -\frac{1}{2(\beta N_s)^2}\sum_{k,p,k',p'}\langle \Delta_k \Delta^{*}_{k'} \bar{c}_{k-p,\uparrow}\bar{c}_{p\downarrow} c_{k'-p',\downarrow} c_{p'\uparrow} + \Delta^{*}_k \Delta_{k'} c_{k-p,\downarrow} c_{p\uparrow} \bar{c}_{k'-p',\uparrow}\bar{c}_{p'\downarrow}\rangle_0 \\
={}& -\frac{1}{2(\beta N_s)^2}\sum_{kpk'p'}\left(\Delta_k \Delta^{*}_{k'} \langle\bar{c}_{k-p,\uparrow}\bar{c}_{p\downarrow} c_{k'-p',\downarrow} c_{p'\uparrow}\rangle_0 + \Delta^{*}_k \Delta_{k'}\langle\bar{c}_{k'-p',\uparrow}\bar{c}_{p'\downarrow}c_{k-p,\downarrow}c_{p\uparrow}\rangle_0\right)
\end{align}$$

Now, we can evaluate the 4-point correlation functions. We note that the only nonzero contractions must have the same spin on both fermion operators. Thus, the 4-point functions evaluate to only a one term which is a product of 2-fermion correlation functions. 

$$\begin{align}
\langle\bar{c}_{k-p,\uparrow}\bar{c}_{p\downarrow} c_{k'-p',\downarrow} c_{p'\uparrow}\rangle_0 ={}& \langle\wick{\c2{\bar{c}}_{k-p,\uparrow}\c1{\bar{c}}_{p\downarrow} \c1{c}_{k'-p',\downarrow} \c2{c}_{p'\uparrow}}\rangle_0 = \langle\bar{c}_{k-p,\uparrow} c_{p'\uparrow}\rangle_0\langle\bar{c}_{p\downarrow} c_{k'-p',\downarrow}\rangle_0 \\
\langle\bar{c}_{k'-p',\uparrow}\bar{c}_{p'\downarrow}c_{k-p,\downarrow}c_{p\uparrow}\rangle_0 ={}& \langle\wick{\c2{\bar{c}}_{k'-p',\uparrow}\c1{\bar{c}}_{p'\downarrow}\c1{c}_{k-p,\downarrow}\c2{c}_{p\uparrow}}\rangle_0 = \langle\bar{c}_{k'-p',\uparrow}c_{p\uparrow}\rangle_0\langle\bar{c}_{p'\downarrow}c_{k-p,\downarrow}\rangle_0
\end{align}$$

Thus, 

$$\begin{align}
\Delta S^{(2)}_{\text{eff}} ={}& -\frac{1}{2(\beta N_s)^2}\sum_{kpk'p'}\left(\Delta_k \Delta^{*}_{k'} \langle\bar{c}_{k-p,\uparrow} c_{p'\uparrow}\rangle_0\langle\bar{c}_{p\downarrow} c_{k'-p',\downarrow}\rangle_0 + \Delta^{*}_k \Delta_{k'}\langle\bar{c}_{k'-p',\uparrow}c_{p\uparrow}\rangle_0\langle\bar{c}_{p'\downarrow}c_{k-p,\downarrow}\rangle_0\right) \\
={}& -\frac{1}{2(\beta N_s)^2}\sum_{kpk'p'}\left(\Delta_k \Delta^{*}_{k'} \mathcal{G}_0(p')\delta_{k-p,p'}\mathcal{G}_0(p)\delta_{p,k'-p'} + \Delta^{*}_k \Delta_{k'}\mathcal{G}_0(p)\delta_{k'-p',p}\mathcal{G}_0(p')\delta_{p',k-p}\right) \\
={}& -\frac{1}{2(\beta N_s)^2}\sum_{kpk'}\left(\Delta_k \Delta^{*}_{k'} \mathcal{G}_0(k-p) \mathcal{G}_0(p)\delta_{p,k'-k+p} + \Delta^{*}_k \Delta_{k'}\mathcal{G}_0(p)\delta_{k'-k+p,p}\mathcal{G}_0(k-p)\right) \\
={}& -\frac{1}{2(\beta N_s)^2}\sum_{kpk'}\left(\Delta_k \Delta^{*}_{k'} \mathcal{G}_0(k-p) \mathcal{G}_0(p)\delta_{k',k} + \Delta^{*}_k \Delta_{k'}\mathcal{G}_0(p)\delta_{k',k}\mathcal{G}_0(k-p)\right) \\
={}& -\frac{1}{2(\beta N_s)^2}\sum_{kp}\left(\Delta_k \Delta^{*}_{k} \mathcal{G}_0(k-p) \mathcal{G}_0(p) + \Delta^{*}_k \Delta_{k}\mathcal{G}_0(p) \mathcal{G}_0(k-p)\right) \\
={}& -\frac{1}{(\beta N_s)^2}\sum_{kp}\Delta_k \Delta^{*}_{k} \mathcal{G}_0(k-p) \mathcal{G}_0(p) \\
={}& -\frac{1}{\beta N_s}\sum_k |\Delta_k|^2 \left(\frac{1}{\beta N}\sum_p \mathcal{G}_0(k-p)\mathcal{G}_0(p)\right)
\end{align}$$

Then, the effective action, written to second order in \\(\Delta\\), is then given by 

$$\begin{equation}
\Delta S_{\text{eff}} = \frac{1}{\beta N_s}\sum_k |\Delta_k|^2\left(\frac{1}{U} - \pi(\k,ik_0)\right)
\end{equation}$$

where the pair bubble \\(\pi\\) is given by 

$$\begin{equation}
\pi(\k,ik_0) = \frac{1}{\beta N_s}\sum_p \mathcal{G}_0(k-p)\mathcal{G}_0(p).
\end{equation}$$

The point at which the theory encounters an instability is when the coefficient of \\(\|\Delta\_k\|^2\\) changes sign. It needs to be positive for the theory to converge. We therefore set the coefficient to be zero. The pair bubble can be evaluated analytically for the choice of \\(\k=0\\) and \\(k\_0 = 0\\), assuming a cutoff \\(D\\) for the conduction electrons. The details of the evaluation are outlined in an exercise. 

$$\begin{equation}
\pi(0,0) = \tilde{\rho}\log\left(\frac{2\beta D}{\pi}e^\gamma\right)
\end{equation}$$

where \\(\tilde{\rho}\\) is the density of states per site, and \\(\gamma\\) is the Euler-Mascheroni constant. Now, we can solve for the transition temperature by setting \\(\pi(0,0) = 1/U\\). This gives us an approximate form for the critical temperature: 

$$\begin{equation}
T_c\sim \frac{2D e^{\gamma}}{\pi k_B} e^{-1/\tilde{\rho} U}
\end{equation}$$


