---
layout: lesson
title: Gaussian Integrals 
dept: physics
course: many-body-II
unit: unit31
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 31
---

It is common in physics to deal with probability distributions which are Gaussian or almost Gaussian. For this reason, we need to learn how to compute expectation values of physical observables with respect to these Gaussian or almost Gaussian probability distributions. The key mathematical tool to develop here is learning how to compute Gaussian integrals. 

We will review how to compute Gaussian integrals in one dimension. 

<div class="example">
<b>Example:</b>
<ol type="a">
<li> Evaluate the integral 

$$\begin{equation}
I = \int_{-\infty}^\infty e^{-x^2/2} \d x
\end{equation}$$

by first considering 

$$\begin{equation}
I^2 = \int_{-\infty}^\infty \int_{-\infty}^\infty e^{-x^2/2} e^{-y^2/2} \d x \d y
\end{equation}$$

Then, change to polar coordinates and evaluate the resulting integral exactly.

</li>
<li> By using the result from part (a), evaluate the integral

$$\begin{equation}
I(a) = \int_{-\infty}^\infty e^{-ax^2/2} \d x
\end{equation}$$

where \(a>0\) is a positive real number.

</li>
<li> Evaluate the integral

$$\begin{equation}
I(a,b) = \int_{-\infty}^\infty e^{-ax^2/2 - bx} \d x.
\end{equation}$$

Do this by completing the square in the exponential and then performing a change of variables.

</li>
<li> Evaluate the integral for any nonnegative integer \(n\):

$$\begin{equation}
I(a,n) = \int_{-\infty}^\infty x^n e^{-ax^2/2} \d x
\end{equation}$$

Do this by taking derivatives of the result of part (c) with respect to \(b\) and then setting \(b=0\).
</li></ol>

<b>Solution:</b>
<ol type="a">
<li> \(I = \sqrt{2\pi}\) 
</li>
<li> \(I = \sqrt{\frac{2\pi}{a}}\) 
</li>
<li> \(I = \sqrt{\frac{2\pi}{a}}e^{b^2/2a}\)
</li>
<li> \(I = 0\) if \(n\) is odd, but if \(n\) is even, then \(I = \sqrt{\frac{2\pi}{a}} \frac{(n)!}{(n/2)!(2a)^{n/2}}\)
</li></ol>

</div>

<div class="example">
<b>Example:</b>
In this problem we will generalize the discussion to multi-dimensional Gaussian integrals.

<ol type="a">
<li> Evaluate the multi-dimensional Gaussian integral

$$\begin{equation}
I(\lambda_1,\lambda_2,\dots,\lambda_d) = \int_{-\infty}^\infty \cdots \int_{-\infty}^\infty e^{-\lambda_1x_1^2/2 - \cdots -\lambda_d x_d^2/2} \d x_1 \cdots \d x_d
\end{equation}$$

where \(\lambda_1,\dots,\lambda_d\) are all positive real numbers.

</li>
<li> Consider a symmetric positive-definite matrix \(A\), which has dimensions \(d\times d\). (Recall that positive definite just means the eigenvalues are all positive). Then, evaluate the integral 

$$\begin{equation}
Z = \int_{-\infty}^\infty \cdots \int_{-\infty}^\infty e^{-\x^T A \x/2} \d x_1\cdots \d x_d
\end{equation}$$

where \(\x = (x_1,\dots,x_d)\) is an \(d\)-component column vector. Do this by diagonalizing the matrix \(A\) and doing a change of variables. 

</li>
<li> Consider an \(d\times d\) symmetric positive-definite matrix \(A\) and an \(d\)-component vector \(\mathbf{J}\). Then evaluate the integral 

$$\begin{equation}
Z(\mathbf{J}) = \int_{-\infty}^\infty \cdots \int_{-\infty}^\infty e^{-\x^T A \x/2 - \mathbf{J}^T \x} \d x_1\cdots \d x_d.
\end{equation}$$

Note that this \(Z(\mathbf{J})\) is called a <i>generating function</i>.

</li>
<li> We define the following \(n\)-point <i>correlation function</i>:

$$\begin{equation}
\langle x_{i_1}\dots x_{i_n}\rangle_0 = \frac{1}{Z(0)}\int x_{i_1}\dots x_{i_n} e^{-\x^T A \x/2} \d x_1 \cdots \d x_d.
\end{equation}$$

where \(Z\) is the result of part (b). Write \(\langle x_{i_1}\dots x_{i_n}\rangle_0\) in terms of derivatives of \(Z(\mathbf{J})\) from part (c).

</li>
<li> Compute \(\langle x_i x_j \rangle_0\). Express your answer in terms of the matrix elements of \(A\).
</li></ol>

<b>Solution:</b>

<ol type="a">
<li> 
$$\begin{equation}
I = \prod_{i=1}^n\sqrt{\frac{2\pi}{\lambda_i}}
\end{equation}$$

</li>
<li> Diagonalize the matrix \(A\), which transforms the situation to part (a). Then the product of eigenvalues is just the determinant of \(A\). Thus 

$$\begin{equation}
I = \sqrt{\frac{(2\pi)^d}{\det(A)}}
\end{equation}$$

</li>
<li> The first thing we do is rewrite the argument of the exponential

$$\begin{align}
-\frac{1}{2}\sum_{i,j} x_i A_{ij} x_j - \sum_i J_i x_i ={}& -\left(\frac{1}{2}\x^T  A \x + \mathbf{J}^T \x \right)\\
={}& -\left(\frac{1}{2}\x^T U^T \Lambda U \x + \mathbf{J}^T \x \right) \\
={}& -\left(\frac{1}{2}\y^T\Lambda \y + \mathbf{J}^TU^T\y  \right) \\
={}& -\left(\frac{1}{2}\y^T\Lambda \y + (U\mathbf{J})^T\y  \right)
\end{align}$$

where we made the substitution \(\y = U\x\). We switch now back to component notation, and define \(\mathbf{K} = U\mathbf{J}\). 

$$\begin{align}
-\frac{1}{2}\sum_{i,j} x_i A_{ij} x_j - \sum_i J_i x_i ={}& -\frac{1}{2}\left(\sum_i \left(y_i\lambda_i y_i  + 2K_i y_i  \right)\right) \\
={}& -\frac{1}{2}\left(\sum_i \lambda_i \left(y_i y_i + 2\frac{K_i}{\lambda_i} y_i  \right)\right) \\
={}& -\frac{1}{2}\left(\sum_i \lambda_i \left(y_i y_i + 2\frac{K_i}{\lambda_i} y_i + \left(\frac{K_i}{\lambda_i}\right)^2 - \left(\frac{K_i}{\lambda_i}\right)^2 \right)\right) \\
={}& -\frac{1}{2}\left(\sum_i\lambda_i\left[\left(y_i + \frac{K_i}{\lambda_i}\right)^2 - \left(\frac{K_i}{\lambda_i}\right)^2\right] \right) \\
={}& -\frac{1}{2}\left(\sum_i\lambda_i \left(y_i + \frac{K_i}{\lambda_i}\right)^2 \right) + \frac{1}{2}\sum_i\frac{K_i^2}{\lambda_i}\\
={}& -\frac{1}{2}\left(\sum_i\lambda_i \left(y_i + \frac{K_i}{\lambda_i}\right)^2 \right) + \frac{1}{2}\sum_i\frac{K_i^2}{\lambda_i}\\
\end{align}$$

Now, we plug this expression back into the integral. This gives us 

$$\begin{align}
Z[\mathbf{J}] = \int \exp\left(-\frac{1}{2}\left(\sum_i\lambda_i \left(y_i - \frac{K_i}{\lambda_i}\right)^2 \right) + \frac{1}{2}\sum_i\frac{K_i^2}{\lambda_i} \right) \d^d\x 
\end{align}$$

