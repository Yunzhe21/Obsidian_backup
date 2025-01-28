#FejerTheorem #FejerKernel 
## Cesaro Summability of Fourier Series

Recall Cesaro Summability:

![[005 Abel Limit Theorem#^CesaroSummable|Cesaro Summable]]

Mathematician Fejer focuses on the sequence $\{\sigma_{n}\}$ 
$$
\sigma_{n}=\frac{s_{0}+\cdots+s_{n}}{n+1}
$$
where $s_{n}$ are partial sums of the Fourier Series

Let $f$ be periodic of period $2\pi$ and suppose $f\in\mathscr{R}[a,a+2\pi]$. Then
$$
\begin{eqnarray}
\sigma_{n}(x)&=&\frac{s_{0}(x)+\cdots+s_{n}(x)}{n+1} \\
&=&\frac{1}{n+1}\sum\limits_{k=0}^{n}\frac{1}{\pi}\int_{-\pi}^{\pi}f(x-t)D_{k}(t)dt \\
&=& \frac{1}{\pi}\int_{-\pi}^{\pi}f(x-t)\cdot\frac{\sum\limits_{k=0}^{n}D_{k}(t)}{n+1}dt
\end{eqnarray}
$$
Thus if we set $K_{n}(t)=\frac{1}{n+1}\sum\limits_{k=0}^{n}D_{k}(t)$, we have the integral representation:
$$
\sigma_{n}(x)=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x-t)K_{n}(t)dt
$$
This is the motivation for *Fejer Kernel*

<font color="#ff0000">Definition:</font> #FejerKernel The Fejer Kernel is defined by the equation $K_{n}(t)=\frac{1}{n+1}\sum\limits_{k=0}^{n}D_{k}(t)$ for all $t\in\mathbb{R}$ and $n=0,1,\dots$  ^93dbe1

Just like the *Dirichlet Kernel*, Fejer Kernel also has a convenient representation.

<font color="#ff0000">Theorem:</font> $K_{n}(t)=\frac{1}{2(n+1)}[\frac{\sin[(n+1)t/2]}{\sin(t/2)}]^{2}$ for all $t$ with $\sin(t/2)\neq0$
	[[Fourier Series (Proof)#^099c21|Proof]]

Now we will study the properties of *Fejer Kernel*

<font color="#ff0000">Theorem: </font>
	1. $K_{n}(t)\geq0$
		Easy to see
	2. $\frac{1}{\pi}\int_{-\pi}^{\pi}K_{n}(t)dt=1$
		Proof follows from [[003 Pointwise Convergence of Fourier Series#^5faef0|Theorem]] and [[004 Uniform Convergence of Fourier Series#^93dbe1|Definition of Fejer Kernel]]
	3. $K_{n}(t)\leq\frac{1}{2(n+1)\sin^{2}(\delta/2)}$ for $0<\delta\leq|t|\leq\pi$
		If $0<\delta\leq|t|\leq\pi$, then $\sin^{2}(\delta/2)\leq\sin^{2}(t/2)$, and the conclusion follows

We are now ready to prove *Fejer Theorem*.

<font color="#ff0000">Theorem:</font> #FejerTheorem Let $f\in CP[a,a+2\pi]$. Let $\{s_{n}\}$ be the sequence of partial sums of the Fourier Series of $f$. Let
$$
\sigma_{n}=\frac{s_{0}+\cdots+s_{n}}{n+1}
$$
Then $\{\sigma_{n}\}$ converges uniformly to $f$.
	[[Fourier Series (Proof)#^978497|Proof]]

<font color="#ff0000">Corollary:</font> Let $f,g\in CP[a,a+2\pi]$. If $f$ and $g$ have the same Fourier Series, then $f(x)=g(x)$ for every $x$ in $\mathbb{R}$.

<font color="#ff0000">Corollary:</font> The trignometric set is complete in $CP[a,a+2\pi]$.
	[[Fourier Series (Proof)#^c7bc50|Proof]]





























