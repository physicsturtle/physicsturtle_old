---
layout: lesson
title: The Kondo Impurity Model
dept: physics
course: many-body-II
unit: unit13
deptDisplay: Physics
courseDisplay: Many Body Physics II
unitDisplay: Unit 13
---
The Kondo model describes otherwise free conduction electrons in the presence of  a single magnetic impurity at the origin \\(\r =0\\). This model is also appropriate multiple magnetic impurities in a metal, but only if they are sufficiently dilute, around \\(n = 10^{-6}\\). This is because they are almost isolated if they are very dilute. For example, the material \\(U_{1-x}Fe_x\\), with \\(x\ll 1\\) exhibits the Kondo effect. The Kondo model can also be used to describe a quantum dot (produced by gating a semiconductor heterostructure) with an odd number of electrons (and hence a net spin) interacting with conduction electrons in the heterostructure. 

Extensions of the Kondo effect include the possibility of including numerous orbitals of conduction electrons to interact with a single magnetic impurity, or even replacing the dipolar impurity with a multipolar analogue. Furthermore, there is a more complicated problem, known as the Kondo lattice problem, in which there is a lattice of magnetic impurities. 

We will construct a model describing the magnetic impurity in the metallic host by starting with a model of free conduction electrons. The free electron model may come from a tight-binding model. We will add to this an on-site interaction between these conduction electrons and the dipole moment. The interaction will be antiferromagnetic; the conduction electron on the impurity site will prefer to anti-align with the impurity spin. The interaction is antiferromagnetic because virtual hopping events are allowed when there is antialignment, but there are no virtual events if they are aligned because of the Pauli exclusion principle. 

An ingredient you may expect in the model would be electron-electron interactions. In fact, we will hope that we can ignore the electron-electron interactions on the basis of Fermi liquid theory. Our conduction electron operators can be thought of as quasiparticle operators if this comforts you. The Kondo interaction actually turns out to create a distinct type of Fermi liquid, called a local Fermi liquid, which further renormalizes the electronic quasiparticles. 

The local Fermi liquid picture however only becomes applicable at low temperatures. By low temperatures, we mean some \\(T\\) such that \\(T \ll T_K\ll E_F\\) as we shall see. The temperature scale \\(T_K\\) is the \textit{Kondo temperature}, and we will derive an expression for it in this section. 

The Kondo model was developed and studied to explain a remarkable experimental observation going back several decades. The observation is that some metals have a resistivity that increases as \\(T\\) is lowered, at low \\(T\\). This is unusual, because for most metals, the resistivity decreases down to zero as \\(T\\) is lowered. Note that in reality, the resistivity in most metals would actually approach a constant due to electric monopole impurity scattering; only in a truly perfect lattice would the resistivity decrease to zero as \\(T\\) is lowered.

%The kondo model was initially developed to describe the behaviour of impurities of transition metal ions, e.g. Mg inside of a normal metal e.g. Cu. The impurity ion acquires a local magnetic moment, which interacts nontrivially with the host (Cu) conduction electrons. In many cases, we have seen that strong interactions don't do much in metals, apart from renormalizint hte effective mass, and the residue of the quasiparticle excitations. This continues to be true in the Kondo model, but strong renormalizations occur in an interesting manner. 