we need to change the differential to \(\d^d\y\), which is easy because the Jacobian is \(\det(U) = 1\). Thus \(\d^d\x = \d^d\y\). After changing the differential, we can also shift the integration variable freely since the integral bounds are \(-\infty\) to \(\infty\) in each component of \(\y\).

$$\begin{align}
Z[\mathbf{J}] ={}& \exp\left(\frac{1}{2}\sum_i\frac{K_i^2}{\lambda_i} \right) \int \exp\left(-\frac{1}{2}\sum_i\lambda_i \left(y_i - \frac{K_i}{\lambda_i}\right)^2 \right) \d^d\y \\
={}& \exp\left(\frac{1}{2}\sum_i K_i \frac{1}{\lambda_i} K_i \right) \int \exp\left(-\frac{1}{2}\sum_i\lambda_i y_i^2 \right) \d^d\y \\
={}& \exp\left(\frac{1}{2} \mathbf{K}^T\Lambda^{-1}\mathbf{K}  \right) \prod_{i=1}^d \int \exp\left(-\frac{1}{2}\lambda_i y_i^2 \right) \\
={}& \exp\left(\frac{1}{2}\mathbf{J}^T U^T \Lambda^{-1} U \mathbf{J}  \right) \prod_{i=1}^d \sqrt{\frac{2\pi}{\lambda_i}} \\
={}& \exp\left(\frac{1}{2} \mathbf{J}^T A^{-1} \mathbf{J} \right) \sqrt{\frac{(2\pi)^d}{\det(A)}} \\
={}& \exp\left(\frac{1}{2} \mathbf{J}^T A^{-1} \mathbf{J} \right) Z(0) \\
\end{align}$$

where we used that the product of all the eigenvalues is the determinant. Now that we have an explicit formula for \(Z[\mathbf{J}]\), it is easy just to take partial derivatives and thereby find the correlation functions. 

</li>
<li> We find that 

$$\begin{equation}
\langle x_{i_1}\cdots x_{i_n} \rangle = \frac{1}{Z(0)}\int \left(\frac{\partial}{\partial J_{i_1}} \cdots \frac{\partial}{\partial J_{i_n}} \right) e^{-\x^TA\x - \mathbf{J}^T \x} \d x_1 \cdots \d x_d\bigg|_{\mathbf{J} = 0} 
\end{equation}$$

This can be rewritten by pulling the derivatives out of the integral to find

$$\begin{equation}
\langle x_{i_1}\cdots x_{i_n} \rangle = \frac{1}{Z(0)} \left(\frac{\partial}{\partial J_{i_1}} \cdots \frac{\partial}{\partial J_{i_n}} \right)\int e^{-\x^TA\x - \mathbf{J}^T \x} \d x_1 \cdots \d x_d \bigg|_{\mathbf{J} = 0} 
\end{equation}$$

We recognize the integral as \(Z(\mathbf{J})\), and we get 

$$\begin{equation}
\langle x_{i_1}\cdots x_{i_n} \rangle = \frac{(-1)^n}{Z(0)} \left(\frac{\partial}{\partial J_{i_1}} \cdots \frac{\partial}{\partial J_{i_n}} \right)Z(\mathbf{J})\bigg|_{\mathbf{J} = 0} 
\end{equation}$$

</li>
<li> We simply use the definition

$$\begin{align}
\langle x_i x_j \rangle_0 ={}& \frac{1}{Z(0)}\frac{\partial}{\partial J_i} \frac{\partial}{\partial J_j} Z(\mathbf{J}) \bigg|_{\mathbf{J} = 0} \\
={}& \frac{\partial}{\partial J_i} \frac{\partial}{\partial J_j} \exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)  \frac{\partial}{\partial J_j}\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m \right]\bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)  \left( \frac{1}{2}\sum_{mn} \delta_{jn}(A^{-1})_{nm}J_m + \frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}\delta_{jm} \right) \right]\bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)  \left( \frac{1}{2}\sum_{m} (A^{-1})_{jm}J_m + \frac{1}{2}\sum_{n} J_n(A^{-1})_{nj} \right) \right]\bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{m} (A^{-1})_{jm}J_m \right]\bigg|_{\mathbf{J}=0} \\
={}& \left[\frac{\partial}{\partial J_i}\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{m} (A^{-1})_{jm}J_m \right. \\
&\left. + \exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \frac{\partial}{\partial J_i}\sum_{m} (A^{-1})_{jm}J_m \right]\bigg|_{\mathbf{J}=0} \\
={}& \left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)\frac{\partial}{\partial J_i}\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{k} (A^{-1})_{jk}J_k \right. \\
&\left. + \exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{m} (A^{-1})_{jm}\delta_{im} \right]\bigg|_{\mathbf{J}=0}
\end{align}$$

The first term goes to zero, but the second term simplifies to \((A^{-1})_{ji} = (A^{-1})_{ij}\). Thus

$$\begin{equation}
\langle x_i x_j \rangle_0 = (A^{-1})_{ij}.
\end{equation}$$

</li></ol>

</div>


