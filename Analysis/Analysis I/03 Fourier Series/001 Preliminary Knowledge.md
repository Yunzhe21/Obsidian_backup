#NormedVectorSpace #InnerProductSpace #TrigonometricSet #FourierSeriesExpansion #PeriodicFunction #BesselInequality #Completeness
## Normed Vector Space

<font color="#ff0000">Definition:</font> A vector space is called a *normed vector space* if **1).** $\|x\|\geq0$ and the equality holds iff $x=0$ **2).** $\|cx\|=|c|\|x\|$ **3).** $\|x+y\|\leq\|x\|+\|y\|$ 

It can be derived immediately from the definition that a **normed vector space** is automatically a **metric space**.

*Banach Space:* complete normed vector space. ^BanachSpace

<font color="#ff0000">Example:</font> $\mathscr{R}[a,b]$: Riemann Integrable functions on $[a,b]$, with norm $\|f\|=\int_{a}^{b}|f(x)|dx$ 
	The problem with this space is that whether $\|f\|=0$ implies $f=0$
	If we define $f=0$ as $f(x)=0$ almost everywhere on $[a,b]$, then there is a counterexample of $f$ being 1 on rational domain but 0 otherwise, also known as *Dirichlet function*, which is not Riemann Integrable.

## Inner Product Space

Check **Linear Algebra** Part for information.

*Hilbert Space:* Complete Inner Product Space ^HilbertSpace

<font color="#ff0000">Example:</font> $C[a,b]=\{f: f\ \text{is continuous on}\ [a,b]\}$, with inner product $\langle f,g\rangle=\int_{a}^{b}f(x)g(x)dx$ 
	We only check the last criteria: $\langle f,f\rangle=\int_{a}^{b}f^{2}(x)dx\geq0$ and the equality holds iff $f=0$ 
	However, it is not complete, for example: $f_{n}(x)=x^{n}$
 
## Trigonometric Set

### Orthonormal Set

<font color="#ff0000">Definition:</font> (Orthogonal Set) Let $S\subset V$ (an inner product space), $S$ is orthogonal set if $\forall x_{1},x_{2}\neq 0\in S$, $x_{1}\neq x_{2}$, $\langle x_{1},x_{2}\rangle=0$

<font color="#ff0000">Definition:</font> (Orthonormal Set) Orthogonal set with norm 1.

