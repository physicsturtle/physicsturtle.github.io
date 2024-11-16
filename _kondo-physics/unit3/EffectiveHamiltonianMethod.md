---
layout: lesson
title: Effective Hamiltonian Method 
dept: physics
course: kondo-physics
unit: unit3
deptDisplay: Physics
courseDisplay: Kondo and Heavy Fermion physics
unitDisplay: Unit 3
---
We aim to rotate out high energy degrees of freedom. Suppose we have a Hamiltonian \\(\Hhat = \Hhat\_0 + \Hhat\_1\\), where \\(\Hhat\_1\\) acts as a perturbation to \\(\Hhat\_0\\). To do this, we define a new Hamiltonian

$$\begin{equation}
\Hhat' = e^{i\Shat}\Hhat e^{-i\Shat}
\end{equation}$$

and expand using the Baker-Campbell-Hausdorff formula

$$\begin{align}
\Hhat' ={}& \Hhat + i[\Shat,\Hhat] - \frac{1}{2}[\Shat,[\Shat,\Hhat]] + \cdots \\
={}& \Hhat_0 + \Hhat_1 + i[\Shat,\Hhat_0] + i[\Shat,\Hhat_1] - \frac{1}{2}[\Shat,[\Shat,\Hhat_0]] - \frac{1}{2}[\Shat,[\Shat,\Hhat_1]] + \cdots
\end{align}$$