\subsection{Wick's Theorem}

<div class="example">
<b>Example:</b>
Here, we will discuss Wick's theorem. We define the noninteracting partition function \(Z(0)\) to be

$$\begin{equation}
Z(0) = \int \exp\left(-\frac{1}{2}\sum_{i,j=1}^d x_i(G^{-1})_{ij}x_j\right) \d x_1\cdots \d x_d.
\end{equation}$$

The generating functional then is 

\(\)Z(\mathbf{J}) = Z(0)\exp\left(\frac{1}{2}\sum_{ij}J_i G_{ij} J_j\right)\(\)

Note the following:
<ul>
<li> We use the notation \(\exp(x) = e^x\) because the argument of the exponential is pretty big and the text would become too small if we used the \(e^x\) notation. 
</li>
<li> We have replaced  \(A\) from problem 1.2 with \(A = G^{-1}\). This is done with that the \(\langle x_i x_j \rangle_0 = G_{ij}\) instead of \((A^{-1})_{ij}\); it is simply nice to remove the annoying matrix inverse symbol. 
</li>
<li> We are no longer writing the bounds of the integrals, but assume we integrate from \(-\infty\) to \(\infty\) for each \(x_i\).
</li>
<li> We are also switching notation for the argument of the exponential:

$$\begin{equation}
\x^TG^{-1}\x = \sum_{i,j=1}^d x_i (G^{-1})_{ij} x_j
\end{equation}$$
</li></ul>

<ol type="a">
<li> Compute the correlation function \(\langle x_i x_j x_k x_\ell\rangle_0\) by using the generating functional. Warning: this is somewhat tedious. I recommend using the Einstein summation convention to make your life easier.

</li>
<li> What is the result if there is a correlation function of an odd number of variables? For example, \(\langle x_1 x_2 x_3 \rangle_0\) or \(\langle x_1^2 x_2 \rangle_0\)?
</li>
<li> The result of the previous sections is indicative of a broader pattern. In fact, this broader pattern is that

$$\begin{equation}
\langle x_{i_1} x_{i_2} \cdots x_{i_{2n}} \rangle_0 = \sum_{\pi} \langle x_{i_{\pi(1)}} x_{i_{\pi(2)}}\rangle_0 \cdots \langle x_{i_{\pi(2n-1)}} x_{i_{\pi(2n)}}\rangle_0 
\end{equation}$$

where \(\pi\) is a permutation running over all possible pairs of items of the original correlator (this explanation isn't particularly precise; compare the result of part (a) with this ``explanation", which should make it more clear). This result is known as <i>Wick's theorem</i>. Thus, the correlator of a large number of variables can be written as the sum over permutations of products of 2-point correlators. These 2-point correlators are related to the matrix elements of \(G\), i.e. \(\langle x_i x_j \rangle_0 = G_{ij}\). 

How many terms are in the sum in the expansion of \(\langle x_{i_1} x_{i_2} \cdots x_{i_{2n}} \rangle_0\)? Does your formula agree with the case \(n=2\) computed in part (a)?

</li>
<li> Using Wick's theorem, compute the following correlators in terms of matrix elements of \(G\):

<ol>[(i)]
<li> \(\langle x_i x_j x_k x_\ell \rangle_0\). The result should be the same as part (a).
</li>
<li> \(\langle x_i x_j x_k^2 \rangle_0\) 
</li>
<li> \(\langle x_i x_j x_k^4 \rangle_0\)
</li></ol>

</li>
<li> By drawing a dot for a particular \(x_i\), (draw a dot and label it \(i\)) and drawing a line between two dots \(x_i\) and \(x_j\) if they appear in a correlator \(\langle x_i x_j \rangle\), draw a sum of diagrams for each of the correlators in part (d). Here are some examples of some expressions and their corresponding diagrams:


\begin{center}
<figure class="center"><p><img src="figures/feynman_diagram_oneline.pdf" alt="Function" class="center" style="width:53.213px;height:18.404px;"> </p></figure>
\captionof{figure}{\(\langle x_i x_j \rangle_0\)}
\end{center}

\begin{center}
<figure class="center"><p><img src="figures/feynman_diagram_figure8.pdf" alt="Function" class="center" style="width:87.931px;height:54.525px;"> </p></figure>
\captionof{figure}{\(\langle x_i x_i \rangle_0 \langle x_i x_i \rangle_0\)}
\end{center}

\begin{center}
<figure class="center"><p><img src="figures/feynman_diagram_oline.pdf" alt="Function" class="center" style="width:96.147px;height:60.044px;"> </p></figure>
\captionof{figure}{\(\langle x_i x_j \rangle_0 \langle x_j x_j \rangle_0 \langle x_j x_k \rangle_0\)}
\end{center}

\begin{center}
<figure class="center"><p><img src="figures/feynman_diagram_discon_figure8_oline.pdf" alt="Function" class="center" style="width:95.733px;height:113.748px;"> </p></figure>
\captionof{figure}{\(\langle x_i x_j \rangle_0 \langle x_k x_k \rangle_0 \langle x_j x_k \rangle_0\langle x_\ell^2\rangle_0^2\)}
\end{center}



</li></ol>


<b>Solution:</b>
<ol type="a">
<li> In this, we will use the Einstein summation notation. We find 

$$\begin{equation}
\frac{\partial}{\partial J_\ell} e^{\frac{1}{2}J_m G_{mn}J_n} = e^{\frac{1}{2}J_m G_{mn}J_n} G_{\ell a}J_a
\end{equation}$$

The second derivative is 

$$\begin{equation}
\frac{\partial}{\partial J_k} \frac{\partial}{\partial J_\ell} e^{\frac{1}{2}J_m G_{mn}J_n} = e^{\frac{1}{2}J_mG_{mn}J_n}\left(G_{kb}J_b G_{\ell a} J_a + G_{k\ell}\right) 
\end{equation}$$

The third derivative is 

$$\begin{equation}
\frac{\partial}{\partial J_j} \frac{\partial}{\partial J_k} \frac{\partial}{\partial J_\ell} e^{\frac{1}{2}J_m G_{mn}J_n} =  e^{\frac{1}{2}J_mG_{mn}J_n} \left(G_{jc}J_c G_{kb}J_b G_{\ell a} J_a + G_{jc}J_c G_{k\ell} + G_{kj} G_{\ell a} J_a + G_{kb}J_b G_{\ell j}\right)
\end{equation}$$

We throw out the term cubic in \(J\) because it will not survive when setting \(J = 0\), even after differentiation. Thus, removing the term gives

$$\begin{equation}
\frac{\partial}{\partial J_j} \frac{\partial}{\partial J_k} \frac{\partial}{\partial J_\ell} e^{\frac{1}{2}J_m G_{mn}J_n} =  e^{\frac{1}{2}J_mG_{mn}J_n} \left(G_{jc}J_c G_{k\ell} + G_{kj} G_{\ell a} J_a + G_{kb}J_b G_{\ell j}\right)
\end{equation}$$

The fourth derivative gives us 

$$\begin{align}
\frac{\partial}{\partial J_i} \frac{\partial}{\partial J_j} \frac{\partial}{\partial J_k} \frac{\partial}{\partial J_\ell} e^{\frac{1}{2}J_m G_{mn}J_n} ={}& e^{\frac{1}{2}J_mG_{mn}J_n} G_{id}J_d \left(G_{jc}J_c G_{k\ell} + G_{kj} G_{\ell a} J_a + G_{kb}J_b G_{\ell j}\right) \\
&+ e^{\frac{1}{2}J_mG_{mn}J_n} \left(G_{ji} G_{k\ell} + G_{kj} G_{\ell i} + G_{ki} G_{\ell j}\right)
\end{align}$$

Now evaluating at zero removes the first line, and we have 

$$\begin{align}
\frac{\partial}{\partial J_i} \frac{\partial}{\partial J_j} \frac{\partial}{\partial J_k} \frac{\partial}{\partial J_\ell} e^{\frac{1}{2}J_m G_{mn}J_n}\bigg|_{\mathbf{J}=0} ={}&  \left(G_{ji} G_{k\ell} + G_{kj} G_{\ell i} + G_{ki} G_{\ell j}\right)
\end{align}$$

This can be rewritten as 

$$\begin{align}
\langle x_i x_j x_k x_\ell \rangle_0 ={}& \langle x_i x_j \rangle_0 \langle x_k x_\ell \rangle_0 + \langle x_j x_k \rangle_0 \langle x_i x_\ell \rangle_0 + \langle x_i x_k \rangle_0 \langle x_j x_\ell \rangle_0
\end{align}$$

\iffalse$$\begin{align}
\langle x_i x_j x_k x_\ell \rangle_0 ={}& \frac{1}{Z(0)} \frac{\partial}{\partial J_i} \frac{\partial}{\partial J_j} \frac{\partial}{\partial x_k} \frac{\partial}{\partial x_\ell} Z(\mathbf{J}) \bigg|_0 \\
={}& \frac{\partial}{\partial J_i} \frac{\partial}{\partial J_j} \exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)  \frac{\partial}{\partial J_j}\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m \right]\bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)  \left( \frac{1}{2}\sum_{mn} \delta_{jn}(A^{-1})_{nm}J_m + \frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}\delta_{jm} \right) \right]\bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)  \left( \frac{1}{2}\sum_{m} (A^{-1})_{jm}J_m + \frac{1}{2}\sum_{n} J_n(A^{-1})_{nj} \right) \right]\bigg|_{\mathbf{J}=0} \\
={}& \frac{\partial}{\partial J_i}\left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{m} (A^{-1})_{jm}J_m \right]\bigg|_{\mathbf{J}=0} \\
={}& \left[\frac{\partial}{\partial J_i}\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{m} (A^{-1})_{jm}J_m \right. \\
&\left. + \exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \frac{\partial}{\partial J_i}\sum_{m} (A^{-1})_{jm}J_m \right]\bigg|_{\mathbf{J}=0} \\
={}& \left[\exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right)\frac{\partial}{\partial J_i}\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{k} (A^{-1})_{jk}J_k \right. \\
&\left. + \exp\left(\frac{1}{2}\sum_{mn} J_n(A^{-1})_{nm}J_m\right) \sum_{m} (A^{-1})_{jm}\delta_{im} \right]\bigg|_{\mathbf{J}=0}
\end{align}$$
\fi

