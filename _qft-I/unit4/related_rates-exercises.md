---
layout: exercises
title: Related Rates - Exercises
dept: math
course: calculus-I
unit: unit4
deptDisplay: Math
courseDisplay: Calculus I
unitDisplay: Unit 4
---

<ol>
<li> <div class="exercise"> Two sides of a triangle are 15 and 20 m long, respectively. 
<ol type="a">
<li> How fast is the third side increasing if the angle between the given sides is $\pi/3$ and is increasing at a rate of $\pi/45$ radians per second? </li>
<li> How fast is the area increasing? </li>
</ol>

<div class="answerBox">
<button onclick="myFunction('answer1')" class="answerButton">Show Answer</button>
<div  id="answer1" class="answer" >
<!--- 
\begin{tikzpicture}[thick]
\coordinate (O) at (0,0);
\coordinate (A) at (4,0.25);
\coordinate (B) at (0,2);
\draw (O)--(A)--(B)--cycle;

\tkzLabelSegment[below=2pt](O,A){\textit{15}}
\tkzLabelSegment[left=2pt](O,B){\textit{l}}
\tkzLabelSegment[above right=2pt](A,B){\textit{20}}

\tkzMarkAngle[fill= orange,size=1.5cm,%
opacity=.4](B,A,O)
\tkzLabelAngle[pos = -1.5](B,A,O){$\theta = \pi/3$}

