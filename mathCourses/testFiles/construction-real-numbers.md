---
layout: page
title: Construction of the Real Numbers
course: test
unit: unit1
permalink: /test/real-numbers
---


In mathematics, four of the most commonly used sets of numbers are the natural numbers $\mathbb{N}$, the integers $\mathbb{Z}$, the rational numbers $\mathbb{Q}$, and the real numbers $\mathbb{R}$. The first of these three have something in common with each other that is different for the real numbers $\mathbb{R}$. They are all countable, but the real numbers are not countable. This begs the question, how can one arrive at an irrational number by using the set of rational numbers? It is possible to define rational numbers by dividing integers, but none of the elementary arithmetic operations, i.e. addition, subtraction, multiplication, or division can help us to arrive at an irrational number. In this lesson, we will construct the real numbers out of the rational numbers using a method called \textit{Dedekind Cuts}. 

\section{Dedekind Cuts}

\begin{definition}
Let $\alpha \subset \mathbb{Q}$. Then $\alpha$ is called a \underline{cut} if it satisfies the following three properties:
\begin{enumerate}[(i)]
\item $\alpha \not= \emptyset$ and $\alpha \not= \mathbb{Q}$
\item If $p\in \alpha$ and $q \in \mathbb{Q}$ and $q < p$, then $q \in \alpha$
\item If $p \in \alpha$, then $p < r$ for some $r\in \alpha$. 
\end{enumerate}
Note that $p,q,r$ are all rational numbers, and $\alpha$ is a cut. We will use Greek letters for cuts. 
\end{definition}

%Examples$
We will now have some examples with cuts. It turns out that cuts will be the definitions of the real numbers.

%Counterexample of a Dedekind cut.
\begin{example}
Let $$\alpha =\left\{ x \in \mathbb{Q} \left| \frac{1}{2} \leq x \leq 1 \right.\right\}$$
We will check the three conditions to see if $\alpha$ is a cut. 
\begin{enumerate}[(i)]
\item Since $\alpha \not= \emptyset$ and $\alpha \not= \mathbb{Q}$, it satisfies the first condition.
\item Let $p = \frac{1}{2} \in \alpha $, and $q = 0 \in \mathbb{Q}$. We have $q < p$, but $q \not\in \alpha$. Thus this cut fails the second condition.
\item Let $p = 1 \in \alpha$. Since $p$ is the largest element of $\alpha$, there does not exist an element $r$ that is bigger than $p$, but also in $\alpha$. Thus this cut $\alpha$ fails the third condition as well. 
\end{enumerate}
\end{example}

%Example of a Dedekind cut with the resulting real number a rational
\begin{example}
Let 
$$\beta = \left\{ x \in \mathbb{Q} \left| x < 1 \right. \right\}$$
We will check the three conditions to see if $\beta$ is a cut. 
\begin{enumerate}[(i)]
\item Since $\beta \not= \emptyset$ and $\beta \not= \mathbb{Q}$, it satisfies the first condition.
\item Let $p \in \beta $, and $q \in \mathbb{Q}$. If $q < p$, then $q < p < 1 $, so $q < 1$. This means that $q \in \beta$. Thus $\beta$ satisfies the second condition. 
\item Let $p \in \beta$. Define $r = \frac{p + 1}{2}$. Thus $r$ is between $p$ and 1 because it is the average of the two points. We then have $p < r < 1$, and $r\in\beta$. Thus the third condition is satisfied.
\end{enumerate}
Since $\beta$ satisfies all three conditions, we can conclude that it is a cut. 
\end{example}

%Example of a Dedekind cut with the resulting real number irrational.
\begin{example}
Let
$$\gamma = \left\{ x \in \mathbb{Q} \left| x^2 < 2 \right. \right\} \cup \left\{ x \in \mathbb{Q} \left| x < 0 \right. \right\}$$
Thus $\gamma$ is the set of all rational numbers which are less than $\sqrt{2}$ (even though we have not defined $\sqrt{2}$ yet). We will check the three conditions to see if $\gamma$ is a cut. 
\begin{enumerate}[(i)]
\item Since $\gamma \not= \emptyset$ and $\gamma \not= \mathbb{Q}$, it satisfies the first condition.
\item Let $p \in \gamma$, and $q \in \mathbb{Q}$. Let $q < p$, and if $0 < q$, then $q^2 < p^2$ so $q \in \gamma$. If $q < 0$, then $q \in \gamma$. Thus $\gamma$ satisfies the second condition. 
\item  Let $p \in \gamma$, and $r \in \mathbb{Q}$. Let $r >0$ and define $r^2 = \frac{p^2+2}{2}$. Thus we have that $r \in \gamma$. So $\gamma$ satisfies the third condition.
\end{enumerate}
Since $\gamma$ satisfies all three conditions, we can conclude that it is a cut. 
\end{example}

From these three examples we conclude that a cut must be unbounded from below, and that the upper bound must not be an element of the set. Note that Dedekind cuts It turns out that the Dedekind cuts that have been defined so far correspond to $\beta = 1$ and $\gamma = \sqrt{2}$. 

\begin{definition}
The set $\mathbb{R}:=\{ \alpha | \alpha \text{ is a cut }\}$ defines the set of all real numbers. 
\end{definition}
It is important to recall that each real number $\alpha$ (a.k.a. cut) is \underline{actually a set}. The operations that we are familiar with from high school such as addition, subtraction, multiplication, and division will need to be defined in terms of the sets that correspond to each cut. 

\section{Operations on the Real Numbers}

\begin{definition}
If $\alpha$ is a proper subset of $\beta$, define $\alpha < \beta$. 
\end{definition}
Set theory gives us 
$$\alpha \subset \beta \wedge \beta \subset \gamma \Rightarrow \alpha \subset \gamma$$
which means that 
$$\alpha < \beta \wedge \beta < \gamma \Rightarrow \alpha < \gamma$$

\begin{definition}
Let 
$$+ : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$$ 
where $$(\alpha, \beta) \mapsto \alpha + \beta$$
be defined by the following cut:
$$\alpha + \beta = \{ p + q | p \in \alpha \wedge q \in\beta\}$$
\end{definition}
However, we need to prove that the set $\alpha + \beta$ is actually a cut. 
\begin{theorem}
If $\alpha$ and $\beta$ are cuts, then 
$$\alpha + \beta = \{ p + q | p \in \alpha \wedge q \in\beta\}$$ is also a cut.
\end{theorem}

\begin{proof}
\begin{enumerate}[(i)]
\item It is clear that $\alpha + \beta$ is a nonempty subset of $\mathbb{Q}$. To show that it is not $\mathbb{Q}$ itself, recall that cuts are bounded from above. Thus if $p' \not\in \alpha$, we have that $p' > p$, $\forall p \in \alpha$. 
\end{enumerate}
\end{proof}


















\end{document}
