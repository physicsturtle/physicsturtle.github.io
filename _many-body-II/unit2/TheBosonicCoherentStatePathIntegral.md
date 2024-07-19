---
layout: lesson
title: The Bosonic Coherent State Path Integral 
dept: physics
course: many-body-II
unit: unit2
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 2
---
We wish to generalize the discussion to theories of bosons on a lattice. In this situation, we obviously do not just have one type of particle which may occupy many different states. Instead, we have many different possible occupiable states (e.g. different sites on a lattice), and many different possible occupation numbers of the bosons on each site. This requires us to generalize the coherent states of the previous section. These new coherent states satisfy 

$$\begin{equation}
\bhat_{i\alpha}\ket{b} = b_{i\alpha}\ket{b}
\end{equation}$$

The point of this property is that when we have the Hamiltonian \\(\Hhat[\bhat^\dagger,\bhat]\\), its matrix elements in terms of bosonic coherent states will be 

$$\bra{b}\Hhat[\bhat^\dagger,\bhat]\ket{b'} = H[b^{*},b'].$$

where \\(b\\) represents all variables at each site of the lattice and for each spin. We can actually write this multivariable coherent state as 

$$\ket{b} = e^{-\sum_{i\alpha} \|b_{i\alpha}\|^2} e^{\sum_{i\alpha} b_{i\alpha} \bhat^\dagger_{i\alpha}}\ket{0}$$

Then, we see that 


Let us now construct the bosonic coherent state path integral. We want to evaluate the partition function

$$\mathcal{Z} = \tr e^{-\beta\Hhat}$$

where \\(\Hhat\\) includes the subtraction of \\(\mu\Nhat\\) in it already. Thus the trace is over the entire Fock space. We write the trace using our formula above. 

$$\mathcal{Z} = \int \bra{\{b_{0}\}} e^{-\beta \Hhat} \ket{\{b_{0}\}} \frac{\D b^{*}_{0} \D b_{0}}{\pi}$$ 

where \\(\ket{\{b_0\}}\\) runs over all sites in the lattice, and \\(\D b_0\\) also runs over all sites in the lattice. Next, we perform a Trotter decomposition by writing

$$e^{-\beta \Hhat} = \left(e^{-\epsilon\Hhat}\right)^N$$

where \\(\epsilon = \beta/N\\). Thus 

$$\mathcal{Z} = \int \bra{\{b_{0}\}} \underbrace{e^{-\epsilon\Hhat} \cdots e^{-\epsilon\Hhat}}_{N\text{-times}} \ket{\{b_{0}\}} \frac{\D b^{*}_{0} \D b_{0}}{\pi}$$ 

In between the \\(N\\) factors, we can insert \\(N-1\\) resolutions of the identity. Doing this, we find 

$$\begin{align}
\mathcal{Z} ={}& \int \bra{\{b_{0}\}} e^{-\epsilon\Hhat}\ket{\{b_{N-1}\}} \bra{\{b_{N-1}\}} \cdots \ket{\{b_1\}} \bra{\{b_1\}} e^{-\epsilon\Hhat} \ket{\{b_{0}\}} \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N} \\
={}& \int \bra{\{b_{N}\}} e^{-\epsilon\Hhat}\ket{\{b_{N-1}\}} \left[\prod_{n=1}^{N-1} \bra{\{b_n\}} e^{-\epsilon\Hhat} \ket{\{b_{n-1}\}}\right] \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N} \\
={}& \int \left[\prod_{n=1}^{N} \bra{\{b_n\}} e^{-\epsilon\Hhat} \ket{\{b_{n-1}\}}\right] \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N} \\
\end{align}$$

where we set \\(b_0 = b_N\\). Let us consider one of the terms in this product. Namely, 

$$\bra{\{b_i\}} e^{-\epsilon\Hhat} \ket{\{b_{i-1}\}}$$

