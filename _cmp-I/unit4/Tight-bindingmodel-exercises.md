---
layout: exercises
title: Tight-binding model  - Exercises
dept: physics
course: cmp-I
unit: unit4
deptDisplay: Physics
courseDisplay: Condensed Matter Physics I
unitDisplay: Unit 4
---
<ol>
<li> <div class="exercise">  Consider a tight-binding model on the square lattice with dispersion

\(\)\epsilon_{\k} = -2t(\cos(k_xa) + \cos(k_ya))\(\)

<ol type="a">
<li> Plot the Fermi surface for \(\mu = 0\)
</li>
<li> Plot the Fermi surface for \(\mu = t\)
</li>
<li> Suppose the system undergoes magnetic ordering with wavevector \((\pi/a,\pi/a)\). Draw the new Brillouin zone for the case \(\mu = t\). Plot the new Fermi surface
</li>
<li> For the reuslt of part (c), does the volume of the Fermi surface change or not?
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer12')" class="answerButton">Show Answer</button> 
 <div  id='answer12' class="answer" >
<ol type="a">
<li> We define \(\xi_{\k} = \epsilon_{\k} - \mu\)
</li>
<li> Now setting \(\xi_{\k} = 0\) we plot \(\epsilon_{\k} = t\), 
</li>
<li> 
</li>
<li> The volume should not change. Although the Brillouin zone shrinks in size, the number of bands doubles and therefore there are the same number of charge carriers.
</li></ol>
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Consider the triangular lattice. The Bravais lattice vectors are \(\mathbf{a}_1 = a(1,0)\), and \(\mathbf{a}_2 = a(1/2,\sqrt{3}/2)\). Compute the tight-binding band structure for the Hamiltonian

\(\)\Hhat = -t\sum_{\langle i,j\rangle;\sigma} (\chat^\dagger_{i\sigma} \chat_{j\sigma} + \hc)\(\)

<figure class="center">
<p><img src="figures/triangular_lattice.pdf" alt="Function" class="center" style="width:170.079px;height:170.079px;"> </p><figcaption class="center">Triangular lattice</figcaption>
</figure>

<div class="answerBox"> 
 <button onclick="myFunction('answer169')" class="answerButton">Show Answer</button> 
 <div  id='answer169' class="answer" >
The 
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Consider the honeycomb lattice. The Bravais lattice vectors are \(\mathbf{a}_1 = a(3/2,\sqrt{3}/2)\) and \(\mathbf{a}_2 = a(0,\sqrt{3})\). The unit cell contains one A site and one B site. We also define the vector \(\mathbf{a}_3 = \mathbf{a}_2 - \mathbf{a}_1 = (-3/2,\sqrt{3}/2)\). The unit \(a\) is the distance between <i>sites</i>, not <i>Bravais lattice sites</i>. Remember that there is a difference between a site and Bravais lattice site because the honeycomb lattice has a 2 site basis.

<figure class="center">
<p><img src="figures/honeycomb_lattice.pdf" alt="Function" class="center" style="width:170.079px;height:170.079px;"> </p><figcaption class="center">Honeycomb lattice. There are two sublattices, indicated by the red and blue dots.</figcaption>
</figure>
	
<div class="answerBox"> 
 <button onclick="myFunction('answer272')" class="answerButton">Show Answer</button> 
 <div  id='answer272' class="answer" >
The Hamiltonian can be rewritten as

\(\)\Hhat = - t\sum_{i} \sum_{j\in[i]} \chat^\dagger_{i\sigma} \chat_{j\sigma}\(\)

Then, we can rewrite the sum as 

\(\)\Hhat = - t\sum_{i\in A}\sum_{j\in[i]}  \chat^\dagger_{i\sigma} \chat_{j\sigma} - t\sum_{i\in B}\sum_{j\in[i]}  \chat^\dagger_{i\sigma} \chat_{j\sigma}\(\)

