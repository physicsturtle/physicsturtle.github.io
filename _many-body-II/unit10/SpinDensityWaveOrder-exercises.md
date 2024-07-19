---
layout: exercises
title: Spin Density Wave Order  - Exercises
dept: physics
course: many-body-II
unit: unit10
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 10
---
<ol>
<li> <div class="exercise">  Evaluate the quantity 
$$\begin{equation}
\frac{1}{\beta}\sum_{ip_0} \mathcal{G}_0(k+p)\mathcal{G}_0(p),
\end{equation}$$

and recall that 
$$\begin{equation}
\mathcal{G}_0(p) = \mathcal{G}_0(\p, ip_0) = \frac{1}{ip_0 - \xi_{\p}}
\end{equation}$$

<div class="answerBox"> 
 <button onclick="myFunction('answer11')" class="answerButton">Show Answer</button> 
 <div  id='answer11' class="answer" >

Thus the final result is given by
$$\begin{equation}
\frac{1}{\beta}\sum_{ip_0}\mathcal{G}_0(k+p)\mathcal{G}_0(p) = \frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}}
\end{equation}$$
</div> 
 </div>

</div> </li>
<li> <div class="exercise">  Itinerant electron ferromagnetism is a special case of a spin-density wave. 
<ol type="a">
<li> What is the ordering vector \(\k\) for ferromagnetism?
</li>
<li> Does this model have a ferromagnetic transition at temperature \(T_C\) for any value of the parameters \(U\), \(\mu\), \(t\)? If so, what is \(T_C\)?
</li></ol>

<div class="answerBox"> 
 <button onclick="myFunction('answer25')" class="answerButton">Show Answer</button> 
 <div  id='answer25' class="answer" >
Clearly, if \(k_0\neq 0\), then there is no solution to the equation 

\(\)\frac{3}{U} + \frac{2}{N}\sum_{\p}\frac{n_F(\xi_{\p}) - n_F(\xi_{\p+\k})}{ik_0 + \xi_{\p} - \xi_{\p+\k}} = 0.\(\)

for \(\k=0\). If however we set \(k_0 = 0\), then we end up with a \(0/0\) situation. We set \(k_0 = 0\) and then take a limit \(\k\to 0\). Doing this, we find that 
</div> 
 </div>


</div> </li></ol>

\begin{faq}
FAQ:

Q:When we do the Hubbard-Stratonovich transformation, how do we do it only at a single site?

A: you can take the product over all sites

Q: When we do the HS stransformatinon, how do we do it only at a single imaginary time? Further more, what's up with the units?

A: For this, you can do the following: (show calculation absorbing \\(\Delta\tau\\) in to the HS field)
\end{faq}

