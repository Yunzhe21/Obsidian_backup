
#ExponentialFunction #LogarithmicFunction #TrigonometricFunctions #EulerFormula #FourierSeriesExpansion 
This part is taken form Rudin's Book "*Principles of Mathematical Analysis*." (Third Edition)

We start by reconstructing elementary functions we've learned before

---

## Exponential Functions

<font color="#ff0000">Definitition:</font> (Exponential Function) 
$$
E(z)=\sum\limits_{n=0}^{\infty}\frac{z^{n}}{n!}
$$ 
By Ratio Test, we know that this series **converges** for every complex number $z$. 

### Property

By **Cauchy Summation**, we have
$$
E(z)E(w)=\sum\limits_{n=0}^{\infty}\frac{z^{n}}{n!}\sum\limits_{m=0}^{\infty}\frac{w^{m}}{m!}=\sum\limits_{n=0}^{\infty}\sum\limits_{k=0}^{n}\frac{z^{k}w^{n-k}}{k!(n-k)!}=\sum\limits_{n=0}^{\infty}\frac{1}{n!}\sum\limits_{k=0}^{n}\binom{n}{k}z^{k}w^{n-k}
=\sum\limits_{n=0}^{\infty}\frac{(z+w)^{n}}{n!}
$$ 
This means that 
$$
E(z+w)=E(z)E(w)
$$ 
 where $z,w$ are complex.

A natural consequence is that 
$$
E(z)E(-z)=E(0)=1
$$
This also implies that $E(z)\neq 0$ for all $z\in\mathbb{C}$ 

By definition, $E(x)>0$ if $x>0$, then by the fact that $E(z)E(-z)=1$, we obtain that $E(x)>0$ for all $x\in\mathbb{R}$.

By definition, $E(x)\rightarrow +\infty$ as $x\rightarrow +\infty$, then by the same fact above, $E(x)\rightarrow0$ as $x\rightarrow-\infty$ 

By definition, $0<x<y$ implies $E(x)<E(y)$, and by the same fact above, $E(-y)<E(-x)$. This shows that $E(x)$ is **strictly increasing** on the real axis.

**Differentiating** $E(x)$:
$$
\lim_{h=0}\frac{E(z+h)-E(z)}{h}=E(z)\lim_{h=0}\frac{E(h)-1}{h}=E(z)
$$
The last equality follows from that fact that:
$$
\frac{E(h)-1}{h}=\frac{1}{h}(h+\frac{h^{2}}{2!}+\cdots)
$$