Then defining now that \(i\) is a Bravais lattice site, instead of an actual lattice site, we have

\(\)\chat_{i\sigma} = \begin{cases}
\chat_{i1\sigma}, & i\in A \\
\chat_{i2\sigma}, & i\in B 
\end{cases}\(\)

then we need to be careful about intra vs. inter unit cell hoppings. If we define the unit cell to be the site at (0,0) and the site at \((a,0)\), then we find that the Hamiltonian can be rewritten as 

\(\)\Hhat = - t\sum_{i\in A}\chat^\dagger_{i1\sigma}(\chat_{i2\sigma} + \chat_{i + \mathbf{a}_3,2\sigma} + \chat_{i - \mathbf{a}_1,2\sigma}) - t\sum_{i\in B}\chat^\dagger_{i2\sigma} (\chat_{i1\sigma} + \chat_{i+\mathbf{a}_1,1\sigma} + \chat_{i - \mathbf{a}_3,1\sigma})\(\)

Then, we plug in the Fourier transforms 

\(\)\chat_{in\sigma} = \frac{1}{\sqrt{N_s}}\sum_{\k} e^{i\k\cdot\mathbf{R}_i} \chat_{\k n\sigma}\(\)

This gives us 

$$\begin{align}
\Hhat ={}& -\frac{t}{N_s}\sum_{\k\k'}\sum_{i\in A}\chat^\dagger_{\k 1\sigma} e^{-i\k\cdot\mathbf{R}_i}(e^{i\k'\cdot\mathbf{R}_i} + e^{i\k'\cdot(\mathbf{R}_i + \mathbf{a}_3)} + e^{i\k'\cdot(\mathbf{R}_i - \mathbf{a}_1)})\chat_{\k' 2\sigma} \\
&- \frac{t}{N_s}\sum_{\k\k'}\sum_{i\in B} \chat^\dagger_{\k2\sigma} e^{-i\k\cdot\mathbf{R}_i}( e^{i\k'\cdot\mathbf{R}_i} + e^{i\k'\cdot(\mathbf{R}_i + \mathbf{a}_1)} + e^{i\k'\cdot(\mathbf{R}_i - \mathbf{a}_3)}) \chat_{\k' 1\sigma} \\
={}& -\frac{t}{N_s}\sum_{\k\k'}\sum_{i\in A}\chat^\dagger_{\k 1\sigma} e^{-i(\k-\k')\cdot\mathbf{R}_i}(1+ e^{i\k'\cdot\mathbf{a}_3} + e^{-i\k'\cdot\mathbf{a}_1})\chat_{\k' 2\sigma} \\
&- \frac{t}{N_s}\sum_{\k\k'}\sum_{i\in B} \chat^\dagger_{\k2\sigma} e^{-i(\k-\k')\cdot\mathbf{R}_i}(1 + e^{i\k'\cdot\mathbf{a}_1} + e^{-i\k'\cdot\mathbf{a}_3}) \chat_{\k' 1\sigma}
\end{align}$$

Then summing over lattice sites gives us 

$$\begin{align}
\Hhat ={}& -t\sum_{\k\k'}\delta_{\k\k'} \chat^\dagger_{\k 1\sigma} (1+ e^{i\k'\cdot\mathbf{a}_3} + e^{-i\k'\cdot\mathbf{a}_1})\chat_{\k' 2\sigma} - t\sum_{\k\k'}\delta_{\k\k'} \chat^\dagger_{\k2\sigma} (1 + e^{i\k'\cdot\mathbf{a}_1} + e^{-i\k'\cdot\mathbf{a}_3}) \chat_{\k' 1\sigma} \\
={}& -t\sum_{\k} \chat^\dagger_{\k 1\sigma} (1+ e^{i\k\cdot\mathbf{a}_3} + e^{-i\k\cdot\mathbf{a}_1})\chat_{\k 2\sigma} - t\sum_{\k} \chat^\dagger_{\k2\sigma} (1 + e^{i\k\cdot\mathbf{a}_1} + e^{-i\k\cdot\mathbf{a}_3}) \chat_{\k 1\sigma} \\
={}& -t\sum_{\k}\begin{pmatrix} \chat^\dagger_{\k 1\sigma} & \chat^\dagger_{\k 2\sigma} \end{pmatrix} \begin{pmatrix} 0 & 1+ e^{i\k\cdot\mathbf{a}_3} + e^{-i\k\cdot\mathbf{a}_1} \\ 1 + e^{i\k\cdot\mathbf{a}_1} + e^{-i\k\cdot\mathbf{a}_3} & 0 \end{pmatrix} \begin{pmatrix} \chat_{\k 1\sigma} \\ \chat_{\k 2\sigma} \end{pmatrix}
\end{align}$$

Then, we can digaonalize this matrix. The eigenvalues and (normalized) eigenvectors are simply 

\(\)\lambda_\pm = \pm\|1 + e^{i\k\cdot\mathbf{a}_3} + e^{-i\k\cdot\mathbf{a}_1}\|\(\)

These can be simplified a little bit to find 

$$\begin{align}
\lambda_\pm ={}& \pm\sqrt{(1 + \cos(\k\cdot\mathbf{a}_3) + \cos(\k\cdot\mathbf{a}_1))^2 + (\sin(\k\cdot\mathbf{a}_3) - \sin(\k\cdot\mathbf{a}_1))^2} \\
={}& \pm\sqrt{3 + 2\cos(\k\cdot\mathbf{a}_1) + 2\cos(\k\cdot\mathbf{a}_3) + 2\cos(\k\cdot\mathbf{a}_1)\cos(\k\cdot\mathbf{a}_3) - 2\sin(\k\cdot\mathbf{a}_3)\sin(\k\cdot\mathbf{a}_1)} \\
={}& \pm\sqrt{3 + 2(\cos(\k\cdot\mathbf{a}_1) + \cos(\k\cdot\mathbf{a}_2) + \cos(\k\cdot\mathbf{a}_3))}
\end{align}$$

Then, if we plug in our lattice vectors, then this simplifies to 

\(\)\lambda_\pm = \pm\sqrt{3 + 4\cos\left(\frac{3k_x a}{2}\right)\cos\left(\frac{\sqrt{3}k_y a}{2}\right) + 2\cos(\sqrt{3}k_y a)}\(\)

Since we have the double angle identity \(\cos(2\theta) = 2\cos^2\theta - 1\), we can rewrite this as 

\(\)\lambda_\pm = \pm\sqrt{1 + 4\cos\left(\frac{3k_x a}{2}\right)\cos\left(\frac{\sqrt{3}k_y a}{2}\right) + 4\cos^2\left(\frac{\sqrt{3}k_y a}{2}\right)}\(\)

These are the energy bands:

\(\)\epsilon_\pm(\k) = \pm\sqrt{1 + 4\cos\left(\frac{3k_x a}{2}\right)\cos\left(\frac{\sqrt{3}k_y a}{2}\right) + 4\cos^2\left(\frac{\sqrt{3}k_y a}{2}\right)}\(\)

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Consider the kagome lattice. Compute the tight-binding band structure for the nearest neigbour hopping Hamiltonian

$$\begin{equation}
\Hhat = -t\sum_{\langle i,j\rangle} (\chat^\dagger_{i\sigma} \chat_{j\sigma} + \hc).
\end{equation}$$

<figure class="center">
<p><img src="figures/kagome_lattice.pdf" alt="Function" class="center" style="width:170.079px;height:170.079px;"> </p><figcaption class="center">Kagome lattice. There are three sublattices, indicated by the red, blue, and green dots.</figcaption>
</figure>

<div class="answerBox"> 
 <button onclick="myFunction('answer740')" class="answerButton">Show Answer</button> 
 <div  id='answer740' class="answer" >
There are three sublattices in this Hamiltonian. We define the \(A,B,C\) sublattices as the red \({\color{red}A}\), blue \({\color{blue}B}\), and green \({\color{green}C}\), respectively. The primitive basis vectors are \(\mathbf{a}_1 = a(2,0)\), \(\mathbf{a}_2 = a(1,\sqrt{3})\), and \(\mathbf{a}_3 = a(-1,\sqrt{3})\), where \(a\) is the lattice spacing between neighbouring sites. The hopping Hamiltonian can be rewritten as 

$$\begin{align}
\Hhat ={}& -t\sum_{ij} \chat^\dagger_{i\sigma} \chat_{j\sigma} \\
={}& -t\sum_{i\in \text{BL}} \chat^\dagger_{i1\sigma}(\chat_{i2\sigma} + \chat_{i3\sigma} + \chat_{i-\mathbf{a}_1,2\sigma} + \chat_{i-\mathbf{a}_2,3\sigma}) \\
&-t\sum_{i\in\text{BL}} \chat^\dagger_{i2\sigma}(\chat_{i1\sigma} + \chat_{i3\sigma} + \chat_{i+\mathbf{a}_1,1\sigma} + \chat_{i-\mathbf{a}_3,3\sigma}) \\
&-t\sum_{i\in\text{BL}} \chat^\dagger_{i3\sigma}(\chat_{i1\sigma} + \chat_{i2\sigma} + \chat_{i+\mathbf{a}_2,1\sigma} + \chat_{i+\mathbf{a}_3,2\sigma})
\end{align}$$

where the sum in the first line is over all sites (there are \(3N\) sites, where \(N_s\) is the number of Bravais lattice unit cells), whereas when \(i,j\in\text{BL}\), then \(i,j\) label Bravais lattice unit cells. Of course the associated Bravais lattice is a triangular lattice. Next, we perform a Fourier transform as:

\(\)\chat_{ia\sigma} = \frac{1}{\sqrt{N_s}}\sum_{\k} e^{i\k\cdot\mathbf{R}_i} \chat_{\k a\sigma}, \quad \chat^\dagger_{ia\sigma} = \frac{1}{\sqrt{N_s}}\sum_{\k} e^{-i\k\cdot\mathbf{R}_i} \chat^\dagger_{\k a\sigma}\(\)

If we do this, then we find that 

$$\begin{align}
\Hhat ={}& - \frac{t}{N_s}\sum_{\k\k'}\sum_{i\in \text{BL}} e^{-i\k'\cdot\mathbf{R}_i} e^{i\k\cdot\mathbf{R}_i} \chat^\dagger_{\k'1\sigma}(\chat_{i2\sigma}(1 + e^{-i\k\cdot\mathbf{a}_1}) + \chat_{\k3\sigma}(1 + e^{-i\k\cdot\mathbf{a}_2})) \\
& - \frac{t}{N_s}\sum_{\k\k'}\sum_{i\in\text{BL}} e^{-i\k'\cdot\mathbf{R}_i} e^{i\k\cdot\mathbf{R}_i} \chat^\dagger_{\k'2\sigma}(\chat_{\k1\sigma}(1 + e^{i\k\cdot\mathbf{a}_1}) + \chat_{\k3\sigma}(1 + e^{-i\k\cdot\mathbf{a}_3})) \\
& - \frac{t}{N_s}\sum_{\k\k'}\sum_{i\in\text{BL}} e^{-i\k'\cdot\mathbf{R}_i} e^{i\k\cdot\mathbf{R}_i} \chat^\dagger_{\k'3\sigma}(\chat_{i1\sigma}(1 + e^{i\k\cdot\mathbf{a}_2}) + \chat_{i2\sigma}(1 + e^{i\k\cdot\mathbf{a}_3}))
\end{align}$$

Then we use the identity 

\(\)\sum_{i\in\text{BL}} e^{-i\k'\cdot\mathbf{R}_i} e^{i\k\cdot\mathbf{R}_i} = N_s\delta_{\k\k'}\(\)

and perform sums over \(i\) and \(\k'\), which gives us 

$$\begin{align}
\Hhat ={}& - t\sum_{\k} \chat^\dagger_{\k1\sigma}(\chat_{i2\sigma}(1 + e^{-i\k\cdot\mathbf{a}_1}) + \chat_{\k3\sigma}(1 + e^{-i\k\cdot\mathbf{a}_2})) \\
& - t\sum_{\k} \chat^\dagger_{\k2\sigma}(\chat_{\k1\sigma}(1 + e^{i\k\cdot\mathbf{a}_1}) + \chat_{\k3\sigma}(1 + e^{-i\k\cdot\mathbf{a}_3})) \\
& - t\sum_{\k} \chat^\dagger_{\k3\sigma}(\chat_{i1\sigma}(1 + e^{i\k\cdot\mathbf{a}_2}) + \chat_{i2\sigma}(1 + e^{i\k\cdot\mathbf{a}_3}))
\end{align}$$

This can be rewritten in a matrix form as 

$$\begin{align}
\Hhat ={}& - t\sum_{\k} \begin{pmatrix} \chat^\dagger_{\k1\sigma} & \chat^\dagger_{\k2\sigma} & \chat^\dagger_{\k3\sigma} \end{pmatrix} 
\begin{pmatrix} 0 & 1 + e^{-i\k\cdot\mathbf{a}_1} & 1 + e^{-i\k\cdot\mathbf{a}_2} \\ 
1 + e^{i\k\cdot\mathbf{a}_1} & 0 & 1 + e^{-i\k\cdot\mathbf{a}_3} \\
1 + e^{i\k\cdot\mathbf{a}_2} & 1 + e^{i\k\cdot\mathbf{a}_3} & 0 
\end{pmatrix} 
\begin{pmatrix} \chat_{\k1\sigma} \\ \chat_{\k2\sigma} \\ \chat_{\k3\sigma} \end{pmatrix}
\end{align}$$

The band structure of this can be found by diagonalizing the matrix. If we diagonalize this, then the eigenvalues are: 

\(\)\lambda_{1,2} = -t \pm \sqrt{3 + 2(\cos(\k\cdot\mathbf{a}_1) + \cos(\k\cdot\mathbf{a}_2) + \cos(\k\cdot\mathbf{a}_3))}, \quad \lambda_3 = 2t\(\)

The band structure can be plotted in the first Brillouin zone. We will plot along the path \(\Gamma\to K\to M \to \Gamma\), where the points are 

\(\)\Gamma = (0,0), \qquad K = \left(\frac{4\pi}{3a}\right), \qquad M = \left(\frac{\pi}{a},\frac{\pi}{a\sqrt{3}}\right)\(\)

this gives us INSERT FIGURE HERE. 

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  What is the degree of divergence for the van Hove singularities at \(\epsilon = 0\) and \(\epsilon = -2t\) for the kagome lattice band structure?

</div> </li>
<li> <div class="exercise">  Consider the square lattice dispersion:

\(\)\epsilon_{\k} = -2t(\cos(k_xa) + \cos(k_ya))\(\)

<ol type="a">
<li> Show that 
\(\)\rho(\epsilon) = \begin{cases} 
\frac{1}{2\pi^2}K(1 - \epsilon^2/16) & \|\epsilon\| w \\ 0 & else \end{cases}\(\)

where \(K\) is the elliptic integral of the first kind.
</li>
<li> What is the singularity at.... the fermi level?
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer812')" class="answerButton">Show Answer</button> 
 <div  id='answer812' class="answer" >
<ol type="a">
<li> 
</li>
<li> \(\rho(\epsilon) \sim \log(1/\|\epsilon\|)\). 

</li></ol>
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  \url{https://doi.org/10.1002/andp.19955070405} Density of states for triangular, honeycomb, kagome lattices

</div> </li></ol>



