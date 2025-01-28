#DotProduct #Norm #OrthogonalComplement #Orthogonal #Orthonormal #LengthPreserving #AnglePreserving #GramSchmidtProcess #QRDecomposition #RowSpace #LeastSquareSolution 
In part II, we will discuss Linear Spaces with **structure**, namely dot product (inner product later on) and norm.

---

## Dot Product

For #DotProduct in $\mathbb{R}^{n}$, the definition is the same as what we have learned in high school. 
Suppose  $x=\begin{pmatrix} x_{1} \\ \vdots \\ x_{n}\end{pmatrix}$, $y=\begin{pmatrix} y_{1} \\ \vdots \\ y_{n} \end{pmatrix}$, then $x\cdot y=x_{1}y_{1}+\cdots+x_{n}y_{n}=x^{T}y\in\mathbb{R}$

<font color="#ff0000">Note:</font> We should know that dot product is only used in **n-dimensional Euclidean Space**.

### Norm in n-dimensional Euclidean Space

From Dot Product, we can define the #Norm  as $\|x\|=\sqrt{x\cdot x}$

### Angle between two vectors

The angle between two vectors in $\mathbb{R}^{n}$ is $\cos(\theta)=\frac{x\cdot y}{\|x\|\|y\|}$ 
	It can be proved through simple calculation

<font color="#ff0000">Corollary:</font> $x\perp y\iff x\cdot y=0$
	Straightforward calculation

Let $H$ be a vector subspace of $\mathbb{R}^{n}$, we introduce #OrthogonalComplement$H^{\perp}=\{z\in \mathbb{R}^{n}| z\perp x, \forall x\in H\}$, which we call *Orthogonal Complement*. 

