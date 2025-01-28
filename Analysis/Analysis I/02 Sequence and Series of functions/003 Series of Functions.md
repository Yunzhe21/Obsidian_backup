#WeierstrassMTest 
<font color="#ff0000">Definition:</font> 
	Series of functions: $\sum\limits_{n=0}^{\infty}u_{n}(x)$, where $u_{n}(x): X\rightarrow \mathbb{R}$ 
	Partial sum: $\sum\limits_{j=0}^{n}u_{n}(x)$

<font color="#ff0000">Definition:</font> The series $\sum\limits_{n=0}^{\infty}u_{n}(x)$ converges pointwise (uniformly) if $\{S_{n}\}_{n=1}^{\infty}$ converges pointwise (uniformly).

<font color="#ff0000">Theorem 1:</font> Let $\{u_{n}(x)\}$ be a sequence of continuous functions from $(M,d)$ to $\mathbb{R}$. If $\sum\limits_{n=0}^{\infty}u_{n}(x)$ converges uniformly to $S(x)$, then $S(x)$ is continuous.
	This can be easily derived from [[002 Characteristic of Uniformly Convergence#^UniformCont|Lemma]]. ^UniformContSeries

<font color="#ff0000">Theorem 2:</font> Let $\{u_{n}(x)\}$ be a sequence of functions in $\mathscr{R}[a,b]$. If $\sum\limits_{n=0}^{\infty}u_{n}(x)$ converges uniformly to $S(x)$, then $S(x)\in\mathscr{R}$.
	This can be easily derived from [[002 Characteristic of Uniformly Convergence#^UniformInt|Theorem]].

<font color="#ff0000">Theorem 3:</font> Let $\{u_{n}(x)\}$ be a sequence of differentiable functions on $[a,b]$, and $\sum\limits_{i=0}^{\infty}u(x)$ converges for some point $x_{0}$ on $[a,b]$ (pointwise). If $\sum\limits_{i=1}^{\infty}u'_{n}(x)$ converges uniformly on $[a,b]$, then $\sum\limits_{i=0}^{\infty}u_{i}(x)$ converges uniformly to $S$, and $S'=\lim_{n\to\infty}\sum\limits_{i=0}^{n}u'_{i}(t)$   
	This can be easily derived from [[002 Characteristic of Uniformly Convergence#^UniformDiff|Proof]]

Weierstrass M-Test:

<font color="#ff0000">Theorem:</font> (Weierstrass M-Test) Given a series of function $\sum\limits_{n=0}^{\infty}u_{n}(x)$. If $|u_{n}(x)|\leq M_{n}$ for all $x\in X$, and if $\sum\limits_{n=0}^{\infty}u_{n}(x)<+\infty$, then $\sum\limits_{n=0}^{\infty}u_{n}(x)$ converges uniformly.
	[[Sequence and Series of functions (Proof)#^1ae6f5|Proof]] ^WeierstrassMTest

### An Important Example

Weierstrass construct a function that is continuous but **nowhere differentiable.**

Define $\varphi(x)=|x|$, and $\varphi(x+2)=\varphi(x)$
![[cdb4ac4bec0c7da5c781b1d9bcbc430.jpg]]
Define $f_{n}(x)=\sum\limits_{n=0}^{\infty}(\frac{3}{4})^{n}\varphi(4^{n}x)\leq\sum\limits_{n=0}^{\infty}(\frac{3}{4})^{n}<+\infty$, then $f_{n}(x)$ converges uniformly to $f(x)$. And since $f_{n}$ is continuous on $\mathbb{R}$, then $f$ is also continuous on $\mathbb{R}$
Fix a real $x$ and an integer $m>0$
$\delta_{m}=\pm\frac{1}{2}\cdot 4^{-m}\rightarrow 0$ as $m\rightarrow \infty$ (the $\pm$ is chosen s.t. no integer lies between $4^{m}x$ and $4^{m}(x+\delta_{m})$ 
Let $\gamma_{n}=\frac{\varphi(4^{n}(x+\delta_{m}))-\varphi(4^{n}x)}{\delta_{m}}$ 
	$n>m$, $4^{n}\delta_{m}$ is an even integer $\Longrightarrow \gamma_{n}=0$
	$0\leq n\leq m$, $|\gamma_{n}|\leq 4^{n}$
Since $|\gamma_{m}|=4^{m}$
$\bigr|\frac{f(x+\delta_{m})-f(x)}{\delta_{m}}\bigr|=\bigr|\sum\limits_{n=0}^{m}(\frac{3}{4})^{n}\gamma_{n}\bigr|=\bigr|(\frac{3}{4})^{m}\gamma_{m}+\sum\limits_{n=0}^{m-1}(\frac{3}{4})^{n}\gamma_{n}\geq\bigr|(\frac{3}{4})^{m}\gamma_{m}\bigr|-|\sum\limits_{n=0}^{m-1}(\frac{3}{4})^{n}\gamma_{n}\bigr|$ $=3^{m}-\bigr|\sum\limits_{n=0}^{m-1}(\frac{3}{4})^{n}\gamma_{n}\bigr|\geq3^{m}-\sum\limits_{n=0}^{m-1}(\frac{3}{4})^{n}|\gamma_{n}|\geq3^{m}-\sum\limits_{n=0}^{m-1}3^{n}$ (since  $|\gamma_{n}|\leq 4^{n}$) 
$\rightarrow +\infty$ as $m\rightarrow +\infty$.
$f$ is nowhere differentiable since the choice of $x$ is arbitrary.











