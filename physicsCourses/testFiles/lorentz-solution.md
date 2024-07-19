---
layout: page
title: Particle in Uniform Electromagnetic Field
course: test
unit: unit1
permalink: /test/lorentz-solution/
---

We are interested in solving the differential equation 

$$m\frac{d\textbf{v}}{dt} = q\left(\textbf{E} + \textbf{v}\times\textbf{B}\right)$$

for uniform $\textbf{E}$ and $\textbf{E}$. When we expand out the cross product, we can turn this into a vector differential equation. 

$$m\frac{d\textbf{v}}{dt} = q\textbf{E} + q\underbrace{\begin{pmatrix} 0 & B_3 & -B_2 \\ -B_3 & 0 & B_1 \\ B_2 & -B_1 & 0 \end{pmatrix}}_{B}\textbf{v}$$

To solve this, we can use standard techniques from ODE theory. First we need to find the eigenvalues of the matrix $B$. First note that this is a skew-symmetric matrix, which means that all of its eigenvalues will have zero real part, i.e. all nonzero eigenvalues will be purely imaginary. Recall the definition of the matrix exponential. If $A$ is a matrix, then its exponential is defined by 

$$e^{A} = \sum_{n=0}^\infty \frac{A^n}{n!}$$

If we now include a variable $t$, then 

$$e^{At} = \sum_{n=0}^\infty \frac{A^n t^n}{n!}$$

This also means that its derivative is 

$$\begin{eqnarray}
\frac{d}{dt} e^{At} &=& \frac{d}{dt} \sum_{n=0}^\infty \frac{A^n t^n}{n!}\\
&=& \sum_{n=1}^\infty \frac{A^n t^{n-1}}{(n-1)!} \\
&=& \sum_{n=0}^\infty \frac{A^{n+1} t^{n}}{n!} \\
&=& A\left(\sum_{n=0}^\infty \frac{A^n t^{n}}{n!}\right)\\
&=& Ae^{At}\\
\end{eqnarray}$$

This also implies that 

$$\frac{d}{dt} e^{At} = A e^{At} = e^{At} A.$$

for differentiation, and that if $A$ is invertible, 

$$\int e^{At} dt = A^{-1} e^{At} = e^{At} A^{-1}.$$

Now we are ready to solve the ODE, by using an integrating factor. The ODE is first order linear, with matrix coefficients, so 

$$\begin{eqnarray}
m\frac{d\textbf{v}}{dt} &=& q\textbf{E} + qB\textbf{v}\\
\textbf{v}' - \frac{q}{m} B\textbf{v} &=& \frac{q}{m}\textbf{E}\\
\exp\left(-\frac{qBt}{m}\right) \textbf{v}' - \frac{q}{m}\exp\left(-\frac{qBt}{m}\right)B\textbf{v} &=& \frac{q}{m}\exp\left(-\frac{qBt}{m}\right)\textbf{E}\\
\frac{d}{dt}\left(\exp\left(-\frac{qBt}{m}\right)\textbf{v}\right) &=& \frac{q}{m}\exp\left(-\frac{qBt}{m}\right)\textbf{E}\\
\exp\left(-\frac{qBt}{m}\right)\textbf{v} &=& \int \frac{q}{m}\exp\left(-\frac{qBt}{m}\right)\textbf{E} dt \\
\exp\left(-\frac{qBt}{m}\right)\textbf{v} &=&  -B^{-1}\exp\left(-\frac{qBt}{m}\right)\textbf{E} + \textbf{c}\\
\textbf{v} &=&  -B^{-1}\textbf{E} + \exp\left(\frac{qBt}{m}\right)\textbf{c}\\
\end{eqnarray}$$

Then plugging in the initial condition $\textbf{v}(0) = \textbf{v}_0$, we find the value for $\textbf{c}$:

$$ \textbf{v} = \exp\left(\frac{qBt}{m}\right)\textbf{v}_0 + \left(\exp\left(\frac{qBt}{m}\right) - I\right) B^{-1}\textbf{E}$$

Now finally integrating once to get the position, 

$$\textbf{r}(t)  = \frac{mB^{-1}}{q}\exp\left(\frac{qBt}{m}\right)\textbf{b}_0 + \left(\frac{m B^{-1}}{q}\exp\left(\frac{qBt}{m}\right) - tI\right) B^{-1}\textbf{E} + \textbf{c}$$

Setting $\textbf{r}(t) = \textbf{r}_0$, we find the final result: 

$$\textbf{r}(t)  = \frac{mB^{-1}}{q}\left(\exp\left(\frac{qBt}{m}\right)-1\right)\textbf{v}_0 + \left(\frac{m B^{-1}}{q}\left(\exp\left(\frac{qBt}{m}\right) - 1\right) - tI\right) B^{-1}\textbf{E} + \textbf{r}_0$$

Now, we need to evaluate the matrix exponential. 





