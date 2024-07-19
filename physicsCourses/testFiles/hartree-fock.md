---
layout: page
title: Hartree Fock Approximation
course: test
unit: unit1
permalink: /test/hartree-fock/
---

In this section, we will derive the Hartree-Fock approximation for a many electron interacting system. The Hartree-Fock approximation can be implemented numerically, which allows one to find the energies of a many body system. We start with the many body Schrödinger equation. 

Consider a system of $N$ atoms. We do not assume that all the atoms are of the same kind, so the $i$th atom has $n_i$ electrons on it, where $i = 1,\dots,N$. The Hamiltonian for such a system is given by the kinetic energies plus all of the potential energies from the Coulomb interactions. Note that we consider nuclei as single particles with a collective charge rather than a collection of protons and neutrons. Additionally, we work in atomic units where $\hbar = 1$, $4\pi\epsilon_0 = 1$, and the mass of the electron $m_e = 1$. 

$$H = \underbrace{\sum_{i=1}^N \frac{\textbf{P}_i^2}{2M_i}}_{Z_i \text{ kinetic energies}} + \underbrace{\sum_{j=1}^{\sum_i n_i} \frac{\textbf{p}_{j}^2}{2}}_{e^-\text{ kinetic energies}} + \underbrace{\sum_{i=1}^N\sum_{j > i} \frac{Z_i Z_j}{|\textbf{R}_i - \textbf{R}_j|}}_\text{nucleus-nucleus interaction} + \underbrace{ \sum_{i=1}^N\sum_{j=1}^{\sum_k n_k} \frac{-Z_i}{|\textbf{R}_i - \textbf{r}_j|}}_\text{electron-nucleus interaction} + \underbrace{\sum_{j=1}^{\sum_i n_i} \sum_{k > j} \frac{1}{|\textbf{r}_j - \textbf{r}_\ell|}}_{e^-\text{ - } e^- \text{ interaction}} $$

We look for a solution $\left|\Psi\right>$ to the equation 

$$H\left|\Psi\right> = E\left|\Psi\right>.$$

This Hamiltonian is extremely complicated, and we are looking for a function $\Psi$ of $3N + 3\sum_i n_i$ variables (assuming we are working in 3 spatial dimensions). This is an extremely difficult problem, and it cannot be solved without making substantial approximations. 

Part of the Hartree-Fock approximation is the Born-Oppenheimer approximation, which we invoke now.

<div class="result">
<b>Born-Oppenheimer Approximation:</b> The Born-Oppenheimer approximation says that the nuclei of a many body system are stationary, and it is only the electrons which move. This means that we only need to solve the electronic problem, and we can remove two terms from the Hamiltonian. This is a good approximation because the nuclei are much heavier than the electrons. 
</div> <br>

After the Born-Oppenheimer approximation, we are ready to rewrite our Hamiltonian in a much simpler form. We remove the kinetic energy terms for the nuclei, as well as the nucleus-nucleus interaction term. The Hamiltonian becomes

$$H = \sum_{j=1}^{\sum_i n_i} \frac{\textbf{p}_{j}^2}{2} - \sum_{i=1}^N\sum_{j=1}^{\sum_k n_k} \frac{Z_i}{|\textbf{R}_i - \textbf{r}_j|} + \sum_{j=1}^{\sum_i n_i} \sum_{k > j} \frac{1}{|\textbf{r}_j - \textbf{r}_\ell|}.$$

We are now looking for a function $\Psi_\text{elec}$ of $3\sum_i n_i$ variables. This is still too many variables for any numerical computations! 




















































