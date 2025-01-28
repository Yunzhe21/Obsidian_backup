
### Continuity

<font color="#ff0000">Definition:</font> $f: (M_{1},d_{1})\rightarrow (M_{2}, d_{2})$ is continuous at $x=a\in M_{1}$ if $\forall \epsilon>0$, $\exists \delta>0$ s.t. whenever $d(x,a)<\delta$, then $d(f(x), f(a))<\epsilon$.

<font color="#ff0000">Sequentially characterization of continuity:</font> 

<font color="#ff0000">Theorem:</font> $f: (M_{1}, d_{1})\rightarrow (M_{2}, d_{2})$ is continuous at $x=a\in M_{1}\iff$ $\forall \{x_{n}\}$ s.t. $x_{n}\rightarrow a$, then $\{f(x_{n})\}\rightarrow f(a)$.
	[[Metric Space (Proofs)#^c82423|Proof]]

<font color="#ff0000">Theorem:</font> The followings are equivalent for $f:(M_{1}, d_{1})\rightarrow (M_{2}, d_{2})$:
	1. $f$ is continuous on $M_{1}$
	2. $\forall V$ open in $M_{2}$, $f^{-1}(V)=U\subset M_{1}$ is also open
		The reverse is not true, consider $f: O\subset M_{1}\longmapsto a\in \mathbb{R}$, $O$ is open, however, $f(O)=\{a\}$ is closed.
	3. $\forall F$ closed in $M_{2}$, $f^{-1}(F)=E\subset M_{1}$ is also closed
		The reverse is not true, consider $f(x)=e^{-x}$ with domain $[0, +\infty)$, the image is $(0, 1]$, not closed. 
	[[Metric Space (Proofs)#^0c0e0b|Proof]] ^527004

<font color="#ff0000">Composition:</font> $(M_{1}, d_{1})\overset{f}{\rightarrow} (M_{2}, d_{2})\overset{g}{\rightarrow} (M_{3}, d_{3})$, $f,g$ are continuous, then $g\circ f$ is continuous.
	Proof:

---

### Compactness and Function

<font color="#ff0000">Theorem:</font> 
	1. If $f: (M, d)\rightarrow \mathbb{R}$ and $M$ is compact, then $f$ is bounded.
	2. There are $x_{min}\in M$ and $x_{max}\in M$ s.t. $f(x_{min})=min(f(x))\leq max(f(x))=f(x_{max})$
	[[Metric Space (Proofs)#^022d32|Proof]]

#### Compactness and Continuity

<font color="#ff0000">Theorem:</font> $f:(M_{1}, d_{1})\rightarrow (M_{2}, d_{2})$ is continuous on a compact set, then $f$ is uniformly continuous.
	[[Metric Space (Proofs)#^9db0f1|Proof]] is similar to the one for closed interval

<font color="#ff0000">Theorem:</font> If $f$ is continuous and bijective from $(M_{1} ,d_{1})\rightarrow (M_{2}, d_{2})$, and if $(M_{1}, d_{1})$ is compact, then $f^{-1}: (M_{2}, d_{2})\rightarrow (M_{1}, d_{1})$ is also continuous.
	[[Metric Space (Proofs)#^790b31|Proof]]






