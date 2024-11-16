---
layout: exercises
title: Pairing and Superconductivity  - Exercises
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
<ol>
<li> <div class="exercise">  Verify the Hubbard-Stratonovich calculation. 

<div class="answerBox"> 
 <button onclick="myFunction('answer3')" class="answerButton">Show Answer</button> 
 <div  id='answer3' class="answer" >
$$\begin{align}
\int \exp\left(-\frac{1}{U}\Delta^{*}\Delta - \Delta \bar{c}_{i\uparrow}\bar{c}_{i\downarrow} - \Delta^{*} c_{i\downarrow} c_{i\uparrow}\right)\d\Delta^{*}\d\Delta ={}& \int\exp\left(-\frac{1}{U}\left[\Delta^{*}\Delta + \Delta\bar{c}_{i\uparrow} \bar{c}_{i\downarrow}\right]\right) \\
={}& e^{U\bar{c}_{i\uparrow}\bar{c}_{i\downarrow}c_{i\downarrow}c_{i\uparrow}}
\end{align}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  

<ol type="a">
<li> Evaluate the Matsubara sum in the pair bubble
</li>
<li> Now set \(\k = 0\) and also \(k_0 = 0\) and and write the momentum sum as an integral over energy. Assume that the energies of the conduction electrons relative to the chemical potential range between \(-D\) and \(+D\). Furthermore, assume a constant density of states, and that the dispersion relation has inversion symmetry.
</li></ol>

$$\begin{equation}
\pi(\k,ik_0) = \frac{1}{\beta N_s}\sum_p \mathcal{G}_0(k-p)\mathcal{G}_0(p)
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer21')" class="answerButton">Show Answer</button> 
 <div  id='answer21' class="answer" >
<ol type="a">
<li> 
First, we evaluate the Matsubara sum. 

$$\begin{align}
\frac{1}{\beta}\sum_{ip_0}\mathcal{G}_0(k-p)\mathcal{G}_0(p) ={}& \frac{1}{\beta}\sum_{ip_0}\frac{1}{ik_0 - ip_0 - \xi_{\k-\p}}\frac{1}{ip_0 - \xi_{\p}} \\
={}& -\frac{n_F(-\xi_{\k-\p})}{ik_0 - \xi_{\k-\p} - \xi_{\p}} + \frac{n_F(\xi_{\p})}{ik_0 - \xi_{\p} - \xi_{\k-\p}} \\
={}& \frac{n_F(\xi_{\p}) - n_F(-\xi_{\k-\p})}{ik_0 - \xi_{\k-\p} - \xi_{\p}} \\
={}& \frac{n_F(-\xi_{\k-\p}) - n_F(\xi_{\p})}{\xi_{\k-\p} + \xi_{\p} - ik_0} \\
={}& \frac{1 - n_F(\xi_{\k-\p}) - n_F(\xi_{\p})}{\xi_{\k-\p} + \xi_{\p} - ik_0} 
\end{align}$$

</li>
<li> The pair bubble can now be written as 

$$\begin{equation}
\pi(\k,ik_0) = \frac{1}{N_s}\sum_{\p} \frac{1 - n_F(\xi_{\k-\p}) - n_F(\xi_{\p})}{\xi_{\k-\p} + \xi_{\p} - ik_0}.
\end{equation}$$

Now, we set \(\k = 0\). This is equivalent to looking for a uniform solution for the order parameter \(\Delta\). 

$$\begin{equation}
\pi(0,0) = \frac{1}{N_s}\sum_{\p} \frac{1 - n_F(\xi_{-\p}) - n_F(\xi_{\p})}{\xi_{\k-\p} + \xi_{\p} - ik_0}.
\end{equation}$$

Since the dispersion relation is even in \(\p\), \(\xi_{-\p} = \xi_{\p}\). Thus, 

$$\begin{align}
\pi(0,0) ={}& \frac{1}{N_s}\sum_{\p} \frac{1 - 2n_F(\xi_{\p})}{2\xi_{\p}} \\
={}& \frac{1}{N_s}\sum_{\p} \frac{1}{2\xi_{\p}}\left(1 - \frac{2}{1+e^{\beta\xi_{\p}}}\right)\\
={}& \frac{1}{N_s}\sum_{\p} \frac{1}{2\xi_{\p}}\left(\frac{1+e^{\beta\xi_{\p}} - 2}{1+e^{\beta\xi_{\p}}}\right) \\
={}& \frac{1}{N_s}\sum_{\p} \frac{1}{2\xi_{\p}}\left(\frac{e^{\beta\xi_{\p}} - 1}{1+e^{\beta\xi_{\p}}}\right) \\
={}& \frac{1}{N_s}\sum_{\p} \frac{1}{2\xi_{\p}}\left(\frac{e^{\beta\xi_{\p}/2} - e^{-\beta\xi_{\p}/2}}{e^{\beta\xi_{\p}/2}e^{-\beta\xi_{\p}/2}}\right) \\
={}& \frac{1}{N_s}\sum_{\p} \frac{1}{2\xi_{\p}}\tanh\left(\frac{\beta\xi_{\p}}{2}\right)
\end{align}$$

Now, we evaluate the sum over \(\p\) by changing it to an integral over energy \(\xi\):

$$\begin{equation}
\pi(0,0) = \frac{V}{N_s}\int_{-D}^D \frac{\tanh(\beta\xi/2)}{2\xi}\rho(\xi)\d\xi.
\end{equation}$$

We assume that \(\rho\) is roughly constant, and pull out \(\rho\) from the integral:

$$\begin{align}
\pi(0,0) ={}& \frac{V\rho }{N_s}\int_{-D}^D \frac{\tanh(\beta\xi/2)}{2\xi}\d\xi \\
={}& \frac{V\rho }{N_s}\int_0^D \frac{\tanh(\beta\xi/2)}{\xi}\d\xi
\end{align}$$

We now change to the dimensionless variable \(x = \beta\xi/2\). Then 

$$\begin{align}
\pi(0,0) ={}& \frac{V\rho }{N_s}\int_0^{\beta D/2} \frac{\tanh x}{x}\d x \\
={}& \frac{V\rho}{N_s}\left[ \tanh x \log x\bigg|_0^{\beta D/2} - \int_0^\infty \frac{\log x}{\cosh^2 x}\d x\right] \\
={}& \tilde{\rho} \left[\log\left(\frac{\beta D}{2}\right) - \log\frac{\pi}{4} + \gamma \right] \\
={}& \tilde{\rho} \log\left(\frac{2 \beta D e^{\gamma}}{\pi} \right) 
\end{align}$$

where we have used the fact that \(\beta D \gg 1\) and also that

$$\begin{equation}
\int_0^\infty \frac{\log x}{\cosh^2 x}\d x = \log\frac{\pi}{4} - \gamma
\end{equation}$$

where \(\gamma\) is the Euler-Mascheroni constant. We also defined \(\tilde{\rho} = V\rho/ N_s\) to be the density of states per site. 

</li></ol>
</div> 
 </div>

</div> </li></ol>

