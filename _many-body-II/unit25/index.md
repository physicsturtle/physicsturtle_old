---
layout: lesson
title: March 27 Lecture
dept: physics
course: many-body-II
unit: unit25
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 25
---
\\(\int d^3\textbf{K}_2 \to k_F^2\int dk \int d\theta \sin\theta 2\pi\\)

where \\(2\pi\\) comes from integratin over azimuthal angle of \\(\textbf{K}_2\\) with axis \\(\textbf{K}_1\\), 

$$$$\begin{align}\int d^3\textbf{K}_3 = k_F^2\int dK_3 d\theta_3 \sin\theta_3 d\phi\end{align}$$$$

It is convenient to measure \\(\theta_3\\) from direction of \\(\textbf{K}_1 + \textbf{K}_2\\), \\(\theta_3 =\theta/2\\). 

where \\(\theta\\) is angle between \\(\textbf{K}_1\\) and \\(\textbf{K}_2\\). \\(\int d\theta_3\\) integral is strongly restricted by condition that \\(k_4 < k_1\\).

It is convenient ot change variables \\(d\theta_3\to dk_4\\).

Form figure, \\(\delta k_4 = k_F \sin\theta \delta\theta_3\\), 

$$$$\begin{align}\delta\theta_3 \to \frac{1}{k_F\sin\theta} dk_4\end{align}$$$$

$$$$\begin{align}\frac{1}{\tau} = \frac{1}{(2\pi)^7}\frac{1}{2!}\int_{-k_1}^0 dk_2 \int_0^{k_1} dk_3 \int_0^{k_1}dk_4\delta(V(k_1 + k_2 - k_3 - k_4))\int_0^\pi d\theta \int_0^{2\pi}d\phi \sin\frac{\theta}{2}|F(\theta,\phi)|^2\end{align}$$$$

We may do \\(k\\) integrals exactly, 

$$\begin{align}
\int_{-k_1}^0 dk_2 \int_0^{k_1}dk_3 \int_0^{k_1}dk_4 \delta(V(k_1 + k_2 - k_3 - k_4)) =& \frac{1}{V}\int_{-k_1}^0 dk_2 \int_0^{k_1} dk_3\theta(k_1 + k_2 - k_3) \\
=& \frac{1}{V}\int_{-k_1}^0 dk_2 \int_0^{k_1 + k_2}dk_3 \\
=& \frac{1}{V}\int_{-k_1}^0 dk_2 (k_1 + k_2) \\
=& \frac{1}{2V}k_1^2
\end{align}$$

$$$$\begin{align}
\frac{1}{\tau} = \frac{1}{(2\pi)^7}\frac{\epsilon_1^2}{2Vk_F} \int_0^\pi d\theta \int_0^{2\pi}d\phi \sin\frac{\theta}{2}|F(\theta,\phi)|^2 \propto \epsilon_1^2
\end{align}$$$$

At finite \\(T\\), decay rate is larger because restriction \\(k_2 < 0\\), \\(k_3,k_4 >0\\) are not strictly enfored but instead we get Fermi function

$$$$\begin{align}
n_F(k_2)(1-n_F(k_3))(1-n_F(k_4))
\end{align}$$$$

\\(\epsilon_1^2\to\epsilon_1^2 + (\pi T)^2\\)

\\(\frac{1}{\tau_1}\propto T^2\\) at \\(\epsilon_1\to 0\\)

insert figure here

looks more and more free-electron like as \\(T,\epsilon\to 0\\).

