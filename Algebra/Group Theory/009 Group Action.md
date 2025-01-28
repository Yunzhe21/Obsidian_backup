---
tags:
  - GroupAction
  - Orbit
  - Transitive
  - Stabilizer
  - Orbit-StabilizerTheorem
  - ClassFormula
  - G-Space
  - p-Group
  - Algebra
---
## Group Action

#GroupAction
>[! def |*] Group Action
>Let $G$ be a group and $X$ be a set, a map $G\times X\overset{f}{\rightarrow} X$ is an action of $G$ on $X$ if 
>1. $\forall x\in X$, $e.x =x$ 
>2. $\forall g, h\in G$, $\forall x\in X$, $g.(h.x)=(gh).x$ 

### Examples

1. $X$ is a set, then $\mathfrak{S}_{X}\times X\longrightarrow X$ as $(\varphi, x)\longmapsto \varphi(x)$ is a group action
- [[Group Action (Proof)#^a8b8d9|Verify]]
2. $V$ is vector space, then $Gl(V)\times V\rightarrow V$ as $(g, v)\longmapsto g(v)=gv$
- Verify: Just routine
3. A). $G\times G\rightarrow G$ as $(g, g')\longmapsto gg'$
3. B). $G\times G\rightarrow G$ as $(y,x)\longmapsto xy^{-1}$ 
3. C). $G\times G\rightarrow G$ as $(g,x)\longmapsto gxg^{-1}$ 

### Proposition

<font color="#ff0000">Another point of view</font> of Group Action, which is the exact definition in Serge Lang's book.

