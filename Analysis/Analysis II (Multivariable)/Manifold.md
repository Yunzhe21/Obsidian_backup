---
tags:
  - "#Manifold"
  - "#TangentSpace"
  - TangentVector
---
## Manifold

The concept of **Manifold** is used to describe a topological space that **locally** "like" euclidean $E^{r}$, for some $r$. This $r$ is called the dimension of the manifold.

We approach the idea of manifold from a rather concrete viewpoint. A manifold $M$ is a subset of some euclidean $E^{n}$ that can locally be described by an equation $\boldsymbol{\Phi}(\textbf{x})=\textbf{0}$, where $D\boldsymbol{\Phi}(\textbf{x})$ must have maximum rank. 

 #Manifold 
>[! def |*] $r$ - Manifold
>Let $1\leq r<n$, $q\geq 1$. A nonempty set $M\subset E^{n}$ is a manifold of dimension $r$ and class $\mathscr{C}^{(q)}$ if $M$ has the property that for every $\textbf{x}_{0}\in M$, there exist a neighborhood $U$ of $\textbf{x}_{0}$ and $\boldsymbol{\Phi}=(\Phi^{1}, \cdots, \Phi^{n-r})$ of class $\mathscr{C}^{(q)}$ on $U$, such that $D\boldsymbol{\Phi}(\textbf{x})$ has rank $n-r$ for every $\textbf{x}\in U$ and $M\cap U=\{\textbf{x}\in U:\boldsymbol{\Phi}(\textbf{x})=\textbf{0}\}$.

In our following discussion, we will only consider $\boldsymbol{\Phi}$ of class $\mathscr{C}^{1}$. So for simplicity, we just call it $r$ -manifold. We also call any subset of $E^{n}$ an $n$ -manifold.

### Intuition of $r$ -manifold

