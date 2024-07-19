---
layout: lesson
title: Heisenberg Picture 
dept: physics
course: many-body-I
unit: unit6
deptDisplay: Physics
courseDisplay: Many Body Physics I
unitDisplay: Unit 6
---
In the Heisenberg picture, the states are time independent, and the operators are time dependent. To find how these states and operators are related to the Schrödinger picture, we require that expectation values remain the same in every picture. That is, if \\(\hat{A}\\) is any operator, then

$$\begin{equation}
\langle\hat{A}\rangle = \bra{\psi_H}\hat{A}_H(t)\ket{\psi_H} = \bra{\psi_S(t)} \hat{A}_S \ket{\psi_S(t)}
\end{equation}$$

We define the Heisenberg states \\(\ket{\psi\_H} = \ket{\psi\_S(0)}\\). Thus, we find that 

$$\begin{equation}
\bra{\psi_S(t)} \hat{A}_S \ket{\psi_S(t)} = \bra{\psi_H}\hat{U}^\dagger (t,0)\hat{A}_S\hat{U}(t,0) \ket{\psi_H} 
\end{equation}$$

so we identify the quantity \\(\hat{U}^\dagger (t,0)\hat{A}\_S\hat{U}(t,0)\\) as \\(\hat{A}\_H(t)\\). We can write this as 

$$\begin{equation}
\hat{A}_H(t) := e^{i\hat{H}t/\hbar} \hat{A}_S e^{-i\hat{H}t/\hbar} 
\end{equation}$$

The Heisenberg equation of motion of a (time independent) operator is given by 

$$\begin{equation}
\frac{\d A}{\d t} = i[H,A]
\end{equation}$$

