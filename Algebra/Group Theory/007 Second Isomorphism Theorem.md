---
tags:
  - SecondIsomorphismThm
  - "#Algebra"
---
---

## Statement 

#SecondIsomorphismThm 
>[! thm |*] Second Isomorphism Theorem
> $f:\ G\rightarrow G'$ is a group homomorphism. Suppose that $N\lhd G,\ N\subseteq ker(f)$. Denote by $p:\ G\rightarrow \frac{G}{N}$ the canonical projection. Then $\exists !\ \overline{f}:\ \frac{G}{N} \rightarrow\ G'$ s.t. $f=\overline{f}\cdot p$. Moreover:
> 1. $\overline{f}\in Hom (\frac{G}{N}, G')$
> 2. $ker(\overline{f})=\frac{ker(f)}{N}$
> 3. $Im(\overline{f})=Im(f)$

^22beed

- Proof is almost identical to [[005 First Isomorphism Theorem#^587107|Proof of the First Isomorphism Theorem]].

>[! cor |*] 
> $\frac{\frac{G}{N}}{\frac{ker(f)}{N}} \sim Im(f)=Im(\overline{f})$ 
- Proof using [[005 First Isomorphism Theorem#^dbe442|Corollary of First Isomorphism Theorem]].

Note that $\frac{ker(f)}{N}\lhd \frac{G}{N}$ 

### Application:

Let $H\lhd G$, $N\lhd G$ s.t. $N\subseteq H$, let $P_{N}:\ y\longmapsto \overline{y}^{N}$, $P_{H}:\ y\longmapsto \overline{y}^{H}$, because $N\subseteq H=ker(P_{H})$, apply second isomorphism theorem to $P_{H}$
- That yields $\frac{\frac{G}{N}}{\frac{H}{N}}\sim \frac{G}{H}$ 

<font color="#ff0000">Example</font>: If $d\mid m\geq 1$ ($\iff m\mathbb{Z}\subseteq d\mathbb{Z}$), then $\frac{\frac{\mathbb{Z}}{m\mathbb{Z}}}{\frac{d\mathbb{Z}}{m\mathbb{Z}}}\sim \frac{\mathbb{Z}}{d\mathbb{Z}}$, when we take $G=\mathbb{Z}$, $N=m\mathbb{Z}$, $H=d\mathbb{Z}$.

---

## Order of an element of a group

$G$ is a group and $x\in G$, define $\alpha_{x}:\ \mathbb{Z}\rightarrow G\ \in Hom(\mathbb{Z},G)$ as $k\longmapsto x^{k}$ 
(Note: ${} Im(\alpha_{x})=\langle x\rangle {}$)
<font color="#ff0000">Case 1:</font>
	If $\alpha_{x}$ is injective $\iff\ ker(\alpha_{x})=\{0\}$, then ${} \langle x\rangle\sim \mathbb{Z} {}$ and one says $x$ has infinite order.
<font color="#ff0000">Case 2:</font>
	If $\alpha_{x}$ is not injective $\iff$ ${} ker({\alpha_{x}})=n\mathbb{Z} {}$ for some $n\geq 1$, then ${} \frac{\mathbb{Z}}{n\mathbb{Z}}\sim \langle x\rangle=Im(\alpha_{x}) {}$, then we say $x$ has finite order $n$.

Notation: $O(x)$ is the order of $x$.

<font color="#ff0000">Equivalent definition of</font> $O(x)$:

>[! def |*] Order of an element
$O(x)=min\{k\geq 1,\ x^{k}=e\}$ is the order of an element $x$ in group $G$.

>[! prp |*]
>If $G$ is finite and $x\in G$, then $x^{|G|}=e$ 
- [[Second Isomorphism Theorem (Proof)#^b46ad9|Proof]]



