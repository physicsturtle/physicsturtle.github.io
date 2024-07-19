---
layout: lesson
title: Spin Density Wave Order 
dept: physics
course: qpt
unit: unit11
deptDisplay: Physics
courseDisplay: Quantum Phase Transitions
unitDisplay: Unit 11
---
In this section, we consider a more realistic Hubbard-Stratonovich decoupling, where we look for spin density wave order. Instead of considering only the \\(z\\) component of an internal magnetic field, we consider all three \\(x,y,z\\) components. This preserves the original spin-rotation invariance in the original Hubbard model, which we recall is given by the action

$$\begin{equation}
S = \int_0^\beta\left[ \sum_{i\sigma}\bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} + \sum_{\k\sigma} \bar{c}_{\k\tau\sigma}\xi_{\k} c_{\k\tau\sigma} + \sum_i \bar{c}_{i\tau\uparrow} \bar{c}_{i\tau\downarrow} c_{i\tau\downarrow} c_{i\tau\uparrow} \right]\d\tau
\end{equation}$$

We introduce a Hubbard-Stratonovich decoupling, which gives us the following partition function. 

$$\begin{equation}
Z = \int\exp\left\{-\int_0^\beta \left[\sum_{i\sigma} \bar{c}_{i\tau\sigma} \partial_\tau c_{i\tau\sigma} + \sum_{\k\sigma} \bar{c}_{\k\tau\sigma} \xi_{\k} c_{\k\tau\sigma} + \frac{3}{2U}\sum_i |\mathbf{m}_{i\tau}|^2 + \sum_{i\alpha\beta} \mathbf{m}_{i\tau}\cdot\bar{c}_{i\tau\alpha}\boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta}\right] \d\tau\right\} \D\bar{c}\D c \D\mathbf{m}
\end{equation}$$

As in the previous section, we rewrite this partition function as 

$$\begin{equation}
Z = Z_0\int\exp\left\{- \frac{3}{2U}\int_0^\beta\sum_i |\mathbf{m}_{i\tau}|^2\d\tau\right\} \left<\exp\left(-\int_0^\beta \sum_{i\alpha\beta} \mathbf{m}_{i\tau}\cdot\bar{c}_{i\tau\alpha}\boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta}\d\tau\right)\right>_0 \D\mathbf{m}
\end{equation}$$

which allows us to define the effective action, which takes into account the simple quadratic term, as well as the logarithm:

$$\begin{equation}
S_\text{eff}[\mathbf{m}] = \frac{3}{2U}\int_0^\beta\sum_i |\mathbf{m}_{i\tau}|^2\d\tau - \log \left<\exp\left(-\int_0^\beta \sum_{i\alpha\beta} \mathbf{m}_{i\tau}\cdot\bar{c}_{i\tau\alpha}\boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta}\d\tau\right)\right>_0
\end{equation}$$

The second term with the logarithm is the modification to the effective action due to the interaction of \\(\mathbf{m}\\) with the fermions:

$$\begin{equation}
\Delta S_\text{eff}[\mathbf{m}] = - \log \left<\exp\left(-\int_0^\beta \sum_{i\alpha\beta} \mathbf{m}_{i\tau}\cdot\bar{c}_{i\tau\alpha}\boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta}\d\tau\right)\right>_0.
\end{equation}$$

The first thing to note is that this quantity cannot be evaluated exactly, and we will need to do a perturbation expansion in powers of \\(\mathbf{m}\\). We can either use a cumulant expansion at this stage, or evaluate the expectation value exactly in terms of a determinant, and then expand that determinant in a power series. We will follow the treatment of Hertz and evaluate the path integral exactly with the determinant. This gives us that 

