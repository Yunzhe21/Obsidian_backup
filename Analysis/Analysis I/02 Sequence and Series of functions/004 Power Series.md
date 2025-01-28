
<font color="#ff0000">Definition:</font> (Power Series) $\sum\limits_{n=0}^{\infty}a_{n}(x-t)^{n}$, $\{a_{n}\}\subset \mathbb{R}$, $x\in (a,b)$ 

<font color="#ff0000">Root Test:</font> Let $L=\limsup_{n\to\infty}|a_{n}|^{\frac{1}{n}}$, and let  $$R=\left\{\begin{matrix}
  0&\text{if}\ L=\infty  \\
  \frac{1}{L}&\text{if}\ 0<L<\infty  \\
  \infty&\text{if}\ L=0 
\end{matrix}\right.$$
Then the series converges if $|x-t|<R$, and diverges if $|x-t|>R$ ^RootTest

<font color="#ff0000">Theorem:</font> Let $\sum\limits_{n=0}^{\infty}a_{n}(x-t)^{n}$ be a power series and let $R$ be the radius of convergence. Let $0<S<R$, then $\sum\limits_{n=0}^{\infty}a_{n}(x-t)^{n}$ converges uniformly on $[t-S,t+S]$.
	[[Sequence and Series of functions (Proof)#^697 eaa|Proof]] ^UniformConvOfPowerSeries

**Conclusion:** $$
\sum\limits_{n=0}^{\infty}a_{n}(x-t)^{n}\ \left\{\begin{matrix}
  \text{Converges} &\text{if}\ |x-t|<R  \\
  \text{Diverges} &\text{if}\ |x-t|>R  \\
  \text{Uniformly Converges} &\text{if}\ |x-t|\leq S,\ \ 0<S<R 
\end{matrix}\right.
$$

<font color="#ff0000">Corollary:</font> $f$ is continuous on $(t-R,t+R)$ 
	$f$ is continuous on $[t-S,t+S]$ for every $0<S<R$. (uniform convergence)
	Then the corollary is proved.

<font color="#ff0000">Theorem:</font> (Integration on power series) Just follow [[002 Characteristic of Uniformly Convergence#^UniformInt|Theorem]].

<font color="#ff0000">Theorem:</font> (Differentiation on power series)

<font color="#ff0000">Theorem:</font> (Uniqueness of power series) If $\sum\limits_{n=0}^{\infty}a_{n}(x-x_{0})^{n}$ is a convergent (absolutely) power series for $|x-x_{0}|<R$, and if $\sum\limits_{n=0}^{\infty}a_{n}(x-x_{0})^{n}=0$ for $|x-x_{0}|<R$, then $a_{n}=0$ for all $n$
	[[Sequence and Series of functions (Proof)#^9a3384|Proof]]

**Example:** (Taylor Expansion) Suppose $f(x)=\mathscr{C}^{m+1}[a,b]$ (i.e. $f$ and its derivatives up to order $m+1$ is continuous on $[a,b]$), then $f(x)-P_{f}^{a}(x)=\frac{f^{m+1}(\xi)}{(m+1)!}(x-a)^{m+1}$ for $x\in[a,b]$, $P_{f}^{a}(x)=f(a)+f'(a)(x-a)+\dots+\frac{f^{(m)}(a)}{m!}(x-a)^{m}$ 







