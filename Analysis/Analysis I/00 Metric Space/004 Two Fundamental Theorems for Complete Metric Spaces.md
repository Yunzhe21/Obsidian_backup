#BaireCategoryTheorem #BanachFixedPointTheorem
#NoWhereDense #FirstCatgory #ContractingMap #Dense
In this section, we will observe
	1. Baire Category Theorem
	2. Banach fixed point Theorem (contracting map)

---

## Baire Category Theorem

<font color="#ff0000">Definition:</font> (Dense) Let $X\subset (M,d)$, $X$ is called *dense* in $M$ if $\overline{X}=M$.

<font color="#ff0000">Theorem:</font> If $\{O_{n}\}_{n=1}^{\infty}$ is a collection of **open and dense** sets in a **complete** metric space $M$, then $\bigcap_{n=1}^{\infty}O_{n}$ is also dense in $M$.
	[[Metric Space (Proofs)#^d1dfc3|Proof]] ^a19c2e

<font color="#ff0000">Definition:</font> $X\subset M$ is called *nowhere dense* if $\overline{X}^{c}$ is open and dense in $M$.

<font color="#ff0000">Definition:</font> $X\subset M$ is of *1-st category* if $X$ is a **countable union** of **nowhere dense** sets in $M$. $X\subset M$ is of *2-nd category* if $X$ is not of *1-st category*.

<font color="#ff0000">Theorem:</font> (Baire Category Theorem) If $M\neq\varnothing$ is a complete metric space, then $M$ is of 2-nd category. (**not** a countable union of nowhere dense sets) #BaireCategoryTheorem 
	[[Metric Space (Proofs)#^491b25|Proof]] ^BaireCategoryThm

---
### Application

![[屏幕截图 2023-12-19 160149.png]]

<font color="#ff0000">Definition:</font> (isolated point) Let $M$ be a metric space and $x\in M$, $x$ is an isolated point if $\exists \epsilon>0$, $B_{\epsilon}(x)\cap M=\{x\}$.

<font color="#ff0000">Theorem:</font> If $M$ is a complete metric space with no isolated points, then $M$ is uncountable.
	[[Metric Space (Proofs)#^ea9594|Proof]]

## Banach Fixed Point Theorem

<font color="#ff0000">Definition:</font> (Contracting mapping) Let $(M,d)$ is a complete metric space. A mapping $f: M\rightarrow M$ is called a *contraction* if there exists positive constant $K<1$ s.t. $d(f(x), f(y))<Kd(x,y)$ for all $x,y\in M$.

<font color="#ff0000">Theorem:</font> (Banach Fixed Point Theorem) Let $(M,d)$ be a complete metric space and let $f: M\rightarrow M$ be a contraction on $M$. Then $f$ hasn a unique fixed point on $M$.
	[[Metric Space (Proofs)#^c210bc|Proof]]










