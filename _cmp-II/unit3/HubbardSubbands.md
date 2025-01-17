---
layout: lesson
title: Hubbard Subbands 
dept: physics
course: cmp-II
unit: unit3
deptDisplay: Physics
courseDisplay: Condensed Matter Physics II
unitDisplay: Unit 3
---

<ol>
<li> <div class="exercise">  Consider the spectral function \(A(\omega)\) of the Hubbard model

\(\)\Hhat = -t\sum_{\langle i,j\rangle;\sigma} (\chat^\dagger_{i\sigma} \chat_{j\sigma} + \hc) - \epsilon_\text{at} \sum_{i\sigma} \nhat_{i\sigma} + U \sum_i \nhat_{i\uparrow} \nhat_{i\downarrow} \(\)

on the hypercubic lattice of dimension \(d\). Note that the coordination number is \(z=2d\) for this system. Recall that the spectral function is defined by

\(\)A(\k,\omega) = -2\Im G^R(\k,\omega)\(\)

and the density of states is \(\rho(\omega) = \frac{1}{N_s}\sum_{\k} A(\k,\omega)\). Then, 

<ol type="a">
<li> In the case \(t = 0\), compute the Matsubara Green function of the system.
</li>
<li> Compute the density of states for the case when \(t = 0\). Plot the result.
 </li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer18')" class="answerButton">Show Answer</button> 
 <div  id='answer18' class="answer" >
<ol type="a">
<li> First, we need to compute the Matsubara Green function

\(\)\mathcal{G}(i,\tau;j) = -\langle T_\tau[ \chat_{i\sigma}(\tau)\chat^\dagger_{j\sigma}]\rangle = -\frac{1}{\langle \Uhat_I(\beta,0)\rangle_0}\langle T_\tau[ \Uhat_I(\beta,0)\chat_{i\sigma}(\tau)\chat^\dagger_{j\sigma}]\rangle_0\(\)

where 

\(\)\Hhat_0 = U\sum_i \nhat_{i\uparrow} \nhat_{i\downarrow} + (-\epsilon_\text{at} - \mu)\sum_{i\sigma} \nhat_{i\sigma}\(\)

Next, we need to compute the time-evolution of \(\chat_{i\sigma}\) with respect to the local Hamiltonian. To do this, we need to compute the commutator 

\(\)[\nhat_{j\sigma'},\chat_{i\sigma}] = -\delta_{\sigma\sigma'}\delta_{ij}\chat_{i\sigma}\(\)

This tells us that (letting \(\xi_\text{at} = -\epsilon_{at} - \mu\))

$$\begin{align}
[\Hhat_0,\chat_{i\sigma}] ={}& U\sum_j [\nhat_{j\uparrow}\nhat_{j\downarrow}, \chat_{i\sigma}] + \xi_\text{at}\sum_{j\sigma'} [\nhat_{j\sigma'} , \chat_{i\sigma} ] \\
={}& -U\chat_{i\sigma} \nhat_{i,-\sigma} - \xi_\text{at} \chat_{i\sigma} \\
={}& -(U\nhat_{i,-\sigma} + \xi_\text{at}) \chat_{i\sigma}
\end{align}$$

This tells us that 

$$\begin{align}
\chat_{i\sigma,I}(\tau) ={}& \sum_{n=0}^\infty \frac{\tau^n}{n!}[\Hhat_0,[\Hhat_0,\dots,[\Hhat_0,\chat_{i\sigma}],\dots]] \\
={}& \sum_{n=0}^\infty \frac{(-\tau)^n}{n!}(U\nhat_{i,-\sigma} - \epsilon_\text{at})^n \chat_{i\sigma} \\
={}& e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})} \chat_{i\sigma}
\end{align}$$

Thus similarly, we find that 

\(\)\chat^\dagger_{i\sigma,I} = e^{\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}\chat^\dagger_{i\sigma}\(\)

The Green function at zeroth order in \(t\) is given by (assuming \(\tau > 0\))

$$\begin{align}
\mathcal{G}(i,\tau;j) ={}& -\langle T_\tau[\chat_{i\sigma}(\tau) \chat^\dagger_{j\sigma}]\rangle_0 \\
={}& -\langle \chat_{i\sigma}(\tau) \chat^\dagger_{j\sigma} \rangle_0 \\
={}& -e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})} \langle \chat_{i\sigma} \chat^\dagger_{j\sigma} \rangle_0
\end{align}$$

