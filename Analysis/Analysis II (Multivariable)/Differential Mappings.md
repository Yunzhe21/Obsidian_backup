---
tags:
  - "#DualLinearMap"
  - "#AffineTransformation"
  - PartialDerivative
  - "#Jacobian"
  - FunctionClasses
  - "#CompositionLaw"
  - "#Laplacian"
  - "#Homeomorphism"
---
## Linear Transformation

The definition of a linear transformation and the corresponding results are the same as we defined in Linear Algebra, so we abbreviate it.

Here, the linear transformation (map) is assume to be from $E^{r}$ to $E^{n}$.
### Dual of a linear transformation

This is the linear transformation from the dual space $(E^{n})^{*}$ into $(E^{r})^{*}$, defined as follows. 

Let $(c_{j}^{i})$ be the linear transformation $\textbf{L}$, and $\textbf{w}^{1}, \cdots, \textbf{w}^{n}$  be covectors of the the matrix. Notice that $\textbf{w}^{i}\in (E^{r})^{*}$ for each $i$. Now, we can properly define linear transformation $\textbf{L}^{*}$.

 #DualLinearMap 
>[! def |*] Dual Linear Map
>For any covector $\textbf{a}=(a_{1}, \cdots, a_{n})$ in $(E^{n})^{*}$, let $\textbf{L}^{*}(\textbf{a})=\sum\limits_{i=1}^{n}a_{i}\textbf{w}^{i}$ 
- <font color="#ff0000">Remark:</font> The covector $\textbf{L}^{*}(\textbf{a})$ is in $(E^{r})^{*}$, since it is simply the linear combination of covectors that are in $(E^{r})^{*}$. 

$\textbf{w}^{i}=\sum\limits_{j=1}c_{j}^{i}\varepsilon^{j}$, where $\{\varepsilon^{1}, \cdots, \varepsilon^{r}\}$ is the standard basis for $(E^{r})^{*}$, and $c_{j}^{i}$ represents the i-th row and j-th column of the matrix.

If we write $\textbf{b}=\textbf{L}^{*}(\textbf{a})$, then the components of $\textbf{b}$ satisfy $b_{j}=\sum\limits_{i=1}^{n}a_{i}c_{j}^{i}$ 

### Affine transformations

#AffineTransformation 
>[! def |*] Affine Transformation
>A transformation $\textbf{g}$ is **affine** if there exists a linear transformation $\textbf{L}$ and $\textbf{x}_{0}$ such that $\textbf{g}(\textbf{t})=\textbf{L}(\textbf{t})+\textbf{x}_{0}$.

### Isometries of $E^{n}$

Refer to Linear Algebra, we omit it here.

 ---
 
## Differential Transformations (Mappings)

<font color="#ff0000">Assumption:</font> $\textbf{g}$ is a transformation from $\Delta\subset E^{r}$ into $E^{n}$.

>[! def |*] Differentiable Mapping
>A transformation $\textbf{g}$ is **differentiable** at $\textbf{t}_{0}$ if there exists a linear transformation $\textbf{L}$ (depending on $\textbf{t}_{0}$) such that $\lim_{\textbf{k}\to\textbf{0}}\frac{1}{|\textbf{k}|}[\textbf{g}(\textbf{t}_{0}+\textbf{k})-\textbf{g}(\textbf{t}_{0})-\textbf{L}(\textbf{k})]=\textbf{0}$

#Differential 
>[! def |*] Differential
>The linear transformation $\textbf{L}$ in the previous definition is called the differential of $\textbf{g}$ at $\textbf{t}_{0}$ and is denoted by $D\textbf{g}(\textbf{t}_{0})$

>[! prp |*]
>Let $\textbf{g}$ and $\textbf{G}$ be differentiable at $\textbf{t}_{0}$, then the sum is differentiable at $\textbf{t}_{0}$, and $D(\textbf{g}+\textbf{G})=D\textbf{g}(\textbf{t}_{0})+D\textbf{G}(\textbf{t}_{0})$
- The proof is natural.

Now, we wish to find the matrix associate to the differential $D\textbf{g}(\textbf{t}_{0})$. First, notice for each $\textbf{t}\in\Delta$, $\textbf{g}(\textbf{t})=g^{1}(\textbf{t})\textbf{e}_{1}+\cdots+g^{n}(\textbf{t})\textbf{e}_{n}$, the j-th partial derivative of $g^{i}$ is denoted as $g^{i}_{j}$ or $\frac{\partial g^{i}}{\partial t^{j}}$ 

