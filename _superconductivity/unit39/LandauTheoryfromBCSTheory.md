---
layout: lesson
title: Landau Theory from BCS Theory 
dept: physics
course: superconductivity
unit: unit39
deptDisplay: Physics
courseDisplay: Superconductivity & Superfluidity
unitDisplay: Unit 39
---

We recall that the effective action, as derived from the attractive Hubbard model, was given by

$$S_\text{eff}[\Delta^*,\Delta] = \int_0^\beta \sum_i \frac{1}{U}\|\Delta_{i\tau}\|^2\d\tau - \log\left<\exp\left(-\int_0^\beta\sum_i \left(\Delta_{i\tau}\bar{c}_{i\tau\uparrow}\bar{c}_{i\tau\downarrow} + \Delta^*_{i\tau} c_{i\tau\downarrow} c_{i\tau\uparrow}\right)\d\tau\right)\right>_0.$$

If we Fourier transform all of the fields in \\(\Delta S_\text{eff}\\) according to 

$$c_{i\tau\sigma} = \frac{1}{\sqrt{N_s\beta}} \sum_k e^{-ik_0\tau + i\mathbf{R}_i\cdot\k}c_{k\sigma}, \quad \bar{c}_{i\tau\sigma} = \frac{1}{\sqrt{N_s\beta}}\sum_k e^{ik_0-i\mathbf{R}_i\cdot\k}\bar{c}_{k\sigma},\quad \Delta_{i\tau} = \frac{1}{\beta N_s}\sum_k e^{-ik_0\tau + i\mathbf{R}_i\cdot\k}\Delta_k $$

we find that 

$$\begin{align}
\Delta S_\text{eff} = -\log\left<\exp\left(-\frac{1}{\beta N_s}\sum_{kq}\left(\Delta_{k+q}\bar{c}_{k\uparrow}\bar{c}_{q\downarrow} + \Delta^*_{k+q}c_{k\downarrow}c_{q\uparrow}\right) \right)\right>_0
\end{align}$$

To easily integrate out the fermions, we perform a Bogolyubov transformation. This is done by writing 

$$\begin{align}
\Delta S_\text{eff} =& -\log\left(\frac{1}{Z_0} \int e^{-S_0} \exp\left(-\frac{1}{\beta N_s}\sum_{kq}\left(\Delta_{k+q}\bar{c}_{k\uparrow}\bar{c}_{q\downarrow} + \Delta^*_{k+q}c_{k\downarrow}c_{q\uparrow}\right) \right)\D\bar{c}\D c\right) \\
=&-\log\left(\frac{1}{Z_0}\int \exp\left(\sum_{kq}\left[ \bar{c}_{k\sigma} \mathcal{G}^{-1}_0(k) c_{q\sigma} \delta_{kq} - \frac{1}{\beta N_s} \Delta_{k+q}\bar{c}_{k\uparrow} \bar{c}_{q\downarrow} - \frac{1}{\beta N_s} \Delta^*_{k+q} c_{k\downarrow} c_{q\uparrow} \right] \right) \D \bar{c} \D c\right)
\end{align}$$

Let us now massage the integrand. We can rewrite it as 

$$\begin{align}
=& \sum_{kq}\left[ \bar{c}_{k\sigma} \mathcal{G}^{-1}_0(k) c_{q\sigma} \delta_{kq} - \frac{1}{\beta N_s} \Delta_{k+q}\bar{c}_{k\uparrow} \bar{c}_{q\downarrow} - \frac{1}{\beta N_s} \Delta^*_{k+q} c_{k\downarrow} c_{q\uparrow} \right] \\
=& \sum_{kq}\begin{pmatrix} \bar{c}_{k\uparrow} & c_{-k\downarrow} \end{pmatrix} \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & -\frac{1}{\beta N_s}\Delta_{k-q} \\ -\frac{1}{\beta N_s}\Delta^*_{q-k} & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix} \begin{pmatrix} c_{q\uparrow} \\ \bar{c}_{-q\downarrow} \end{pmatrix} 
\end{align}$$

Here \\(\mathcal{G}_0(-k)\\) refers to swapping the signs of both the Matsubara frequency and the momentum. Now, if we evaluate the integral 

$$\int\exp\left(\sum_{kq}\begin{pmatrix} \bar{c}_{k\uparrow} & c_{-k\downarrow} \end{pmatrix} \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & -\frac{1}{\beta N_s}\Delta_{k-q} \\ -\frac{1}{\beta N_s}\Delta^*_{q-k} & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix} \begin{pmatrix} c_{q\uparrow} \\ \bar{c}_{-q\downarrow} \end{pmatrix} \right)\D\bar{c}\D c = \det \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & -\frac{1}{\beta N_s}\Delta_{k-q} \\ -\frac{1}{\beta N_s}\Delta^*_{q-k} & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix} $$

Note that the determinant is NOT simply over this \\(2\times 2\\) matrix, but rather also over \\(k\\) and \\(q\\). We then have that 

$$\begin{align}
\Delta S_\text{eff} =& -\log \left[\frac{1}{Z_0}\det \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & -\frac{1}{\beta N_s}\Delta_{k-q} \\ -\frac{1}{\beta N_s}\Delta^*_{q-k} & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix}\right] \\
=& \log Z_0 -\tr\log \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & -\frac{1}{\beta N_s}\Delta_{k-q} \\ -\frac{1}{\beta N_s}\Delta^*_{q-k} & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix} 
\end{align}$$

Now, we write this as a matrix multiplication: 

