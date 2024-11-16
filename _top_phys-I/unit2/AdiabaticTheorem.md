---
layout: lesson
title: Adiabatic Theorem 
dept: physics
course: top_phys-I
unit: unit2
deptDisplay: Physics
courseDisplay: Topological Physics I
unitDisplay: Unit 2
---
We consider a Hamiltonian parameterized by some set of parameters organized into a vector \\(\mathbf{X}\\). This set of parameters could be, for example, the 3 components of a magnetic field, the point in \\(\k\\) space for some condensed matter system, or..... The set of parameters \\(\mathbf{X}\\) are taken from some set, and the topology of this set is what will often concern us in topological physics. The Hamiltonian we consider is a function on these parameters, but not a function of time. However, we let the Hamiltonian depend on time via the parameters \\(\mathbf{X}\\): 

$$\begin{equation}
\hat{H}(\mathbf{X}(t))
\end{equation}$$

and then observe what happens to the eigenstates and eigenvalues of this Hamiltonian as \\(\mathbf{X}\\) is taken through its set over time. The time scale over which \\(\mathbf{X}\\) changes is much longer than the time scale over which wavefunction phases change, that is, the time scale over which \\(\mathbf{X}\\) changes is much slower than \\(E/\bhat\\), where \\(E\\) is an energy eigenvalue. If we consider the eigenvalues and eigenvectors of this Hamiltonian, they will depend on time (of course via \\(\mathbf{X}\\) as well):

$$\begin{equation}
\hat{H}(\mathbf{X}(t))\ket{\phi_n(t)} = E_n(t)\ket{\phi_n(t)}.
\end{equation}$$

It is in terms of these basis states that we will write the solution to the time-dependent Schrödinger equation:

$$\begin{equation}
i\hbar \frac{\partial}{\partial t}\ket{\Psi} = \hat{H}\ket{\Psi}
\end{equation}$$

as a superposition of these time-dependent basis states

$$\begin{equation}
\ket{\Psi(t)} = \sum_n a_n(t) e^{i\theta_n(t)} \ket{\phi_n(t)}
\end{equation}$$

where the phase angle is

$$\begin{equation}
\theta_n(t) = -\frac{1}{\hbar}\int_0^t E_n(t')\d t'.
\end{equation}$$

If we plug this representation of the \\(\ket{\Psi}\\) into the time-dependent Schrödinger equation, we get 

$$\begin{equation}
i\hbar\sum_n\left(\dot{a}_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} + a_n(t)i\dot{\theta}_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} + a_n(t)e^{i\theta_n(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}\right) = \sum_n a_n(t)e^{i\theta_n(t)}\hat{H}\ket{\phi_n(t)}
\end{equation}$$

We can simplify the expression with \\(\dot{\theta}\_n(t)\\), as well as the right hand side since \\(\ket{\phi\_n(t)}\\) since it's an eigenvector

$$\begin{equation}
i\hbar\sum_n\left(\dot{a}_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} - a_n(t)\frac{i}{\hbar}E_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} + a_n(t)e^{i\theta_n(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}\right) = \sum_n a_n(t)e^{i\theta_n(t)}E_n(t)\ket{\phi_n(t)}
\end{equation}$$

This allows us to cancel out the right hand side with the second term on the left hand side:

$$\begin{equation}
i\hbar\sum_n\left(\dot{a}_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} + a_n(t)e^{i\theta_n(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}\right) = 0
\end{equation}$$

Next, we take the inner product with \\(\bra{\phi\_m(t)}\\). This will simplify the equation because, at each time \\(t\\), \\(\bra{\phi\_m(t)}\ket{\phi\_n(t)} = \delta\_{mn}\\). This gives us 

$$\begin{equation}
i\hbar\sum_n\left(\dot{a}_n(t)e^{i\theta_n(t)}\delta_{mn} + a_n(t)e^{i\theta_n(t)}\bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}\right) = 0
\end{equation}$$

which simplifies to 

$$\begin{equation}
\dot{a}_m(t) = -\sum_n a_n(t) e^{i(\theta_n(t) - \theta_m(t))}\bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}.
\end{equation}$$

For reasons we will see later, we rewrite this as 

$$\begin{equation}
\dot{a}_m(t) = - a_m(t) \bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_m(t)} -\sum_{n\neq m} a_n(t) e^{i(\theta_n(t) - \theta_m(t))}\bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}.
\end{equation}$$

