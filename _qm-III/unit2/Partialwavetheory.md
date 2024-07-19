---
layout: lesson
title: Partial wave theory 
dept: physics
course: qm-III
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics III
unitDisplay: Unit 2
---
Partial wave theory is concerned with decomposing the scattering wave functions into different angular momentum modes. For a spherically symmetric potential, the different angular momentum modes will all scatter independently, so we can look at each one separately. For a spherically symmetric potential, we start by rewriting the Schrödinger equation as a 1 dimensional problem with an effective potential \\(V\_\text{eff}\\). The Schrödinger equation for this situation is given by 

$$\begin{equation}
-\frac{\hbar^2}{2m}\nabla^2 \psi + V(\x)\psi = E\psi
\end{equation}$$

We assume that \\(V(\x) = V(r)\\) is spherically symmetric. Then, writing the Laplacian as 

$$\begin{equation}
\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta} \frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta} \frac{\partial^2}{\partial \varphi^2}
\end{equation}$$

We note that this can be related to the angular momentum operator because 

$$\begin{equation}
\mathbf{L}^2 = -\hbar^2\left(\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{\sin^2\theta}\frac{\partial^2}{\partial\varphi^2}\right)
\end{equation}$$

so that the Laplacian is 

$$\begin{equation}
\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) - \frac{1}{\hbar^2r^2}\mathbf{L}^2
\end{equation}$$

Then we can rewrite the Schrödinger equation as 

$$\begin{equation}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right)\psi + \frac{1}{2mr^2}\mathbf{L}^2\psi + V(r)\psi = E\psi
\end{equation}$$

Now, let us separate variables by setting \\(\psi(r,\theta,\varphi) = R(r)Y^m\_\ell(\theta,\varphi)\\). Doing this, we get 

$$\begin{align}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right)Y^m_\ell + \frac{R}{2mr^2}\mathbf{L}^2Y^m_\ell + V(r)RY^m_\ell ={}& ERY^m_\ell \\
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right)Y^m_\ell + \frac{R\hbar^2\ell(\ell+1)}{2mr^2}Y^m_\ell + V(r)RY^m_\ell ={}& ERY^m_\ell 
\end{align}$$

Now, we can divide both sides by \\(Y^m\_\ell\\), to get 

$$\begin{align}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + \left[\frac{\hbar^2\ell(\ell+1)}{2mr^2} + V(r)\right]R ={}& ER
\end{align}$$

This allows us to define the effective potential

$$\begin{equation}
V_\text{eff}(r) = \frac{\hbar^2\ell(\ell+1)}{2mr^2} + V(r)
\end{equation}$$

$$\begin{align}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + V_\text{eff}(r)R ={}& ER
\end{align}$$

Now, to simplify the equation, we set \\(R(r) = \frac{1}{r}u(r)\\), which gives us 

$$\begin{align}
r^2\frac{\partial R}{\partial r} ={}& r^2\left(-\frac{1}{r^2}u + \frac{1}{r}\frac{\partial u}{\partial r}\right) \\
={}& -u + r\frac{\partial u}{\partial r}
\end{align}$$

and taking one further derivative, we find 

$$\begin{align}
\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) ={}& \frac{\partial}{\partial r}\left(-u + r\frac{\partial u}{\partial r}\right)\\
={}& -\frac{\partial u}{\partial r} + \frac{\partial u}{\partial r} + r\frac{\partial^2 u}{\partial r^2}\\
={}& r\frac{\partial^2 u}{\partial r^2}
\end{align}$$

Thus, we find that 

$$\begin{align}
-\frac{\hbar^2}{2mr}\frac{\partial^2 u}{\partial r^2} + V_\text{eff}(r)\frac{u}{r} ={}& E\frac{u}{r} \\
-\frac{\hbar^2}{2m}\frac{\partial^2 u}{\partial r^2} + V_\text{eff}(r) u ={}& E u
\end{align}$$

We rearrange one more time to get 

