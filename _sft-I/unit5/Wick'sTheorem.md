---
layout: lesson
title: Wick's Theorem 
dept: physics
course: sft-I
unit: unit5
deptDisplay: Physics
courseDisplay: Statistical Field Theory I
unitDisplay: Unit 5
---
In this section, we will discuss Wick's theorem for evaluating correlation functions of many points. It can be applied to Gaussian probability distribution functions. When we say Gaussian probability functions, this could mean some discrete, continuous, or even functional distribution functions. (check the terminology here). Suppose we have a probability density function of a real variable \\(\x \in \RR^d\\). 

$$\begin{equation}
P[\x] = e^{-\frac{1}{2}\sum_{i,j} x_i A_{ij}x_j},
\end{equation}$$

where \\(i\\) runs from \\(1\\) to \\(d\\). We are interested in calculating high order correlation functions such as \\(\left<x_i x_j x_\ell x_m\right>\\) with respect to this distribution. To do this, we define a <i>generating function</i> \\(Z_J\\) by

$$\begin{equation} \label{eq:vector_gaussian_generating_function}
Z[\mathbf{J}] = \int \exp\left(-\frac{1}{2}\sum_{i,j} x_i A_{ij}x_j + \sum_i J_i x_i \right) \d^d\x 
\end{equation}$$

and we make the following observation:

$$\begin{align}
 \frac{1}{Z[0]} \left(\frac{\partial}{\partial J_m} Z\right)[0] ={}& \frac{1}{Z[0]} \int \frac{\partial}{\partial J_m}\exp\left(-\frac{1}{2}\sum_{i,j} x_i A_{ij}x_j + \sum_i J_i x_i \right) \d^d\x \bigg|_{J = 0} \\
={}&  \frac{1}{Z[0]} \int \frac{\partial}{\partial J_m} \left(\sum_i J_i x_i\right) \exp\left(-\frac{1}{2}\sum_{i,j} x_i A_{ij}x_j + \sum_i J_i x_i \right) \d^d\x  \bigg|_{J = 0}\\
={}&  \frac{1}{Z[0]} \int \left(\sum_i \delta_{im} x_i\right) \exp\left(-\frac{1}{2}\sum_{i,j} x_i A_{ij}x_j + \sum_i J_i x_i \right) \d^d\x  \bigg|_{J = 0}\\
={}&  \frac{1}{Z[0]} \int x_m \exp\left(-\frac{1}{2}\sum_{i,j} x_i A_{ij}x_j + \sum_i J_i x_i \right) \d^d\x \bigg|_{\mathbf{J} = 0} \\
={}&  \frac{1}{Z[0]} \int x_m \exp\left(-\frac{1}{2}\sum_{i,j} x_i A_{ij}x_j\right) \d^d\x \\
={}& \left<x_m\right>
\end{align}$$

so, we can generate correlation functions by differentiating the generating function, then evaluating the resulting quantity at \\(\mathbf{J} = 0\\). This justifies the name <i>generating function</i>. Higher order correlation functions can be calculated by differentiating more times. You may have seen related concepts before in a probability course under the names of <i>moment generating function</i>, or <i>characteristic function</i>. This concept of course applies to expectation values with respect to any probability distribution function, not just the Gaussian. However, for the case of a Gaussian probability distribution function, we are actually able to find a closed form expression for \\(Z_J\\). This is what we will do now. 

Let's analyze the exponent of Eq. \eqref{eq:vector_gaussian_generating_function}. Suppose for the moment that \\(A\\) is a symmetric matrix with all positive eigenvalues (otherwise the integral is divergent). The symmetry property means that its eigenvectors are all orthogonal, so when we diagonalize it as \\(A = U^T \Lambda U\\),  \\(U\\) is an orthogonal matrix (so \\(U^{-1} = U^T\\)). We will switch between component notation and matrix/vector notation in order to make certain steps clearer. 

$$\begin{align}
-\frac{1}{2}\sum_{i,j} x_i A_{ij} x_j - \sum_i J_i x_i ={}& -\left(\frac{1}{2}\x^T  A \x + \mathbf{J}^T \x \right)\\
={}& -\left(\frac{1}{2}\x^T U^T \Lambda U \x + \mathbf{J}^T \x \right) \\
={}& -\left(\frac{1}{2}\y^T\Lambda \y + \mathbf{J}^TU^T\y  \right) \\
={}& -\left(\frac{1}{2}\y^T\Lambda \y + (U\mathbf{J})^T\y  \right)
\end{align}$$

where we made the substitution \\(\y = U\x\\). We switch now back to component notation, and define \\(<b>K</b> = U\mathbf{J}\\). 

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

we need to change the differential to \\(\d^d\y\\), which is easy because the Jacobian is \\(\det(U) = 1\\). Thus \\(\d^d\x = \d^d\y\\). After changing the differential, we can also shift the integration variable freely since the integral bounds are \\(-\infty\\) to \\(\infty\\) in each component of \\(\y\\).

$$\begin{align}
Z[\mathbf{J}] ={}& \exp\left(\frac{1}{2}\sum_i\frac{K_i^2}{\lambda_i} \right) \int \exp\left(-\frac{1}{2}\sum_i\lambda_i \left(y_i - \frac{K_i}{\lambda_i}\right)^2 \right) \d^d\y \\
={}& \exp\left(\frac{1}{2}\sum_i K_i \frac{1}{\lambda_i} K_i \right) \int \exp\left(-\frac{1}{2}\sum_i\lambda_i y_i^2 \right) \d^d\y \\
={}& \exp\left(\frac{1}{2} <b>K</b>^T\Lambda^{-1}<b>K</b>  \right) \prod_{i=1}^d \int \exp\left(-\frac{1}{2}\lambda_i y_i^2 \right) \\
={}& \exp\left(\frac{1}{2}\mathbf{J}^T U^T \Lambda^{-1} U \mathbf{J}  \right) \prod_{i=1}^d \sqrt{\frac{2\pi}{\lambda_i}} \\
={}& \exp\left(\frac{1}{2} \mathbf{J}^T A^{-1} \mathbf{J} \right) \sqrt{\frac{(2\pi)^d}{\det(A)}} \\
\end{align}$$

where we used that the product of all the eigenvalues is the determinant. Now that we have an explicit formula for \\(Z[\mathbf{J}]\\), it is easy just to take partial derivatives and thereby find the correlation functions. 

 
