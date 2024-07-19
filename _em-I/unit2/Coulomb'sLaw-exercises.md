---
layout: exercises
title: Coulomb's Law  - Exercises
dept: physics
course: em-I
unit: unit2
deptDisplay: Physics
courseDisplay: Electromagnetism I
unitDisplay: Unit 2
---
<ol>
<li> <div class="exercise">  Consider 8 point charges, each of charge \(q\), at the vertices of a cube of side length \(2a\) centred at the origin. Calculate the electric field at a point \((0,0,z)\). 

<div class="answerBox"> 
 <button onclick="myFunction('answer3')" class="answerButton">Show Answer</button> 
 <div  id='answer3' class="answer" >
We can apply symmetry here. The \(x\) and \(y\) components of the electric fields will be zero, so we only need to calculate the \(z\) component. First, let's get the contribution from the charges at \((a,a,a),(-a,a,a),(a,-a,a),\) and \((-a,-a,a)\). The magnitude of electric field due to the charge at \((a,a,a)\) is 

$$\begin{equation}
E_\text{top} = \frac{q}{4\pi\epsilon_0r_\text{top}}
\end{equation}$$

and the unit vector is \(\rhat_\text{top} = (a,a,z-a)/\sqrt{2a^2+(z-a)^2}\). Thus, the electric field from both the top and bottom charges is (the bottom ones are easy to construct once the top contribution is done)

$$\begin{equation}
\mathbf{E} = \frac{q(z-a)\zhat}{\pi\epsilon_0(2a^2+(z-a)^2)^{3/2}} + \frac{q(z+a)\zhat}{\pi\epsilon_0(2a^2+(z+a)^2)^{3/2}}
\end{equation}$$

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Consider an insulating wire \(\ell_1 + \ell_2\) metres long, which contains a charge density of \(\lambda\) coulombs/meter. Assume that the origin is at \(\ell_1\) from the bottom of the wire, as shown in the figure.
<ol type="a">
<li> Find the potential \(V\) at the point \((0,0,r)\) a distance \(r\) from the line of charge. 
</li>
<li> Compare your answer to part (a) with the expected potential if \(r \gg (\ell_1 + \ell_2)\).
</li>
<li> Check your answer to part (a) in the limit \(r \ll (\ell_1 + \ell_2)\) by comparing the electric field \(\mathbf{E}\) derived from \(V\) with the field derived using Gauss's law.
</li></ol>

<figure class="center"><p><img src="figures/uneven_wire_exercise.pdf" alt="Function" class="center" style="width:152.363px;height:89.291px;"> </p></figure>

<div class="answerBox"> 
 <button onclick="myFunction('answer36')" class="answerButton">Show Answer</button> 
 <div  id='answer36' class="answer" >
<ol type="a">
<li> The potential \(\d V\) at the point \((0,0,r)\) due to a small length \(\d x\) of the line is given by 

$$\begin{equation}
\d V = \frac{\d Q}{4\pi\epsilon_0 R} = \frac{\lambda \d x}{4\pi\epsilon_0\sqrt{x^2+r^2}}\end{equation}$$
Thus 

$$\begin{equation}
V = \int_{-\ell_1}^{\ell_2}  \frac{\lambda \d x}{4\pi\epsilon_0\sqrt{x^2+r^2}} = \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{\ell_2 +\sqrt{\ell_2^2+r^2}}{-\ell_1 + \sqrt{\ell_1^2+r^2}}\right\|
\end{equation}$$

</li>
<li> If \(r \gg \ell_1+\ell_2\), then we expect the line of charge to behave as a point charge with magnitude \(Q = \lambda(\ell_1+\ell_2)\). That would be \(\displaystyle{V \approx \frac{\lambda(\ell_1+\ell_2)}{4\pi\epsilon_0 r}}\). Recall \(\ln(1+x) \approx x\) for small \(x\). For the formula from part (a) we have

$$\begin{align}
V ={}&  \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{\ell_2 +\sqrt{\ell_2^2+r^2}}{-\ell_1 + \sqrt{\ell_1^2+r^2}}\right\|\\
\approx{}& \frac{\lambda}{4\pi\epsilon_0}\ln\left\|\frac{\ell_2 + r}{r - \ell_1}\right\| \\
={}& \frac{\lambda}{4\pi\epsilon_0}\ln\left\|\frac{\ell_2 +\ell_1 + r - \ell_1}{r - \ell_1}\right\|\\
={}& \frac{\lambda}{4\pi\epsilon_0}\ln\left\|1 + \frac{\ell_2 +\ell_1}{r - \ell_1}\right\|\\
\approx{}& \frac{\lambda}{4\pi\epsilon_0} \frac{\ell_2 +\ell_2}{r - \ell_1}\\
\approx{}& \frac{\lambda}{4\pi\epsilon_0} \frac{\ell_2 +\ell_2}{r}
\end{align}$$

