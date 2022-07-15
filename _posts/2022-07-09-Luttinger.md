---
layout: post
title: "Luttinger liquid theory of the quantum Hall edge"
date: 2022-07-09
categories: opinion
tags: [resources, jekyll]
image:
---

### spin-charge seperation
In the 1D electron system, the striking feature is the charge-spin separation, which is the characteristic feature of non-Fermi liquids. Here we introduce a very important 1D lattice model with short-range repulsive force--Hubbard model, and discuss the charge-spin separation feature. 

With discrete lattice sites, the the 1D continuous Hamiltonian in Eq.~(\ref{eq:1}) can be written as a tight-binding model:

$$
H_0=-\sum_{l,l',\sigma} t_{l,l'}c^{\dagger}_{l\sigma}c_{l'\sigma}-\mu\sum_{l,\sigma}c^{\dagger}_{l\sigma}c_{l\sigma}, 
$$

where $l$ is the lattice site, $\sigma$ is the degree of freedom of spin. We can simplify $t_{l,l'}$ as $t$. For the single lattice site per unit cell, on can obtain the single band as:

$$
H_0=\sum_{k,\sigma} \left(-2t\cos(ak)-\mu \right) c^{\dagger}_{k,\sigma}c_{k,\sigma},
$$

where $a$ is the lattice constant of 1D model. The fundamental Hamiltonian describing the interaction electrons is: 

$$
H_{int}=\frac{1}{2}\sum_{\sigma,\sigma'}\int dxdx' \psi^{\dagger}_{\sigma}(x)\psi^{\dagger}_{\sigma'}(x')\frac{e^2}{\abs{x-x'}}\psi_{\sigma'}(x')\psi_{\sigma}(x).
$$

In the lattice system, we can simplify the above interacting Hamiltonian by only considering on-site Coulomb repulsion, we can have:

$$
H_{U}=U\sum_{l}n_{l\uparrow}n_{l\downarrow},
$$

where $n_{l\sigma}=c^{\dagger}_{l\sigma}c_{l\sigma}$ is the electron number operator in site $l$, and $U$ is the interaction strength of on-site electrons. The so-called Hubbard model can be written as:

$$
H=&H_0+H_U\\
=&-t\sum_{l,l',\sigma}c^{\dagger}_{l\sigma}c_{l'\sigma}-\mu\sum_{l,\sigma}c^{\dagger}_{l\sigma}c_{l\sigma}+U\sum_{l}n_{l\uparrow}n_{l\downarrow}.
$$

The competition between $H_0$ and $H_U$ is the basic physics picture of the Hubbard model. Similar to Eqs.~(\ref{eq:10}), we define the spin density and spin current density:

$$
j^s_0(x)=\sum_{\sigma}\sigma j_{0,\sigma}(x)=j_{0,\uparrow}(x)-j_{0,\downarrow}(x),\\
j^s_1(x)=\sum_{\sigma}\sigma j_{1,\sigma}(x)=j_{1,\uparrow}(x)-j_{1,\downarrow}(x).
$$

Using the Kac-Moody algebra in~(\ref{eq:16}), we obtain the commutation relation between $j^s_0(x)$ and $j^s_1(x)$: 

$$
[j^s_0(x),j^s_1(x')]=-\frac{2i}{\pi}\partial_x \delta(x-x')
$$

Let's consider about the following commutation relations:
$$
[\rho_{R}(p),H_0]&=2t p \rho_R(p),\\
[\rho_{L}(p),H_0]&=-2t p \rho_L(p),
$$

where $t$ is the hopping parameter. That means we can effectively write the $H_0$ as the form:

$$
\tilde{H}_0=4\pi t \sum_{p>0,\sigma}(\rho_{R,\sigma}(-p)\rho_{R,\sigma}(p)+\rho_{L,\sigma}(p)\rho_{L,\sigma}(-p)),
$$

so that the commutation relations in (\ref{eq:47}) are maintained. And this equals:

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

Using the Eqs.~(\ref{eq:49}) and (\ref{eq:51}), So the total Hubbard Hamiltonian can be written as: 

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

Similarly, we introduce the auxiliary Bose field for spin part, which has the relations:

$$
j^s_0(x)=\sqrt{\frac{2}{\pi}}\partial_x \phi_s(x), \qquad
j^s_1(x)=-\sqrt{\frac{2}{\pi}}\Pi_s(x).
$$

We can rearrange Eqs.~(\ref{eq:53}) and (\ref{eq:54}) with Bose fields as:

$$
H_{charge}=v_c\int dx \left[K_c(\partial_x\phi_c(x))^2+\frac{1}{K_c}(\Pi_c(x))^2\right],
$$

where the velocity $v_c$ and the stiffness $K_c$ are:

$$
v_c=\sqrt{t\left(t+\frac{U}{2\pi}\right)}, \qquad K_c=\sqrt{\frac{t+U/2\pi}{t}}.
$$

For the spin part, we have: 

$$
H_{spin}=v_s\int dx \left[K_s(\partial_x\phi_s(x))^2+\frac{1}{K_s}(\Pi_s(x))^2\right],
$$

where the velocity $v_s$ and the stiffness $K_s$ are:

$$
v_s=\sqrt{t\left(t-\frac{U}{2\pi}\right)}, \qquad K_s=\sqrt{\frac{t-U/2\pi}{t}}.
$$

In this chapter, I will intruduce the density matrix renormalization group approach in 
strongly-correlated quantum magnetic system, using **XXX-Heisenberg** model as an explicit example.

<!--more-->

<img class="centered" src="https://www.mathjax.org/badge/mj-logo.svg" />

### Heisenberg model

The Heisenberg model is given by:

$$ H=\sum_{ij\alpha}J_{\alpha}\sigma^{\alpha}_i\sigma^{\alpha}_j $$


### How to implement MathJax with Jekyll

I followed the instructions described by Dason Kurkiewicz for
[using Jekyll and Mathjax](http://dasonk.github.io/blog/2012/10/09/Using-Jekyll-and-Mathjax/).

Here are some important details. I had to modify the Ruby library for Markdown in
my ```_config.yml``` file. Now I'm using redcarpet so the corresponding line in the
configuration file is: ```markdown: redcarpet```

To load the MathJax javascript, I added the following lines in my layout ```page.html```
(located in my folder ```_layouts```)

{% highlight r %}
<script type="text/javascript"
    src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
{% endhighlight %}

Of course you can choose a different file location in your jekyll layouts.


### A Couple of Examples

Here's a short list of examples. To know more about the details behind MathJax, you can
always checked the provided documentation available at
[http://docs.mathjax.org/en/latest/](http://docs.mathjax.org/en/latest/)

I'm assuming you are familiar with LaTeX. However, you should know that MathJax does not
have the exactly same behavior as LaTeX. By default, the **tex2jax** preprocessor defines the
LaTeX math delimiters, which are ```\\(...\\)``` for in-line math, and ```\\[...\\]``` for
displayed equations. It also defines the TeX delimiters ```$$...$$``` for displayed
equations, but it does not define ```$...$``` as in-line math delimiters. Fortunately,
you can change these predefined specifications if you want to do so.

Let's try a first example. Here's a dummy equation:

$$a^2 + b^2 = c^2$$

How do you write such expression? Very simple: using **double dollar** signs

{% highlight r %}
$$a^2 + b^2 = c^2$$
{% endhighlight %}

To display inline math use ```\\( ... \\)``` like this ```\\( sin(x^2) \\)``` which gets
rendered as \\( sin(x^2) \\)


Here's another example using type ```\mathsf```

{% highlight r %}
$$ \mathsf{Data = PCs} \times \mathsf{Loadings} $$
{% endhighlight %}

which gets displayed as

$$ \mathsf{Data = PCs} \times \mathsf{Loadings} $$

Or even better:

{% highlight r %}
\\[ \mathbf{X} = \mathbf{Z} \mathbf{P^\mathsf{T}} \\]
{% endhighlight %}

is displayed as

\\[ \mathbf{X} = \mathbf{Z} \mathbf{P^\mathsf{T}} \\]

If you want to use subscripts like this \\( \mathbf{X}\_{n,p} \\) you need to scape the
underscores with a backslash like so ``` \mathbf{X}\_{n,p} ```:

{% highlight r %}
$$ \mathbf{X}\_{n,p} = \mathbf{A}\_{n,k} \mathbf{B}\_{k,p} $$
{% endhighlight %}

will be displayed as

\\[ \mathbf{X}\_{n,p} = \mathbf{A}\_{n,k} \mathbf{B}\_{k,p} \\]
