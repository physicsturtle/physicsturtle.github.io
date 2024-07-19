---
layout: page
title: Calculating Residues
course: test
unit: unit1
permalink: /test/calculating-residues
---

Calculating residues in complex analysis is very useful for a variety of applications, from purely mathematical purposes to integrals from physics. Here let's discuss a few tricks. 

We expand a function \\(f : \mathbb{C}\to\mathbb{C}\\) in a Laurent series

$$ f(z) = \sum_{n = -\infty}^{\infty} a_n(z-z_0)^n$$

the coefficient \\(a_{-1}\\) is known as the *residue of \\(f\\) at \\(z_0\\)*.

$$\text{Res}(f,z_0) = a_{-1}$$

Depending on what kind of pole \\(z_0\\) is, there are different tricks for calculating the residue. 

If \\(z_0\\) is a simple pole (pole of order 1), then 

$$\text{Res}(f,z_0) = \lim_{z\to z_0}f(z)(z-z_0)$$ 

If \\(z_0\\) is a pole of order \\(k\\), then 

$$\text{Res}(f,z_0) = \frac{1}{(k-1)!}\left.\frac{d^{k-1}}{dz^{k-1}} f(z)(z-z_0)^{k}\right|_{z=z_0}$$ 