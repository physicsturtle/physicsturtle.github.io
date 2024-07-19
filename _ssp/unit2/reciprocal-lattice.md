---
layout: lesson
title: Reciprocal Lattice
course: ssp
unit: unit1
---

Given a Bravais lattice, it is possible to construct a so called reciprocal lattice out of the Bravais lattice vectors. 

Suppose the primitive lattice vectors of a lattice at $\textbf{a}_1$, $\textbf{a}_2$ and $\textbf{a}_3$. Then, we define the reciprocal lattice vectors $\{\textbf{b}_1, \textbf{b}_2, \textbf{b}_3\}$ so that they satisfy 

$$\textbf{a}_i\cdot\textbf{b}_j = 2\pi \delta_{ij}$$

Exercise: Calculate the formulas for the reciprocal lattice vectors in terms of the real lattice vectors in 2 dimensions. Again use the formula 

$$\textbf{a}_i\cdot\textbf{b}_j = 2\pi \delta_{ij}.$$

Solution: Let the real lattice vectors be $\textbf{a}_1$ and $\textbf{a}_2$. Since they form a basis, we can express the reciprocal lattice vectors in terms of them. To do this, pick some coefficients and write

$$\textbf{b}_1 = x_{11}\textbf{a}_1 + x_{12}\textbf{a}_2,\qquad \textbf{b}_2 = x_{21}\textbf{a}_2 + x_{22}\textbf{a}_2.$$

If we take all the appropriate dot products, then we find the following 4 equations:

\begin{align*}
x_1\textbf{a}_1\cdot\textbf{a}_1 + y_1\textbf{a}_1 \cdot\textbf{a}_2 = 2\pi \\
x_1\textbf{a}_2\cdot\textbf{a}_2 + y_1\textbf{a}_2\cdot\textbf{a}_2 = 0\\
x_2\textbf{a}_1\cdot\textbf{a}_1 + y_2\textbf{a}_1\cdot\textbf{a}_2 = 0\\
x_2\textbf{a}_1\cdot\textbf{a}_2 + y_2\textbf{a}_2\cdot\textbf{a}_2 = 2\pi
\end{align*}

If we solve these equations, we find that 

\begin{align*}
x_{11} = \frac{2\pi\textbf{a}_2\cdot\textbf{a}_2}{\textbf{a}_1\cdot\textbf{a}_1 \textbf{a}_2\cdot\textbf{a}_2 - (\textbf{a}_1\cdot\textbf{a}_2)^2}\\
x_{12}1 = -\frac{2\pi \textbf{a}_1\cdot\textbf{a}_2}{\textbf{a}_1\cdot\textbf{a}_1 \textbf{a}_2\cdot\textbf{a}_2 - (\textbf{a}_1\cdot\textbf{a}_2)^2}\\
x_{21} = -\frac{2\pi \textbf{a}_1\cdot\textbf{a}_2}{\textbf{a}_1\cdot\textbf{a}_1 \textbf{a}_2\cdot\textbf{a}_2 - (\textbf{a}_1\cdot\textbf{a}_2)^2}\\
x_{22} = \frac{2\pi \textbf{a}_1\cdot\textbf{a}_1}{\textbf{a}_1\cdot\textbf{a}_1 \textbf{a}_2\cdot\textbf{a}_2 - (\textbf{a}_1\cdot\textbf{a}_2)^2}
\end{align*}

This gives us coefficients for a matrix:

$$\begin{pmatrix} \textbf{g}_1 \\ \textbf{g}_2 \end{pmatrix} = \begin{pmatrix} x_{11} & x_{12} \\ x_{21} & x_{22}\end{pmatrix}\begin{pmatrix} \textbf{a}_1 \\ \textbf{a}_2 \end{pmatrix} $$




