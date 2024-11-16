---
layout: lesson
title: Tight-binding model 
dept: physics
course: cmp-I
unit: unit4
deptDisplay: Physics
courseDisplay: Condensed Matter Physics I
unitDisplay: Unit 4
---
The tight-binding model considers a system for which the electrons are tightly bound to their atoms. The implications of this is that, even when the electron wave functions on nearby sites overlap, the overlap is not that large, so the resulting localized wave functions closely resemble their atomic constituents. We can derive the energy eigenvalues of such a situation in the following way. We start by considering an isolated atom centred at the origin. The atom has numerous energy levels \\(E\_n\\), which may be localized eigenfunctions, or scattering states. The scattering states are <i>not</i> considered. The localized eigenfunctions can be thought of as the wave functions of a hydrogen atom, although these wave functions will of course be modified in the presence of other nuclei, as well as interactions with electrons from other shells. Let us ignore the interactions between electrons on the particular atom, as well as the interactions between electrons on different atoms. This means that we can consider a single-particle Schrödinger equation. The single-particle Schrödinger equation for an atom is given by 

$$\begin{equation}
\Hhat_\text{at}\psi_n(\x) = E_n \psi_n(\x).
\end{equation}$$

The most general atomic wave function is given by a generic superposition of all of the different localized orbitals:

$$\begin{equation}
\phi(\x) = \sum_n b_n \psi_n(\x). \label{eq:general_on_site_atomic_wf}
\end{equation}$$

Suppose we now have a lattice made of up atoms at positions \\(\mathbf{R}\_i\\) in a Bravais lattice. How can we write a general atomic wave function for an electron which is localized about an atom on site \\(\mathbf{R}\_i\\), rather than the origin? Well, we simply have to shift the wave function which we had at the origin to now be centred about site \\(i\\). The general atomic wave function localized on site \\(i\\) would be \\(\phi\_i(\x) = \phi(\x-\mathbf{R}\_i)\\). Can we construct a Bloch wave function out of these localized orbitals? Well, the answer is yes. The only condition that our Bloch function must satisfy is \\(\Psi(\x + \mathbf{R}) = e^{i\k\cdot\mathbf{R}}\Psi(\x)\\), for any Bravais lattice vector \\(\mathbf{R}\\). With the big picture in mind, we can now proceed with the analysis.

The potential for a lattice is given by

$$\begin{equation}
U(\x) = \sum_{i=1}^N U_\text{loc}(\x-\mathbf{R}_i),
\end{equation}$$

where \\(U\_\text{loc}(\x - \mathbf{R}\_i)\\) is the potential due to the atom at site \\(i\\). Thus, the Hamiltonian for a crystal can be written in terms of the atomic Hamiltonian (which includes the potential due to the atom at the origin), plus the potential due to all of the other atoms. Thus, the Hamiltonian for a crystal can be written as 

$$\begin{equation}
\Hhat = \Hhat_\text{at} + \Delta U(\hat{\x})
\end{equation}$$

where the atomic part includes the kinetic energy and the potential of the atom centred at \\(\x=0\\), which we remind the reader is given by

$$\begin{equation}
\Hhat_\text{at} = \frac{\hat{\p}^2}{2m} + U_\text{loc}(\hat{\x}).
\end{equation}$$

The other part of the lattice Hamiltonian considers the potential due to the atoms at all other lattice sites, given by

$$\begin{equation}
\Delta U(\x) = \sum_{i\neq0} U(\x - \mathbf{R}_i).
\end{equation}$$

Assume that we have solved the atomic problem 

$$\begin{equation}
\Hhat_\text{at}\psi_n = E_n \psi_n.
\end{equation}$$

Each of these \\(\psi\_n(\x)\\) wave functions will be centred at \\(\x = 0\\). Now, in order to construct a wave function for the whole lattice, let us consider a superposition of these atomic wave functions, by adding together one centred at each lattice site. To do this, let us define a ``Bloch" wave function for the orbital \\(n\\), which is given by something resembling a Fourier transform, given by

$$\begin{equation}
\psi_{n\k}(\x) = \sum_i e^{i\k\cdot\mathbf{R}_i} \psi_n(\x-\mathbf{R}_i).
\end{equation}$$

This will be our guess for the wave function in the whole lattice. Note that, for this to be a reasonable guess, it should satisfy Bloch's theorem. If we check Bloch's theorem, then we have that

