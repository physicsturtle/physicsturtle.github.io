---
layout: lesson
title: Hydrogen Atom and Rigid Rotor
dept: physics
course: qm-I
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics I
unitDisplay: Unit 2
---

In both classical and quantum physics, a rigid rotor is a 3-dimensional rotating system. For example, a top, a figure skater, a water molecule are all examples of rigid rotors. To describe such a system classically, one can solve Newton's equation for a rigid body or solve the Euler-Lagrange equations. In quantum mechanics, we are generally concerned with rigid rotors that have certain symmetries. In this course, the only rigid rotor that we will consider is the two body rotor. The hydrogen molecule falls under this category, and the bodies are the proton (nucleus) and the electron. 

### Hydrogen Atom
The hydrogen atom is a two body system. This means that its (classical) Hamiltonian is described by the kinetic energies of the proton and electron, as well as an interaction term. The interaction is the Coulomb force. Mathematically, this Hamiltonian is 

$$H = \frac{\textbf{p}_p^2}{2m_p} + \frac{\textbf{p}_e^2}{2m_e} - \frac{e^2}{4\pi\epsilon_0 r},$$

where 
* $p_p$ is the momentum of the proton
* $p_e$ is the momentum of the electron
* $m_p$ is the mass of the proton
* $m_e$ is the mass of the electron
* $r$ is the distance between the proton and the electron
* $e$ is the charge of the proton. 

In classical mechanics, one makes the following coordinate transformations:

$$\textbf{R} = \frac{1}{2}(\textbf{r}_e + \textbf{r}_p),\qquad \textbf{r} = \textbf{r}_e - \textbf{r}_p.$$

If one performs these substitutions, then the Hamiltonian becomes 

$$H = \frac{\textbf{P}^2}{2M} + \frac{\textbf{p}^2}{2\mu} - \frac{e^2}{4\pi\epsilon_0 r^2},$$

where $\textbf{P}$ is the total momentum of the system (so $\textbf{P}$ is conserved), and $\textbf{p}$ is an effective momentum term describing the rate of change of the distance between the two particles. Since $\textbf{P}$ is conserved, it is constant, and may be removed from the Hamiltonian without loss of generality. We now rewrite our Hamiltonian as 

$$H = \frac{\textbf{p}^2}{2\mu} - \frac{e^2}{4\pi\epsilon_0 r}.$$

If we rewrite this Hamiltonian in its quantum form by setting 

$$\textbf{p} = -i\hbar \nabla,$$

then we get 

$$H = -\frac{\hbar^2}{2\mu}\nabla^2 - \frac{e^2}{4\pi\epsilon_0 r}.$$

This Hamiltonian can be solved exactly! 