1. If $G\times X\to X: (g,x)\mapsto g. x$ is a group action, then for any $g\in G$, ${} \varphi(g): X\to X {}$ as ${} x\mapsto g. x\in\mathfrak{S}_{X} {}$. Moreover, $\varphi: G\to\mathfrak{S}_{X}$ as $g\mapsto \varphi(g)\in Hom(G,\mathfrak{S}_{X})$.
	- [[Group Action (Proof)#^159ba7|Proof]]

2.  Conversely, if $\varphi:G\to\mathfrak{S}_{X}\in Hom(G,\mathfrak{S}_{X})$, then the map ${} G\times X\to X: (g,x)\mapsto\varphi(g)(x)=:g. x {}$ is an action of $G$ on $X$.
	- Proof is simple, we omit it.

The following proposition indicates that a Group Action creates an equivalent relation.

>[! prp |*] 
>Suppose $G\times X\rightarrow X$ as ${} (g, x)\longmapsto g.x {}$ is an action of $G$ on $X$, then the notion $x\sim y$ if there exists $g\in G$ s.t. $y=g.x$ is an equivalent relation on $X$
- [[Group Action (Proof)#^505a5a|Proof]] 

---

## Orbit-Stabilizer Theorem

### Orbit

#Orbit 
>[! def |*] Orbit
>If $G\times X\to X$ is an action of $G$ on $X$, then $Cl_{\sim}(x)$ is called the $(G,\cdot)$ orbit of $x$. Note that $Cl_{\sim}(x)=\{g.x|g\in G\}$. 

<font color="#ff0000">Notation:</font> $G.x:=Cl_{\sim}(x)$ or $O_{X}:=Cl_{\sim}(x)$.

<font color="#ff0000">Example:</font> Let $V$ be a $K$ -vector space of dimension $n$. The orbit for $GL(V)\times V\to V: (g,v)\to g(v)$ are $V-\{0\}$ and $\{0\}$.
- [[Group Action (Proof)#^4878be|Proof]] ^666d1c

### Transitivity

#Transitive 
>[! def |*] Transitive
>One say the action of $G$ on $X$ is transitive if there exists $x\in X$ such that ${} X=G.x {}$, which is also equivalent to say for all $x\in X$, $X=G.x$.

Recall our previous [[009 Group Action#^666d1c|Example]], it's easy to see that $GL_{n}(V)$ is transitive on $V-\{0\}$.

<font color="#ff0000">Example:</font> $\mathfrak{S}_{n}\times \{1, \cdots, n\}\to\{1,\cdots, n\}$ is transitive.
- [[Group Action (Proof)#^098b1f|Proof]]

### Stabilizer

>[! def |*] Stabilizer
>If $G\times X\to X$ is an action of $G$ on $X$, then stabilizer of $x$ in $G$ is $\text{Stab}_{G}(x)=\{g\in G, g.x=x\}$.

<font color="#ff0000">Fact:</font> $\text{Stab}_{G}(x)\leq G$
- Trivial

#### Examples

1. $\mathfrak{S}_{n}\times\{1,\cdots,n\}\to\{1,\cdots,n\}$, then ${} \text{Stab}_{\mathfrak{S}_{n}}(n)\sim\mathfrak{S}_{n-1} {}$, where $\text{Stab}_{\mathfrak{S}_{n}}(n)=\{\sigma\in\mathfrak{S}_{n}:\sigma(n)=n\}$
	- [[Group Action (Proof)#^1d853d|Proof]]

2. Let $H\leq G$, then the map $G\times \frac{G}{H}\to \frac{G}{H}$ as $(g,g'H)\to gg'H$ defines a transitive action $G$ on $\frac{G}{H}$. For this action, $\text{Stab}_{G}(eH)=H$ 

### The Theorem

#Orbit-StabilizerTheorem 
>[! thm |*] Orbit-Stabilizer Theorem
>If $G$ acts on $X$, then the map ${} \varphi_{x}: \frac{G}{\text{Stab}_{G}(x)}\to G.x {}$ as $g\text{Stab}_{G}(x)\mapsto g.x$ is well-defined and bijective. In particular if $G$ and $X$ are finite, then $|G.x|=\frac{|G|}{|\text{Stab}_{G}(x)|}$
- [[Group Action (Proof)#^e39246|Proof]]

In particular, if the action is transitive, then $\frac{G}{\text{Stab}_{G}(x)}\sim X$  

#ClassFormula 
>[! cor |*] Class Formula
>If $X$ is finite and the partition of $X$ into $G$ -orbits is given by ${} X=\bigcup_{i=1}^{r}G.x_{i} {}$, then ${} |X|=\sum\limits_{i=1}^{r}|G.x_{i}| {}$. Moreover, if $G$ is finite, then $|X|=\sum\limits_{i=1}^{r}\frac{|G|}{|\text{Stab}_{G}(x_{i})|}$. 

^c623d1

#G-Space 
>[! def |*] G-Space
>Let $G$ be a group, we say that $X$ is a $G$ -space if $G$ acts on $X$.

>[! def |*] G-equivariant
>If $X$ and $Y$ are two $G$ -spaces, we say that a map $\varphi: X\to Y$ is $G$ -equivariant if $\varphi(g.x)=g.\varphi(x)$ 


---

## $p$ -Group

#p-Group 
>[! def |*] $p$ -Group
>If $p$ is a prime number, one call $G$ a $p$ -Group if it is finite and has cardinality $|G|=p^{a}$ for some $a\in\mathbb{N}$.
- By [[004 Quotient Group#^LagrangeThm|Lagrange Theorem]], it is immediate that the subgroup of a $p$ -group is a $p$ -group.

>[! def |*] 
>If $X$ is a $G$ -space, we set $X^{G}=\{x\in X: \forall g\in G, g.x=x\}$. In other word, $X^{G}$ denotes fix points of $X$ up to group action $G$.

### Application

>[! thm | *]
>Let $G$ be a $p$ -group for some prime number $p$, and $X$ be a finite set, then $|X|\equiv |X^{G}| \text{ mod } p$ 
- [[Group Action (Proof)#^8b8753|Proof]]

>[! cor |*]
If $G$ is a non-trivial $p$ -group for some prime number $p$, then $Z(G)$ is not reduced $\{e\}$.
- [[Group Action (Proof)#^5487f8|Proof]]

>[! example | 1]
>Let $G$ be a group with order $p^2$ where $p$ is a prime number, then $G$ is commutative.
- [[Group Action (Proof)#^b48fac|Proof]]

---

## Example

> [! example |*]
> Let $\mathbb{H} = \{x\in\mathbb{C}, Im(z) > 0\}$, also called Poincaré upper half plane. For 
> $\begin{pmatrix} a&b \\c&d \end{pmatrix}\in SL_{2}(\mathbb{R})$ and $z\in\mathbb{H}$, define the operation as $g.z = \frac{az+b}{cz+d}$
> 1. Prove that this defines an action of $SL_{2}(\mathbb{R})$ on $\mathbb{H}$
> 2. Prove it's transitive
> 3. Find ${} \text{Stab}_{SL_{2}(\mathbb{R})}(i) {}$
> 4. Prove that $SL_{2}(\mathbb{R})/SO_{2}(\mathbb{r})\sim\mathbb{H}$ 

Proof: 
1. Check if $z\in\mathbb{H}$ and $g\in SL_{2}(\mathbb{R})$ implies $g.z\in\mathbb{H}$. Suppose that $Im(z)>0$ and $y$ is such invertible matrix with $ad-bc = 1$, $cz+d\neq0$ (this condition is implicitly given since the only way for $cz+d = 0$ is both $c,d$ are $0$, which contradicts invertibility of the matrix), then $\frac{az+b}{cz+d} = \frac{(az+b)(\overline{c}\overline{z}+\overline{d})}{|cz+d|^{2}}$, write $z = x+iy$ and by simple calculation, we get $Im\left(\frac{az+b}{cz+d}\right)>0$. Finally, check whether it's a group action. First of all, $I_{2}.z = z$ is simple, secondly, take $\begin{pmatrix} a&b \\ c&d \end{pmatrix}$ and $\begin{pmatrix} \alpha &\beta \\ \gamma &\delta \end{pmatrix}\in SL_{2}(\mathbb{R})$, $\begin{pmatrix} a&b \\ c&d \end{pmatrix}\left(\begin{pmatrix} \alpha &\beta \\ \gamma &\delta \end{pmatrix}. z\right) = \frac{(a\alpha +b\beta)z+a\beta+b\delta}{(c\alpha +d\gamma)z + c\beta+b\delta} = \begin{pmatrix} a\alpha+b\gamma&a\beta+b\delta \\ c\alpha+d\gamma&c\beta+d\delta \end{pmatrix}\cdot z$, thus the statement is proved.
2. Notice that $\begin{pmatrix} a&b \\ 0&a^{-1} \end{pmatrix}. i = a^{2}i+ab$, then for $x+iy\in\mathbb{H}$, set $a=\sqrt{y}, b = \frac{x}{\sqrt{y}}$, then $x+iy = \begin{pmatrix} a&b \\ 0&a^{-1} \end{pmatrix}$, then it's transitive.
3. Suppose that $\begin{pmatrix} a&b \\ c&d \end{pmatrix}\in \text{Stab}_{SL_{2}(\mathbb{R})}(i)$, then $\frac{ai+b}{ci+d} = i$, which implies $a = d, b =  -c$, thus it will be of the form $\begin{pmatrix} a&-c \\ c&a \end{pmatrix}$, also, since $a^{2}+c^{2}$, this is exactly the $SO(2)$ group.
4. By the Orbit-Stabilizer Theorem, $\frac{SL_{2}(\mathbb{R})}{SO_{2}(\mathbb{R})}\sim \mathbb{H}$. 