Which agrees with what we have from the potential formula as if the length of charge was a point charge.

</li>
<li> Recall that \((x+1)^{1/2} \approx 1+x/2\) for small \(x\). If \(r \ll \ell_1 + \ell_2\), then

$$\begin{align}
V ={}&  \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{\ell_2 +\sqrt{\ell_2^2+r^2}}{-\ell_1 + \sqrt{\ell_1^2+r^2}}\right\|\\
={}&  \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{\ell_2(1 +\sqrt{1+r^2/\ell_2^2})}{\ell_1(-1 + \sqrt{1+r^2/\ell_1^2})}\right\|\\
\approx{}&  \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{\ell_2(1 +1+r^2/2\ell_2^2)}{\ell_1(-1 +1+r^2/2\ell_1^2)}\right\|\\
={}&  \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{\ell_2(2+r^2/2\ell_2^2)}{\ell_1(r^2/2\ell_1^2)}\right\|\\
\approx{}&  \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{\ell_2(2)}{r^2/2\ell_1}\right\|\\
={}& \frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{4\ell_1\ell_2}{r^2}\right\|\\
\end{align}$$

Differentiating,

$$\begin{align}
\mathbf{E} ={}& \left(-\frac{\d}{\d r}V\right)\rhat\\
={}&\left(-\frac{d}{dr} \left(\frac{\lambda}{4\pi\epsilon_0}\ln \left\| \frac{4\ell_1\ell_2}{r^2}\right\|\right)\right)\rhat\\
={}& \frac{\lambda}{2\pi\epsilon_0 r}\rhat
\end{align}$$

Using Gauss's law with a cylindrical gaussian surface, with axis along the line gives us 
$$\begin{equation}
\mathbf{E} = \frac{\lambda}{2\pi\epsilon_0 r}\rhat 
\end{equation}$$

Which agrees with the above result. 
</li></ol>

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  A charge \(Q\) is uniformly distributed over an <i>arc</i> (no charge along the \(x\) axis or radius) of radius \(a\) and angle \(\alpha\) that extends from the \(x\)-axis counterclockwise. Find the force (as a function of \(\alpha\)) on the charge \(q\). 
Hint: Pretend that the arc extends from \(-\alpha/2\) to \(\alpha/2\) so that you can exploit symmetry when performing the integration. 

<div class="answerBox"> 
 <button onclick="myFunction('answer93')" class="answerButton">Show Answer</button> 
 <div  id='answer93' class="answer" >
To find the force on charge \(q\) we will integrate the force over the circular arc. Linear charge density is $$\begin{equation}\lambda = \frac{Q}{a\alpha}\end{equation}$$
 Consider the force \(\d\mathbf{F}\) due to a small length of charge \(\d Q\), which resides at an angle \(\theta\). In order to simplify the problem, pretend like the arc extends along \([-\alpha/2,\alpha/2]\) instead of \([0,\alpha]\). This will cause the \(y\) components of the force to cancel out, so we would only need to find the force in the \(x\) direction. The force will then be

$$\begin{equation}
\d F_x = \frac{1}{4\pi\epsilon_0} \frac{q\d Q\cos\theta}{r^2} = \frac{1}{4\pi\epsilon_0}\frac{q \cos\theta \d Q }{a^2}
\end{equation}$$

Since \(\d Q = \lambda a\d\theta\), we can plug that in to the resulting integral:

$$\begin{equation}
F_x = \frac{1}{4 \pi \epsilon _0} \int_{-\alpha/2}^{\alpha/2}\frac{q\lambda}{a}\cos\theta \d\theta=\frac{1}{4 \pi \epsilon _0} 2\int_{0}^{\alpha/2}\frac{ qQ}{\alpha a^2}\cos\theta \d\theta
\end{equation}$$

Thus we have for the magnitude of the force in the \(x\) direction (with the rotated arc) to be

