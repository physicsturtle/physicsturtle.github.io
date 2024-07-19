---
layout: lesson
title: Path Integral for a Fermionic Field Theory 
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
In this section, we will formulate the partition function for a field theory of fermions. We will do this in the grand canonical ensemble. We will employ the generalized expressions for the trace and identity formulated in Section ??, because the Hilbert space now contains many accessible single-particle states. The expression for the partition function is given by 

$$\begin{equation}
\mathcal{Z} = \tr e^{-\beta (\Hhat-\mu\hat{N})}.
\end{equation}$$

We want to formulate the calculation of the partition function in terms of a path integral. We have already seen how to calculate the trace of an operator as an integral over Grassmann numbers. The trace of the operator \\(e^{-\beta H}\\) is

$$\begin{equation}
\mathcal{Z} = \int\bra{\{-\bar{c}\}}e^{-\beta \Hhat}\ket{\{c\}} e^{-\bar{c}c}\d\bar{c}\d c
\end{equation}$$

where we are using the short notation \\(\ket{\{c\}} = \ket{\{c_{i\sigma}\}}\\), \\(\bra{\{-\bar{\psi}\}} = \bra{\{-\bar{c}_{i\sigma}\}}\\). This enumerates all states in our system. We also write 

$$\begin{equation}
\bar{c}c = \sum_{i\sigma} \bar{c}_{i\sigma} c_{i\sigma},
\end{equation}$$

and the differential \\(\D\bar{c}_0 = \prod_{i\sigma} \d\bar{c}_{i0\sigma}\\), \\(\D c_0 = \prod_{i\sigma} \d c_{i0\sigma}\\). Before moving on to rewriting the partition function as a path integral, relabel the \\(c\\) and \\(\bar{c}\\) to have a subscript 0:

$$\begin{equation}
\mathcal{Z} = \int\bra{\{-\bar{c}_0\}}e^{-\beta \Hhat }\ket{\{c_0\}} e^{-\bar{c}_0 c_0} \D\bar{c}_0\D c_0
\end{equation}$$

Let us now formulate this partition function in terms of a path integral. We apply the <i>Trotter decomposition</i> by rewriting the exponential of the Hamiltonian as follows:

$$\begin{equation}
e^{-\beta \Hhat} = (e^{-\epsilon \Hhat})^N
\end{equation}$$

where \\(\epsilon = \beta/N\\). The final step of the computation will be to take \\(N\to\infty\\), but for now just think of \\(N\\) is a very large number. In between each of these \\(N\\) factors, we insert the identity in terms of a Grassmann integral (see Eq. ??). We will label the \\(\psi\\) Grassmann numbers with an index \\(n=1,\dots,N\\) for each identity that we insert. 

$$\begin{align}
\mathcal{Z} ={}& \int \bra{\{-c_{0}\}} \underbrace{e^{-\epsilon\Hhat} \cdots e^{-\epsilon\Hhat}}_{N\text{-times}} \ket{\{c_{0}\}} e^{-\bar{c}_0c_0} \D \bar{c}_{0} \D c_{0} \\
={}& \int\bra{\{-\bar{c}_0\}}(e^{-\epsilon\Hhat})\1\cdots \1(e^{-\epsilon\Hhat})\ket{\{c_0\}} e^{-\bar{c}_0c_0} \D\bar{c}_0 \D c_0
\end{align}$$

In between the \\(N\\) factors, we can insert \\(N-1\\) resolutions of the identity. We recall that 

$$\begin{equation}
\1 = \int\ket{\{c\}}\bra{\{\bar{c}\}}\exp\left(-\sum_{i\sigma} \bar{c}_{i\sigma}c_{i\sigma}\right)\D\bar{c}\D c,
\end{equation}$$

whereby \\(\{c\}\\) contains the states for all sites, \\(\D c = \prod_{i\sigma} \d c_{i\sigma}\\), and \\(\D\bar{c} = \prod_{i\sigma} \d \bar{c}_{i\sigma}\\). 

Doing this, we find (setting \\(c_N = -c_0\\))

$$\begin{align}
\mathcal{Z} ={}& \int \bra{\{c_{N}\}} e^{-\epsilon\Hhat}\ket{\{c_{N-1}\}} \bra{\{c_{N-1}\}} \cdots \ket{\{c_1\}} \bra{\{c_1\}} e^{-\epsilon\Hhat} \ket{\{c_{0}\}} e^{-\bar{c}_0c_0} \cdots e^{- \bar{c}_{N-1}c_{N-1}} \prod_{n=1}^N \D \bar{c}_{n} \D c_{n} \\
={}& \int \bra{\{c_{N}\}} e^{-\epsilon\Hhat}\ket{\{c_{N-1}\}} \left[\prod_{n=1}^{N-1} \bra{\{c_n\}} e^{-\epsilon\Hhat} \ket{\{c_{n-1}\}}\right] e^{-\bar{c}_0c_0} \cdots e^{-\bar{c}_{N-1}c_{N-1}} \prod_{n=1}^N \D \bar{c}_{n} \D c_{n} \\
={}& \int \left[\prod_{n=1}^{N} \bra{\{c_n\}} e^{-\epsilon\Hhat} \ket{\{c_{n-1}\}}\right] e^{-\bar{c}_0c_0} \cdots e^{-\bar{c}_{N-1}c_{N-1}}\prod_{n=1}^N \D \bar{c}_{n} \D c_{n}
\end{align}$$

