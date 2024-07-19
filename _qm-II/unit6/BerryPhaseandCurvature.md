---
layout: lesson
title: Berry Phase and Curvature 
dept: physics
course: qm-II
unit: unit6
deptDisplay: Physics
courseDisplay: Quantum Mechanics II
unitDisplay: Unit 6
---
Consider an adiabatically transported parameter. The Hamiltonian is \\(\Hhat = \Hhat(\boldsymbol{\lambda}(t))\\), where \\(\boldsymbol{\lambda}\\) are parameters of the Hamiltonian. We assume that the internal frequency is much greater than teh external frequency. Goal: calculate how an eigenstate of the Hamiltonian at <i>fixed</i> poarameter varies with time. If \\(\Hhat\\) is independnet of time, then a particle starting in the \\(n\\)th eigenstate 

$$\Hhat\psi_n = E_n\psi_n$$

will stay in the \\(n\\)th eigenstate. If, on the other hand, \\(\Hhat\\) depends on time, then 

$$\Hhat(t) \psi_n(t) = E_n(t) \psi_n(t)$$

But, we still have \\(\bra{\psi_n(t)}\ket{\psi_m(t)} = \delta_{mn}\\).. Also, we still have \\(i\hbar \partial_t \psi(t) = \Hhat(t) \psi(t)\\). Thus, 

$$\psi(t) = \sum_n c_n(t) \psi_n(t) e^{i\theta_n(t)}$$

where \\(\theta_n = -\frac{1}{\hbar}\int_0^t E_n(t') \d t'\\). In the Schrödinger equation, we have that 

$$\begin{align}
i\hbar\partial_t\sum_n c_n(t) e^{i\theta_n(t)} \psi_n(t) ={}& \sum_n c_n(t) e^{i\theta_n(t)} \Hhat(t)\psi_n(t) \\
i\hbar\sum_n \dot{c}_n(t) e^{i\theta_n(t)} \psi_n(t) + i\hbar \sum_n c_n(t) e^{i\theta_n(t)} \dot{\psi}_n(t) - \hbar \sum_n \dot{\theta}_n(t) c_n(t) \psi_n(t) e^{i\theta_n(t)} ={}& \sum_n c_n(t) e^{i\theta_n(t)} E_n(t)\psi_n(t) \\
\end{align}$$

But, \\(\theta_n(t) = -\frac{1}{\hbar}\int_0^t E_n(t') \d t'\\), so \\(\dot{\theta}_n = -E_n(t)/\hbar\\). Thus, we have that 

$$\sum_n \left[\dot{c}_n(t) e^{i\theta_n(t)}\psi_n(t) + c_n(t) e^{i\theta_n(t)} \dot{\psi}_n(t)\right] = 0$$

Now, we want to solve for \\(c_n(t)\\). We can derive an ODE for these constants. To do this, we can take the inner prdouct on both sides as 

$$\sum_n \left[\dot{c}_n(t) e^{i\theta_n(t)} \bra{\psi_m(t)}\ket{\psi_n(t)} + c_n(t) e^{i\theta_n(t)} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}\right] = 0$$

Thus, solving, we have (note that we used \\(\bra{\psi_m(t)}\ket{\psi_n(t)} = \delta_{mn}\\), 

$$\dot{c}_m(t) e^{i\theta_m(t)} = -\sum_n c_n(t) e^{i\theta_n(t)} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}$$

and finally, 

$$\dot{c}_m(t) = -\sum_n c_n(t) e^{i(\theta_n(t) - \theta_m(t))} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}$$

We want to find an expression for \\(\ket{\dot{\psi}_n(t)}\\). For this, let us differentiate both sides of the Schrödinger equation:

$$\dot{\Hhat}(t)\ket{\psi_n(t)} + \Hhat(t)\ket{\dot{\psi}_n(t)} = \dot{E}_n(t)\ket{\psi_n(t)} + E_n(t)\ket{\dot{\psi}_n(t)}$$

Now taking the bra \\(\bra{\psi_m(t)}\\) on both sides, we have 