$$\begin{align}
\Delta S_\text{eff} =& -\tr\log\left[ \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & 0 \\ 0 & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix}  \begin{pmatrix} \delta_{kq} & -\frac{1}{\beta N_s}\mathcal{G}_0(k)\Delta_{k-q} \\ \frac{1}{\beta N_s}\mathcal{G}_0(-k)\Delta^*_{q-k} & \delta_{kq} \end{pmatrix} \right]
\end{align}$$

Now, using \\(\tr\log[AB] = \tr\log A + \tr\log B\\), we have that 

$$\begin{align}
\Delta S_\text{eff} =& \log Z_0 - \tr\log \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & 0 \\ 0 & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix} - \tr\log \begin{pmatrix} \delta_{kq} & -\frac{1}{\beta N_s}\mathcal{G}_0(k)\Delta_{k-q} \\ \frac{1}{\beta N_s}\mathcal{G}_0(-k)\Delta^*_{q-k} & \delta_{kq} \end{pmatrix} \\
=& \log Z_0 - \log\det \begin{pmatrix} \mathcal{G}^{-1}_0(k)\delta_{kq} & 0 \\ 0 & -\mathcal{G}^{-1}_0(-k)\delta_{kq}\end{pmatrix} - \tr\log(\1-X)
\end{align}$$

Since the first term is completely diagonal, it reduces to a product over diagonal elements in both \\(k\\) space and in the \\(2\times 2\\) space, and also the matrix \\(X\\) is given by 

$$\begin{equation}
X_{kq} = \begin{pmatrix} 0 & -\frac{1}{\beta N_s}\mathcal{G}_0(k)\Delta_{k-q} \\ \frac{1}{\beta N_s}\mathcal{G}_0(-k)\Delta^*_{q-k} & 0\end{pmatrix}
\end{equation}$$

Thus, the effective action can be written as 

$$\begin{align}
\Delta S_\text{eff} =& \log Z_0 - \underbrace{\log\prod_k (\mathcal{G}^{-1}_0)^2}_{Z_0}- \tr\log(\1-X)
\end{align}$$

Now, the effective action can be Taylor expanded according to 

$$-\log(\1 - X) = \sum_{n=1}^\infty \frac{X^n}{n}$$

It is clear that the first order correction is zero. The second order correction is nonzero, so we compute \\(X^2\\):

$$\begin{align}
(X^2)_{k_1q_2} =& \tr\left[\begin{pmatrix} 0 & -\frac{\mathcal{G}_0(k_1)}{\beta N_s}\Delta_{k_1-q_1} \\ \frac{\mathcal{G}_0(-k_1)}{\beta N_s}\Delta^*_{q_1-k_1} & 0 \end{pmatrix} \begin{pmatrix} 0 & -\frac{\mathcal{G}_0(k_2)}{\beta N_s}\Delta_{k_2-q_2} \\ \frac{\mathcal{G}_0(-k_2)}{\beta N_s}\Delta^*_{q_2-k_2} & 0 \end{pmatrix}\right] \\
=& -\frac{1}{(\beta N_s)^2}\sum_{q_1k_2} \begin{pmatrix} \delta_{q_1k_2} \mathcal{G}_0(k_1)\Delta_{k_1-q_1}\mathcal{G}_0(-k_2)\Delta^*_{q_2-k_2}& 0 \\ 0 & \delta_{q_1k_2} \mathcal{G}_0(-k_1)\Delta^*_{q_1-k_1}\mathcal{G}_0(k_2)\Delta_{k_2-q_2} \end{pmatrix} \\
=& -\frac{1}{(\beta N_s)^2} \sum_{k_2} \begin{pmatrix} \mathcal{G}_0(k_1)\Delta_{k_1-k_2}\mathcal{G}_0(-k_2)\Delta^*_{q_2-k_2}& 0 \\ 0 & \mathcal{G}_0(-k_1)\Delta^*_{k_2-k_1}\mathcal{G}_0(k_2)\Delta_{k_2-q_2} \end{pmatrix} 
\end{align}$$


The fourth order contribution comes from 

$$\begin{align}
(X^4)_{k_1q_4} =&\frac{1}{(\beta N_s)^4}\begin{pmatrix} (x_1)_{k_1q_4}& 0 \\0 & (x_2)_{k_1q_4} \end{pmatrix}
\end{align}$$

where

$$\begin{align}
(x_1)_{k_1q_4} =& \sum_{k_2q_2k_3k_4} \mathcal{G}_0(k_1)\Delta_{k_1-k_2}\mathcal{G}_0(-k_2)\Delta^*_{q_2-k_2}\delta_{q_2k_3} \mathcal{G}_0(k_3)\Delta_{k_3-k_4}\mathcal{G}_0(-k_4) \Delta^*_{q_4-k_4} \\
=& \sum_{k_2k_3k_4} \mathcal{G}_0(k_1)\Delta_{k_1-k_2}\mathcal{G}_0(-k_2)\Delta^*_{k_3-k_2} \mathcal{G}_0(k_3)\Delta_{k_3-k_4}\mathcal{G}_0(-k_4) \Delta^*_{q_4-k_4} \\
(x_2)_{k_1q_4} =& \sum_{k_2q_2k_3k_4} \mathcal{G}_0(-k_1)\Delta_{k_2-q_2}\mathcal{G}_0(k_2)\Delta^*_{k_2-k_1} \delta_{q_2k_3}\mathcal{G}_0(-k_3)\Delta_{k_4-q_4} \mathcal{G}_0(k_4)\Delta^*_{k_4-k_3} \\
=& \sum_{k_2k_3k_4} \mathcal{G}_0(-k_1)\Delta_{k_2-k_3}\mathcal{G}_0(k_2)\Delta^*_{k_2-k_1} \mathcal{G}_0(-k_3)\Delta_{k_4-q_4} \mathcal{G}_0(k_4)\Delta^*_{k_4-k_3}
\end{align}$$

