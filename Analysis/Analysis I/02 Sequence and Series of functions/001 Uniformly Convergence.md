#UniformConvergence #InfiniteNorm 
<font color="#ff0000">Definition:</font> (Uniformly Convergence) Let $\{f_{n}\}$ be a sequence of functions from $(M,d)$ to $\mathbb{R}$, we say $\{f_{n}\}$ converges uniformly to $f$ if $\forall \epsilon>0$, $\exists N\in \mathbb{N}^{+}$ s.t. whenever $n>N$, $|f_{n}(x)-f(x)|<\epsilon$ for all $x\in M$.
	Note that the choice of $N$ is independent of $x$.

<font color="#ff0000">Theorem:</font> (Cauchy Criteria) Let $\{f_{n}\}$ be a sequence of functions form $(M,d)$ to $\mathbb{R}$, then $\{f_{n}\}$ converges unidformly to $f$ if $\forall\epsilon>0$, $\exists N>0$ s.t. whenever $m,n>N$, $|f_{m}-f{n}|<\epsilon$. ^CauchyCriteria
	[[Sequence and Series of functions (Proof)#^505a69|Proof]]

<font color="#ff0000">Definition:</font> (Infinite Norm) Let $f: (M,d)\rightarrow \mathbb{R}$, then $\|f\|_{\infty}=\text{sup}\{f(x): x\in M\}$  

<font color="#ff0000">Corollary:</font> $\{f_{n}\}$ converges uniformly to $\{f\}$ iff $\|f_{n}-f\|_{\infty}\rightarrow0$ 
	Proof

<font color="#ff0000">Example:</font> Denote $B[a,b]$ be the set of bounded functions, with metric $d(f,g)=\|f-g\|_{\infty}$, then $(B[a,b], d)$ is complete.
	[[Sequence and Series of functions (Proof)#^fd405e|Proof]]




