$$\begin{equation}
\psi_{n\k}(\x + \mathbf{R}) = \sum_i e^{i\k\cdot\mathbf{R}_i} \psi_n(\x + \mathbf{R} - \mathbf{R}_i).
\end{equation}$$

Then, we perform a change of variables \\(\mathbf{R}\_j = \mathbf{R}\_i - \mathbf{R}\\). Thus, we get 

$$\begin{align}
\psi_{n\k}(\x + \mathbf{R}) ={}& \sum_i e^{i\k\cdot(\mathbf{R}_j + \mathbf{R})} \psi_n(\x - \mathbf{R}_j) \\
={}& e^{i\k\cdot\mathbf{R}} \sum_i e^{i\k\cdot\mathbf{R}_j} \psi_n(\x - \mathbf{R}_j) \\
={}& e^{i\k\cdot\mathbf{R}}\psi_{n\k}(\x).
\end{align}$$

Thus, the guess satisfies Bloch's theorem with wave vector \\(\k\\). This is good progress, but it is not useful if wave functions with different \\(n\\) (so, different orbitals) on different sites overlap. Thus, instead of considering a superposition of only the \\(n\\)th orbital from different sites, we consider the most general atomic wave function, but superposed over different sites. We define this by

$$\begin{equation}
\psi_{\k}(\x) = \sum_i e^{i\k\cdot\mathbf{R}_i} \phi(\x - \mathbf{R}_i)
\end{equation}$$

where \\(\phi(\x)\\) is the most general wave function centred at \\(\x=0\\) (see Eq.\eqref{eq:general\_on\_site\_atomic\_wf}). Since \\(\phi(\x)\\) is the most general atomic function, we expand it in terms of the atomic orbitals \\(\psi\_n(\x)\\). Then, we get 

$$\begin{equation}
\phi(\x) = \sum_n b_n \psi_n(\x). \label{eq:general_atomic_bloch}
\end{equation}$$

Let's plug our wave function into the full Scrödinger equation

$$\begin{align}
\Hhat \psi_{\k}(\x) ={}& \epsilon(\k)\psi_{\k}(\x) \\
={}& (\Hhat_\text{at} + \Delta U(\x))\psi_{\k}(\x).
\end{align}$$

Then, let's multiply both sides by the \\(m\\)th orbital wave function centred at \\(\x = 0\\), and then integrate. This gives us 

$$\begin{align}
\int \psi^{*}_m(\x)\epsilon(\k) \psi_{\k}(\x) \d^3\x ={}& \int \psi^{*}_m(\x) (\Hhat_\text{at} + \Delta U(\x))\psi_{\k}(\x) \d^3\x \\
={}&  \int \psi^{*}_m(\x) \Hhat_\text{at}\psi_{\k}(\x) \d^3\x + \int \psi^{*}_m(\x) \Delta U(\x)\psi_{\k}(\x) \d^3\x 
\end{align}$$

Since \\(\psi\_m^{\*}(\x)\Hhat\_\text{at} = \psi\_m^{\*}(\x)E\_m\\) (where \\(E\_m\\) is the \\(m\\)th energy level of the on-site energy), this simplifies a bit to get 

$$\begin{equation}
(\epsilon(\k) - E_m)\int \psi^{*}_m(\x) \psi_{\k}(\x) \d^3\x = \int \psi^{*}_m(\x)\Delta U(\x) \psi_{\k}(\x) \d^3\x.
\end{equation}$$

Then, we substitute in the form of \\(\psi\_{\k}(\x)\\), which gives us 

$$\begin{align}
(\epsilon(\k) - E_m)\sum_i e^{i\k\cdot\mathbf{R}_i} \int \psi^{*}_m(\x) \phi(\x - \mathbf{R}_i) \d^3\x =\sum_i e^{i\k\cdot\mathbf{R}_i}  \int \psi^{*}_m(\x)\Delta U(\x) \phi(\x - \mathbf{R}_i)\d^3\x
\end{align}$$

Then, we plug in the form of \\(\phi(\x - \mathbf{R}\_i)\\), given by Eq.~\eqref{eq:general\_atomic\_bloch}, which gives us 

