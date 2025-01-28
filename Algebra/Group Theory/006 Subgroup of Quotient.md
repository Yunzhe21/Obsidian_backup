---
tags:
  - "#CorrespondenceTheorem"
  - "#Algebra"
---
---

>[! lem |*] 
>Take $f\in Hom(G,G')$, take $H\lhd G$, $K\lhd G'$, then
>1. $f(H)\lhd f(G)$ 
>2. $f^{-1}(K)\lhd G$
- [[Quotient Group (Proof)#^2ce42d|Proof]] ^ImageInverseImageOfNormalSubgroup

#CorrespondenceTheorem 
>[! thm |*] Correspondence Theorem
>Take $f\in Hom(G,G')$, Consider $A=\{H\leq G:\ ker(f)\leq H\}$, $B=\{K\leq G': K\leq Im(f)=f(G)\}$, then map $I:\ A\rightarrow B$ as $H\longmapsto f(H)$ and $J:\ B\rightarrow A$ as $K\longmapsto f^{-1}(K)$ are well-defined and inverse of each other.
- [[Quotient Group (Proof)#^aadc17|Proof]]

>[! cor |*]
>Let $N\lhd G$, and $p:\ G\rightarrow \frac{G}{N}$ as $y\longmapsto \overline{y}$ be the canonical projection. Then the map $f:\ H\longmapsto p(H)$ is a bijection from ${} \{H:H\leq G, N\leq H\}$ to $\{K\leq \frac{G}{N}\}$ with inverse map $K\longmapsto p^{-1}(K)$.   
- Proof is strightforward

**Restatement (in fact weaker):** $K\leq \frac{G}{N}$, $\exists !\ H\leq G\ s.t.\ N\subseteq H$ with $K=\frac{H}{N}$. Moreover, $H$ is normal in $G\ \iff\ K\lhd \frac{G}{N}$ ^RewriteSubgroupOfQuotient
- This corollary implies that the **subgroup of a quotient group** is another quotient group with the denominator being a subgroup.

---

>[! prp |*]
>If $G$ is cyclic and $H\leq G$, then $H$ is cyclic.
- [[Subgroup of Quotient (Proof)#^d3808d|Proof]] 

<font color="#ff0000">Exercise:</font> $K\leq \frac{\mathbb{Z}}{m\mathbb{Z}}\ (m\geq 1)$, then $K=\frac{d\mathbb{Z}}{m\mathbb{Z}}$ for $d$ s.t. $d\bigr | m$. 
- This exercise shows us what exactly are subgroups of $\frac{\mathbb{Z}}{m\mathbb{Z}}$.
- The proof is straight from the previous restatement.