$$\begin{align}
\Delta S_\text{eff}[\mathbf{m}] ={}& - \log \left\{\frac{1}{Z_0} \int e^{-S_0} \exp\left(-\int_0^\beta \sum_{i\alpha\beta} \mathbf{m}_{i\tau}\cdot\bar{c}_{i\tau\alpha}\boldsymbol{\sigma}_{\alpha\beta} c_{i\tau\beta}\d\tau\right)\D\bar{c}\D c \right\} \\
={}& -\log\left\{\frac{1}{Z_0}\int\exp\left(-\left[ \sum_{k\sigma} \bar{c}_{k\sigma} (-ik_0 + \xi_{\k}) c_{k\sigma} + \frac{1}{\beta N_s}\sum_{kq\alpha\beta} \bar{c}_{k\alpha} \mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta} c_{q\beta}\right]\right) \D\bar{c} \D c\right\} \\
={}& -\log\left\{\frac{1}{Z_0}\int\exp\left(\sum_{kq\alpha\beta} \bar{c}_{k\sigma}\left[  (ik_0 - \xi_{\k})\delta_{\alpha\beta}\delta_{kq} - \frac{1}{\beta N_s}\mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta} \right]c_{q\beta}\right) \D\bar{c} \D c\right\} \\
={}& -\log\left\{\frac{1}{Z_0}\int\exp\left(\sum_{kq\alpha\beta} \bar{c}_{k\sigma}\left[  \mathcal{G}_0^{-1}(k)\delta_{kq}\delta_{\alpha\beta} - \frac{1}{\beta N_s}\mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta} \right]c_{q\beta}\right) \D\bar{c} \D c\right\} \\
={}& -\log\left\{\frac{1}{Z_0}\det \left[  \mathcal{G}_0^{-1}(k)\delta_{kq}\delta_{\alpha\beta} - \frac{1}{\beta N_s}\mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta} \right]\right\} \\
={}& -\log\left\{\frac{1}{Z_0}\det(\mathcal{G}^{-1}_0(k)\delta_{kq}\delta_{\alpha\beta}) \det \left[  \delta_{kq}\delta_{\alpha\beta} - \frac{1}{\beta N_s}\mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta}\mathcal{G}_0(k) \right]\right\} \\
={}& -\log \det \left[  \delta_{kq}\delta_{\alpha\beta} - \frac{1}{\beta N_s}\mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta}\mathcal{G}_0(k) \right] 
\end{align}$$

where the free Green function is given by 

$$\begin{equation}
\mathcal{G}_0(k) = \frac{1}{ik_0 - \xi_{\k}}
\end{equation}$$

and we note that \\(Z_0 = \det(\mathcal{G}^{-1}_{0}(k,q) \delta_{\alpha\beta})\\), which is how we cancelled it out. Now, we use the identity \\(\log(\det( A)) = \tr( \log (A))\\), so that 

$$\begin{align}
\Delta S_\text{eff}[\mathbf{m}] ={}& -\tr\log \left[  \delta_{kq}\delta_{\alpha\beta} - \frac{1}{\beta N_s}\mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta}\mathcal{G}_0(k,q) \right] 
\end{align}$$

Now, we apply the Taylor expansion of the logarithm:

$$\begin{equation}
-\log(\1 - X) = \sum_{n=0}^\infty \frac{X^n}{n}, \qquad X_{kq\alpha\beta} = \frac{1}{\beta N_s}\mathbf{m}_{k-q}\cdot\boldsymbol{\sigma}_{\alpha\beta}\mathcal{G}_0(k).
\end{equation}$$

The trace yields zero for the first power of \\(X\\) because the Pauli matrices are traceless. The second order contribution yields 

$$\begin{align}
\tr X^2 ={}& \frac{1}{(\beta N_s)^2} \sum_{k_1k_2q_1q_2}\sum_{\ell_1\ell_2\alpha_1\alpha_2\beta_1\beta_2} \delta_{k_1q_2}\delta_{\alpha_1\beta_2}  m^{\ell_1}_{k_1-q_1} \sigma^{\ell_1}_{\alpha_1\beta_1}\mathcal{G}_0(k_1) \delta_{q_1k_2}\delta_{\beta_1\alpha_2} m^{\ell_2}_{k_2-q_2} \sigma^{\ell_2}_{\alpha_2\beta_2}\mathcal{G}_0(k_2) \\
={}& \frac{1}{(\beta N_s)^2} \sum_{k_1q_1}\sum_{\ell_1\ell_2} m^{\ell_1}_{k_1-q_1} \mathcal{G}_0(k_1) m^{\ell_2}_{q_1-k_1} \mathcal{G}_0(q_1) \tr(\sigma^{\ell_1}\sigma^{\ell_2}) \\
={}& \frac{1}{(\beta N_s)^2}\sum_{kq} 2\delta_{\ell_1\ell_2} m^{\ell_1}_{k-q} m^{\ell_2}_{q-k} \mathcal{G}_0(k)\mathcal{G}_0(q) 
\end{align}$$