<font color="#ff0000">Theorem:</font> Let $V$ be an inner product space and let $z\in V$. The function $f$ defined by $f(x)=(x,z)$ is continuous on $V$.
	[[Fourier Series (Proof)#^9a699a|Proof]]

<font color="#ff0000">Corollary:</font> Let $V$ be an inner product space and let $z\in V$. Suppose $\sum\limits_{n=1}^{\infty}y_{n}$ converges to $y$. Then $(y,z)=(\sum\limits_{n=1}^{\infty}y_{n}, z)=\sum\limits_{n=1}^{\infty}(y_{n}, z)$ ^25e832

<font color="#ff0000">Theorem:</font> Let $\{x_{1}, \cdots\}$ be an orthonormal set in an inner product space $V$ and let $x\in V$. Suppose $x=\sum\limits_{n=1}^{\infty}c_{n}x_{n}$, then $c_{n}=(x,x_{n})$
	$(x,x_{n})=(\sum\limits_{j=1}^{\infty}c_{j}x_{j}, x_{n})=\sum\limits_{j=1}^{\infty}c_{j}(x_{j}, x_{n})=c_{n}$  ^9c2958

The next theorem is crucial, but first, we prove a lemma

<font color="#ff0000">Lemma:</font> Let $\{x_{1}, \cdots, x_{n}\}$ be an orthogonal set in an inner product space $V$ and let $x\in V$. Let $c_{1}, \cdots, c_{n}$ be $n$ scalars and set $y=\sum\limits_{k=1}^{n}c_{k}x_{k}$, then $\|x-y\|^{2}=\|x\|^{2}-\sum\limits_{k=1}^{n}(x,x_{k})^{2}+\sum\limits_{k=1}^{n}[(x,x_{k})-c_{k}]^{2}$
	Proof is striaght computation

<font color="#ff0000">Theorem:</font> Let $\{x_{1}, x_{2}, \cdots\}$ be an orthonormal set in an inner product space $V$ and let $x\in V$. Let $c_{1}, \cdots, c_{n}$ be $n$ scalars and set $y_{n}=\sum\limits_{k=1}^{n}c_{k}x_{k}$, $z_{n}=\sum\limits_{k=1}^{n}(x,x_{k})x_{k}$, then $\|x-z_{n}\|\leq\|x-y_{n}\|$.
	[[Fourier Series (Proof)#^a76f60|Proof]]

<font color="#ff0000">Theorem:</font> #BesselInequality Let $\{x_{1}, x_{2}, \cdots\}$ be an orthonormal set in an inner product space $V$ and let $x\in V$. Then the series $\sum\limits_{n=1}^{\infty}(x,x_{n})^{2}$ converges and $\sum\limits_{n=1}^{\infty}(x,x_{n})^{2}\leq\|x\|^{2}$
	[[Fourier Series (Proof)#^cf9740|Proof]]

<font color="#ff0000">Corollary:</font> Let $\{x_{1}, x_{2}, \cdots\}$ be an orthonormal set in an inner product space $V$ and let $x\in V$. Then, $\lim_{n\rightarrow\infty}(x,x_{n})=0$

#### Complete Orthonormal Set

<font color="#ff0000">Definition:</font> #Completeness Let $X=\{x_{1}, x_{2}, \cdots\}$ be an orthonormal set in an inner product space $V$. If $x=\sum\limits_{n=1}^{\infty}(x,x_{n})x_{n}$ for every $x$ in $V$ (convergence is relative to the inner product space), then we say $X$ is *complete*.
	Notice that this #Completeness  is different from what we discussed in previous section concerning Metric Space.

<font color="#ff0000">Theorem:</font> Let $X=\{x_{1}, x_{2}, \cdots\}$ be a complete orthonormal set in an inner product space $V$. Then
	1. $(x,y)=\sum\limits_{n=1}^{\infty}(x,x_{n})(y,x_{n})$ for all $x,y\in V$
		[[Fourier Series (Proof)#^0ddf22|Proof]]
	2. #ParsevalTheorem $\|x\|^{2}=\sum\limits_{n=1}^{\infty}(x,x_{n})^{2}$ for all $x\in V$.
		Follow immediately from 1.
	3. If a vector $x$ in $V$ is orthogonal to $x_{n}$ for all $n$, then $x=0$
		[[Fourier Series (Proof)#^b83575|Proof]]
	4. If $x\notin X$, the set $x\notin X$, the set $X\cup\{x\}$ is not orthonormal
		[[Fourier Series (Proof)#^740066|Proof]]
### Example:

Now we introduce *Trigonometric set*:
$\phi_{0}(x)=\frac{1}{\sqrt{2\pi}}$, $\phi_{2n-1}(x)=\frac{\sin(nx)}{\sqrt{\pi}}$, $\phi_{2n}(x)=\frac{\cos(nx)}{\sqrt{\pi}}$, all defined on $[0,2\pi]$

Notice that: $\int_{0}^{2\pi}\phi_{2n-1}^{2}(x)dx=\int_{0}^{2\pi}\frac{\sin^{2}(nx)}{\pi}=\int_{0}^{2\pi}\frac{1-\cos(2nx)}{2\pi}=1$ 
Similarly, $\int_{0}^{2\pi}\phi_{2n}(x)dx=1$
Also, $\int_{0}^{2\pi}\sin(nx)\cos(nx)=0$
Hence, the Trigonometric set is an orthogonal set.

<font color="#ff0000">Question:</font> If $f\in C[a,b]$, $f\in\mathscr{R}[a,b]$, does there exist $a_{0}, a_{1}, b_{1}, a_{2}, b_{2}, \dots$ s.t. $f(x)=a_{0}+a_{1}\cos(x)+b_{1}\sin(x)+\dots$?

For any $f$ s.t. $f^{2}(x)$ is integrable, write function $f$ into a series of this form is called the *Fourier Series Expansion* of $f$. (**To be continued**) 

## Periodic Function

<font color="#ff0000">Definition:</font> (Periodic Function) Let $f$ be a function on $\mathbb{R}$, we say that $f$ is periodic of period $p>0$ if $f(x+p)=f(x)$ for all $x\in\mathbb{R}$.

<font color="#ff0000">Theorem:</font> Let $f$ be periodic of period $p>0$, and suppose that $f\in\mathscr{R}[a,a+p]$, then if $c\in\mathbb{R}$, $f\in\mathscr{R}[c,c+p]$ and $\int_{a}^{a+p}f(t)dt=\int_{c}^{c+p}f(t)dt$ 
	[[Fourier Series (Proof)#^dea7ac|Proof]]


Denote $CP[a,b]$ the set of functions continuous on $\mathbb{R}$ with period $(b-a)$.



