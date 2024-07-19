---
layout: page
title: Linearization
course: test
unit: unit1
permalink: /test/linearization/
---

For one dimensional autonomous systems $x' = f(x)$, we linearize as follows. If $f(\xi) = 0$, then we can linearize about $\xi$ by Taylor expanding about it. This approximation is $f(x) \approx f(\xi) + (x-\xi)f'(\xi) = (x-\xi)f'(\xi)$. So, in the neighbourhood of $\xi$, the system becomes $x' \approx (x-\xi)f'(\xi)$, because $f(\xi) = 0$. 

Note that we have ignored quadratic and higher order terms in $(x-\xi)$. This is because they are negligbly small compared to the first order term. However, if $f'(\xi) = 0$, then they are not neglibly small at all! In this case, we need to do a nonlinear stability analysis. It is also possible that $f'(\xi)$ does not exist; maybe $f(x) = \sqrt{x}$, so $x= 0$ is a fixed point but $f'(0)$ doesn't exist! 






