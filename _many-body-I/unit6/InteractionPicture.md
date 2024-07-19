---
layout: lesson
title: Interaction Picture 
dept: physics
course: many-body-I
unit: unit6
deptDisplay: Physics
courseDisplay: Many Body Physics I
unitDisplay: Unit 6
---
In the interaction picture, also known as the Dirac picture (although I do not think ``Dirac picture" is common terminology), the states and operators are both time dependent, but in a different way than seen in the previous two pictures. We again require that expectation values be the same. However, this time, the interaction picture time evolution is given by

$$\begin{equation}
\hat{A}_I(t) := e^{i\hat{H}_0t/\hbar}\hat{A}_S e^{-i\hat{H}_0t/\hbar}.
\end{equation}$$

Using this, we can find how the interaction picture states are defined. To do this, we again return to the expectation values and get 

$$\begin{align}
\bra{\psi_S(t)}\hat{A}_S\ket{\psi_S(t)} ={}&\bra{\psi_I(t)}\hat{A}_I(t) \ket{\psi_I(t)} \\
\bra{\psi_S(0)}e^{i\hat{H}t/\hbar} \hat{A}_S e^{-i\hat{H}t/\hbar}\ket{\psi_S(0)}  ={}& \bra{\psi_I(t)} e^{i\hat{H}_0t/\hbar}\hat{A}_S e^{-i\hat{H}_0t/\hbar} \ket{\psi_I(t)} \\
\end{align}$$

from which we conclude that 

$$\begin{equation}
e^{-i\hat{H}t/\hbar}\ket{\psi_S(0)} = e^{-i\hat{H}_0t/\hbar}\ket{\psi_I(t)},\qquad \ket{\psi_I(t)} = e^{i\hat{H}_0t/\hbar}e^{-i\hat{H}t/\hbar} \ket{\psi_S(0)}.
\end{equation}$$

so calculating the time evolved interaction picture operators is much easier than calculating the time evolved interaction picture state. This also gives us the relationship between the Heisenberg and interaction picture operators: 

$$\begin{equation}
\hat{A}_I(t) = e^{i\hat{H}_0t/\hbar}e^{-i\hat{H}t/\hbar} \hat{A}_H(t) e^{i\hat{H}t/\hbar} e^{-i\hat{H}_0t/\hbar}
\end{equation}$$

We can find the time evolution operator in the interaction picture by writing

$$\begin{align}
\ket{\psi_I(t')} ={}& e^{i\hat{H}_0t'/\hbar}e^{-i\hat{H}t'/\hbar} \ket{\psi_S(0)}\\
\ket{\psi_S(0)} ={}& e^{i\hat{H}t/\hbar}e^{-i\hat{H}_0t/\hbar}\ket{\psi_I(t)}
\end{align}$$ 

which allows us to plug the second equation into the first, and find

$$\begin{align}
\ket{\psi_I(t')} = e^{i\hat{H}_0t'/\hbar} e^{-i\hat{H}(t'-t)/\hbar} e^{-i\hat{H}_0t/\hbar} \ket{\psi_I(t)}
\end{align}$$

and therefore we find that 

$$\begin{equation}
\hat{U}_I(t',t) = e^{i\hat{H}_0t'/\hbar} e^{-i\hat{H}(t'-t)/\hbar} e^{-i\hat{H}_0t/\hbar}
\end{equation}$$