</li>
<li> The result is 0 if there are an odd number of variables.

</li>
<li> There are \((2n-1)(2n-3)\cdots 1 = (2n-1)!!\) many terms.

</li>
<li> 

<ol>[(i)]
<li> \(\langle x_i x_j x_k x_\ell \rangle_0 = \langle x_i x_j \rangle_0 \langle x_k x_\ell \rangle_0 + \langle x_i x_k \rangle_0 \langle x_j x_\ell \rangle_0 + \langle x_i x_\ell \rangle_0 \langle x_j x_k \rangle_0\)
</li>
<li> \(\langle x_i x_j x_k^2 \rangle_0 = \langle x_i x_j \rangle_0 \langle x_k^2 \rangle_0 + 2\langle x_i x_k \rangle_0 \langle x_j x_k \rangle_0 \) 
</li>
<li> \(\langle x_i x_j x_k^4 \rangle_0 = 3\langle x_i x_j \rangle_0 \langle x_k^2 \rangle_0 \langle x_k^2 \rangle_0 + 12 \langle x_i x_k \rangle_0 \langle x_j x_k \rangle_0 \langle x_k^2 \rangle_0\)
</li></ol>

</li>
<li> Insert pictures here!

</li></ol>


</div>

<div class="example">
<b>Example:</b>
Let us now explore perturbation theory. For this problem, we define the <i>partition function</i> \(Z(u)\):

$$\begin{equation}
Z(u) = \int \exp\left(-\frac{1}{2}\sum_{i,j=1}^d x_i(G^{-1})_{ij}x_j - \frac{u}{24}\sum_{i=1}^d x_i^4\right) \d^d\x.
\end{equation}$$

We have defined the notation \(\d^d\x = \d x_1 \cdots \d x_d\). It also compresses notation to define

\(\)S_0 = \frac{1}{2}\sum_{i,j=1}^d x_i(G^{-1})_{ij}x_j ,\quad S_{\text{int}} =  \frac{u}{24}\sum_{i=1}^d x_i^4\(\)

so that the partition function becomes

$$\begin{equation}
Z(u) = \int e^{-S_0 - S_{\text{int}}} \d^d\x.
\end{equation}$$

We also define the <i>interacting expectation value</i> (here, \(A(x_1,\dots,x_d) = A(\x)\) is some function of all the \(\x=(x_1,\dots,x_d)\) variables, and it is not related to the \(A\) we used in problem 1.2) by the following expression:

$$\begin{equation}
\langle A(\x) \rangle = \frac{1}{Z(u)}\int A(\x) e^{-S_0-S_{\text{int}}} \d^d\x.
\end{equation}$$

Note that \(\langle A(\x)\rangle\) is also called the <i>expectation value of </i>\(A(\x)\). We also define the <i>noninteracting expectation value</i>

$$\begin{equation}
\langle A(\x) \rangle_0 = \frac{1}{Z(0)}\int A(\x)  e^{-S_0}\d^d\x.
\end{equation}$$

Note that here \(Z(0)\) refers to \(Z(u=0)\); the argument of the partition function no longer refers to \(\mathbf{J}\). The only purpose of introducing \(\mathbf{J}\) earlier was to learn about Wick's theorem.

<ol type="a">
<li> By considering the quadratic and quartic terms of the partition function separately, i.e.

$$\begin{align}
Z(u) ={}& \int  e^{-S_0} e^{-S_{\text{int}}} \d^d\x
\end{align}$$

Write the partition function as a noninteracting correlation function. Hint: Multiply by \(Z(0)/Z(0)\).

</li>
<li> Write an interacting correlation function \(\langle A(\x) \rangle\) in terms of noninteracting correlation functions. 

</li>
<li> By Taylor expanding the quartic part of the partition function, i.e. 

$$\begin{align}
Z(u) ={}& \int e^{-S_0} \sum_{n=0}^\infty \frac{1}{n!} (-S_{\text{int}})^n \d^d\x,
\end{align}$$

Compute the following quantity up until order \(u^2\) (truncate the Taylor series at second order): 

$$\begin{equation}
\frac{Z(u)}{Z(0)}.
\end{equation}$$

Provide your answer in terms of the matrix elements of \(G\) and make sure to be careful about combinatorial factors! (the same expression may appear multiple times, and you have to account for relabelling of indices since the sum in the interaction is a dummy index)

</li>
<li> Using the same rules for drawing diagrams as in problem 1.3(e), draw diagrams for each term found in the previous part.

</li>
<li> By setting the answer of part (c) to be 

\(\)\frac{Z(u)}{Z(0)} = 1+\epsilon,\(\)

Compute the following quantity up to order \(u^2\):

\(\)\log\left(\frac{Z(u)}{Z(0)}\right) = \log(1+\epsilon) = \epsilon - \frac{\epsilon^2}{2} + \cdots\(\)

</li>
<li> Draw diagrams for the series encountered in the previous part.
</li></ol>

<b>Solution:</b>
<ol type="a">
<li> We can simply write 

\(\)Z(u) = \int e^{-S_0} e^{-S_{\text{int}}} \d\x = \frac{Z(0)}{Z(0)}\int e^{-S_0} e^{-S_{\text{int}}}\d\x = Z_0\langle e^{-S_{\text{int}}}\rangle_0\(\)

</li>
<li> Similarly, we find 

\(\)\langle A(\x) \rangle = \frac{\langle A(\x) e^{-S_{\text{int}}}\rangle_0}{\langle e^{-S_{\text{int}}}\rangle_0}\(\)

</li>
<li> The quartic part can be Taylor expanded to second order as 

\(\) \sum_{n=0}^\infty \frac{1}{n!} (-S_{\text{int}})^n = 1 - S_{\text{int}} + \frac{1}{2}S_{\text{int}}^2 + \cdots\(\)

Now, computing 

$$\begin{align}
\frac{Z(u)}{Z(0)} = \langle 1 - S_{\text{int}} + \frac{1}{2}S_{\text{int}}^2 \rangle_0
\end{align}$$

The zeroth order just gives us 1. The first order term gives 

$$\begin{align}
\langle S_{\text{int}} \rangle_0 ={}& \frac{u}{24}\sum_{i=1}^d \langle x_i^4 \rangle_0 \\
={}& \frac{u}{24}\sum_{i=1}^d \left(3\langle x_i^2 \rangle_0 \langle x_i^2 \rangle_0 \right) \\
={}& \frac{u}{8}\sum_{i=1}^d \langle x_i^2 \rangle_0 \langle x_i^2 \rangle_0 \\
={}& \frac{u}{8}\sum_i G_{ii}^2
\end{align}$$

The only diagram has a combinatorial factor of 3. This is because \(\binom{4}{2} = 6\), but this leads to a double counting so we divide by 2. The second order term gives 

$$\begin{align}
\langle S_{\text{int}}^2 \rangle_0 ={}& \frac{u^2}{24^2}\sum_{i,j} \langle x_i^4 x_j^4 \rangle_0 \\
={}& \frac{u}{24^2}\left[9 (\langle x_i^2 \rangle_0)^4+ 72 \langle x_i^2 \rangle_0\langle x_j^2 \rangle_0 ( \langle x_i x_j \rangle_0)^2 + 24 (\langle x_i x_j \rangle_0)^4\right]
\end{align}$$

The first diagram has a combinatorial factor of 9 because \(9=3^2\) and we computed the 3 in the first order part. The second diagram comes from \(\langle x_j^4 x_i^4 \rangle_0\) and we need to first do \(\binom{4}{2}^2 = 36\) to decide which lines attach to the other vertex, and we need to make this decision for each vertex. Then, there are two ways to join up the two vertices, so we get 72 total. For the third diagram, we simply have \(4! = 24\) because there are 4 possible partners for the first line, 3 possible partners for the second line, and so on. 

