---
layout: exercises
title: Wick's Theorem  - Exercises
dept: physics
course: sft-I
unit: unit5
deptDisplay: Physics
courseDisplay: Statistical Field Theory I
unitDisplay: Unit 5
---
<ol>
<li> <div class="exercise">  In this problem, we will derive the generating function for a complex field. Consider the integral

$$\begin{align}
Z[\mathbf{J},\mathbf{J}^\dagger] = \int \exp\left(-\x^\dagger A \x - \mathbf{J}^\dagger\x - \x^\dagger \mathbf{J}\right) \d^d\z^\dagger\d^d\z
\end{align}$$

where the notation \(\d^d\x^\dagger \d^d\x = \d^d\Re\x \d^d\Im\x\). Compute this integral.

<div class="answerBox"> 
 <button onclick="myFunction('answer9')" class="answerButton">Show Answer</button> 
 <div  id='answer9' class="answer" >
First, we diagonalize and write \(A = U^\dagger \Lambda U\), so we get 

\(\)Z[\mathbf{J},\mathbf{J}^\dagger] = \int \exp\left(-\x^\dagger U^\dagger \Lambda U \x - \mathbf{J}^\dagger\x - \x^\dagger \mathbf{J}\right) \d^d\x^\dagger\d^d\x\(\)

where \(U\) is a unitary matrix. Now, we make the substitution \(\y = U\x\):

\(\)Z[\mathbf{J},\mathbf{J}^\dagger] = \int \exp\left(-\y^\dagger\Lambda\y- \mathbf{J}^\dagger U^\dagger\y - \y^\dagger U\mathbf{J}\right) \d^d\y^\dagger\d^d\y\(\)

which leads us to define \(<b>K</b> = U\mathbf{J}\), and we get 

\(\)Z[\mathbf{J},\mathbf{J}^\dagger] = \int \exp\left(-\y^\dagger\Lambda\y- <b>K</b>^\dagger \y - \y^\dagger <b>K</b>\right) \d^d\y^\dagger\d^d\y\(\)

Now, we change to index notation:

$$\begin{align}
Z[\mathbf{J},\mathbf{J}^\dagger] ={}& \int \exp\left(-\sum_{i=1}^d (y_i^* y_i \lambda_i + K_i^* y_i + y_i^* K_i) \right) \d^d\y^\dagger\d^d\y \\
={}& \int \exp\left(-\sum_{i=1}^d \lambda_i \left(y_i^* y_i + \frac{K_i^* y_i}{\lambda_i} + \frac{y_i^* K_i}{\lambda_i} \right) \right) \d^d\y^\dagger\d^d\y \\
={}& \int \exp\left(-\sum_{i=1}^d \lambda_i \left(y_i^* y_i + \frac{K_i^* y_i}{\lambda_i} + \frac{y_i^* K_i}{\lambda_i} + \frac{K_i^* K_i}{\lambda_i^2} - \frac{K_i^* K_i}{\lambda_i^2} \right) \right) \d^d\y^\dagger\d^d\y \\
={}& \int \exp\left(-\sum_{i=1}^d \lambda_i \left(y_i^* + \frac{K_i^*}{\lambda_i} \right)\left( y_i + \frac{K_i}{\lambda_i}\right) + \sum_i \frac{K_i^* K_i}{\lambda_i} \right) \d^d\y^\dagger\d^d\y
\end{align}$$

We now shift the integration variable to get 

$$\begin{align}
Z[\mathbf{J},\mathbf{J}^\dagger] ={}& \exp\left( \sum_i \frac{K_i^* K_i}{\lambda_i} \right) \int \exp\left(-\sum_{i=1}^d \lambda_iy_i^*y_i\right) \d^d\y^\dagger\d^d\y \\
={}& e^{<b>K</b>^\dagger\Lambda^{-1} <b>K</b>} \prod_{i=1}^d \int e^{-\lambda_i y_i^* y_i} \d y_i^* \d y_i \\
={}& e^{\mathbf{J}^\dagger U^\dagger \Lambda^{-1} U \mathbf{J}} \prod_{i=1}^d \int e^{-\lambda_i \Re(y_i)^2 - \lambda_i \Im(y_i)^2 } \d \Re(y_i) \d \Im(y_i)
\end{align}$$

