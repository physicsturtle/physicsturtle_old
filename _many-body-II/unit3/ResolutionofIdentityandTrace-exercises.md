---
layout: lesson
title: Resolution of Identity and Trace - Exercises
dept: physics
course: many-body-II
unit: unit3
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 3
---
<ol>
\question Consider the case where there are two occupiable states. Then, the identity is given by 

$$\1 = \ket{0,0}\bra{0,0} + \ket{1,0}\bra{1,0} + \ket{0,1}\bra{0,1} + \ket{1,1}\bra{1,1}.$$

Show, by direct computation, that 

<ol type="a">
</li> 
 <li> 
$$\1 = \int \ket{\eta_1,\eta_2}\bra{\bar{\eta}_1,\bar{\eta}_2} e^{-\bar{\eta}_1\eta_1 - \bar{\eta}_2\eta_2} \d\bar{\eta}_1 \d\eta_1 \d\bar{\eta}_2 \d\eta_2$$
</li> 
 <li> Propose a generalization for \\(N\\) occupiable states
\end{parts}

\begin{solution}
<ol type="a">
</li> 
 <li>  $$\begin{align}
\1 =& \int \ket{\eta_1,\eta_2}\bra{\bar{\eta}_1,\bar{\eta}_2} e^{-\bar{\eta}_1\eta_1 - \bar{\eta}_2\eta_2} \d\bar{\eta}_1 \d\eta_1 \d\bar{\eta}_2 \d\eta_2 \\
=& \int \ket{\eta_1}\otimes\ket{\eta_2}\bra{\bar{\eta}_1}\otimes\bra{\bar{\eta}_2} (1-\bar{\eta}_1\eta_1)e^{-\bar{\eta}_2\eta_2} \d\bar{\eta}_1 \d\eta_1 \d\bar{\eta}_2 \d\eta_2 \\
=& \int (\ket{0} - \eta_1\ket{1})\otimes\ket{\eta_2} (\bra{0} - \bra{1}\bar{\eta}_1) \otimes\bra{\bar{\eta}_2} (1-\bar{\eta}_1\eta_1)e^{-\bar{\eta}_2\eta_2} \d\bar{\eta}_1 \d\eta_1 \d\bar{\eta}_2 \d\eta_2 \\
=& \int\left(\ket{0}\ket{\eta_2} \bra{0}\bra{\bar{\eta}_2} - \eta_1\ket{1} \ket{\eta_2}\bra{0}\bra{\bar{\eta}_2} - \ket{0} \ket{\eta_2} \bra{1}\bar{\eta}_1\bra{\bar{\eta}_2} + \eta_1\ket{1}\ket{\eta_2} \bra{1}\bar{\eta}_1 \bra{\bar{\eta}_2} \right)(1-\bar{\eta}_1\eta_1)\d\bar{\eta}_1\d\eta_1 e^{-\bar{\eta}_2\eta_2}\d\bar{\eta}_2\d\eta_2 \\
=& \int -\ket{0}\ket{\eta_2}\bra{0}\bra{\eta_2}\bar{\eta}_1\eta_1 \d\bar{\eta_1}\d\eta_1 e^{-\bar{\eta}_2\eta_2} \d\bar{\eta_2}\d\eta_2 + \int\eta_1\ket{1}\ket{\eta_2}\bra{1}\bar{\eta}_1\bra{\bar{\eta}_2} \d\bar{\eta}_1\d\eta_1 e^{-\bar{\eta}_2\eta_2} \d\bar{\eta}_2\d\eta_2 \\
=& \int \ket{0}\ket{\eta_2} \bra{0} \bra{\bar{\eta}_2} e^{-\bar{\eta}_2 \eta_2} \d\bar{\eta}_2 \d\eta_2 + \int \ket{1} \ket{\eta_2} \bra{1} \bra{\bar{\eta}_2} e^{-\bar{\eta}_2\eta_2} \d\bar{\eta}_2 \d\eta_2 \\
=& (\ket{0}\bra{0} + \ket{1}\bra{1}) \int\ket{\eta_2} \bra{\bar{\eta}_2} e^{-\bar{\eta}_2 \eta_2} \d\bar{\eta}_2 \d\eta_2 \\
=& (\ket{0}\bra{0} + \ket{1}\bra{1}) (\ket{0}\bra{0} + \ket{1}\bra{1}) \\
=& \ket{0,0}\bra{0,0} + \ket{1,0}\bra{1,0} + \ket{0,1}\bra{0,1} + \ket{1,1}\bra{1,1}
\end{align}$$

Thus, it works out! 

</li> 
 <li> Thus, we have 

$$\1 = \int e^{-\sum_{i\sigma} \bar{\eta}_{i\sigma} \eta_{i\sigma}} \prod_{i\sigma} \d\bar{\eta}_{i\sigma} \d\eta_{i\sigma}$$

\end{parts}

\end{solution}

\end{questions}