We want to replace the operators by their eigenvalues with respect to the coherent states. However, this is only possible for a normal ordered expression. Since the exponential scrambles things up and they aren't normal ordered anymore, this appears to not be possible! However, in the limit \\(\epsilon\to 0\\), this is actually possible. This is because 

$$\begin{align}
\bra{\{b_n\}} e^{-\epsilon\Hhat} \ket{\{b_{n-1}\}} \approx & \bra{\{b_n\}} (1 - \epsilon\Hhat[\bhat^\dagger,\bhat]) \ket{\{b_{n-1}\}} + O(\epsilon^2) \\
={}&\bra{\{b_n\}} (1 - \epsilon H[b^{*}_n ,b_{n-1}]) \ket{\{b_{n-1}\}} + O(\epsilon^2) \\
={}&\bra{\{b_n\}}\ket{\{b_{n-1}\}}(1 - \epsilon H[b^{*}_n ,b_{n-1}])  + O(\epsilon^2) \\
\approx & \exp\left(-\frac{1}{2}\sum_i \|b_{in}\|^2 - \frac{1}{2}\sum_i \|b_{i,n-1}\|^2 + \sum_i b_{in}^{*} b_{i,n-1}\right) e^{-\epsilon H[b_n^{*}, b_{n-1}]} + O(\epsilon^2)
\end{align}$$

Now, if we plug this into the path integral, we find 

$$\begin{align}
\mathcal{Z} ={}& \int \left[\prod_{n=1}^N \exp\left(-\frac{1}{2}\sum_i \|b_{in}\|^2 - \frac{1}{2}\sum_i \|b_{i,n-1}\|^2 + \sum_i b_{in}^{*} b_{i,n-1}\right) e^{-\epsilon H[b_n^{*}, b_{n-1}]}\right] \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N} \\
={}& \int \left[\prod_{n=1}^N \exp\left(-\sum_i \|b_{i,n}\|^2 + \sum_i b_{in}^{*} b_{i,n-1}\right) e^{-\epsilon H[b_n^{*}, b_{n-1}]}\right] \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N} \\
={}& \int \left[\prod_{n=1}^N \exp\left(-\sum_i b_{i,n}^{*}(b_{i,n} - b_{i,n-1})\right) e^{-\epsilon H[b_n^{*}, b_{n-1}]}\right] \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N}
\end{align}$$

Now, we reinterpret the \\(n\\) index as an imaginary time. We call \\(\tau_n = \epsilon n \beta\\). Then, we write this as 

$$\begin{align}
\mathcal{Z} ={}& \int \exp\left(-\sum_{n=1}^N \left[\sum_i  b_{i,n}^{*}\left(\frac{b_{i,n} - b_{i,n-1}}{\epsilon}\right) + H[b_n^{*}, b_{n-1}] \right]\epsilon \right) \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N}
\end{align}$$

As we take the limit \\(\epsilon \to 0\\), the sum over \\(n\\) becomes an integral, and \\(b_{in}\\) becomes a derivative in imaginary time. Furthermore, the difference between the two indices \\(n\\) and \\(n-1\\) in \\(H[b_n^{*}, b_{n-1}]\\) become irrelevant since they are spaced closer and closer together. Thus we can write 

$$\begin{align}
\mathcal{Z} ={}& \int \exp\left(-\int_0^\beta \left[\sum_i  b^{*}_{i\tau} \partial_\tau b_{i\tau} + H[b^{*}, b] \right]\d\tau \right) \D b^{*} \D b
\end{align}$$

where 

$$\D b^{*} \D b = \lim_{N\to\infty} \frac{\D b^{*}_{0} \D b_{0}\D b^{*}_1 \D b_1 \cdots \D b^{*}_{N-1} \D b_{N-1}}{\pi^N}$$

We finally define the action 

$$S = \int_0^\beta \left[\sum_i  b^{*}_{i\tau} \partial_\tau b_{i\tau} + H[b^{*}, b] \right]\d\tau$$

and the partition function is then

$$\mathcal{Z} = \int e^{-S} \D b^{*} \D b$$