Now, let's compute the second order correction:

$$\begin{align}
\Delta S_\text{eff}^{(2)} =& \frac{1}{2}\tr X^2 \\
=& -\frac{1}{2(\beta N_s)^2}\sum_{k_1k_2q_2} \delta_{q_2k_1} \tr_{2\times 2} \begin{pmatrix} \mathcal{G}_0(k_1)\Delta_{k_1-k_2}\mathcal{G}_0(-k_2)\Delta^*_{q_2-k_2}& 0 \\ 0 & \mathcal{G}_0(-k_1)\Delta^*_{k_2-k_1}\mathcal{G}_0(k_2)\Delta_{k_2-q_2} \end{pmatrix} \\
=& -\frac{1}{2(\beta N_s)^2}\sum_{k_1k_2} \tr_{2\times 2} \begin{pmatrix} \mathcal{G}_0(k_1)\Delta_{k_1-k_2}\mathcal{G}_0(-k_2)\Delta^*_{k_1-k_2}& 0 \\ 0 & \mathcal{G}_0(-k_1)\Delta^*_{k_2-k_1}\mathcal{G}_0(k_2)\Delta_{k_2-k_1} \end{pmatrix} \\
=& -\frac{1}{2(\beta N_s)^2}\sum_{k_1k_2} \tr_{2\times 2} \begin{pmatrix} \mathcal{G}_0(k_1) \mathcal{G}_0(-k_2) \|\Delta_{k_1-k_2}\|^2& 0 \\ 0 & \mathcal{G}_0(-k_1) \mathcal{G}_0(k_2)\|\Delta_{k_2-k_1}\|^2 \end{pmatrix} \\
=& -\frac{1}{2(\beta N_s)^2}\sum_{kq} \tr_{2\times 2} \begin{pmatrix} \mathcal{G}_0(k) \mathcal{G}_0(q-k) \|\Delta_q\|^2 & 0 \\ 0 & \mathcal{G}_0(k) \mathcal{G}_0(q-k) \|\Delta_q\|^2\end{pmatrix} \\
=& -\frac{1}{\beta N_s}\sum_{k}\|\Delta_k\|^2 \frac{1}{\beta N_s}\sum_q \mathcal{G}_0(q) \mathcal{G}_0(k-q) 
\end{align}$$

We finally define \\(P(k) = \frac{1}{\beta N_s} \sum_q \mathcal{G}_0(q) \mathcal{G}_0(k-q) \\), and get 

$$\begin{align}
\Delta S_\text{eff}^{(2)} =& -\frac{1}{\beta N_s}\sum_{k}\|\Delta_k\|^2 P(k) 
\end{align}$$

Now, we compute the fourth order correction:

$$\begin{align}
\Delta S_\text{eff}^{(4)} =& \frac{1}{4}\tr X^4 \\
=& \frac{1}{4(\beta N_s)^4}\tr_{2\times 2} \begin{pmatrix} \tr_{k} (x_1) & 0 \\0 & \tr_k (x_2) \end{pmatrix} 
\end{align}$$

Now, we evaluate the traces over the momenta and Matsubara sums. This gives

$$\begin{align}
\tr_k(x_1) =& \sum_{k_1k_2k_3k_4q_4}\delta_{q_4k_1}\mathcal{G}_0(k_1)\Delta_{k_1-k_2}\mathcal{G}_0(-k_2)\Delta^*_{k_3-k_2}\mathcal{G}_0(k_3)\Delta_{k_3-k_4}\mathcal{G}_0(-k_4)\Delta^*_{q_4-k_4} \\
=& \sum_{k_1k_2k_3k_4}\mathcal{G}_0(k_1)\Delta_{k_1-k_2}\mathcal{G}_0(-k_2)\Delta^*_{k_3-k_2}\mathcal{G}_0(k_3)\Delta_{k_3-k_4}\mathcal{G}_0(-k_4)\Delta^*_{k_1-k_4} \\
=& \sum_{k_1k_2k_3}\Delta_{k_1}\Delta^*_{k_2}\Delta_{k_3}\Delta^*_{k_1-k_2+k_3}\sum_{q}\mathcal{G}_0(q)\mathcal{G}_0(k_1-q)\mathcal{G}_0(q-k_1+k_2)\mathcal{G}_0(k_1+k_3-k_2-q)
\end{align}$$

SImilarly, we find that 

$$\begin{align}
\tr_k(x_2) =& \sum_{k_1k_2k_3k_4q_4} \delta_{q_4k_1} \mathcal{G}_0(-k_1) \Delta_{k_2-k_3} \mathcal{G}_0(k_2) \Delta^*_{k_2-k_1} \mathcal{G}_0(-k_3) \Delta_{k_4-q_4} \mathcal{G}_0(k_4) \Delta^*_{k_4-k_3} \\
=& \sum_{k_1k_2k_3k_4} \mathcal{G}_0(-k_1)\Delta_{k_2-k_3} \mathcal{G}_0(k_2) \Delta^*_{k_2-k_1} \mathcal{G}_0(-k_3) \Delta_{k_4-k_1} \mathcal{G}_0(k_4) \Delta^*_{k_4-k_3} \\
=& \sum_{k_1k_2k_3} \Delta_{k_1}\Delta^*_{k_2}\Delta_{k_3}\Delta^*_{k_1-k_2+k_3} \sum_q \mathcal{G}_0(q) \mathcal{G}_0(k_1-q)\mathcal{G}_0(q-k_1+k_2)\mathcal{G}_0(k_1+k_3-k_2-q)
\end{align}$$

