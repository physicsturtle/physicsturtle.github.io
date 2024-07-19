---
layout: lesson
title: The Hubbard-Stratonovich transformation 
dept: physics
course: sft-I
unit: unit4
deptDisplay: Physics
courseDisplay: Statistical Field Theory I
unitDisplay: Unit 4
---
So far, we have studied the Ising model, Heisenberg model, and other classical models. These models are described in terms of very concrete spin degrees of freedom. In order to construct a field theory for the Ising model, we will introduce an extremely important tool known as the <i>Hubbard-Stratonovich transformation</i>. Normally, the Gaussian integral is given by 

$$\begin{align}
\int_{-\infty}^\infty e^{-a\phi^2+b\phi} \d \phi = \sqrt{\frac{\pi}{a}}e^{b^2/4a}.
\end{align}$$

We typically read this equation from left to right; evaluating the integral on the left yields the result on the right hand side. The Hubbard-Stratonovich involves reading this equation from right to left: we can rewrite the exponential \\(e^{b^2/4a}\\) in terms of an integral. This may not appear obvious why it is useful, but we will demonstrate its utility shortly. First, we need a generalization of the Gaussian integral. The appropriate generalization is given by 


$$\begin{align}
\int \exp\left(-\frac{1}{2}\sum_{i,j} \phi_i A_{ij} \phi_j + \sum_i J_i \phi_i \right) \d^d\boldsymbol{\phi} ={}& \exp\left(\frac{1}{2} \mathbf{J}^T A^{-1} \mathbf{J} \right) \sqrt{\frac{(2\pi)^d}{\det(A)}}
\end{align}$$

The Hamiltonian for the ferromagnetic Ising model on the square lattice is given by 

$$\begin{align}
H = -J\sum_{\langle i,j\rangle} \sigma_i \sigma_j - h\sum_i \sigma_i
\end{align}$$

where \\(J > 0\\). The partition function is then written as 

$$\begin{align}
Z = \sum_{\{\sigma_1,\dots,\sigma_N\}} e^{-\beta H[\sigma]}
\end{align}$$

To write this as a field theory, we can use the Hubbard-Stratonovich transformation. To do this, let's first define a vector \\(\boldsymbol{\sigma} = (\sigma_1,\dots,\sigma_N)\\). Then, we can write the Hamiltonian as 

$$\begin{align}
H = - \frac{1}{2}\sum_{i,j} \sigma_i J_{ij} \sigma_j - h\sum_i \sigma_i
\end{align}$$

where \\(J\\) is now a matrix, and \\(J_{ij} = J\\) if \\(i,j\\) are nearest neighbours, and 0 otherwise. Then, in the partition function, we have 

$$\begin{align}
Z ={}& \sum_{\{\sigma_1,\dots,\sigma_N\}} \exp\left(\beta\frac{1}{2}\sum_{ij} \sigma_i J_{ij} \sigma_j + \beta h\sum_i \sigma_i \right) \\
={}& \sum_{\{\sigma_1,\dots,\sigma_N\}} \exp\left(\beta \frac{1}{2} \sum_{ij} \sigma_i J_{ij} \sigma_j\right) \exp\left(\beta h\sum_i \sigma_i \right) \\
={}& \sum_{\{\sigma_1,\dots,\sigma_N\}} \sqrt{\frac{\det(J)}{(2\pi)^N}} \int \exp\left(-\frac{\beta}{2} \sum_{i,j} \phi_i (J^{-1})_{ij} \phi_j + \beta \sum_i \sigma_i \phi_i \right) \mathcal{D}\phi \exp\left(\beta h\sum_i \sigma_i \right)
\end{align}$$

Here, \\(\mathcal{D}\phi = \prod_i \d \phi_i\\). We throw out the constant, and now notice that \\(\sigma_i\\), which previously appeared quadratically, now appears linearly. This means that we can evaluate the sum over \\(\sigma\\) exactly! We find that 

$$\begin{align}
Z ={}& \int \exp\left(-\frac{\beta}{2} \sum_{i,j} \phi_i (J^{-1})_{ij} \phi_j\right) \sum_{\sigma_1=\pm1}\cdots \sum_{\sigma_N=\pm 1} \exp\left(\sum_i \beta(\phi_i + h_i)\sigma_i \right) \mathcal{D}\phi \\
={}& \int \exp\left(-\frac{\beta}{2} \sum_{i,j} \phi_i (J^{-1})_{ij} \phi_j\right) \left(\sum_{\sigma_1} e^{\sigma_1\beta(\phi_1+h_1)}\right) \cdots\left(\sum_{\sigma_N} e^{\sigma_N\beta(\phi_N+h_N)}\right) \mathcal{D}\phi \\
={}& \int \exp\left(-\frac{\beta}{2} \sum_{i,j} \phi_i (J^{-1})_{ij} \phi_j\right) (2\cosh(\beta h_1+\beta \phi_1)) \cdots(2\cosh(\beta h_N + \beta\phi_N))\mathcal{D}\phi \\
={}& \int \exp\left(-\frac{\beta}{2} \sum_{i,j} \phi_i (J^{-1})_{ij} \phi_j\right) 2^N \prod_i \cosh(\beta h_i + \beta \phi_i) \mathcal{D}\phi
\end{align}$$

We can drop the factor of \\(2^N\\), and then take the product and re-exponentiate it. We get 

$$\begin{align}
Z ={}& \int \exp\left(-\frac{\beta}{2} \sum_{i,j} \phi_i (J^{-1})_{ij} \phi_j\right) \exp\left(\sum_i \log \cosh(\beta h_i + \beta \phi_i)\right) \D\phi
\end{align}$$

We can then combine everything into an action, 

$$\begin{align}
S[\phi] = \frac{\beta}{2}\sum_{i,j} \phi_i (J^{-1})_{ij} \phi_j - \sum_i \log \cosh(\beta h_i + \beta \phi_i)
\end{align}$$

and write the partition function as 

$$\begin{align}
Z = \int e^{-S[\phi]} \D\phi
\end{align}$$

Now, we have rewritten the partition function as an integral over magnetization fields at all sites! To appreciate the full utility of this approach, we need to take the continuum limit to transform this into a true field theory.

