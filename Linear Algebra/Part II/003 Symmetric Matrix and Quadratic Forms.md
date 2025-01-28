#QuadraticForm #OrthogonalDiagonalizale #PositiveDefinite #PositiveSemiDefinite #SquareRootOfMatrix #QuadraticCurve #SingularValue #SingularValueDecomposition 

---

A quadratic form is $a_{1}x_{1}^{2}+\cdots+a_{n}x_{n}^{2}+\sum\limits_{1\leq i<j\leq n}a_{ij}x_{i}x_{j}$
It can also be written as $(x_{1}, \cdots, x_{n})\begin{pmatrix} a_{1} && \frac{a_{12}}{2} && && \\ \frac{a_{12}}{2} && a_{22} && && \\ && && \ddots && \\ && && && a_{nn}\end{pmatrix}\begin{pmatrix} x_{1} \\ \dots \\ x_{n}\end{pmatrix}$ #QuadraticForm  
Notice that the middle matrix is symmetric, and that's the reason why we should study symmetric matrix. ^d07d28

---

## Symmetric 

<font color="#ff0000">Notice:</font> whenever we talk about symmetric matrix, we refer to real symmetric matrix.

<font color="#ff0000">Lemma:</font> Eigenvectors from distinct eigenvalues of a symmetric matrix are orthogonal
	[[Symmetric Matrix and Quadratic Forms (Proof)#^7b0d4f|Proof]]

<font color="#ff0000">Lemma:</font> The eigenvalues of symmetric real matrix $A$ is real. For each eigenvalue $\lambda$ of $A$, exists real eigenvector $x$ s.t. $Ax=\lambda x$.
	[[Symmetric Matrix and Quadratic Forms (Proof)#^f8788f|Proof]]

We ask a question that "Is a real symmetric matrix diagonalizable?"
	The answer is Yes, and we can even have a stronger statement.

<font color="#ff0000">Definition:</font> #OrthogonalDiagonalizale A matrix $M$ is orthogonal diagonalizable if there exists an orthogonal matrix $Q$ and diagonal matrix $D$ s.t. $M=QDQ^{-1}$ 

<font color="#ff0000">Theorem:</font> A real matrix $A$ is symmetric iff it's orthogonal diagonalizable.
	[[Symmetric Matrix and Quadratic Forms (Proof)#^0eacac|Proof]] ^55e9d6

<font color="#ff0000">Conclusion: </font> If $A_{n\times n}=A_{n\times n}^{T}$, then
	1. Eigenvalues of $A$ must be real.
	2. Eigenvectors of different eigenspaces are orthogonal
	3. $A$ is orthogonal diagonalizable ^8017ee

We may later compare this conclusion with further observations.

---

## Quadratic Form

Recall that $q(x)=x^{T}Ax$, where $A$ is symmetric. By virtue of the [[003 Symmetric Matrix and Quadratic Forms#^55e9d6|Theorem]] stated above, $A=PDP^{-1}$, where $P$ is orthogonal matrix and $D$ is diagonal.

Then $q(x)=x^{T}Ax=y^{T}Ay=(y_{1}, \cdots, y_{n})\begin{pmatrix} d_{1} && && \\ && \ddots && \\ && && d_{n}\end{pmatrix}\begin{pmatrix} y_{1} \\ \vdots \\ y_{n}\end{pmatrix}$
$=d_{1}y_{1}^{2}+\cdots+d_{n}y_{n}^{2}$, where $y=P^{T}x$ ^0ca38c

<font color="#ff0000">Corollary:</font> $q(x)=x^{T}Ax\geq0$ for all $x\in\mathbb{R}^{n}$ iff all eigenvalues of $A$ are non-negative 
If $d_{1}, \cdots, d_{n}$ are positive, then $q(x)=0$ iff $x=0$.

### P. S.D & P.D.

<font color="#ff0000">Question:</font> For what kind of symmetric matrix $A_{n\times n}$, $x^{T}Ay$ is an inner product.

<font color="#ff0000">Lemma:</font> $x^{T}Ay$ is an inner product iff all eigenvalues $d_{1}, \cdots, d_{n}>0$.
	[[Symmetric Matrix and Quadratic Forms (Proof)#^47ec87|Proof]]

<font color="#ff0000">Definition:</font> A quadratic form $q(x)=x^{T}Ax$ is 
	1. Positive definite if $q(x)\geq0$ for all $x\in\mathbb{R}^{n}$ and $q(x)=0$ iff $x=0$. #PositiveDefinite
		$\iff d_{i}>0$ for all $i$  
	2. Positive semi-definite if $q(x)\geq0$ for all $x\in\mathbb{R}^{n}$ #PositiveSemiDefinite
		$\iff d_{i}\geq0$

Similarly, we say **real symmetric** matrix $A$ is positive definite when $x^{T}Ax$ is positive definite.

<font color="#ff0000">Lemma:</font> A matrix $A$ is positive semi-definite iff $A=SS^{T}$ for some $S$.
	[[Symmetric Matrix and Quadratic Forms (Proof)#^9e7db1|Proof]]
	We can further see that when $A$ is positive definite, then the $S$ is invertible. However, this case, the $S$ is not unique as we can multiply $S$ with any orthogonal matrix.

The uniqueness of positive-semi definite case is rather complicated, so we shall state it as a theorem
<font color="#ff0000">Theorem: </font>For positive semi-definite $A$, there exists unique positive semi-definite $S$ s.t. $A=SS^{T}=S^{2}$, denote $S=\sqrt{A}=A^{1/2}$ #SquareRootOfMatrix

### Application to Quadratic curves

![[35c619116e8b0383f03d085c520b0a8.jpg]]


<font color="#ff0000">Definition:</font> #QuadraticCurve A quadratic curve is $\{(x,y)\in\mathbb{R}^{2}| ax^{2}+by^{2}+cxy+dx+ey+f=0\}$ 

<font color="#ff0000">Remark: </font>
	1. If $a=b=c=0$, we have $dx+cy+f=0$, which is a line
	2. If $(ax+by+c)(cx+dy+e)=0$, then the curve is the union of two lines
We call these two cases **degenerate curves**

---

For $ax^{2}+by^{2}+cxy+dx+ey+f=0$, write it as 
$(x,y)\begin{pmatrix} a && \frac{c}{2} \\ \frac{c}{2} && b\end{pmatrix}\begin{pmatrix} x \\ y \end{pmatrix}+(x,y)\begin{pmatrix} d \\ e\end{pmatrix} +f=0$ 

Exists orthogonal $P$ and $D=\begin{pmatrix} d_{1} && 0 \\ 0 && d_{2}\end{pmatrix}$ s.t. $A=P^{-1}DP$
Let $\begin{pmatrix} x' \\ y'\end{pmatrix}=P\begin{pmatrix} x \\ y\end{pmatrix}$, $\begin{pmatrix} x\\ y\end{pmatrix}=P^{-1}\begin{pmatrix} x'\\ y'\end{pmatrix}$, $(x,y)=(x',y')P$
$\Longrightarrow d_{1}x'^{2}+d_{2}y'^{2}+d'x'+e'y+f=0$

<font color="#ff0000">Discussion: </font>

1). $d_{1}=0, d_{2}=0\Longrightarrow$ Line
2). $d_{1}\neq0,d_{2}=0$ (or $d_{1}=0, d_{2}\neq0$)
	$d_{1}(x+u_{1})^{2}+e'y+f'=0$
		2.1). $e'=0\Longrightarrow$ either empty or a point
		2.2). $e'\neq0\Longrightarrow$ parabolic
3). Both $d_{1},d_{2}$ are not zero, then $d_{1}(x'+u_{1})^{2}+d_{2}(y'+u_{2})^{2}+f'=0$
	3.1).  $d_{1}>0,d_{2}>0$
		3.1.1). $f'>0$, empty
		3.1.2). $f'=0$, a point
		3.1.3). $f'<0$, an elliptic curve
	3.2). $d_{1}>0,d_{2}<0$
		3.2.1). $f'=0$, an "$X$"-like curve
		3.2.2). $f'\neq0$, a hyperbolic

