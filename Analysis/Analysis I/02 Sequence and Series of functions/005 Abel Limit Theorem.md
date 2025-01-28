#AbelSummable #CesaroSummable #AbelTest #AbelTheorem #SummationByParts #TauberianTheorem 
## Abel's Theorem

<font color="#ff0000">Definition:</font> (Abel summability) Given $\sum\limits_{n=0}^{\infty}a_{n}$, if $\sum\limits_{n=0}^{\infty}a_{n}x^{n}=f(x)$ converges for $|x|<1$, and define $\lim_{x\to1^{-}}f(x)=S$, then define $\sum\limits_{n=0}^{\infty}a_{n}=S$ (Abel) and $\sum\limits_{n=0}^{\infty}a_{n}$ is called Abel summable. ^AbelSummable

<font color="#ff0000">Example:</font> $\sum\limits_{n=0}^{\infty}(-1)^{n}$ 
$\sum\limits_{n=0}^{\infty}(-1)^{n}x^{n}=1-x+x^{2}\dots=\frac{1}{1+x}$
Then $\sum\limits_{n=0}^{\infty}=\frac{1}{2}\ (A)$ (i.e. in Abelian sense)

<font color="#ff0000">Theorem:</font> (Abel's Theorem) Let $\sum\limits_{n=0}^{\infty}a_{n}$ be a cpnvergent series, then $\sum\limits_{n=0}^{\infty}a_{n}x^{n}$ converges uniformly on $[0,1]$ ^AbelThm

To prove this theorem, we first need to prove **Abel Test**
**Abel Test**: Let $\{u_{n}(x)\}$ be a sequence of functions on $X$ s.t. $\sum\limits_{n=1}^{\infty}u_{n}(x)$ converges uniformly on $X$. Let $\{v_{n}(x)\}$ be a sequence of monotone decreasing (in $n$) function in $X$, $\{v_{n}(x)\}$ are uniformly bounded. Then $\sum\limits_{n=1}^{\infty}u_{n}v_{n}$ converges uniormly on $X$. ^AbelTest

Hint: Use **summation by parts**
		For $\sum\limits_{k=1}^{n}a_{k}b_{k}$, let $S_{k}=\sum\limits_{j=1}^{k}a_{j}$ and $S_{0}=0$, we have $\sum\limits_{k=1}^{n}a_{k}b_{k}=\sum\limits_{k=1}^{n}(S_{k}-S_{k-1})b_{k}=\sum\limits_{k=1}^{n}S_{k}b_{k}-\sum\limits_{k=1}^{n-1}S_{k}b_{k+1}=\sum\limits_{k=1}^{n-1}S_{k}(b_{k}-b_{k+1})+S_{n}b_{n}$ ^SummationByParts

[[Sequence and Series of functions (Proof)#^7cc85e|Proof of Abel Test]]
[[Sequence and Series of functions (Proof)#^a2fb48|Proof of Abel's Theorem]]

### Examples

<font color="#ff0000">Example 1:</font> $(\log(1+x))'=\frac{1}{1+x}=1-x+x^{2}-x^{3}+\dots$
	Notice that the power series converges uniformly when $|x|<1$
	Then $\log(1+x)=x-\frac{x^{2}}{2}+\frac{x^{3}}{3}-\dots=\sum\limits_{n=1}^{\infty}(-1)^{n-1}\frac{x^{n}}{n}$ converges uniformly on $[0,1]$.

<font color="#ff0000">Example 2:</font> $(\arctan(x))'=\frac{1}{1+x^{2}}=1-x^{2}+x^{4}-x^{6}+\dots$
	Notice that the power series converges uniformly
	Then $\arctan(x)=x-\frac{x^{3}}{3}+\frac{x^{5}}{5}-\frac{x^{7}}{7}+\dots$ 
	Moreover, we find that $\frac{\pi}{4}=\arctan(1)=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots$

## Relation between Convergent, Cesaro Summable and Abel Summable

<font color="#ff0000">Definition:</font> (Cesaro Summable) Given $\sum\limits_{n=1}^{\infty}a_{n}$, we say that the series is Cesaro Summable if $\sum\limits_{k=1}^{n}\frac{S_{k}}{n}\rightarrow s$, where $S_{k}=\sum\limits_{j=1}^{k}a_{j}$. Denote $s=(C)\sum\limits_{n=1}^{\infty}a_{n}$. ^CesaroSummable

<font color="#ff0000">Summary:</font> 
	1. Convergence $\Longrightarrow$ Abel Summable (by  [[005 Abel Limit Theorem#^AbelThm|Abel Theorem]]), however, the reverse is not true
		Eg. $\sum\limits_{n=1}^{\infty}(-1)^{n}$
	2. Cesaro Summable $\centernot\implies$ Converges
		Eg. $\sum\limits_{n=1}^{\infty}(-1)^{n}$ 
	3. Abel Summable $\centernot\implies$ Cesaro Summable
		Eg. $\sum\limits_{n=0}^{\infty}(-1)^{n+1}n$ 

<font color="#ff0000">Theorem:</font> (Tauberian First Theorem) If $(A)\sum\limits_{n=0}^{\infty}a_{n}=s$ (Abel Summable), and if $na_{n}\rightarrow0$, then $\sum\limits_{n=0}^{\infty}a_{n}$ converges.
	This Theorem is an attempt to show how Summary 1 can be improved.
	[[Sequence and Series of functions (Proof)#^5a8071|Proof]] 

<font color="#ff0000">Theorem:</font> (Cesaro Summable implies Abel Summable) If $(C)\sum\limits_{n=0}^{\infty}a_{n}=s$, then $(A)\sum\limits_{n=0}^{\infty}a_{n}=s$
	[[Sequence and Series of functions (Proof)#^b4b41d|Proof]]