$$\begin{align}
(\epsilon(\k) - E_m)\sum_{in} b_n e^{i\k\cdot\mathbf{R}_i} \int \psi^{*}_m(\x) \psi_n(\x - \mathbf{R}_i) \d^3\x =\sum_{in} b_n e^{i\k\cdot\mathbf{R}_i}  \int \psi^{*}_m(\x)\Delta U(\x) \psi_n(\x - \mathbf{R}_i)\d^3\x
\end{align}$$

Next, we separate the sum over sites into the \\(\mathbf{R}\_i = 0\\) site and the rest. We get 

$$\begin{align}
(\epsilon(\k) - E_m)&\left[\sum_{n} b_n \int \psi^{*}_m(\x) \psi_n(\x) \d^3\x + \sum_{i\neq0; n} b_n e^{i\k\cdot\mathbf{R}_i} \int \psi^{*}_m(\x) \psi_n(\x - \mathbf{R}_i) \d^3\x\right] \\
={}&\sum_{n} b_n  \int \psi^{*}_m(\x)\Delta U(\x) \psi_n(\x)\d^3\x + \sum_{i\neq0; n} b_n e^{i\k\cdot\mathbf{R}_i}  \int \psi^{*}_m(\x)\Delta U(\x) \psi_n(\x - \mathbf{R}_i)\d^3\x
\end{align}$$

Then, since, on a single site, \\(\int \psi^{\*}\_m(\x) \psi\_n(\x) \d^3\x = \delta\_{mn}\\), this simplifies a little bit to be

$$\begin{align}
(\epsilon(\k) - E_m)b_m ={}& -(\epsilon(\k) - E_m)\sum_{i\neq0; n} b_n e^{i\k\cdot\mathbf{R}_i} \int \psi^{*}_m(\x) \psi_n(\x - \mathbf{R}_i) \d^3\x \\
&+\sum_{n} b_n  \int \psi^{*}_m(\x)\Delta U(\x) \psi_n(\x)\d^3\x + \sum_{i\neq0; n} b_n e^{i\k\cdot\mathbf{R}_i}  \int \psi^{*}_m(\x)\Delta U(\x) \psi_n(\x - \mathbf{R}_i)\d^3\x
\end{align}$$

The integral \\(\int \psi^{\*}\_m(\x) \psi\_n(\x - \mathbf{R}\_i) \d^3\x\\) is assumed to be small because we assumed the wave functions are well localized, so they do not overlap very much. Furthermore, the integrals \\( \int \psi^{\*}\_m(\x)\Delta U(\x) \psi\_n(\x - \mathbf{R}\_i)\d^3\x\\) are small for the same reason. Lastly, the integrals \\(\int \psi^{\*}\_m(\x)\Delta U(\x) \psi\_n(\x)\d^3\x\\) are small because \\(\Delta U(\x)\\) is small around \\(\x = 0\\), but \\(\psi\_n,\psi^{\*}\_m\\) are small where \\(\Delta U\\) is larger. Thus, we conclude that the left hand side is also small. Thus, there are two cases:

<ul>
<li> If, for a particular \(m\), \(b_m\) is not small, then \((\epsilon(\k) - E_m)\) is small. This is the case where \(\epsilon(\k)\) should be close to the atomic level \(E_m\). Since \(\sum_m |b_m|^2 = 1\) (the atomic wave function should be normalized), the other \(b_n\) (for \(n\neq m\)) should be small. This tells us that \(\epsilon(\k) \sim E_m\) for the particular \(m\), and \(b_n \approx 0\) if \(n\neq m\).
</li>
<li> If \(\epsilon(\k) - E_m\) is not small, then \(b_m\) is small. The implications of this are the same as the previous case!
</li></ul>

Now, let us use these results to determine the dispersion relation for some simple examples. 

<div class="example">
<b>Example:</b>
Consider the  case of a single \(s\)-orbital. Defining

$$\begin{align}
\beta ={}& -\int \Delta U(\x) |\psi_s(\x)|^2 \d^3\x \\
\alpha ={}& \int \psi_s^*(\x) \psi_s(\x-\mathbf{R}_i) \d^3\x \\
\gamma ={}& -\int \psi_s^*(\x) \Delta U(\x) \psi_s(\x-\mathbf{R}_i) \d^3\x
\end{align}$$

find the band structure on 

<ol type="a">
<li> A square lattice, using only nearest neighbour wave function overlap
</li>
<li> A triangular lattice, using only nearest neighbour wave function overlap
</li></ol>

In both parts, explain the approximations used.


