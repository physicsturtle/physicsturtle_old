---
layout: lesson
title: The OPE
dept: physics
course: many-body-II
unit: unit18
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 18
---
The OPE (operator product expansion) is something we assume a bunch of things to have WHY???

We consider two general right-moving operators \\(\Ahat_R(z^{*})\\) and \\(\Bhat_R(z^{*})\\). These are both analytic functions of \\(z^{*}\\), and we may consider these as the current operator. Assume that we can compute all the multi-point Green functions of \\(A\\), B, and any other operator in the theory. We assume that the operators have the following property:

$$\Ahat_R(z_1^{*})\Bhat_R(z^{*}_2) = \frac{C_R(z_2^{*})}{(z_1^{*}-z_2^{*})^2} + \frac{D_R(z_2^{*})}{z_1^{*} - z_2^{*}} + O(1)$$


This is called an OPE. 

<div class="example">
<b>Example:</b>
Let us look at an example of an OPEs. Consider the product of two current operators:

$$T_\tau [\Jhat_R(z_1^{*})\Jhat_R(z_2^{*})] = T[:\psihat^\dagger_R(z_1^{*}) \psihat_R(z_1^{*}): :\psihat^\dagger_R(z_2^{*}) \psihat_R(z_2^{*}):] $$

We note that the time ordering is always implicit, we we include it for pedagogical purposes. We now consider the following expression expanded with Wick's theorem:

$$\begin{align}
T_\tau[\psihat^\dagger(z_1^{*}) \psihat_(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*})] =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}): + \langle T_\tau[\psihat^\dagger(z_1^{*}) \psihat(z_1^{*})] \rangle :\psihat^\dagger(z_2^{*})\psihat(z_2^{*}): \\
&+ \langle T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_2^{*})] \rangle :\psihat(z_1^{*})\psihat^\dagger(z_2^{*}): + :\psihat^\dagger(z_1^{*}) \psihat(z_2^{*}): \langle T_\tau[\psihat(z_1^{*})\psihat^\dagger(z_2^{*})]\rangle \\
&+ :\psihat^\dagger(z_1^{*}) \psihat(z_1^{*}): \langle T_\tau[\psihat^\dagger(z_2^{*}) \psihat(z_2^{*})]\rangle + \langle T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})] \rangle \langle T_\tau[\psihat^\dagger(z_2^{*}) \psihat(z_2^{*})]\rangle \\
&+ \langle T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_2)] \rangle \langle T_\tau[\psihat(z_1^{*})\psihat^\dagger(z_2^{*})]\rangle 
\end{align}$$

Now we can substitute in \\(\Jhat(z_1^{*}) = :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}):\\) and also \\(\mathcal{G}(z_2^{*};z_1^{*}) = -\langle T_\tau[ \psihat(z_2^{*})\psihat^\dagger(z_1^{*})]\rangle\\). 

$$\begin{align}
T_\tau[\psihat^\dagger(z_1^{*}) \psihat_(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*})] =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}): + \langle T_\tau[\psihat^\dagger(z_1^{*}) \psihat(z_1^{*})] \rangle \Jhat(z_2^{*}) \\
&+ \mathcal{G}(z_2^{*};z_1^{*}) :\psihat(z_1^{*})\psihat^\dagger(z_2^{*}): - :\psihat^\dagger(z_1^{*}) \psihat(z_2^{*}): \mathcal{G}(z_1^{*};z_2^{*})  \\
&+ \Jhat(z_1^{*}) \langle T_\tau[\psihat^\dagger(z_2^{*}) \psihat(z_2^{*})]\rangle + \langle T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})] \rangle \langle T_\tau[\psihat^\dagger(z_2^{*}) \psihat(z_2^{*})]\rangle \\
&- \mathcal{G}(z_2^{*};z_1^{*})\mathcal{G}(z_1^{*};z_2^{*})
\end{align}$$

Now recalling that \\(\Jhat(z_1^{*}) = T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})] - \langle T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})]\rangle\\), we can substitute this in to get 

$$\begin{align}
T_\tau[\psihat^\dagger(z_1^{*}) \psihat_(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*})] =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}): + \langle T_\tau[\psihat^\dagger(z_1^{*}) \psihat(z_1^{*})] \rangle \Jhat(z_2^{*}) \\
&+ \mathcal{G}(z_2^{*};z_1^{*}) :\psihat(z_1^{*})\psihat^\dagger(z_2^{*}): - :\psihat^\dagger(z_1^{*}) \psihat(z_2^{*}): \mathcal{G}(z_1^{*};z_2^{*})  \\
&+ \Jhat(z_1^{*}) \langle T_\tau[\psihat^\dagger(z_2^{*}) \psihat(z_2^{*})]\rangle + (T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})] - \Jhat(z_1^{*}))(T_\tau[\psihat^\dagger(z_2^{*})\psihat(z_2^{*})] - \Jhat(z_2^{*})) \\
&- \mathcal{G}(z_2^{*};z_1^{*})\mathcal{G}(z_1^{*};z_2^{*})
\end{align}$$

Rearranging some terms, 

