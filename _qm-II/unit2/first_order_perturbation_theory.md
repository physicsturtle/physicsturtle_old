---
layout: page
title: First Order Perturbation Theory
dept: physics
course: qm-II
unit: unit2
deptDisplay: Physics
courseDisplay: Quantum Mechanics II
unitDisplay: Unit 2
---

In this section, we will discuss the first order perturbation theory. 

Consider the Schrödinger equation for a Hamiltonian $\hat{H}^0$ with known eigenvalues $\\{E^0_n\\}$ and corresponding eigenvectors $\\{\left\|\psi_n\right>\\}$. Thus, they satisfy the equation

$$\hat{H}^0 \left| \psi^0_n\right>  = E^0_n \left| \psi^0_n \right>.$$

In this section, we assume that the eigenvalues are nondegenerate; so there is one and only one eigenstate for each eigenvalue. We then look for how these energy eigenvalues and their states change when we change the Hamiltonian to $\hat{H} = \hat{H}^0 + \lambda \hat{H}'$. 

<div class = "remark">
Remark: Note that when we do perturbation theory in quantum mechanics, we usually have that $\hat{H}'$ is a small Hamiltonian, and ramp the parameter $\lambda$ up to 1 at the end. So, $\lambda$ is used more as a bookkeeping device. In mathematics courses on asymptotic analysis/perturbation theory, one usually keeps $\lambda$ as a small parameter throughout the entire problem. 
</div>

We define power series in $\lambda$ to approximately satisfy the equation for the full Hamiltonian

$$\hat{H} \left| \psi_n\right>  = E_n \left| \psi_n \right>. $$

The power series are

$$E_n = \sum_{\ell=0}^\infty \lambda^\ell E^\ell_n$$

$$\left|\psi_n\right> = \sum_{k=0}^\infty \lambda^k \left|\psi_n^k\right>$$

where the notation $E^\ell_n$ means the $k$th correction to the $n$th eigenvalue, and the notation $\left\|\psi_n^k\right>$ means the $k$th correction to the $n$th eigenfunction. Let's plug these power series representations into the Schrödinger equation. 

### Corrections to the Energy Eigenvalues

