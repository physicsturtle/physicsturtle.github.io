---
layout: lesson
title: Propagator as a Path Integral 
dept: physics
course: qm-V
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics V
unitDisplay: Unit 2
---

From the previous section, we learned that the <i>propagator</i> of a single-particle quantum system in 1-dimension  is given by 

$$\begin{equation}
K(\x,t;\x',t') = \bra{\x}\hat{U}(t,t')\ket{\x'}.
\end{equation}$$

In this section, we will discuss how to evaluate this object for time-independent Hamiltonians. The situation becomes much more complicated when the Hamiltonian depends on time. In the special case that the Hamiltonian is time independent, the time evolution operator is given by 

$$\begin{equation}
\hat{U}(t,t') = e^{-i\hat{H}(t-t')/\hbar}.
\end{equation}$$

We further specialize to the case where the Hamiltonian is of the form

$$\begin{equation} \label{eq:1D_hamil}
\hat{H} = \frac{\hat{p}^2}{2m} + V(\hat{\x}),
\end{equation}$$

where \\(V(\hat{\x})\\) is some potential. Note that this Hamiltonian is time independent. Furthermore, note that we are not considering cases where e.g. there is a classical electromagnetic field coupled to the particle; we will discuss that in a coming section. Equipped with a Hamiltonian of this form, we first rewrite the propagator by defining \\(T = t-t'\\), and \\(\epsilon = T/N\\). We further define \\(\x = \x_N\\) and \\(\x' = \x_0\\). The parameter \\(N\\) is imagined to be very large; we will take a limit later on and send \\(\epsilon \to 0\\). Then, the propagator can be rewritten as 