$$\begin{align}
\frac{\partial^2 u}{\partial r^2} + \left(\frac{2m E}{\hbar^2} - \frac{2m V_\text{eff}(r)}{\hbar^2} \right)u ={}& 0
\end{align}$$

and then we let \\(k^2 = 2mE/\hbar^2\\), and label our eigenfunctions by \\(u\_{k\ell}\\)

$$\begin{align}
\frac{\partial^2 u_{k\ell}}{\partial r^2} + \left(k^2 - \frac{2m V_\text{eff}(r)}{\hbar^2} \right)u_{k\ell} ={}& 0
\end{align}$$

Now, in the limit \\(r\to\infty\\), we will find a simplified Schrödinger equation and solve for \\(u\\) in this limit. This will give us the scattering wave function. Now, let us take the limit \\(r\to\infty\\), which gives us \\(V\_\text{eff}(r) \to 0\\). Then, we solve for the approximate solution \\(\tilde{u}\\) to get 

$$\begin{align}
\frac{\partial^2 \tilde{u}_{k\ell}}{\partial r^2} + k^2\tilde{u}_{k\ell} ={}& 0
\end{align}$$

The solution to this is 

$$\begin{equation}
\tilde{u}_{k\ell} = Ae^{ikr} + Be^{-ikr}
\end{equation}$$


Now, keeping \\(r\\) dependence of the centrifugal term but removing the \\(V(r)\\) term, let's compute the wave function in the intermediate region. If we return to the original representation (\\(R\\) equation instead of \\(u\\) equation), then the equation is 

$$\begin{equation}
-\frac{\hbar^2}{2mr^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + \frac{\hbar^2\ell(\ell+1)}{2mr^2}R = ER
\end{equation}$$

Then, expanding this out and defining \\(k^2 = 2mE/\hbar^2\\), we have that 

$$\begin{equation}
-\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial R}{\partial r}\right) + \frac{\ell(\ell+1)}{r^2}R = k^2R
\end{equation}$$

Rearranging, we get 

$$\begin{equation}
r^2R" + 2rR' + (k^2r^2 - \ell(\ell+1))R = 0
\end{equation}$$

The solution to this is simply \\(R = j\_\ell(kr)\\) and \\(y\_\ell(kr)\\). These are the spherical Bessel functions of the first and second kind, respectively. The spherical Bessel function of the second kind is sometimes called a Neumann function. These functions can somewhat be intuited by looking at their asymptotic forms: 

$$\begin{equation}
j_\ell(kr) \sim \frac{1}{kr}\sin\left(kr - \frac{\ell\pi}{2}\right),\qquad y_\ell(kr) = -\frac{1}{kr}\cos\left(kr - \frac{\ell\pi}{2}\right)
\end{equation}$$

Thus, it makes sense to define the <i>Hankel functions</i>, which define incoming and outgoing waves by \\(h^{(1)}\_\ell(kr) = j\_\ell(kr) + iy\_\ell(kr)\\). These are analogous to writing \\(e^{ikr} = \cos(kr) + i\sin(kr)\\), which works because the sine and cosine are each superpositions of incoming and outgoing waves, so we can recover only the outgoing component. Then, we can write the radial solution in terms of incoming and outoging waves. We pick only the outgoing ones, and therefore get \\(R(kr) = h^{(1)}\_\ell(kr)\\). The outgoing wave function is then given by 

$$\begin{equation}
\psi = \sum_{\ell,m} c_{\ell,m} h^{(1)}_\ell(kr) Y^m_\ell(\theta,\varphi)
\end{equation}$$

We note that, because the scattering is symmetric about the \\(z\\) axis, that it should be independent of \\(\varphi\\). Then, we can assume that \\(m=0\\). If we assume this, then

$$\begin{equation}
Y^0_\ell(\theta,\varphi) = \sqrt{\frac{2\ell+1}{4\pi}} P_\ell(\cos\theta)
\end{equation}$$