$$\begin{align}
\bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)} + \bra{\psi_m(t)}\Hhat(t)\ket{\dot{\psi}_n(t)} ={}& \bra{\psi_m(t)}\dot{E}_n(t)\ket{\psi_n(t)} + \bra{\psi_m(t)}E_n(t)\ket{\dot{\psi}_n(t)} \\
\bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)} + E_m(t)\bra{\psi_m(t)}\ket{\dot{\psi}_n(t)} ={}& \dot{E}_n(t)\delta_{mn} + E_n(t)\bra{\psi_m(t)}\ket{\dot{\psi}_n(t)}
\end{align}$$

Thus, 

$$(E_n(t) - E_m(t))\bra{\psi_m(t)}\ket{\dot{\psi}_n(t)} = \bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)} - \dot{E}_n(t)\delta_{mn}$$

Now, we split the sum for the \\(c\\) equation

$$\begin{align}
\dot{c}_m(t) ={}& - c_m(t) \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)} -\sum_{n\neq m} c_n(t) e^{i(\theta_n(t) - \theta_m(t))} \bra{\psi_m(t)}\ket{\dot{\psi}_n(t)} \\
={}& - c_m(t) \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)} - \sum_{n\neq m} c_n(t) e^{i(\theta_n(t) - \theta_m(t))} \frac{\bra{\psi_m(t)}\dot{\Hhat}(t)\ket{\psi_n(t)}}{E_n(t) - E_m(t)} \\
\end{align}$$

Since we have assumed that the internal frequencies are much faster than the external frequencies, \\(\dot{\psi}_m(t)\\) has an internal frequency, but \\(\dot{\Hhat}(t)\\) has an external frequency, we drop the sum. Thus, we have 

$$\begin{align}
\dot{c}_m(t) ={}& - c_m(t) \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)}
\end{align}$$

Now that the equations are decoupled, we can solve this as 

$$c_m(t) = c_m(0)\exp\left(-\int_0^t \bra{\psi_m(t)}\ket{\dot{\psi}_m(t)}\d t\right)$$

Now, substituting this back in, we find 

$$\ket{\psi}(t) = \sum_n c_n(0) e^{i\gamma_n(t)} e^{i\theta_n(t)} \ket{\psi_n(t)}$$

where we have defined 

$$\gamma_n(t) = i\int_0^t \bra{\psi_n(t')}\ket{\dot{\psi}_n(t')}\d t'$$

We can rewrite this as 

$$\gamma_n(t) = i\int_{\boldsymbol{\lambda}(0)}^{\boldsymbol{\lambda}(t)} \bra{\psi_n(\boldsymbol{\lambda})}\nabla_{\boldsymbol{\lambda}}\ket{\psi_n(\boldsymbol{\lambda})} \cdot \d \boldsymbol{\lambda}$$

Then, we define 

$$\mathbf{A}_n = -i\bra{\psi_n(\boldsymbol{\lambda})}\nabla_{\boldsymbol{\lambda}}\ket{\psi_n(\boldsymbol{\lambda})}$$

so that 

$$\gamma_n(t) = -\int_{\boldsymbol{\lambda}(0)}^{\boldsymbol{\lambda}(t)} \mathbf{A}_n(\boldsymbol{\lambda}) \cdot \d\boldsymbol{\lambda}$$

If the parameters \\(\boldsymbol{\lambda}(t)\\) depend on \\(t\\) in a way that returns after \\(t=T\\) seconds, then 

$$\gamma_n = -\oint \mathbf{A}_n(\boldsymbol{\lambda}) \cdot \d\boldsymbol{\lambda}$$












Now, we make the observation that, since the Hamiltonian depended on time only via the parameters \\(\hat{H}(t) = \hat{H}(<b>X</b>(t))\\), we can use the chain rule: 

$$\begin{equation}
\frac{\partial}{\partial t}\ket{\phi_m(t)} = \frac{\partial}{\partial t}\ket{\phi_m(<b>X</b>(t))} = \frac{\partial}{\partial<b>X</b>}\ket{\phi_m(<b>X</b>)} \cdot\frac{\d <b>X</b>}{\d t}
\end{equation}$$

Thus we rewrite the formula for the geometric phase as 

