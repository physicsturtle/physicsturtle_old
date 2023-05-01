---
layout: lesson
title: Bose Hubbard Model
dept: physics
course: many-body-II
unit: unit8
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 8
---

In this section, we will consider the Hubbard model for spinless bosons, which is given by 

$$\Hhat = -t\sum_{\left<i,j\right>} \bhat^\dagger_{i}\bhat_{j} + U\sum_i \frac{\nhat_i(\nhat_i-1)}{2}.$$

An example of a spinless boson is helium-4. This is because the nucleus has net spin 0, and the two electrons also cancel out to make net spin 0. The on-site repulsion is between all particles. If there are \\(\nhat_i\\) particles at site \\(i\\), then there is a repulsion \\(U\\) between all \\(\nhat_i\\). The number of ways to pick two particles is \\(\binom{\nhat_i}{2} = \frac{\nhat_i(\nhat_i-1)}{2}\\). That is the origin of that term. By using the canonical commutation relation

$$[\bhat_i,\bhat_j^\dagger] = \delta_{ij}$$

we can rewrite the model as 

$$\Hhat = -t\sum_{\left<i,j\right>} \bhat^\dagger_{i}\bhat_{j} + \frac{U}{2} \sum_i \bhat^\dagger_i \bhat^\dagger_i \bhat_i \bhat_i.$$

In the grand canonical ensemble, we have 

$$\Hhat = -t\sum_{\left<i,j\right>} \bhat^\dagger_{i}\bhat_{j} + \frac{U}{2} \sum_i \bhat^\dagger_i \bhat^\dagger_i \bhat_i \bhat_i - \mu\sum_i \nhat_i.$$

In two limits, the model is easy to solve. In the case \\(U = 0\\), we get delocalized states:

$$H_0 = \sum_{\k} (\epsilon_{\k} - \mu)\bhat^\dagger_{\k} \bhat_{\k}$$

In this case, for \\(T < T_\text{BEC}\\), the bosons will condense at \\(\k = 0\\). When interactions are turned on, new quasiparticles emerge. In the other case \\(t = 0\\), we have a model that gives localized states:

$$H_\text{int} = \sum_i \left(\frac{U}{2}\nhat_i(\nhat_i-1) - \mu\nhat_i\right) = \sum_i E(\nhat_i)$$

To find the ground state of \\(H_\text{int}\\), we can minimize each \\(E(\nhat_i)\\) individually, since the sites are decoupled. We take the discrete derivative:

$$E(\nhat_i+1) - E(\nhat_i) = U\nhat_i - \mu = \Delta E^+$$
$$E(\nhat_i - 1) - E(\nhat_i) = -U(\nhat_i - 1) + \mu = \Delta E^-.$$

For a minimum, we require that \\(\Delta E^\pm > 0\\)

This tells us that \\(U\nhat_i - \mu > 0\\) and that \\(-U\nhat_i + U + \mu > 0\\) so that \\(\nhat_i > \mu/U\\) and \\(\nhat_i < 1 + \mu/U\\), so we need to pick the integer in this range. Thus \\(\partial n/\partial\mu = 0\\) so it is incompressible (equivalent to being gapped). When the hopping is turned on, the regimes of \\(\mu\\) where \\(\nhat_i\\) jumps will be able to support delocalized bosons. Between the Mott insulator plateaus are windows of Bose Einstein condensate. We posit the phase diagram as ....

