---
layout: lesson
title: Ising Order 
dept: physics
course: qpt
unit: unit11
deptDisplay: Physics
courseDisplay: Quantum Phase Transitions
unitDisplay: Unit 11
---
The Hubbard Hamiltonian is given by 

$$\begin{equation}
\hat{H} = \sum_{\k\sigma} \epsilon_{\k} \chat^\dagger_{\k\sigma} \chat_{\k\sigma} + U\sum_i \chat^\dagger_{i\uparrow}\chat^\dagger_{i\downarrow} \chat_{i\downarrow} \chat_{i\uparrow}
\end{equation}$$

In terms of the fermionic coherent state path integral, we can write the partition function (in the grand canonical ensemble) as

$$\begin{equation}
Z = \int \exp\left[-\int_0^\beta \left(\sum_{i\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} +H[\bar{c},c]\right)\d\tau\right] \D\bar{c}\D c
\end{equation}$$

We perform the standard Hubbard-Stratonovich decoupling which allows us to rewrite the partition function as 

$$\begin{equation}
Z = \int e^{-S} \D \bar{c} \D c \D m
\end{equation}$$

where the action is given by 

$$\begin{equation}
S = \int_0^\beta\left(\frac{1}{2U}\sum_i m_{i\tau}^2 + \sum_{i\alpha\beta} \sigma^z_{\alpha\beta} m_{i\tau}\bar{c}_{i\tau\alpha}c_{i\tau\beta} + \sum_{i\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} + \sum_{\k\sigma} \xi_{\k} \bar{c}_{\k\tau\sigma} c_{\k\tau\sigma}\right)\d\tau
\end{equation}$$

We can rewrite the partition function as 

$$\begin{align}
Z ={}& \int\exp\left(-\frac{1}{2U}\int_0^\beta \sum_i m_{i\tau}^2 \d\tau\right)\exp\left(-\int_0^\beta\left(\sum_{i\sigma}\bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} + \sum_{\k\sigma} \xi_{\k} \bar{c}_{\k\tau\sigma} c_{\k\tau\sigma} + \sum_{i\alpha\beta}\sigma^z_{\alpha\beta} m_{i\tau}\bar{c}_{i\tau\alpha} c_{i\tau\beta} \right)\d\tau\right) \D\bar{c}\D c \D m \\
={}& Z_0\int\exp\left(-\frac{1}{2U}\int_0^\beta \sum_i m_{i\tau}^2 \d\tau\right)\left\langle \exp\left(-\int_0^\beta \sum_{i\alpha\beta}\sigma^z_{\alpha\beta} m_{i\tau}\bar{c}_{i\tau\alpha} c_{i\tau\beta} \d\tau\right) \right\rangle_0 \D m
\end{align}$$

We then end up with a functional \\(S_\text{eff}\\) describing the theory: 

$$\begin{equation}
S_\text{eff}[m] = \frac{1}{2U}\int_0^\beta\sum_i m_{i\tau}^2\d\tau - \log \left<\exp\left(-\int_0^\beta \sum_{i\alpha\beta}\sigma^z_{\alpha\beta} m_{i\tau}\bar{c}_{i\tau\alpha} c_{i\tau\beta} \d\tau\right) \right>_0
\end{equation}$$

Although this is exact so far, it is not possible to exactly evaluate the expectation value. We therefore have to do it perturbatively in powers of \\(\Psi\\). Defining 

$$\begin{equation}
\Delta S_\text{eff}[m] =  - \log \left<\exp\left(-\int_0^\beta \sum_{i\alpha\beta}\sigma^z_{\alpha\beta} m_{i\tau}\bar{c}_{i\tau\alpha} c_{i\tau\beta} \d\tau\right) \right>_0,
\end{equation}$$

We start by rewriting the quantity as a determinant of a rather complicated matrix. To do this, we will use the identity 

$$\begin{equation}
\int \exp\left(-\sum_{\alpha\beta}\bar{\psi}_\alpha A_{\alpha\beta} \psi_\beta\right) \D\bar{\psi} \D\psi = \det(A)
\end{equation}$$


<div class="remark">
<b>Remark:</b>
Is it permissible to integrate out the gapless fermions? 

</div>