<font color="#ff0000">Lemma:</font> $H^{\perp}$ is a vector subspace
	[[Orthogonality (Proof)#^75c25a|Proof]]

---

Now we take a deeper view at *Orthogonal Complement* 

<font color="#ff0000">Recall:</font> Considering $Ax=b$, where $A$ is an n-by-m matrix (Linear map from $\mathbb{R}^{m}$ to $\mathbb{R}^{n}$), we have
	$\text{Null}(A)=\{z\in\mathbb{R}^{n}:Az=0\}$
	$\text{Col}(A)=\{Ax:x\in\mathbb{R}^{m}\}$

<font color="#ff0000">Theorem:</font> $\text{Col}(A)^{\perp}=\text{Null}(A^{T})$
	[[Orthogonality (Proof)#^d6900e|Proof]]
	This Theorem is extremely important

<font color="#ff0000">Lemma:</font> $(H^{\perp})^{\perp}=H$
	Till now, we can only prove one-side inclusion ($H\subset (H^{\perp})^{\perp}$)
	[[Orthogonality (Proof)#^3b4a85|One Side Proof]]
	We will finish the proof afterwards ^196b9c

---

## Orthogonality

<font color="#ff0000">Definition:</font> A set of vectors $\{v_{1}, \cdots, v_{n}\}$ is #Orthogonal if $v_{i}\perp v_{j}$ for $1\leq i\neq j\leq n$.

<font color="#ff0000">Definition:</font> A set of vectors $\{v_{1},\cdots, v_{n}\}$ is #Orthonormal if it's #Orthogonal and $\|v_{i}\|=1$ for all $i$.

<font color="#ff0000">Lemma:</font> Suppose that $\{v_{1}, \cdots, v_{n}\}$ is an orthogonal basis of $\mathbb{R}^{n}$, then for all $x\in \mathbb{R}^{n}$, $x=\sum\limits_{i=1}^{n}\frac{x\cdot v_{i}}{\|v_{i}\|^{2}}v_{i}$.
	[[Orthogonality (Proof)#^b7c63c|Proof]]
	The form is very similar to #FourierSeriesExpansion discussed in [[001 Preliminary Knowledge#^9c2958|Analysis]].

<font color="#ff0000">Definition:</font> #Projection Suppose that $\{v_{1}, \cdots, v_{n}\}$ is an orthogonal basis and $H=\text{span}\{v_{1}, \cdots v_{k}\}\ (k\leq n)$, then for all $x\in\mathbb{R}^{n},\ \text{Proj}_{H}(x)=\sum\limits_{i=1}^{k}\frac{x\cdot v_{i}}{\|v_{i}\|^{2}}v_{i}$ 

<font color="#ff0000">Example:</font> Let $x=\begin{pmatrix} 1\\ 1\\ 1 \end{pmatrix}$, $y=\begin{pmatrix} 1\\2\\3\end{pmatrix}$, then $\text{Proj}_{\mathbb{R}_{y}}(x)=\frac{x\cdot y}{\|y\|^{2}}y=\frac{3}{7}y$.

<font color="#ff0000">Corollary:</font> Suppose that $H\subset\mathbb{R}^{n}$ spanned by an orthonormal basis $\{v_{1}, \cdots, v_{k}\}$, then for arbitrary $x\in\mathbb{R}^{n}$, $\text{Proj}_{H}(x)=[v_{1}, \cdots, v_{k}][v_{1}, \cdots, v_{k}]^{T}x$
	[[Orthogonality (Proof)#^317927|Proof]]

---

### Orthogonal Matrix

This Corollary provides us with a motivation to define a new class of matrix, namely orthogonal matrix

<font color="#ff0000">Definition:</font> A square matrix $A_{n\times n}$ is orthogonal if $AA^{T}=I_{n}$

<font color="#ff0000">Corollary:</font> $A$ is orthogonal, then $A$ is invertible

<font color="#ff0000">Corollary:</font> The columns of an orthogonal matrix are orthogonal (in fact orthonormal)
	[[Orthogonality (Proof)#^0b5e1d|Proof]]

Now, we will discuss properties of orthogonal matrix. There are two properties: **length-preserving** and **angle-preserving**.

Length-preserving: $\|f(x)\|=\|x\|$ #LengthPreserving
Angle-preserving: $\measuredangle (x,y)=\measuredangle (f(x),f(y))$ #AnglePreserving

<font color="#ff0000">Lemma:</font> Let $f:\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$ be a linear map. $f$ preserves length iff the standard matrix $A$ of $f$ is orthogonal.
	[[Orthogonality (Proof)#^04db56|Proof]]

<font color="#ff0000">Corollary:</font> If a linear map $f:\mathbb{R}^{n}\rightarrow\mathbb{R}^{n}$ preserves length, then it's angle preserving 
	Easy to verify
	Notice that angle-preserving doesn't imply length-preserving

---

Till now, we are mostly talking under the assumption that a set (basis) is orthogonal (orthonormal). So the natural question is that how to turn a set (basis) into an orthogonal (orthonormal) set (basis).

## Gram-Schmidt Orthogonalization Process

Let ${} H=\{v_{1}, \cdots, v_{k}\} {}$, we set $u_{1}=v_{1}$
$u_{2}=v_{2}-\text{Proj}_{\mathbb{R}_{v_{1}}}=v_{2}-\frac{v_{2}\cdot v_{1}}{\|v_{1}\|^{2}}v_{1}$ 
$u_{3}=v_{3}-\frac{v_{3}\cdot u_{1}}{\|u_{1}\|^{2}}u_{1}-\frac{v_{3}\cdot u_{2}}{\|u_{2}\|^{2}}u_{2}$ 
$\vdots$
$u_{i}=v_{i}-\text{Proj}_{\text{span}(v_{1}, \cdots, v_{i-1})}(v_{i})$  ^d5429a

We can verify that this indeed gives us a orthogonal set. #GramSchmidtProcess
Also, we notice that this process can be represented by **matrix multiplication**

$[u_{1}, \cdots, u_{k}]_{n\times k}=[v_{1}, \cdots, v_{k}]_{n\times k}\begin{pmatrix} 1 && \ast && \cdots \\ 0 && 1 && \cdots \\ \vdots && && \\ 0 && \cdots && 1\end{pmatrix}_{k\times k}$, the last matrix is an upper-triangular matrix (automatically invertible whose inverse is also an upper-triangular matrix.)

If $k=n$, then $[\frac{u_{1}}{\|u_{1}\|}, \cdots, \frac{u_{n}}{\|u_{n}\|}]\begin{pmatrix} \|u_{1}\| && && && \\ 0 && \|u_{2}\| && && \\ \vdots && && \ddots && \\ 0 && \cdots && 0 && \|u_{n}\|\end{pmatrix}=[v_{1}, \cdots, v_{n}]$, the latter matrix is invertible. 

This leads to #QRDecomposition 

<font color="#ff0000">Theorem:</font> Any invertible matrix $A$ is a product of an orthogonal matrix and an upper-triangular matrix.
	Proof is shown above.

<font color="#ff0000">Corollary:</font> (of Gram-Schmidt Process) $\mathbb{R}^{n}$ has a orthogonal basis.

<font color="#ff0000">Corollary:</font> $\mathbb{R}^{n}=H\oplus H^{\perp}$ 
	[[Orthogonality (Proof)#^243991|Proof]]

Now we are ready to prove the [[001 Orthogonality#^196b9c|Lemma]] we left two sections before.
	[[Orthogonality (Proof)#^65bd68|Proof]]

Let observe some facts about Row Space:

$\text{Row}(A)^{\perp}=\text{Col}(A^{T})^{\perp}=\text{Ker}((A^{T})^{T})=\text{Ker}(A)$
Then by the the Corollary above, we have $\mathbb{R}^{n}=\text{Ker}(A)\oplus \text{Row}(A)$. This gives a intuitive understanding of Row Space #RowSpace

---

## Least Square Solution

Recall $Ax=b$, it is possible that this system doesn't have a solution. Least Square Solution (LSS) is defined due to this fact. 

<font color="#ff0000">Definition:</font> #LeastSquareSolution A Least-Square Solution to $Ax=b$ is an element $x_{0}\in\mathbb{R}^{n}$ satisfying $\|b-Ax_{0}\|=\inf\|b-Ax\|$ 
![[f589982cc8add4bcdf5503b2d648a37.jpg]]
Naturally, two questions arises, namely **Existence** and **Uniqueness**. 

The existence can be seen from the definition.

<font color="#ff0000">Theorem:</font> A vector $x_{0}$ is a least-square solution of $Ax=b$ iff $A^{T}Ax_{0}=A^{T}b$.
	[[Orthogonality (Proof)#^ffb957|Proof]]

<font color="#ff0000">Corollary:</font> $Ax=b$ has a unique least-square solution $x_{0}$ iff the columns of $A$ are linear independent.
	[[Orthogonality (Proof)#^937c83|Proof]]