$$\begin{align}
T_\tau[\psihat^\dagger(z_1^{*}) \psihat_(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*})] =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}): + (\langle T_\tau[\psihat^\dagger(z_1^{*}) \psihat(z_1^{*})] \rangle - T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})) \Jhat(z_2^{*}) \\
&+ \mathcal{G}(z_2^{*};z_1^{*}) :\psihat(z_1^{*})\psihat^\dagger(z_2^{*}): - :\psihat^\dagger(z_1^{*}) \psihat(z_2^{*}): \mathcal{G}(z_1^{*};z_2^{*})  \\
&+ \Jhat(z_1^{*}) (\langle T_\tau[\psihat^\dagger(z_2^{*}) \psihat(z_2^{*})]\rangle - T_\tau[\psihat^\dagger(z_2^{*})\psihat(z_2^{*}))  + T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})] T_\tau[\psihat^\dagger(z_2^{*})\psihat(z_2^{*})]  \\
&+ \Jhat(z_1^{*})\Jhat(z_2^{*}) - \mathcal{G}(z_2^{*};z_1^{*})\mathcal{G}(z_1^{*};z_2^{*})
\end{align}$$

$$\begin{align}
T_\tau[\psihat^\dagger(z_1^{*}) \psihat_(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*})] =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}): - \Jhat(z_1^{*}) \Jhat(z_2^{*}) \\
&+ \mathcal{G}(z_2^{*};z_1^{*}) :\psihat(z_1^{*})\psihat^\dagger(z_2^{*}): - :\psihat^\dagger(z_1^{*}) \psihat(z_2^{*}): \mathcal{G}(z_1^{*};z_2^{*})  \\
&- \Jhat(z_1^{*}) \Jhat(z_2^{*}) + T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})] T_\tau[\psihat^\dagger(z_2^{*})\psihat(z_2^{*})]  \\
&+ \Jhat(z_1^{*})\Jhat(z_2^{*}) - \mathcal{G}(z_2^{*};z_1^{*})\mathcal{G}(z_1^{*};z_2^{*})
\end{align}$$

If we assume that \\(T_\tau[\psihat^\dagger(z_1^{*}) \psihat_(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*})] = T_\tau[\psihat^\dagger(z_1^{*})\psihat(z_1^{*})] T_\tau[\psihat^\dagger(z_2^{*})\psihat(z_2^{*})] \\), then we cancel it out, and move all the current products to the other side:

$$\begin{align}
  \Jhat(z_1^{*})\Jhat(z_2^{*}) =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}):  \\
&+ \mathcal{G}(z_2^{*};z_1^{*}) :\psihat(z_1^{*})\psihat^\dagger(z_2^{*}): - :\psihat^\dagger(z_1^{*}) \psihat(z_2^{*}): \mathcal{G}(z_1^{*};z_2^{*})  \\
&- \mathcal{G}(z_2^{*};z_1^{*})\mathcal{G}(z_1^{*};z_2^{*})
\end{align}$$

Now we set \\(z_{12}^{*} = z_1^{*} - z_2^{*}\\) and assume that \\(z_{12}^{*}\\) is small. We also note that 

$$\mathcal{G}(z_1^{*};z_2^{*}) \sim -\frac{1}{z_{12}^{*}} $$

With this approximation, we find 

$$\begin{align}
  \Jhat(z_1^{*})\Jhat(z_2^{*}) =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}):  \\
&- \frac{1}{z_{12}^{*}}:\psihat^\dagger(z_2^{*}) \psihat(z_2^{*} + z_{12}^{*}): + \frac{1}{z_{12}^{*}} :\psihat^\dagger(z_2^{*} + z_{12}^{*}) \psihat(z_2^{*}): \\
&+ \frac{1}{z_{12}^{*2}}
\end{align}$$

Then Taylor expanding the field operators a little bit, we find 

$$\begin{align}
  \Jhat(z_1^{*})\Jhat(z_2^{*}) =& :\psihat^\dagger(z_1^{*})\psihat(z_1^{*}) \psihat^\dagger(z_2^{*}) \psihat(z_2^{*}): + \frac{1}{z_{12}^{*2}} \\
&- \frac{1}{z_{12}^{*}}:\psihat^\dagger(z_2^{*}) (\psihat(z_2^{*}) + z_{12}^{*} \partial_{z^{*}}\psihat(z_2^{*})): + \frac{1}{z_{12}^{*}} :(\psihat^\dagger(z_2^{*}) + z_{12}^{*}\partial_{z^{*}}\psihat^\dagger(z_2^{*}))\psihat(z_2^{*}): \\
=& \frac{1}{z_{12}^{*2}} +\partial_{z^{*}}\psihat^\dagger(z_2^{*})\psihat(z_2^{*}) - \psihat^\dagger(z_2^{*})\partial_{z^{*}}\psihat(z_2^{*})
\end{align}$$

Where the normal ordered product of the 4 operators goes to zero by the Pauli principle as \\(z_{12}\to 0\\). This is the operator product expansion of the current operators. One important thing to note about the OPE is that, since everything occurs under a time-ordering symbol, the OPEof \\(\Ahat(z+\delta)\Bhat(z)\\) and \\(\Bhat(z)\Ahat(z+\delta)\\) are related. In fact, they are the same if \\(\Ahat\\) and \\(\Bhat\\) are bosonic operators, and you get the negative if they are fermionic operators. 

</div>