The total result is therefore 

\(\)\frac{Z(u)}{Z(0)} = 1 - \frac{u}{8}\sum G_{ii}^2 + \frac{1}{2}\left(\frac{u}{8}\sum_i G^2_{ii}\right)^2 + \frac{u^2}{16}\sum_{ij} G_{ii}G_{jj}G_{ij}^2 + \frac{u^2}{48}\sum_{ij} G_{ij}^4\(\)

</li>
<li> The first order expression corresponds to 

\(\)\langle S_{\text{int}}\rangle_0 = 
<figure class="center"><p><img src="figures/feynman_diagram_1st_corr.pdf" alt="Function" class="center" style="width:87.931px;height:54.525px;"> </p></figure>\(\)

The second order expression corresponds to 

\(\)\langle S_{\text{int}}^2 \rangle_0 = 
<figure class="center"><p><img src="figures/feynman_diagram_2nd_corr1.pdf" alt="Function" class="center" style="width:87.931px;height:97.045px;"> </p></figure>
 +  
<figure class="center"><p><img src="figures/feynman_diagram_2nd_corr2.pdf" alt="Function" class="center" style="width:130.451px;height:54.525px;"> </p></figure> 
+
<figure class="center"><p><img src="figures/feynman_diagram_2nd_corr3.pdf" alt="Function" class="center" style="width:73.542px;height:54.395px;"> </p></figure> \(\)


</li>
<li> Setting 

\(\)\epsilon = - \frac{u}{8}\sum G_{ii}^2 + \frac{1}{2}\left(\frac{1}{8}\sum_i G_{ii}\right)^2 + \frac{u^2}{16}\sum_{ij} G_{ii}G_{jj}G_{ij}^2 + \frac{u^2}{48}\sum_{ij} G_{ij}^4\(\)

We compute 

\(\)\log(1+\epsilon) = \epsilon - \frac{\epsilon^2}{2}\(\)

Note that we can throw out all the terms of order \(u^3\) and higher. Thus we find 

$$\begin{align}
\log(1+\epsilon) ={}& - \frac{u}{8}\sum G_{ii}^2 + \frac{1}{2}\left(\frac{u}{8}\sum_i G_{ii}\right)^2 + \frac{u^2}{16}\sum_{ij} G_{ii}G_{jj}G_{ij}^2 + \frac{u^2}{24}\sum_{ij} G_{ij}^4 - \frac{1}{2}\left(- \frac{u}{8}\sum G_{ii}^2\right)^2 \\
={}& - \frac{u}{8}\sum G_{ii}^2 + \frac{u^2}{16}\sum_{ij} G_{ii}G_{jj}G_{ij}^2 + \frac{u^2}{48}\sum_{ij} G_{ij}^4
\end{align}$$

</li>
<li>  The first order expression corresponds to 

\(\)\langle S_{\text{int}}\rangle_0 =
<figure class="center"><p><img src="figures/feynman_diagram_1st_corr1.pdf" alt="Function" class="center" style="width:87.931px;height:54.525px;"> </p></figure>\(\)

The second order expression corresponds to 

\(\)\langle S_{\text{int}}^2 \rangle_0 = 
<figure class="center"><p><img src="figures/feynman_diagram_2nd_corr4.pdf" alt="Function" class="center" style="width:130.451px;height:54.525px;"> </p></figure>
+
<figure class="center"><p><img src="figures/feynman_diagram_2nd_corr5.pdf" alt="Function" class="center" style="width:73.542px;height:54.395px;"> </p></figure> \(\)

</li></ol>

</div>

<div class="example">
<b>Example:</b>
Finally, we discuss the Green function. We define the following quantity 

$$\begin{equation}
C_{ij} = \langle x_i x_j \rangle = \frac{1}{Z(u)}\int x_i x_j e^{-S_0-S_{\text{int}}} \d^d\x = \frac{\langle x_i x_j e^{-S_{\text{int}}}\rangle_0}{\langle e^{-S_{\text{int}}}\rangle_0}
\end{equation}$$

to be the <i>interacting Green function</i>. The quantity \(G_{ij} = \langle x_i x_j \rangle_0\) is called the <i>noninteracting Green function</i>. It is not possible to compute the Green function \(C_{ij}\) exactly in general (the integrals are too difficult!). It can only be computed order by order in perturbation theory. The name ``Green function" is simple a name at this point; it should not be obvious why it is called this. Note: This section is crucial for the Ginzburg-Landau theory of superconductivity, as well as Fermi liquid theory.

    
<ol type="a">
<li> Compute the numerator of the Green function 

$$\begin{equation}
\langle x_i x_j e^{-S_{\text{int}}}\rangle_0
\end{equation}$$

up to second order in \(u\). 

</li>
<li> Draw diagrams according to the familiar rules for the quantity computed in part (a).

</li>
<li> By using the result of 1.4(c), as well as the Taylor expansion

$$\begin{equation}
\frac{1}{1-x} = 1 + x + x^2 + \cdots
\end{equation}$$

compute the interacting Green function \(\langle x_i x_j \rangle\) up to second order in \(u\). Compare the result to the result of part (a).

</li>
<li> Draw diagrams according to the familiar rules for the Green function computed in part (c). Compare the result to the result of part (b). Which diagrams have cancelled out? 

</li></ol>

<b>Solution:</b>
<ol type="a">
<li> Taylor expanding gives us

$$\begin{align}
\langle x_i x_j e^{-S_{\text{int}}}\rangle_0 = \langle x_i x_j \rangle_0 -  \langle x_i x_j S_{\text{int}}\rangle_0 + \frac{1}{2} \langle x_i x_j S_{\text{int}}^2\rangle_0 + \cdots
\end{align}$$

The zeroth order term is just \(\langle x_i x_j \rangle_0 = G_{ij}\). The first order term contributes 

$$\begin{align}
\langle x_i x_j S_{\text{int}}\rangle_0 ={}& \frac{u}{24}\sum_k \langle x_i x_j x_k^4 \rangle_0 \\
={}& \frac{u}{24}\sum_k \left(3G_{ij}G_{kk}^2 + 12 G_{ik}G_{kk}G_{jk}\right) \\
={}& \frac{u}{8}G_{ij}\sum_k G_{kk}^2 + \frac{u}{2}\sum_k G_{ik}G_{kk}G_{jk} 
\end{align}$$

The combinatorial factor in the first diagram is 3 because of the same reasons as in the partition function expansion. The second diagram is 12 because there are \(\binom{4}{2} = 6\) ways to pick the two lines which will connect to the external points \(i\) and \(j\). Then, there are 2 ways to join up \(i\) and \(j\), so we get \(6\times 2 = 12\).

The second order term contributes 

$$\begin{align}
\langle x_i x_j S_{\text{int}}^2\rangle_0 ={}& \frac{u^2}{24^2}\sum_{k\ell}\langle x_i x_j x_k^4 x_\ell^4 \rangle_0 \\
={}&\frac{u^2}{24^2}\left( 9\langle x_i x_j \rangle_0 \langle x_k^2\rangle_0^2\langle x_\ell^2\rangle_0^2 + 72 \langle x_i x_j \rangle_0 \langle x_k^2\rangle_0 \langle x_\ell^2\rangle_0 \langle x_k x_\ell\rangle_0^2 + 24\langle x_i x_j \rangle_0 \langle x_k x_\ell\rangle_0^4 \right. \\
&+ 72 \langle x_i x_k \rangle_0 \langle x_j x_k \rangle_0 \langle x_k^2\rangle_0 \langle x_\ell^2\rangle_0^2 + 192 \langle x_i x_k \rangle_0 \langle x_j x_\ell \rangle_0 \langle x_k x_\ell \rangle_0^3 \\
&+ \left. 288\langle x_i x_k \rangle_0 \langle x_k x_\ell \rangle_0 \langle x_j x_\ell \rangle_0 \langle x_k^2 \rangle_0 \langle x_\ell^2\rangle_0 + 288 \langle x_i x_k \rangle_0 \langle x_k x_j \rangle_0 \langle x_k x_\ell\rangle_0^2 \langle x_\ell^2\rangle_0 \right)
\end{align}$$

