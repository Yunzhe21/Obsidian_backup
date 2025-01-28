#RiemannIntegrable #DarbonxRiemanCriteria #RiemannSum #ChangeOfVariableFormula 
We will be primarily discussing Riemann Integral rather than a more general case (Riemann–Stieltjes Integral) just for simplicity.

---

## Riemann Integral

<font color="#ff0000">Definition:</font> Partition $P$ of an interval $[a,b]$, $P: a=x_{0}<x_{1}<\cdots<x_{n}=b$, $\Delta x_{i}=x_{i}-x_{i-1}$

Let $f:[a,b]\longrightarrow\mathbb{R}$ be a bounded function.

<font color="#ff0000">Definition:</font> (Upper & Lower Sum) $U(f,P)=\sum\limits_{i=1}^{n}M_{i}\Delta x_{i}$, where $M_{i}=\sup\{f(x): x_{i-1}\leq x\leq x_{i}\}$
$\mathscr{L}(f,P)=\sum\limits_{i=1}^{n}m_{i}\Delta x_{i}$, where $m_{i}=\inf \{f(x): x_{i-1}\leq x\leq x_{i}\}$

$\overline{\int_{a}^{b}}f(x)dx=\inf\{U(f,P): P \ \text{be arbitrary partition}\}$ 
${} \underline{\int_{a}^{b}}f(x)dx=\sup\{\mathscr{L}(f,P): P\ \text{be arbitrary partition}\} {}$

<font color="#ff0000">Question:</font> Is $\overline{\int_{a}^{b}}f(x)dx\geq\underline{\int_{a}^{b}}f(x)dx$ ?

<font color="#ff0000">Definition:</font> (Refinement) Let $P$ be a partition, $P^{*}$ is called a refinement of $P$ if $P\subseteq P^{*}$ 

<font color="#ff0000">Theorem:</font> If $P^{*}$ is a refinement of $P$, then $\mathscr{L}(f,P)\leq\mathscr{L}(f,P^{*})\leq U(f,P^{*})\leq U(f,P)$
	[[Riemann Integral (Proof)#^0d846e|Proof]]

<font color="#ff0000">Definition:</font> #RiemannIntegrable $f$ a bounded function on $[a,b]$ is called Riemann Integrable if $\overline{\int_{a}^{b}}fdx=\underline{\int_{a}^{b}}fdx$

---

## Integrable

Here are some criteria in judging whether the function is Riemann integrable.

<font color="#ff0000">Theorem:</font> #DarbonxRiemanCriteria Let $f$ be a bounded function on $[a,b]$, then $f$ is Riemann Integrable $\iff$ $\forall \epsilon>0: \exists$ partition $P$ s.t. $U(f,P)-\mathscr{L}(f,P)<\epsilon$
	[[Riemann Integral (Proof)#^f60ab3|Proof]]

<font color="#ff0000">Theorem:</font> If $f\in C[a,b]$, then ${} f\in\mathscr{R}[a,b] {}$.
	Cucial point is #Compactness 
	[[Riemann Integral (Proof)#^a61b7e|Proof]]

<font color="#ff0000">Theorem:</font> If $f: [a,b]\longrightarrow\mathbb{R}$ is bounded and monotone, then $f\in\mathscr{R}[a,b]$
	[[Riemann Integral (Proof)#^debd58|Proof]]

<font color="#ff0000">Theorem:</font> Let $f\in\mathscr{R}[a,b]$, with $m\leq f(x)\leq M$ for all $x\in[a,b]$. Let $g: [m,M]\longrightarrow\mathbb{R}$, then $g\circ f(x)\in\mathscr{R}[a,b]$.
	[[Riemann Integral (Proof)#^d712a7|Proof]]

<font color="#ff0000">Definition:</font> #RiemannSum Let $P: a=x_{0}<x_{1}<\cdots<x_{n}=b$ be a partition and $t_{i}\in[x_{i-1}, x_{i}]$, then $S(f,P,T)=\sum\limits_{i=1}^{n}f(t_{i})\Delta x_{i}$, where $T$ is the set of all $t_{i}'s$.
Naturally, we can conclude that $\mathscr{L}(f,P)\leq S(f,P,T)\leq U(f,P)$

In previous cases, we assume arbitrary partition, but it's not practical. So we aim to use equal partition only.

<font color="#ff0000">Lemma:</font> $f\in\mathbb{R}\iff \forall\epsilon>0: \exists$ an equal partition $P$ s.t. $U(f,P)-\mathscr{L}(f,P)<\epsilon$
	[[Riemann Integral (Proof)#^da33d4|Proof]]

---

## Properties

<font color="#ff0000">Fundamental Theorem of Calculus</font>
1. If $f$ is continuous function on $[a,b]$ and differentiable on $[a,b]$, $f'(x)\in\mathscr{R}[a,b]$, then $\int_{a}^{b}f'(x)dx=f(b)-f(a)$
2. If $f\in\mathscr{R}[a,b]$ and let $F(x)=\int_{a}^{x}f(t)dt$, $x\in[a,b]$. Then $F(x)$ is differentiable at $x_{0}$ whenever $f$ is continuous at $x=x_{0}$ and $F'(x_{0})=f(x_{0})$

<font color="#ff0000">Theorem:</font> #ChangeOfVariableFormula If $f\in\mathscr{R}[a,b]$ and $g$ is a differentiable and one-one map from $[c,d]$ onto $[a,b]$ with $g'\in\mathscr{R}$, then $f\circ g(x)g'(x)dx=\int_{a}^{b}f(u)du$ 
	[[Riemann Integral (Proof)#^b77223|Proof]]










































