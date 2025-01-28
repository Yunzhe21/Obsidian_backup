#CloseSubset #OpenSubset #RelativeMetric #Compactness #Connectness #Completeness 
#AccumulationPoint #TotallyBounded
## Closed Subset

<font color="#ff0000">Definition:</font> (Cluster point or Accumulation point) Let $(\mathbb{M}, d)$ be a metric space, and let $X$ be a subset of $\mathbb{M}$. Given $x\in \mathbb{M}$, we say $x$ is an *accumulation point* of $X$ if there exists $\{x_{n}\}\subset X-\{x\}$ s.t. $\{x_{n}\}\rightarrow x$.   

![[ee53abfe1b60f965ca51b27ba4969ef.jpg|Accumulation point]]

<font color="#ff0000">Definition:</font> (Closed subset) A subset $X$ is called a closed subset of $\mathbb{M}$ if $X$ contains all it accumulation points, i.e. $X$ is closed $\iff$ $X=\bar{X}$. 

<font color="#ff0000"><font color="#ff0000">Proposition A</font>: </font> A finite union of closed subsets of $\mathbb{M}$ is also closed, i.e. If $X_{1}, \dots, X_{n}$ are closed, then $\bigcup_{i=1}^{n}X_{i}=X$ is closed.
	[[Metric Space (Proofs)#^0873e4|Proof]]

<font color="#ff0000">Proposition B:</font> An infinite intersection of closed subsets of $\mathbb{M}$ is also closed, i.e. If $\{X_{j}\}_{j=1}^{\infty}$ are closed subsets of $\mathbb{M}$, then $\bigcap_{j=1}^{\infty}X_{j}=X$ is closed.
	[[Metric Space (Proofs)#^353f1a|Proof]]

## Open Subset

<font color="#ff0000">Definition:</font> (Open subset) Let $X\subset \mathbb{M}$, we say $X$ is open if $\forall x\in X$, there is an $\epsilon>0$ (depending on $x$ and $X$) s.t. $B_{\epsilon}(x)\subset X$

<font color="#ff0000">Theorem:</font> $X\subset \mathbb{M}$ is open $\iff$ $X^{c}=\mathbb{M}-X$ is closed.
	[[Metric Space (Proofs)#^f4b14d|Proof]]  ^ComplementOfCloseOpen

<font color="#ff0000">Proposition A:</font> Let $O_{1}, \dots, O_{N}$ are open in $\mathbb{M}$, then $\bigcap_{i=1}^{N}O_{i}$ is open.
	[[Metric Space (Proofs)#^980e86|Proof]]

<font color="#ff0000">Proposition B:</font> If $\{O_{i}\}_{i=1}^{\infty}$ are open, then $\bigcup_{i=1}^{\infty}O_{i}$ is also open.
	[[Metric Space (Proofs)#^c95eff|Proof]]

## Relative metric

Let $(\mathbb{M}, d)$ be a metric space and let $X\subset \mathbb{M}$. The relative metric on $X$ is simply the restriction of $d$ (on $\mathbb{M}$) onto $X$. It's easy to see that ($X$, $d$) is a metric space.

<font color="#ff0000">Example:</font> An open ball in $X$ centered at $a$: $B_{\epsilon}^{X}(a)=\{x\in X, d(x, a)<\epsilon\}=X\cap B_{\epsilon}(a)$ 

<font color="#ff0000">Theorem:</font> Let $(\mathbb{M},d)$ be a metric space and $X$ as defined above
	1. $U\subset X$, $U$ is open relative to $X$ $\iff$ $U=X\cap V$ for some open $V$ in $\mathbb{M}$.
	2. $E\subset X$ is closed relative to $X$ $\iff$ $E=X\cap F$ for some $F$ closed in $\mathbb{M}$.
	Proof: ^CloseOpenRelative

<font color="#ff0000">Note:</font> "Openness" and "Closeness" can vary according to the *relative metric* we choose. However, **Compactness**, which we will discuss, behaves better under various relative metrices.

## Compact metric space

### Recall

<font color="#ff0000">Theorem:</font> (Heine Borel) Let $\{I_{\alpha}\}_{\alpha\in\Lambda}$ is a collection of open intervals and $[a,b]$ is a closed and bounded interval. Suppose that $[a,b]\subset \bigcup_{\alpha\in\Lambda}I_{\alpha}$, then $\exists \alpha_{1}, \dots, \alpha_{m}$ s.t. $\mathbb{M}\subset \bigcup_{j=1}^{m}O_{\alpha_{j}}$ ^HeineBorel

<font color="#ff0000">Theorem:</font> (Bolzano-Weierstrass Theorem) $[a,b]$ a closed and bounded interval, let $\{x_{n}\}\subset [a,b]$, $\exists$ a subsequence $\{x_{n_{k}}\}$ of $\{x_{n}\}$ s.t. $\{x_{n_{k}}\}\rightarrow x_{\star}$ ^BWThm

Compactness is the generalization of the two theorems.

<font color="#ff0000">Definition:</font> (Open cover) Let $(M,d)$ be a metric space, $\{O_{\alpha}\}_{\alpha\in\Lambda}$ is a collection of open sets that can be called an open cover if $\mathbb{M}\subset\bigcup_{\alpha\in\Lambda}O_{\alpha}$.

<font color="#ff0000">Definition:</font> (Compactness) A metric space is called compact if for any open cover $\{O_{\alpha}\}_{\alpha\in\Lambda}$ of $\mathbb{M}$, there exists a finite subcover $\{O_{i}\}_{i=1}^{n}$.
	This definition coincides with [[002 Topology for metric spaces (M, d)#^HeineBorel|"Heine-Borel Theorem"]] discussed before. 

<font color="#ff0000">Definition:</font> (Sequentially Compactness) $\mathbb{M}$ is sequencially compact if $\forall \{x_{n}\}$ in $\mathbb{M}$, there exists a subsequence $\{x_{n_{k}}\}\rightarrow x_{\star}\in \mathbb{M}$
	This definition coincides with [[002 Topology for metric spaces (M, d)#^BWThm|Bozano-Weierstrass Theorem]] discussed before.

### Compact and Sequentially Compact

It's important to see that **Compactness** and **Sequentially Compactness** are **equivalent**
	[[Metric Space (Proofs)#^5d3219|"Compactness implies Sequentially Compactness"]] 
However, the converse direction is complicated.

First we [[Metric Space (Proofs)#^433766|prove]] a lemma: If $(\mathbb{M},d)$ is sequentially compact, then $\mathbb{M}$ is *totally bounded*, which means that $\forall \epsilon>0$, there are $x_{1}, \dots, x_{m}\in \mathbb{M}$ (the number $m$ depends on $\epsilon$) s.t. $\mathbb{M}\subset \bigcup_{i=1}^{m}B_{\epsilon}(x_{i})$.
	<font color="#ff0000">Note 1:</font> The definition of *totally bounded* is different from the definition of *compact*, since totally bounded requires the cover to be balls, while compactness requires arbitrary open cover.  ^74be69

<font color="#ff0000">Lemma 3:</font> 
	1. If $(\mathbb{M},d)$ is compact, and $K\subset M$ is closed, then $K$ is compact
	2. If $(\mathbb{M}, d)$ is sequentially compact, and $K$ is a closed subset of $\mathbb{M}$, then $K$ is sequentially compact
[[Metric Space (Proofs)#^e2dba9|Proof of 1]]
[[Metric Space (Proofs)#^5e2d84|Proof of 2]] ^886425

<font color="#ff0000">Theorem:</font> If $(\mathbb{M}, d)$ is sequentially compact, then $(\mathbb{M}, d)$ is compact
	[[Metric Space (Proofs)#^cd19a4|Proof]]

In conclusion, Compactness is equivalent to Sequential Compactness ^CompactEqualSequential

### Property of Compact sets

Next, we observe how compact sets behave better than open and closed subsets up to relative metric

<font color="#ff0000">Theorem:</font> Suppose $K\subset Y\subset X$, $K$ is compact relative to $X$ iff $K$ is relative to $Y$.
	[[Metric Space (Proofs)#^667fc8|Proof]]
By virtue of this theorem, we are able to consider compact sets as metric spaces in their own rights.

<font color="#ff0000">Property 1:</font> If $C$ is compact subset of $M$, then $C$ is closed and bounded in $M$
	[[Metric Space (Proofs)#^d87cfd|Proof]]

<font color="#ff0000">Property 2:</font> If $C$ is closed and bounded in $\mathbb{R}^{n}$, then $C$ is compact in $\mathbb{R}^{n}$.
	[[Metric Space (Proofs)#^58787a|Proof]] 

## Connected Metric Space

<font color="#ff0000">Definition:</font> Let $M$ be a metric space, if all subsets of $M$ that are both open and closed relative to $M$ are $\varnothing$  and $M$ itself, then $M$ is called *connected metric space*.  

<font color="#ff0000">Theorem:</font> Let $M$ be a metric space, then the following statements are equivalent:
	1. $M$ is not connected
	2. There are open and nonempty subset $U,V$ s.t. $U\cup V=M$, $U\cap V=\varnothing$.
	3. There are closed and nonempty subset $U,V$ s.t. $U\cup V=M$, $U\cap V=\varnothing$
	For the proof of this theorem, we prove from 1 to 2 & 3; 2 to 3; 3 to 4.
	[[Metric Space (Proofs)#^84b417|Proof]]

### Example

Here we discuss connected subset of $\mathbb{R}$.

<font color="#ff0000">Theorem:</font> A subset $X$ of $\mathbb{R}$ is connected iff $\forall a,b\in X$, and $a<b$, then $[a, b]\subset X$.
	[[Metric Space (Proofs)#^cfbc21|Proof]]

<font color="#ff0000">Corollary:</font> If $X\subset \mathbb{R}$ is a connected set, then $X=\{p\}$ or an interval.

## Complete Metric Space

### Recall:

<font color="#ff0000">Cauchy Sequence:</font> A sequence $\{x_{n}\}$ is called *Cauchy* if $\forall \epsilon>0$, $\exists K\in\mathbb{N}$ s.t. $\forall m,n>K$, $|a_{m}-a_{n}|\leq\epsilon$.

<font color="#ff0000">Remarks:</font>
	1. Convergent sequences are Cauchy.
	2. Cauchy sequences are bounded.

However, there is **no guarantee** that Cauchy sequences are convergent. This is the motivation for the definition of *completeness*.

<font color="#ff0000">Examples:</font> Under the domain $\mathbb{Q}$, we consider a sequence $\{1, 1.4, 1.414, \dots\}$ (decimal expansion of $\sqrt{2}$), the sequence is Cauchy (proof is trivial), however, this sequence doesn't converge because $\sqrt{2}$ is not in the domain.

<font color="#ff0000">Definition:</font> A metric space is *complete* if all Cauchy sequences are convergent.

<font color="#ff0000">Examples:</font> 
	$\mathbb{R}^{n}$ is complete when $n$ is fixed
	$l^{1}, l^{2}, l^{\infty}, c_{0}$ are all complete metric spaces.

Theorem: Let $(M,d)$ be a metric space, then this metric space can always be *completed*, i.e. $(M,d), (\overline{M}, \overline{d})$, s.t. $M\subset \overline{M}$, $d=\overline{d}$ on $M$, and $(\overline{M}, \overline{d})$ is complete.
	Proof is boring, we omit it. The proof can be found in the text book













