# Methods of Molecular Quantum Mechanics

Molecular stationary states are determined by time-independent Schrödinger equation (SE). 
$$H \Psi(\boldsymbol{x_{1}},\boldsymbol{x_{2}},\cdots, \boldsymbol{x_{N}}) = E \Psi(\boldsymbol{x_{1}},\boldsymbol{x_{2}},\cdots,\boldsymbol{x_{N}})$$
where bold letter $\boldsymbol{x_{i}}$ collectively symbolizes particle $i$'s coordinates $(x_{i},y_{i},z_{i})$ and spin variable $\alpha$ or $\beta$. 
When $\Psi$ is normalized, $|\Psi|^{2}$ has the physical interpretation that $|\Psi|^{2}\mathrm{d}\boldsymbol{x_{1}}\mathrm{d}\boldsymbol{x_{2}}\cdots \mathrm{d}\boldsymbol{x_{N}}$ equals the probability of finding electrons $1,2,\cdots,N$ simultaneously in volume elements $\mathrm{d}\boldsymbol{x_{1}}\times\mathrm{d}\boldsymbol{x_{2}}\times\cdots\times\mathrm{d}\boldsymbol{x_{N}}$. [[Probability Construction of Quantum Mechanics]]
Any experimental observation is performed on a **macroscopic aggregate of molecules**, not a single molecule, and the interaction between molecules and environment will also disturb the observation. Therefore, we may not be able to describe **real chemical reactions** which include collision and scattering processes, and gas, liquid or solid phase; even in molecular level, such processes are time-dependent (TD) and require TD SE:
$$H \Psi = \mathrm{i}\hbar \frac{ \partial \Psi }{ \partial t }$$
However, **the radiation field**, including transitions from one state to another, and properties of **individual molecular states** can be accurately obtained from observation.

### Example: Helium Atom

Consider Helium-like atom,
$$H(1,2) = h(1)+h(2)+g(1,2)$$
where 
$$\begin{aligned}
h(i) &= - \frac{1}{2}\nabla^{2}(i) - \frac{Z}{r_{i}}\\
g(1,2) &= \frac{1}{r_{12}}
\end{aligned}$$
##### First approximation

^533af6