We can comment on where these combinatorial factors come from. For the first line, this is just known stuff from the partition function. 

For the second line, in the first term we have the 12 from the first order contribution times the 3 from the number of ways to make the partition function diagram, times 2 because you could pick either vertex to be connect to the external lines. 

For the second diagram on the second line, you have 4 choices of which line should connect to the external point, and you make this decision twice, and you could also swap vertices so we get \(2\times 4^2 = 32\). Then, there are 6 ways to connect up the three internal lines, so we get \(32\times 6 = 192\). 

For the third line, we have to pick 2 lines of each vertex to participate in the long line, so we get \(\binom{4}{2}^2 = 36\), and since we can swap vertices another factor of 2. Then, we need to choose which of the remaining two lines on each vertex should connect to the external lines, which gives two more factors of 2. Thus, we have \(36\times 2\times 4 = 288\). 

For the second of the two diagrams on the third line, we have to pick 2 of the lines on the \(k\) vertex to connect to the \(\ell\) vertex, and a similar choice for the \(\ell\) vertex connecting to the \(k\) vertex, which gives \(\binom{4}{2}^2 = 36\). There are 2 ways to do this connection. Then, we have to pick which of the remaining legs of \(k\) connects to \(i\), so we get another factor of 2. Lastly, we can swap \(k\) and \(\ell\) so we get one more factor of 2. This gives again 288.

The result of all this is  

$$\begin{align}
\langle x_i x_j S_{\text{int}}^2\rangle_0 ={}&\frac{u^2}{24^2}\sum_{k\ell} \left( 9G_{ij} G_{kk}^2 G_{\ell\ell}^2 + 72G_{ij}G_{kk} G_{\ell\ell} G_{k\ell}^2 + 24G_{ij}G_{k\ell}^4 + 72 G_{ik}G_{jk}G_{kk}G_{\ell\ell}^2\right. \\
&+\left. 192 G_{ik}G_{j\ell}G_{k\ell}^3 + 288G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + 288 G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} \right) \\
={}&u^2G_{ij}\left(\frac{1}{64} \sum_{k\ell}G_{kk}^2 G_{\ell\ell}^2 + \frac{1}{8}\sum_{k\ell}G_{kk} G_{\ell\ell} G_{k\ell}^2 + \frac{1}{24}\sum_{k\ell}G_{k\ell}^4\right) + \frac{u^2}{8}\sum_{k\ell}G_{ik}G_{jk}G_{kk}G_{\ell\ell}^2 \\
&+ \frac{u^2}{3} \sum_{k\ell}G_{ik}G_{j\ell}G_{k\ell}^3 + \frac{u^2}{2}\sum_{k\ell} G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + \frac{u^2}{2}\sum_{k\ell}G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} 
\end{align}$$

In total, we therefore have 

$$\begin{align}
\langle x_i x_j  e^{-S_{\text{int}}} \rangle_0 ={}& G_{ij} - \frac{u}{8}G_{ij}\sum_k G_{kk}^2 - \frac{u}{2}\sum_k G_{ik}G_{kk}G_{jk} + \frac{u^2}{128}G_{ij}\left(\sum_k G_{kk}^2\right)^2 \\
&+ \frac{u^2}{16}G_{ij}\sum_{k\ell}G_{kk}G_{\ell\ell}G_{k\ell}^2 + \frac{u^2}{48}G_{ij}\sum_{k\ell}G_{k\ell}^4 + \frac{u^2}{16}\sum_{k\ell}G_{ik}G_{jk}G_{kk}G_{\ell\ell}^2 \\
&+ \frac{u^2}{6} \sum_{k\ell}G_{ik}G_{j\ell}G_{k\ell}^3 + \frac{u^2}{4}\sum_{k\ell} G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + \frac{u^2}{4}\sum_{k\ell}G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} 
\end{align}$$

</li>
<li> We won't draw all the diagrams in the first line because some of them are just a bare line times a diagram from the partition function. These are the first, second, and fourth terms on line 1. The third term however has the diagram 

<figure class="center"><p><img src="figures/feynman_diagram_ijk.pdf" alt="Function" class="center" style="width:95.733px;height:60.044px;"> </p></figure>



For the second line, we have one disconnected diagram

<figure class="center"><p><img src="figures/feynman_diagram_ijk_figure8.pdf" alt="Function" class="center" style="width:95.733px;height:113.748px;"> </p></figure>

Then we have the diagram 

<figure class="center"><p><img src="figures/feynman_diagram_ijkl_oyster.pdf" alt="Function" class="center" style="width:138.253px;height:54.395px;"> </p></figure>

For the third line, we have 

<figure class="center"><p><img src="figures/feynman_diagram_ijkl_2loop.pdf" alt="Function" class="center" style="width:138.253px;height:59.628px;"> </p></figure>

and finally we have 

<figure class="center"><p><img src="figures/feynman_diagram_ijk_looplloop.pdf" alt="Function" class="center" style="width:95.733px;height:102.564px;"> </p></figure>


</li>
<li> The first thing we do is to compute 

$$\begin{equation}
\frac{1}{\langle e^{-S_{\text{int}}}\rangle} = \frac{Z(0)}{Z(u)}
\end{equation}$$

Defining

$$\begin{equation}
x = \frac{u}{8}\sum_i G_{ii}^2 - \frac{1}{2}\left(\frac{u}{8}\sum_i G_{ii}^2\right)^2 - \frac{u^2}{16}\sum_{ij}G_{ii}G_{jj}G_{ij}^2 - \frac{u^2}{48}\sum_{ij}G_{ij}^4
\end{equation}$$

then we can compute 

$$\begin{align}
\frac{1}{\langle e^{-S_{\text{int}}}\rangle_0} ={}& \frac{1}{1-x} \\
={}& 1 + x + x^2\\
={}& 1 + \frac{u}{8}\sum_i G_{ii}^2 - \frac{1}{2}\left(\frac{u}{8}\sum_i G_{ii}^2\right)^2 - \frac{u^2}{16}\sum_{ij}G_{ii}G_{jj}G_{ij}^2 - \frac{u^2}{48}\sum_{ij}G_{ij}^4 + \left(\frac{u}{8}\sum_iG_{ii}^2\right)^2 \\
={}& 1 + \frac{u}{8}\sum_i G_{ii}^2 + \frac{1}{2}\left(\frac{u}{8}\sum_i G_{ii}^2\right)^2 - \frac{u^2}{16}\sum_{ij}G_{ii}G_{jj}G_{ij}^2 - \frac{u^2}{48}\sum_{ij}G_{ij}^4 
\end{align}$$

