---
layout: lesson
title: Cooper instability 
dept: physics
course: superconductivity
unit: unit4
deptDisplay: Physics
courseDisplay: Superconductivity & Superfluidity
unitDisplay: Unit 4
---
In the previous section, we showed that, for a bound state to occur, the potential must be attractive in at least one angular momentum mode. This was done for two particles in a vacuum. In this section, we will show that any infinitesimally small interaction can lead to a bound state if there are other particles around. To do this, we note that now that \\(\k\\) below \\(k\_F\\) should already be filled up, and therefore \\(\epsilon\_{\k}\\) should be measured from \\(\epsilon\_F\\). 

Let us now reintroduce the Fermi sea of other (noninteracting) electrons. The pair of electrons whose equation we investigated in the previous section are now moving in the presence of this Fermi sea. Suppose that the centre of mass momentum \\(\mathbf{K}\\) is zero. Then, based on the above calculation, we have that \\(\k\_1 = \k\\) and \\(\k\_2 = -\k\\). Furthermore, since we are assuming that the Fermi sea exists, and that the attraction between electrons happens between the two additional electrons, these two additional electrons must have wave vectors which are slightly larger than the Fermi surface. Thus, they have wave vectors \\(\k\_1\\) and \\(\k\_2\\) satisfying \\(\|\k\_1\| > k\_F\\) and \\(\|\k\_2\| > k\_F\\). This implies that \\(\|\k\| = k > k\_F\\), or, the probability of having a \\(k < k\_F\\) is zero. Thus, 

$$\begin{equation}
\phi_{\ell m}(k) = \theta(k - k_F)\phi_{\ell m}(k)
\end{equation}$$

where \\(\theta(x)\\) is the Heaviside function (\\(\theta(x) = 1\\) if \\(x > 0\\), and \\(\theta(x) = 0\\) if \\(x<0\\)). We start with the equation from the end of the previous section:

$$\begin{equation}
(2\epsilon_k - \tilde{E})\phi_{\ell m}(k) = -\frac{1}{(2\pi)^3}\int V_\ell(k,k') \phi_{\ell m}(k') (4\pi) k^{\prime 2} \d k'
\end{equation}$$

Dividing both sides by \\(2\epsilon\_k - \tilde{E}\\), and also multiplying both sides by \\(k^2\\), we get 

$$\begin{equation}
\phi_{\ell m}(k)k^2 = -\frac{1}{(2\pi)^3}\int \frac{V_\ell(k,k') \phi_{\ell m}(k')}{2\epsilon_k - \tilde{E}} (4\pi) k^{\prime 2} k^2 \d k'
\end{equation}$$

Now integrating both sides over \\(k\\), we get 

$$\begin{equation}
\int \phi_{\ell m}(k) k^2 \d k= -\frac{1}{(2\pi)^3}\int \frac{V_\ell(k,k') \phi_{\ell m}(k')}{2\epsilon_k - \tilde{E}} (4\pi) k^{\prime 2} k^2 \d k' \d k
\end{equation}$$

Swapping the \\(k,k'\\) variables on the right hand side, we get 

$$\begin{equation}
\int \phi_{\ell m}(k) k^2\d k= -\frac{\V}{(2\pi)^3}\int \frac{V_\ell(k',k) \phi_{\ell m}(k)}{2\epsilon_{k'} - \tilde{E}} (4\pi) k^2 k^{\prime 2} \d k' \d k
\end{equation}$$

Now moving everything to one side, we get 

$$\begin{equation}
0= \int \left(1 + \int \frac{V_\ell(k',k)}{2\epsilon_{k'} - \tilde{E}} \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3}\right)  \phi_{\ell m}(k)k^2 \d k
\end{equation}$$

Since this is obviously zero for \\(k < k\_F\\) (because \\(\phi\_{\ell m}(k) = 0\\) there), we set that, for any \\(k > k\_F\\),

$$\begin{equation}
1 + \int \frac{V_\ell(k',k)}{2\epsilon_{k'} - \tilde{E}} \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3} = 0.
\end{equation}$$

This allows \\(\phi\_{\ell m}(k)\\) to be nontrivial for \\(k > k\_F\\)! Next, let's assume that the interaction to be attractive in some particular angular momentum channel \\(\ell\\), and assume, for some \\(\lambda\_\ell > 0\\), that

$$\begin{equation}
V_\ell(k,k') = \begin{cases} -\lambda_\ell & \epsilon_F < \frac{\hbar^2k^2}{2m},\frac{\hbar^2k^{\prime 2}}{2m} < \epsilon_F + D \\ 0 & \text{else} \end{cases}.
\end{equation}$$

We rewrite the equation of the previous part 

$$\begin{equation}
1 = - \int \frac{V_\ell(k',k)}{2\epsilon_{k'} - \tilde{E}} \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3} 
\end{equation}$$

which we see can be simplified by plugging in our specific potential. This gives us 

