---
layout: lesson
title: Trigonometric Integrals 
dept: math
course: calculus-II
unit: unit2
deptDisplay: Math
courseDisplay: Calculus II
unitDisplay: Unit 2
---
Trigonometric integrals are integrals that have trigonometric functions in them. It is useful to learn to evaluate these integrals because they come up in the study of differential equations (and therefore in physics), and we will also reduce certain integrals to trigonometric integrals by using trigonometric substitution later. Please note that trigonometric integrals (the subject of this section) are not to be confused with the method of trigonometric substitution. 

By a trigonometric integral, we mean an integral which only contains trigonometric functions, such as \\(\sin\\), \\(\cos\\), \\(\tan\\), \\(\sec\\), \\(\csc\\), or \\(\cot\\). Some trigonometric integrals are straightforward, and some are very difficult. We will only treat the simple ones in this section. We will however make note of the difficult ones, and we will come back to them when doing partial fractions in the next section. In this course, we will consider the following trigonometric integrals:

\begin{tabular}{|c|c|c|}
Integral & \\(u\\) substitution & Difficulty \\
\\(\displaystyle{\int\sin^{2m} x \cos^{2n+1} x \d x}\\) & \\(u = \sin x\\) & Easy \\
\\(\displaystyle{\int\cos^{2m} x \sin^{2n+1} x \d x}\\) & \\(u = \cos x\\) & Easy \\
\\(\displaystyle{\int\sec^{2m} x \tan^{2n} x \d x}\\) & \\(u = \tan x\\) & Easy
\\
\\(\displaystyle{\int\sec^{2m+1} x \tan^{2n+1} x \d x}\\) & \\(u = \sec x\\) & Easy \\
\\(\displaystyle{\int\csc^{2m} x \cot^{2n} x \d x}\\) & \\(u = \cot x\\) & Easy
\\
\\(\displaystyle{\int\csc^{2m+1} x \cot^{2n+1} x \d x}\\) & \\(u = \csc x\\) & Easy \\
\\(\displaystyle{\int\sin^{2m} x \cos^{2n} x \d x}\\) & N/A & Difficult
\\
\end{tabular}

<div class="example">
<b>Example:</b>
Evaluate the integral 
\(\)\int \sin^2x\cos^x\d x\(\)


<b>Solution:</b> The first thing to note is that this integral may already be obvious from the section on \(u\)-substitution, but it is good to start with a simple example. The appropriate \(u\)-substitution for this problem is \(u = \sin x\). Then, \(\d u = \cos x \d x\) so the integral can be rewritten as 

$$\begin{align}
\int \sin^2x\cos^x\d x ={}& \int u^2 \d u \\
={}& \frac{1}{3}u^3 + C\\
={}& \frac{1}{3}\sin^3 x + C
\end{align}$$


</div>

Let's now move on to a slightly more difficult example, but again involving sines and cosines. 

<div class="example">
<b>Example:</b>
Evaluate the integral 
\(\)\int \sin^5x\cos^4x\d x\(\)


<b>Solution:</b> This integral is a little bit more complicated, so before employing the \(u\)-substitution we will rewrite the integrand by using the identity \(\sin^2 x = 1-\cos^2 x\):

\(\)\int \sin^5x\cos^4x\d x = \int (1-\cos^2 x)^2\cos^4 x \sin x \d x\(\)

Now it is more obvious that the appropriate \(u\)-substitution here is \(u = \cos x\), so \(\d u = -\sin x \d x\). Thus 

$$\begin{align}
\int \sin^5x\cos^4x\d x ={}& -\int (1-u^2)^2 u^4 \d u \\
={}& -\int (1-2u^2+u^4)u^4 \d u \\
={}& -\int (u^4-2u^6+u^8) \d u \\
={}& -\frac{u^5}{5} + \frac{2u^7}{7} - \frac{u^9}{9} + C \\
={}& -\frac{\cos^5 x}{5} + \frac{2\cos^7x}{7} - \frac{\cos^9x}{9} + C \\
\end{align}$$


</div>

Now that we have seen some examples of solving integrals with powers of sines and cosines in them, let's move on to integrals with tangents and secants. The integrals with tangents and secants are solving in essentially the same way as cotangents and cosecants, so we will only do examples of the former. 


