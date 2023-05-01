---
layout: lesson
title: Determinant formula
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
Consider the expression

$$$$\begin{align}
\int \exp(-\sum_{i,j = 1}^N\bar{\psi}_i M_{ij}\psi_j)\prod_{i=1}^N \d\bar{\psi}_i \d\psi_i .
\end{align}$$$$

In order to evaluate it, we will need to do a Taylor expansion. Which terms in Taylor expansion give a nonzero integral? Well, since \\(\int 1 \d\psi_1 = 0\\), we need all of the Grassmann variables to appear in a product once and only once since the integration measure has all the Grassmann variables once and only once. Since we have \\(N\\) Grassmann variables, this means that we need to take the \\(N\\)th term of the Taylor series. Thus, using an abbreviated notation for the product over Grassmann variables in the integration measure, (we reintroduce it again on the next line)

$$\begin{align}
\int \exp(-\sum_{i,j = 1}^N\bar{\psi}_i M_{ij}\psi_j) \D\bar{\psi}\D\psi =& \frac{(-1)^N}{N!}\int \left(\sum_{i,j = 1}^N\bar{\psi}_i M_{ij}\psi_j \right)^N \D\bar{\psi}\D\psi \\
=& \frac{(-1)^N}{N!}\int \sum_{i_1,j_1,\dots,i_N,j_N=1}^N \bar{\psi}_{i_1}M_{i_1j_1}\psi_{j_1}\cdots \bar{\psi}_{i_N}M_{i_N,j_N}\psi_{j_N} \prod_{i=1}^N \d\bar{\psi}_i \d\psi_i .
\end{align}$$

Numerous terms in the sums are zero. The only nonzero terms are the ones for which \\(i_1,\dots,i_N\\) are all distinct, and also \\(j_1,\dots,j_N\\) are all distinct. Thus, instead of a sum over \\(N^{2N}\\) terms, we will only sum over \\((N!)^2\\) terms. That is, we will sum over \\(S_N\\), the permutation group on \\(N\\) symbols, twice. Sum once for the \\(i\\)s and once for the \\(j\\)s. Thus 

$$\begin{align}
\int \exp(-\sum_{i,j = 1}^N\bar{\psi}_i M_{ij}\psi_j) \D\bar{\psi}\D\psi =& \frac{(-1)^N}{N!}\int \sum_{\substack{(i_1,\dots,j_N)\in S_N \\ (j_1,\dots,j_N)\in S_N}} \bar{\psi}_{i_1}M_{i_1,j_1}\psi_{j_1}\cdots \bar{\psi}_{i_N}M_{i_N,j_N} \psi_{j_N} \prod_{i=1}^N \d\bar{\psi}_i \d\psi_i.
\end{align}$$

Since all the variables are now distinct, it is meaningful to think about rearranging them (not worrying about the expression being zero). We will rearrange them so that all the ``barred" variables are on the left and the ``unbarred" variables are on the right. We need to move \\(\psi_{j_{N-1}}\\) across 1 variable, namely \\(\bar{\psi}_{i_N}\\). Then, we need to move \\(\psi_{j_{N_2}}\\) across 2 variables, namely the combination \\(\bar{\psi}_{i_{N-1}}\bar{\psi_{i_N}}\\). Lastly, the variable \\(\psi_{j_1}\\) needs to be moved across \\(N-1\\) variables. We therefore pick up factors of \\((-1)^1(-1)^2\cdots(-1)^{N-1} = (-1)^{1+2+\cdots + N-1}\\). The sum in the exponent is \\((N-1)N/2\\). 

$$\begin{align}
\int \exp(-\sum_{i,j = 1}^N\bar{\psi}_i M_{ij}\psi_j) \D\bar{\psi}\D\psi =& \frac{(-1)^N}{N!}\int \sum_{\substack{(i_1,\dots,j_N)\in S_N \\ (j_1,\dots,j_N)\in S_N}} \bar{\psi}_{i_1}\cdots \bar{\psi}_{i_N} (M_{i_1j_1}\cdots M_{i_N,j_N})\psi_{j_1}\cdots\psi_{j_N} \prod_{i=1}^N \d\bar{\psi}_i \d\psi_i.
\end{align}$$

