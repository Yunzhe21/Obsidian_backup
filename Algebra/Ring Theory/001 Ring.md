---
tags:
  - Ring
  - Subring
  - "#Algebra"
---
## Ring

#Ring
>[! def |*] Ring
>A triple $(A,+,\times)$ where $+$ and $\times$ are two binary operations on a set is called a ring if 
>1. $(A,+)$ is a commutative group.
>2. $\times$ is associative, and has a neutral element $1_{A}$.
>3. $\times$ is distributive with respect to $+:$ $a(b+c)=ab+ac$ and $(b+c)a=ba+ca$.

>[! def |*] Commutative Ring
>A Ring is called commutative if $\times$ is commutative.

Here are some easy conclusions of a Ring.

>[! prp | 1]
> $A$ is a ring, then $0_{A}\times x=x\times0_{A}=0_{A}$.
- $x+0x=x(1+0)=x$ for arbitrary $x\in A$.

>[! prp |2]
> $(-1_{A})\times x=x\times (-1_{A})=-x$, where $-x$ is the additive inverse of $x\in A$.
- $x+(-1_{A})x=(1+(-1))x=0x=0$ for arbitrary $x\in A$.

>[! prp |3]
> $a(b-c)=ab-ac$, and $(b-c)a=ba-ca$
- Proof is trivial by applyint previous proposition and distributive law.

>[! example |*]
>1. Triples $(\mathbb{Z}, +, \times)$, $(\mathbb{Q}, +, \times)$, $(\mathbb{R}, +, \times)$, and $(\mathbb{C}, +, \times)$ are commutative ring.
>2. Triples $(\mathcal{M}(\mathbb{Z}), +, \times)$, $(\mathcal{M}(\mathbb{Q}), +, \times)$, $(\mathcal{M}(\mathbb{R}), +, \times)$, and $(\mathcal{M}(\mathbb{C}), +, \times)$ are non commutative group when $n\geq 2$.


---

## Subrings

#Subring
>[! def |*] Subring
>A subset $B$ of a ring $A$ is called a subring if
>1. $B$ is stable under $+$, and $(B,+)$ is a subgroup of $A$
>2. $B$ is stable under $\times$
>3. $B$ contains $1_{A}$
- We use the same notation $B\leq A$ for ring relation.

>[! exm |*]
>1. $(\mathbb{Z}, +, \times)\leq (\mathbb{Q}, +, \times)\leq (\mathbb{R}, +, \times)\leq (\mathbb{C}, +, \times)$  
>2. $(\mathcal{M}(\mathbb{Z}, +, \times))\leq (\mathcal{M}(\mathbb{Q}, +, \times))\leq (\mathcal{M}(\mathbb{R}, +, \times))\leq (\mathcal{M}(\mathbb{C}, +, \times))$ 


We say that $\{0\}$ is a trivial ring, and in fact $A$ is a trivial ring if and only if $0_{A}=1_{A}$.
- [[Ring (Proof)#^d0aa6d|Proof]]

>[! def |*] Center
>If $A$ is a ring, we set $Z(A)=\{z\in A: zx=xz, \forall x\in A\}$ and call this subset the center of $A$.

>[! prp |*] 
>If $A$ is a ring, then $Z(A)\leq A$ and $Z(A)=A$ if and only if $A$ is commutative.
- Proof is trivial










