---
layout: lesson
title: Adiabatic Theorem 
dept: physics
course: qm-II
unit: unit6
deptDisplay: Physics
courseDisplay: Quantum Mechanics II
unitDisplay: Unit 6
---
We consider a Hamiltonian parameterized by some set of parameters organized into a vector \\(<b>X</b>\\). This set of parameters could be, for example, the 3 components of a magnetic field, the point in \\(\k\\) space for some condensed matter system, or..... The set of parameters \\(<b>X</b>\\) are taken from some set, and the topology of this set is what will often concern us in topological physics. The Hamiltonian we consider is a function on these parameters, but not a function of time. However, we let the Hamiltonian depend on time via the parameters \\(<b>X</b>\\): 

$$\begin{equation}
\hat{H}(<b>X</b>(t))
\end{equation}$$

and then observe what happens to the eigenstates and eigenvalues of this Hamiltonian as \\(<b>X</b>\\) is taken through its set over time. The time scale over which \\(<b>X</b>\\) changes is much longer than the time scale over which wavefunction phases change, that is, the time scale over which \\(<b>X</b>\\) changes is much slower than \\(E/\bhat\\), where \\(E\\) is an energy eigenvalue. If we consider the eigenvalues and eigenvectors of this Hamiltonian, they will depend on time (of course via \\(<b>X</b>\\) as well):

$$\begin{equation}
\hat{H}(<b>X</b>(t))\ket{\phi_n(t)} = E_n(t)\ket{\phi_n(t)}.
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

We can simplify the expression with \\(\dot{\theta}_n(t)\\), as well as the right hand side since \\(\ket{\phi_n(t)}\\) since it's an eigenvector

$$\begin{equation}
i\hbar\sum_n\left(\dot{a}_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} - a_n(t)\frac{i}{\hbar}E_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} + a_n(t)e^{i\theta_n(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}\right) = \sum_n a_n(t)e^{i\theta_n(t)}E_n(t)\ket{\phi_n(t)}
\end{equation}$$

This allows us to cancel out the right hand side with the second term on the left hand side:

$$\begin{equation}
i\hbar\sum_n\left(\dot{a}_n(t)e^{i\theta_n(t)}\ket{\phi_n(t)} + a_n(t)e^{i\theta_n(t)}\frac{\partial}{\partial t}\ket{\phi_n(t)}\right) = 0 
\end{equation}$$

Next, we take the inner product with \\(\bra{\phi_m(t)}\\). This will simplify the equation because, at each time \\(t\\), \\(\bra{\phi_m(t)}\ket{\phi_n(t)} = \delta_{mn}\\). This gives us 

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

and then we take the inner product with \\(\bra{\phi_m(t)}\\), which gives 

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

Plugging this into the formula for \\(\dot{a}_m\\), we find 

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

so that \\(a_m(t) = a_m(0)e^{i\gamma_m(t)}\\). This phase \\(\gamma_m(t)\\) is known as the geometric phase. 

