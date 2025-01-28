#SpectralTheorem 

<font color="#ff0000">Recall:</font> $V$ is an inner product space over $\mathbb{F}=\mathbb{R}$ or $\mathbb{C}$. $f: V\longrightarrow W$, then $f^{*}:W\rightarrow V$ s.t. $\langle y,f(x)\rangle=\langle f^{*}(y),x\rangle$ 

<font color="#ff0000">Definition:</font> If $f=f^{*}$, when $V=W$, we call $f$ self-adjoint.

<font color="#ff0000">Corollary:</font> $f=f^{*} \iff AB$ is Hermitian, where $A$ is the representation matrix of inner product and $B$ is the representation matrix of $f$.
	[[Self-adjoint Operator (Proof)#^954051|Proof]]

We should see that self-adjoint operator is the generalization of symmetric matrix, so the natural question is that do self-adjoint operators share similar properties as symmetric matrix.

![[003 Symmetric Matrix and Quadratic Forms#^8017ee]]

However, we haven't really defined what are "eigenvector" and "eigenvalue" in general operator sense. We are now fixing it.

<font color="#ff0000">Definition:</font> $f:V\longrightarrow V$. If $f(x)=\lambda x$ for $x\neq\in V$ and $\lambda\in\mathbb{F}$, then $\lambda$ is an eigenvalue of $f$

<font color="#ff0000">Question:</font> Can we always find eigenvalues for $f$ where $\mathbb{F}=\mathbb{C}$ ?
	No

<font color="#ff0000">Example:</font> $S(x_{1}, x_{2}, \cdots)=(0, x_{1}, x_{2}, \cdots)$
If it has eigenvalue $\lambda$, then $\lambda(x_{1}, x_{2}, \cdots)=(0, x_{1}, x_{2}, \cdots)\iff (\lambda x_{1}, \lambda x_{2}, \cdots)=(0, x_{1}, \cdots)$ 
	1. If $\lambda=0$, then $0=x_{1}=x_{2}=\cdots$
	2. If $\lambda\neq0$, then the same.

<font color="#ff0000">Lemma:</font>  Any eigenvalue of a self-adjoint linear map is real. 
	[[Self-adjoint Operator (Proof)#^767124|Proof]]

<font color="#ff0000">Lemma:</font> Eigenspaces of self-adjoint map $f$ are orthogonal.
	[[Self-adjoint Operator (Proof)#^8263d2|Proof]]

Till now, we have found the analog of the first two properties of symmetric matrix.

<font color="#ff0000">Theorem:</font> #SpectralTheorem Let $V$ be a finite dimensional inner product space over $\mathbb{F}=\mathbb{R}$ or $\mathbb{C}$, then there exists an orthonormal basis $\{v_{1}, \cdots, v_{n}\}$ on which the representation matrix of a self-adjoint $f$ is real diagonal.
	[[Self-adjoint Operator (Proof)#^4c6f15|Proof]]

<font color="#ff0000">Definition:</font> #Normal A matrix $A$ is normal if $A^{*}A=AA^{*}$

<font color="#ff0000">Theorem:</font> A complex square matrix $A: \mathbb{C}^{n}\longrightarrow\mathbb{C}^{n}$ is unitary diagonalizable iff it's normal
	[[Self-adjoint Operator (Proof)|Proof]]