Now shifting the momentum indices and rewriting as a dot product, we find 

$$\begin{align}
\tr X^2 ={}& \frac{2}{(\beta N_s)^2}\sum_{kq} \mathbf{m}_{k} \cdot \mathbf{m}_{-k} \mathcal{G}_0(k+q)\mathcal{G}_0(q) \\
={}& -\frac{1}{\beta N_s}\sum_{k} \mathbf{m}_k \cdot\mathbf{m}_{-k} \Pi_0(k).
\end{align}$$

We have defined the Lindhard function, which is given by

$$\begin{align}
\Pi_0(k) ={}& -\frac{2}{\beta N_s}\sum_q \mathcal{G}_0(k+q)\mathcal{G}_0(q) \\
={}& -\frac{2}{\beta N_s} \sum_{\q} \sum_{iq_0} \frac{1}{i\omega + iq_0 - \xi_{\k+\q}} \frac{1}{iq_0 - \xi_{\q}} \\
={}& -\frac{2}{N_s}\sum_{\q} \frac{n_F(\xi_{\q}) - n_F(\xi_{\k+\q})}{\xi_{\q} - \xi_{\k+\q} + i\omega}.
\end{align}$$

In the problems, we will evaluate the Lindhard function explicitly for a spherical Fermi surface. If we combine the result of \\(\Delta S^{(2)}_{\text{eff}}\\) with \\(\mathbf{m}^2\\) term found by performing the Hubbard-Stratonovich transformation, then the resulting quadratic part of the action is given by 

$$S^{(2)}_\text{eff} = \sum_k\left(\frac{3}{2U} - \frac{1}{2}\Pi_0(k)\right)\mathbf{m}_k \cdot \mathbf{m}_{-k}$$

Next, we compute the quartic contribution to the action. The details of the calculation are left to the problems. 



Now, the fourth power of \\(X\\) yields 

$$\begin{align}
\tr X^4 ={}& \frac{1}{(\beta N_s)^4}\sum_{\substack{k_1k_2k_3k_4 \\ q_1q_2q_3q_4}} \sum_{\ell_1\ell_2\ell_4\ell_4} \sum_{\substack{ \alpha_1\alpha_2\alpha_3\alpha_4 \\ \beta_1\beta_2\beta_3\beta_4}} \delta_{k_1q_4}\delta_{\alpha_1\beta_4}[m^{\ell_1}_{k_1-q_1}\sigma^{\ell_1}_{\alpha_1\beta_1}\mathcal{G}_0(k_1)] \delta_{q_1k_2}\delta_{\beta_1\alpha_2} \\
&\times [m^{\ell_2}_{k_2-q_2}\sigma^{\ell_2}_{\alpha_2\beta_2}\mathcal{G}_0(k_2)] \delta_{q_2k_3}\delta_{\beta_2\alpha_3} [m^{\ell_3}_{k_3-q_3}\sigma^{\ell_3}_{\alpha_3\beta_3}\mathcal{G}_0(k_3)] \delta_{q_3k_4}\delta_{\beta_3\alpha_4}[m^{\ell_4}_{k_4-q_4}\sigma^{\ell_4}_{\alpha_4\beta_4}\mathcal{G}_0(k_4)] \\
={}& \frac{1}{(\beta N_s)^4} \sum_{\substack{ k_1k_2k_3k_4 \\ \alpha_1\alpha_2\alpha_3\alpha_4 \\ \ell_1\ell_2\ell_4\ell_4}} m^{\ell_1}_{k_1-k_2}\sigma^{\ell_1}_{\alpha_1\alpha_2}\mathcal{G}_0(k_1)m^{\ell_2}_{k_2-k_3}\sigma^{\ell_2}_{\alpha_2\alpha_3}\mathcal{G}_0(k_2)m^{\ell_3}_{k_3-k_4}\sigma^{\ell_3}_{\alpha_3\alpha_4}\mathcal{G}_0(k_3)m^{\ell_4}_{k_4-k_1}\sigma^{\ell_4}_{\alpha_4\alpha_1}\mathcal{G}_0(k_4) \\
={}& \frac{1}{(\beta N_s)^4} \sum_{\substack{ k_1k_2k_3k_4 \\ \ell_1\ell_2\ell_4\ell_4}} m^{\ell_1}_{k_1-k_2}\mathcal{G}_0(k_1)m^{\ell_2}_{k_2-k_3}\mathcal{G}_0(k_2)m^{\ell_3}_{k_3-k_4}\mathcal{G}_0(k_3)m^{\ell_4}_{k_4-k_1}\mathcal{G}_0(k_4) \tr(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}\sigma^{\ell_4}) \\
\end{align}$$