Now, we will get another equation by differentiating 

$$\begin{equation}
\hat{H}(t)\ket{\phi_n(t)} = E_n(t)\ket{\phi_n(t)}.
\end{equation}$$

which gives us 

$$\begin{equation}
\frac{\partial \hat{H}(t)}{\partial t}\ket{\phi_n(t)} + \hat{H}(t)\frac{\partial}{\partial t}\ket{\phi_n(t)} = \dot{E}_n(t)\ket{\phi_n(t)} + E_n(t)\frac{\partial}{\partial t}\ket{\phi_n(t)}
\end{equation}$$

and then we take the inner product with \\(\bra{\phi\_m(t)}\\), which gives 

$$\begin{equation}
\bra{\phi_m(t)}\frac{\partial \hat{H}(t)}{\partial t}\ket{\phi_n(t)} + \bra{\phi_m(t)}\hat{H}(t)\frac{\partial}{\partial t}\ket{\phi_n(t)} = \bra{\phi_m(t)}\dot{E}_n(t)\ket{\phi_n(t)} + \bra{\phi_m(t)}E_n(t)\frac{\partial}{\partial t}\ket{\phi_n(t)}
\end{equation}$$

For the second term, we can act with the Hamiltonian from the right to simplify things:

$$\begin{equation}
\bra{\phi_m(t)}\frac{\partial \hat{H}(t)}{\partial t}\ket{\phi_n(t)} + \bra{\phi_m(t)}E_m(t)\frac{\partial}{\partial t}\ket{\phi_n(t)} = \dot{E}_n(t)\delta_{mn} + \bra{\phi_m(t)}E_n(t)\frac{\partial}{\partial t}\ket{\phi_n(t)}
\end{equation}$$

This can be rearranged to get 

$$\begin{equation}
\bra{\phi_m(t)}\frac{\partial \hat{H}(t)}{\partial t}\ket{\phi_n(t)} + \bra{\phi_m(t)}E_m(t)\frac{\partial}{\partial t}\ket{\phi_n(t)} = \dot{E}_n(t)\delta_{mn}  + \bra{\phi_m(t)}E_n(t)\frac{\partial}{\partial t}\ket{\phi_n(t)}
\end{equation}$$

If \\(n\neq m\\), then we can rewrite this as 

$$\begin{equation}
\frac{\bra{\phi_m(t)}\frac{\partial \hat{H}(t)}{\partial t}\ket{\phi_n(t)}}{E_n(t) - E_m(t)} = \bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}
\end{equation}$$

Plugging this into the formula for \\(\dot{a}\_m\\), we find 

$$\begin{equation}
\dot{a}_m(t) = - a_m(t) \bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_m(t)} - \sum_{n\neq m} a_n(t) e^{i(\theta_n(t) - \theta_m(t))}\frac{\bra{\phi_m(t)}\frac{\partial \hat{H}(t)}{\partial t}\ket{\phi_n(t)}}{E_n(t) - E_m(t)}.
\end{equation}$$

This is an exact formula (again assuming that the eigenvalues are nondegenerate), and cannot be solved exactly. We can however solve it perturbatively. The approximation that we make is that the timescale that the Hamiltonian evolves on is extremely small, so \\(\partial \hat{H}(t)/\partial t\\) is extremely small. We therefore drop the second term and have 

$$\begin{equation}
\dot{a}_m(t) = - a_m(t) \bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_m(t)}.
\end{equation}$$

To integrate this equation, we rewrite it as

$$\begin{equation}
\frac{\dot{a}_m(t)}{a_m(t)} = - \bra{\phi_m(t)}\frac{\partial}{\partial t}\ket{\phi_m(t)}
\end{equation}$$

and this gives us 

$$\begin{equation}
a_m(t) = a_m(0)\exp\left(-\int_0^t \bra{\phi_m(t')}\frac{\partial}{\partial t'}\ket{\phi_m(t')}\d t'\right)
\end{equation}$$

We then define 

$$\begin{equation}
\gamma_m(t) = i\int_0^t \bra{\phi_m(t')}\frac{\partial}{\partial t'}\ket{\phi_m(t')}\d t'
\end{equation}$$

so that \\(a\_m(t) = a\_m(0)e^{i\gamma\_m(t)}\\). This phase \\(\gamma\_m(t)\\) is known as the geometric phase. 


\subsection{Berry Phase and Curvature} %ready
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



