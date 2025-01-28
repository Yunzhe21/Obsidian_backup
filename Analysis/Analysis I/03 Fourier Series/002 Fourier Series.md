#RiemannLebesgueLemma 
<font color="#ff0000">Definition:</font> Let $X=\{x_{1}, x_{2}, \dots\}$ be a **countable orthonormal set** in an **inner product space** $V$ and let $x\in V$, the infinite series 
$$
\sum\limits_{n=1}^{\infty}(x,x_{n})x_{n} ^bf4a7d
$$

is called the Fourier Series of $x$ (relative to $X$)

The Fourier Series of a function $f\in\mathscr{R}[a,a+2\pi]$ relative to Trigonometric set is
$$
\sum\limits_{n=0}^{\infty}(f,\phi_{n})\phi_{n}(x)=\frac{1}{\sqrt{2\pi}}\int_{a}^{a+2\pi}\frac{f(t)}{\sqrt{2\pi}}+\sum\limits_{n=1}^{\infty}
(\frac{\cos(nx)}{\sqrt{\pi}}\int_{a}^{a+2\pi}f(t)\frac{\cos(nt)}{\sqrt{\pi}}dt+\frac{\sin(nx)}{\sqrt{\pi}}\int_{a}^{a+2\pi}f(t)\frac{\sin(nt)}{\sqrt{\pi}}dt)
$$

We often denote $a_{n}=\frac{1}{\pi}\int_{a}^{a+2\pi}f(t)\cos(nt)dt$, $b_{n}=\frac{1}{\pi}\int_{a}^{a+2\pi}f(t)\sin(nt)dt$
Then the series is reduced to $\frac{a_{0}}{2}+\sum\limits_{n=1}^{\infty}(a_{n}\cos(nx)+b_{n}\sin(nx))$ 

Notice that both $a_{n},b_{n}\rightarrow0$ as $n\rightarrow\infty$. (**Riemann-Lebesgue Lemma**)

---

<font color="#ff0000">Example:</font>

Calculate the Fourier Series of $f(x)=x$, where $-\pi\leq x\leq\pi$ 
	$a_{n}=\frac{1}{\pi}\int_{-\pi}^{\pi}t\cos(nt)dt=0$
	$b_{n}=\frac{1}{\pi}\int_{-\pi}^{\pi}t\sin(nt)dt=(-1)^{n+1}\frac{2}{n}$
	Then the Fourier Series is concluded.

The Fourier Series of a function $f\in\mathscr{R}[a,a+2\pi]$ converges to $f$ if $\forall\epsilon>0$, there exists $N$ s.t. whenever $n>N$, we have 
$$

\|f-\sum\limits_{i=0}^{n}(f,\phi_{i})\phi_{i}(x)\|<\epsilon
$$ 
which means 
$$
\sqrt{\int_{a}^{a+2\pi}(f-\sum\limits_{i=0}^{n}(f,\phi_{i})\phi_{i})dt}<\epsilon
$$


We call such convergence $\mathscr{L}^{2}$ convergence.

---

So here are two fundamental questions concerning Fourier Series:
	1. Does Fourier Series of $f$ converges pointwise to $f$ ? [[003 Pointwise Convergence of Fourier Series|Discuss]]
	2. Does Fourier Series of $f$ converges uniformly to $f$ ? [[004 Uniform Convergence of Fourier Series|Discuss]]