We therefore see that \\(\tr_k(x_1) = \tr_k(x_2)\\), so that we get 

$$\begin{align}
\Delta S_\text{eff}^{(4)} =& \frac{1}{2(\beta N_s)^4} \tr(x_1) \\
=&  \frac{1}{2(\beta N_s)^4} \sum_{k_1k_2k_3} \Delta_{k_1}\Delta^*_{k_2}\Delta_{k_3}\Delta^*_{k_1-k_2+k_3} \sum_q \mathcal{G}_0(q) \mathcal{G}_0(k_1-q)\mathcal{G}_0(q-k_1+k_2)\mathcal{G}_0(k_1+k_3-k_2-q)
\end{align}$$

We then define 

$$u(k_1,k_2,k_3) = \frac{1}{2\beta N_s} \sum_q \mathcal{G}_0(q) \mathcal{G}_0(k_1-q)\mathcal{G}_0(q-k_1+k_2)\mathcal{G}_0(k_1+k_3-k_2-q)$$

Thus, we get 

$$\begin{align}
\Delta S_\text{eff}^{(4)} =&  \frac{1}{(\beta N_s)^3} \sum_{k_1k_2k_3} u(k_1,k_2,k_3) \Delta_{k_1}\Delta^*_{k_2}\Delta_{k_3}\Delta^*_{k_1-k_2+k_3}
\end{align}$$

The full effective action is therefore given by 

$$S_\text{eff}[\Delta,\Delta^*] = \frac{1}{\beta N_s}\sum_k \|\Delta_k\|^2\left(\frac{1}{U} -  P(k)\right) + \frac{1}{(\beta N_s)^3} \sum_{k_1k_2k_3}u(k_1,k_2,k_3) \Delta_{k_1} \Delta^*_{k_2} \Delta_{k_3} \Delta^*_{k_1-k_2+k_3} + O(\Delta^6)$$

Now let's try to learn a little bit more about these coefficients. We can rewrite 

$$\begin{align}
P(k) =& \frac{1}{\beta N_s}\sum_q \mathcal{G}_0(q) \mathcal{G}_0(k-q) \\
=& \frac{1}{N_s}\sum_{\q} \frac{1}{\beta} \sum_{i\omega} \frac{1}{i\omega - \xi_{\q}} \frac{1}{ik_0 - i\omega - \xi_{\k-\q}} \\
=& \frac{1}{N_s} \sum_{\q} \frac{n_F(\xi_{\q}) - n_F(-\xi_{\k-\q})}{ik_0 - \xi_{\q} - \xi_{\k-\q}} \\
=& \frac{1}{N_s}\sum_{\q} \frac{1 - n_F(\xi_{\q}) - n_F(\xi_{\k-\q})}{-ik_0 + \xi_{\q} + \xi_{\k-\q}}
\end{align}$$

Now, let's take the Taylor expansion around small \\(\k\\) and \\(k_0\\). This makes sense because high powers of \\(k\\) and \\(k_0\\) will be irrelevant. We first find 

$$\begin{align}
P(0) =& \frac{1}{N_s}\sum_{\q} \frac{1 - 2n_F(\xi_{\q})}{2\xi_{\q}} \\
=& \frac{1}{N_s}\sum_{\q} \frac{\tanh(\beta\xi_{\q}/2)}{2\xi_{\q}} \\
=& \int_{-\Lambda}^\Lambda \rho(\xi) \frac{\tanh(\beta \xi/2)}{2\xi} \d\xi \\
\sim & \rho(0)\int_{0}^\Lambda \frac{\tanh(\beta \xi/2)}{\xi} \d\xi \\
=& \rho(0)\int_{0}^{\beta\Lambda/2} \frac{\tanh x}{x} \d x \\
=& \rho(0)\left[\log x \tanh x \bigg|_0^{\beta\Lambda/2} - \int_{0}^{\beta\Lambda/2} \frac{\log x}{\cosh^2 x} \d x \right] \\
\sim & \rho(0)\left[\log \frac{\beta\Lambda}{2} \tanh \frac{\beta\Lambda}{2} - \int_{0}^{\infty} \frac{\log x}{\cosh^2 x} \d x \right] \\
=& \rho(0)\left[\log \frac{\beta\Lambda}{2} - \log\left(\frac{\pi}{4e^\gamma}\right) \right] \\
=& \rho(0)\log \left(\frac{2e^\gamma\beta\Lambda}{\pi}\right) \\
\end{align}$$

Next, we need to compute \\(P(ik_0,0)\\) for small Matsubara frequency. To do this, we set \\(\k = 0\\). Doing this, we get 

$$\begin{align}
P(ik_0,0) =& \frac{1}{N_s}\sum_{\q} \frac{1 - 2n_F(\xi_{\q})}{-ik_0 + 2\xi_{\q}} \\
=& \int_{-\Lambda}^{\Lambda} \rho(\xi) \frac{\tanh(\beta\xi/2)}{-ik_0 + 2\xi} \d\xi \\
=& \rho(0) \int_{-\Lambda}^{\Lambda} \frac{\tanh(\beta\xi/2)}{-ik_0 + 2\xi} \d\xi \\
\end{align}$$