<font color="#ff0000">Theorem:</font> A non-degenerate quadratic curve is either elliptic, hyperbolic or parabolic.

---

## Extreme Value

### Extreme Value of Quadratic Form

We first view quadratic form as a operator.

$q: \mathbb{R}^{n}\longrightarrow\mathbb{R}$, where $x\longmapsto x^{T}Ax$.
Observe: $\lambda x\longmapsto q(\lambda x)=\lambda^{2}q(x)$

For all $x\neq0\in\mathbb{R}^{n}$, $q(x)=q(\|x\|\frac{x}{\|x\|})=\|x\|^{2}q(\frac{x}{\|x\|})$, now we restrict the domain on $S^{n-1}=\{x\in\mathbb{R}^{2}: \|x\|=1\}$.

Since $S^{n-1}$ is compact, $\max_{x\in S^{n-1}}q(x)=q(x_{0})$ for some $x_{0}\in S^{n-1}$

<font color="#ff0000">Question:</font> What's $\max_{x\in S^{n-1}}q(x)$ ?

$\max_{x\in S^{n-1}}=\max_{y\in\S ^{n-1}}(d_{1}y_{1}^{2}+\cdots+d_{n}y_{n}^{2})$
Assume that $d_{1}\geq d_{2}\geq\cdots d_{n}$, then $d_{1}y_{1}^{2}+\cdots+d_{n}y_{n}^{2}\leq d_{1}(y_{1}^{2}+\cdots+y_{n}^{2})=d_{\max}=d_{1}$

