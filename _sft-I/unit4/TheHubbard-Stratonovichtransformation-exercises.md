---
layout: exercises
title: The Hubbard-Stratonovich transformation  - Exercises
dept: physics
course: sft-I
unit: unit4
deptDisplay: Physics
courseDisplay: Statistical Field Theory I
unitDisplay: Unit 4
---
<ol>
<li> <div class="exercise">  In this problem, we are going to show that the mean field theory (MFT) is exact for the infinite-range Ising model. Let's consider the Ising Hamiltonian

$$\begin{align}
H = -\frac{1}{2}\sum_{ij}J_{ij}S_iS_j
\end{align}$$

and assume that \(J_{ij}\) has the same value for any sites \(i,j\). In particular, let \(J_{ij} = J/N\), where \(N\) is the total number of sites.

<ol type="a">
<li> Show that the Ising model Hamiltonian in this case is 

$$\begin{align}
H = -\frac{J}{2N}\left(\sum_i S_i\right)^2
\end{align}$$

</li>
<li> The Hubbard-Stratonovich transformation is easier in this case, because \(\sum_i S_i\) can be treated as one variable. Show that the partition function becomes (apart from a non-essential prefactor \(\sqrt{N/(2\pi JT)}\)

$$\begin{align}
Z = \sum_{\{S\}}\int_{-\infty}^\infty e^{-\frac{N}{2JT}\varphi^2 + \frac{\varphi}{T}\sum_i S_i}\d\varphi = \int_{-\infty}^\infty e^{-NS[\phi]} \d\varphi
\end{align}$$

and write down the expression for \(S[\varphi]\).

</li>
<li> Write down the equation for \(\bar{\varphi}\) that minimizes \(S[\varphi]\).
</li>
<li> Expand \(S[\varphi]\) around the value \(\bar{\varphi}\) that minimizes it (without explicitly calculating \(\bar{\varphi}\) and \(\d^2S/\d\varphi^2\)), calculate the free energy and show that in the limit \(N\to\infty\) you get 

$$\begin{align}
F = NTS[\bar{\varphi}]
\end{align}$$
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer32')" class="answerButton">Show Answer</button> 
 <div  id='answer32' class="answer" >
<ol type="a">
<li> This is trivial, as we can write 

$$\begin{align}
H = -\frac{1}{2N}J \sum_{ij} S_i S_j = -\frac{J}{2N}\left(\sum_i S_i\right)^2
\end{align}$$

</li>
<li> We can write 

$$\begin{align}
e^{\beta J(\sum S)^2/2N} = e^{b^2/4a}
\end{align}$$

where we set \(b = \beta \sum S\), and \(a = \frac{N}{2J T}\). Thus 

$$\begin{align}
\int_{-\infty}^\infty e^{-\frac{N}{2JT}\varphi^2 + \frac{\varphi}{T}\sum_i S_i} \d\varphi = e^{\beta J (\sum S)^2 /2N}
\end{align}$$

Thus, the partition function is 

$$\begin{align}
Z = \sum_{\{S\}} e^{-\beta H} = \sum_{\{S\}} \int_{-\infty}^\infty e^{-\frac{N}{2JT}\varphi^2 + \frac{\varphi}{T}\sum_i S_i} \d\varphi
\end{align}$$

We can now exactly evaluate the sum over \(\{S\}\). This gives us 

$$\begin{align}
Z = \int_{-\infty}^\infty e^{-\frac{N}{2JT}\varphi^2}\left[2\cosh\frac{\varphi}{T}\right]^N \d\varphi
\end{align}$$

We can rewrite this as 

$$\begin{align}
Z = \int_{-\infty}^\infty e^{-NS} \d\varphi
\end{align}$$

where

$$\begin{align}
S[\varphi] = \frac{1}{2JT}\varphi^2 - \log\cosh\frac{\varphi}{T}
\end{align}$$

</li>
<li> Now, we calculate 

$$\begin{align}
\frac{\partial S}{\partial \phi} = \frac{N\varphi}{JT} - \frac{N}{T} \tanh\frac{\varphi}{T} = 0
\end{align}$$

Thus 

$$\begin{align}
\bar{\varphi} = J\tanh\frac{\bar{\varphi}}{T}
\end{align}$$

</li>
<li> Taylor expanding, we find 

$$\begin{align}
S[\varphi] = S[\bar{\varphi}] + (\varphi - \bar{\varphi})^2S'[\bar{\varphi}] + \frac{1}{2}(\varphi - \bar{\varphi})^2 \frac{\partial^2 S}{\partial\varphi^2}
\end{align}$$

Thus 

$$\begin{align}
Z = \int_{-\infty}^\infty e^{-S[\bar{\varphi}]} e^{-\frac{1}{2}\delta\varphi \partial^2S/\partial\varphi^2} \d(\delta\varphi) = e^{-NS[\bar{\varphi}]} \sqrt{\frac{2\pi}{N\partial^2S/\partial\varphi^2}}
\end{align}$$

Thus, 

$$\begin{align}
F = -T\log Z = TNS[\bar{\varphi}] + T\log N + \cdots
\end{align}$$

The \(N\) part dominates, and we find 

$$\begin{align}
F = NTS[\bar{\varphi}].
\end{align}$$

</li></ol>
</div> 
 </div>

</div> </li></ol>