Now, we multiply this with the numerator of the Green function, which we recall was 
$$\begin{align}
\langle x_i x_j  e^{-S_{\text{int}}} \rangle_0 ={}& G_{ij} - \frac{u}{8}G_{ij}\sum_k G_{kk}^2 - \frac{u}{2}\sum_k G_{ik}G_{kk}G_{jk} + \frac{u^2}{128}G_{ij}\left(\sum_k G_{kk}^2\right)^2 \\
&+ \frac{u^2}{16}G_{ij}\sum_{k\ell}G_{kk}G_{\ell\ell}G_{k\ell}^2 + \frac{u^2}{48}G_{ij}\sum_{k\ell}G_{k\ell}^4 + \frac{u^2}{16}\sum_{k\ell}G_{ik}G_{jk}G_{kk}G_{\ell}^2 \\
&+ \frac{u^2}{6} \sum_{k\ell}G_{ik}G_{j\ell}G_{k\ell}^3 + \frac{u^2}{4}\sum_{k\ell} G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + \frac{u^2}{4}\sum_{k\ell}G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} 
\end{align}$$

Multiplying together now, we find 

$$\begin{align}
\langle x_i x_j \rangle ={}& \frac{\langle x_i x_j e^{-S_{\text{int}}}\rangle}{\langle e^{-S_{\text{int}}} \rangle} \\
={}& G_{ij}\left(1 + \frac{u}{8}\sum_i G_{ii}^2 + \frac{1}{2}\left(\frac{u}{8}\sum_i G_{ii}^2\right)^2 - \frac{u^2}{16}\sum_{ij}G_{ii}G_{jj}G_{ij}^2 - \frac{u^2}{48}\sum_{ij}G_{ij}^4 \right) \\
&+ \left(1+\frac{u}{8}\sum_k G_{kk}^2\right)\left(-\frac{u}{8}G_{ij}\sum_k G_{kk}^2 - \frac{u}{2}\sum_k G_{ik}G_{kk}G_{jk}\right) + \frac{u^2}{128}G_{ij}\left(\sum_k G_{kk}^2\right)^2 \\
&+ \frac{u^2}{16}G_{ij}\sum_{k\ell}G_{kk}G_{\ell\ell}G_{k\ell}^2 + \frac{u^2}{48}G_{ij}\sum_{k\ell}G_{k\ell}^4 + \frac{u^2}{16}\sum_{k\ell}G_{ik}G_{jk}G_{kk}G_{\ell\ell}^2 \\
&+ \frac{u^2}{6} \sum_{k\ell}G_{ik}G_{j\ell}G_{k\ell}^3 + \frac{u^2}{4}\sum_{k\ell} G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + \frac{u^2}{4}\sum_{k\ell}G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} 
\end{align}$$

We see some substantial cancellations. Let's do these before expanding out the brackets in the second line, just to save some space. The final two terms in the first line cancel with the first two terms in the third line. Also the middle term in the first line combines with the final term in the second line. Thus our equations simplify to 

$$\begin{align}
\langle x_i x_j \rangle ={}& \frac{\langle x_i x_j e^{-S_{\text{int}}}\rangle}{\langle e^{-S_{\text{int}}} \rangle} \\
={}& G_{ij}\left(1 + \frac{u}{8}\sum_i G_{ii}^2 \right) \\
&+ \left(1+\frac{u}{8}\sum_k G_{kk}^2\right)\left(-\frac{u}{8}G_{ij}\sum_k G_{kk}^2 - \frac{u}{2}\sum_k G_{ik}G_{kk}G_{jk}\right) + \frac{u^2}{64}G_{ij}\left(\sum_k G_{kk}^2\right)^2 \\
&+ \frac{u^2}{16}\sum_{k\ell}G_{ik}G_{jk}G_{kk}G_{\ell\ell}^2 \\
&+ \frac{u^2}{6} \sum_{k\ell}G_{ik}G_{j\ell}G_{k\ell}^3 + \frac{u^2}{4}\sum_{k\ell} G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + \frac{u^2}{4}\sum_{k\ell}G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} 
\end{align}$$

Now, expanding out the brackets we get 

$$\begin{align}
\langle x_i x_j \rangle ={}& G_{ij} + \frac{u}{8}G_{ij} \sum_k G_{kk}^2  \\
& -\frac{u}{8}G_{ij}\sum_k G_{kk}^2 - \frac{u}{2}\sum_k G_{ik}G_{kk}G_{jk} - \frac{u^2}{64}G_{ij}\left(\sum_{k}G_{kk}\right)^2 - \frac{u^2}{16}\sum_k G_{ik}G_{kk}G_{jk}\sum_\ell G_{\ell\ell}^2  \\
&+ \frac{u^2}{64}G_{ij}\left(\sum_k G_{kk}^2\right)^2+ \frac{u^2}{16}\sum_{k\ell}G_{ik}G_{jk}G_{kk}G_{\ell\ell}^2 \\
&+ \frac{u^2}{6} \sum_{k\ell}G_{ik}G_{j\ell}G_{k\ell}^3 + \frac{u^2}{4}\sum_{k\ell} G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + \frac{u^2}{4}\sum_{k\ell}G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} 
\end{align}$$

Now, the second term of the first line cancels with the first term of the second line, and the final two terms of the second line cancel the third line completely. Thus, we get 

$$\begin{align}
\langle x_i x_j \rangle ={}& G_{ij} - \frac{u}{2}\sum_k G_{ik}G_{kk}G_{jk} \\
&+ \frac{u^2}{6} \sum_{k\ell}G_{ik}G_{j\ell}G_{k\ell}^3 + \frac{u^2}{4}\sum_{k\ell} G_{ik}G_{k\ell}G_{j\ell}G_{kk}G_{\ell\ell} + \frac{u^2}{4}\sum_{k\ell}G_{ik}G_{kj}G_{k\ell}^2 G_{\ell\ell} 
\end{align}$$

We see that this is almost the same as the result of part (a), but the ``disconnected" diagrams have gone away! This is an example of the <i>linked cluster theorem</i>, which states that only the connected diagrams need to be kept. What we mean by connected will be more obvious when we actually draw the diagrams in the next part.

</li>
<li> The corresponding diagrams are 

$$\begin{align}
\langle x_i x_j \rangle ={}& 
<figure class="center"><p><img src="figures/feynman_diagram_GF_ij.pdf" alt="Function" class="center" style="width:53.213px;height:18.404px;"> </p></figure> 
+ 
<figure class="center"><p><img src="figures/feynman_diagram_GF_ijk.pdf" alt="Function" class="center" style="width:95.733px;height:60.044px;"> </p></figure> \\
&+ 
<figure class="center"><p><img src="figures/feynman_diagram_GF_ijkl_oyster.pdf" alt="Function" class="center" style="width:138.253px;height:54.395px;"> </p></figure> 
+ 
<figure class="center"><p><img src="figures/feynman_diagram_GF_ijkl_2loop.pdf" alt="Function" class="center" style="width:138.253px;height:59.628px;"> </p></figure> \\
&+ 
<figure class="center"><p><img src="figures/feynman_diagram_GF_ijk_looplloop.pdf" alt="Function" class="center" style="width:95.733px;height:102.564px;"> </p></figure>
\end{align}$$

We can see that these are the ``connected diagrams"
</li></ol>

</div>

\subsection{Cumulant Expansion}

<ol>
<li> <div class="exercise">  This problem will discuss the cumulant expansion. This is a technique which is useful doing certain types of perturbation theory, for example when treating interactions in statistical mechanics, when deriving effective theories for order parameters, and for doing renormalization group calculations. Suppose we have a quantity \(A(\x)\) whose expectation value we want to compute: \(A(\x) = e^{rB(\x)}\). We are interested in calculating 

$$\begin{equation}
\langle A(\x) \rangle = \langle e^{rB(\x)} \rangle.
\end{equation}$$

If we are interested in the logarithm of this expectation value, which is something that will come up later, is there any way to write it in terms of expectation values of \(B(\x)\)? Let's consider the quantity 

