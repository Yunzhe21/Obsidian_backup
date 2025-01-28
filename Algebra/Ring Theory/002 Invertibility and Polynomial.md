---
tags:
  - Algebra
  - Invertibility
---

---
## Invertibility 

#Invertibility
>[! def |*] Invertible
>If $A$ is a ring, then $x\in A$ is invertible if $\exists y\in A$ such that $xy=yx=1_{A}$
- Note that the $y$ is unique 
- Notation: $A^{\times}=\{\text{invertible elements in } A\}$ 

>[! prp |*]
>If $A$ is a ring, then $(A^{\times}, \times)$ is a group.
- [[Ring (Proof)#^d86342|Proof]]

---

## Polynomial

If $A$ is a commutative ring, then we set ${} A[X]=\left\{\sum\limits_{k=0}^{\infty}a_{k}X^{k}: a_{k}\in A, \text{and }\exists k_{0}\in\mathbb{N}\text{ such that } a_{k}=0\text{ for all }k>k_{0}\right\} {}$  
- Note that this definition is not entirely rigorous and we take for granted that for $P, Q\in A[X]$, $P=Q$ if and only if all its "cordinates" are the same.


>[! def |*]
>Let $A$ be a commutative ring. For $P=\sum\limits_{k=0}^{\infty}a_{k}X^{k}$ and $Q=\sum\limits_{k=0}^{\infty}b_{k}X^{k}$ in $A[X]$, we set $P+Q=\sum\limits_{k=0}^{\infty}(a_{k}+b_{k})X^{k}$ and $PQ=\sum\limits_{k=0}^{\infty}c_{k}X^{k}$, where $c_{k}=\sum\limits_{i=0}^{k}a_{k-i}b_{k}$.


>[! prp |*]
>Let $A$ be a commutative ring, then $(A[X], +, \times)$ is a commutative ring with $1_{A[X]}=1_{A}\times X^{0}$ and $0_{A[X]}=0_{A}\times X^{0}$. For $k,l\in\mathbb{N}$, we have $X^{k}\times X^{l}=X^{k+l}$.