Now, we multiply by the conjugate to find

$$\begin{align}
P(ik_0,0) =& \rho(0) \int_{-\Lambda}^{\Lambda} \frac{\tanh(\beta\xi/2)}{k_0^2 + 4\xi^2}(ik_0 + 2\xi) \d\xi \\
=& \rho(0) \int_{-\Lambda}^{\Lambda} \frac{\tanh(\beta\xi/2)}{k_0^2 + 4\xi^2}2\xi \d\xi \\
=& 4\rho(0) \int_{0}^{\Lambda} \frac{\xi\tanh(\beta\xi/2)}{k_0^2 + 4\xi^2} \d\xi \\
\end{align}$$

Now, we want this integral to look like the original integral \\(P(0,0)\\). To do this, we perform the following manipulation:

$$\begin{align}
P(ik_0,0) =& \rho(0) \int_{0}^{\Lambda} \frac{1}{\xi} \tanh\left(\frac{\beta\xi}{2}\right)\left(\frac{4\xi^2}{k_0^2 + 4\xi^2} - 1 + 1\right)\d\xi \\
=& \rho(0) \int_{0}^{\Lambda} \frac{1}{\xi} \tanh\left(\frac{\beta\xi}{2}\right)\d\xi + \rho(0)\int_0^\Lambda \frac{1}{\xi} \tanh\left(\frac{\beta\xi}{2}\right)\left(\frac{4\xi^2}{k_0^2 + 4\xi^2} - 1\right)\d\xi \\
=& P(0) - \rho(0)\int_0^\Lambda \frac{1}{\xi} \tanh\left(\frac{\beta\xi}{2}\right)\frac{k_0^2}{k_0^2 + 4\xi^2} \d\xi \\
=& P(0) - \rho(0)k_0^2\int_0^\Lambda \frac{1}{\xi} \tanh\left(\frac{\beta\xi}{2}\right)\frac{1}{k_0^2 + 4\xi^2} \d\xi \\
\approx & P(0) - \rho(0)k_0^2\int_0^\infty \frac{1}{\xi} \tanh\left(\frac{\beta\xi}{2}\right)\frac{1}{k_0^2 + 4\xi^2} \d\xi
\end{align}$$

Since \\(k_0\\) is small, the integral is dominated by small \\(\xi\\). Thus let us replace \\(\tanh(\beta\xi/2)/\xi\\) by its value at \\(\xi = 0\\). This gives us 

$$\begin{align}
P(ik_0,0) =& P(0) - \frac{\beta\rho(0)}{2} k_0^2\int_0^\infty \frac{1}{k_0^2 + 4\xi^2} \d\xi \\
=& P(0) - \frac{\rho(0)\beta}{2} k_0^2 \frac{1}{2\|k_0\|} \arctan\left(\frac{2\xi}{k_0}\right)\bigg|_0^\infty \\
=& P(0) - \frac{\rho(0)\beta}{2} k_0^2 \frac{1}{2\|k_0\|} \frac{\pi}{2} \\
=& P(0) - \frac{\rho(0)\beta \pi}{8} \|k_0\|
\end{align}$$

Lastly, we compute \\(P(0,\k)\\) for small momentum. Let us do this for \\(k_0 = 0\\) and Taylor expand in small \\(\k\\). We define \\(\xi_{\q-\k} = \xi_{\q} + \epsilon\\), where \\(\epsilon\\) is small.

$$\begin{align}
P(0,\k) =& \frac{1}{N_s}\sum_{\q} \frac{1 - n_F(\xi_{\q}) - n_F(\xi_{\k-\q})}{\xi_{\q} + \xi_{\k-\q}}
\end{align}$$

Let us first compute the derivatives of \\(P(0,\k)\\). This gives us 

