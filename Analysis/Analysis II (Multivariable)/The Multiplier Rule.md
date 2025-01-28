---
tags:
  - MultiplierRule
---
---

## Lagrange Multiplier Rule

Let $M$ be a manifold and $f$ be a real-valued function of class $\mathscr{C}^{1}$ defined on a open set containing $M$. We aim to find the extrema of the function $f|M$. This problem is called constrained extrema.

If $\textbf{x}_{0}$ is a point of $M$ at which $f$ has a constrained relative maximum, then $\textbf{x}_{0}$ has a neighborhood $U_{0}$ such that $f(\textbf{x})\leq f(\textbf{x}_{0})$ for every $\textbf{x}\in M\cap U_{0}$.

Since $M$ is a manifold, there exists a neighborhood $U$ of $\textbf{x}_{0}$ and $\boldsymbol{\Phi}$ of class $\mathscr{C}^{1}$ on $U$ such that $M\cap U=\{\textbf{x}\in U: \boldsymbol{\Phi}(\textbf{x})=\textbf{0}\}$ and $D\boldsymbol{\Phi}(\textbf{x})$ has maximum rank $m$ for every $\textbf{x}\in U$. We may assume that $U\subseteq U_{0}$.

#MultiplierRule
>[! thm |*]  Lagrange multiplier rule
>Let $f$ have a constrained relative extremum at $\textbf{x}_{0}$. Then there exist real numbers $\sigma_{1}, \cdots, \sigma_{m}$ such that $\textbf{x}_{0}$ such that $\textbf{x}_{0}$ is a critical point of the function $F=f+\sigma_{1}\boldsymbol{\Phi}^{1}+\cdots+\sigma_{m}\boldsymbol{\Phi}^{m}$.
- The name "multiplier rule" means that this approach can translate the constrained extremum problem into ordinary extremum problem by introducing multipliers $\sigma_{1}, \cdots, \sigma_{m}$.
- [[Manifold (Proof)#^da7b6b|Proof]]

<font color="#ff0000">Example:</font> 

Let ${} f(\textbf{x})=\sum\limits_{i=1}^{n}b_{i}(x^{i})^{2} {}$, where $b_{i}\neq 0$ for each $i=1, \cdots, n$. Let $M$ be the hyperplane $\{\textbf{x}: \textbf{y}\cdot\textbf{x}=1\}$, and $F(\textbf{x})=f(\textbf{x})+\sigma(1-\textbf{y}\cdot\textbf{x})$. If $\textbf{x}_{0}$ is a critical point of $F$, then $\textbf{0}=\text{grad}F(\textbf{x}_{0})=\text{grad}f(\textbf{x}_{0})-\sigma\textbf{y}$. 

Thus, $\text{grad}f(\textbf{x}_{0})=\sigma\textbf{y}$, or in another word, $f_{i}(\textbf{x}_{0})=2b_{i}x_{0}^{i}=\sigma y^{i}$ for $i=1, \cdots, n$. From this and the equation $\textbf{y}\cdot\textbf{x}_{0}=1$, then $x_{0}^{i}=\frac{\sigma y^{i}}{2b_{i}}$, $\frac{1}{\sigma}=\frac{1}{2}\sum\limits_{i=1}^{n}\frac{(y^{i})^{2}}{b_{i}}$.

To determine whether $\textbf{x}_{0}$ gives an extremum, use the formula $f(\textbf{x}_{0}+\textbf{h})=f(\textbf{x}_{0})+\text{grad}f(\textbf{x}_{0})\cdot\textbf{h}+f(\textbf{h})$, which is true for this $f$. Points of the hyper plane $M$ are of the form $\textbf{x}_{0}+\textbf{h}$, where $\textbf{y}\cdot\textbf{h}=0$. Since $\text{grad}f(\textbf{x}_{0})=\sigma\textbf{y}$, the above formula simplifies to $f(\textbf{x}_{0}+\textbf{h})=f(\textbf{x}_{0})+f(\textbf{h})$. If $f(\textbf{h})\geq 0$ for every $\textbf{h}$ satisfying $\textbf{y}\cdot\textbf{h}=0$, then $f$ has an absolute constrained minimum at $\textbf{x}_{0}$.

### Multiplier Rule and Eigenvalue

Consider the quadratic polynomial $f(\textbf{x})=\textbf{L}(\textbf{x})\cdot\textbf{x}=\sum\limits_{i,j=1}^{n}c_{j}^{i}x^{i}x^{j}$, and let $M_{1}$ br the unit $(n-1)$ - sphere in $E^{n}$, $M_{1}=\{\textbf{x}: |\textbf{x}|=1\}$. Let $\lambda_{1}=\max\{f(\textbf{x}):\textbf{x}\in M_{1}\}$, and let $\textbf{v}_{1}$ be a point of $M_{1}$ at which the maximum is attained. By the multiplier rule, with $F(\textbf{x})=f(\textbf{x})+\sigma(1-\textbf{x}\cdot\textbf{x})$, there is a multiplier $\sigma$ such that $\textbf{v}_{1}$ is a critical point of $\textbf{F}$, $\text{grad}f(\textbf{x})=2\textbf{L}(\textbf{x})$ (verify). Hence $\textbf{0}=\text{grad}F(\textbf{v}_{1})=2\textbf{L}(\textbf{v}_{1})-2\sigma\textbf{v}_{1}$. Hence $\textbf{L}(\textbf{v}_{1})=\sigma\textbf{v}_{1}$, which shows that $\sigma$ is a characteristic value and $\textbf{v}_{1}$ is a characteristic vector. Since $f(x)=\textbf{L}(\textbf{x})\cdot\textbf{x}$, $\lambda_{1}=f(\textbf{v}_{1})=\textbf{L}(\textbf{v}_{1})\cdot\textbf{v}_{1}=\sigma\textbf{v}_{1}\cdot\textbf{v}_{1}$, and since $\textbf{v}_{1}\cdot\textbf{v}_{1}=1$, $\sigma=\lambda_{1}$. 

Next, we let ${} M_{2}=\{\textbf{x}:|\textbf{x}|=1, \textbf{x}\cdot\textbf{v}_{1}=0\} {}$, $\lambda_{2}=\max\{f(\textbf{x}):\textbf{x}\in M_{2}\}$, and $\textbf{v}_{2}\in M_{2}$ such that $f(\textbf{v}_{2})=\lambda_{2}$. We have added another constraint. Hence $M_{2}\subseteq M_{1}$ and $\lambda_{2}\leq\lambda_{1}$. Obviously, $\textbf{v}_{2}\cdot\textbf{v}_{1}=0$. For $k=3, \cdots, n$, let $M_{k}=\{\textbf{x}: |\textbf{x}|=1, \textbf{x}\cdot\textbf{v}_{i}=0, \text{for } i=1, \cdots, k-1 \}$, $\lambda_{k}=\max\{f(\textbf{x}):\textbf{x}\in\ M_{k}\}$, and $\textbf{v}_{k}\in M_{k}$ be such that $\lambda_{k}=f(\textbf{v}_{k})$. Then $\lambda_{n}\leq\lambda_{n-1}\leq\cdots\leq\lambda_{1}$ and $\{\textbf{v}_{1}, \cdots, \textbf{v}_{n}\}$ is an orthonormal basis for $E^{n}$.

Let us show by induction on $k$ that $\lambda_{k}$ is a characteristic value and $\textbf{v}_{k}$ a characteristic vector. As we've shown before that this is true if $k=1$. Let $k\geq 2$. Apply the multiplier rule with $F(\textbf{x})=f(\textbf{x})+\sigma_{1}(1-\textbf{x}\cdot\textbf{x})+\sum\limits_{i=1}^{k-1}\sigma_{i+1}\textbf{x}\cdot\textbf{v}_{i}$, we get $\textbf{0}=2\textbf{L}(\textbf{v}_{k})-2\sigma_{1}\textbf{v}_{k}+\sum\limits_{i=1}^{k-1}\sigma_{i+1}\textbf{v}_{i}$. Since $\textbf{v}_{i}\cdot\textbf{v}_{j}=0$ for $i\neq j$, we take inner product of both sides with $\textbf{v}_{j}$, then $0=2\textbf{L}(\textbf{v}_{k})\cdot\textbf{v}_{j}+\sigma_{j+1}$ for $j<k$, and $\sigma_{1}=\textbf{L}(\textbf{v}_{k})\cdot\textbf{v}_{k}=f(\textbf{v}_{k})$, or $\sigma_{1}=\lambda_{k}$.

Since $(c_{j}^{i})$ is symmetric, $\textbf{L}(\textbf{x})\cdot\textbf{y}=\textbf{x}\cdot\textbf{L}(\textbf{y})$ for all $\textbf{x},\textbf{y}$ (verify). In particular, $\textbf{L}(\textbf{v}_{k})\cdot\textbf{v}_{j}=\textbf{v}_{k}\cdot\textbf{L}(\textbf{v}_{j})$, by induction hypothesis, we have $\textbf{L}(\textbf{v}_{k})\cdot\textbf{v}_{j}=\textbf{v}_{k}\cdot(\lambda_{j}\textbf{v}_{j})=0$ if $j<k$. Hence $\sigma_{2}=\cdots=\sigma_{k}=0$ and $\textbf{L}(\textbf{v}_{k})=\lambda_{k}\textbf{v}_{k}$. 