$$\begin{equation}
1 =  \lambda_\ell \int_{k_F}^{k_c} \frac{1}{2\epsilon_{k'} - \tilde{E}} \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3}
\end{equation}$$

where \\(k\_c = \sqrt{2m(\epsilon\_F + D)}/\hbar\\) is the wave vector at the cutoff energy. Next, we plug in the density of states (here \\(\V\\) is the volume of the system, and \\(\epsilon\_{\k} = \hbar^2\k^2/2m\\))

$$\begin{equation}
\rho(\epsilon) = \frac{1}{\V}\sum_{\k} \delta(\epsilon - \epsilon_{\k}) = \int \delta(\epsilon - \epsilon_{\k}) \frac{\d^3\k}{(2\pi)^3} = \int \delta(\epsilon - \epsilon_k) \frac{4\pi k^2\d k}{(2\pi)^3}
\end{equation}$$

which we can do because 

$$\begin{equation}
\int_{-\infty}^\infty \delta(\epsilon - \epsilon_{\k}) \d\epsilon = 1
\end{equation}$$

This gives us 

$$\begin{align}
1 ={}&  \lambda_\ell \int_{-\infty}^\infty \int_{k_F}^{k_c} \frac{1}{2\epsilon_{k'} - \tilde{E}} \delta(\epsilon - \epsilon_{k'}) \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3} \d\epsilon 
\end{align}$$

We can rewrite this by introducing the functions \\(\theta(k\_c - k)\theta(k - k\_F)\\), which gives us 

$$\begin{align}
1 ={}&  \lambda_\ell \int_{-\infty}^\infty \int_0^\infty \frac{\theta(k_c-k)\theta(k-k_F)}{2\epsilon - \tilde{E}} \delta(\epsilon - \epsilon_{k'}) \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3} \d\epsilon 
\end{align}$$

We can't quite introduce the density of states yet, but if we note that the \\(\theta\\) functions can be rewritten as \\(\theta(k\_c - k) = \theta(\epsilon\_F + D - \epsilon)\\) and \\(\theta(k-k\_F) = \theta(\epsilon - \epsilon\_F)\\), we have 

$$\begin{align}
1 ={}& \lambda_\ell \int_{-\infty}^\infty \int_0^\infty \frac{\theta(\epsilon_F + D - \epsilon)\theta(\epsilon - \epsilon_F)}{2\epsilon_{k'} - \tilde{E}} \delta(\epsilon - \epsilon_{k'}) \frac{4\pi k^{\prime 2} \d k'}{(2\pi)^3} \d\epsilon \\
={}& \lambda_\ell  \int_{-\infty}^\infty \frac{\theta(\epsilon_F + D - \epsilon)\theta(\epsilon - \epsilon_F)}{2\epsilon - \tilde{E}} \rho(\epsilon) \d\epsilon \\
={}& \lambda_\ell \int_{\epsilon_F}^{\epsilon_F + D} \frac{1}{2\epsilon - \tilde{E}} \rho(\epsilon) \d\epsilon
\end{align}$$

Next, we assume that the density of states is roughly constant over the given region of integration \\(\rho(\epsilon) \approx \rho(\epsilon\_F)\\), and then we can evaluate the integral 

$$\begin{align}
1 ={}& \lambda_\ell \rho(\epsilon_F) \int_{\epsilon_F}^{\epsilon_{F}+D} \frac{1}{2\epsilon - \tilde{E}} \d\epsilon \\
={}& \frac{\lambda_\ell \rho(\epsilon_F)}{2}\log(2\epsilon - \tilde{E})\bigg|_{\epsilon_F}^{\epsilon_F+D} \\
={}& \frac{\lambda_\ell \rho(\epsilon_F)}{2}\log\left(\frac{2\epsilon_F + 2D - \tilde{E}}{2\epsilon_F - \tilde{E}}\right) 
\end{align}$$

Next defining \\(\Delta = 2\epsilon\_F - \tilde{E}\\), we get 

$$\begin{align}
e^{2/\lambda_\ell \rho(\epsilon_F)} ={}& \frac{\Delta + 2D}{\Delta}
\end{align}$$

which we can rearrange to get 
$$\begin{equation}
\Delta = \frac{-2D}{1 - e^{2/\lambda_\ell\rho(\epsilon_F)}} = 2D\frac{e^{-2/ \lambda_\ell\rho(\epsilon_F)}}{1 - e^{-2/\lambda_\ell \rho(\epsilon_F)}} \approx  2De^{-2/ \lambda_\ell\rho(\epsilon_F)}
\end{equation}$$

It is important that \\(\tilde{E} < 2\epsilon\_F\\) because, in the absence of interaction \\(\lambda\_\ell = 0\\), the pair of electrons would have no interaction energy, only kinetic energy. The fact that the interaction is attractive allows them to decrease their energy, and subsequently form a bound state. Also note that any \\(\lambda\_\ell > 0\\) allows the formation of a bound state. It does not have to be stronger than some threshold. This is a consequence of the background Fermi sea. Note that the final equality (or rather approximation) is the <i>weak coupling</i> limit, where \\(\lambda\_\ell\\) is small.