Let us indicate how an $r$ -manifold is locally like $E^{r}$. First assume that $\tilde{J}\boldsymbol{\Phi}(\textbf{x}_{0})\neq 0$ with $\tilde{J}\boldsymbol{\Phi}(\textbf{x}_{0})$ defined as before. Define $\textbf{f}$ as in the proof of the [[Differentiation of real-valued Functions (Proof)#^5bb822|Implicit Function Theorem]]. The neighborhood in the proof need not coincide with that in the definition of manifold, we call the former one $U_{1}$, $R$ in the previous proof as $R_{1}$. We may suppose that $U_{1}\subset U$. Now $\textbf{f}|_{U_{1}}$ is a [[Differential Mappings#^3b5902|Regular Tranformation]] and $\textbf{f}(M\cap U_{1})=\{(\hat{\textbf{x}},\textbf{0}):\hat{\textbf{x}}\in R_{1}\}$ is a relatively open subset of the $r$ -dimensional subspace of $E^{n}$ spanned by $e_{1}, \cdots, e_{r}$. Therefore it is reasonable to say that $M\cap U_{1}$ is like $E^{r}$.

### Examples

<font color="#ff0000">Example 1:</font> Let $H$ be the hyperbola $x^{2}-y^{2}=1$, show that $H$ is a $1$ -manifold.
- Take $\Phi(x,y)=x^{2}-y^{2}-1$, then $D\Phi(x,y)=2x\textbf{e}^{1}-2y\textbf{e}^{2}$. If $(x,y)\neq\textbf{0}$, then $D\Phi(x,y)\neq\textbf{0}$ and the rank is $1$. Given $(x_{0},y_{0})\in H$, let $U$ be any neighborhood of $(x_{0},y_{0})$ that does not contain $(0,0)$.

In the previous example, the choice of $\Phi$ is not dependent on $(x_{0},y_{0})$, however, the next example requires us to find different $\Phi$.

<font color="#ff0000">Example 2:</font> Let $M$ be the union of $H$ and one of its asymptotes, $M=\{(x,y):x^{2}-y^{2}=1\}\cup\{(x,y):y=x\}$. Show that $M$ is a $1$ -manifold.
- If $(x_{0},y_{0})\in H$, then we let $\Phi(x,y)=x^{2}-y^{2}-1$ as before, and let $U$ be any neighborhood of $(x_{0},y_{0})$ that does not meet the asymptote $y=x$. However, if $(x_{0},y_{0})$ is on the asymptote, take $\Phi(x,y)=y-x$ and $U$ be any neighborhood that does not meet $H$. 

<font color="#ff0000">Example 3:</font> Let $M=\{(x,y):x^{2}=y^{2}\}$. This set consists of two lines $y=\pm x$, and is not a $1$ -manifold.
- Consider $(0,0)$.

For most examples of manifolds that we consider are obtained in the following way. Let ${} \boldsymbol{\Phi} {}$ be a transformation of class $\mathscr{C}^{(1)}$, from an open set $D\subset E^{n}$. Let $M=\{\textbf{x}:\boldsymbol{\Phi}(\textbf{x})=\textbf{0} \text{ and } D\boldsymbol{\Phi}(\textbf{x})\text{ has rank }m\}$. If $M$ is not empty, then it is a $r$ -manifold.

To show that $M$ is a $r$ -manifold. Since $\{\textbf{x}:D\boldsymbol{\Phi}(\textbf{x})\text{ has rank }m\}$ is open (verify). Hence any $\textbf{x}_{0}\in M$ has a neighborhood $U$ such that $D\boldsymbol{\Phi}$ has rank m. So there is no need to worry about whether the rank condition holds in some neighborhood.

>[! def |*] 
>When $M=\{\textbf{x}:\boldsymbol{\Phi}(\textbf{x})=\textbf{0} \text{ and } D\boldsymbol{\Phi}(\textbf{x})\text{ has rank }m\}$ holds, we say $M$ is the $r$ -manifold determined by $\boldsymbol{\Phi}$.

<font color="#ff0000">Example 4:</font> The $(n-1)$ -sphere $\{\textbf{x}:|\textbf{x}|=1\}$ is an $(n-1)$ -manifold. Particularly, it is a $(n-1)$ -manifold determined by $\Phi(\textbf{x})=|\textbf{x}|^{2}-1$. The only critical point is $\textbf{0}$, which is not on the sphere.

<font color="#ff0000">Example 5:</font> Let $F$ be real-valued and of class $\mathscr{C}^{(1)}$. Consider the level set $B_{c}=\{\textbf{x}:F(\textbf{x})=c\}$. Let $\Phi(\textbf{x})=F(\textbf{x})-c$. Then $d\Phi(\textbf{x})=dF(\textbf{x})$. If $B_{c}$ is not empty and contains no critical points of $F$, then $B_{c}$ is the $(n-1)$ -manifold determined by $\Phi$. Otherwise, just exclude those critical points.

---

## Tangent vectors to a manifold

Let $M$ be a manifold and $\textbf{x}_{0}\in M$.

#TangentVector
>[! def |*] Tangent Vector
>A vector $\textbf{h}$ is a **tangent vector** to $M$ at $\textbf{x}_{0}$ id there exists a function $\boldsymbol{\psi}$ from an interval $(-\delta,\delta)$ into $M$ such that $\boldsymbol{\psi}(0)=\textbf{x}_{0}$ and $\boldsymbol{\psi}'(0)=\textbf{h}$.

### Geometric Implication

Geometrically, let $\textbf{x}_{t}=\textbf{x}_{0}+t\textbf{h}$, then $\textbf{h}$ is a tagent vector if for some $\delta>0$, there exists $\textbf{y}_{t}\in M$ such that whenever $0<|t|<\delta$, $\lim_{t\to0}\frac{|\textbf{y}_{t}-\textbf{x}_{t}|}{|t|}=0$. If we set $\boldsymbol{\psi}(t)=\textbf{y}_{t}$ for $0<|t|<\delta$, and $\boldsymbol{\psi}(0)=\textbf{x}_{0}$, then $\lim_{t\to0}\frac{|\textbf{y}_{t}-\textbf{x}_{t}|}{|t|}=0$ implies that $\boldsymbol{\psi}'(0)=\textbf{h}$.

#TangentSpace
>[! def |*] Tangent Space
> $T(\textbf{x}_{0})$ is called the tangent space to $M$ at $\textbf{x}_{0}$ if it contains all tangent vectors at $\textbf{x}_{0}$.

Since we say $M$ is a $r$ -manifold, then it is plausible that the tangent space is a vector space of dimension $r$.

>[! thm |*] 
>The tangent space $T(\textbf{x}_{0})$ is the kernel of the linear transformation $D\boldsymbol{\Phi}(\textbf{x}_{0})$.
>

^b78b3f

- [[Manifold (Proof)#^5db12f|Proof]]

---

## Normal vectors to a manifold

A vector $\textbf{n}$ is called normal to $M$ at $\textbf{x}_{0}$ if $\textbf{n}\cdot\textbf{h}=0$ for every $\textbf{h}\in T(\textbf{x}_{0})$.

The normal vector form a vector space of dimension $m=n-r$, the orthogonal complement of the tangent space $T(\textbf{x}_{0})$.

Denote the gradient ${} \text{grad}\boldsymbol{\Phi}^{l}(\textbf{x}_{0}) {}$ the vector with the same component as the covector $d\boldsymbol{\Phi}^{l}(\textbf{x}_{0})$. Thus by [[Manifold#^b78b3f|Theorem]], $\text{grad}\boldsymbol{\Phi}^{l}(\textbf{x}_{0})\cdot\textbf{h}=d\boldsymbol{\Phi}^{l}(\textbf{x}_{0})\cdot\textbf{h}=0$ for every $\textbf{h}\in T(\textbf{x}_{0})$, $l=1, \cdots, m$. Hence $\text{grad}\boldsymbol{\Phi}^{1}(\textbf{x}_{0}), \cdots, \boldsymbol{\Phi}^{m}(\textbf{x}_{0})$ are normal vectors to $M$ at $\textbf{x}_{0}$. Since $D\boldsymbol{\Phi}(\textbf{x}_{0})$ has rank $m$, by the fact that $\text{rank}A = \text{rank}A^{T}$, these vectors are linearly independent.

>[! cor |*] 
>The gradients $\text{grad}\boldsymbol{\Phi}(\textbf{x}_{0}), \cdots, \text{grad}\boldsymbol{\Phi}^{m}(\textbf{x}_{0})$ form a basis for the space of normal vectors to $M$ at $\textbf{x}_{0}$.

## Tangent $r$ -planes

The $r$ -plane tangent to $M$ at $\textbf{x}_{0}$ is $\{\textbf{x}:\textbf{x}_{0}+\textbf{h}, \textbf{h}\in T(\textbf{x}_{0})\}$. The term tangent line, tangent plane, and tangent hyperplane are used when $r=1,2$, and $n-1$. The tangent $r$ -plane can also be interpreted as $\{\textbf{x}: \text{grad}\boldsymbol{\Phi}^{l}\cdot(\textbf{x}-\textbf{x}_{0}) \text{ for } l=1, \cdots, m\}$.