Consider the \\(N=2\\) case. 

$$$$\begin{align}\sum_{i,j,k,\ell = 1}^2\int \bar{\psi}_i M_{ij} \psi_j \bar{\psi}_k M_{k\ell}\psi_\ell \d\bar{\psi}_1 \d\psi_1 \d\bar{\psi}_2 \d\psi_2\end{align}$$$$

Only two nonzero terms, each occurring twice. 

$$\begin{align}2M_{11}M_{22}\int\bar{\psi}_1 \psi_1 \bar{\psi}_2\psi_2 \d\bar{\psi}_1 \d\psi_1 \d\bar{\psi}_2 \d\psi_2 + 2M_{12}M_{21}\int \bar{\psi}_1\psi_2 \bar{\psi}_2 \psi_1 \d\bar{\psi}_1 \d\psi_1 \d\bar{\psi}_2 \d\psi_2 =& 2(M_{11}M_{22} - M_{12}M_{21}) \\
=& 2\det M
\end{align}$$

so that

$$$$\begin{align}\int\exp(-\bar{\psi}M\psi) \D\bar{\psi} \D\psi = \det M\end{align}$$$$

for \\(N=2\\). Generalize to arbitrary \\(N\\) using

$$$$\begin{align}\int\exp(-\bar{\psi} M\psi) \D\bar{\psi} \D\psi = \frac{1}{N!}\sum_{i_1,\dots,i_N}\sum_{i_1,\dots,j_N} M_{i_1j_1}M_{i_2j_2}\dots M_{i_N j_N}\epsilon_{i_1,\dots i_N}\epsilon_{j_1,\dots j_N}\end{align}$$$$

where \\(\epsilon_{i_1,\dots,i_N} = \sgn(i_1,\dots,i_N)\\) for \\(\{i_1,\dots,i_N\}\\) a permutation of \\(\{1,\dots,N\}\\). Thus this equals 

$$$$\begin{align}\frac{1}{N!}\sum_{i_1,\dots,i_N}\sum_{i_1,\dots,j_N} M_{i_1j_1}M_{i_2j_2}\dots M_{i_N j_N}\epsilon_{i_1,\dots i_N}\epsilon_{j_1,\dots j_N} = \sum_{j_1,\dots,j_N} \epsilon_{j_1,\dots,j_N} M_{1,j_1}\dots M_{N,j_N} = \det M\end{align}$$$$

This is the opposite of ordering integral

$$$$\begin{align}\int\exp(-z^{*} M z)\D z^{*} \D z = (\det M)^{-1}\end{align}$$$$

as we see by making a unitary transformation to diagonalize \\(M\\) (assume \\(M\\) is Hermitian and positive definite). Given

$$$$\begin{align}\prod_{i=1}^N \frac{1}{\lambda_i} = \frac{1}{\det M}\end{align}$$$$

now resolution of identity is

$$$$\begin{align}I = \int\ket{\bar{\psi}_1,\dots,\bar{\psi}_N}\bra{\psi_1,\dots,\psi_N}e^{-\sum\bar{\psi}_i\psi}\prod d\bar{\psi}_i d\psi_i\end{align}$$$$

This usually follows from factorization

$$$$\begin{align}\ket{\bar{\psi}_1,\dots,\bar{\psi}_N}\bra{\psi_1,\dots,\psi_N} = \ket{\bar{\psi}_1}\ket{\psi_1}\otimes \ket{\bar{\psi}_2}\bra{\psi_2}\otimes\cdots\otimes\ket{\bar{\psi}_N}\bra{\psi_N}\end{align}$$$$

$$$$\begin{align}e^{-\sum\bar{\psi}_i\psi_i} = \prod_i e^{-\bar{\psi}_i\psi_i}\end{align}$$$$

and using the fact that a \textbf{pair} of Grassmann numbers commutes with everything. 


