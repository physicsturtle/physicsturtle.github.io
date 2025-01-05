---
layout: lesson
title: Screening in the electron gas (physical discussion) 
dept: physics
course: many-body-I
unit: unit29
deptDisplay: Physics
courseDisplay: Many Body Physics I
unitDisplay: Unit 29
---
If one places an impurity charge \\(Q\\) in an interacting electron gas, how do the electrons rearrange themselves to account for its presence? Well, one would na\"ively expect that the electrons would feel a force due to the Coulomb potential energy

$$\begin{equation}
V(\x) = \frac{Q}{4\pi\epsilon_0 |\x|}
\end{equation}$$

Even when we take into account the Thomas-Fermi screening, as was done in the lecture, the potential is modified to 

$$\begin{equation}
V(\x) = \frac{Qe^{-k_{\text{TF}}|\x|}}{4\pi\epsilon_0 |\x|}
\end{equation}$$

We see that it is much weaker, but it is still repulsive. Let us consider the following cartoon (see the following \href{https://gravityandlevity.wordpress.com/2009/06/02/friedel-oscillations-wherein-we-learn-that-the-electron-has-a-size}{blog post}, where I learned this explanation from). Consider the interacting electron gas. Pictorially, we draw the electron gas as a bunch of negative charges moving in a uniformly charged positive background. 

<figure class="center">
<p><img src="figures/interacting_electron_gas.pdf" alt="Function" class="center" style="width:142.131px;height:142.131px;"> </p><figcaption class="center">Electron gas (also called jellium model). There is no lattice, and the electrons just move around, interacting only through the Coulomb force. The density would be more uniform than what I have drawn in the figure, but I did not want to draw them spaced exactly equally, because this would suggest that the electrons form a lattice.</figcaption>
</figure>

Now, suppose we have an external charge \\(+Q\\) sitting in an electron gas. Note that an electron gas has a uniformly charged positive background. Then, we have something like the following Figure. We see that the negative charges will be drawn to it. 


<figure class="center">
<p><img src="figures/impurity_charge_interacting_electron_gas.pdf" alt="Function" class="center" style="width:142.131px;height:142.131px;"> </p><figcaption class="center">Electron gas with an impurity at the origin. The electrons work to screen the impurity charge. This is actually an effect which can be derived <i>classically</i>. In the lecture notes, this effect was studied semiclassically, but you can look up Debye-H\"uckel theory, where a fully classical calculation can show the existence of something analogous to Thomas-Fermi screening. The electrons screen strongly close to the impurity, but more weakly as we move farther from the impurity.</figcaption>
</figure>

However, the picture that we have just discussed is incomplete. We remember that, in quantum mechanics, electrons are described by wave functions, and in the electron gas electron wave functions look like \\(\psi\_{\k}(\x) = \frac{1}{\sqrt{\V}}\sin(\k\cdot\x)\\). This wave function has a charge density which looks like \\(\|\psi\_{\k}(\x)\|^2\\). Thus, an electron with wave vector \\(\k\\) has size \\(\lambda/2 = \frac{\pi}{k}\\). Note that the size is halved because we take the modulus squared to get the actual charge density of the electron.

<figure class="center">
<p><img src="figures/wave_function_size.pdf" alt="Function" class="center" style="width:207.042px;height:161.791px;"> </p><figcaption class="center">Wave function and charge density of an electron with wave vector \(\k\). The wavelength is \(\lambda = 2\pi/k\), so the size of the electron is \(\lambda/2 = \pi/k\).</figcaption>
</figure>

\newpage

Now to modify our cartoon, we need to draw the electrons as ovals with length \\(\lambda/2\\). Doing this, we have that 

<figure class="center">
<p><img src="figures/friedel_oscillation_configuration.pdf" alt="Function" class="center" style="width:142.131px;height:142.131px;"> </p><figcaption class="center">Electron gas with an impurity at the origin. The first layer of charges screen the impurity. The width of the screening region is \(0 < r < \lambda/2\). After this distance, the negative background compensates for the electrons, and again the electrons see a positive impurity. Then, the next layer comes in for \(\lambda/2 < r < \lambda\). This forms the second layer. This continues on, and we have a periodic pattern with wavelength \(\lambda/2\). This periodic pattern is called <i>Friedel oscillations</i>.</figcaption>
</figure>

The key thing to notice here is that the size of the electron is \\(\lambda/2 = \pi/k\\), but since only low-energy electrons contribute, \\(k = k\_F\\). Thus the oscillation should repeat itself with period \\(\lambda\_F/2 = \pi/k\_F\\). Thus, we should have something like \\(\cos(2\pi r/(\pi/k\_F)) = \cos(2k\_Fr)\\). The rate at which the decay occurs, we cannot predict unless we do some math. Let us see if we are at least correct about the oscillations.

