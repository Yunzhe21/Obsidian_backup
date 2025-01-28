---
tags:
  - "#TaylorExpansion"
---

>[! def |*]
>If $\textbf{x}_{0}$ is a point of $A$ such that $f(\textbf{x}_{0})\leq f(\textbf{x})$ for every $\textbf{x}\in A$, then $f$ has an **absolute minimum** ar $\textbf{x}_{0}$. The number $f(\textbf{x}_{0})=\inf\{f(\textbf{x}):\textbf{x}\in A\}$ is the minimum value of $f$ on $A$. (There need not exist such $\textbf{x}_{0}$ in many cases)


>[! def |*] 
>We say that $f$ has a **relative minimum** at $\textbf{x}_{0}$ if there is a neighborhood $U$ of $\textbf{x}_{0}$ such that $f(\textbf{x}_{0})\leq f(\textbf{x})$ for every $\textbf{x}\in A\cap U$ 

The **absolute maximum** and **relative maximum** and be defined easily in the similar manner.

>[! def |*] Critical Point
>A point $\textbf{x}_{0}$ is a **critical point** of $f$ if $df(\textbf{x}_{0})=\textbf{0}$.
- If $f$ is a differentiable function, one need look at the critical points of $f$ in order to find minimal and maximal value.

---

## Conclusions relating to Max & Min


