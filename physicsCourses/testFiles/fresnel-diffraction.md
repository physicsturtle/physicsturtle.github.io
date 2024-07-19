---
layout: page
title: Fresnel Diffraction
course: test
permalink: /test/fresnel-diffraction/
---

The formula that we derived in the Fraunhofer case for the electric field due to a mask with mask function $f(x,y)$ was 

$$E = \int_{-\infty}^\infty\int_{-\infty}^\infty \frac{E_0 e^{ikr}{4\pi r}}f(x'y') dx'dy'$$

The distance 

$$r = \sqrt{z^2 + (x-x')^2 + (y-y')^2} = z\sqrt{1+\frac{(x-x')^2 + (y-y')^2}{z^2}}$$

can be approximated in the case that $\frac{(x-x')^2 + (y-y')^2}{z^2} \ll 1$, which leads to 

$$r \approx z + \frac{(x-x')^2 + (y-y')^2}{2z}$$

If we plug this into the formula for the electric field, at leading order we get 

$$E\sim \frac{E_0 e^{ikz}}{4\pi\sqrt{x^2+y^2+z^2}} \int_{-\infty}^\infty\int_{-\infty}^\infty \exp\left(ik\frac{(x-x')^2+ (y-y')^2}{2z}\right) f(x',y') dx'dy'$$

which is the Fresnel diffraction formula. If the mask is independent of $y$, then this simplifies to 

$$E\sim \frac{E_0e^{ikz}}{4\pi \sqrt{x^2+y^2+z^2}}\int_{-\infty}^\infty e^{ik(x-x')^2/2z}f(x')dx'$$