$$\begin{equation}
F_x =\frac{1}{4 \pi \epsilon _0} \frac{qQ}{a^2 \alpha}2\sin\left(\frac{\alpha}{2}\right) = \frac{1}{2 \pi \epsilon _0} \frac{qQ}{a^2 \alpha}\sin\left(\frac{\alpha}{2}\right) 
\end{equation}$$

If we want to find the force on the charge \(q\) when the arc is in its true position, we can deduce from symmetry that resultant force will be at an angle of \(\alpha/2\), and pointing towards the origin. Thus we can multiply the magnitude of the force by a unit vector that points towards the origin. That unit vector will be

$$\begin{equation}
\mathbf{u} = \left(-\cos \left(\frac{\alpha}{2}\right) ,-\sin \left(\frac{\alpha}{2}\right)\right)
\end{equation}$$

Thus the force on the charge \(q\) due to the wire which arcs from \([0,\alpha]\) will be 

$$\begin{equation}
\mathbf{F} = \frac{1}{2 \pi \epsilon _0} \frac{qQ}{a^2 \alpha}\sin\left(\frac{\alpha}{2}\right) \left(-\cos \left(\frac{\alpha}{2}\right) ,-\sin \left(\frac{\alpha}{2}\right)\right)
\end{equation}$$
</div> 
 </div>


</div> </li>
<li> <div class="exercise">  A charged square insulating wire of side length \(a\), of uniform linear charge density \(\lambda\), is centred about the origin of the \(xy\) plane with sides parallel to the \(x\) and \(y\) axes. A charge \(Q\) lies a distance \(\ell\) above its centre.
<ol type="a">
<li> Find the magnitude and direction of the force \(\mathbf{F}\) acting on the charge \(Q\).
</li>
<li> Find the approximate magnitude of the force \(\mathbf{F}\) acting on the charge \(Q\) for \(\ell \gg a\).
</li>
<li> Find the approximate magnitude of the force \(\mathbf{F}\) acting on the charge \(Q\) for \(\ell \ll a\). 
</li>
<li> If the charge \(Q\) has a mass \(m\), and \(\lambda < 0\), and \(Q > 0\), find the angular frequency of small oscillations of \(Q\) about the origin.
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer135')" class="answerButton">Show Answer</button> 
 <div  id='answer135' class="answer" >
<ol type="a">
<li>  Let \(\lambda\) be the linear charge density of the square insulator. Then, a little element of charge on the insulator is given by \(\d Q = \lambda \d x\), and the distance from any point \((x,y)\) on the square to the charge is given by \(r = \sqrt{x^2 + y^2 + \ell^2}\). First, note that the \(x\) and \(y\) components of the force on \(Q\) will cancel out, and it will only be pushed upwards. Thus, we only need to find the \(z\) component of force on \(Q\) from one of the sides, then multiply by 4. Let's integrate along the \(x\) direction.

$$\begin{align}
\d F_z ={}& \frac{Q\d Q\cos\theta}{4\pi\epsilon_0 r^2} \\
={}& \frac{Q\lambda \d x\cos\theta}{4\pi\epsilon_0 r^2} \\
={}& \frac{Q\lambda \d x}{4\pi\epsilon_0 r^2}\cdot \frac{\ell}{r} \\
={}& \frac{Q\ell\lambda \d x}{4\pi\epsilon_0 (x^2+y^2+\ell^2)^{3/2}}
\end{align}$$

Thus the force on \(Q\) is given by \(\mathbf{F} = F_z \zhat\). Note that we set \(y = a/2\) because we integrate along one side of the square, then multiply the final result by 4.

$$\begin{align}
F_z ={}& \int^{a/2}_{-a/2} \frac{Q\ell\lambda \d x}{4\pi\epsilon_0 (x^2 + y^2 + \ell^2)^{3/2}} \\
={}& \frac{Q\ell\lambda}{4\pi\epsilon_0}\cdot \int^{a/2}_{-a/2}\frac{\d x}{(x^2+(a/2)^2 + \ell^2)^{3/2}} \\
={}& \frac{Q\ell\lambda}{\pi\epsilon_0}\cdot \int^{a/2}_{-a/2} \frac{2\d x}{(4x^2+(4\ell^2+a^2))^{3/2}}
\end{align}$$