To evaluate the correlator, we compute the trace using the occupation number basis. We then get that 

$$\begin{align}
\mathcal{G}(i,\tau;j) ={}& -e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}\frac{1}{Z_\text{loc}}  \tr(e^{-\beta \Hhat_0} \chat_{i\sigma} \chat^\dagger_{j\sigma}) 
\end{align}$$

Here, the local partition function for one site is

$$\begin{align}
Z_\text{loc} ={}& \tr e^{-\beta \Hhat_0} \\
={}& \bra{0} e^{-\beta \Hhat_0} \ket{0} + \bra{\uparrow} e^{-\beta \Hhat_0} \ket{\uparrow} + \bra{\downarrow} e^{-\beta \Hhat_0} \ket{\downarrow} + \bra{\uparrow\downarrow} e^{-\beta\Hhat_0} \ket{\uparrow\downarrow} \\
={}& 1 + 2 e^{-\beta \xi_\text{at}} + e^{-\beta(U + 2\xi_\text{at})} 
\end{align}$$

Then, we find that 

$$\begin{align}
\mathcal{G}(i,\tau;j) ={}& -\frac{1}{Z_\text{loc}}  \tr(e^{-\beta \Hhat_0} e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}\chat_{i\sigma} \chat^\dagger_{j\sigma}) \\
={}& -\delta_{ij} \frac{1}{Z_\text{loc}}  \tr(e^{-\beta \Hhat_0} e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}\chat_{i\sigma} \chat^\dagger_{i\sigma}) \\
={}& -\delta_{ij} \frac{1}{Z_\text{loc}}  \tr(e^{-\beta \Hhat_0}e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}(1 - \nhat_{i\sigma})) \\
={}& -\delta_{ij} \frac{1}{Z_\text{loc}}  \left(\sum_{\sigma'} \bra{\sigma'} e^{-\beta \Hhat_0}e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}(1 - \nhat_{i\sigma}) \ket{\sigma'}   \right. \\
&\left. + \bra{0}e^{-\beta \Hhat_0}e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}(1 - \nhat_{i\sigma}) \ket{0} + \bra{\uparrow\downarrow}e^{-\beta \Hhat_0}e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}(1 - \nhat_{i\sigma}) \ket{\uparrow\downarrow}  \right)\\
={}& -\delta_{ij} \frac{1}{Z_\text{loc}}  \left(\sum_{\sigma'} \bra{\sigma'} e^{-\beta \Hhat_0}e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})}\ket{\sigma'}(1 - \delta_{\sigma\sigma'})    \right. \\
&\left. + \bra{0}e^{-\beta \Hhat_0}e^{-\tau(U\nhat_{i,-\sigma} + \xi_\text{at})} \ket{0}  \right)\\
={}& -\delta_{ij} \frac{1}{Z_\text{loc}}  \left(\sum_{\sigma'} \bra{\sigma'} e^{-\beta \Hhat_0}\ket{\sigma'}e^{-\tau(U\delta_{\sigma',-\sigma} + \xi_\text{at})}(1 - \delta_{\sigma\sigma'}) + \bra{0}e^{-\beta \Hhat_0}\ket{0}e^{-\tau\xi_\text{at}} \right)\\
={}& -\delta_{ij} \frac{1}{Z_\text{loc}}  \left( \sum_{\sigma'} e^{\beta\epsilon_{at}} e^{-\tau(U\delta_{\sigma',-\sigma} + \xi_\text{at})}(1 - \delta_{\sigma\sigma'}) + e^{-\tau\xi_\text{at}} \right) \\
={}& -\delta_{ij} \frac{1}{Z_\text{loc}}  \left(e^{-\beta\xi_{at}} e^{-\tau(U + \xi_\text{at})} + e^{-\tau\xi_\text{at}} \right)
\end{align}$$

Next, we Fourier transform in imaginary time to get the Matsubara frequency space representation. This gives us 

$$\begin{align}
\mathcal{G}(i,i\omega;j) ={}& \int_0^\beta e^{i\omega\tau} \mathcal{G}(i,\tau;j) \d\tau \\
={}& \delta_{ij}\frac{1}{Z_\text{loc}}\left(\frac{1 + e^{-\beta \xi_{at}}}{i\omega - \xi_{at}} + \frac{e^{-\beta\xi_{at}} + e^{-\beta(2\xi_{at} + U)}}{i\omega - \xi_{at} - U}\right)
\end{align}$$

The poles of the single particle Green function correspond to the different single particle excitations in the system. We can have an excitation with energy \(\xi_\text{at}\), which is what happens when we go from an empty to singly occupied site. We can also have a two-particle excitation with energy \(\xi_\text{at} + U\), which is what happens when we go from a singly to doubly occupied site. Note that we can also rewrite this using the fact that 

\(\)\langle \nhat_{\sigma} \rangle = \frac{1}{Z_\text{loc}}(e^{-\beta\xi_\text{at}} + e^{-\beta(2\xi_\text{at} + U)}), \quad 1 - \langle \nhat_\sigma\rangle = \frac{1}{Z_\text{loc}}(1 + e^{-\beta\xi_\text{at}})\(\)

which means that 

$$\begin{align}
\mathcal{G}(i,i\omega;j) ={}& \delta_{ij}\left(\frac{1 - \langle \nhat_{i\sigma}\rangle}{i\omega - \xi_\text{at}} + \frac{\langle \nhat_{i\sigma} \rangle}{i\omega - \xi_\text{at} - U}\right)
\end{align}$$

Finally, we Fourier transform to momentum space. If we define \(\mathcal{G}(\mathbf{R}_i - \mathbf{R}_j,i\omega) = \mathcal{G}(i,i\omega;j)\), then we get

$$\begin{align}
\mathcal{G}(\k,i\omega) ={}& \sum_{i} e^{-i\mathbf{R}_i\cdot\k} \mathcal{G}(\mathbf{R}_i,i\omega) \\
={}& \sum_{i} e^{-i\mathbf{R}_i\cdot\k}  \delta_{i,0}\left(\frac{1 - \langle \nhat_{i\sigma}\rangle}{i\omega - \xi_\text{at}} + \frac{\langle \nhat_{i\sigma} \rangle}{i\omega - \xi_\text{at} - U}\right) \\
={}& \frac{1 - \langle \nhat_{\sigma}\rangle}{i\omega - \xi_{at}} + \frac{\langle \nhat_{\sigma} \rangle}{i\omega - \xi_\text{at} - U}
\end{align}$$

so we see that the Green function is independent of the wave vector.

</li>
<li> Next, we analytically continue to find that the retarded Green function is given by

$$\begin{align}
G^R(\k,\omega) ={}& \mathcal{G}(\k,\omega + i\eta) \\
={}& \frac{1 - \langle \nhat_\sigma\rangle}{\omega - \xi_\text{at} + i\eta} + \frac{\langle \nhat_\sigma\rangle}{\omega - \xi_\text{at} - U + i\eta} \\
={}& (1 - \langle \nhat_\sigma\rangle)\left(\frac{1}{\omega - \xi_\text{at}} - i\pi\delta(\omega - \xi_\text{at})\right) + \langle \nhat_\sigma\rangle\left(\frac{1}{\omega - \xi_\text{at} - U} - i\pi\delta(\omega - \xi_\text{at} - U)\right)
\end{align}$$

The corresponding spectral function is given by 

$$\begin{align}
A(\k,\omega) ={}& 2\pi(1 - \langle \nhat_\sigma\rangle)\delta(\omega - \xi_\text{at}) + 2\pi\langle \nhat_\sigma\rangle \delta(\omega - \xi_\text{at} - U)
\end{align}$$

Thus, the density of states is given by 

$$\begin{equation}
\rho(\omega) = 2\pi(1 - \langle \nhat_\sigma\rangle)\delta(\omega - \xi_\text{at}) + 2\pi\langle \nhat_\sigma\rangle \delta(\omega - \xi_\text{at} - U).
\end{equation}$$

The plot of this is simply two delta functions. These correspond to the upper and lower Hubbard subbands, but here they are infinitely narrow. This is because the single particle states have an infinite lifetime. To acquire a broadening and subsequent finite lifetime, we need to include the hopping between neighbouring sites.

 
 
 
 
 
</li></ol>
</div> 
 </div>



</div> </li></ol>


