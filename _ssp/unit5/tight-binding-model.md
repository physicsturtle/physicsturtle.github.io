---
layout: lesson
title: Tight Binding Model
dept: physics
course: ssp
unit: unit5
deptDisplay: Physics
courseDisplay: Solid State Physics
unitDisplay: Unit 5
---

In this section, we will outline another method for calculating band structures. As per its name, it assumes that electrons primarily experience the potential due to atoms in the lattice, and the perturbation is the effect of neighbouring atoms. This can be constrasted with the nearly free electron model, in which the electrons were primarily free, and the perturbation was the effect of a small periodic potential. 

The tight binding model is well suited for wide gap insulators in which the wave function overlap between neighbouring atoms is small, and the distance between neighbouring atoms is large. 

Consider the wave function $\psi(\r)$ an electron moving in the potential created by a single atom. Then, an electron moving in the potential created by an atom which is at $\textbf{R}$ would be $\psi(\r-\textbf{R})$. Let's define a superposition state of the electrons in each of the potentials of their atoms:

$$\psi)\k(\r) = \sum_\textbf{R} e^{i\k\cdot\textbf{R}}\psi(\r-\textbf{R}).$$

where $\textbf{R}$ ranges over all Bravais lattice vectors, but we restrict $\k$ to the first Brillouin zone. This wave function obeys Bloch's theorem, where 

$$u_\k(\r) = \sum_\textbf{R} e^{i\k\cdot(\textbf{R} - \r)}\psi(\r-\textbf{R}).$$

We thus estimate the energy of the electron by taking the expectation value of the Hamiltonian in our ansatz state $\psi_\k(\r)$. 






