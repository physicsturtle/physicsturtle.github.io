---
layout: exercises
title: Pairing requires an attractive interaction  - Exercises
dept: physics
course: superconductivity
unit: unit4
deptDisplay: Physics
courseDisplay: Superconductivity & Superfluidity
unitDisplay: Unit 4
---
<ol>
<li> <div class="exercise">  One subtlety of the above calculation is that the wave vector \(\k\) is the wave vector of the displacement between the two particles. However, if we are concerned with the Fermi surface, then the wave vector should be that of the actual individual electron. Show that the wavevectors \(\k_1,\k_2\), corresponding to the coordinates \(\r_1,\r_2\), are related to the wave vectors \(\k,\K\) of the relative and centre of mass coordinates \(\r,\boldsymbol{R}\) via 

$$\begin{equation}
\k_1 = \frac{1}{2}\K + \k,\quad \k_2 = \frac{1}{2}\K - \k
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer7')" class="answerButton">Show Answer</button> 
 <div  id='answer7' class="answer" >
The wave function of the pair is

$$\begin{equation}
\psi(\r_1,\r_2) = \psi(\r,\boldsymbol{R})
\end{equation}$$

where there are two different forms of the coordinates. Let us consider Fourier transforming both of these:

$$\begin{align}
\psi(\r_1,\r_2) ={}& \int e^{i\k_1\cdot\r_1} e^{i\k_2\cdot\r_2} \psi(\k_1,\k_2) \frac{\d^d\k_1}{(2\pi)^d} \frac{\d^d\k_2}{(2\pi)^d} \\
\psi(\r,\boldsymbol{R}) ={}& \int e^{i\k\cdot\r} e^{i\K\cdot\boldsymbol{R}} \psi(\k,\K) \frac{\d^d\k}{(2\pi)^d} \frac{\d^d\K}{(2\pi)^d}
\end{align}$$

Now, performing the variable transformation

$$\begin{equation}
\r = \r_1-\r_2,\qquad \boldsymbol{R} = \frac{\r_1+\r_2}{2},\qquad \r_1 = \boldsymbol{R} + \frac{1}{2}\r,\quad \r_2 = \boldsymbol{R} - \frac{1}{2}\r
\end{equation}$$

we can write 

$$\begin{align}
\psi(\k,\K) ={}& \int e^{-i\k\cdot\r} e^{-i\K\cdot\boldsymbol{R}} \psi(\r,\boldsymbol{R}) \d^d\r\d^d\boldsymbol{R} \\
={}& \int e^{-i\k\cdot\r} e^{-i\K\cdot\boldsymbol{R}} \psi(\r_1,\r_2) \d^d\r\d^d\boldsymbol{R} \\
={}& \int e^{-i\k\cdot\r} e^{-i\K\cdot\boldsymbol{R}} \int e^{i\k_1\cdot\r_1} e^{i\k_2\cdot\r_2} \psi(\k_1,\k_2) \frac{\d^d\k_1}{(2\pi)^d} \frac{\d^d\k_2}{(2\pi)^d} \d^d\r\d^d\boldsymbol{R} \\
={}& \int e^{-i\k\cdot\r} e^{-i\K\cdot\boldsymbol{R}} \int e^{i\k_1\cdot(\boldsymbol{R} + \r/2)} e^{i\k_2\cdot(\boldsymbol{R} - \r/2)} \psi(\k_1,\k_2) \frac{\d^d\k_1}{(2\pi)^d} \frac{\d^d\k_2}{(2\pi)^d} \d^d\r\d^d\boldsymbol{R} \\
={}& \int \delta^{(d)}(\k_1/2 - \k_2/2 - \k) \delta^{(d)}(\k_1+\k_2-\K) \psi(\k_2,\k_1) \d^d\k_1 \d^d\k_2
\end{align}$$

Thus, we have that 

$$\begin{equation}
\K = \k_1 + \k_2,\quad \k = \frac{1}{2}(\k_1-\k_2)
\end{equation}$$

Therefore, solving for \(\k_1\) and \(\k_2\), we have that

$$\begin{equation}
\k_1 = \frac{1}{2}\K + \k,\quad \k_2 = \frac{1}{2}\K - \k
\end{equation}$$
</div> 
 </div>

 
 
</div> </li></ol>


