---
layout: lesson
title: Appendix
dept: physics
course: many-body-II
unit: unit35
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 35
---
Since \\(V' = V(b) = V(1+\ell) = V + \ell \frac{\d V}{\d\ell}\\), we find 

$$\frac{\d V}{\d \ell} = - \Pi = -\frac{1}{8\pi^2}\int V(\theta-\theta_3)V(\theta_1-\theta)\d\theta$$

Then, we can write in terms of a Fourier transform:

$$V(\theta) = \sum_m e^{im\theta} v_m$$

which gives the flow equation

$$\frac{\d v_m}{\d\ell} = -\frac{v_m^2}{4\pi}$$

We see that the couplings always flow to smaller values. If \\(v_m > 0\\), then it flows to zero. If \\(v_m < 0\\), it flower to minus infinity. This is the BCS instability! Thus we have two results. The result for \\(F\\) is that there is a renormalization of the band structure, but that the interaction is marginal. 

