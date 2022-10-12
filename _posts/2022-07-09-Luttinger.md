---
layout: post
title: "Luttinger liquid theory of the quantum Hall edge"
date: 2022-07-09
categories: opinion
tags: [resources, jekyll]
image:
---

### Hubbard model

In the 1D electron system, the striking feature is the charge-spin separation, which is the characteristic feature of non-Fermi liquids. Here we introduce a very important 1D lattice model with short-range repulsive force -- Hubbard model, and discuss the charge-spin separation feature. With discrete lattice sites, the the 1D continuous Hamiltonian can be written as a tight-binding model:

$$
H_0=-\sum_{l,l',\sigma} t_{l,l'}c^{\dagger}_{l\sigma}c_{l'\sigma}-\mu\sum_{l,\sigma}c^{\dagger}_{l\sigma}c_{l\sigma}, 
$$

where $l$ is the lattice site, $\sigma$ is the degree of freedom of spin. We can simplify $t_{l,l'}$ as $t$. For the single lattice site per unit cell, on can obtain the single band as:

$$
H_0=\sum_{k,\sigma} \left(-2t\cos(ak)-\mu \right) c^{\dagger}_{k,\sigma}c_{k,\sigma},
$$

where $a$ is the lattice constant of 1D model. The fundamental Hamiltonian describing the interaction electrons is: 

$$
H_{int}=\frac{1}{2}\sum_{\sigma,\sigma'}\int dxdx' \psi^{\dagger}_{\sigma}(x)\psi^{\dagger}_{\sigma'}(x')\frac{e^2}{\lvert x-x' \rvert}\psi_{\sigma'}(x')\psi_{\sigma}(x).
$$

In the lattice system, we can simplify the above interacting Hamiltonian by only considering on-site Coulomb repulsion, we can have:

$$
H_{U}=U\sum_{l}n_{l\uparrow}n_{l\downarrow},
$$

where $$n_{l\sigma}=c^{\dagger}_{l\sigma}c_{l\sigma}$$ is the electron number operator in site $$l$$, and $$U$$ is the interaction strength between on-site electrons. The so-called Hubbard model can be written as:

$$
H=H_0+H_U
=-t\sum_{l,l',\sigma}c^{\dagger}_{l\sigma}c_{l'\sigma}-\mu\sum_{l,\sigma}c^{\dagger}_{l\sigma}c_{l\sigma}+U\sum_{l}n_{l\uparrow}n_{l\downarrow}.
$$

The competition between $H_0$ and $H_U$ is the basic physics picture of the Hubbard model. The kinetic term delocalizes the electron, while the Hubbard term contributes the electron localization. We define the spin density
$$
j^s_0(x)=\sum_{\sigma}\sigma j_{0,\sigma}(x)=j_{0,\uparrow}(x)-j_{0,\downarrow}(x),
$$

and the spin current density
$$
j^s_1(x)=\sum_{\sigma}\sigma j_{1,\sigma}(x)=j_{1,\uparrow}(x)-j_{1,\downarrow}(x).
$$

Using the Kac-Moody algebra, we obtain the commutation relation between $j^s_0(x)$ and $j^s_1(x)$: 

$$
[j^s_0(x),j^s_1(x')]=-\frac{2i}{\pi}\partial_x \delta(x-x')
$$

Let's consider about the following commutation relations:

$$
[\rho_{R}(p),H_0]=2t p \rho_R(p),\qquad
[\rho_{L}(p),H_0]=-2t p \rho_L(p),
$$

where $t$ is the hopping parameter. That means we can effectively write the $H_0$ as the form:

$$
\tilde{H}_0=4\pi t \sum_{p>0,\sigma}(\rho_{R,\sigma}(-p)\rho_{R,\sigma}(p)+\rho_{L,\sigma}(p)\rho_{L,\sigma}(-p)),
$$

so that the commutation relations can be retained. And this equals:

$$
\tilde{H}_0=\frac{\pi t}{2} \int dx \left[ (j^c_0(x))^2+(j^c_1(x))^2+(j^s_0(x))^2+(j^s_1(x))^2 \right].
$$

For the interacting term $H_U$, we have:

$$
H_U=U\sum_{l}n_{l\uparrow}n_{l\downarrow}=\frac{U}{4} \sum_{l}\left[(n_{l\uparrow}+n_{l\downarrow})^2-(n_{l\uparrow}-n_{l\downarrow})^2 \right],
$$

where $n_{l\uparrow}+n_{l\downarrow}$ is $j_0(l)$, the charge density at site $l$, and $n_{l\uparrow}-n_{l\downarrow}$ is $j^s_0(l)$, the spin density at site $l$. The Hubbard term can be rewritten as:  

$$
H_U=\frac{U}{4}\int dx \left[(j^c_0(x))^2-(j^s_0(x))^2\right].
$$

### Spin-charge seperation

Thus, we can rewrite the interacting Hamiltonian as: 

$$
H=H_{charge}+H_{spin},
$$

where

$$
H_{charge}=\int dx \left[\left(\frac{\pi t}{2}+\frac{U}{4}\right)(j^c_0(x))^2+\frac{\pi t}{2}(j^c_1(x))^2\right],
$$

and
$$
H_{spin}=\int dx \left[\left(\frac{\pi t}{2}-\frac{U}{4}\right)(j^s_0(x))^2+\frac{\pi t}{2}(j^s_1(x))^2\right].
$$

Similarly, we introduce the auxiliary Bose field for spin sector, which has the relations:

$$
j^s_0(x)=\sqrt{\frac{2}{\pi}}\partial_x \phi_s(x),
$$

and
$$
j^s_1(x)=-\sqrt{\frac{2}{\pi}}\Pi_s(x).
$$

We can rearrange the Hamiltonian with only the Bose fields as:

$$
H_{charge}=v_c\int dx \left[K_c(\partial_x\phi_c(x))^2+\frac{1}{K_c}(\Pi_c(x))^2\right],
$$

where
$$
v_c=\sqrt{t\left(t+\frac{U}{2\pi}\right)}
$$
is the velocity of charge excitation, and
$$
\quad K_c=\sqrt{\frac{t+U/2\pi}{t}}.
$$
is the stiffness.

For the spin excitation part, we have: 

$$
H_{spin}=v_s\int dx \left[K_s(\partial_x\phi_s(x))^2+\frac{1}{K_s}(\Pi_s(x))^2\right],$$

with
$$v_s=\sqrt{t\left(t-\frac{U}{2\pi}\right)}$$, and $$ K_s=\sqrt{\frac{t-U/2\pi}{t}}$$.

One can see the spin and charge excitations have different velocities, which reveals that the two basic excited modes follow the different equations of motion.

### Quantum Hall edge and effective theory