Choose $y_{1}=1,y_{2}=\cdots=y_{n}=0$ to get $q(x_{0})=d_{1}$, where $x_{0}=P\begin{pmatrix} 1 \\ 0\\ \vdots \\0\end{pmatrix}$, which is the unit vector corresponding to the largest eigen value of $A$.

Similarly, $\min_{x\in S^{n-1}}q(x)=d_{min}$.

### Matrix Norm

<font color="#ff0000">Question:</font> What's $\|A\|=\sup_{x\in S^{n-1}}\|Ax\|=\max_{x\in S^{n-1}}=\|Ax_{0}\|$ for some $x_{0}\in S^{n-1}$.

<font color="#ff0000">Answer:</font> Since $\|Ax\|^{2}=Ax\cdot Ax=(Ax)^{T}Ax=x^{T}A^{T}Ax$, according to the conclusion above, $\|A\|=\sqrt{\text{Largest eigenvalue of} \ A^{T}A}$.

Also notice that $A^{T}A$ is positive semi-definite as $x^{T}A^{T}Ax\geq0$ for all $x$.

<font color="#ff0000">Definition:</font> #SingularValue The singular value of $A_{n\times m}$ is the square root of the eigenvalue $\lambda_{i}$ of $A^{T}A$.

We may soon introduce another matrix decomposition, which is Singular Value Decomposition.

<font color="#ff0000">Theorem:</font>  #SingularValueDecomposition $\forall$ real matrix $A_{n\times m}$, there exists orthonormal basis $\{P_{1}, \cdots, P_{m}\}$ of $\mathbb{R}^{m}$ and orthonormal basis $\{v_{1}, \cdots, v_{n}\}$ of $\mathbb{R}^{n}$ s.t. the representation matri of $A: \mathbb{R}^{m}\longrightarrow \mathbb{R}^{n}$ is $\begin{pmatrix} \sigma_{1} && 0 && \cdots && 0 \\ && \ddots && && \\ && && \sigma_{k} && \\ 0 && \cdots && \cdots && \textbf{0}\end{pmatrix}$
$A_{n\times m}=V_{n\times m}\begin{pmatrix} \sigma_{1} && 0 && \cdots && 0 \\ && \ddots && && \\ && && \sigma_{k} && \\ 0 && \cdots && \cdots && \textbf{0}\end{pmatrix}P_{m\times m}^{T}$, where $k=\text{rank}(A)$
	[[Symmetric Matrix and Quadratic Forms (Proof)#^426715|Proof]]

<font color="#ff0000">Lemma:</font> $\sigma_{i}(B)=\sqrt{\lambda_{i}(BB^{T})}=\sqrt{\lambda_{i}(B^{T}B)}$
	[[Symmetric Matrix and Quadratic Forms (Proof)|Proof]]


