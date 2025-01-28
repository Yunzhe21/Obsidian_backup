#DiniTheorem 
## Uniform convergence and Continuity

<font color="#ff0000">Lemma:</font> (Uniform Convergence preserves Continuity) Let $\{f_{n}\}$ be a sequence of functions from $(M,d)$ to $\mathbb{R}$ that all $f_{n}$ continuous at point $x=a$, and that $\{f_{n}\}$ converges uniformly to $f$, then $f$ is continuous at point $x=a$.
	[[Sequence and Series of functions (Proof)#^abcf77|Proof]] ^UniformCont

<font color="#ff0000">Coro:</font> $\{f_{n}\}_{n=1}^{\infty}\subset \mathscr{C}[a,b]$ and $f_{n}\rightarrow f$ uniformly, then $f\in\mathscr{C}[a,b]$ 
	$\Longrightarrow (\mathscr{C}[a,b],\|\cdot\|_{\infty})$ is complete metric space

<font color="#ff0000">Theorem:</font> (Dini Theorem) If $\{f_{n}\}$ is a sequence in $\mathscr{C}[a, b]$ s.t. $f_{n}\geq f_{n+1} \geq\dots$ If $f_{n}\rightarrow f$ pointwise and $f$ is continuous, then $f_{n}\rightarrow f$ uniformly.
	[[Sequence and Series of functions (Proof)#^fe3c96|Proof]] ^DiniThm

## Uniform Convergence and Integrability

<font color="#ff0000">Theorem:</font> (Uniform Convergence preserves Integrability) Let $\{f_{n}\}$ be a sequence of functions in $\mathscr{R}[a, b]$. Assume that $f_{n}$ converges uniformly to $f$, then $f\in\mathscr{R}[a, b]$, and $\int_{a}^{b}f_{n}(x)dx\rightarrow\int_{a}^{b}f(x)dx$ as $n$ approach $\infty$.
	[[Sequence and Series of functions (Proof)#^cacde9|Proof]] ^UniformInt

## Uniform Convergence and Differentiability

For differentiability, we can't easily say that uniform convergence preserves differentiability

<font color="#ff0000">Theorem:</font> Suppose $\{f_{n}\}$ be a sequence of **differentiable functions** on $[a,b]$, $\{f_{n}\}$ converges at some point $x_{0}$. If $\{f'_{n}\}$ converges uniformly on $[a,b]$, then $\{f_{n}\}$ converges uniformly on $[a,b]$ to $f$, and $f'=\lim_{n=1}^{\infty}f'_{n}$.
	[[Sequence and Series of functions (Proof)#^113c33|Proof]] ^UniformDiff