Since \(A^{-1} = U^\dagger\Lambda^{-1} U\), we get 

$$\begin{align}
Z[\mathbf{J},\mathbf{J}^\dagger] ={}& e^{\mathbf{J}^\dagger A^{-1} \mathbf{J}} \prod_{i=1}^d \frac{\pi}{\lambda_i} \\
={}& e^{\mathbf{J}^\dagger A^{-1} \mathbf{J}} \frac{\pi^d}{\det(A)}
\end{align}$$

</div> 
 </div>


</div> </li>
<li> <div class="exercise">  In this problem, we will perform a simple generalization of Wick's theorem to a complex vector variable.
<ol type="a">
<li> Generalize the proof above to prove Wick's theorem for a complex vector \(\x \in \CC^d\). Consider a Hermitian matrix \(A\). 
</li>
<li> Write the four-point correlation function as a sum of two point generating functions. Use the generating function
</li></ol>

$$\begin{equation}
Z[\mathbf{J}, \mathbf{J}^\dagger] = \int \exp\left(-\frac{1}{2}\x^\dagger A\x + \mathbf{J}^\dagger \x + \x^\dagger \mathbf{J}\right) \d^d\x^* \d^d\x
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer59')" class="answerButton">Show Answer</button> 
 <div  id='answer59' class="answer" >
Coming
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Generalization of Wick's theorem. We want to prove that, if \(V_{i_1 i_2 i_3 i_4} = x^*_{i_1} x^*_{i_2}  x_{i_3}  x_{i_4} \), we can use Wick's theorem on the 16-point function \(A = \left<V_{i_1i_2i_3i_4} V_{j_1j_2j_3j_4} V_{k_1k_2k_3k_4} V_{\ell_1\ell_2\ell_3\ell_4} \right>\) which we have disguised as a 4-point function. 

<div class="answerBox"> 
 <button onclick="myFunction('answer65')" class="answerButton">Show Answer</button> 
 <div  id='answer65' class="answer" > 
Let's define 

\(\)\partial_I = \frac{\partial}{\partial J_{i_1}} \frac{\partial}{\partial J_{i_2}} \frac{\partial}{\partial J^*_{i_3}} \frac{\partial}{\partial J^*_{i_4}} \(\)

and similarly for the \(j\), \(k\), and \(\ell\) indices. Thus, we can write the 16-point function as

\(\)A =  \left(\partial_I \partial_J \partial_K \partial_L \right) Z[\mathbf{J}]\bigg|_{\mathbf{J} = 0}\(\)

Letting a single derivative operator act, we get

</div> 
 </div>

</div> </li>
<li> <div class="exercise">  In this problem, we will derive the generating function for the real vector but in Fourier space. We define 

$$\begin{equation}
x_n = \frac{1}{d} \sum_{m=1}^d e^{inq_m}x(q_m),\qquad x(q_m) = \sum_{n=1}^d e^{-inq_m}x_n
\end{equation}$$

where \(q_m = 2\pi m/d\), and both \(n,m\) run from \(1\) to \(d\), inclusive. We consider the same generating function, but after transforming to Fourier space, we will be able to generate correlation functions in momentum space by differentiating our new generating function. It is easiest to write the Fourier transform as a matrix equation. This is done like

$$\begin{equation}
\x = F\tilde{\x} \qquad \tilde{\x} = F^{-1}\x
\end{equation}$$

where \(F\) is the \(d\times d\) matrix with entries \(F_{nm} = \frac{1}{d}e^{inq_m}\). 


Plugging our expressions into the 

$$\begin{align}
-\frac{1}{2}\sum_{i,j} x_i A_{ij} x_j + \sum_i J_i x_i ={}& -\frac{1}{2}\left(\x^\dagger A \x - 2\mathbf{J}^\dagger\x \right) \\
={}& -\frac{1}{2}\left(\tilde{\x}^\dagger F^\dagger A F \tilde{\x} - 2\tilde{\mathbf{J}}^\dagger F^\dagger F\tilde{\x} \right)
\end{align}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer100')" class="answerButton">Show Answer</button> 
 <div  id='answer100' class="answer" >
Coming
</div> 
 </div>

</div> </li></ol>

