#DirichletKernel #RiemannLocalization #LipschitzCondition 
We consider Fourier Series in inner product space $\mathscr{R}[a,a+2\pi]$ 
We will prove a sufficient condition for the Fourier Series of $f$ to converge to $f$ pointwise.

---

To do so, we have to ensure that the limit of partial sum at $x$ exists.
$$
\begin{eqnarray}
s_{n}(x) & = &\frac{1}{2\pi}\int_{a}^{a+2\pi}f(t)dt+\frac{1}{\pi}\sum\limits_{k=1}^{n}\int_{a}^{a+2\pi}f(t)[\cos(kx)\cos(kt)+\sin(kx)\sin(kt)]dt \\
& =&\frac{1}{2\pi}\int_{a}^{a+2\pi}f(t)dt+\frac{1}{\pi}\sum\limits_{k=1}^{n}\int_{a}^{a+2\pi}f(t)\cos[k(x-t)]dt
\end{eqnarray}
$$
We can redefine $f$ to be periodic on $\mathbb{R}$ by letting $f(a+2\pi)=f(a)$.

**Change of variable:** $u=x-t$, we have
$$
\begin{eqnarray}
s_{n}(x)& =&\frac{1}{2\pi}\int_{x-(a+2\pi)}^{x-a}f(x-u)du+\frac{1}{\pi}\sum\limits_{k=1}^{n}\int_{x-(a+2\pi)}^{x-a}f(x-u)\cos(ku)du \\
&=&\frac{1}{2\pi}\int_{-\pi}^{\pi}f(x-t)dt+\frac{1}{\pi}\sum\limits_{k=1}^{n}\int_{-\pi}^{\pi}f(x-t)\cos(kt)dt
\end{eqnarray}
$$
Then if we let $D_{n}(t)=\frac{1}{2}+\sum\limits_{k=1}^{n}\cos(kt)$, we can obtain an elegent form
$$
s_{n}(x)=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x-t)D_{n}(t)dt
$$
This is the motivation for *Dirichlet kernel*

<font color="#ff0000">Definition:</font> #DirichletKernel
$$
D_{0}(t)=\frac{1}{2},\ D_{n}(t)=\frac{1}{2}+\sum\limits_{k=1}^{n}\cos(kt)
$$
Now, we study the *Dirichlet Kernel*

<font color="#ff0000">Theorem:</font> 
	1. $D_{n}(t)=\frac{\sin[(n+1/2)t]}{2sin(t/2)}$, for all $t$ that $\sin(t/2)\neq0$
		[[Fourier Series (Proof)#^9d7a2d|Proof]]
	2. $\frac{1}{\pi}\int_{-\pi}^{\pi}D_{n}(t)dt=1$
		Easy to verify ^5faef0

If we let $\sin(t/2)\rightarrow0$, 
$$
\lim_{\sin(t/2)\rightarrow0}\frac{\sin(n+1/2)t}{2\sin(t/2)}=\lim_{t\rightarrow0}\frac{\sin(n+1/2)t}{2\sin(t/2)}
$$
Usind L'Hospital Rule, 
$$
=\lim_{t\rightarrow0}\frac{(n+1/2)\cos(n+1/2)t}{\cos(t/2)}=n+\frac{1}{2}
$$

---

<font color="#ff0000">Theorem:</font> (Riemann Localization Theorem) Let $g\in\mathscr{R}[-\pi,\pi]$ and let $\delta$ satisfy $0<\delta<\pi$. Then 
$$
\lim_{n\rightarrow\infty}\bigr [\int_{-\pi}^{-\delta}g(t)D_{n}(t)dt+\int_{\delta}^{\pi}g(t)D_{n}(t)dt\bigr]=0
$$
[[Fourier Series (Proof)#^6e1316|Proof]] 

From this theorem, we observe that for
$$
\lim_{n\rightarrow\infty}s_{n}(x)=\lim_{n
\rightarrow\infty}\frac{1}{\pi}\int_{-\pi}^{\pi}f(x-t)D_{n}(t)dt
$$
to exists $\iff$ $\lim_{n\rightarrow\infty}\frac{1}{\pi}\int_{-\delta}^{\delta}f(x-t)D_{n}(t)dt=$ exists for some $0<\delta<\pi$.

**Why** the theorem is called Localization Theorem?
	Because we find that the behavior (converges or not) depends on the integral in an inteval including $x$ (local).

In conlusion, we have so far observed that the pointwise convergence of Fourier Series depends on the behavior of $f$ in a neighborhood of $x$.

---

We are now going to prove that differentiability of $f$ at $x$ implies that the Fourier Series of $f$ converges to $f$ at $x$.

<font color="#ff0000">Definition:</font> #LipschitzCondition A function $f$ is said to satisfy a *Lipschitz condition* at $x$ if for some $M>0$ and $\delta>0$, 
$$
|f(x)-f(y)|\leq M|x-y|
$$
whenever $|y-x|\leq\delta$.

<font color="#ff0000">Theorem:</font> If $f$ is differentiable at $x$, then $f$ satisfies a Lipschitz condition at $x$.
	[[Fourier Series (Proof)#^55d110|Proof]] ^25c7f6

<font color="#ff0000">Theorem:</font> Let $f$ be periodic of period $2\pi$ and suppose $f\in\mathscr{R}[a,a+2\pi]$. If $f$ satisfies a Lipschitz condition at $x$, then the Fourier Series of $f$ converges to $f$ at $x$.
	[[Fourier Series (Proof)#^a8ebd5|Proof]] ^35a7a0

<font color="#ff0000">Corollary:</font>  Let $f$ be periodic of period $2\pi$ and suppose $f\in\mathscr{R}[a,a+2\pi]$. If $f$ is differentiable at $x$, then the Fourier Series of $f$ converges to $f$ at $x$.
	Combine [[003 Pointwise Convergence of Fourier Series#^25c7f6|Theorem]] and [[003 Pointwise Convergence of Fourier Series#^35a7a0|Theorem]]