$$(\hat{H}^0 + \lambda\hat{H}') \sum_{k=0}^\infty \lambda^k \left|\psi_n^k\right> = \sum_{\ell=0}^\infty \lambda^\ell E^\ell_n \sum_{k=0}^\infty \lambda^k \left|\psi_n^k\right>$$

Let's now collect terms at zeroth and first order. At zeroth order, we simply recover the unperturbed problem! 

$$O(1):\quad  \hat{H}^0 \left| \psi_n^0\right> = E^0_n \left| \psi_n^0\right>  $$

At first order, we have the equation 

$$O(\lambda): \quad \hat{H}^0 \left| \psi^1_n\right> + \hat{H}' \left|\psi^0_n\right> = E^1_n\left|\psi^0_n\right> + E^0_n\left|\psi^1_n\right>$$

Now, let's act on the left with the bra $\left<\psi^0_n\right\|$. 

$$\left<\psi^0_n\right|\hat{H}^0 \left| \psi^1_n\right> + \left<\psi^0_n\right|\hat{H}' \left|\psi^0_n\right> = \left<\psi^0_n\right|E^1_n\left|\psi^0_n\right> + \left<\psi^0_n\right|E^0_n\left|\psi^1_n\right>$$

Since the Hamiltonian $\hat{H}^0$ is Hermitian, we can think of it as acting from the right on the bra $\left<\psi^0_n\right\|$, which means that 

$$\left<\psi^0_n\right|\hat{H}^0 \left| \psi^1_n\right> = \left<\psi^0_n\right|E^0_n\left|\psi^1_n\right>$$

Thus, the equation simplifies to 

$$\left<\psi^0_n\right|\hat{H}' \left|\psi^0_n\right> =E^1_n \left<\psi^0_n\right| \left|\psi^0_n\right>$$

Since the states $\{\left\|\psi^0_n\right>\}$ are normalized, we simply get 

<div class="result">
Result: The first order correction to the $n$th eigenstate due to a perturbation Hamiltonian $\hat{H}'$ is

$$E^1_n = \left<\psi^0_n\right|\hat{H}' \left|\psi^0_n\right>$$

</div>

Thus we have the first order corrections to the energies. Now, let's find the first order corrections to the eigenfunctions. 


### Corrections to the Eigenstates
To find the corrections to the eigenstates, let's return to the $O(\lambda)$ equation before we acted on it with the bra. 

$$\hat{H}^0 \left| \psi^1_n\right> + \hat{H}' \left|\psi^0_n\right> = E^1_n\left|\psi^0_n\right> + E^0_n\left|\psi^1_n\right>$$

Let's rearrange it slightly 

$$(\hat{H}^0 - E^0_n)\left|\psi^1_n\right> = (E^1_n - \hat{H}')\left|\psi^0_n\right>$$

Now, let's expand the ket $\left\|\psi^1_n\right>$ in terms of the basis $\\{\left\|\psi^0_n\right>\\}$:

$$\left|\psi^1_n\right> = \sum_{m\neq n} c_{mn}\left|\psi^0_m\right> $$

now, all we need to do is find the coefficients $c_{mn}$. Note that the sum does not include $m=n$ because $(\hat{H}^0 - E^0_n)\left\|\psi^0_n\right> = 0$ anyways. Plugging this representation in, 

$$(\hat{H}^0 - E^0_n)\sum_{m\neq n} c_{mn}\left|\psi^0_m\right> = (E^1_n - \hat{H}')\left|\psi^0_n\right>$$

To isolate the constants $c_{mn}$, act with the bra $\left<\psi^0_p\right\|$ (where $p\neq n$) on both sides. 

$$\left<\psi^0_p\right|(\hat{H}^0 - E^0_n)\sum_{m\neq n} c_{mn}\left|\psi^0_m\right> = \left<\psi^0_p\right|(E^1_n - \hat{H}')\left|\psi^0_n\right>$$

Let's simplify this to 

$$\sum_{m\neq n} \left<\psi^0_p\right|(\hat{H}^0 - E^0_n) c_{mn}\left|\psi^0_m\right> = \left<\psi^0_p\right|E^1_n\left|\psi^0_n\right> -  \left<\psi^0_p\right| \hat{H}'\left|\psi^0_n\right>$$

Since $\left<\psi^0_p\right\|\hat{H}^0 = \left<\psi^0_p\right\|E^0_p$, this simplifies to 

$$\sum_{m\neq n} \left<\psi^0_p\right|(E^0_p - E^0_n) c_{mn}\left|\psi^0_m\right> = -  \left<\psi^0_p\right| \hat{H}'\left|\psi^0_n\right>$$

Finally, we get 

$$\sum_{m\neq n}(E^0_p - E^0_n) c_{mn}\delta_{pm}  = -  \left<\psi^0_p\right| \hat{H}'\left|\psi^0_n\right>$$

which, because of the Kronecker delta, simplifies to 

$$(E^0_p - E^0_n) c_{pn}  = -  \left<\psi^0_p\right| \hat{H}'\left|\psi^0_n\right>$$

Relabelling $p$ back to $n$ and solving for $c_{mn}$, we find 

$$c_{mn} = \frac{\left<\psi^0_m\right|\hat{H}'\left|\psi^0_n\right>}{E^0_n - E^0_m}$$

Now that we have the expansion coefficients, we get

\left|\psi^1_n\right> = \sum_{m\neq n} \frac{\left<\psi^0_m\right|\hat{H}'\left|\psi^0_n\right>}{E^0_n - E^0_m}\left|\psi^0_m\right> 

and it is at this point we note that it is important that the energy eigenvalues were nondegenerate. If they were, we would have a division by zero! 












