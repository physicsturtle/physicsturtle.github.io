---
layout: lesson
title: Schrodinger Picture 
dept: physics
course: many-body-I
unit: unit6
deptDisplay: Physics
courseDisplay: Many Body Physics I
unitDisplay: Unit 6
---
In the Schrödinger picture, the states are time dependent and the operators are time independent. States obey the Schrödinger equation

$$\begin{equation} \label{eq:schr_equation}
i\hbar\frac{\partial}{\partial t}\ket{\Psi_S(t)} = \hat{H}(t)\ket{\Psi_S(t)},
\end{equation}$$

where the Hamiltonian \\(\hat{H}(t)\\) is potentially time dependent. Whether or not the Hamiltonian is time dependent, we can write the evolution of a state at time \\(t\\) to a time \\(t'\\) in terms of the <i>time evolution operator</i> \\(\hat{U}(t',t)\\). 

$$\begin{equation} \label{eq:time_evolution}
\ket{\Psi_S(t')} = \hat{U}(t',t)\ket{\Psi_S(t)}
\end{equation}$$

If we plug \eqref{eq:time_evolution} into \eqref{eq:schr_equation}, then we find that 

$$\begin{equation}
i\hbar\frac{\partial}{\partial t'}\ket{\Psi_S(t')} = \frac{\partial}{\partial t'}\hat{U}(t',t) \ket{\Psi_S(t)}
\end{equation}$$

Then, we use the Schrödinger equation to rewrite the left hand side as

$$\begin{equation}
\hat{H}(t')\ket{\Psi_S(t')} = \frac{\partial}{\partial t'}\hat{U}(t',t) \ket{\Psi_S(t)}
\end{equation}$$

Now, we write the \\(\ket{\Psi\_S(t')} = \hat{U}(t',t)\ket{\Psi(t)}\\), and get 

$$\begin{equation}
\hat{H}(t')  \hat{U}(t',t)\ket{\Psi_S(t)} = i\hbar\frac{\partial}{\partial t'}\hat{U}(t',t) \ket{\Psi_S(t)}
\end{equation}$$

Since this equation is to be true for any state \\(\ket{\Psi}\\), we conclude that 

$$\begin{equation}
 i\hbar\frac{\partial}{\partial t'}\hat{U}(t',t) = \hat{H}(t') \hat{U}(t',t)
\end{equation}$$

which is the differential equation for the time evolution operator. In general, to solve this equation is extremely difficult, and it must be expressed as a time-ordered exponential. We will come to this detail later when we develop perturbation theory. For now however, we can discuss some simple cases where we can exactly solve for \\(\hat{U}\\). 

If \\(\hat{H}\\) is a time independent Hamiltonian, then we can solve explicitly for this time evolution operator \\(\hat{U}\\). For a time independent Hamiltonian, we get

$$\begin{equation}
\hat{U}(t',t) = e^{-i\hat{H}(t'-t)/\hbar}.
\end{equation}$$

This allows us to define the Schrödinger states in terms of states at \\(t = 0\\). We can write a state at a general time \\(t\\) by

$$\begin{equation}
\ket{\psi_S(t)} = \hat{U}(t,0)\ket{\psi_S(0)} = e^{-i\hat{H}t/\hbar} \ket{\psi_S(0)} 
\end{equation}$$

We may also write \\(\hat{U}(t,0) = \hat{U}(t)\\).