<b>Solution:</b> If we have a single \(s\)-orbital, then this implies that all \(b\) coefficients are zero, except for the one corresponding to the \(s\) orbital. In this case, then we have 

$$\begin{align}
(\epsilon(\k) - E_s)b_s ={}& -(\epsilon(\k) - E_s)\sum_{i\neq 0}b_s e^{i\k\cdot\mathbf{R}_i} \int \psi^*_s(\x) \psi_s(\x-\mathbf{R}_i) \d^3\x \\
&+ b_s \int \psi^*_s(\x)\Delta U \psi_s(\x) \d^3\x + \sum_{i\neq 0}b_s e^{i\k\cdot\mathbf{R}_i}\int \psi^*_s(\x) \Delta U(\x) \psi_s(\x-\mathbf{R}_i)\d^3\x
\end{align}$$

Then only keeping nearest neighbour interactions, we get 

$$\begin{align}
\epsilon(\k) - E_s ={}& -(\epsilon(\k) - E_s)\sum_{i\in \text{n.n}} e^{i\k\cdot\mathbf{R}_i} \alpha_i - \beta - \sum_{i\in \text{n.n}} e^{i\k\cdot\mathbf{R}_i}\gamma_i
\end{align}$$

Then, solving for \(\epsilon(\k)\), we get 

$$\begin{equation}
\epsilon(\k) = E_s - \frac{\beta + \sum_{i\in \text{n.n}} e^{i\k\cdot\mathbf{R}_i} \gamma}{1 + \sum_{i\in \text{n.n}} e^{i\k\cdot\mathbf{R}_i} \alpha}
\end{equation}$$

The \(\alpha\) terms are small, and if we Taylor expand them, then they only correct the numerator by a small amount, so we ignore them to get 

$$\begin{equation}
\epsilon(\k) = E_s - \beta - \sum_{i\in \text{n.n}} e^{i\k\cdot\mathbf{R}_i} \gamma
\end{equation}$$

<ol type="a">
<li> Now, applying the result of above, we sum over the nearest neighbours. The nearest neighbours are \(\mathbf{a}_1 = (a,0)\) and \(\mathbf{a}_2 = (0,a)\). Thus, we find 

$$\begin{align}
\epsilon(\k) ={}& E_s - \beta - \gamma(e^{ik_xa} + e^{-ik_xa} + e^{ik_ya} + e^{-ik_ya}) \\
={}& E_s - \beta - 2\gamma(\cos(k_x a) + \cos(k_y a)) 
\end{align}$$

</li>
<li> This time, the nearest neighbours are \(\mathbf{a}_1 = (a,0)\), \(\mathbf{a}_2 = a(\frac{1}{2},\frac{\sqrt{3}}{2})\), and \(\mathbf{a}_3 = a(-\frac{1}{2},\frac{\sqrt{3}}{2})\). Then, we find 

$$\begin{align}
\epsilon(\k) ={}& E_s - \beta - \gamma(e^{ik_xa} + e^{-ik_xa} + e^{ia(k_x + \sqrt{3}k_y)/2} + e^{-ia(k_x + \sqrt{3}k_y)/2} + e^{ia(-k_x + \sqrt{3}k_y)/2} + e^{-ia(-k_x + \sqrt{3}k_y)/2}) \\
={}& E_s - \beta - 2\gamma\left[\cos(k_x a) + \cos\left(a\left(\frac{k_x}{2} + \frac{\sqrt{3}k_y}{2}\right)\right) + \cos\left(a\left(-\frac{k_x}{2} + \frac{\sqrt{3}k_y}{2}\right)\right)\right]
\end{align}$$
</li></ol>

</div>







### Wannier functions

We have seen that it is possible to approximate the wave function of an electron by 



Consider the tight binding model 

$$\begin{equation}
\Hhat = -t\sum_{\left<i,j\right>} \chat^\dagger_i \chat_j
\end{equation}$$

We now consider a multiorbital tight-binding model. This means that we will have two kinds of creation/annihilation operators. 

$$\begin{equation}
\Hhat =  -\sum_{\left<i,j\right>}\sum_{a,b} t_{ab}\chat^\dagger_{ia} \chat_{jb}
\end{equation}$$

where now we consider hopping between the two orbitals  

<div class="example">
<b>Example:</b>
Consider the following tight-binding model on the square lattice. 

</div>


