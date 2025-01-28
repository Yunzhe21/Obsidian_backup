#InnerProductSpace #HermitionMatrix #UnitaryMatrix #SchurTheorem #RieszRepresentation #AdjointLinearMap #Involution #NormedVectorSpace #ParallelgramIdentity #PolarizationIdentity 
In the previous chapter, we mainly discuss things in $\mathbb{R}^{n}$. Now, we aim to generalize #DotProduct into more cases while keeping the properties discussed before.

---

## Inner Product in Real Vector Space

<font color="#ff0000">Definition:</font>  Let $V$ be a $\mathbb{R}$ -vector space, $\langle \ , \  \rangle: V\times V \rightarrow\mathbb{R}$ is called an Inner Product if 
	1. $\langle a_{1}x_{1}+a_{2}x_{2},y\rangle=a_{1}\langle x_{1},y\rangle +a_{2}\langle x_{2},y\rangle$ 
	2. $\langle x,y\rangle=\langle y,x\rangle$
	3. $\langle x,x\rangle \geq 0$ and the equality iff $x=0$

An #InnerProductSpace is a linear space along with an Inner Product

### Properties

Norm (Generalized Length): #Norm $\|x\|=\sqrt{\langle x,x\rangle}$

Lemma: #CauchySchwazInequality $|\langle x,y\rangle|\leq \|x\|\|y\|$
	[[Inner Product (Proof)#^105258|Proof]]

Angle (Generalized Angle): $\cos(\theta)=\bigr |\frac{\langle x,y\rangle}{\|x\|\|y\|}\bigr |$
	$\theta=\frac{\pi}{2}\iff\langle x,y\rangle=0\iff x\perp y$
	In this sense, we also define generalized orthogonal
	#OrthogonalComplement $H^{\perp}=\{z\in V: z\perp x, \forall x\in H\}$

<font color="#ff0000">Lemma:</font> $H^{\perp}$ is a subspace of $V$
	Easy to verify

---

## Inner Product in Complex Vector Spaec

In the case of Complex Vector Space, we need to slightly modify one criterion, which is symmetry. That is because the standard inner product in $\mathbb{C}^{n}$ is $x^{*}y$, where $x^{*}=(\overline{x})^{T}$

<font color="#ff0000">Definition:</font> An inner product on a complex (Real/ AnyField) vector space $V$ is a function $\langle \ ,\ \rangle: V\times V\rightarrow \mathbb{F}$ satisfying 
	1.  $\langle x,y\rangle=\overline{\langle y,x\rangle}$
	2. $\langle x,a_{1}y_{1}+a_{2}y_{2}\rangle=a_{1}\langle x,y_{1}\rangle+a_{2}\langle x,y_{2}\rangle$
	3. $\langle x,x\rangle\geq0$ and the equality holds iff $x=0$.

### Conclusions in this case

Gram-Schmidt Process: almost the same as [[001 Orthogonality#^d5429a|Dot Product Case]]
$u_{1}=v_{1}$
$u_{2}=v_{2}-\frac{\langle v_{1},v_{2}\rangle}{\|u_{1}\|^{2}}u_{1}$
$\vdots$
$u_{i+1}=v_{i+1}-\sum\limits_{j=1}^{i}\frac{\langle u_{j}, v_{i+1}\rangle}{\|u_{j}\|^{2}}u_{j}$
Notice that the sequence in the inner product cannot be switched due to our definiton.

<font color="#ff0000">Lemma:</font> For $\langle \ ,\ \rangle: V\times V\rightarrow\mathbb{F}$ that is a inner product and we have a basis $C$ of $V$, then there exists $A_{n\times n},\ n=\text{dim}V$ s.t. $[x^{*}Ay]_{C}=\langle x,y\rangle$
	[[Inner Product (Proof)#^15fad5|Proof]]
	<font color="#ff0000">Remark:</font> This lemma tells us that inner product can be represented by a matrix multiplication.

If we take a look at the proof of the lemma above, we may observe that 
	$B=(\langle e_{i},e_{j}\rangle)_{n\times n}=\overline{B}^{T}$
	This cues the definition of **Hermition matrix**.

<font color="#ff0000">Definition:</font> #HermitionMatrix An $n\times n$ complex matrix is called Hermition if $A=A^{*}=\overline{A}^{T}$
	In particular, a real Hermition matrix is exactly symmetric. So we may say that Hermition matrix is a generalization of symmetric matrix.

Notice $\{u_{1}, \cdots, u_{n}\}$ is an orthonormal basis iff $[u_{1}, \cdots, u_{n}]^{*}A[u_{1}, \cdots, u_{n}]=I_{n}$, for $A$ that is the matrix representation of an inner product with respect to the standard matrix
	This is trivial.

A special case in $(\mathbb{C}^{n},\langle x,y\rangle=x^{*}y)$, we have $[u_{1}, \cdots, u_{n}]^{*}I_{n}[u_{1}, \cdots, u_{n}]=I_{n}$. This is the motivation for **unitary matrix**.

<font color="#ff0000">Definition:</font> #UnitaryMatrix A square matrix $U$ is called unitary matrix if $U^{*}U=I_{n}$

It is self-evident that $U$ is unitary matrix $\iff$ columns of $U$ form a orthonormal set.

---

## Two Applications

<font color="#ff0000">Theorem:</font> #SchurTheorem Let $f: V\rightarrow V$ be a linear map on a finite $\mathbb{C}$ -vector space of dimensional $n$. If $V$ is an inner product space, then exists an orthonormal basis on which the representation matrix of $f$ is upper-triangular.
	[[Inner Product (Proof)#^bd1b41|Proof]]
	This Theorem is for **finite dimensional** vector spaces

<font color="#ff0000">Corollary:</font> For any matrix $A_{n\times n}$, there exists unitary matrix $P$ s.t. $PAP^{-1}$ is upper-triangular

<font color="#ff0000">Theorem:</font> #RieszRepresentation Let $V$ be an inner product space over $\mathbb{R}$ or $\mathbb{C}$, denote it as $\mathbb{F}$. Suppose that $f: V\rightarrow \mathbb{F}$ is linear, then there exists unique $y\in V$ satisfying $f(x)=\langle y,x\rangle$ for all $x\in V$.
	[[Inner Product (Proof)#^d03113|Proof]]

### Application of Riesz Representation Theorem

The main product of this application is to introduce Adjoint linear map.

Let $f:V\rightarrow W$ be a linear map between inner product spaces with possibly different inner products.

Fix $y_{0}\in W$, $\langle y_{0},f(-)\rangle_{W}: V\rightarrow \mathbb{F}$ is a linear functional on $V$, $x\longmapsto\langle y_{0},f(x)\rangle_{W}$.

Riesz-Representation Theorem implies that there exists unique $v_{0}\in V$ s.t. $\langle y_{0},f(x)\rangle_{W}=\langle v_{0},x\rangle_{V}$

So we have $f^{*}:W\rightarrow V$, where $y_{0}\longmapsto v_{0}$, which is called the adjoint of $f$ #AdjointLinearMap
	Notice that the domain $W$ need not be finite dimensional.

<font color="#ff0000">Lemma:</font> $f^{*}: W\rightarrow V$ is linear  
	[[Inner Product (Proof)#^9afbfb|Proof]]

<font color="#ff0000">Example:</font> $f: \mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$, and $f(x)=Ax$, what about $f^{*}$?
	$\langle f^{*}(y),x\rangle=\langle y,f(x)\rangle=y^{T}Ax$ 
	Then $(f^{*}y)^{T}x=y^{T}(f^{*})^{T}x=y^{T}Ax$ for all $x,y$
	Then $f^{*}=A^{T}$.


More generally, in exercise question:
<font color="#ff0000">Ex:</font> Let $f: V\rightarrow W$ be a linear map between two finite dimensional inner product spaces. Suppose that $B,C$ are orthogonal basis of $V,W$ respectively. Suppose that $M_{f}$ is the representation matrix of $f$, with respect to $B,C$. Find the representation matrix of $f^{*}$ with respective to $B,C$.
	Let $B=\{v_{1}, \cdots, v_{n}\}$ and $C=\{w_{1}, \cdots, w_{m}\}$
	$M_{f^{*}}=\left [ \begin{pmatrix} \langle w,w_{1}\rangle_{W} && \cdots && \\ && \ddots && \\ && && \langle w_{m}, w_{m}\rangle_{W}\end{pmatrix}M_{f}\begin{pmatrix} \frac{1}{\langle v_{1}, v_{1}\rangle_{V}} && && \\ && \ddots && \\ && && \frac{1}{\langle v_{n}, v_{n}\rangle_{V}}\end{pmatrix}\right]^{*}$ 
This exercise tells us that if $f$ is a **linear operator**, then if we choose **orthonormal basis**, we have $M_{f^{*}}=M_{f}^{*}$.

<font color="#ff0000">Remark:</font> $(f^{*})^{*}=f$
	[[Inner Product (Proof)#^625582|Proof]]
	This star operator is an **Involution** because of this property. #Involution

<font color="#ff0000">Lemma:</font> $*$ is conjugate-linear (i.e. $(af+bg)^{*}=\overline{a}f^{*}+\overline{b}g^{*}$, for all $a,b\in\mathbb{F}$)

<font color="#ff0000">Lemma:</font> $(\text{Im}f^{*})^{\perp}=\text{Ker}f$ 
	[[Inner Product (Proof)#^8aba30|Proof]]
	Equivalently, $\text{Ker}f^{\perp}=\text{Im}f^{*}$

If we consider matrix $A$, then the previous lemma tells us that $\text{Im}(A^{T})^{\perp}=\text{Null}(A)\subset\mathbb{R}^{m}$
$\mathbb{R}^{m}=\text{Null}(A)\oplus\text{Im}(A^{T})$ 

---

## Inner Product and Norm

Inner product decides norm, which is shown by the definition, but the reverse is not true.

Distance-preserving: $\|f(x)\|=\|x\|$ #LengthPreserving 

<font color="#ff0000">Lemma:</font> A linear map $f$ is distance-preserving iff it preserves inner product (i.e. $\langle f(x),f(y)\rangle=\langle x,y\rangle$)
	[[Inner Product (Proof)#^3166b2|Proof]]

<font color="#ff0000">Corollary:</font> If $f:V\rightarrow V$ is distance-preserving, then $f$ is angle-preserving

<font color="#ff0000">Lemma:</font> If $f$ is distance preserving, $V$ is a finite-dimensional inner product space and has a basis $B=\{b_{1}, \cdots, b_{n}\}$. $M$ is the representation matrix of $f$ and $A$ is the representation matrix of the inner product all w.r.t $B$, then $A=M^{*}AM$ 
	[[Inner Product (Proof)#^f4397e|Proof]]

<font color="#ff0000">Corollary:</font> A length-preserving linear map is invertible.
	[[Inner Product (Proof)#^5e1839|Proof]]

<font color="#ff0000">Definition:</font> #NormedVectorSpace Let $V$ be a vector space over $\mathbb{F}=\mathbb{R}$ or $\mathbb{C}$. A norm on $V$ is a function $\|\cdot\|: V\rightarrow\mathbb{R}_{\geq0}$ satisfying
	1. $\|\lambda x\|=|\lambda|\|x\|$
	2. $\|x+y\|\leq \|x\|+\|y\|$
	3. $\|x\|\geq0$ and the equality hold iff $x=0$

<font color="#ff0000">Lemma:</font> A normed vector space is a metric space
	The verification process is simple

<font color="#ff0000">Remark:</font> $\{\text{inner product}\}\subset\{\text{norm}\}\subsetneq\{\text{metrics}\}$
	This means that inner product can decides norm; norm defines a metric.

So the natural question is that whether all norms can be expressed as $\sqrt{\langle x,x\rangle}$ ?
	No!

Parallelgram Identity: $\|x+y\|^{2}+\|x-y\|^{2}=2(\|x\|^{2}+\|y\|^{2})$ #ParallelgramIdentity

<font color="#ff0000">Theorem:</font> The norm on a normed vector space comes from  an inner product iff it satisfies Prarllegram identity.
	Crucial part in the proof: #PolarizationIdentity $\langle x,y\rangle=\frac{1}{4}(\|x+y\|^{2}+i\|ix+y\|^{2}-\|-x+y\|^{2}-i\|-ix+y\|^{2})$ 
	[[Inner Product (Proof)#^f50011|Proof]]