and plugging this in, we define \\(c\_{\ell,0} = i^{\ell+1}k\sqrt{4\pi(2\ell+1)}a\_\ell\\). Then, the outgoing wave function is given by 

$$\begin{equation}
\psi = k\sum_{\ell=0}^\infty i^{\ell+1}(2\ell+1)a_\ell h^{(1)}_\ell(kr) P_\ell(\cos\theta)
\end{equation}$$

The total wave function is then given by 

$$\begin{equation}
\psi = A\left(e^{ikz} + k\sum_{\ell=0}^\infty i^{\ell+1}(2\ell+1)a_\ell h^{(1)}_\ell(kr) P_\ell(\cos\theta)\right)
\end{equation}$$

Note that the Hankel function has the asymptotic form 

$$\begin{equation}
h^{(1)}_\ell(kr) \sim (-i)^{\ell+1}\frac{e^{ikr}}{r},\qquad kr\gg 1
\end{equation}$$

which gives the outgoing wave to be 

$$\begin{equation}
\psi = f(\theta) \frac{e^{ikr}}{r}, \qquad f(\theta) = \sum_{\ell=0}^\infty a_\ell (2\ell+1)P_\ell(\cos\theta)
\end{equation}$$

Thus, the total ingoing and outgoing wave function in the radiation zone is 

$$\begin{equation}
\psi = A\left(e^{ikz} + f(\theta)\frac{e^{ikr}}{r}\right)
\end{equation}$$

Now, returning to the full wave function, we note that we have done things in terms of plane waves and also spherical waves. Then, we can use Rayleigh's formula which we proved last week:

$$\begin{equation}
e^{ikz} = \sum_{\ell=0}^\infty i^\ell (2\ell+1)j_\ell(kr) P_\ell(\cos\theta)
\end{equation}$$

and thus find the wave function to be 

$$\begin{equation}
\psi = A\sum_{\ell=0}^\infty i^\ell(2\ell+1)\left[j_\ell(kr) + ika_\ell h^{(1)}_\ell(kr)\right]P_\ell(\cos\theta)
\end{equation}$$

The coefficient \\(a\_\ell\\) is called a partial wave amplitude. 

<div class="example">
<b>Example:</b>
Compute the partial wave amplitudes for the potential 

$$\begin{equation}
V(r) = \begin{cases}
\infty & r \leq a \\
0 & r > a
\end{cases}
\end{equation}$$

<b>Solution:</b> The boundary condition for this is \(\psi(a,\theta)\). Thus, if we take the wave function

$$\begin{equation}
\psi(a,\theta) = \sum_{\ell=0}^\infty i^\ell(2\ell+1)\left[j_\ell(ka) + ika_\ell h^{(1)}_\ell(ka)\right] P_\ell(\cos\theta) = 0
\end{equation}$$

Since this should hold for all \(\ell\), we have that 

$$\begin{equation}
j_\ell(ka) + ika_\ell h^{(1)}_\ell(ka) = 0 \rightarrow a_\ell = \frac{ij_\ell(ja)}{kh^{(1)}_\ell(ka)}
\end{equation}$$

The scattering cross section is given by the following (this was derived in class). A quick reminder is the following. We have \(\d N = I\d\sigma\). Since 