$$\begin{equation}
\gamma_m(t) = i\int_0^t \bra{\phi_m(<b>X</b>(t'))}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>(t'))} \cdot \frac{\d<b>X</b>}{\d t'}\d t'
\end{equation}$$

We recognize that this can be rewritten in terms of a line integral through parameter space:

$$\begin{equation}
\gamma_m(t) = -i\int_{<b>X</b>(0)}^{<b>X</b>(t)} \bra{\phi_m(<b>X</b>)}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>)} \cdot\d<b>X</b>
\end{equation}$$

Now, we finally can write 

$$\begin{equation}
\ket{\Psi(t)} = \sum_n a_n(0)e^{i(\theta_n(t) - \gamma_n(t))} \ket{\phi_n(t)}.
\end{equation}$$

So the time evolution is simply the standard one: if the system is starts out in an eigenstate \\(\ket{\phi_n(t)}\\), then it stays in that eigenstate and is modified only by a phase factor. In the special case that the parameter \\(<b>X</b>\\) goes around a closed loop, the geometric phase is instead called the Berry phase, and can be written as

$$\begin{equation}
\gamma_m = -i\oint_C \bra{\phi_m(<b>X</b>)}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>)} \cdot\d<b>X</b>
\end{equation}$$

Let's now turn to a discussion of the Berry phase. We define the quantity 

$$\begin{equation}
<b>A</b>_m = -i\bra{\phi_m(<b>X</b>)}\frac{\partial}{\partial <b>X</b>}\ket{\phi_m(<b>X</b>)}
\end{equation}$$

where \\(<b>A</b>\\) is a vector field with the same number of components as \\(<b>X</b>\\). In the special case where the parameter space is 3-dimensional, then we can apply Stoke's theorem to rewrite the Berry phase as 

$$\begin{equation}
\gamma_m = \iint \nabla\times<b>A</b>_m \cdot \nhat\d S.
\end{equation}$$

This resembles the integral of a magnetic field \\(<b>B</b> = \nabla\times<b>A</b>\\) over a closed surface, which is interpreted as the flux! Of course, this vector field has, in general, nothing to do with an actual magnetic field; the similarity is purely mathematical. We call the quantity \\(<b>A</b>\\) the <i>Berry connection</i> and \\(<b>B</b>\\) the <i>Berry curvature</i>. There is an interpretation of the field \\(<b>A</b>\\) as a connection in the differential geometric sense, and we will discuss that in an aside section later.

<div class="example">
<b>Example:</b>
In this example, we will actually compute the Berry phase and Berry curvature for a 2-level system. The system is a single electron immersed in a time-dependent magnetic field \(<b>B</b>\). Note that it is mere coincidence that there is an actual magnetic field in this problem; normally the vector potential and magnetic field which are abstractly discussed in the context of topological physics are merely analogous to the ones in electromagnetism. The Hamiltonian for this system is given by 

$$\begin{equation}
\hat{H} = -\boldsymbol{\mu}\cdot<b>B</b>(t)
\end{equation}$$

where \(\boldsymbol{\mu} = \gamma<b>S</b>\), and \(<b>S</b> = \frac{\hbar}{2}(\sigma^x,\sigma^y,\sigma^z)\), where \(\sigma^i\) are the ordinary Pauli matrices. The magnetic field is given by \(<b>B</b>(t) = B_0(\sin\theta\cos\varphi, \sin\theta\sin\varphi, \cos\theta)\). Therefore the Hamiltonian is 

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
<b>A</b>_\pm = \pm \frac{\sin^2(\theta/2)}{r\sin\theta}\hat{e}_\varphi
\end{equation}$$

Next, we need to compute the curl of these quantities, which gives us the Berry curvature:

$$\begin{equation}
<b>B</b>_\pm = \pm \frac{1}{2r^2}\hat{e}_r
\end{equation}$$

Lastly, we can integrate this to find the Berry phase:

$$\begin{align}
\gamma_\pm ={}& \int<b>B</b>_\pm \cdot \nhat\d S \\
={}& \int <b>B</b>_\pm \cdot \hat{e}_r r^2\d\Omega \\
={}& \frac{1}{2}\int \d\Omega \\
={}& \frac{\Omega}{2}
\end{align}$$

where \(\Omega\) is the solid angle traced out by the closed trajectory in \(\theta,\varphi\) space. 



</div>