$$\begin{equation}
\log\langle e^{rB(\x)} \rangle
\end{equation}$$

To tackle this, we can first Taylor expand the exponential:

$$\begin{align}
\log\langle e^{rB(\x)} \rangle ={}& \log \left\langle \sum_{n=0}^\infty \frac{r^n}{n!} B(\x)^n \right\rangle \\
={}& \log\left(1 + \sum_{n=1}^\infty \frac{r^n}{n!}\langle B(\x)^n\rangle\right)
\end{align}$$

Next, we could Taylor expand the logarithm as 

$$\begin{equation}
\log(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots = \sum_{n=1}^\infty (-1)^{n+1} \frac{x^n}{n}
\end{equation}$$

It is clear that the resulting expression would be an absolute mess. We would be taking the power of a Taylor series (\(x\) itself is a sum of infinitely many terms!). What is clear however is that there will be some combinations of expectation values which will come up, but what are these combinations? Well, let's call the combinations at a certain order \(\langle B(\x)^n\rangle_c\). Note that the subscript \(c\) means this is NOT the same as the expectation value from before. Then these <i>cumulants</i> are defined by 

$$\begin{equation}
\log\langle e^{rB(\x)} \rangle = \sum_{n=1}^\infty \frac{r^n}{n!}\langle B(\x)^n \rangle_c.
\end{equation}$$

<ol type="a">
<li> Expand out the expressions of the cumulant expansion to second order in \(r\). That is, for the following equation, 

\(\)\log\left(1 + \sum_{n=1}^\infty \frac{r^n}{n!}\langle B(\x)^n \rangle \right) = \sum_{n=1}^\infty \frac{r^n}{n!}\langle B(\x)^n \rangle_c,\(\)

match coefficients of \(r\) and \(r^2\), and thereby determine what \(\langle B(\x)\rangle_c\) and \(\langle B(\x)^2\rangle_c\) are in terms of \(\langle B(\x) \rangle\) and \(\langle B(\x)^2 \rangle\).

</li>
<li> There is actually a diagrammatic way to determine what the cumulants are (this is unrelated to the diagram technique that we looked at in the previous problems). The expectation \(\langle A(\x)^n\rangle\) can be expressed in terms of cumulants. Draw \(n\) dots, then consider all possible ways to draw circles around them. For the case of \(n=3\), we find that 

$$\begin{equation}
\langle A(\x)^3 \rangle = 
<figure class="center"><p><img src="figures/cumulant_30.pdf" alt="Function" class="center" style="width:28.745px;height:28.745px;"> </p></figure> 
\quad + \quad 3\times\,
<figure class="center"><p><img src="figures/cumulant_21.pdf" alt="Function" class="center" style="width:28.745px;height:25.91px;"> </p></figure>  
\quad +\quad 
<figure class="center"><p><img src="figures/cumulant_111.pdf" alt="Function" class="center" style="width:25.91px;height:25.91px;"> </p></figure> 
\end{equation}$$

In terms of symbols, this translates to 

$$\begin{equation}
\langle A(\x)^3 \rangle = \langle A(\x)^3 \rangle_c + 3\langle A(\x)^2\rangle_c \langle A(\x) \rangle_c + \langle A(\x) \rangle_c^3
\end{equation}$$

Solve for \(\langle A(\x)^3\rangle_c\) in terms of ordinary expectation values.

</li>
<li> Use the diagram technique to compute what \(\langle A(\x)^4 \rangle_c\) is in terms of ordinary expectation values.

</li>
<li> Using the cumulant expansion, compute \(\log (Z(u)/Z(0)) \) up to order \(u^2\). Also draw these diagrams. What is the difference between the diagrams in \(\log (Z(u)/Z(0))\) vs. the ones in \(Z(u)/Z(0)\)?

 
 </li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer1082')" class="answerButton">Show Answer</button> 
 <div  id='answer1082' class="answer" >
<ol type="a">
<li> Doing this, we find out that 

\(\)\log\left(1 + r\langle B(\x)\rangle + \frac{r^2}{2}\langle B(\x)^2\rangle\right) \sim  r\langle B(\x)\rangle + \frac{r^2}{2} \langle B(\x)^2\rangle - \frac{r^2}{2} \langle B(\x)\rangle^2\(\)

This tells us that \(\langle B(\x)\rangle = \langle B(\x)\rangle_c\), and also that \(\langle B(\x)^2\rangle_c = \langle B(\x)^2\rangle - \langle B(\x)^2\rangle\). 

</li>
<li> This gives us 

$$\begin{align}
\langle A(\x)^3\rangle_c ={}& \langle A(\x)^3\rangle - 3(\langle A(\x)^2\rangle - \langle A(\x)\rangle^2)\langle A(\x)\rangle - \langle A(\x)\rangle^3 \\
={}& \langle A(\x)^3\rangle - 3\langle A(\x)^2\rangle \langle A(\x)\rangle + 2\langle A(\x)\rangle^3
\end{align}$$


</li>
<li> The diagram technique yields 

$$\begin{equation}
\langle A(\x)^4 \rangle = 
<figure class="center"><p><img src="figures/cumulant_40.pdf" alt="Function" class="center" style="width:34.415px;height:34.415px;"> </p></figure> 
\quad + \quad 4\times 
<figure class="center"><p><img src="figures/cumulant_31.pdf" alt="Function" class="center" style="width:28.502px;height:26.707px;"> </p></figure>  
\quad +\quad 3\times 
<figure class="center"><p><img src="figures/cumulant_22.pdf" alt="Function" class="center" style="width:28.745px;height:25.91px;"> </p></figure> 
\quad + \quad 6\times 
<figure class="center"><p><img src="figures/cumulant_211.pdf" alt="Function" class="center" style="width:28.745px;height:25.91px;"> </p></figure> 
\quad + \quad 
<figure class="center"><p><img src="figures/cumulant_1111.pdf" alt="Function" class="center" style="width:25.91px;height:25.91px;"> </p></figure> 
\end{equation}$$

whose equation is given by 

$$\begin{equation}
\langle A(\x)^4\rangle = \langle A(\x)^4\rangle_c + 4\langle A(\x)^3\rangle_c \langle A(\x)\rangle_c + 3\langle A(\x)^2\rangle_c^2 + 6\langle A(\x)^2\rangle_c \langle A(\x)\rangle_c^2 + \langle A(\x)\rangle_c^4
\end{equation}$$

Now, plugging in the previously known values, we find 

$$\begin{equation}
\langle A(\x)^4\rangle_c = \langle A(\x)^4\rangle - 4\langle A(\x)^3\rangle \langle A(\x)\rangle - 3\langle A(\x)^2\rangle^2 + 12\langle A(\x)^2\rangle \langle A(\x)\rangle^2 - 6\langle A(\x)\rangle^4
\end{equation}$$

</li>
<li> According to the cumulant expansion, we have 

$$\begin{equation}
\log\left(\frac{Z(u)}{Z(0)}\right) = \log \langle e^{-S_{\text{int}}}\rangle = \langle -S_{\text{int}}\rangle_{0,c} + \frac{1}{2}\langle (-S_{\text{int}})^2 \rangle_{0,c} + \cdots 
\end{equation}$$

Now plugging in the definitions of the cumulants, we have 

$$\begin{equation}
\log\left(\frac{Z(u)}{Z(0)}\right) = -\langle S_{\text{int}}\rangle_0 + \frac{1}{2}(\langle S_{\text{int}}^2\rangle_0 - \langle S_{\text{int}}\rangle_0^2) + \cdots
\end{equation}$$

It is then clear that the series generated will just give us the <i>connected</i> diagrams! The disconnected ones are subtracted away! 

</li></ol>
</div> 
 </div>

</div> </li></ol>


