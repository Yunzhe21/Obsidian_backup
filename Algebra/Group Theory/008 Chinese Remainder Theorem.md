---
tags:
  - ChineseRemainderTheorem
  - FinitelyGeneratedGroup
  - SmithNormalForm
  - "#Algebra"
---
---

## Statement

#ChineseRemainderTheorem
>[! thm |*] Chinese Remainder Theorem
>Take $a,\ b\in \mathbb{N}^{*}$, and suppose $\text{gcd}(a,b)=1$, then $\frac{\mathbb{Z}}{ab\mathbb{Z}}\sim \frac{\mathbb{Z}}{a\mathbb{Z}}\times \frac{\mathbb{Z}}{b\mathbb{Z}}$  
- [[Chinese Remainder Theorem (Proof)#^4b767d|Proof]]

#FinitelyGeneratedGroup 
>[! def |*] Finitely Generated Group
>A group $G$ that has a finite set $S$ that generates $G$, meaning that every element $g\in G$ can be written as the combination of finitely many elements in $S$ and inverses.


>[! prp |*] 
>Every subgroup of $\mathbb{Z}^{n}$ is finitely generated.
- [[Chinese Remainder Theorem (Proof)#^5f1331|Proof]]

Here we introduce a new concepts that may seem arbitrary.

#SmithNormalForm
>[! def |*] Smith Normal Form
>A matrix is called of Smith Normal form if it is of the form $$
\begin{pmatrix}
  \alpha_{1}& \cdots & 0 & 0 & \cdots & 0\\
  \vdots& \ddots & \vdots & \vdots & \ddots & \vdots\\
  0& \cdots & \alpha_{r} & 0 & \cdots & 0\\
  0& \cdots & 0 & 0 & \cdots & 0\\
  \vdots& \ddots & \vdots & \vdots & \ddots & \vdots\\
  0& \cdots & 0 & 0 & \cdots &0
\end{pmatrix}
$$ where $\alpha_{i}\mid\alpha_{i+1}, \alpha_{i}>0$.

The notion of Smith Normal Form is important in our discussion of the next theorem. However, some proposition relating to it can not be done without the study of Ring Theory, which will be presented in the next section. But for now, we will use some definitions with little explanation.

>[! prp |*] 
>Every integral $A$ (matrix with integer entries) can be reduced to Smith Normal Form by row and column operation.
- [[Chinese Remainder Theorem (Proof)#^345d52|Proof]]

Now we can state **the classification of finitely generated commutative group**.

>[! thm |*] Classification of Finitely Generated Commutative Group
>Let $A$ be a finitely generated commutative group, then there exists a unique $m\in\mathbb{N}$, a unique $r\in\mathbb{N}$, and a unique sequence of positive integers $(d_{1}, \cdots, d_{r})$ at least **greater** than 2 with $d_{i}\mid d_{i+1}$ such that $A\sim \mathbb{Z}^{m}\times\frac{\mathbb{Z}}{d_{1}\mathbb{Z}}\times\cdots\times\frac{\mathbb{Z}}{d_{r}\mathbb{Z}}$. 
>- If $m=0$, then $\mathbb{Z}^{m}\times\frac{\mathbb{Z}}{d_{1}\mathbb{Z}}\times\cdots\times\frac{\mathbb{Z}}{d_{r}\mathbb{Z}}=\frac{\mathbb{Z}}{d_{1}\mathbb{Z}}\times\cdots\times\frac{\mathbb{Z}}{d_{r}\mathbb{Z}}$. 
>- If $r=1$, then it's equal to $\mathbb{Z}^{m}$. 
>- If $m,r=0$, then it's equal to $\{0\}$.
- [[Chinese Remainder Theorem (Proof)#^6a7cf2|Proof]]

>[! thm|*] 
>Let $G$ be a finite commutative group, then there exists a unique $r\in\mathbb{N}^{*}$ and a unique sequence of positive integers $(d_{1}, \cdots, d_{r})$ with $d_{i}\mid d_{i+1}$ such that $G\sim\frac{\mathbb{Z}}{d_{1}\mathbb{Z}}\times\cdots\times\frac{\mathbb{Z}}{d_{r}\mathbb{Z}}$ 
- This is a natural corollary of previous Theorem, since finite commutative group is itself a finitely generated commutative group. Also, $\mathbb{Z}^{m}$ shouldn't occur, otherwise it would not be finite.

If a finite commutative group is written as the above form, we call that such group is under the **standard form**. 

---

## Example

Put the group $G=\frac{\mathbb{Z}}{45\mathbb{Z}}\times \frac{\mathbb{Z}}{105\mathbb{Z}}\times \frac{\mathbb{Z}}{40\mathbb{Z}}\times \frac{\mathbb{Z}}{12\mathbb{Z}}$ under standard form.

*Solution:* Factorize 45, 105, 40, 12 and we have
$G\sim \frac{\mathbb{Z}}{3^{2}\mathbb{Z}}\times \frac{\mathbb{Z}}{5\mathbb{Z}}\times \frac{\mathbb{Z}}{3\mathbb{Z}}\times \frac{\mathbb{Z}}{5\mathbb{Z}}\times \frac{\mathbb{Z}}{7\mathbb{Z}}\times \frac{\mathbb{Z}}{2^{3}\mathbb{Z}}\times \frac{\mathbb{Z}}{5\mathbb{Z}}\times \frac{\mathbb{Z}}{2^{2}\mathbb{Z}}\times \frac{\mathbb{Z}}{3\mathbb{Z}}$
	2 appears with power: 0, 2, 3
	3 appears with power: 1, 1, 2
	5 appears with power: 1, 1, 1
	7 appears with power: 0, 0, 1
	So the standard form is $G\sim \frac{\mathbb{Z}}{3\cdot 5\mathbb{Z}}\times \frac{\mathbb{Z}}{2^{2}\cdot 3\cdot 5\mathbb{Z}}\times \frac{\mathbb{Z}}{2^{3}\cdot 3^{2}\cdot 5\cdot 7\mathbb{Z}}$