$$\begin{align}
\frac{\partial P}{\partial k_\alpha} =& \frac{1}{N_s}\sum_{\q} \left(\frac{-n_F'(\xi_{\k-\q})}{\xi_{\q} + \xi_{\k-\q}} - \frac{1 - n_F(\xi_{\q}) - n_F(\xi_{\k-\q})}{(\xi_{\q} + \xi_{\k-\q})^2}\right)\partial_\alpha\xi_{\k-\q}
\end{align}$$

Setting \\(\k = 0\\), we then see that the only remaining terms are odd in \\(\q\\) (assuming that \\(\xi\\) is an even function). This means that all the terms go to zero because the sum is odd. Now, for the second derivative, we find 

$$\begin{align}
\frac{\partial^2 P}{\partial k_\alpha k_\beta} =& \frac{1}{N_s}\sum_{\q} \left(\frac{-n_F'(\xi_{\k-\q})}{\xi_{\q} + \xi_{\k-\q}} - \frac{1 - n_F(\xi_{\q}) - n_F(\xi_{\k-\q})}{(\xi_{\q} + \xi_{\k-\q})^2}\right)\partial_\alpha\partial_\beta\xi_{\k-\q} \\
&+ \frac{1}{N_s}\sum_{\q}\left(2\frac{n_F'(\xi_{\k-\q})}{(\xi_{\q} + \xi_{\k-\q})^2} - \frac{n_F"(\xi_{\k-\q})}{\xi_{\q} + \xi_{\k-\q}} + 2\frac{1 - n_F(\xi_{\q}) - n_F(\xi_{\k-\q})}{(\xi_{\q} + \xi_{\k-\q})^3} \right) (\partial_\alpha \xi_{\k-\q}) (\partial_\beta \xi_{\k-\q}) 
\end{align}$$

For the first line, if we set that \\(\k = 0\\) and assume that \\(\partial_\alpha \partial_\beta \xi_{\k-\q}\\) is independent of \\(\q\\), then the all the terms are odd in \\(\xi\\) and with an even density of states it all goes away. This the expression simplifies to 

$$\begin{align}
\frac{\partial^2 P}{\partial k_\alpha k_\beta} =& \frac{1}{N_s}\sum_{\q}\left(2\frac{n_F'(\xi_{\q})}{(2\xi_{\q})^2} - \frac{n_F"(\xi_{\q})}{2\xi_{\q}} + 2\frac{\tanh(\beta\xi_{\q}/2)}{(2\xi_{\q})^3} \right) v_F^2
\end{align}$$

where we set \\(\partial_\alpha \xi_{\k-\q} = v_F\\). We can now change everything to an integral over energies

$$\begin{align}
\frac{\partial^2 P}{\partial k_\alpha k_\beta} =& v_F^2\rho(0) \int_{-\Lambda}^\Lambda \left(\frac{n_F'(\xi)}{2\xi^2} - \frac{n_F"(\xi)}{2\xi} + \frac{\tanh(\beta\xi/2)}{4\xi^3} \right)\d\xi \\
=& v_F^2\rho(0) \int_0^\Lambda \left(\frac{n_F'(\xi)}{\xi^2} - \frac{n_F"(\xi)}{\xi} + \frac{\tanh(\beta\xi/2)}{2\xi^3} \right)\d\xi \\
=& v_F^2\rho(0) \int_0^{\beta\Lambda/2} \left(-\frac{\beta^3}{16x^2\cosh^2 x} - \frac{\beta^3\sinh x}{8x\cosh^3 x} + \frac{\beta^3\tanh x}{16x^3} \right)\frac{2}{\beta}\d x \\
\sim & \frac{\beta^2 v_F^2\rho(0)}{8} \int_0^{\infty} \left(-\frac{1}{x^2\cosh^2 x} - \frac{2\sinh x}{x\cosh^3 x} + \frac{\tanh x}{x^3} \right) \d x
\end{align}$$

Now, we can rewrite some of this:

$$\begin{align}
\frac{\partial^2 P}{\partial k_\alpha k_\beta} =& \frac{\beta^2 v_F^2\rho(0)}{8} \left[\int_0^{\infty} \left(\frac{\d}{\d x}\frac{1}{x\cosh^2 x} + \frac{1}{2x^2\cosh^2 x} \right) \d x - \frac{\tanh x}{2x^2}\bigg|_0^\infty \right] \\
=& \frac{\beta^2 v_F^2\rho(0)}{8} \left[\int_0^{\infty} \frac{1}{2x^2\cosh^2 x} \d x + \left(\frac{1}{x\cosh^2 x} - \frac{\tanh x}{2x^2}\right)\bigg|_0^\infty \right] \\
=& \frac{\beta^2 v_F^2\rho(0)}{8}\left[-\int_0^\infty \frac{\sinh x}{x\cosh^3 x} \d x + \left(\frac{1}{2x\cosh^2 x} - \frac{\tanh x}{2x^2}\right)\bigg|_0^\infty \right] \\
=& -\frac{\beta^2 v_F^2\rho(0)}{8}\int_0^\infty \frac{\sinh x}{x\cosh^3 x} \d x \\
\end{align}$$

Finally, we use the integral

$$\int_0^\infty \frac{\sinh x}{x\cosh^3 x} \d x = \frac{7\zeta(3)}{\pi^2}$$

to get that 

$$\begin{align}
\frac{\partial^2 P}{\partial k_\alpha k_\beta} =& -\frac{7\beta^2 v_F^2\rho(0)\zeta(3)}{8\pi^2}
\end{align}$$

Finally, we get that 

$$P(ik_0,\k) \sim \rho(0)\left[\log\left(\frac{2 e^\gamma \beta\Lambda}{\pi}\right) - \frac{\beta\pi\|k_0\|}{8} - \frac{7\beta^2 v_F^2 \zeta(3)}{16\pi^2}\k^2\right]$$

We need to calculate \\(u\\) and check that it is positive. Since the contributions which have powers of \\(k\\) will be irrelevant, let us simply plug in \\(k_1=k_2=k_3 = 0\\). Doing this, we find 

$$\begin{align}
u(0,0,0) =& \frac{1}{2\beta N_s}\sum_q \mathcal{G}_0(q) \mathcal{G}_0(-q) \mathcal{G}_0(q)\mathcal{G}_0(-q) \\
=& \frac{1}{2\beta N_s} \sum_q \frac{1}{(iq_0 - \xi_{\q})^2} \frac{1}{(-iq_0 - \xi_{-\q})^2} \\
=& \frac{1}{2\beta N_s} \sum_q \frac{1}{(q^2 + \xi_{\q}^2)^2}
\end{align}$$

We first integrate over the energies. This gives us 

$$\begin{align}
u(0,0,0) =& \frac{1}{2\beta}\sum_{iq_0}  \int_{-\infty}^\infty \rho(\xi) \frac{1}{(q^2 + \xi^2)^2} \d\xi \\
\sim & \frac{\rho(0)}{2\beta}\sum_{iq_0}  \int_{-\infty}^\infty \frac{1}{(q^2 + \xi^2)^2} \d\xi \\
=& \frac{\rho(0)}{4\beta}\sum_{iq_0} \frac{1}{q_0^3}\left(\arctan\left(\frac{\xi}{q_0}\right) + \frac{\xi/q_0}{1+(\xi/q_0)^2}\right)\bigg|_{-\infty}^\infty \\
=& \frac{\rho(0)}{4\beta}\sum_{iq_0} \frac{1}{q_0^3}\pi \\
=& \frac{\rho(0)\pi}{4\beta}\frac{\beta^3}{\pi^3}\sum_{n=-\infty}^\infty \frac{1}{(2n-1)^3} \\
=& \frac{\rho(0)\beta^2}{4\pi^2}2\sum_{n=1}^\infty \frac{1}{(2n-1)^3} 
\end{align}$$

We note that 

$$\sum_{n=1}^\infty \frac{1}{(2n-1)^3} + \sum_{n=1}^\infty \frac{1}{(2n)^3} = \zeta(3) = \sum_{n=1}^\infty \frac{1}{(2n-1)^3} + \frac{1}{8}\zeta(3) $$

which gives us 

$$\sum_{n=1}^\infty \frac{1}{(2n-1)^3}  = \frac{7}{8}\zeta(3)$$

which finally tells us that 

$$\begin{align}
u(0,0,0) =& \frac{\rho(0) \beta^2}{2\pi^2}\frac{7}{8}\zeta(3) \\
=& \frac{7\rho(0)\beta^2 \zeta(3)}{16\pi^2}
\end{align}$$

Now, the Ginzburg-Landau action is given by 

$$S_\text{eff}[\Delta,\Delta^*] = \frac{1}{\beta N_s}\sum_k \|\Delta_k\|^2\left(r + s\|k_0\| + g\k^2\right) + \frac{u}{(\beta N_s)^3} \sum_{k_1k_2k_3}\Delta_{k_1} \Delta^*_{k_2} \Delta_{k_3} \Delta^*_{k_1-k_2+k_3}$$

whereby \\(r = \frac{1}{U} - \rho(0)\log\left(\frac{2e^\gamma \beta\Lambda}{\pi}\right)\\), \\(s = \frac{\beta\pi\rho(0)}{8}\\), \\(g = \frac{7\beta^2 v_F^2\zeta(3)\rho(0)}{16\pi^2}\\), and \\(u = \frac{7\rho(0)\beta^2 \zeta(3)}{16\pi^2}\\). We have neglected the irrelevant dependence of \\(u\\) on the Matsubara frequencies and momenta, and also the higher order terms in the kinetic energy. The observant reader may recognize this as (almost) the same action which appears in a 3-dimensional itinerant antiferromagnet, the difference being that the order parameter field is the magnetization instead of the superconducting gap. 

<ol>
<li> <div class="exercise">  Show that
$$\begin{equation}
\int_{0}^{\infty} \frac{\log x}{\cosh^2 x} \d x = \log\left(\frac{\pi}{4e^\gamma}\right)
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer315')" class="answerButton">Show Answer</button> 
 <div  id='answer315' class="answer" >
To evaluate this, consider computing 

$$\begin{equation}
I(s) = \int_0^\infty \frac{x^{s}}{\cosh^2 x}\d x
\end{equation}$$

For this, consider the following identity for the \href{https://en.wikipedia.org/wiki/Dirichlet_eta_function}{Dirichlet eta function}:

$$\begin{equation}
2^{1-s}\Gamma(s+1)\eta(s) = \int_0^\infty \frac{t^s}{\cosh^2 t} \d t
\end{equation}$$

We want to compute \(I'(0)\). This gives us 

$$\begin{equation}
I'(s) = -\log(2)2^{1-s}\Gamma(s+1)\eta(s) + 2^{1-s}\Gamma'(s+1)\eta(s) + 2^{1-s}\Gamma(s+1)\eta'(s)
\end{equation}$$

We know that the derivative of the \(\Gamma\)-function \(\Gamma'(z) = \Gamma(z)\psi(z)\), where \(\psi\) is the digamma function. Since \(\Gamma(1) = 1\) and \(\psi(1) = -\gamma\), where \(\gamma\) is the Euler-Mascheroni constant, the second term is also solved. For the third term, we need that \(\eta(0) = 1/2\). 

$$\begin{equation}
\eta '(s)=2^{1-s}\log(2)\zeta (s)+(1-2^{1-s})\zeta'(s)
\end{equation}$$

Since \(\zeta'(0) = -\frac{1}{2}\log(2\pi)\) and \(\zeta(0) = -1/2\), we have that 

$$\begin{equation}
\eta'(0) = -\log 2 +\frac{1}{2}\log(2\pi) = \frac{1}{2}\log\frac{\pi}{2}
\end{equation}$$


Thus, we have that 

$$\begin{align}
I'(0) ={}& -2\log 2\Gamma(1)\eta(0) + 2\Gamma'(1)\eta(0) + 2\Gamma(1)\eta'(0) \\
={}& -\log2 - \gamma + \log\frac{\pi}{2} \\
={}& \log\left(\frac{\pi}{4e^\gamma}\right)
\end{align}$$

Thus,

$$\begin{equation}
\int_{0}^{\infty} \frac{\log x}{\cosh^2 x} \d x = \log\left(\frac{\pi}{4e^\gamma}\right)
\end{equation}$$

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Show that the following integral

$$\begin{equation}
\int_0^\infty \frac{\sinh x}{x \cosh^3 x} \d x = \frac{7\zeta(3)}{\pi^2}
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer369')" class="answerButton">Show Answer</button> 
 <div  id='answer369' class="answer" >
Let us call the desired integral

$$\begin{equation}
J = \int_0^\infty \frac{\sinh x}{x \cosh^3 x} \d x
\end{equation}$$

First, we use the following identity for the Dirichlet eta function (see Wikipedia):

$$\begin{equation}
2^{1-s}\Gamma(s+1)\eta(s) = \int_0^\infty \frac{t^s}{\cosh^2 t} \d t
\end{equation}$$

Let us then define 

$$\begin{equation}
I(a,s) = \int_0^\infty \frac{t^s}{\cosh^2(at)} \d t = \frac{1}{a^{s+1}}\int_0^\infty \frac{t^s}{\cosh^2 t} \d t = \frac{2^{1-s}\Gamma(s+1)\eta(s)}{a^{s+1}}
\end{equation}$$

Then, we note that the derivative of \(I\) with respect to \(a\) is related to the original integral \(J\). We can see this as

$$\begin{equation}
\partial_a I(a,s) = -2\int_0^\infty \frac{t^{s+1}\sinh(at)}{\cosh^3(at)} \d t
\end{equation}$$

Finally, we define that \(J = J(1,-2)\), whereby

$$\begin{equation}
J(a,s) = -\frac{1}{2}\partial_a I(a,s)
\end{equation}$$

Taking the derivative of \(I\), we have that 

$$\begin{equation}
\partial_a I = -\frac{2^{1-s}(s+1)\Gamma(s+1)\eta(s)}{a^{s+2}}
\end{equation}$$

and using the identity \(\eta(s) = (1-2^{1-s})\eta(s)\), we get 

$$\begin{equation}
\partial_a I = -\frac{2^{1-s}(s+1)\Gamma(s+1)(1-2^{1-s})\zeta(s)}{a^{s+2}}
\end{equation}$$

We cannot substitute in \(\zeta(-2)\) because it is infinite, we can use the identity \(\zeta(s) = 2^s \pi^{s-1}\sin(\pi s/2)\Gamma(1-s)\zeta(1-s)\). Then we get 

$$\begin{equation}
\partial_a I = -\frac{2^{1-s}(s+1)\Gamma(s+1)(1-2^{1-s}) 2^s \pi^{s-1}\sin(\pi s/2)\Gamma(1-s)\zeta(1-s)}{a^{s+2}}
\end{equation}$$

so that 

$$\begin{equation}
J(a,s) = \frac{(s+1)\Gamma(s+1)(1-2^{1-s})\pi^{s-1}\sin(\pi s/2)\Gamma(1-s)\zeta(1-s)}{a^{s+2}}
\end{equation}$$

Then, using \(\Gamma(s+1) = s\Gamma(s)\), and then \(\Gamma(s)\Gamma(1-s) = \pi/\sin(\pi s)\), we get

$$\begin{equation}
J(a,s) = \frac{(s+1)s(1-2^{1-s})\pi^s\sin(\pi s/2)\zeta(1-s)}{\sin(\pi s)a^{s+2}}
\end{equation}$$

Finally, setting \(a = 1\), and taking the limit 

$$\begin{equation}
\lim_{s\to -2} \frac{\sin(\pi s/2)}{\sin(\pi s)} = -\frac{1}{2}
\end{equation}$$

we get 

$$\begin{equation}
J(1,-2) = (-1)(-2)(1-2^{3})\pi^{-2}\zeta(3)\left(-\frac{1}{2}\right) = \frac{7\zeta(3)}{\pi^2}
\end{equation}$$

Thus, we find that 

$$\begin{equation}
\int_0^\infty \frac{\sinh t}{t\cosh^3 t} \d t = \frac{7\zeta(3)}{\pi^2}
\end{equation}$$

</div> 
 </div>

</div> </li></ol>

\subsection{Ginzburg-Landau Theory in a Magnetic Field}
One could simply change derivatives, but we can also do this microscopically. This is instructive to do! We consider the Peierls phase 

\subsection{Project: Ginzburg-Landau superconductivity in the Repulsive Hubbard Model}

In this section, we will analyze the repulsive Hubbard model and look for a superconducting instability. We will explore different Hubbard-Stratonovich transformations, and see which of them may give a superconductor. The Hubbard model is given by 

$$\Hhat = -t\sum_{\langle i,j\rangle,\sigma} (\chat^\dagger_{i\sigma} \chat_{j\sigma}  + \hc)  - \mu\sum_{i\sigma} \nhat_{i\sigma} + U\sum_i \chat^\dagger_{i\uparrow} \chat^\dagger_{i\downarrow} \chat_{i\downarrow} \chat_{i\uparrow}$$

As a first step, show that the partition function can be written as 

$$\mathcal{Z} = \int e^{-S} \D\bar{c}\D c \D\Delta^* \D\Delta$$

where

$$S = \int_0^\beta \left[\sum_{\k\sigma} \bar{c}_{\k\tau\sigma}(\partial_\tau + \xi_{\k})c_{\k\tau\sigma} + \sum_i\left(\frac{\|\Delta_{i\tau}\|^2}{2U} + i(\Delta_{i\tau}\bar{c}_{i\tau\uparrow} \bar{c}_{i\tau\downarrow} + \Delta^*_{i\tau} c_{i\tau\downarrow} c_{i\tau\uparrow})\right)\right]\d\tau$$




Now, let us consider a more general Hubbard-Stratonovich transformation. We want to allow for the possibility of spin triplet pairing. To allow for this in the Hubbard model, we need a general 