$$\begin{align}
K(\x_N,t;\x_0,t') =& \bra{\x_N}e^{-i\hat{H}T/\hbar}\ket{\x_0} \\
=& \bra{\x_N}\underbrace{\left(e^{-i\hat{H}\epsilon/\hbar}\right)\cdot \left(e^{-i\hat{H}\epsilon/\hbar}\right)\cdots \left(e^{-i\hat{H}\epsilon/\hbar}\right)}_{N\,\text{times}}\ket{\x_0}
\end{align}$$

Next, we insert the identity \\(\int\ket{\x}\bra{\x} \d\x\\) in between each factor of \\(e^{-i\hat{H}\epsilon/\hbar}\\). This amounts to inserting the identity \\(N-1\\) times. Doing this, the propagator is rewritten as

$$\begin{equation}
K(\x_N,t;\x_0,t') = \bra{\x_N}e^{-i\hat{H}\epsilon/\hbar}\left(\int \ket{\x_{N-1}}\bra{\x_{N-1}} \d\x_{N-1}\right) e^{-i\hat{H}\epsilon/\hbar}\cdots \left(\int \ket{\x_{1}}\bra{\x_{1}} \d\x_1\right)e^{-i\hat{H}\epsilon/\hbar}\ket{\x_0}.
\end{equation}$$

We rearrange the notation by bringing all the integrals to the front, and the differentials to the back:

$$\begin{align} 
K(\x_N,t;\x_0,t') =& \int \bra{\x_N} e^{-i\hat{H}\epsilon/\hbar} \ket{\x_{N-1}} \cdots \ket{\x_1}\bra{\x_1}e^{-i\hat{H}\epsilon/\hbar}\ket{\x_0} \d\x_1 \cdots \d\x_{N-1} \label{eq:disc_path_int} \\
=& \int K(\x_N,\epsilon;\x_{N-1},0) \cdots K(\x_2,\epsilon;\x_1,0) K(\x_1,\epsilon;\x_0,0) \d\x_1 \cdots \d\x_{N-1} 
\end{align}$$

Let's focus now on a specific term in this product. 

$$\begin{equation}
K(\x_n,\epsilon;\x_{n-1},0) = \bra{\x_n} e^{-i\hat{H}\epsilon/\hbar} \ket{\x_{n-1}}.
\end{equation}$$

To evaluate this, we will take advantage of the fact that \\(\epsilon\to 0\\), and perform a simplification. The simplification also relies on the explicit form Eq. \eqref{eq:1D_hamil} of the Hamiltonian. The time evolution operator for very small \\(\epsilon\\) can be rewritten as 

$$\begin{align}
\exp\left(-\frac{i\hat{H}\epsilon}{\hbar}\right) =& \exp\left(-\frac{i\epsilon\hat{p}^2}{2m\hbar} - i\frac{\epsilon V(\hat{x})}{\hbar}\right) \\
\sim & \exp\left(-\frac{i\epsilon\hat{p}^2}{2m\hbar}\right) \exp\left(-\frac{i\epsilon V(\hat{x})}{\hbar}\right)
\end{align}$$

The reason we can split up the product like this is because, if we included the other terms in the Baker-Campbell-Hausdorff formula, they would be higher order in \\(\epsilon\\), and we will take \\(\epsilon\to 0\\) at the end of the calculation. Now, it is much easier to evaluate the matrix element:

$$\begin{align}
\bra{x_n} e^{-i\hat{H}\epsilon/\hbar} \ket{x_{n-1}} =& \bra{x_n}  e^{-i\epsilon\hat{p}^2/2m\hbar} e^{-i\epsilon V(\hat{x})/\hbar} \ket{x_{n-1}} \\
=& \bra{x_n}  e^{-i\epsilon\hat{p}^2/2m\hbar} \ket{x_{n-1}} e^{-i\epsilon V(x_{n-1})/\hbar}
\end{align}$$

Now we have the exponential of the momentum operator. To deal with this, we will insert the identity 

$$\begin{equation}
\1 = \int \ket{p}\bra{p}\d p
\end{equation}$$

Doing this, we get 

$$\begin{align}
\bra{x_n} e^{-i\hat{H}\epsilon/\hbar} \ket{x_{n-1}} =& \int \bra{x_n} e^{-i\epsilon\hat{p}^2/2m\hbar} \ket{p}\bra{p}\ket{x_{n-1}} \d p e^{-i\epsilon V(x_{n-1})/\hbar} \\
=& \int \bra{x_n} \ket{p}\bra{p}\ket{x_{n-1}} e^{-i\epsilon p^2/2m\hbar} \d p e^{-i\epsilon V(x_{n-1})/\hbar}
\end{align}$$

Now, we use the wave function representation of the momentum eigenstates:

$$\begin{equation}
\bra{x}\ket{p} = \frac{e^{i p x/\hbar}}{\sqrt{2\pi\hbar}}.
\end{equation}$$

Plugging these in, we find that 

$$\begin{align}
\bra{x_n} e^{-i\hat{H}\epsilon/\hbar} \ket{x_{n-1}} =& \frac{1}{2 \pi\hbar} \left(\int e^{ipx_n/\hbar} e^{-ipx_{n-1}/\hbar} e^{-i\epsilon p^2/2m\hbar}  \d p \right) e^{-i\epsilon V(\hat{x}_{n-1})/\hbar} \\
=& \frac{e^{-i\epsilon V(x_{n-1})/\hbar}}{2\pi\hbar} \int e^{-i\epsilon p^2/2m\hbar + ip(x_n - x_{n-1})/\hbar }  \d p  \\
=& \frac{e^{-i\epsilon V(\hat{x}_{n-1})/\hbar} }{2\pi\hbar}\int \exp\left(-\frac{i\epsilon}{2m\hbar}\left(p^2 - \frac{2m}{\epsilon}(x_n - x_{n-1})p\right)\right) \d p 
\end{align}$$

We now complete the square of the expression inside the exponential, which yields 

$$\begin{align}
\bra{x_n} e^{-i\hat{H}\epsilon/\hbar} \ket{x_{n-1}} =& \frac{e^{-i\epsilon V(x_{n-1})/\hbar}}{2pi\hbar} \int \exp\left\{-\frac{i\epsilon}{2m\hbar}\left[\left(p - \frac{m}{\epsilon}(x_n-x_{n-1})\right)^2 - \frac{m^2}{\epsilon^2}(x_n-x_{n-1})^2\right] \right\} \d p \\
=& \frac{e^{-i\epsilon V(x_{n-1})/\hbar}}{2\pi\hbar} \exp\left(\frac{im}{2\epsilon\hbar} (x_n - x_{n-1})^2\right) \int \exp\left\{-\frac{i\epsilon}{2m\hbar}\left(p - \frac{m}{\epsilon}(x_n - x_{n-1}) \right)^2 \right\} \d p 
\end{align}$$

where we have pulled out the \\(p\\)-independent term from the integral. We now have an integral over \\(p\\), but with a simple shift. Since \\(p\\) ranges from \\(-\infty\\) to \\(\infty\\), we can remove the shift. 

$$\begin{align}
\bra{x_n} e^{-i\hat{H}\epsilon/\hbar} \ket{x_{n-1}} =& \frac{e^{-i\epsilon V(x_{n-1})/\hbar}}{2\pi\hbar} \exp\left(\frac{im}{2\epsilon\hbar} (x_n - x_{n-1})^2\right) \int \exp\left\{-\frac{i\epsilon}{2m\hbar}p^2 \right\} \d p
\end{align}$$

We evaluate the final integral by using the identity 

$$\begin{equation}
\int_{-\infty}^\infty e^{\pm ir^2} \d r = e^{\pm i\pi/4}\sqrt{\pi}.
\end{equation}$$

We note that the sign in the exponential matters! Using this result, we find that 

$$\begin{align}
K(x_n,\epsilon; x_{n-1},0) =& \bra{x_n} e^{-i\hat{H}\epsilon/\hbar} \ket{x_{n-1}} \\
=&  \frac{e^{-i\epsilon V(x_{n-1})/\hbar}}{2\pi\hbar} \exp\left(\frac{im}{2\epsilon\hbar} (x_n - x_{n-1})^2\right) \sqrt{\frac{2m\pi\hbar}{i\epsilon}} \\
=&  \sqrt{\frac{m}{2\pi \hbar i\epsilon}} \exp\left(\frac{im}{2\epsilon\hbar} (x_n - x_{n-1})^2 -i\frac{\epsilon}{\hbar}  V(x_{n-1})\right) 
\end{align}$$

but we have kept in mind that the \\(i\\) in the denominator of the prefactor is actually \\(i = e^{i\pi/2}\\). (i.e. not \\(e^{-3\pi i/2}\\); this would give the wrong result when taking the square root). Now, we plug this expression into \eqref{eq:disc_path_int} which gives us 

$$\begin{equation}
K(x,t;x',t') = \int \left(\frac{m}{2\pi i \hbar\epsilon}\right)^{N/2} \exp\left\{\frac{i\epsilon}{\hbar}\sum_{n=1}^N \left(\frac{m(x_n - x_{n-1})^2}{2\epsilon^2} - V(x_{n-1})\right)\right\} dx_1\dots dx_{N-1}
\end{equation}$$

with the boundary conditions \\(x(t') = x'\\) and \\(x(t) = x\\). 

where we note that there was a product of \\(N\\) exponentials, but there are only \\(N-1\\) differentials. We can finally move to the continuum by taking \\(N\to\infty\\) (or, equivalently, \\(\epsilon\to 0\\)), which gives us 


$$\begin{equation}
K(x,t;x',t') = \int \exp\left(\frac{i}{\hbar}\int_{t'}^{t} \left(\frac{m\dot{x}^2}{2} - V(x)\right) dt\right) \D x
\end{equation}$$

whereby our notation for the differential means

$$\begin{equation}
\int \D x = \lim_{N\to\infty} \sqrt{\frac{m}{2\pi i \hbar\epsilon}}\prod_{n=1}^{N-1}\int \sqrt{\frac{m}{2\pi i \hbar\epsilon}} dx_n.
\end{equation}$$

We thus recognize the expression inside the exponential as the integral of the Lagrangian, or, the action! 

<div class="result">
<b>Result:</b>
The propagator is written as
 
$$\begin{equation}
K(x,t;x_0,t_0) = \int e^{iS[x]/\hbar} \D x,
\end{equation}$$

where 

$$\begin{equation}
\int \D x = \lim_{N\to\infty} \sqrt{\frac{m}{2\pi i \hbar\epsilon}}\prod_{n=1}^{N-1}\int \sqrt{\frac{m}{2\pi i \hbar\epsilon}} dx_n.
\end{equation}$$

The action is given by

$$\begin{equation}
S[x] = \int_{t'}^{t} \mathcal{L}(x,\dot{x}) \d t
\end{equation}$$

and we have the boundary conditions \(x(t) = x\) and \(x(t') = x_0\). 

</div>

We will now see how to actually evaluate such a path integral. For most cases, this is impossible (or, very difficult), to do exactly. Here, I will present one example of how to do it exactly. We will try some more examples in the exercises. 


Let's consider the case of a quantum particle moving in the simple harmonic oscillator potential. 


