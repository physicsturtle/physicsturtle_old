---
layout: lesson
title: Feynman Diagrams for Interacting Fermions: the Jellium Model
dept: physics
course: many-body-II
unit: unit6
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 6
---
The free electron model is quite successful in predicting certain qualitative features of metals. For example, the linear specific heat capacity is correctly predicted by this model. Another feature which is predicted by the 


In this section, we will develop the theory of the interacting electron gas in the path integral formalism. The Hamiltonian we are dealing with has a free part:

$$\Hhat_0 = -\frac{\hbar^2}{2m}\sum_\sigma \int \psihat_\sigma^\dagger(\r) \nabla^2 \psihat_\sigma(\r) \d\r $$

and a Coulomb interaction

$$\Hhat_\text{int} = \frac{1}{2}\sum_{\sigma_1\sigma_2}\int \psihat_{\sigma_1}^\dagger(\r_1) \psihat_{\sigma_2}^\dagger(\r_2) \frac{e^2}{4\pi\epsilon_0|\r_1-\r_2|}\psihat_{\sigma_2}(\r_2) \psihat_{\sigma_1}(\r_1) \d\r_1\d\r_2$$

If we assume that the system is in a box of volume \\(\V\\), then the Fourier transform of the electron field operators is 

$$\psihat_\sigma(\r) = \frac{1}{\sqrt{\V}}\sum_{\k} e^{i\k\cdot\r} \psihat_\sigma(\k) $$

where \\(\k\\) is an unbounded but discrete variable with values determined by the size of the box. The inverse Fourier transform is 

$$\psihat_\sigma(\k) = \frac{1}{\sqrt{\V}} \int e^{-i\k\cdot\r} \psihat_\sigma(\r) \d\r$$

If we write the Hamiltonian in terms of the Fourier transformed operators, and also employ atomic units where \\(4\pi\epsilon_0 = 1\\), we get 

$$\Hhat_0 = \sum_{\k\sigma} \epsilon(\k)\psihat^\dagger_{\k\sigma} \psihat_{\k\sigma} $$

where \\(\epsilon_{\k} = \hbar^2\k^2/2m\\), and the interaction is (defining \\(V(\q) = 4\pi e^2/\q^2\\))

$$\Hhat_\text{int} = \frac{1}{2\V} \sum_{\k\p\q\sigma_1\sigma_2} V(\q) \psihat^\dagger_{\k+\q,\sigma_1} \psihat^\dagger_{\p-\q,\sigma_2} \psihat_{\p\sigma_2} \psihat_{\k\sigma_1} $$

We can now write the action for this theory; note that we have done the Fourier transform in space for the Berry term

$$S = \int_0^\beta \left(\sum_{\k\sigma}\bar{\psi}_{\k\tau\sigma}(\partial_\tau + \xi_{\k})\psi_{\k\tau\sigma} + \frac{1}{2\V} \sum_{\k\p\q\sigma_1\sigma_2} V(\q) \bar{\psi}_{\k+\q,\tau\sigma_1} \bar{\psi}_{\p-\q,\tau\sigma_2} \psi_{\p\tau\sigma_2} \psi_{\k\tau\sigma_1} \right) \d\tau$$

If we Fourier transform to Matsubara frequencies, we finally have the action in the most convenient form:

$$S_0 = \sum_{k\sigma} (-ik_0 + \xi_{\k}) \bar{\psi}_{k\sigma} \psi_{k\sigma}$$

$$S_\text{int} = \frac{1}{2\V\beta} \sum_{kpq\sigma_1\sigma_2} V(\q) \bar{\psi}_{k+q,\sigma_1} \bar{\psi}_{p-q,\sigma_2} \psi_{p\sigma_2} \psi_{k\sigma_1}$$

The goal of this section is to develop an approximation scheme for the single particle Green function. We will also develop an approximation for the effective vertex between electrons. 

