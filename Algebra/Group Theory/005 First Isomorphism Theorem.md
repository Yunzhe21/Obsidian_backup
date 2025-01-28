---
tags:
  - FirstIsomorphismThm
  - "#Algebra"
---
---

# First Isomorphism Theorem

#FirstIsomorphismThm 
>[! thm |*] First Isomorphism Theorem
>Let $f\in Hom(G, G')$, then $\exists ! \ \overline{f}\in Hom(\frac{G}{ker(f)}, G')$ s.t. $f=\overline{f}\circ p$ where $p:\ G\rightarrow \frac{G}{ker(f)}$ is the canonical projection. Moreover, $\overline{f}$ is injective.

^82b689

- [[Quotient Group (Proof)#^caf9fa|Proof]]  ^587107

>[! cor|*] 
>If $f\in Hom(G,G')$, then $\overline{f}:\ \frac{G}{ker(f)}\rightarrow f(G)$ bijectively, thus $\frac{G}{ker(f)}\sim f(G)$.

^dbe442

- This Corollary can tell us how to prove one quotient group is isomorphic to another group.

## Application

1. If $G=\langle x\rangle=\{x^{k},k\in \mathbb{Z}\}$, then either $G\sim \mathbb{Z}$ or $\exists !\ m\in \mathbb{N}\ s.t.\ G\sim \frac{\mathbb{Z}}{m\mathbb{Z}}$
	*Proof:* $f:\ \mathbb{Z}\rightarrow G$: $k\longmapsto x^{k}$ is surjective and $f\in Hom(\mathbb{Z}, G)$
	$\Longrightarrow \ \overline{f}:\ \frac{\mathbb{Z}}{ker(f)}\sim Im(f)=G$
	But $ker(f)\lhd \mathbb{Z}$, hence $\exists m\in \mathbb{N}\ s.t.\ ker(f)=m\mathbb{Z}$ $\Longrightarrow\ G\sim \frac{\mathbb{Z}}{m\mathbb{Z}}$ 
		If $m=0$, $G\sim \frac{\mathbb{Z}}{\{0\}}\sim \mathbb{Z}$ 
		If $m\geq 1$, $G\sim \frac{\mathbb{Z}}{m\mathbb{Z}}$, and $\bigr |\frac{\mathbb{Z}}{m\mathbb{Z}}\bigr |=m$

2. $n\geq 1\in \mathbb{N}$, then ${} \frac{\mathbb{Z}}{n\mathbb{Z}}\sim U_{n}=\{z\in \mathbb{C}^{*}: z^{n}=1\} {}$.
	*Proof:* $f:\ (\mathbb{R},+) \rightarrow (\mathbb{C}_{n},\times)$: $k\longmapsto e^{\frac{2\pi ki}{n}}$ is surjective group homomorphism.
	$\Longrightarrow\ \frac{\mathbb{Z}}{ker(f)}\sim U_{n}=Im(f)$, $k\in ker(f)\iff k=n\mathbb{Z}$ 

3. $\mathbb{Z}\lhd \mathbb{R}$, $\frac{\mathbb{R}}{\mathbb{Z}}\sim \mathbb{C}_{u}$ 
	*Proof:* $f:\ (\mathbb{R}, +)\rightarrow (\mathbb{C}_{u}, \times)$ as ${} \theta \longmapsto e^{2\pi i\theta} {}$, clearly $f$ is surjective
	$ker(f)=\mathbb{Z}$ 
	$f$ is also homomorphism, hence $\frac{\mathbb{R}}{ker(f)}\sim \mathbb{C}_{u}$


