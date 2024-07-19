---
layout: page
title: Gamma Function
course: test
unit: unit1
permalink: /test/gamma-function/
---


\subsection{Introduction}
The purpose of this exposition is to give the reader an introduction to the gamma function and some of its properties and applications.

\section{Motivation}
Suppose one is interested in factorials, and decides to plot $f(n) = n!$ for $n\in  \mathbb{N}_0$. Then, one draws a line through the points and wonders if there is some function defined on $\mathbb{R}$ that will go through all of the points $f(n) = n!$, $n\in \mathbb{N}_0$. There is some function $f(z) : \mathbb{C} \mapsto \mathbb{C}$ that satisfies this condition. It is in fact enough to find a function that satisfies the following two conditions: $$f(z+1) = zf(z)$$ $$f(1) = 1$$
\section{Definition}
A function that satisfies the above two conditions is the following:
\begin{definition}
Let $\Gamma(z) : \{z\in\mathbb{C} | \Re(z) > 0 \} \mapsto \mathbb{C}$ be defined by 
$$\Gamma(z) = \int_0^\infty e^{-x}x^{z-1} dx $$

\end{definition}