**Iterating** $E(x+y)=E(x)E(y)$, we have 
$$
E(z_{1}+\cdots+z_{n})=E(z_{1})\cdots E(z_{n})
$$ 
Take $z_{1}=\cdots=z_{n}=1$, since $E(1)=e$, we have 
$$
E(n)=e^{n}
$$ 
We [[Fourier Series (Proof)#^6b455a|extend]] the domain from $\mathbb{N}$ to $\mathbb{R}$, $E(x)=e^{x}$

<font color="#ff0000">Notation:</font> $\exp(x)$ is often used to denote $e^{x}$, when $x$ has a complicated expression.

<font color="#ff0000">Theorem:</font>
	1. $e^{x}$ is continuous and differentiable for all $x$
	2. $(e^{x})'=e^{x}$
	3. $e^{x}$ is a strictly increasing function of $x$, $e^{x}>0$.
	4. $e^{x+y}=e^{x}e^{y}$
	5. $e^{x}\rightarrow+\infty$ as $x\rightarrow+\infty$, $e^{x}\rightarrow0$ as $x\rightarrow-\infty$ 
	6. $\lim_{x\rightarrow+\infty}x^{n}e^{-x}=0$ for every $n$.
	[[Fourier Series (Proof)#^adda82|Proof of the last property]]

This is one way to construct the exponential function.

---

## Logarithmic Function

Since $E$ is strictly increasing and differentiable on $\mathbb{R}$, it has an inverse function, let's denote it as $L$. We call it the logarithmic Function (or $\log$ by convention.)

### Properties 

**Differentiation:** We have $L(E(x))=x$ and $E(L(y))=y$, then by the Chain Rule
$$
L'(E(x))E(x)=1
$$ 
 writing $y=E(x)$, this gives us $$
L'(y)=\frac{1}{y}\ (y>0).$$
**Algebraic:** Writing $u=E(x), v=E(y)$, we have by virtue of the properties proven in the previous section.
$$
L(uv)=L(E(x)E(y))=L(E(x+y))=x+y
$$ 
 which means $L(uv)=L(u)+L(v)$.

**Long-term Behavior:**  
$\log(x)\rightarrow+\infty$ as $x\rightarrow+\infty$
$\log(x)\rightarrow-\infty$ as $x\rightarrow0$.

For if $0<\epsilon<\alpha$, and $x>1$, then 
$x^{-\alpha}\log(x)=x^{-\alpha}\int_{1}^{x}t^{-1}dt<x^{-\alpha}\int_{1}^{x}t^{\epsilon-1}dt=x^{-\alpha}\cdot\frac{x^{\epsilon}-1}{\epsilon}<\frac{x^{\epsilon-\alpha}}{\epsilon}$. 
This indicates that $\lim_{x\rightarrow+\infty}x^{-\alpha}\log(x)=0$

---

## Further about Exponential Functions

Since $x^{n}=E(nL(x))$ for $x>0$ and integer $n$ and $x^{\frac{1}{m}}=E(\frac{1}{m}L(x))$
We have $$
x^{\alpha}=E(\alpha L(x))=e^{\alpha\log(x)}
$$ for rational $\alpha$.
**Differnetiation:** $(x^{\alpha})'=E(\alpha L(x))\frac{\alpha}{x}=\alpha x^{\alpha-1}$ for rational $\alpha$.

---

## Trigonometric Functions

<font color="#ff0000">Definition:</font> $$
C(x)=\frac{1}{2}[E(ix)+E(-ix)],\ S(x)=\frac{1}{2}[E(ix)-E(-ix)]
$$ We will show that $C(x)$ and $S(x)$ are essentially $\cos(x)$ and $\sin(x)$.

By definition of exponential function, we have $\overline{E(z)}=E(\overline{z})$, hence this shows that $C(x)$ and $S(x)$ are both real. 

**Very importantly**, we notice that 
$$
E(ix)=C(x)+iS(x)
$$

^f227c8

$|E(ix)|^{2}=E(ix)\overline{E(ix)}=E(ix)E(-ix)=E(0)=1$, then we have $|E(ix)|=1$. 

**Differentiation:** $C'(x)=-S(x)$, $S'(x)=C(x)$. (Easily derived from definition)

**Singular Point:** there exists positive number $x$ such that $C(x)=0$ 
	If not, then $C(x)>0$ for all $x$ (Because $C(0)>0$, and the fact that $C$ is continuous)
	Since $S'(x)=C(x)>0$, $S$ is strictly increasing. Combining the fact that $S(0)=0$, $S(x)>0$ for $x>0$. Hence if $0<x<y$, we have $S(x)(y-x)<\int_{x}^{y}S(t)dt=C(x)-C(y)\leq2$ ([[Fourier Series (Proof)#^edf180|Verify]])
	 But this cannot be true for $y$ sufficiently large, then by contradiction, the claim is proved.

Let $x_{0}$ be the smallest positive number such that $C(x_{0})=0$, and this exists because of [[003 Metric space and Function#^527004|theorem]].
We define $\pi$ by
$$
\pi=2x_{0}
$$
Then $C(\pi/2)=0$ and $S(\pi/2)=1$. (by the fact that $|E(ix)|=1$, and $S$ is increasing in $(0,\pi/2)$)

Then by [[000 A different Approach to Fourier Series#^f227c8|formula]] $E(\frac{\pi i}{2})=i$ 
This gives us $E(\pi i)=E(\frac{\pi i}{2})E(\frac{\pi i}{2})=-1$, the famous "Euler Formula" #EulerFormula 
And $E(2\pi i)=1$, which indicates the periodicty of the $E$.

Moreover:
<font color="#ff0000">Theorem:</font> 
	1. Function $E$ is periodic, with period $2\pi i$
	2. Function $C$ and $S$ are periodic with period $2\pi$
		**Proof** follows from statement 1 and the definition of $C,S$.
	1. If $0<t<2\pi$, then $E(it)\neq1$
		Proof
	4. If $z$ is a complex number with $|z|=1$, there is a unique $t$ in $[0,2\pi)$ such that $E(it)=z$
		Proof

The curve $\gamma$ defined by 
$$
\gamma(t)=E(it)\ (0\leq t\leq2\pi)
$$
is a simple, closed curve whose range is the unit circle in the plane. The arclength of $\gamma$ is 
$$
\int_{0}^{2\pi}|\gamma'(t)|dt=\int_{0}^{2\pi}|iE(it)|dt=2\pi
$$
In a similar manner, we can show that $\gamma(t)$ indeed shows that $C,S$ are geometrically identical to $\cos,\sin$. In this way, we construct the trigonometric functions without relying on geometric intuition. 

---

## Fourier Series

<font color="#ff0000">Definition:</font> (Trigonometric polynomial) 
$$
f(x)=a_{0}+\sum\limits_{n=1}^{N}(a_{n}\cos(nx)+b_{n}\sin(nx))
$$
Very importantly, it can also be written in the form
$$
f(x)=\sum\limits_{-N}^{N}c_{n}e^{inx}
$$
Definition: (trignometric series)
$$
\sum\limits_{-\infty}^{\infty}c_{n}e^{inx}
$$





