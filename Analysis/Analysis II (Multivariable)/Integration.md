---
tags:
---
---

Notation: The $n$ - dimensional measure of a set $A$ is denoted by $V_{n}(A)$. If the dimension $n$ is clear from the context, we write simply "measure" rather than $n$ - dimensional measure and $V(A)$ rather than $V_{n}(A)$. The integral of $f$ over $A$ is denoted by $\int_{A}fdV_{n}$ or $\int_{A}f(\textbf{x})dV_{n}(\textbf{x})$.

For rigorous explanation on Lebesgue integral, we refer to Stein Real Analysis. Here, we discuss effective procedure in evaluating multivariable integrals.

## Iterated integrals

One method for evaluating multi-variable integral is by writing the integral as an iterated integral and applying the fundamental theorem of calculus.

Let $1\leq s< n$. In most cases we shall take $s=1$ or $x=n-1$. Write $\textbf{x}=(\textbf{x}',\textbf{x}'')$, where ${} \textbf{x}'=(x^{1}, \cdots, x^{s})\in E^{s} {}$ and $\textbf{x}''=(x^{s+1}, \cdots, x^{n})\in E^{n-s}$. 

Let $A$ be a set and $f$ be a function whose domain contains $A$. We assume at present that $A$ is compact and $f$ is continuous on $A$. We show that $\int_{A}fdV$ can be expressed as an iterated integral.

First, for fixed $\textbf{x}'$, integrate over a set $A(\textbf{x}')\subseteq E^{n-s}$. Then integrate the result of the first integration over a set $R\subseteq E^{s}$, where $R=\{\textbf{x}':A(\textbf{x}')\text{ is not empty}\}$, we can understand $R$ as the projection of $A$ onto $E^{s}$.

>[! thm |*] 
>Let $f$ be continuous on a compact set $A$. Then $\int_{A}f(\textbf{x})dV_{n}(\textbf{x})=\int_{\mathbb{R}}\left \{\int_{A(\textbf{x}')}f(\textbf{x}',\textbf{x}'')dV_{n-s}(\textbf{x}'')\right\}dV_{s}(\textbf{x}')$.
>
