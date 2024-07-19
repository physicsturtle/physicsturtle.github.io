---
layout: lesson
title: The Propagator 
dept: physics
course: qm-V
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics V
unitDisplay: Unit 2
---
In quantum mechanics, we typically formulate the idea of time evolution of a quantum state using the time-evolution operator \\(\hat{U}(t,t')\\), which brings a state \\(\ket{\psi(t')}\\) at time \\(t'\\) to a state \\(\ket{\psi(t)}\\) at time \\(t\\):

$$\begin{equation}
\ket{\psi(t)} = \hat{U}(t,t')\ket{\psi(t')}.
\end{equation}$$

Note that everything here is in the Schrödinger picture. This equation can be rewritten in terms of wave functions by acting with \\(\bra{\x}\\) on both sides from the left:

$$\begin{equation}
\bra{\x}\ket{\psi(t)} = \bra{\x}\hat{U}(t,t')\ket{\psi(t')}.
\end{equation}$$

We can then express this in terms of matrix elements of the time evolution operator by inserting the identity

$$\begin{equation}
\bra{\x}\ket{\psi(t)} = \int \bra{\x}\hat{U}(t,t')\ket{\x'}\bra{\x'} \ket{\psi(t')} \d \x'. 
\end{equation}$$

Now, writing this in terms of wave functions, we find that 

$$\begin{equation}
\psi(\x,t) = \int \bra{\x}\hat{U}(t,t')\ket{\x'} \psi(\x',t') \d \x'. 
\end{equation}$$

<div class="definition">
<b>Definition:</b>
We define the integral kernel 

$$\begin{equation}
K(\x,t;\x',t') = \bra{\x}\hat{U}(t,t')\ket{\x'}
\end{equation}$$

as the <i>propagator</i>. We can therefore see that the propagator is very similar to the time-evolution operator; it is simply the matrix elements of the time-evolution operator. We note that the propagator is (very similar? same?) to the Green functions that we will define later in the course. The interpretation of this kernel is the transition amplitude between a particle at \(\x\) at time \(t\) and a particle at \(\x'\) at another time \(t'\). Thus the time evolution for the wave function becomes 

\(\)\psi(\x,t) = \int_{-\infty}^\infty K(\x,t;\x',t')\psi(x',t')\d \x'\(\)

</div>

The propagator is, except for the simplest examples, extremely difficult to calculate. We therefore refer to perturbation theory for the calculation of most propagators. Even for simple examples, the calculation of the propagator seems quite opaque at this stage (unless the position operator is an eigenstate of the time evolution operator). 