$$\begin{equation}
I = \frac{\#\text{particles}}{\text{unit area} \times \text{unit time}}
\end{equation}$$

and we have that \([\mathbf{J}] = 1/\text{m}^2\text{s}\) (particles per unit area per second), we have that simply \(I = \mathbf{J}_\text{inc}\cdot\zhat\). We also have that the number of particles passing through an outgoing area is given by 

$$\begin{equation}
\d N = \frac{\#\text{particles}}{\text{unit time}}
\end{equation}$$

Thus to get this, we need to take the outgoing probability current and multiply by the area that it is going through to get 

$$\begin{equation}
\d N = \mathbf{J}_\text{out}\cdot\hat{r} (r^2\d\Omega)
\end{equation}$$

Thus, computing each of these for \(\psi_\text{inc} = Ae^{ikz}\), and \(\psi_\text{out} = A\frac{e^{ikr}}{r}f(\theta)\), we have that \(I = \frac{\hbar}{m}|A|^2 k\zhat\), and also 

$$\begin{equation}
\mathbf{J}_\text{out} = \frac{\hbar|A|^2}{m}\frac{|f(\theta)|^2}{r^2} \nabla(kr) = \frac{\hbar|A|^2}{m}\frac{|f(\theta)|^2}{r^2}\hat{r} k
\end{equation}$$

which gives us 

$$\begin{equation}
\d N = \frac{\hbar}{m}|A|^2|f(\theta)|^2k\d\Omega
\end{equation}$$

and combining these two to get 

$$\begin{equation}
\frac{\hbar|A|^2}{m}|f(\theta)|^2 k \d\Omega = \frac{\hbar}{m}|A|^2 k \d\sigma
\end{equation}$$

we find that the <i>differential scattering cross section</i> is

$$\begin{equation}
D(\theta) = |f(\theta)|^2 = \frac{\d\sigma}{\d\Omega}
\end{equation}$$

where 

$$\begin{equation}
f(\theta) = \sum_{\ell=0}^\infty (2\ell+1)a_\ell P_\ell(\cos\theta)
\end{equation}$$

so that 

$$\begin{align}
\sigma {}&= \int\sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* P_\ell(\cos\theta) P_{\ell'}(\cos\theta) \d\Omega \\
={}& \int_0^\pi \int_0^{2\pi} \sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* P_\ell(\cos\theta) P_{\ell'}(\cos\theta) \sin\theta\d\varphi\d\theta\\
={}& 2\pi \int_{-1}^1  \sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* P_\ell(x) P_{\ell'}(x) x\d x
\end{align}$$

Using the orthogonality relation 

$$\begin{equation}
\int_{-1}^1 P_\ell(x) P_{\ell'}(x) \d x = \frac{2}{2\ell+1} \delta_{\ell\ell'}
\end{equation}$$

we find 

$$\begin{align}
\sigma ={}& 2\pi \int_{-1}^1  \sum_{\ell\ell'} (2\ell+1)(2\ell'+1)a_\ell a_{\ell'}^* \frac{2\delta_{\ell\ell'}}{2\ell+1} \\
={}& 4\pi \sum_{\ell} (2\ell+1)|a_\ell|^2 \\
={}& 4\pi \sum_{\ell=0}^\infty (2\ell+1)\left|\frac{j_\ell(ka)}{kh^{(1)}_\ell(kr)}\right|^2
\end{align}$$

To get some intuition for this, let's consider the limit \(ka \ll 1\) (the low energy limit) so that the series will converge quickly. This allows us to use the asymptotic forms 

$$\begin{equation}
j_\ell(z) \sim \frac{z^\ell 2^\ell \ell!}{(2\ell+1)(2\ell)!},\qquad y_\ell(z) \sim -\frac{(2\ell)!}{z^{\ell+1}2^\ell \ell!},\qquad z\to 0
\end{equation}$$

which means that 

$$\begin{align}
\sigma ={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty (2\ell+1)\left|\frac{j_\ell(ka)}{j_\ell(ka) + iy_\ell(ka)}\right|^2 \\
={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty (2\ell+1)\left|\frac{j_\ell(ka)}{y_\ell(ka)}\right|^2 \\
={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty (2\ell+1)\left|\frac{z^{2\ell+1}(\ell!)^2 2^{2\ell}}{(2\ell+1)(2\ell)!^2}\right|^2 \\
={}& \frac{4\pi}{k^2} \sum_{\ell=0}^\infty \frac{(ka)^{4\ell+2}}{2\ell+1} \left(\frac{\ell! 2^\ell}{(2\ell)!}\right)^4 \\
={}& 4\pi a^2
\end{align}$$

which is 4 times the classical cross section of a sphere of radius \(a\). 


</div>