Evaluating the integral (I show the steps for evaluating the integral below if you're interested) gives:

$$\begin{align}
\frac{Q\ell\lambda}{\pi\epsilon_0}\cdot \int^{a/2}_{-a/2} \frac{2\d x}{(4x^2+(4\ell^2+a^2))^{3/2}} ={}& \frac{Q\ell \lambda}{\pi\epsilon_0(4l^2+a^2)}\cdot \left.\left( \frac{2x}{\sqrt{4x^2+4\ell^2+a^2}}\right)\right\|^{a/2}_{-a/2}\\
={}& \frac{Q\ell a\sqrt{2}\lambda}{\pi\epsilon_0(4\ell^2+a^2)\sqrt{a^2+2\ell^2}}
\end{align}$$

Thus the force on the charge (multiplying by 4) \(Q\) is

$$\begin{equation}
\mathbf{F} =  \frac{Q\ell a\lambda4\sqrt{2}}{\pi\epsilon_0(4\ell^2+a^2)\sqrt{a^2+2\ell^2}}\zhat
\end{equation}$$

</li>
<li> If \(\ell \gg a\), then \(4\ell^2 + a^2\approx 4\ell^2\), and \(\sqrt{a^2+2l^2}\approx \sqrt{2}\ell\). Then we have

$$\begin{equation}
\mathbf{F}\approx \frac{Qa\lambda}{\pi\epsilon_0 \ell^2}\zhat
\end{equation}$$

which agrees with the model of approximating the charged square as a point charge of magnitude \(4a\lambda\), at distance \(\ell\) from the charge \(Q\).

</li>
<li> If \(l \ll a\), then we can approximate \(4\ell^2 + a^2 \approx a^2\), and \(\sqrt{a^2+2\ell^2}\approx a\). Then we have

$$\begin{equation}
\mathbf{F} \approx \frac{\lambda Q \ell 4\sqrt{2}}{\pi\epsilon_0 a^2} \zhat
\end{equation}$$

</li>
<li> Relabelling \(\ell = z\), we can apply Newton's second law to obtain
$$\begin{equation} 
mz"(t) = \frac{Q\lambda 4\sqrt{2}}{\pi\epsilon_0 a^2}z(t)
\end{equation}$$

The angular frequency is then (we have a minus sign because \(Q\lambda < 0\))

$$\begin{equation}
\omega = \sqrt{-\frac{Q\lambda 4\sqrt{2}}{m\pi\epsilon_0 a^2}}
\end{equation}$$


</li></ol>

<b>Evaluation of the Integral (For those interested students)</b>
$$\begin{equation}
\frac{Q\ell\lambda}{\pi\epsilon_0}\cdot \int^{a/2}_{-a/2} \frac{2\d x}{(4x^2+(4\ell^2+a^2))^{3/2}}
\end{equation}$$

First, we find the antiderivative. Let \(2x = \sqrt{4\ell^2+a^2}\tan\theta \Rightarrow 2\d x = \sqrt{4\ell^2+a^2}\sec^2\theta \d\theta\). Then 

$$\begin{align}
\int \frac{2\d x}{(4x^2+(4\ell^2+a^2))^{3/2}} ={}& \int \frac{\sqrt{4\ell^2+a^2}\sec^2\theta \d\theta}{[(4\ell^2+a^2)\tan^2\theta+(4\ell^2+a^2)]^{3/2}} \\
={}& \frac{1}{4\ell^2+a^2}\cdot \int \cos\theta \d\theta = \frac{1}{4\ell^2+a^2}\sin\theta
\end{align}$$

Expressing \(\sin\theta\) in terms of \(x\) gives 

$$\begin{equation}
\frac{1}{4\ell^2+a^2}\sin\theta = \frac{1}{4\ell^2+a^2}\cdot \frac{2x}{\sqrt{4x^2+4\ell^2+a^2}}
\end{equation}$$

Now, plugging this back into the original expression gives: 
$$\begin{align}
\frac{Q\ell\lambda}{\pi\epsilon_0}\cdot \int^{a/2}_{-a/2} \frac{2\d x}{(4x^2+(4\ell^2+a^2))^{3/2}} ={}& \frac{Q\ell\lambda}{\pi\epsilon_0(4\ell^2+a^2)}\cdot \left.\left( \frac{2x}{\sqrt{4x^2+4\ell^2+a^2}}\right)\right\|^{a/2}_{-a/2}\\
={}& \frac{Q\ell a\sqrt{2}\lambda}{\pi\epsilon_0(4\ell^2+a^2)\sqrt{a^2+2\ell^2}}
\end{align}$$
</div> 
 </div>

</div> </li></ol>