The first thing we do is sum over the spin indices. We use the identity 

$$\begin{equation}
\sigma^a\sigma^b = \delta_{ab}\sigma^0 + i\epsilon_{abc}\sigma^c.
\end{equation}$$

Then, the trace simplifies down to

$$\begin{align}
\tr(\sigma^{\ell_1}\sigma^{\ell_2}\sigma^{\ell_3}\sigma^{\ell_4}) ={}& \tr([\delta_{\ell_1\ell_2}\sigma^0 + i\epsilon_{\ell_1\ell_2a}\sigma^a][\delta_{\ell_3\ell_4}\sigma^0 + i\epsilon_{\ell_3\ell_4b}\sigma^b]) \\
={}& \tr(\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4}\sigma^0 + i\delta_{\ell_1\ell_2}\epsilon_{\ell_3\ell_4 b}\sigma^b + i\delta_{\ell_3\ell_4}\epsilon_{\ell_1\ell_2}\sigma^a - \epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 b}\sigma^a\sigma^b) \\
={}& 2\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - \epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 b}\tr(\sigma^a\sigma^b) \\
={}& 2\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - 2\epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 b}\delta_{ab} \\
={}& 2\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - 2\epsilon_{\ell_1\ell_2 a}\epsilon_{\ell_3\ell_4 a}
\end{align}$$

Thus, we can rewrite 

$$\begin{align}
\sum_{\ell_1\ell_2\ell_3\ell_4} m^{\ell_1}_{k_1-k_2} m^{\ell_2}_{k_2-k_3} m^{\ell_3}_{k_3-k_4}m^{\ell_4}_{k_4-k_1}(\delta_{\ell_1\ell_2}\delta_{\ell_3\ell_4} - \epsilon_{\ell_1\ell_2\mu}\epsilon_{\ell_3\ell_4\mu}) ={}& (\mathbf{m}_{k_1-k_2}\cdot\mathbf{m}_{k_2-k_3})(\mathbf{m}_{k_3-k_4}\cdot\mathbf{m}_{k_4-k_1}) \\
&- (\mathbf{m}_{k_1-k_2}\times\mathbf{m}_{k_2-k_3})\cdot(\mathbf{m}_{k_3-k_4}\times\mathbf{m}_{k_4-k_1}) 
\end{align}$$

Thus, we have that \\(\tr X^4\\) becomes 
$$\begin{align}
\tr X^4 ={}& \frac{2}{(\beta N_s)^4} \sum_{k_1k_2k_3k_4} \mathcal{G}_0(k_1)\mathcal{G}_0(k_2)\mathcal{G}_0(k_3)\mathcal{G}_0(k_4)\left[ (\mathbf{m}_{k_1-k_2}\cdot\mathbf{m}_{k_2-k_3})(\mathbf{m}_{k_3-k_4}\cdot\mathbf{m}_{k_4-k_1}) \right. \\
&- \left.  (\mathbf{m}_{k_1-k_2}\times\mathbf{m}_{k_2-k_3})\cdot(\mathbf{m}_{k_3-k_4}\times\mathbf{m}_{k_4-k_1}) \right]
\end{align}$$

We now relabel the indices on the \\(m\\) fields. Let \\(k_1-k_2 = q_1\\), \\(k_2-k_3 = q_2\\), and \\(k_3-k_4 = q_3\\). Thus \\(k_4-k_1 = -(q_1+q_2+q_3)\\). Furthermore, \\(k_1 = k_4+q_1+q_2+q_3\\), \\(k_2 = k_4 + q_2+q_3\\), and \\(k_3 = k_4+q_3\\). We therefore rewrite as 