We are now tasked with computing the matrix element \\(\bra{\{c_n\}} e^{-\epsilon\Hhat} \ket{\{c_{n-1}\}}\\). To compute this, let us employ a Taylor expansion, which is valid because \\(N\\) is large and thus \\(\epsilon = \beta/N\\) is small. Doing this, we find 

$$\begin{align}
\bra{\{c_n\}} e^{-\epsilon\Hhat} \ket{\{c_{n-1}\}}\sim & \bra{\{c_n\}} (1 - \epsilon\Hhat[\chat^\dagger,\chat]) \ket{\{c_{n-1}\}} \\
={}& \bra{\{c_n\}} (1 - \epsilon\Hhat[\bar{c}_n,c_{n-1}]) \ket{\{c_{n-1}\}} \\
={}& \bra{\{c_n\}}\ket{\{c_{n-1}\}} (1 - \epsilon\Hhat[\bar{c}_n,c_{n-1}]) 
\end{align}$$

We have replaced \\(\chat^\dagger\\) by \\(\bar{c}\\) and \\(\chat\\) by \\(c\\) in the Hamiltonian because it is normal ordered, and the coherent states are eigenstates of the annihilation operator. Next, since \\(\epsilon\\) is small, we re-exponentiate this and also use the overlap formula for coherent states

$$\begin{align}
\bra{\{c_n\}} e^{-\epsilon\Hhat} \ket{\{c_{n-1}\}} \sim e^{\bar{c}_nc_{n-1}} e^{- \epsilon\Hhat[\bar{c}_n,c_{n-1}]} 
\end{align}$$

Plugging this back in to the partition function, we find that 

$$\begin{align}
\mathcal{Z} ={}& \int \left[\prod_{n=1}^{N} e^{\bar{c}_nc_{n-1}} e^{- \epsilon\Hhat[\bar{c}_n,c_{n-1}]} \right] e^{-\bar{c}_0c_0} \cdots e^{-\bar{c}_{N-1}c_{N-1}}\prod_{n=1}^N \D \bar{c}_{n} \D c_{n} \\
={}& \int \exp\left(-\left[\sum_{n=1}^N \frac{\bar{c}_n(c_n - c_{n-1})}{\epsilon}\epsilon + \epsilon H[\bar{c}_n,c_{n-1}]\right]\right)\prod_{n=1}^N \D\bar{c}_n \D c_n \\
={}& \int \exp\left(-\left[\sum_{n=1}^N \frac{\bar{c}_n(c_n - c_{n-1})}{\epsilon} + H[\bar{c}_n,c_{n-1}]\right]\epsilon\right)\prod_{n=1}^N \D\bar{c}_n \D c_n
\end{align}$$

Let's now write \\(c_n = c(\tau_n)\\), where \\(\tau_n = n\epsilon\\). This means that

$$\begin{equation}
\frac{c_{n} - c_{n-1}}{\epsilon} \sim \frac{\partial}{\partial\tau}c(\tau_n). 
 \end{equation}$$

We recognize this as a Riemann sum! We therefore change the \\(n\\) index to \\(\tau_n = n\epsilon = \beta n/N\\) and write this as an integral from \\(\tau = 0\\) to \\(\beta\\). This gives us 

$$\begin{align}
\mathcal{Z} ={}& \int \exp\left(-\int_0^\beta \left(\bar{c}_\tau \partial_\tau c_\tau + H[\bar{c},c]\right)\d\tau \right) \D c \D c \\
={}& \int \exp\left(-\int_0^\beta \left(\sum_{i\sigma} \bar{c}_{i\tau\sigma} \partial_\tau c_{i\tau\sigma} + H[\bar{c},c]\right)\d\tau \right) \D c \D c
\end{align}$$

Where we restored the longhand notation for \\(\bar{c}c\\) as the sum over all sites and spins, as well as define \\(\D c = \lim_{N\to\infty}\prod_{n=1}^N \D c_n = \prod_{\tau\in[0,\beta]} \D \bar{c}(\tau)\D c(\tau)\\). This is not a rigorous notation, but it suffices. We then define the action

$$\begin{equation}
S = \int_0^\beta \left(\sum_{i\sigma} \bar{c}_{i\tau\sigma}\partial_\tau c_{i\tau\sigma} + H[\bar{c},c]\right)\d\tau
\end{equation}$$

where the Hamiltonian should include the \\(-\mu N\\) term because this is technically a grand partition function. Thus, the grand partition function becomes 

$$\begin{equation}
\mathcal{Z} = \int e^{-S}\D \bar{c}\D c.
\end{equation}$$


   
   
   
 
   
   
 
   
 
   
 
 
   
   
 
     
