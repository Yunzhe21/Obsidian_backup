#MeasureZero #OscillationFunction 

This part will be further developed in **Real Analysis**. Our main focus here is to prove the fact that as long as the function has "small" number of discontinuity, that $f$, being bounded by assumption, will be #RiemannIntegrable 

---

<font color="#ff0000">Defintion:</font> #MeasureZero A set $E\subseteq\mathbb{R}$ is called of measure zero if $\forall\epsilon>0:\exists (a_{i},b_{i})_{n=1}^{\infty}$ s.t. $E\subset\bigcup_{i=1}^{n}(a_{i},b_{i})$ and $\sum\limits_{i=1}^{\infty}(b_{i}-a_{i})<\epsilon$.

Given $f:[a,b]\longrightarrow\mathbb{R}$, $f$ bounded, **the set of discontinuity** of $f$ is denoted as $\mathscr{D}(f)$

<font color="#ff0000">Definition:</font> #OscillationFunction $\omega_{f}(x,\delta)=\sup f(y)-\inf f(y)$ for $y\in(x-\delta,x+\delta)$
	Notice that when $\delta\downarrow$, then $\omega_{f}(x,\delta)\downarrow$ 
	Define $\omega_{f}(x)=\lim_{\delta\to0^{+}}\omega_{f}(x,\delta)$

These lemma below are crucial in proving the **Lebesgue Theorem**, which is the goal of this chapter.

<font color="#ff0000">Lemma:</font> $f$ is continuous at $x_{0}\iff \omega_{f}(x_{0})=0$
	[[Riemann Integral (Proof)#^1320dc|Proof]]

We observe from this lemma that $\mathscr{D}(f)=\{x: \omega_{f}(x)>0\}=\bigcup_{m=1}^{\infty}\{x: \omega_{f}(x)\geq\frac{1}{m}\}$

<font color="#ff0000">Lemma:</font> For $c>0$, ${} \{x\in[a,b]:\omega_{f}(x)<c\} {}$ is open, where $f$ is bounded in $[a,b]$
	[[Riemann Integral (Proof)#^8038bb|Proof]]
	This lemma indicates that $\{x\in[a,b]:\omega_{f}(x)\geq\frac{1}{m}\}$ is closed.

<font color="#ff0000">Lemma:</font> 