Model non-interacting system
$$H_{0}(1,2) = h(1)+h(2)$$
By variable separation we reduce the problem to one-electron eigenvalue problem.
$$h \phi_{i} = \epsilon \phi_{i}, i\in \{1,2\} $$
[[Atomic Orbitals]]
And total energy $E = \epsilon_{1}+\epsilon_{2}$, where $\epsilon_{i}$ are called orbital energies. 
Then construct the simultaneous eigenstate $\Phi(r_{1},r_{2}) = \phi_{1}(r_{1})\phi_{2}(r_{2})$, which satisfies both 
$$\begin{aligned}
h(1)\Phi(r_{1},r_{2}) &= \epsilon_{1}\Phi(r_{1},r_{2})\\
h(2)\Phi(r_{1},r_{2}) &= \epsilon_{2}\Phi(r_{1},r_{2})
\end{aligned} $$
Therefore,
$$H_{0}\Phi(r_{1},r_{2}) = (\epsilon_{1}+\epsilon_{2})\Phi(r_{1},r_{2}) $$
This approach can be generalized for any number of electrons with neglecting interaction term $g$. Therefore, in non-interacting case, we only need to solve for one-electron problem, and taking a product of one-electron eigenfunctions, we get the final solution $\Phi(r_{1},r_{2},\cdots,r_{N})$. Noted that even we introduce interaction term $g$, the product function form can still be used to describe and classify the **possible electronic states** of the many-electron system.
And the independent-particle model (IPM) can be refined to Hartree-Fock method by introducing interaction in an average potential way. 
A product function 
$$\Phi(r_{1},r_{2},\cdots,r_{N}) = \phi_{1}(r_{1})\phi_{2}(r_{2})\cdots \phi_{N}(r_{N})$$
provides a specification of orbitals $\phi_{1},\phi_{2},\cdots,\phi_{N}$ to $N$ electrons. The solutions of SE[[Atomic Orbitals#^6702b9]] form an infinite set $\phi_{1},\phi_{2},\cdots$, and the orbitals appearing in product functions $\Phi(r_{1},r_{2},\cdots,r_{N})$ are said to be occupied, all others being unoccupied. 
In the Helium example, with no interaction, the occupied AOs may both be 1s, or may be 1s the other 2s, or may even include 2p, 3s... orbitals. Here we only consider the first two cases, where the corresponding wavefunctions and energies being 
$$\begin{aligned}
\Phi_{1}(r_{1},r_{2}) &= \text{1s}(r_{1})\text{1s}(r_{2}), E_{1} = 2\epsilon_{\text{1s}}\\
\Phi_{2}(r_{1},r_{2}) &= \text{1s}(r_{1})\text{2s}(r_{2}),E_{2} =\epsilon_{\text{1s}}+\epsilon_{\text{2s}}
\end{aligned}$$
The specification of occupied orbitals defines an **orbital configuration**, which frequently abbreviated by symbols such as $\text{1s}^{2},\text{1s 2s}$, etc. 

##### Symmetry of wavefunction 

Because electrons are indistinguishable, the wavefunction's form has a restriction. Suppose the exact wavefunction $\Psi(r_{1},r_{2})$ equals to $\Phi_{2}(r_{1},r_{2})=\text{1s}(r_{1})\text{2s}(r_{2})$, then $|\Psi(r_{1},r_{2})|^{2}\mathrm{d}r_{1}\mathrm{d}r_{2}$ is the probability of finding two electrons simultaneously in volume elements $\mathrm{d}r_{1}\times \mathrm{d}r_{2}$. 
But if we switch the electrons, the corresponding probability will be $|\Psi(r_{2},r_{1})|^{2}\mathrm{d}r_{1}\mathrm{d}r_{2}$. Since electrons are physically indistinguishable, we should obtain same probability. However in this case 
$$|\Psi(r_{1},r_{2})|^{2} \ne |\Psi(r_{2},r_{1})|^{2}$$
That is, the product function **violates** the indistinguishable requirement. Furthermore, the requirement shows that $\Psi(r_{1},r_{2})$ and $\Psi(r_{2},r_{1})$ should differ at most by a phase $e^{\mathrm{i}\theta}$. [[From group theory we know]] that the only distinct possibilities need to be considered are $\pm 1$, which corresponding to symmetric and antisymmetric cases. 
$$\begin{aligned}
\Psi(r_{2},r_{1}) &= \Psi(r_{1},r_{2}) \quad \text{(symmetric wavefunction)}\\
\Psi(r_{2},r_{1}) &= -\Psi(r_{1},r_{2}) \quad \text{(antisymmetric wavefunction)}
\end{aligned}$$
Generally, we have 
$$\begin{aligned}
\hat{P}\Psi(r_{1},r_{2},\cdots,r_{N}) &= \Psi(r_{1},r_{2},\cdots,r_{N}) \quad \text{(symmetric wavefunction)}\\
\hat{P}\Psi(r_{1},r_{2},\cdots,r_{N}) &= (-1)^{\tau_{\hat{P}}}\Psi(r_{1},r_{2},\cdots,r_{N}) \quad \text{(antisymmetric wavefunction)}
\end{aligned}$$
where $\hat{P}$ effects any permutation of $(r_{1},r_{2},\cdots,r_{N})$, and $\tau_{\hat{P}}$ corresponding to the inverse number of permutation $\hat{P}$. Noted that the relation will be modified after introducing spin.
Come back to the Helium example, $\Phi_{1}(r_{1},r_{2})$ is acceptable as symmetric wavefunction, but neither $\Phi_{2}(r_{1},r_{2})$ nor $\Phi_{2}(r_{2},r_{1})$ is acceptable. They are **degenerate** with same energy $\epsilon_{\text{1s}}+\epsilon_{\text{2s}}$ However, since SE is linear, the two latter wavefunctions can be combined with coefficients to yield another solution:
$$\Phi_{2}^{\prime} = c_{1}\Phi_{2}(r_{1},r_{2})+c_{2}\Phi_{2}(r_{2},r_{1})$$
Then we obtain following acceptable wavefunctions for Helium-like system: 
(1) configuration $\text{1s}^{2}$, 
$$\Psi_{1}(r_{1},r_{2}) = \Phi_{1}(r_{1},r_{2})$$
(2) configuration $\text{1s 2s}$,
$$\begin{aligned}
\Psi_{2}(r_{1},r_{2}) &= \frac{1}{\sqrt{2}}(\Phi_{2}(r_{1},r_{2})+\Phi_{2}(r_{2},r_{1}))\\
\Psi_{3}(r_{1},r_{2}) &= \frac{1}{\sqrt{2}}(\Phi_{2}(r_{1},r_{2})-\Phi_{2}(r_{2},r_{1}))
\end{aligned}$$
Noted that other orbital configurations such as $\text{1s 2p}_{0}$ can be constructed in the same way. Such states are frequently degenerate in IPM view owing to degeneracies of AOs themselves. When electron interaction is admitted, the energies of IPM states are modified, and the original degeneracies may be resolved, but the states are still classified in terms of electron configurations and **IPM ideas still exist** in the theory of atomic spectra. [Condon and Shortley, 1935](<file:///C:/Users/Yi/Desktop/zbook Base>) 

##### Effect of single electron spin 

Single electron is not completely characterized by spatial wavefunction $\phi(r)$; even in a state without orbital angular momentum, application of magnetic field reveals that the state is really **a degenerate pair or doublet**. The small splitting of energy levels which is [[Zeeman effect]], suggests an **intrinsic magnetic moment** whose component along the **field direction** can take only one of two possible values $\alpha$ or $\beta$. The splitting arises from small field-dependent terms in $H$ which we have so far ignored.
The intrinsic angular momentum is called **spin** and the permitted values of the spin component are found to be $\pm\hbar /2$. The direction along which the component is measured is chosen as $z$ axis. Mathematically, we introduce a **spin variable** $s$ in addition to the **position variable** $r$, and we associate operators $S_{x},S_{y}$ and $S_{z}$ with the three components of spin angular momentum. Now the **spinless Hamiltonian** works on **external** variable $r$, while the **spin operators** work on **internal** variable $s$. That is,
![[Drawing 2024-12-11 15.39.50.excalidraw]]
_I have to say that is an awesome way to explain **spin**._
Like the product function $\Phi(r_{1},r_{2})$ is a simultaneous eigenfunction of two parts of the system, so is the spin-orbital $\Psi(\boldsymbol{x}) := \Psi(r,s) = \phi(r)\eta(s)$, where we adopt $\boldsymbol{x}$ for space-spin variables, i.e. $r$ and $s$ together. If we interested in states with a definite value of $S_{z}$, then the spin state $\eta(s)$ will be a solution of
$$S_{z}\eta = \lambda \eta$$
and if the orbital state is of energy $\epsilon$, then $\phi(r)$ satisfies 
$$h \phi = \epsilon \phi$$
Consequently, since each operator works only on its own variables,
$$\boxed{\begin{aligned}
h \Psi &= \epsilon \Psi\\
S_{z}\Psi &= \lambda \Psi
\end{aligned}}$$

^f09564
and $\Psi$ is a simultaneous eigenstate of $h$ and $S_{z}$. Also, observation shows that Eq. [[1 Introduction#^f09564]] has only two solutions: these are normally written as $\alpha$ and $\beta$ and satisfy
$$S_{z}\alpha = \frac{1}{2}\alpha, S_{z}\beta = - \frac{1}{2}\beta$$
where we use dimensionless $S$ to avoid repeated appearance of $\hbar$, which is the atomic unit. We also know that every orbital $\phi$ yields two possible spin-orbitals, $\psi = \phi \alpha$ and $\bar{\psi} = \phi \beta$. 
The observed spin components behave like components of a vector and satisfy commutation relations exactly like the orbital angular momentum operators. [[Angular Momentum]]
A spin-orbital $\Psi$ may be an exact eigenfunction without neglect of spin effects because spatial and spin parts are separated in total Hamiltonian, and spin part is just $S_{z}$ or some function of $S_{z}$. [[Nonlinear Function of S]] Also, to have a more visualized view of $\alpha(s)$ and $\beta(s)$, we can take them as delta functions because they vanish for $s \ne \pm \frac{1}{2}$, respectively. [Dirac, 1958](<file:///C:/Users/Yi/Desktop/zbook Base>) And we have orthonormal relation:
$$\begin{aligned}
\int \alpha(s)^{*}\alpha(s)\mathrm{d}s &=  \int \beta(s)^{*}\beta(s)\mathrm{d}s = 1\\
\int \alpha(s)^{*}\beta(s)\mathrm{d}s &=  \int \beta(s)^{*}\alpha(s)\mathrm{d}s = 0
\end{aligned}$$

##### Classification of electron states 

We return to the Helium-like system including spin, then electrons must each be assigned to spin-orbitals as
$$\text{1s}\alpha,\text{1s}\beta,\text{2s}\alpha,\text{2s}\beta,\cdots$$
For configuration $\text{1s}^{2}$, we have four product functions as
$$\Phi(\boldsymbol{x_{1}},\boldsymbol{x_{2}}) \in \{\text{1s}\alpha,\text{1s}\beta \}_{1} \times \{\text{1s}\alpha,\text{1s}\beta \}_{2}$$
i.e.
$$\begin{aligned}
\Phi_{1} := \Phi_{1}(\boldsymbol{x_{1}},\boldsymbol{x_{2}}) &= \text{1s}(r_{1})\alpha(s_{1})\text{1s}(r_{2})\alpha(s_{2})\\
\Phi_{2} :=\Phi_{2}(\boldsymbol{x_{1}},\boldsymbol{x_{2}}) &= \text{1s}(r_{1})\alpha(s_{1})\text{1s}(r_{2})\beta(s_{2})\\
\Phi_{3} :=\Phi_{3}(\boldsymbol{x_{1}},\boldsymbol{x_{2}}) &= \text{1s}(r_{1})\beta(s_{1})\text{1s}(r_{2})\alpha(s_{2})\\
\Phi_{4} :=\Phi_{4}(\boldsymbol{x_{1}},\boldsymbol{x_{2}}) &= \text{1s}(r_{1})\beta(s_{1})\text{1s}(r_{2})\beta(s_{2})
\end{aligned}$$
and they are all degenerate. (We fix $\Phi_{1}$ as $\Phi_{1}(\boldsymbol{x_{1}},\boldsymbol{x_{2}})$) By combination we obtain another four symmetric or antisymmetric wavefunctions.
$$\begin{aligned}
\Psi_{1}^{a} &= \frac{1}{\sqrt{2}}(\Phi_{2}-\Phi_{3})\\
\Psi_{1}^{s} &= \Phi_{1}\\
\Psi_{2}^{s} &= \frac{1}{\sqrt{2}}(\Phi_{2}+\Phi_{3})\\
\Psi_{3}^{s} &= \Phi_{4}
\end{aligned}$$
Similarly for $\text{1s}\text{2s}$, [[Configuration 1s2s Derivation]] we can get its spin-orbital wavefunctions. And their energies are shown below.
![[Drawing 2024-12-11 18.11.24.excalidraw]]
When applying a magnetic field, we can see the triplet states be resolved ([[not into three components]]), and can be identified spectroscopically. From experimental data, we verifies antisymmetric existence, which means electrons' wavefunctions satisfy antisymmetric relation, i.e. **antisymmetry principle**: 
The wavefunction $\Psi(\boldsymbol{x_{1}},\boldsymbol{x_{2}},\cdots,\boldsymbol{x_{N}})$ describing any state of an N-electron system is antisymmetric under any permutation of electrons.
$$\hat{P} \Psi(\boldsymbol{x_{1}},\boldsymbol{x_{2}},\cdots,\boldsymbol{x_{N}}) = (-1)^{\tau_{\hat{P}}}\Psi(\boldsymbol{x_{1}},\boldsymbol{x_{2}},\cdots,\boldsymbol{x_{N}})$$
This is a generalization of **Pauli exclusion principle**. The connection is made in the case of $N=2$. If two electrons are put into same spin-orbital, the wavefunction can only be symmetric, in violation of the antisymmetry requirement. Therefore, two electrons (**in IPM description**) cannot occupy the same state, that is, in Pauli's statement, possess identical sets of quantum numbers. 
Noted that for more than two electrons, it's not possible to find a **spatial-spin product form** of $\Psi$ satisfies antisymmetry principle. [[When can we separate spatial and spin part of wavefunction]] 

### Example: Hydrogen Molecule

It seems like our [[1 Introduction#^533af6]] approach can be generalized to any many-electron system: (1) model Hamiltonian $H_{0}$ describe $N$ non-interacting electrons moving in the field of all fixed nuclei; (2) product functions are simultaneous eigenstate; (3) and when symmetry considerations are satisfied, we may get a fair description including interaction. 
However, in passing from atoms to molecules, we don't have one-electron eigenfunctions in closed form because $h$ includes **several nuclei** instead of just one. 
We shall need **polycentric molecular orbitals (MOs)** that describe the states of a single electron moving over the whole nuclear framework.  ^f14b69

##### Hydrogen molecule ion $\mathrm{H_{2}^{+}}$

The simplest 1-electron 2-center system is $\mathrm{H_{2}^{+}}$, in which we illustrate the nature of the polycentric problem. The SE is 
$$h \phi = \epsilon \phi$$
where
$$h = - \frac{1}{2}\nabla^{2}- \left( \frac{1}{r_{a}}+\frac{1}{r_{b}} \right)$$
The SE can be solved with variable separation by [Burrau, 1927](<file:///C:/Users/Yi/Desktop/zbook Base>). However, solutions in this way is not generally possible, so we directly pass to simpler approximation. 
If the electron is near any nucleus, the Hamiltonian will approximately a single hydrogen atom. Then we use $a(r)$ for the $\text{1s}$ orbital centered on nucleus a and $b(r)$ for that centered at nucleus b. Since 1s functions fall rather rapidly from their peak value at the nuclei, we write the trial function (MO) as 
$$\phi(r) = c_{a}a(r)+c_{b}b(r)$$
And 
$$|\phi(r)|^{2}\mathrm{d}r = [c_{a}^{2}a(r)^{2}+c_{b}^{2}b(r)^{2}+2c_{a}c_{b}a(r)b(r)]\times \mathrm{d}r$$
corresponding to the probability of finding electron at $r$. Due to the mirror symmetry, we have 
$$|\phi(r)|^{2} = |\phi(-r)|^{2}$$
That is 
$$c_{a}^{2}a(r)^{2}+c_{b}^{2}b(r)^{2}+\cancel{2c_{a}c_{b}a(r)b(r)} = c_{a}^{2}b(r)^{2}+c_{b}^{2}a(r)^{2}+\cancel{2c_{a}c_{b}a(r)b(r)}$$
So we have $c_{a}=\pm c_{b}$. Therefore we have two approximate MOs,
$$\begin{aligned}
B(r) &= m_{B}[a(r)+b(r)]\\
A(r) &= m_{A}[a(r)-b(r)]
\end{aligned}$$
where $B$ refers to bonding (ground state) and $A$ refers to antibonding (first excited state), and $m_{i}$ are normalization constant.
MOs in **linear combination of atomic orbitals (LCAO) form**, is extremely important in molecular quantum mechanics. [[How to identify ground state and excited state in LCAO]] Actually, LCAO is a method to deal with the polycentric problem in [[1 Introduction#^f14b69]], that's how we obtain molecule-level "AOs" for one electron without interaction. 

##### Normal molecule $\mathrm{H_{2}}$

Use the LCAO from $\mathrm{H_{2}^{+}}$, we consider solve for the real molecule $\mathrm{H_{2}}$. Like Helium atom[[1 Introduction#^533af6]], we first absent electron interaction, and an approximate spatial wavefunction for the state of lowest energy will be
$$\Phi(r_{1},r_{2}) = B(r_{1})B(r_{2})$$
just like 1s orbital for Hydrogen atom. (1s-like MOs) And the spatial wavefunction gives an energy expectation $E = 2\epsilon_{B}$. Combined with a antisymmetric spin part, we get the antisymmetric spin-orbital wavefunction: 
$$\Psi(\boldsymbol{x_{1}},\boldsymbol{x_{2}}) = B(r_{1})B(r_{2})\times \frac{1}{\sqrt{2}}[\alpha(s_{1})\beta(s_{2})-\beta(s_{1})\alpha(s_{2})]$$