$$\begin{align}
\tr X^4 ={}& \frac{1}{(\beta N_s)^3} \sum_{q_1q_2q_3} u(q_1,q_2,q_3) \left[(\mathbf{m}_{q_1}\cdot\mathbf{m}_{q_2})(\mathbf{m}_{q_3}\cdot\mathbf{m}_{-q_1-q_2-q_3}) - (\mathbf{m}_{q_1}\times\mathbf{m}_{q_2})\cdot(\mathbf{m}_{q_3}\times\mathbf{m}_{-q_1-q_2-q_3}) \right]
\end{align}$$

where the coupling constant is given by 

$$\begin{align}
u(q_1,q_2,q_3) ={}& \frac{2}{\beta N_s}\sum_{k_4} \mathcal{G}_0(k_4+q_1+q_2+q_3)\mathcal{G}_0(k_4+q_2+q_3)\mathcal{G}_0(k_4+q_3)\mathcal{G}_0(k_4) 
\end{align}$$

We now make two approximations. We approximate \\(u(q_1,q_2,q_3) = u = -\frac{v}{12}\rho"(E_F)\\) to be a constant, and also remove the second term. The second term goes away if we assume that the coupling is independent of \\(q\\). See Hertz paper for details. Also: renormalizability argument for why it should be independent of \\(q\\)?? Now, we write the effective action as 

$$\begin{equation}
\Delta S_\text{eff}[\mathbf{m}] = - \frac{1}{2\beta N_s} \sum_k \mathbf{m}_k \cdot \mathbf{m}_{-k} \Pi_0(k) + \frac{u}{4(\beta N_s)^3} \sum_{q_1q_2q_3} (\mathbf{m}_{q_1}\cdot\mathbf{m}_{q_2})(\mathbf{m}_{q_3}\cdot\mathbf{m}_{-q_1-q_2-q_3})
\end{equation}$$

so the total effective action is given by 

$$\begin{equation}
S_\text{eff}[\mathbf{m}] = \frac{1}{2}\sum_k \left(\frac{3}{U} - \Pi_0(k)\right)\mathbf{m}_k\cdot\mathbf{m}_{-k} + \frac{u}{4(\beta N_s)^3} \sum_{k_1k_2k_3} (\mathbf{m}_{k_1}\cdot\mathbf{m}_{k_2})(\mathbf{m}_{k_3}\cdot\mathbf{m}_{-k_1-k_2-k_3})
\end{equation}$$

We then define 

$$\begin{equation}
\mathcal{G}_0^{-1}(k) = \frac{3}{U} - \Pi_0(k)
\end{equation}$$

To be the (inverse of the) free paramagnon propagator, so the effective action is simply 

$$\begin{equation}
S_\text{eff}[\mathbf{m}] = \frac{1}{2}\sum_k \mathcal{G}^{-1}_0(k) \mathbf{m}_k\cdot\mathbf{m}_{-k} + \frac{u}{4(\beta N_s)^3} \sum_{k_1k_2k_3} (\mathbf{m}_{k_1}\cdot\mathbf{m}_{k_2})(\mathbf{m}_{k_3}\cdot\mathbf{m}_{-k_1-k_2-k_3})
\end{equation}$$

The inverse of the paramagnon propagator, for small \\(k\\) and \\(\omega\\), is given by 

$$\begin{align}
\mathcal{G}_0(k) ={}& \frac{3}{U} -  \rho(E_F)\left[1 - \frac{1}{3}\left(\frac{k}{2k_F}\right)^2 - \frac{\pi|\omega|}{2kv_F}\right] \\
={}& r + gk^2 + s\frac{|\omega|}{k}
\end{align}$$

whereby \\(r = \frac{3}{U} - \rho(E_F)\\), \\(g = \frac{\rho(E_F)}{12 k_F^2}\\), and \\(s = \frac{\rho(E_F)\pi}{2v_F}\\). Also, we find that \\(u = -\frac{v}{12}\rho"(E_F)\\). 