>[! prp |*]
>If $f$ has a relative extremum at $\textbf{x}_{0}$ and $f$ is differentiable at $\textbf{x}_{0}$, then $\textbf{x}_{0}$ is a critical point of $f$
-  [[Differentiation of real-valued Functions (Proof)#^81c654|Proof]]

Recall **second order derivative test** from single variable calculus, we try to construct something similar. 

Let $f$ be a function of class $\mathscr{C}^{(2)}$ on $A$, and let $Q$ be the function with domain $A\times E^{n}$ defined by the formula $Q(\textbf{x},\textbf{h})=\sum\limits_{i,j=1}^{n}f_{ij}(\textbf{x})h^{i}h^{j}$.
$Q(\cdot, \textbf{h})$ is essentially a [[003 Symmetric Matrix and Quadratic Forms#^d07d28|quadratic]] form corresponding to a matrix $(f_{ij}(\textbf{x}))$， which is symmetric.

In preparation for the theorem discussed below, we use the following notation. $U$ is a neighborhood of a critical point $\textbf{x}_{0}$, whose radius is small enough such that $U\subseteq A$. Points of $U$ are denoted by $\textbf{x}$, ${} \textbf{h}=\textbf{x}-\textbf{x}_{0} {}$. Since $U$ is convex, we can apply #TaylorExpansion  and get $f(\textbf{x})=f(\textbf{x}_{0})+df(\textbf{x}_{0})\cdot\textbf{h}+\frac{1}{2}Q(\textbf{x}_{0}+s\textbf{h}, \textbf{h})$. Since $\textbf{x}_{0}$ is a critical point, $df(\textbf{x}_{0})=0$, then the Taylor expansion becomes $f(\textbf{x})=f(\textbf{x}_{0})+\frac{1}{2}Q(\textbf{x}_{0}+s\textbf{h}, \textbf{h})$

To say that $f$ has a relative minimum at $\textbf{x}_{0}$ is equivalent to say $Q(\textbf{x}_{0}+s\textbf{h}, \textbf{h})\geq 0$ for all $\textbf{x}\in U$. **But** this condition on $Q$ is **difficult to apply**, so we put our attention to the following theorem that depends on the sign of $Q$ at the critical point $\textbf{x}_{0}$.

>[! thm |*]
>Let $f$ be of class $\mathscr{C}^{(2)}$ on an open set $A$, and $\textbf{x}_{0}\in A$ a critical point. Then:
>1. $\textbf{x}_{0}$ is a relative minimum, then $Q(\textbf{x}_{0}, \cdot)\geq 0$.
>2. $Q(\textbf{x}_{0}, \cdot)>0$, then $\textbf{x}_{0}$ is a strict relative minimum.
>3. $\textbf{x}_{0}$ is a relative maximum, then $Q(\textbf{x}_{0},\cdot)\leq 0$
>4. If $Q(\textbf{x}_{0}, \cdot)<0$, then $\textbf{x}_{0}$ is a strict relative maximum.
- Proof: [[Differentiation of real-valued Functions (Proof)#^666d5b|1)]]. [[Differentiation of real-valued Functions (Proof)#^9c23a1|2)]].

<font color="#ff0000">Remark:</font> Notice that this theorem works only on a open set $A$, thus if we aim to find the extremum at the boundary of $A$, or say we want to find extremum of closed $A$, where the extremum can exists on the boundary, we will need more advanced technique (**Lagrange multiplier**)

Let $d_{n}(\textbf{x})=\det(f_{ij}(\textbf{x}))$ denote the determinant of the matrix of second order derivatives. This determinant is called the **Hessian**. This matrix itself can be called **Hessian matrix**.

>[! def |*]
>A critical point $\textbf{x}$ is non-degenerate if the Hessian determinant $d_{n}(\textbf{x})$ is not 0.

Next, we will discuss the behavior of $f$ near a nondegenerate critical point, which is determined by that of the quadratic function $Q(\textbf{x},\cdot)$. We will state **three criteria** according to which one can test whether a nondegenerate critical point **gives a relative extremum**.

### Criterion I

Consider the case $n=2$, $Q(x,y,h,k)=f_{11}h^{2}+2f_{12}hk+f_{22}k^{2}$.
Since $(x,y)$ is a nondegenerate critical point, $d_{2}(x,y)=f_{11}f_{22}-f_{12}^{2}\neq 0$. 
#### Case I

If  $d_{2}>0$, then the quadratic equation $Q(x,y,h,k)=0$ has no root $(h,k)$ except $(0,0)$. Therefore, $Q(x,y,h,k)$ has the same sign for all $(h,k)\neq (0,0)$. We have $Q(x,y,h,0)=f_{11}h^{2}$ and $Q(x,y,0,k)=f_{22}k^{2}$. The sign of $f_{11}$ and $f_{22}$ determines whether $Q(x,y,\cdot,\cdot)>0$ or $Q(x,y, \cdot, \cdot)<0$. By our previous theorem, $(x,y)$ is a point of relative maximum ($f_{11}>0, f_{22}>0$) or minimum ($f_{11}<0,f_{22}<0$)

#### Case II

If $f_{11}f_{22}-f^{2}_{12}<0$, then $\{(h,k): Q(x,y,h,k)=0\}$ consists of two lines intersecting at $(0,0)$, two of which is positive, the other are negative. In this case $Q(x,y,\cdot,\cdot)$ is indefinite. A critical point where $f_{11}f_{22}-f_{12}^{2}<0$ is called a **saddle point**.

### Criterion II

For any $n$, let $d_{n}=\det(f_{ij}(\textbf{x}))$.

> $Q(\textbf{x}, \cdot)>0$ if and only if $d_{m}(\textbf{x})>0$ for all $m=1,\cdots, n$.
> $Q(\textbf{x}, \cdot)<0$ if and only if $(-1)^{m}d_{m}(\textbf{x})>0$ for all $m=1, \cdots, n$

The second criterion is not convenient if we consider large $n$.


### Criterion III

As we know from [[003 Symmetric Matrix and Quadratic Forms#^0ca38c|Linear Algebra]], any quadratic form can be written as a linear combination of squares by choosing a proper basis. Therefore $Q(\textbf{x}, \textbf{h})=\sum\limits_{i=1}^{n}\lambda_{i}(\textbf{x})[\eta^{i}(\textbf{x})]^{2}$ for each $\textbf{h}$, where $\eta^{i}$ are components of $\textbf{h}$ w.r.t the proper basis, and $\lambda_{i}$ are eigen values of the Hessian matrix.


> $Q(\textbf{x}, \cdot)>0$ if and only if ${} \lambda_{i}>0 {}$ for $i=1, \cdots, n$.
> $Q(\textbf{x}, \cdot)<0$ if and only if $\lambda_{i}<0$ for $i=1, \cdots, n$.
- Proof: If $\lambda_{i}(\textbf{x})>0$ for each $i$, then $Q(\textbf{x}, \textbf{h})>0$ unless $\textbf{h}=\textbf{0}$. In this case $Q(\textbf{x}, \cdot)$ is positive definite. Conversely, if $\textbf{h}=\textbf{v}_{i}(\textbf{x})$, then $Q(\textbf{x},\textbf{h})=\lambda_{i}(\textbf{x})>0$


