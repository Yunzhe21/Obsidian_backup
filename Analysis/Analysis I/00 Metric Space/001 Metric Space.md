#MetricSpace #Sequence 
## Definition and examples

**<font color="#ff0000">Definition:</font>**  Let $\mathbb{M}$ be a set, a metric on $\mathbb{M}$ is a function $d:\ \mathbb{M}\times\mathbb{M}\longrightarrow [0, +\infty)$ satisfying:
	1). $d(x,y)=0$ iff $x=y$ 
	2). $d(x,y)=d(y,x)$ for all $x,y\in \mathbb{M}$
	3). $d(x,z)\leq d(x,y)+d(y,z)$ for all $x,y,z\in \mathbb{M}$ <font color="#ff0000">(triangular inequality)</font> ^MetricSpace

### Example 1
For $\mathbb{R}^{2}$, $d(x,y)=\sqrt{(x_{1}-y_{1})^{2}+(x_{2}-y_{2})^{2}}$  defines a metric on $\mathbb{R}^{2}$, called "usual/Euclidean metric on $\mathbb{R}^{2}$"
	Proof of this $d$ as a metric is simple except for the third criterion, which we will prove it by proving a stronger statement regarding $\mathbb{R}^{n}$.

### Example 2
<font color="#ff0000">Definition:</font> Let $l^{1}$ denotes the set of all real sequences $\{a_{n}\}$ s.t. $\sum\limits_{n=1}^{\infty}{a_{n}}$ converges absolutely 

Define $d(\{a_{n}\}, \{b_{n}\})=\sum\limits_{n=1}^{\infty}|a_{n}-b_{n}|$, then $d$ is a metric on $l^{1}$
	[[Metric Space (Proofs)#^0c8517|Proof]] 

### Example 3
Let $\mathbb{X}$ be a set, define $d(x,y)=$
	0, if $x=y$
	1, if $x\neq y$
is a metric on $\mathbb{X}$.
	Proof is routine.

### Example 4
The space $\mathbb{R}^{n}$ is called *real Euclidean n-space* where $d(x,y)=\sqrt{\sum\limits_{k=1}^{n}(x_{k}-y_{k})^{2}}$
	[[Metric Space (Proofs)#^4987c9|Verify]]

### Example 5
<font color="#ff0000">Example 5:</font> $d(x,y)=\sqrt{\sum\limits_{1}^{\infty}(x_{k}-y_{k})^{2}}$ defines a metric on $l^{2}$
	First [[Metric Space (Proofs)#^4289cc|verify]] that $d$ is well-defined on $l^{2}$
	Then we [[Metric Space (Proofs)#^370861|verify]] the three criteria.

## Sequences in general Metric Space

<font color="#ff0000">Definition:</font> Let $(\mathbb{M}, d)$ be a metric space and let $\{a_{n}\}$ be a sequence of points in $\mathbb{M}$. We say that $\{a_{n}\}\rightarrow a$ as $n\rightarrow n$ if $\forall \epsilon>0, \exists N\in \mathbb{N}$ s.t. if $n\leq N$, then $0\leq d(a_{n}, a)<\epsilon$  

<font color="#ff0000">Fact:</font> $\{x^{k}\}$ in $\mathbb{R}^{n}$, $x^{k}=(x_{1}^{k}, \dots, x_{n}^{k})$. Then $\{x^{k}\}\rightarrow x \iff$ For each $j\in\{1, \dots, n\}$, $\{x_{j}^{k}\}\rightarrow x$
	[[Metric Space (Proofs)#^28bf6e|Proof]]

Note that this statement doesn't hold for infinite dimensional metric spaces.
<font color="#ff0000">Example</font>: consider $$\delta_{n}^{k}=\left\{\begin{matrix}
 0 &n\neq k \\
  1&n=k
\end{matrix}\right.$$
$x_{j}^{k}\rightarrow 0$, but $x^{k}$ not approaching 0.


