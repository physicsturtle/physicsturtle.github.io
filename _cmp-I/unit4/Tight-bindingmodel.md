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
The tight-binding model considers a system for which the electrons are tightly bound to their atoms. The implications of this is that, even when the electron wave functions on nearby sites overlap, the overlap is not that large, so the resulting localized wave functions closely resemble their atomic constituents. We can derive the energy eigenvalues of such a situation in the following way. We start by considering an isolated atom centred at the origin. The atom has numerous energy levels \\(E_n\\), which are all localized eigenfunctions (such as the wave functions of a hydrogen atom). The Schrödinger equation for such a situation is 

$$\begin{equation}
\Hhat_\text{at}\psi_n(\x) = E_n \psi_n(\x).
\end{equation}$$

The most general atomic wave function is given by a generic superposition of all of the different localized orbitals:

$$\begin{equation}
\phi(\x) = \sum_n a_n \psi_n(\x).
\end{equation}$$

Suppose we now have a lattice made of up atoms at positions \\(\mathbf{R}_i\\) in a Bravais lattice. How can we write a general atomic wave function for an electron which is localized about an atom on site \\(\mathbf{R}_i\\)? Well, we simply have to shift the wave function which we had at the origin to now be centred about site \\(i\\). This wave function would be \\(\phi_i(\x) = \phi(\x-\mathbf{R}_i)\\). Can we construct a Bloch wave function out of these localized orbitals? Well, the answer is yes. The only condition that our Bloch function must satisfy is \\(\Psi(\x + \mathbf{R}) = e^{i\k\cdot\mathbf{R}}\Psi(\x)\\), for any Bravais lattice vector \\(\mathbf{R}\\).  





Consider the tight binding model 

$$\begin{equation}
\Hhat = -t\sum_{\left<i,j\right>} \chat^\dagger_i \chat_j
\end{equation}$$

We now consider a multiorbital tight-binding model. This means that we will have two kinds of creation/annihilation operators. 

$$\begin{equation}
\Hhat =  -\sum_{\left<i,j\right>}\sum_{a,b} t_{ab}\chat^\dagger_{ia} \chat_{jb}
\end{equation}$$

where now we consider hopping between the two orbitals  