With \\(\Hhat\_0\\) being \\(O(1)\\) in the perturbation, we set \\(\Hhat\_1 + i[\Shat,\Hhat\_0] = 0\\), because these terms are the ones at \\(O(H\_1)\\); defining this cancellation also tells us that \\(S = O(H\_1)\\). Therefore, we have no linear term and the next term after \\(O(1)\\) is the quadratic term. We will truncate the series after the quadratic term, leaving us with an effective Hamiltonian. In other words, \\(H\_\text{eff}\\) is the truncation of the expansion of \\(H'\\) to quadratic order. We immediately notice that \\([\Shat,[\Shat,\Hhat\_1]] = O(H\_1^3)\\), so we remove it from our definition of \\(\Hhat\_\text{eff}\\). 

$$\begin{align}
\Hhat_\text{eff} ={}& \Hhat_0 + i[\Shat,\Hhat_1] - \frac{1}{2}[\Shat,[\Shat,\Hhat_0]] \\
={}& \Hhat_0 + i[\Shat,\Hhat_1] - \frac{1}{2}[\Shat, i\Hhat_1] \\
={}& \Hhat_0 + \frac{i}{2}[\Shat,\Hhat_1]
\end{align}$$

### Rotating The Anderson Model 

We can actually use this to perform the Schrieffer-Wolff transformation to derive the Kondo Hamiltonian. Note that one can simply use a clever ansatz to do this, but evaluating this integral provides a more systematic method. In our case, we want to solve the equation 

$$\begin{equation}
\Shat \Hhat_0 - \Hhat_0 \Shat = i\Hhat_1
\end{equation}$$

so, identifying \\(\Xhat = \Shat\\), \\(\Ahat = \Hhat\_0\\), and \\(\Bhat = i\Hhat\_1\\), we find that 

$$\begin{equation}
\Shat = -\lim_{\eta\to 0^+}\int_0^\infty e^{-\eta t} e^{i\Hhat_0 t} \Hhat_1 e^{-i\Hhat_0 t} \d t 
\end{equation}$$

we recognize the integrand as being able to be expanded with the Baker-Campbell-Hausdorff formula. 

$$\begin{equation}
\Shat = -\lim_{\eta\to 0^+}\int_0^\infty e^{-\eta t}\sum_{n=0}^\infty \frac{(it)^n}{n!}[\Hhat_0,[\Hhat_0,\dots, [\Hhat_0,\Hhat_1]]] \d t 
\end{equation}$$

The Anderson model is given by 

$$\begin{equation}
\Hhat = \Hhat_0 + \Hhat_1
\end{equation}$$

where we are treating \\(\Hhat\_1\\) as a perturbation. We treat it as a perturbation because we want to examine the system in a low-energy subspace, where there is no hopping onto or off of the impurity, and the impurity is bound in place. The unperturbed and perturbed Hamiltonians are given below.

$$\begin{align}
\Hhat_0 ={}& \sum_{\k} \epsilon_{\k} \chat^\dagger_{\k\sigma}\chat_{\k\sigma} + \sum_\sigma \epsilon_d \fhat^\dagger_{\sigma} \fhat_{\sigma} + U\nhat_{d\uparrow}\nhat_{d\downarrow}\\
\Hhat_1 ={}& \sum_{\k\sigma} V_{\k}(\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \fhat^\dagger_{\sigma}\chat_{\k\sigma})
\end{align}$$

it is helpful to split up \\(H\_0\\) into three parts: the free electron part \\(\Hhat\_e\\), the binding energy on the impurity part \\(\Hhat\_i\\), and the Coulomb potential part \\(\Hhat\_c\\). We will also split up \\(\Hhat\_1\\) into two parts

$$\begin{equation}
H_1 = \sum_{\k\sigma} V_{\k} \chat^\dagger_{\k\sigma}\fhat_{\sigma} + \sum_{\k\sigma} V_{\k} \fhat^\dagger_{\sigma}\chat_{\k\sigma}
\end{equation}$$

where we pick those subscrips to mean that the electron is going off of the impurity or onto the impurity. The goal is to calculate \\([H\_0,H\_1]\\), and see if a pattern arises to these nested commutators. To do this, we calculate

$$\begin{align}
[\chat^\dagger_{\k\sigma}\chat_{\k\sigma},\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}] ={}& \chat^\dagger_{\k\sigma}\chat_{\k\sigma}\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'} - \chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}\chat^\dagger_{\k\sigma}\chat_{\k\sigma} \\
={}& \left(\chat^\dagger_{\k\sigma}\chat_{\k\sigma}\chat^\dagger_{\k'\sigma'} - \chat^\dagger_{\k'\sigma'}\chat^\dagger_{\k\sigma}\chat_{\k\sigma} \right)\fhat_{\sigma'} \\
={}& \left(\chat^\dagger_{\k\sigma}(\delta_{\k\k'}\delta_{\sigma\sigma'} -\chat^\dagger_{\k'\sigma'} \chat_{\k\sigma}) - \chat^\dagger_{\k'\sigma'}\chat^\dagger_{\k\sigma}\chat_{\k\sigma} \right)\fhat_{\sigma'} \\
={}& \chat^\dagger_{\k\sigma}\fhat_{\sigma'}\delta_{\k\k'}\delta_{\sigma\sigma'}
\end{align}$$

$$\begin{align}
[\chat^\dagger_{\k\sigma}\chat_{\k\sigma},\fhat^\dagger_{\sigma'}\chat_{\k'\sigma'}] ={}& \chat^\dagger_{\k\sigma}\chat_{\k\sigma}\fhat^\dagger_{\sigma'}\chat_{\k'\sigma'} - \fhat^\dagger_{\sigma'}\chat_{\k'\sigma'}\chat^\dagger_{\k\sigma}\chat_{\k\sigma} \\
={}& \fhat^\dagger_{\sigma'}\left(\chat^\dagger_{\k\sigma}\chat_{\k\sigma}\chat_{\k'\sigma'} -\chat_{\k'\sigma'}\chat^\dagger_{\k\sigma}\chat_{\k\sigma}\right) \\
={}& \fhat^\dagger_{\sigma'}\left(\chat^\dagger_{\k\sigma}\chat_{\k\sigma}\chat_{\k'\sigma'} - (\delta_{\k\k'}\delta_{\sigma\sigma'} - \chat^\dagger_{\k\sigma}\chat_{\k'\sigma'})\chat_{\k\sigma}\right) \\
={}& -\fhat^\dagger_{\sigma'}\chat_{\k\sigma}\delta_{\k\k'}\delta_{\sigma\sigma'}
\end{align}$$

$$\begin{align}
[\fhat^\dagger_{\sigma}\fhat_{\sigma},\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}] ={}& \fhat^\dagger_{\sigma}\fhat_{\sigma}\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'} - \chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}\fhat^\dagger_{\sigma}\fhat_{\sigma} \\
={}& \chat^\dagger_{\k'\sigma'}\left(\fhat^\dagger_{\sigma}\fhat_{\sigma}\fhat_{\sigma'} - \fhat_{\sigma'}\fhat^\dagger_{\sigma}\fhat_{\sigma} \right) \\
={}& \chat^\dagger_{\k'\sigma'}\left(\fhat^\dagger_{\sigma}\fhat_{\sigma}\fhat_{\sigma'} - (\delta_{\sigma\sigma'} - \fhat^\dagger_{\sigma} \fhat_{\sigma'})\fhat_{\sigma} \right) \\
={}& -\chat^\dagger_{\k'\sigma'}\fhat_{\sigma}\delta_{\sigma\sigma'}
\end{align}$$

$$\begin{align}
[\fhat^\dagger_{\sigma}\fhat_{\sigma},\fhat^\dagger_{\sigma'}\chat_{\k'\sigma'}] ={}& \fhat^\dagger_{\sigma}\fhat_{\sigma}\fhat^\dagger_{\sigma'}\chat_{\k'\sigma'} - \fhat^\dagger_{\sigma'}\chat_{\k'\sigma'}\fhat^\dagger_{\sigma}\fhat_{\sigma}\\
={}& \left(\fhat^\dagger_{\sigma}\fhat_{\sigma}\fhat^\dagger_{\sigma'}- \fhat^\dagger_{\sigma'}\fhat^\dagger_{\sigma}\fhat_{\sigma} \right)\chat_{\k'\sigma'} \\
={}& \left(\fhat^\dagger_{\sigma}(\delta_{\sigma\sigma'} - \fhat^\dagger_{\sigma'} \fhat_{\sigma}) - \fhat^\dagger_{\sigma'}\fhat^\dagger_{\sigma}\fhat_{\sigma} \right)\chat_{\k'\sigma'} \\
={}& \fhat^\dagger_{\sigma}\chat_{\k'\sigma'}\delta_{\sigma\sigma'}
\end{align}$$

$$\begin{align}
[\nhat_{d\uparrow}\nhat_{d\downarrow},\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}] ={}& \nhat_{d\uparrow}[\nhat_{d\downarrow},\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}] + [\nhat_{d\uparrow},\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}]\nhat_{d\downarrow} \\
={}& \nhat_{d\uparrow}\left(-\chat^\dagger_{\k'\sigma'}\fhat_{\downarrow}\delta_{\downarrow\sigma'}\right) + \left(-\chat^\dagger_{\k'\sigma'}\fhat_{\uparrow}\delta_{\uparrow\sigma'}\right)\nhat_{d\downarrow}\\
={}& - \nhat_{d\uparrow}\chat^\dagger_{\k'\downarrow}\fhat_{\downarrow} \delta_{\downarrow\sigma'}- \chat^\dagger_{\k'\uparrow}\fhat_{\uparrow}\nhat_{d\downarrow} \delta_{\uparrow\sigma'}\\
={}& -\sum_{\sigma}\chat^\dagger_{\k'\sigma}\fhat_{\sigma}\nhat_{d,-\sigma}\delta_{\sigma\sigma'} \\
={}& -\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}\nhat_{d,-\sigma'}
\end{align}$$

$$\begin{align}
[\nhat_{d\uparrow}\nhat_{d\downarrow},\fhat^\dagger_{\sigma'}\chat_{\k'\sigma'}] ={}& \nhat_{d\uparrow}[\nhat_{d\downarrow},\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}] + [\nhat_{d\uparrow},\chat^\dagger_{\k'\sigma'}\fhat_{\sigma'}]\nhat_{d\downarrow} \\
={}& \nhat_{d\uparrow}\fhat^\dagger_{\downarrow}\chat_{\k'\sigma'}\delta_{\downarrow\sigma'} + \fhat^\dagger_{\uparrow}\chat_{\k'\sigma'}\delta_{\uparrow\sigma'} \nhat_{d\downarrow} \\
={}& \nhat_{d\uparrow}\fhat^\dagger_{\downarrow}\chat_{\k'\downarrow}\delta_{\downarrow\sigma'} + \fhat^\dagger_{\uparrow}\chat_{\k'\uparrow}\nhat_{d\downarrow}\delta_{\uparrow\sigma'} \\
={}& \sum_{\sigma}\fhat^\dagger_{\sigma}\chat_{\k'\sigma}\nhat_{d,-\sigma}\delta_{\sigma\sigma'} \\
={}& \fhat^\dagger_{\sigma'}\chat_{\k'\sigma'}\nhat_{d,-\sigma'}
\end{align}$$

We see that all of the commutators have worked out to a term which is proportional to something which already existed in \\(H\_1\\). We now search for the pattern, which will allow us to evaluate a general nested commutator. As an intermediate step, let's collect some of the results we previously calculated by doing

$$\begin{align}
[H_0,\chat^\dagger_{\k\sigma} \fhat_{\sigma}] ={}& \sum_{\k'\sigma'} \epsilon_{\k'} [\chat^\dagger_{\k'\sigma'}\chat_{\k'\sigma'},\chat^\dagger_{\k\sigma}\fhat_{\sigma}] + \sum_{\sigma'}\epsilon_d[\fhat^\dagger_{\sigma'}\fhat_{\sigma'},\chat^\dagger_{k\sigma}\fhat_{\sigma}] + U[\nhat_{d\uparrow}\nhat_{d\downarrow},\chat^\dagger_{\k\sigma}\fhat_{\downarrow}] \\
={}& \sum_{\k'\sigma'}\epsilon_{\k'}\chat^\dagger_{\k'\sigma'}\fhat_{\sigma}\delta_{\k\k'}\delta_{\sigma\sigma'} + \sum_{\sigma'}\epsilon_d (-\chat^\dagger_{\k\sigma}\fhat_{\sigma'}\delta_{\sigma\sigma'}) + U(-\chat^\dagger_{\k\sigma}\fhat_{\sigma}\nhat_{d,-\sigma})\\
={}& \epsilon_{\k}\chat^\dagger_{\k\sigma}\fhat_{\sigma} -\epsilon_d \chat^\dagger_{\k\sigma}\fhat_{\sigma} - U\chat^\dagger_{\k\sigma}\fhat_{\sigma}\nhat_{d,-\sigma} \\
={}& (\epsilon_{\k}-\epsilon_d - U\nhat_{d,-\sigma})\chat^\dagger_{\k\sigma}\fhat_{\sigma}
\end{align}$$

$$\begin{align}
[H_0,\fhat^\dagger_{\sigma} \chat_{\k\sigma}] ={}& \sum_{\k'\sigma'}\epsilon_{\k'} [\chat^\dagger_{\k'\sigma'}\chat_{\k'\sigma'},\fhat^\dagger_{\sigma} \chat_{\k\sigma}] + \sum_{\sigma'}\epsilon_d [\fhat^\dagger_{\sigma'}\fhat_{\sigma'},\fhat^\dagger_{\sigma} \chat_{\k\sigma}] + U[\nhat_{d\uparrow}\nhat_{d\downarrow},\fhat^\dagger_{\sigma} \chat_{\k\sigma}] \\
={}&\sum_{\k'\sigma'}(-\epsilon_{\k'})\fhat^\dagger_{\sigma}\chat_{\k'\sigma'}\delta_{\k\k'}\delta_{\sigma\sigma'} + \sum_{\sigma'}\epsilon_d \fhat^\dagger_{\sigma'}\chat_{\k\sigma}\delta_{\sigma\sigma'} + U\fhat^\dagger_{\sigma}\chat_{\k\sigma}\nhat_{d,-\sigma} \\
={}& -\epsilon_{\k}\fhat^\dagger_{\sigma}\chat_{\k\sigma} + \epsilon_d \fhat^\dagger_{\sigma}\chat_{\k\sigma} + U\fhat^\dagger_{\sigma}\chat_{\k\sigma}\nhat_{d,-\sigma} \\
={}& (-\epsilon_{\k} + \epsilon_d + U\nhat_{d,-\sigma})\fhat^\dagger_{\sigma}\chat_{\k\sigma}
\end{align}$$

which we will now plug into the full commutator between \\(H\_0\\) and \\(H\_1\\).

$$\begin{align}
[H_0,H_1] ={}& \sum_{\k\sigma}V_{\k} \left( [H_0,\chat^\dagger_{\k\sigma}\fhat_{\sigma}] + [H_0,\fhat^\dagger_{\sigma}\chat_{\k\sigma}]\right) \\
={}& \sum_{\k\sigma}\epsilon_{\k} V_{\k}\left( \chat^\dagger_{\k\sigma}\fhat_{\sigma} -\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right) \\
&+ \sum_{\k\sigma}\epsilon_d V_{\k} \left(-\chat^\dagger_{\k\sigma}\fhat_{\sigma}+ \fhat^\dagger_{\sigma}\chat_{\k\sigma}\right) \\
&+ U\sum_{\k\sigma}V_{\k} \left( -\nhat_{d,-\sigma}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \nhat_{d,-\sigma}\fhat^\dagger_{\sigma}\chat_{\k\sigma} \right) \\
={}& \sum_{\k\sigma}V_{\k}\left[\left(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}\right)\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \left(-\epsilon_{\k} + \epsilon_d + U\nhat_{d,-\sigma}\right)\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right]
\end{align}$$

which looks very similar to our original expression for \\(H\_1\\), but with different values for \\(V\_{\k}\\). Before moving on with finding the pattern, let's evaluate the commutator 

To simplify these commutators, it is useful to know

$$\begin{align}
[\nhat_{d\sigma},n_{d\sigma'}] ={}& \fhat^\dagger_{\sigma}[\fhat_{\sigma},n_{d\sigma'}] + [\fhat^\dagger_{\sigma},\nhat_{d\sigma'}]\fhat_{\sigma} \\
={}& \fhat^\dagger_{\sigma}(\fhat_{\sigma}\fhat^\dagger_{\sigma'}\fhat_{\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma'}\fhat_{\sigma}) + (\fhat^\dagger_{\sigma}\fhat^\dagger_{\sigma'}\fhat_{\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma'}\fhat^\dagger_{\sigma})\fhat_{\sigma} \\
={}& \fhat^\dagger_{\sigma}((\delta_{\sigma\sigma} - \fhat^\dagger_{\sigma'}\fhat_{\sigma})\fhat_{\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma'}\fhat_{\sigma}) + (\fhat^\dagger_{\sigma}\fhat^\dagger_{\sigma'}\fhat_{\sigma'} - \fhat^\dagger_{\sigma'}(\delta_{\sigma\sigma'}- \fhat^\dagger_{\sigma}\fhat_{\sigma'}))\fhat_{\sigma}\\
={}& \fhat^\dagger_{\sigma}\fhat_{\sigma'}\delta_{\sigma\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma'}\delta_{\sigma\sigma'}\\
={}& 0.
\end{align}$$

which therefore tells us that

$$\begin{align}
[H_0,\nhat_{d,-\sigma}] ={}& \sum_{\k\sigma'}\epsilon_{\k} [\nhat_{\k\sigma'},\nhat_{d,-\sigma}] + \sum_{\sigma'}\epsilon_d [\nhat_{d\sigma'},\nhat_{d,-\sigma}] + U[\nhat_{d\uparrow}\nhat_{d\downarrow},\nhat_{d,-\sigma}] \\
={}& 0
\end{align}$$

If we now consider taking an expression like \\([H\_0,[H\_0,H\_1]]\\), what do we get? 

$$\begin{align}
[H_0,[H_0,H_1]] ={}& \sum_{\k\sigma}V_{\k}\left([H_0,\left(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}\right)\chat^\dagger_{\k\sigma}\fhat_{\sigma}] + [H_0,\left(-\epsilon_{\k} + \epsilon_d + U\nhat_{d,-\sigma}\right)\fhat^\dagger_{\sigma}\chat_{\k\sigma}]\right)
\end{align}$$



Since we have just shown that \\([H\_0,\nhat\_{d,-\sigma}] = 0\\), we know that \\([H\_0,\epsilon\_{\k} - \epsilon\_d - U\nhat\_{d,-\sigma}] = 0\\) so we can simplify 

$$\begin{align}
[H_0,[H_0,H_1]] ={}& \sum_{\k\sigma}V_{\k}\left(\left(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}\right)[H_0,\chat^\dagger_{\k\sigma}\fhat_{\sigma}] + \left(-\epsilon_{\k} + \epsilon_d + U\nhat_{d,-\sigma}\right)[H_0,\fhat^\dagger_{\sigma}\chat_{\k\sigma}]\right) \\
={}& \sum_{\k\sigma}V_{\k}\left(\left(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}\right)^2\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \left(-\epsilon_{\k} + \epsilon_d + U\nhat_{d,-\sigma}\right)^2\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right)
\end{align}$$

From this, it is now obvious that if we have \\(n\\) nested commutators, then 

$$\begin{equation}
\underbrace{[H_0,[H_0,\dots[H_0,H_1]]]}_{n\,\text{times}} = \sum_{\k\sigma}V_{\k}\left(\left(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}\right)^n\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \left(-\epsilon_{\k} + \epsilon_d + U\nhat_{d,-\sigma}\right)^n\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right)
\end{equation}$$

Now plugging this in to our formula for \\(S\\),

$$\begin{align}
S ={}& -\lim_{\eta\to 0^+}\int_0^\infty e^{-\eta t}\sum_{n=0}^\infty \frac{(it)^n}{n!} \sum_{\k\sigma}V_{\k}\left(\left(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}\right)^n\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \left(-\epsilon_{\k} + \epsilon_d + U\nhat_{d,-\sigma}\right)^n\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right) \d t\\
={}& -\lim_{\eta\to 0^+}\int_0^\infty e^{-\eta t}\sum_{\k\sigma}V_{\k}\left[ \exp\left(it(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma})\right) \chat^\dagger_{\k\sigma}\fhat_{\sigma} + \exp\left(-it(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma})\right)\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right]\d t \\
={}& \sum_{\k\sigma}V_{\k}\lim_{\eta\to 0^+} \left((-\eta + i(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}))^{-1}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + (-\eta - i(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}))^{-1}\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right)\\
={}& \sum_{\k\sigma}V_{\k}\left(( i(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}))^{-1}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + (- i(\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}))^{-1}\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right)\\
={}&-i \sum_{\k\sigma}V_{\k} \frac{1}{\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}} \left( \chat^\dagger_{\k\sigma}\fhat_{\sigma} - \fhat^\dagger_{\sigma}\chat_{\k\sigma}\right) 
\end{align}$$

Now we need to deal with the nasty \\((\epsilon\_{\k} - \epsilon\_d - U\nhat\_{d,-\sigma})^{-1}\\). To deal with this, we expand in a Taylor series in \\(\nhat\_{d,-\sigma}\\). This gives us 

$$\begin{align}
\frac{1}{\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}} ={}& \frac{1}{\epsilon_{\k} - \epsilon_d}\frac{1}{1 - U\nhat_{d,-\sigma}/(\epsilon_{\k} - \epsilon_d)} \\
={}& \frac{1}{\epsilon_{\k} - \epsilon_d} \sum_{n=0}^\infty \left(\frac{U\nhat_{d,-\sigma}}{\epsilon_{\k} - \epsilon_d}\right)^n
\end{align}$$

Since, for \\(n \geq 1\\), we have \\(\nhat\_{d,-\sigma}^n = \nhat\_{d,-\sigma}\\), we can rewrite this as 

$$\begin{align}
\frac{1}{\epsilon_{\k} - \epsilon_d - U\nhat_{d,-\sigma}}={}& \frac{1}{\epsilon_{\k} - \epsilon_d} \left(1 + \sum_{n=1}^\infty \left(\frac{U\nhat_{d,-\sigma}}{\epsilon_{\k} - \epsilon_d}\right)^n\right) \\
={}& \frac{1}{\epsilon_{\k} - \epsilon_d} +  \frac{1}{\epsilon_{\k} - \epsilon_d} \sum_{n=1}^\infty \left(\frac{U}{\epsilon_{\k} - \epsilon_d}\right)^n \nhat_{d,-\sigma} \\
={}& \frac{1}{\epsilon_{\k} - \epsilon_d} +  \frac{1}{\epsilon_{\k} - \epsilon_d} \left(\frac{1}{1 - U/(\epsilon_{\k} - \epsilon_d)} - 1\right) \nhat_{d,-\sigma} \\ 
={}& \frac{1}{\epsilon_{\k} - \epsilon_d} +   \left(\frac{1}{\epsilon_{\k} - \epsilon_d - U} - \frac{1}{\epsilon_{\k} - \epsilon_d}\right) \nhat_{d,-\sigma}
\end{align}$$

Thus, we plug this result in to get 

$$\begin{align}
S ={}& -i\sum_{\k\sigma}V_{\k}\left[\frac{1}{\epsilon_{\k} - \epsilon_d} +   \left(\frac{1}{\epsilon_{\k} - \epsilon_d - U} - \frac{1}{\epsilon_{\k} - \epsilon_d}\right) \nhat_{d,-\sigma}\right]\left(\chat^\dagger_{\k\sigma}\fhat_{\sigma} - \fhat^\dagger_{\sigma}\chat_{\k\sigma}\right).
\end{align}$$

For later ease of notation, we define

$$\begin{equation}
A_{\k} = \frac{V_{\k}}{\epsilon_{\k} - \epsilon_d} ,\qquad V_{\k} = V_{\k}\left(\frac{1}{\epsilon_{\k} - \epsilon_d - U} - \frac{1}{\epsilon_{\k} - \epsilon_d}\right).
\end{equation}$$

### From Anderson to Kondo


The next step is to plug our expression for \\(S\\) into the expansion of the effective Hamiltonian. 

$$\begin{equation}
H_\text{eff} = H_0 + \frac{i}{2}[S, H_1]
\end{equation}$$

The intermediate steps in evaluating \\([S,H\_1]\\) consist of evaluating the commutators 

$$\begin{align}
[\chat^\dagger_{\k\sigma}\fhat_{\sigma}, \fhat^\dagger_{\sigma'} \chat_{\k'\sigma'}] ={}& \chat^\dagger_{\k\sigma}\fhat_{\sigma} \fhat^\dagger_{\sigma'} \chat_{\k'\sigma'} - \fhat^\dagger_{\sigma'} \chat_{\k'\sigma'} \chat^\dagger_{\k\sigma}\fhat_{\sigma} \\
={}& \chat^\dagger_{\k\sigma}(\delta_{\sigma\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma}) \chat_{\k'\sigma'} - \fhat^\dagger_{\sigma'}(\delta_{\k\k'}\delta_{\sigma\sigma'} - \chat^\dagger_{\k\sigma}\chat_{\k'\sigma'}) \fhat_{\sigma} \\
={}& \chat^\dagger_{\k\sigma}\chat_{\k'\sigma'}\delta_{\sigma\sigma'} - \chat^\dagger_{\k\sigma}\fhat^\dagger_{\sigma'} \fhat_{\sigma} \chat_{\k'\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma} \delta_{\k\k'} \delta_{\sigma\sigma'} + \fhat^\dagger_{\sigma'} \chat^\dagger_{\k\sigma} \chat_{\k'\sigma'} \fhat_{\sigma} \\ 
={}& \chat^\dagger_{\k\sigma}\chat_{\k'\sigma'}\delta_{\sigma\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma} \delta_{\k\k'} \delta_{\sigma\sigma'} 
\end{align}$$

This means that we can now calculate commutators with \\(H\_1\\). 

$$\begin{align}
[\chat^\dagger_{\k\sigma} \fhat_{\sigma}, H_1] ={}& \sum_{\k'\sigma'} V_{\k'} \left([\chat^\dagger_{\k\sigma} \fhat_{\sigma}, \chat^\dagger_{\k'\sigma'} \fhat_{\sigma'}] + [\chat^\dagger_{\k\sigma} \fhat_{\sigma}, \fhat^\dagger_{\sigma'} \chat_{\k'\sigma'} ] \right) \\
={}& \sum_{\k'\sigma'} V_{\k'} \left( \chat^\dagger_{\k\sigma}\chat_{\k'\sigma'}\delta_{\sigma\sigma'} - \fhat^\dagger_{\sigma'}\fhat_{\sigma} \delta_{\k\k'} \delta_{\sigma\sigma'}  \right) \\
={}& \sum_{\k'} V_{\k'} \left( \chat^\dagger_{\k\sigma}\chat_{\k'\sigma} - \fhat^\dagger_{\sigma}\fhat_{\sigma} \delta_{\k\k'}  \right) 
\end{align}$$

where the first commutator is zero because the \\(\k\\) operators are both creation, and the \\(d\\) operators are both annihilation. We therefore get perfect anticommutation between them, but because we have an even number of operators we get commuting behaviour. 

Then, we can easily calculate the commutator with the complex conjugate,

$$\begin{align}
[\fhat^\dagger_{\sigma} \chat_{\k\sigma}, H_1] ={}& -[\chat^\dagger_{\k\sigma} \fhat_{\sigma}, H_1]^\dagger \\
={}& -\sum_{\k'} V_{\k'} \left( \chat^\dagger_{\k'\sigma}\chat_{\k\sigma} - \fhat^\dagger_{\sigma}\fhat_{\sigma} \delta_{\k\k'}  \right) \\
\end{align}$$

One more commutator that we need is 

$$\begin{align}
[\nhat_{d,-\sigma}, H_1] ={}& \sum_{\k'\sigma'} V_{\k'} \left( [\nhat_{d,-\sigma}, \chat^\dagger_{\k'\sigma'} \fhat_{\sigma'}] + [\nhat_{d,-\sigma}, \fhat^\dagger_{\sigma'} \chat_{\k'\sigma'}] \right) \\
={}& \sum_{\k'\sigma'} V_{\k'} \left( -\delta_{\sigma',-\sigma}\chat^\dagger_{\k'\sigma'}\fhat_{,-\sigma} + \delta_{\sigma',-\sigma}\fhat^\dagger_{,-\sigma} \chat_{\k'\sigma'} \right) \\
={}& \sum_{\k'} V_{\k'} \left( - \chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma} + \fhat^\dagger_{,-\sigma} \chat_{\k',-\sigma} \right)
\end{align}$$



Now we are ready to calculate \\(\frac{i}{2}[S,H\_1]\\). 

$$\begin{align}
\frac{i}{2}[S,H_1] ={}& \frac{1}{2}\left[\sum_{\k\sigma}(A_{\k} + B_{\k}\nhat_{d,-\sigma})(\chat^\dagger_{\k\sigma}\fhat_{\sigma} - \fhat^\dagger_{\sigma} \chat_{\k\sigma}), H_1\right] \\
={}& \frac{1}{2}\sum_{\k\sigma}\left( (A_{\k} + B_{\k} \nhat_{d,-\sigma})\left[\chat^\dagger_{\k\sigma} \fhat_{\sigma} - \fhat^\dagger_{\sigma} \chat_{\k\sigma}, H_1\right] + \left[A_{\k} + B_{\k} \nhat_{d,-\sigma}, H_1\right](\chat^\dagger_{\k\sigma}\fhat_{\sigma} - \fhat^\dagger_{\sigma}\chat_{\k\sigma}) \right) 
\end{align}$$

Now we use all the commutator relations that we just calculated to simplify this down. We get 

$$\begin{align}
\frac{i}{2}[S,H_1] ={}& \frac{1}{2}\sum_{\k\sigma}(A_{\k} + B_{\k} \nhat_{d,-\sigma})\sum_{\k'} V_{\k'd}\left(\chat^\dagger_{\k\sigma}\chat_{\k'\sigma} - \fhat^\dagger_{\sigma}\fhat_{\sigma}\delta_{\k\k'} + \chat^\dagger_{\k'\sigma}\chat_{\k\sigma} - \fhat^\dagger_{\sigma} \fhat_{\sigma}\delta_{\k\k'} \right) \\
&+ \frac{1}{2}\sum_{\k\sigma} B_{\k} \sum_{\k'}V_{\k' d}\left(-\chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma} + \fhat^\dagger_{,-\sigma}\chat_{\k',-\sigma}\right)\left(\chat^\dagger_{\k\sigma}\fhat_{\sigma} - \fhat^\dagger_{\sigma}\chat_{\k\sigma}\right) \\
={}& \frac{1}{2}\sum_{\k\sigma\k'}V_{\k'd}(A_{\k} + B_{\k} \nhat_{d,-\sigma})\left(\chat^\dagger_{\k\sigma}\chat_{\k'\sigma} + \chat^\dagger_{\k'\sigma}\chat_{\k\sigma}- 2\fhat^\dagger_{\sigma}\fhat_{\sigma}\delta_{\k\k'}\right) \\
&+ \frac{1}{2}\sum_{\k\sigma\k'} B_{\k} V_{\k' d}\left(-\chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \fhat^\dagger_{,-\sigma}\chat_{\k',-\sigma}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\fhat^\dagger_{\sigma}\chat_{\k\sigma} - \fhat^\dagger_{,-\sigma}\chat_{\k',-\sigma} \fhat^\dagger_{\sigma}\chat_{\k\sigma} \right)
\end{align}$$

Now we expand out the brackets in the first sum, then collect some of the \\(B\_{\k}\\) terms together. 

$$\begin{align}
\frac{i}{2}[S,H_1] ={}& -\sum_{\k\sigma}V_{\k d}(A_{\k} + B_{\k} \nhat_{d,-\sigma}) \fhat^\dagger_{\sigma}\fhat_{\sigma} +  \frac{1}{2} \sum_{\k\sigma\k'}V_{\k'd}(A_{\k} + B_{\k} \nhat_{d,-\sigma}) \left(\chat^\dagger_{\k\sigma}\chat_{\k'\sigma}  + \chat^\dagger_{\k'\sigma} \chat_{\k\sigma}\right) \\
&+ \frac{1}{2}\sum_{\k\sigma\k'} B_{\k} V_{\k' d}\left(\fhat^\dagger_{,-\sigma}\chat_{\k',-\sigma}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right) \\
&-\frac{1}{2}\sum_{\k\sigma\k'} B_{\k} V_{\k' d}\left(\chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \fhat^\dagger_{,-\sigma}\chat_{\k',-\sigma} \fhat^\dagger_{\sigma}\chat_{\k\sigma} \right) \\
={}& -\sum_{\k\sigma}V_{\k d}(A_{\k} + B_{\k} \nhat_{d,-\sigma}) \nhat_{d\sigma} +  \frac{1}{2} \sum_{\k\sigma\k'}V_{\k'd}A_{\k} \left(\chat^\dagger_{\k\sigma}\chat_{\k'\sigma}  + \chat^\dagger_{\k'\sigma} \chat_{\k\sigma}\right) \\
&+\frac{1}{2}\sum_{\k\sigma\k'} V_{\k' d} B_{\k} \left[ \nhat_{d,-\sigma}  \left(\chat^\dagger_{\k\sigma}\chat_{\k'\sigma}  + \chat^\dagger_{\k'\sigma} \chat_{\k\sigma}\right) +\fhat^\dagger_{,-\sigma}\chat_{\k',-\sigma}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\fhat^\dagger_{\sigma}\chat_{\k\sigma}\right]  \\
&-\frac{1}{2}\sum_{\k\sigma\k'} B_{\k} V_{\k' d}\left(\chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\chat^\dagger_{\k\sigma}\fhat_{\sigma} + \fhat^\dagger_{,-\sigma}\chat_{\k',-\sigma} \fhat^\dagger_{\sigma}\chat_{\k\sigma} \right)
\end{align}$$

We can drastically simplify some of these terms by splitting up expressions and then swapping \\(\k\\) and \\(\k'\\). Doing this, and also swapping the order of some operators to clean up the expressions, we find 

$$\begin{align}
\frac{i}{2}[S,H_1] ={}& -\sum_{\k\sigma}V_{\k d}(A_{\k} + B_{\k} \nhat_{d,-\sigma}) \nhat_{d\sigma} +  \frac{1}{2} \sum_{\k\sigma\k'}(V_{\k'd}A_{\k}+V_{\k d}A_{\k'}) \chat^\dagger_{\k\sigma}\chat_{\k'\sigma}\\
&+\frac{1}{2}\sum_{\k\sigma\k'} (V_{\k' d} B_{\k}+ V_{\k d} B_{\k'}) \left[ \nhat_{d,-\sigma}  \chat^\dagger_{\k\sigma}\chat_{\k'\sigma} -\chat^\dagger_{\k\sigma}\chat_{\k',-\sigma}\fhat^\dagger_{,-\sigma}\fhat_{\sigma} \right]  \\
&-\frac{1}{2}\sum_{\k\sigma\k'} B_{\k} V_{\k' d}\left(\chat^\dagger_{\k\sigma}\chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\fhat_{\sigma} + \chat_{\k\sigma}\chat_{\k',-\sigma} \fhat^\dagger_{,-\sigma}\fhat^\dagger_{\sigma} \right)
\end{align}$$

Now, let's isolate some of these terms. Let's define 

$$\begin{align}
\Hhat_0' ={}& -\sum_{\k\sigma}V_{\k d}(A_{\k} + B_{\k} \nhat_{d,-\sigma})\nhat_{d\sigma} \\
={}& -\frac{1}{2} \sum_{\k\sigma}2V_{\k d}(A_{\k} + B_{\k} \nhat_{d,-\sigma})\nhat_{d\sigma} \\
\end{align}$$

$$\begin{align}
\Hhat_0" ={}& \frac{1}{2} \sum_{\k\sigma\k'}(V_{\k'd}A_{\k}+V_{\k d}A_{\k'}) \chat^\dagger_{\k\sigma}\chat_{\k'\sigma} \\
={}& \sum_{\k\k'\sigma} W_{\k\k'}\chat^\dagger_{\k\sigma}\chat_{\k'\sigma}
\end{align}$$

where

$$\begin{equation}
W_{\k\k'} = \frac{1}{2}(V_{\k d} A_{\k'} + V_{\k' d} A_{\k}).
\end{equation}$$

We also define 

$$\begin{equation}
\Hhat_\text{ch} = -\frac{1}{2}\sum_{\k\sigma\k'} B_{\k} V_{\k' d}\left(\chat^\dagger_{\k\sigma}\chat^\dagger_{\k',-\sigma}\fhat_{,-\sigma}\fhat_{\sigma} + \chat_{\k\sigma}\chat_{\k',-\sigma} \fhat^\dagger_{,-\sigma}\fhat^\dagger_{\sigma} \right)
\end{equation}$$

which corresponds to changing the occupancy of the impurity by 2. The last part of \\(\frac{i}{2}[\hat{S},\Hhat\_1]\\) actually contains some spin operators hidden in it. To make this clear, let's show how the spin operators are written in terms of creation/annihilation operators. We define the notation

$$\begin{equation}
\Shat^x_{\k\k'} = \chat^\dagger_{\k\uparrow}\chat_{\k'\downarrow} + \chat^\dagger_{\k\downarrow}\chat_{\k'\uparrow},\qquad \Shat^y_{\k\k'} = -i\chat^\dagger_{\k\uparrow} \chat_{\k'\downarrow} + i\chat^\dagger_{\k\downarrow} \chat_{\k'\uparrow} ,\qquad \Shat^z_{\k\k'} = \chat^\dagger_{\k\uparrow}\chat_{\k'\uparrow} - \chat^\dagger_{\k\downarrow}\chat_{\k'\downarrow}
\end{equation}$$

$$\begin{equation}
2\Shat^x_{d} = \fhat^\dagger_{\uparrow}\fhat_{\downarrow} + \fhat^\dagger_{\downarrow}\fhat_{\uparrow},\qquad 2\Shat^y_{d} = -i\fhat^\dagger_{\uparrow} \fhat_{\downarrow} + i\fhat^\dagger_{\downarrow} \fhat_{\uparrow} ,\qquad 2\Shat^z_{d} = \fhat^\dagger_{\uparrow}\fhat_{\uparrow} - \fhat^\dagger_{\downarrow}\fhat_{\downarrow}
\end{equation}$$

The factor of two in defining the impurity spin is just an arbitrary convention. Note that these definitions also induce the \\(\Shat^+\\) and \\(\Shat^-\\) operators:

$$\begin{equation}
\Shat^+_{\k\k'} = \Shat^x_{\k\k'} + i\Shat^y_{\k\k'} = 2\chat^\dagger_{\k\uparrow} \chat_{\k'\downarrow} ,\qquad \Shat^-_{\k\k'} = \Shat^x_{\k\k'} - i\Shat^y_{\k\k'} = 2\chat^\dagger_{\k\downarrow}\chat_{\k'\uparrow}
\end{equation}$$

$$\begin{equation}
\Shat^+_d = \Shat^x_d + i\Shat^y_d = \fhat^\dagger_{\uparrow} \fhat_{\downarrow}, \qquad \Shat^-_d = \Shat^x_d - i\Shat^y_d = \fhat^\dagger_{\downarrow} \fhat_{\uparrow}
\end{equation}$$

Let's take products of these conduction electron spin operators and impurity spin operators so that we get terms quartic in fermionic operators, and then try to match said terms with terms in the expression for \\(\frac{i}{2}[\hat{S},\Hhat\_1]\\). First, let's consider 

$$\begin{align}
2\Shat^z_{\k\k'}\Shat^z_d ={}& \chat^\dagger_{\k\uparrow} \chat_{\k'\uparrow}\fhat^\dagger_{\uparrow} \fhat_{\uparrow} + \chat^\dagger_{\k\downarrow}\chat_{\k'\downarrow} \fhat^\dagger_{\uparrow}\fhat_{\uparrow} - \chat^\dagger_{\k\uparrow}\chat_{\k'\uparrow} \fhat^\dagger_{\downarrow} \fhat_{\downarrow} - \chat^\dagger_{\k\downarrow} \chat_{\k\downarrow} \fhat^\dagger_{\uparrow} \fhat_{\uparrow} \\
={}& \sum_\sigma\left(\chat^\dagger_{\k\sigma}\chat_{\k'\sigma}\fhat^\dagger_{\sigma}\fhat_{\sigma} - \chat^\dagger_{\k\sigma}\chat_{\k'\sigma}\fhat^\dagger_{,-\sigma}\fhat_{,-\sigma}\right)
\end{align}$$

and also 

$$\begin{align}
\Shat^+_{\k\k'} \Shat^-_d + \Shat^-_{\k\k'}\Shat^+_d ={}& 2\chat^\dagger_{\k\uparrow}\chat_{\k'\downarrow}\fhat^\dagger_{\downarrow}\fhat_{\uparrow} + 2\chat^\dagger_{\k\downarrow}\chat_{\k'\uparrow}\fhat^\dagger_{\uparrow}\fhat_{\downarrow} \\
(\Shat^x_{\k\k'}+i\Shat^y_{\k\k'})(\Shat^x_d - i\Shat^y_d) + (\Shat^x_{\k\k'} - i\Shat^y_{\k\k'})(\Shat^x_d + i\Shat^y_d) ={}& 2\sum_\sigma \chat^\dagger_{\k\sigma}\chat_{\k',-\sigma} \fhat^\dagger_{,-\sigma}\fhat_{\sigma} \\
2\Shat^x_{\k\k'}\Shat^x_d + 2\Shat^y_{\k\k'} \Shat^y_d ={}& 2\sum_\sigma \chat^\dagger_{\k\sigma}\chat_{\k',-\sigma} \fhat^\dagger_{,-\sigma}\fhat_{\sigma}
\end{align}$$

We substitute these expressions in to the second line of our expression for \\(\frac{i}{2}[\hat{S},\Hhat\_1]\\). This gives us 

$$\begin{align}
={}& \frac{1}{2}\sum_{\k\sigma\k'} (V_{\k' d} B_{\k}+ V_{\k d} B_{\k'}) \left[ \nhat_{d,-\sigma}  \chat^\dagger_{\k\sigma}\chat_{\k'\sigma} -\chat^\dagger_{\k\sigma}\chat_{\k',-\sigma}\fhat^\dagger_{,-\sigma}\fhat_{\sigma} \right] \\
={}& \frac{1}{2}\sum_{\k\k'} (V_{\k' d} B_{\k}+ V_{\k d} B_{\k'})\left[ \sum_\sigma \chat^\dagger_{\k\sigma}\chat_{\k'\sigma}\fhat^\dagger_{\sigma} \fhat_{\sigma} - 2\Shat^z_{\k\k'} \Shat^z_d - \Shat^x_{\k\k'}\Shat^x_d - \Shat^y_{\k\k'} \Shat^y_d \right] \\
={}& \frac{1}{2}\sum_{\k\k'} (V_{\k' d} B_{\k}+ V_{\k d} B_{\k'})\left[ \sum_\sigma \chat^\dagger_{\k\sigma}\chat_{\k'\sigma}\fhat^\dagger_{\sigma} \fhat_{\sigma} - \Shat^z_{\k\k'} \Shat^z_d - \hat{\mathbf{S}}_{\k\k'}\cdot\hat{\mathbf{S}}_d \right] \\
={}& \frac{1}{2}\sum_{\k\k'} (V_{\k' d} B_{\k}+ V_{\k d} B_{\k'})\left[\sum_\sigma \left( \chat^\dagger_{\k\sigma}\chat_{\k'\sigma}\fhat^\dagger_{\sigma} \fhat_{\sigma} - \frac{1}{2}\chat^\dagger_{\k\sigma}\chat_{\k'\sigma} \fhat^\dagger_{\sigma}\fhat_{\sigma} + \frac{1}{2}\chat^\dagger_{\k\sigma} \chat_{\k'\sigma} \fhat^\dagger_{,-\sigma} \fhat_{,-\sigma}\right) - \hat{\mathbf{S}}_{\k\k'}\cdot\hat{\mathbf{S}}_d \right] \\
={}& \frac{1}{2}\sum_{\k\k'} (V_{\k' d} B_{\k}+ V_{\k d} B_{\k'})\left[ \sum_\sigma\left(\frac{1}{2}\chat^\dagger_{\k\sigma}\chat_{\k'\sigma}(\fhat^\dagger_{\sigma} \fhat_{\sigma} + \fhat^\dagger_{,-\sigma} \fhat_{,-\sigma}) \right) - \hat{\mathbf{S}}_{\k\k'}\cdot\hat{\mathbf{S}}_d \right] \\
={}& \frac{1}{4}\sum_{\k\sigma\k'} J_{\k\k'} \chat^\dagger_{\k\sigma}\chat_{\k'\sigma}(\fhat^\dagger_{\sigma} \fhat_{\sigma} + \fhat^\dagger_{,-\sigma} \fhat_{,-\sigma}) - \frac{1}{2}\sum_{\k\sigma\k'} J_{\k\k'} \hat{\mathbf{S}}_{\k\k'}\cdot\hat{\mathbf{S}}_d
\end{align}$$

where we have defined 

$$\begin{equation}
J_{\k\k'} = V_{\k' d} B_{\k} + V_{\k d} B_{\k'}
\end{equation}$$

$$\begin{equation}
\Hhat_\text{dir} = \frac{1}{4}\sum_{\k\sigma\k'} J_{\k\k'} \chat^\dagger_{\k\sigma}\chat_{\k'\sigma}(\fhat^\dagger_{\sigma} \fhat_{\sigma} + \fhat^\dagger_{,-\sigma} \fhat_{,-\sigma})
\end{equation}$$

and 

$$\begin{equation}
\Hhat_\text{exch} = -\frac{1}{2}\sum_{\k\k'\sigma} J_{\k\k'} \hat{\mathbf{S}}_{\k\k'}\cdot\hat{\mathbf{S}}_d.
\end{equation}$$

Thus, the total Hamiltonian is given by 

$$\begin{equation}
\hat{\tilde{H}} = \Hhat_0 + \Hhat_0' + \Hhat_0" + \Hhat_\text{ch} + \Hhat_\text{dir} + \Hhat_\text{exch}.
\end{equation}$$

Let's drop \\(\Hhat\_\text{ch}\\) since it changes the occupancy of the impurity by 2. The other terms \\(\Hhat\_0'\\), \\(\Hhat\_0"\\), and \\(\Hhat\_\text{dir}\\) are all one-electron terms. We will always have one electron on the impurity, so these merely contribute constants in the one-particle sector. We therefore keep only \\(\Hhat\_\text{exch}\\). Thus, 

$$\begin{equation}
\hat{\tilde{H}} = \Hhat_0 + \Hhat_\text{exch}.
\end{equation}$$

Let's now discuss the exchange term, which constitutes the Kondo interaction. The interaction term is 

$$\begin{equation}
\Hhat_\text{exch} = -\frac{1}{2}\sum_{\k\k'\sigma} J_{\k\k'} \hat{\mathbf{S}}_{\k\k'}\cdot\hat{\mathbf{S}}_d.
\end{equation}$$

and the coupling constant is given by

$$\begin{align}
J_{\k\k'} ={}& V_{\k' d}  V_{\k d}\left(\frac{1}{\epsilon_{\k} - \epsilon_d - U} - \frac{1}{\epsilon_{\k} - \epsilon_d}\right) + V_{\k d}  V_{\k' d}\left(\frac{1}{\epsilon_{\k'} - \epsilon_d - U} - \frac{1}{\epsilon_{\k'} - \epsilon_d}\right) \\
={}& V_{\k d} V_{\k' d}\left(\frac{1}{\epsilon_{\k} - \epsilon_d - U} - \frac{1}{\epsilon_{\k} - \epsilon_d} + \frac{1}{\epsilon_{\k'} - \epsilon_d - U} - \frac{1}{\epsilon_{\k'} - \epsilon_d}\right).
\end{align}$$

What can we say about the sign of \\(J\_{\k\k'}\\)? Well, if we have an incoming conduction electron near the Fermi surface, and the electron is also outgoing near the Fermi surface, let's set \\(\|\k\| \approx \|\k'\| \approx k\_F\\). 

$$\begin{align}
J_{k_Fk_F} \approx & |V_{k_F d}|^2 \left(\frac{1}{\epsilon_{k_F} - \epsilon_d - U} - \frac{1}{\epsilon_{k_F} - \epsilon_d} + \frac{1}{\epsilon_{k_F} - \epsilon_d - U} - \frac{1}{\epsilon_{k_F} - \epsilon_d}\right) \\
={}& 2|V_{k_F d}|^2 \left(\frac{1}{\epsilon_{k_F} - \epsilon_d - U} - \frac{1}{\epsilon_{k_F} - \epsilon_d}\right) \\
={}& 2|V_{k_F d}|^2 \frac{\epsilon_{k_F} - \epsilon_d - \epsilon_{k_F} + \epsilon_d + U}{(\epsilon_{k_F} - \epsilon_d - U)(\epsilon_{k_F} - \epsilon_d)} \\
={}& \frac{2|V_{k_F d}|^2 U}{(\epsilon_{k_F} - \epsilon_d - U)(\epsilon_{k_F} - \epsilon_d)}
\end{align}$$

Since we have set the dispersion relation to be zero at the Fermi surface (because of the chemical potential), this simplifies. Additionally, \\(\epsilon\_d\\) is the binding energy of the electron on the impurity, so it is negative. Replacing \\(\epsilon\_d = -\|\epsilon\_d\|\\), we find 

$$\begin{align}
J_{k_Fk_F} ={}& \frac{2|V_{k_F d}|^2 U}{(\epsilon_d + U)\epsilon_d} \\
={}& \frac{2|V_{k_F d}|^2 U}{(|\epsilon_d| - U)|\epsilon_d|} 
\end{align}$$

Since we are dealing with the particle-hole symmetric case (this is equivalent to taking a constant density of states above and below the Fermi energy), we can set \\(\|\epsilon\_d\| = U/2\\), which tells us that \\(J\_{k\_Fk\_F} < 0\\), so the interaction is antiferromagnetic.

