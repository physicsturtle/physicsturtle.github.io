---
layout: lesson
title: Berry Phase and Curvature 
dept: physics
course: top_phys-I
unit: unit2
deptDisplay: Physics
courseDisplay: Topological Physics I
unitDisplay: Unit 2
---
Now, we make the observation that, since the Hamiltonian depended on time only via the parameters \\(\hat{H}(t) = \hat{H}(\mathbf{X}(t))\\), we can use the chain rule: 

$$\begin{equation}
\frac{\partial}{\partial t}\ket{\phi_m(t)} = \frac{\partial}{\partial t}\ket{\phi_m(\mathbf{X}(t))} = \frac{\partial}{\partial\mathbf{X}}\ket{\phi_m(\mathbf{X})} \cdot\frac{\d \mathbf{X}}{\d t}
\end{equation}$$

Thus we rewrite the formula for the geometric phase as 

$$\begin{equation}
\gamma_m(t) = i\int_0^t \bra{\phi_m(\mathbf{X}(t'))}\frac{\partial}{\partial \mathbf{X}}\ket{\phi_m(\mathbf{X}(t'))} \cdot \frac{\d\mathbf{X}}{\d t'}\d t'
\end{equation}$$

We recognize that this can be rewritten in terms of a line integral through parameter space:

$$\begin{equation}
\gamma_m(t) = -i\int_{\mathbf{X}(0)}^{\mathbf{X}(t)} \bra{\phi_m(\mathbf{X})}\frac{\partial}{\partial \mathbf{X}}\ket{\phi_m(\mathbf{X})} \cdot\d\mathbf{X}
\end{equation}$$

Now, we finally can write 

$$\begin{equation}
\ket{\Psi(t)} = \sum_n a_n(0)e^{i(\theta_n(t) - \gamma_n(t))} \ket{\phi_n(t)}.
\end{equation}$$

So the time evolution is simply the standard one: if the system is starts out in an eigenstate \\(\ket{\phi\_n(t)}\\), then it stays in that eigenstate and is modified only by a phase factor. In the special case that the parameter \\(\mathbf{X}\\) goes around a closed loop, the geometric phase is instead called the Berry phase, and can be written as

$$\begin{equation}
\gamma_m = -i\oint_C \bra{\phi_m(\mathbf{X})}\frac{\partial}{\partial \mathbf{X}}\ket{\phi_m(\mathbf{X})} \cdot\d\mathbf{X}
\end{equation}$$

Let's now turn to a discussion of the Berry phase. We define the quantity 

$$\begin{equation}
\mathbf{A}_m = -i\bra{\phi_m(\mathbf{X})}\frac{\partial}{\partial \mathbf{X}}\ket{\phi_m(\mathbf{X})}
\end{equation}$$

where \\(\mathbf{A}\\) is a vector field with the same number of components as \\(\mathbf{X}\\). In the special case where the parameter space is 3-dimensional, then we can apply Stoke's theorem to rewrite the Berry phase as 

$$\begin{equation}
\gamma_m = \iint \nabla\times\mathbf{A}_m \cdot \nhat\d S.
\end{equation}$$

This resembles the integral of a magnetic field \\(\mathbf{B} = \nabla\times\mathbf{A}\\) over a closed surface, which is interpreted as the flux! Of course, this vector field has, in general, nothing to do with an actual magnetic field; the similarity is purely mathematical. We call the quantity \\(\mathbf{A}\\) the <i>Berry connection</i> and \\(\mathbf{B}\\) the <i>Berry curvature</i>. There is an interpretation of the field \\(\mathbf{A}\\) as a connection in the differential geometric sense, and we will discuss that in an aside section later.

<div class="example">
<b>Example:</b>
In this example, we will actually compute the Berry phase and Berry curvature for a 2-level system. The system is a single electron immersed in a time-dependent magnetic field \(\mathbf{B}\). Note that it is mere coincidence that there is an actual magnetic field in this problem; normally the vector potential and magnetic field which are abstractly discussed in the context of topological physics are merely analogous to the ones in electromagnetism. The Hamiltonian for this system is given by 

$$\begin{equation}
\hat{H} = -\boldsymbol{\mu}\cdot\mathbf{B}(t)
\end{equation}$$

where \(\boldsymbol{\mu} = \gamma\mathbf{S}\), and \(\mathbf{S} = \frac{\hbar}{2}(\sigma^x,\sigma^y,\sigma^z)\), where \(\sigma^i\) are the ordinary Pauli matrices. The magnetic field is given by \(\mathbf{B}(t) = B_0(\sin\theta\cos\varphi, \sin\theta\sin\varphi, \cos\theta)\). Therefore the Hamiltonian is 

$$\begin{equation}
\hat{H} = \frac{\omega_1\hbar}{2}\begin{pmatrix} \cos\theta & \sin\theta e^{-i\varphi} \\ \sin\theta e^{i\varphi} & -\cos \theta \end{pmatrix}
\end{equation}$$

where \(\omega_1 = eB/m\) is the cyclotron frequency. The eigenvalues of the Hamiltonian are, surprisingly, time independent and are \(E_\pm = \pm \hbar\omega_1/2\). The corresponding eigenvectors of this Hamiltonian can be calculated as 

$$\begin{equation}
\ket{\chi_+} = \begin{pmatrix}\cos(\theta/2)  \\ \sin(\theta/2) e^{i\varphi} \end{pmatrix} ,\qquad \ket{\chi_-}  = \begin{pmatrix} \sin(\theta/2)e^{-i\varphi} \\ -\cos(\theta/2) \end{pmatrix}
\end{equation}$$

Now that we have the two states of the system, we can compute the gradient, which will appear in the Berry connection. This gives us 

$$\begin{align}
\nabla \ket{\chi_+} ={}& \frac{1}{r}\frac{\partial \ket{\chi_+}}{\partial\theta} \hat{e}_\theta + \frac{1}{r \sin\theta}\frac{\partial \ket{\chi_+}}{\partial\varphi}\hat{e}_\varphi \\
={}& \frac{1}{2r}\begin{pmatrix} -\sin(\theta/2) \\ \cos(\theta/2)e^{i\varphi} \end{pmatrix} \hat{e}_\theta + \frac{1}{r\sin\theta}\begin{pmatrix} 0 \\ i\sin(\theta/2)e^{i\varphi}\end{pmatrix} \hat{e}_\varphi 
\end{align}$$

Similarly, we can compute 

$$\begin{align}
\nabla\ket{\chi_-} = \frac{1}{2r}\begin{pmatrix} \cos(\theta/2)e^{-i\varphi} \\ \sin(\theta/2) \end{pmatrix} \hat{e}_\theta + \frac{1}{r\sin\theta} \begin{pmatrix} -i\sin(\theta/2) e^{-i\varphi} \\ 0\end{pmatrix} \hat{e}_\varphi
\end{align}$$

Therefore, we find the Berry connections for the different ``bands" to be:

$$\begin{equation}
\bra{\chi_+}\nabla\ket{\chi_+} = i\frac{\sin^2(\theta/2)}{r\sin\theta} \hat{e}_\varphi,\qquad \bra{\chi_-}\nabla\ket{\chi_-} = -i\frac{\sin^2(\theta/2)}{r\sin\theta}\hat{e}_\varphi
\end{equation}$$

so the Berry connections are 

$$\begin{equation}
\mathbf{A}_\pm = \pm \frac{\sin^2(\theta/2)}{r\sin\theta}\hat{e}_\varphi
\end{equation}$$

Next, we need to compute the curl of these quantities, which gives us the Berry curvature:

$$\begin{equation}
\mathbf{B}_\pm = \pm \frac{1}{2r^2}\hat{e}_r
\end{equation}$$

Lastly, we can integrate this to find the Berry phase:

$$\begin{align}
\gamma_\pm ={}& \int\mathbf{B}_\pm \cdot \nhat\d S \\
={}& \int \mathbf{B}_\pm \cdot \hat{e}_r r^2\d\Omega \\
={}& \frac{1}{2}\int \d\Omega \\
={}& \frac{\Omega}{2}
\end{align}$$

where \(\Omega\) is the solid angle traced out by the closed trajectory in \(\theta,\varphi\) space. 



</div>

<b>FAQ:</b>
Frequently asked questions:
<ol>
<li> The Berry phase is often used when there is no hint of time dependence in the problem. By what mechanism is the external parameter changed? 
</li></ol>



<ol>
<li> <div class="exercise">  In graphene, which is a hexagonal lattice of carbon atoms, there are 4 different orbitals which could contribute to conduction. They are the \(s\), \(p_x\), \(p_y\), and \(p_z\) orbitals. It turns out that only the \(p_z\) orbitals are contribute to conduction, and are each half-filled. We can therefore model the system with the following tight-binding model:

\(\)\hat{H} = -t\sum_{\langle i,j\rangle,\sigma} (\chat^\dagger_{i\sigma} \chat_{j\sigma} + \chat^\dagger_{j\sigma}\chat_{i\sigma}).\(\)

<ol type="a">
<li> What are the Bravais lattice vectors and reciprocal lattice vectors? 
</li>
<li> By Fourier transforming the creation/annihilation operators, rewrite the Hamiltonian in the form
\(\)\hat{H} = \sum_{\k\sigma} \chat^\dagger_{\k\sigma} H(\k) \chat_{\k\sigma} \(\)
and find the matrix \(H(\k)\). Note that this \(H(\k)\) matrix can be itself thought of as a Hamiltonian, but merely parametrized with \(\k\). 
</li>
<li> Diagonalize \(H(\k)\) to calculate the band structure. 
</li>
<li> 
</li></ol>

</div> </li>
<li> <div class="exercise">  Consider the tight-binding model with spin-orbit coupling. In this scenario, the hopping parameter can flip the spin of the hopping electron. The tight-binding Hamiltonian for this scenario is given by 

\(\)\hat{H} = -\sum_{\langle i,j\rangle,\alpha\beta}\left( s_{ij\alpha\beta}\chat^\dagger_{i\alpha}\chat_{j\beta} + \hc\right)\(\)

where \(s_{ij\alpha\beta} = t_{ij}\delta_{\alpha\beta} + i\mathbf{v}_{ij}\cdot\boldsymbol{\sigma}_{\alpha\beta}\), and the vector \(\mathbf{v}_{ij} = -\mathbf{v}_{ji}\). We assume that the hopping parameter \(t_{ij} = t\) for nearest neighbours, and \(\mathbf{v}_{ij} = \mathbf{v}\) for nearest neighbours with \(i>j\). By \(i>j\), we mean that either the \(x\) or \(y\) coordinates of 

<ol type="a">
<li> If we put this model on the 2D square lattice with lattice constant \(a\), rewrite the Hamiltonian as 
\(\)\hat{H} = \sum_{\k} \begin{pmatrix} \chat^\dagger_{\k\uparrow} & \chat^\dagger_{\k\downarrow} \end{pmatrix} H(\k) \begin{pmatrix} \chat_{\k\uparrow} \\ \chat_{\k\downarrow} \end{pmatrix} \(\)
</li>
<li> By calculating the eigenvalues of the \(H(\k)\) matrix, compute the band structure of the model.
</li>
<li> Compute the eigenvectors of the model.
</li>
<li> Calculate the Berry connection and Berry curvature for each band.
</li>
<li> Calculate the Chern number of each band. 
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer147')" class="answerButton">Show Answer</button> 
 <div  id='answer147' class="answer" >
<ol type="a">
<li> We Fourier transform the conduction electron operators as 

\(\)\chat_{i\sigma} = \frac{1}{\sqrt{N_s}}\sum_{\k} e^{i\k\cdot\mathbf{R}_i} \chat_{\k\sigma} ,\qquad \chat^\dagger_{i\sigma} = \frac{1}{\sqrt{N_s}}\sum_{\k} e^{-i\k\cdot\mathbf{R}_i}\chat^\dagger_{\k\sigma} \(\)

This means the Hamiltonian can be written as 

$$\begin{align}
\hat{H} ={}& -\frac{1}{N_s} \sum_{\langle i,j\rangle,\alpha\beta} \sum_{\k\k'} \left(t_{ij}\delta_{\alpha\beta} + i\mathbf{v}_{ij}\cdot\boldsymbol{\sigma}_{\alpha\beta}\right) e^{-i\k\cdot\mathbf{R}_i}e^{i\k'\cdot\mathbf{R}_j} \chat^\dagger_{\k\alpha}\chat_{\k'\beta} + \Hc \\
={}& -\frac{1}{N_s} \sum_{\alpha\beta} \sum_{\k\k'} \sum_{\langle i,j\rangle} \left(t \delta_{\alpha\beta} + i\mathbf{v}_{ij}\cdot\boldsymbol{\sigma}_{\alpha\beta}\right) e^{-i(\k-\k')\cdot\mathbf{R}_i}e^{i\k'\cdot(\mathbf{R}_j-\mathbf{R}_i)} \chat^\dagger_{\k\alpha}\chat_{\k'\beta} + \Hc \\
={}& -\frac{1}{N_s} \sum_{\alpha\beta} \sum_{\k\k'} \sum_i e^{-i(\k-\k')\cdot\mathbf{R}_i} \left[ \left(t\delta_{\alpha\beta} + i\mathbf{v}\cdot\boldsymbol{\sigma}_{\alpha\beta}\right) (e^{-iak_x'} + e^{-iak_y'}) \right]\chat^\dagger_{\k\alpha}\chat_{\k'\beta} + \Hc \\
={}& -\frac{1}{N_s} \sum_{\alpha\beta} \sum_{\k\k'} N_s\delta_{\k\k'} \left[ \left(t\delta_{\alpha\beta} + i\mathbf{v}\cdot\boldsymbol{\sigma}_{\alpha\beta}\right) (e^{-iak_x'} + e^{-iak_y'}) \right]\chat^\dagger_{\k\alpha}\chat_{\k'\beta} + \Hc \\
={}& - \sum_{\alpha\beta} \sum_{\k} \left[ \left(t\delta_{\alpha\beta} + i\mathbf{v}\cdot\boldsymbol{\sigma}_{\alpha\beta}\right) (e^{-iak_x} + e^{-iak_y}) \right]\chat^\dagger_{\k\alpha}\chat_{\k\beta} + \Hc \\
={}& - \sum_{\alpha\beta} \sum_{\k} \left[ \left(t\delta_{\alpha\beta} + i\mathbf{v}\cdot\boldsymbol{\sigma}_{\alpha\beta}\right) (e^{-iak_x} + e^{-iak_y}) \right]\chat^\dagger_{\k\alpha}\chat_{\k\beta} \\
&-\sum_{\alpha\beta}\sum_{\k} \left[ \left(t\delta_{\alpha\beta} - i\mathbf{v}\cdot\boldsymbol{\sigma}_{\alpha\beta}^* \right) (e^{iak_x} + e^{iak_y}) \right]\chat^\dagger_{\k\beta}\chat_{\k\alpha} 
\end{align}$$

Here, the \(*\) on the Pauli matrix just means complex conjugate; no transpose. Thus we can rewrite this as 

$$\begin{align}
\hat{H} ={}& - \sum_{\alpha\beta} \sum_{\k} \left[ \left(t\delta_{\alpha\beta}2(\cos(ak_x) + \cos(ak_y)) + 2(\sin(ak_x) + \sin(ak_y))\mathbf{v}\cdot\boldsymbol{\sigma}_{\alpha\beta}\right) \right]\chat^\dagger_{\k\alpha}\chat_{\k\beta} \\
={}& \sum_{\k}\begin{pmatrix} \chat^\dagger_{\k\uparrow} & \chat^\dagger_{\k\downarrow} \end{pmatrix} \begin{pmatrix} a(\k) + v_z b(\k) & b(\k)(v_x - iv_y) \\ b(\k)(v_x+iv_y) & a(\k) - v_zb(\k) \end{pmatrix} \begin{pmatrix} \chat_{\k\uparrow} \\ \chat_{\k\downarrow} \end{pmatrix}
\end{align}$$

where \(a(\k) = -2t(\cos(ak_x) + \cos(ak_y))\) and \(b(\k) = -2(\sin(ak_x) + \sin(ak_y))\).

</li>
<li> \(\)\epsilon_{\k} = -2t(\cos(k_xa) + \cos(k_ya)) \pm 2|\mathbf{v}|(\sin(k_xa) + \sin(k_ya)).\(\)
Thus, we can write the Hamiltonian as 
\(\)\hat{H} = \sum_{\k\sigma} \chat^\dagger_{\k\sigma} \(\)
</li>
<li> 
</li>
<li> 
</li></ol>
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Calculate the next correction to the adiabatic approximation. 

<div class="answerBox"> 
 <button onclick="myFunction('answer184')" class="answerButton">Show Answer</button> 
 <div  id='answer184' class="answer" >

</div> 
 </div>


</div> </li></ol>

\subsection{Chern Number}
We call the following quantity the Chern number:
$$\begin{equation}
C_n = \frac{1}{2\pi}\int_S \mathbf{F}_n \cdot d\mathbf{S} = n\in \ZZ
\end{equation}$$