>[! prp |*]
>A transformation $\textbf{g}$ is **differentiable** at $\textbf{t}_{0}$ if and only if each of its components $g^{1}, \cdots, g^{n}$ is differentiable at $\textbf{t}_{0}$. And if $\textbf{g}$ is differentiable at $\textbf{t}_{0}$, then the matrix of the linear transformation is the matrix of partial derivatives $g_{j}^{i}(\textbf{t}_{0})$
-  [[Differentiation of real-valued Functions (Proof)#^36fd77|Proof]]

#PartialDerivative 
>[! def |*] Partial Derivative
> $\textbf{g}_{j}(\textbf{t}_{0})=\lim_{s\to0}\frac{\textbf{g}(\textbf{t}_{0}+s\boldsymbol{\epsilon})-\textbf{g}(\textbf{t}_{0})}{s}$, $j=1, \cdots, r$
- From our previous proposition, we can easily see that the j-th partial derivative, namely $\textbf{g}_{j}(\textbf{t}_{0})$, is the j-th column of the matrix $(g_{j}^{i}(\textbf{t}_{0}))$

#Jacobian In the case where $r=n$ ($\textbf{g}$ maps $E^{n}$ to $E^{n}$), the determinant of the linear transformation is called the **Jacobian** of $\textbf{g}$ at $\textbf{t}$, and denoted by $J\textbf{g}(\textbf{t})$. Another way of denoting Jacobian is $\frac{\partial (g^{1}, \cdots, g^{n})}{\partial (t^{1}, \cdots, t^{n})}(\textbf{t})$

### Classes of Functions

#FunctionClasses 
>[! def |*] Function Classes
>If the components $g^{1}, \cdots, g^{n}$ are of class $\mathscr{C}^{(q)}$, $q\geq 0$, then $\textbf{g}$ is a transformation of class $\mathscr{C}^{(q)}$. 

>[! thm |*]
>Every differentiable transformation is of class $\mathscr{C}^{(0)}$. Every transformation of class $\mathscr{C}^{1}$ is differentiable.
- Proof is not hard

---

## Composition

>For most theorem in the differential calculus of transformation, one needs to assume that $\textbf{g}$ is of class $\mathscr{C}^{(1)}$ at least, an exception is the composite function theorem, in which only differentiability need to be assumed.

### Technical preparation

>[! prp |*]
>Let $\textbf{g}$ be differentiable at $\textbf{t}_{0}$. Then given $\epsilon>0$ there exists a neighborhood $\Omega_{0}$ of $\textbf{t}_{0}$ such that $\Omega\subset\Delta$ and $|\textbf{g}(\textbf{t})-\textbf{g}(\textbf{t}_{0})|\leq\epsilon|\textbf{t}-\textbf{t}_{0}|$.
- Proof ^aedaf7

The previous proposition can be made stronger if we assume $\textbf{g}$ to be of $\mathscr{C}^{1}$.

>[! prp |*]
>Let $\textbf{g}$ be of class $\mathscr{C}^{(1)}$ and $\textbf{t}_{0}\in\Delta$. Then given $\epsilon>0$ there exists a neighborhood $\Omega$ of $\textbf{t}_{0}$ such that $\Omega\subset\Delta$ and $|\textbf{g}(\textbf{s})-\textbf{g}(\textbf{t})|\leq (|D\textbf{g}(\textbf{t}_{0})|+\epsilon)|\textbf{s}-\textbf{t}|$.
- Proof ^d18699

### Composition Law

>Let $\textbf{g}$ be a transformation from an open set $\Delta\subset E^{r}$ into an open set $D\subset E^{n}$, and let $\textbf{f}$ be a transformation from $D$ into $E^{p}$.

#CompositionLaw 
>[! thm |*] 
>Let $\textbf{g}$ be differentiable at $\textbf{t}_{0}$ and $\textbf{f}$ be differentiable at $\textbf{x}_{0}=\textbf{g}(\textbf{t}_{0})$. Then the composite $\textbf{F}=\textbf{f}\circ\textbf{g}$ is differentiable at $\textbf{t}_{0}$ and $D\textbf{F}(\textbf{t}_{0})=D\textbf{f}(\textbf{x}_{0})\circ D\textbf{g}(\textbf{t}_{0})$ 
-  [[Differentiation of real-valued Functions (Proof)#^aa9300|Proof]]

From this theorem, we can derive four more commonly used corollary.

>[! cor | 1]
> Let $F=f\circ\textbf{g}$, then $F_{j}=\sum\limits_{i=1}^{n}f_{i}g_{j}^{i}$, $j=1, \cdots, r$, where $F_{j}=F_{j}(\textbf{t}_{0})$, $f_{i}=f_{i}(\textbf{x}_{0})$, $g_{j}^{i}=g_{j}^{i}(\textbf{t}_{0})$.

The matrix product from the last theorem becomes 
$$(F_{1}, \cdots, F_{r})=(f_{1}, \cdots, f_{n})\begin{pmatrix}
  g_{1}^{1}&\cdots  &g_{r}^{1} \\
  \vdots&  & \\
  g_{1}^{n}&\cdots  &g_{r}^{n}
\end{pmatrix}$$
<font color="#ff0000">Remark:</font> $dF(\textbf{t}_{0})=\textbf{L}^{*}[df(\textbf{x}_{0})]$ when $\textbf{L}=D\textbf{g}(\textbf{t}_{0})$ 


>[! cor | 2]
>Let $r=1$, then $\textbf{F}'(t_{0})=D\textbf{f}(\textbf{x}_{0})[\textbf{g}'(t_{0})]$, where $\textbf{x}_{0}=\textbf{g}(t_{0})$ and $\textbf{g}'(t_{0})$ is the $n\times 1$ matrix $D\textbf{g}(t_{0})$.
- Easily derived from the main theorem.
- <font color="#ff0000">Remark:</font> This corollary will be used in the discussion of tangent vector.

>[! cor | 3]
>If $\textbf{f}$ and $\textbf{g}$ are of class $\mathscr{C}^{(q)}$, then $\textbf{F}$ is of class $\mathscr{C}^{(q)}$.
- First assume $\textbf{f}$ to be a scalar function and apply Corollary 1, then this Corollary follows for each components of the mapping.

<font color="#ff0000">Important Example:</font> Let $f$ be of class $\mathscr{C}^{(2)}$ and let $F(r,\theta)=f[r\cos(\theta), r\sin(\theta)]$, we will show that $f_{11}+f_{22}=F_{11}+\frac{1}{r^{2}}F_{22}+\frac{1}{r}F_{1}$
	[[Differentiation of real-valued Functions (Proof)#^396865|Proof]]
	<font color="#ff0000">Remark:</font> #Laplacian Left hand side is called Laplacian of $f$

>[! cor | 4]
>Let $n=r=p$, and let $\textbf{f}$ and $\textbf{g}$ be differentiable, then for every $t\in \Delta$, $$
\frac{\partial(F^{1}, \cdots, F^{n})}{\partial(t^{1}, \cdots, t^{n})}=\frac{\partial(f^{1}, \cdots, f^{n})}{\partial (x^{1}, \cdots, x^{n})}\frac{\partial(g^{1}, \cdots, g^{n})}{\partial (t^{1}, \cdots, t^{n})} $$
- Proof is trivial

### Inverse Function Theorem

During this section, we assume that $r=n$. Our goal is to find a criterion which guarantees that the inverse $\textbf{g}^{-1}$ exists, and a formula for its differential without explicitly finding $\textbf{g}^{-1}$ itself.

In order to prove the theorem, two lemmas are required.

>[! lem | 1] 
>Let $\boldsymbol{\phi}$ be continuous on $\Omega_{1}$ (which is a neighborhood of $0$ with radius ${} \delta_{1} {}$) and satisfy $|\boldsymbol{\phi}(\textbf{t})|\leq c|\textbf{t}|$ for all $\textbf{t}\in\Omega_{1}$ with $0<c<1$. Let $\Omega$ be the $\delta$ -neighborhood of $\textbf{0}$, where $\delta\leq(1-c)\delta_{1}$, and let ${} \boldsymbol{\psi}(\textbf{t})=\sum\limits_{m=0}^{\infty}\boldsymbol{\phi}^{[m]}(\textbf{t}) {}$ for all $\textbf{t}\in\Omega$, where $\boldsymbol{\phi}^{[m]}(\textbf{t})$ is the $m$ -times composition of $\boldsymbol{\phi}(\textbf{t})$. Then for all $\textbf{t}\in\Omega$, $|\boldsymbol{\psi}(\textbf{t})|\leq\frac{|\textbf{t}|}{1-c}$ and $\boldsymbol{\psi}(\textbf{t})-\boldsymbol{\phi}[\boldsymbol{\psi}(\textbf{t})]=\textbf{t}$
-  [[Differentiation of real-valued Functions (Proof)#^d75147|Proof]] ^887023

>[! lem | 2]
>Let $\textbf{g}$ be of class $\mathscr{C}^{(1)}$, from $\Delta$ into $E^{n}$, with $J\textbf{g}(\textbf{t}_{1})\neq 0$, $\textbf{t}_{1}\in\Delta$. Then there exist a neighborhood $\Omega$ of $\textbf{t}_{1}$ with $\Omega\subset\Delta$, a neighborhood $U$ of $\textbf{x}_{1}=\textbf{g}(\textbf{t}_{1})$, and a function $\textbf{F}$ defined on $U$, such that: 
>1. The restriction $\textbf{g}|_{\Omega}$ is injective
>2. $U\subset\textbf{g}(\Omega)$ and $\textbf{F}(U)\subset\Omega$
>3. $\textbf{g}[\textbf{F}(\textbf{x})]=\textbf{x}$ for all $\textbf{x}\in U$
>4. $\textbf{F}$ is differentiable at $\textbf{x}_{1}$, and $D\textbf{F}(\textbf{x}_{1})=[D\textbf{g}(\textbf{t}_{1})]^{-1}$
- Proof: [[Differentiation of real-valued Functions (Proof)#^3226fc|1).]] [[Differentiation of real-valued Functions (Proof)#^ae5800|2), 3).]] [[Differentiation of real-valued Functions (Proof)#^5381ca|4).]] 

#InverseMappingThm
>[! thm |*] Inverse Mapping Theorem
>Let $\textbf{g}$ be a transformation of class $\mathscr{C}^{(q)}$, $q\geq 1$, from an open set $\Delta\subset E^{n}$ into $E^{n}$. If $J\textbf{g}(\textbf{t}_{0})\neq 0$ (which is equivalent to say $\textbf{g}'(\textbf{t}_{0})$ is **invertible**), then there exists an open set $\Delta_{0}$ containing $\textbf{t}_{0}$, such that
>1. The restriction $\textbf{g}|_{\Delta_{0}}$ is injective.
>2. The set $\textbf{g}(\Delta_{0})$ is open
>3. The inverse $\textbf{f}$ of $\textbf{g}|_{\Delta_{0}}$ is of class $\mathscr{C}^{(q)}$
>4. $D\textbf{f}(\textbf{x})=[D\textbf{g}(\textbf{t})]^{-1}$, if $\textbf{x}=\textbf{g}(\textbf{t})$, $\textbf{t}\in\Delta_{0}$ 	
-  [[Differentiation of real-valued Functions (Proof)#^efaec8|Proof]] ^9b2b16

>[! cor |*]
>Let $\textbf{g}$ be of class $\mathscr{C}^{1}$, and suppose that $J\textbf{g}(\textbf{t})\neq 0$ for all $\textbf{t}\in\Delta$. Then the image $\textbf{g}(B)$ of any open set $B\subset \Delta$ is an open set.
-  [[Differentiation of real-valued Functions (Proof)#^3f4846|Proof]]


### Regular Transformation

This definition merges from the previous Corollary by adding the condition of univalent (injectivity).

#RegularTransformation
>[! def |*] Regular Transformation
>Assuming $\textbf{g}$ is an operator. Tranformation $\textbf{g}$ is regular if
>1. $\textbf{g}$ is of class $\mathscr{C}^{(1)}$
>2. $\textbf{g}$ is injective
>3. $J\textbf{g}(\textbf{t})\neq0$ for every $\textbf{t}\in \Delta$ 

^3b5902


<font color="#ff0000">Remark:</font> By [[Differential Mappings#^9b2b16|Inverse Mapping Theorem]], a regular transformation has an inverse which is also of class $\mathscr{C}^{(1)}$. This definition is sometimes called #Diffeomorphism  of class $\mathscr{C}^{(1)}$. A transformation of class $\mathscr{C}^{(0)}$ which has an inverse of class $\mathscr{C}^{(0)}$ is called a #Homeomorphism

The follwoing definition of Diffeomorphism varies from the one stated above, but essentially, they are the same.

#Diffeomorphism
>[! def |*] Diffeomorphism
>A mapping $\textbf{f}: U\rightarrow V$, where $U,V\subset E^{n}$ are open, is called (global) diffeomorphism if it is $\mathscr{C}^{1}$ and bijective. It is called local diffeomorphism if there exists $r=r_{x}$ such that $\textbf{f}|_{B_{r}(x)}$ is $\mathscr{C}^{1}$ and bijective. 

Intuitively, a regular transformation **preserves the structure** of the domain. This notion is very important for the coordinate changes on manifolds. 

---

### Implicit Function Theorem

Generally, suppose that $1\leq m<n$. Consider a transformation ${} \boldsymbol{\Phi}=(\Phi^{1}, \cdots, \Phi^{m}) {}$ from an open set $D\subset E^{n}$ into $E^{m}$. The implicit function theorem ensures that the equation ${} \boldsymbol{\Phi}(\textbf{x})=\textbf{0} {}$ determines $m$ components of $\textbf{x}\in E^{n}$ as functions of the remaining $n-m$ components, in a neighborhood of any $\textbf{x}_{0}$ such that ${} \boldsymbol{\Phi}(\textbf{x}_{0})=\textbf{0} {}$ and ${} D\boldsymbol{\Phi}(\textbf{x}_{0}) {}$ has maximum rank $m$.

If $D\boldsymbol{\Phi}(\textbf{x}_{0})$ has maximum rank $m$, then some set of $m$ columns of its matrix is linearly independent. Without loss of generality, we may assume that the **last** $m$ columns are linearly independent. Let $r=n-m$, and let $$
\tilde{J}\boldsymbol{\Phi}(\textbf{x})=\frac{\partial(\Phi^{1}, \cdots, \Phi^{m})}{\partial(x^{r+1}, \cdots, x^{n})}
$$ denote the Jacobian of the sub-matrix with those columns. We also let $\hat{\textbf{x}}=(x^{1}, \cdots, x^{r})$ denote the vectors obtained by taking only the first components of $\textbf{x}$. 

We seek to write the remaining components as $x^{r+l}=\phi^{l}(\hat{\textbf{x}})$ for $l=1, \cdots, m$ for $\hat{\textbf{x}}$ in some open set $R$ containing $\hat{\textbf{x}}_{0}$. When it is possible, we write $\boldsymbol{\phi}=(\phi^{1}, \cdots, \phi^{m})$ and $\textbf{x}=(\hat{\textbf{x}}, \boldsymbol{\phi}(\hat{\textbf{x}}))$.

#ImplicitMappingThm 
>[! thm |*] Implicit Mapping Theorem
>Let $\boldsymbol{\Phi}$ be of class $\mathscr{C}^{(q)}$ from an open set $D\subset E^{n}$ into $E^{m}$, where $q\geq 1$ and $1\leq m<n$. Let $\textbf{x}_{0}\in D$ be such that $\boldsymbol{\Phi}(\textbf{x}_{0})=\textbf{0}$ and $\tilde{J}\boldsymbol{\Phi}(\textbf{x}_{0})\neq 0$. Then there exist a neighborhood $U$ of $\textbf{x}_{0}$, an open set $R\subset E^{r}$ containing $\hat{\textbf{x}}_{0}$, and $\boldsymbol{\phi}=(\phi^{1}, \cdots, \phi^{m})$ of class $\mathscr{C}^{(q)}$ on $R$ such that ${} \tilde{J}\boldsymbol{\Phi}(\textbf{x})\neq 0 {}$ for all $\textbf{x}\in U$ and $\{\textbf{x}\in U: \boldsymbol{\Phi}(\textbf{x})=\textbf{0}\}=\{(\hat{\textbf{x}}, \boldsymbol{\phi}(\hat{\textbf{x}})):\hat{\textbf{x}}\in R\}$.
-  [[Differentiation of real-valued Functions (Proof)#^5bb822|Proof]]





