\end{tikzpicture} --->
<ol type="a">
<li> We know from the given information that $\displaystyle{\frac{d\theta}{dt}=\frac{\pi}{45}}$. Using the cosine law, we relate the lengths of the sides and the angle $\theta$, then differentiate with respect to time, $t$.
\begin{eqnarray*}
l^2 &=& 15^2 +20^2 - 2(15)(20)\cos(\theta)\\
l^2 &=& 625-600\cos(\theta)\\
\frac{d}{dt}[l^2] &=& \frac{d}{dt}[625] - \frac{d}{dt}[600\cos(\theta)]\\
2l\cdot l' &=& 600\sin(\theta)\theta' 
\end{eqnarray*}
Now that we have an expression involving $l'$, we need to find evaluate both sides of the equation at $\theta = \pi/3$. We are trying to find $l'$ when $\theta = \pi/3$ so we need to calculate $l(\pi/3)$ and plug that value into the expression above.
\[\textit{l}^2=15^2 +20^2 -2(15)(20)\cos(\pi/3) = 325 \]
Solving for $l$, we get \[ \textit{l} = 5\sqrt{13}\]
We now have all three values to evaluate $2l\cdot l' = 600\sin(\theta)\theta' $. They are
\[\theta = \frac{\pi}{3} ,\quad \theta' = \frac{\pi}{45} ,\quad \textit{l}=5\sqrt{13}\]
Plugging the values in,
\[2(5\sqrt{13})l'=600\sin\left(\frac{\pi}{3}\right) \cdot \frac{\pi}{45}\]
Now solving for $l'$:
\[l' = \frac{2\pi}{\sqrt{39}}\,\si{m/s}\]
</li>
<li> The area of a triangle is given by $A=\frac{1}{2}ab\sin(C)$. We differentiate the formula for the area of a triangle with respect to time $t$, and then evaluate at $\theta = \pi/3$.

\begin{eqnarray*}
\frac{d}{dt}[A]&=&\frac{d}{dt}[150\sin(\theta)]\\
A'&=& 150\cos(\theta)\cdot\theta'\\
A'&=& 150\cos\left(\frac{\pi}{3}\right)\cdot\frac{\pi}{45}=\frac{75\pi}{45} 
\end{eqnarray*}
\[A'(\pi/3) = \frac{5\pi}{3}\,\si{m^2/s}\]
</li>
</ol>
</div>
</div>
</div>
</li>


<li> <div class="exercise"> Two ships sail from the origin at the same time. One sails south at 15 km/hr; the other sails east at 25 km/hr for 1 hour and then turns north. Find the rate of rotation in rad/s of the line joining them after 3 hours. 

<div class="answerBox">
<button onclick="myFunction('answer2')" class="answerButton">Show Answer</button>
<div  id="answer2" class="answer" >
<!--- 
\begin{tikzpicture}[thick]
\draw (-1,0) -- (4,0);
\draw (0,-2) -- (0,4);
\filldraw [gray] (0,0) circle (2pt);

\coordinate (O) at (0,-1);
\coordinate (A) at (3.5,-1);
\coordinate (B) at (3.5,2.5);
\draw (O)--(A)--(B)--cycle;

\tkzLabelSegment[below=2pt](O,A){\textit{x component}}
\tkzLabelSegment[left=2pt](O,B){\textit{displacement}}
\tkzLabelSegment[above right=2pt](A,B){\textit{y component}}

\tkzMarkAngle[fill= red,size=0.5cm,%
opacity=.4](A,O,B)
\tkzLabelAngle[pos = 0.7](A,O,B){$\theta$}

\coordinate (N) at (3.5,3.5);
\coordinate (S) at (0,-2);
\draw[red] [->] (B) -- (N);
\draw[red] [->] (O) -- (S);
\tkzLabelSegment[right=2pt](B,N){$\frac{dy}{dt}=25$\:km/h}
\tkzLabelSegment[left=2pt](O,S){$\frac{dy}{dt}=-15$\:km/h}

\end{tikzpicture}
--->

The question can be simplified by setting $t=0$ at one hour where the east bound ship is 25km east, then turns north, and the south bound ship is 15km south, then find the rad/s after 2 hours instead of 3. Based on the diagram above, which is simplified to show some time after 1 hour displays the following: \textit{displacement}, \textit{x-component}, and \textit{y-component} of the displacement. It also shows the vectors along which the ships are travelling in red, and their rate of travel.

First, determine the net change in $y$ of \textit{displacement} with respect to time: $y'=\frac{dy}{dt}=25+15=40$ km/h. Also, note that the \textit{x component} is a constant 15 km because the erstwhile eastbound ship only had 1 hour at 15 km/h to travel in the $+x$ direction, so this does not change with time.
After 3 hours, the $y$ component of the displacement is $y = 2\cdot 25 + 3\cdot 15 = 95\,\si{km}$; remember that it is 2 times 25, not 3 times 25, because the north bound ship has been travelling north for the latter 2 hours.
Second, relate $\theta$ and \textit{y} using tan, then differentiate with respect to time using the chain rule:
\begin{eqnarray*}
\tan(\theta) &=& \frac{y}{25}\\
\theta &=& \arctan\left(\frac{y}{25}\right)\\
\theta' &=& \frac{d\theta}{dt}\left[\arctan\left(\frac{y}{25}\right)\right]\\
\theta' &=& \frac{1}{1+(\frac{y}{25})^2}\cdot\frac{y'}{25}\\
\theta' &=& \frac{1}{1+(\frac{95}{25})^2}\cdot \frac{40}{25} \approx 0.1036
\end{eqnarray*}

So the angle is changing at 0.1036 rad/h

</div>
</div>
</div>
</li>


<li> <div class="exercise"> Gas is escaping from a spherical balloon at the rate of 2 cubic feet per minute. How fast is the surface area shrinking when the radius is 12 ft?

<div class="answerBox">
<button onclick="myFunction('answer3')" class="answerButton">Show Answer</button>
<div  id="answer3" class="answer" >
For a sphere, the formula for the volume is 
\[V = \frac{4}{3}\pi r^3\]
and the formula for the surface area is 
\[A = 4\pi r^2\] we can do the following rearrangement to find a relationship between the area and volume of a sphere: 
\[A^{3/2} = (4\pi)^{3/2}r^3\] This means that 
\[V  =\frac{ A^{3/2}}{3\sqrt{4\pi}}\]
Now we differentiate both sides: 
\[\frac{dV}{dt} = -2 = \frac{\sqrt{A}}{2\sqrt{4\pi}}\cdot\frac{dA}{dt}\]
When $r = 12$, $A = 4\pi\cdot144$, so then we can evaluate the derivative:
\[-2 = \frac{12}{2}\frac{dA}{dt}\]
Solving for $dA/dt$:
\[\frac{dA}{dt} = -\frac{1}{3} \,\si{ft^2/s}\]

</div>
</div>
</div>
</li>

<li> <div class="exercise"> Water, at the rate of $10\,\si{ft^3/min}$, is pouring into a leaky cistern whose shape is a cone 16 feet deep and 8 inches diameter at the top. At the time the water is 12 feet deep, the water level is observed to be rising 4 inches/min. How fast is the water leaking away?

<div class="answerBox">
<button onclick="myFunction('answer4')" class="answerButton">Show Answer</button>
<div  id="answer4" class="answer" >
The volume of a cone is given by 
\[V = \frac{1}{3}\pi r^2h\]
From similar triangles, we have 
\[h(t) = 48r(t)\]
Substituting $r$ into the volume formula, we obtain 
\[V = \frac{\pi h^3}{3\cdot 48^2}\]
Differentiating this new volume formula with respect to $t$, 
\[\frac{dV}{dt} = \pi\frac{h^2}{48^2}\frac{dh}{dt}\]
Now evaluating this at $h = 12\,\si{ft}$, and $h' = 1/3\,\si{ft/min}$, we get that
\[\frac{dV}{dt} = \frac{\pi}{48}\,\si{ft^3/min}\]
Let the net water flow in be $\displaystyle{\frac{dV}{dt} = 10 - \frac{dV_\text{out}}{dt}}$\\
Then, $\displaystyle{10 - \frac{dV_\text{out}}{dt} = \frac{\pi}{48}}$, so the rate of water flow out of the cone is 
\[\frac{dV_\text{out}}{dt} = \left(10 - \frac{\pi}{48}\right)\,\si{ft^3/min}\]

</div>
</div>
</div>
</li>


</ol>
