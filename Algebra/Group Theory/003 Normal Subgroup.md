---
tags:
  - Normal
  - Center
  - "#Algebra"
---
---

## Normal Subgroup

#Normal
>[! def |*] Normal Subgroup
>A subgroup $H$ is called *normal* if $\forall h\in H,\ x\in G,\ \text{then, } xhx^{-1}\in H$.
$\iff$ $H$ is <u>stable</u> under any [[002 Morphism between Groups#^a10ff0|inner automorphism]] of $G$

^eaa5c3

<font color="#ff0000">Notation:</font> $H\lhd G$.     

## Property of normal subgroup

>[! prp | 1]
>If $f\in Hom(G, G')$ and $H'\lhd G'$, then $H\coloneqq f^{-1}(H')$ is a normal subgroup of G. 
- [[Normal Subgroup (Proof)#^d9419e|Proof]] 

>[! prp | 2]
>If $f\in Hom(G,G')$, surjective, and $H\lhd G$, then $H':=f(H)$ is a normal subgroup of $G'$.
- Proof is almost identical to 1. 

>[! prp | 3]
>If $f\in Hom(G, G')$, then $ker(f)\lhd G$.
- [[Normal Subgroup (Proof)#^cec921|Proof]] 

---

## Center of a group

#Center 
>[! def | *] Center
>Let G be a group, then the center of $G$ is $Z(G)=\{x\in G:\ \forall y\in G,\ xy=yx\}$ 

### Property of $Z(G)$ 

>[! prp | 1]
> $Z(G)\lhd G$, and in fact $H\leq Z(G)\Longrightarrow \ H\lhd G$. 
- [[Normal Subgroup (Proof)#^0bc35a|Proof]] 

>[! prp | 2]
> $G$ is commutative $\iff$ $G=Z(G)$.
- [[Normal Subgroup (Proof)#^705713|Proof]] 

>[! prp | 3]
> $Z(G)$ is commutative.
- Proof is obvious

>[! cor | *]
>If A is commutative, then $H\leq A\Longrightarrow H\lhd A$.


<font color="#ff0000">Example:</font> $Z(GL_{n}(K))=\{\lambda I_{n},\lambda\in K^{*}\}$, where $K$ is a field, and $K^{*}=K-\{0\}$.
- [[Normal Subgroup (Proof)#^8a7dfb|Proof]] 




