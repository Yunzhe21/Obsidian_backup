---
tags:
  - "#solvable"
  - ButterflyLemma
---
---

# Solvable Group

> [!def | ] Tower
> Let $G$ be a group, the sequence of subgroups $G = G_{0}\supset G_{1}\supset \cdots \supset G_{m}$ is a tower of subgroups.
> 
- The tower is normal if each $G_{i+1}$ is normal in $G_{i}$. 
- It's called abelian/cyclic if it's normal tower and each factor group $G_{i} / G_{i+1}$ is abelian/cyclic

> [! def | ] refinement
> A refinement of a tower $G = G_{0}\supset G_{1}\supset \cdots \supset G_{m}$ is a tower which can be obtained by inserting a finite number of subgroups in the given tower.

#solvable
> [! def |] solvable
> A group is said to be solvable if it has an abelian tower whose last element is the trivial subgroup.

> [! prp | ]
> Let $G$ be a finite group. An abelian tower of $G$ admits a cyclic refinement. Let $G$ be a finite solvable group. Then $G$ admits a cyclic tower, whose last element is $\{e\}$.
- [[Solvability (Proof)#^828192|Proof]]

> [! thm |] 
> Let $G$ be a group and $H$ a normal subgroup. Then $G$ is solvable if and only if  $H$ and $G / H$ are solvable.
- [[Solvability (Proof)#^8a5d14|Proof]]

#ButterflyLemma
> [!lem |] Butterfly Lemma
> Let $U, V$ be subgroups of a group, and let $u, v$ be normal subgroups respectively, then $u(U\cap v)$ is normal in $u(U\cap V)$, and $(u\cap V)v$ is normal in $(U\cap V)v$. Moreover, $\frac{u(U\cap V)}{u(U\cap v)}\sim \frac{U\cap V}{(U\cap v)(V\cap u)}\sim\frac{v(U\cap V)}{v(u\cap V)}$ 
```tikz
\usepackage{tikz}
\usetikzlibrary{positioning}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
	\begin{tikzpicture}[scale=1, every node/.style={draw, circle, inner sep=2pt, fill=black},
    label distance=2mm]
    	% Nodes
		\node[label=above:$U$] (U) at (0,4) {};
		\node[label=above:$V$] (V) at (4,4) {};
		\node[label=left:$u(U \cap V)$] (uUV) at (0,3.5) {};
		\node[label=right:$(U \cap V)v$] (UVv) at (4,3.5) {};
		\node[label=above:$U \cap V$] (UV) at (2,3) {};
		\node[label=left:$u(U \cap v)$] (uUv) at (0,2) {};
		\node[label=right:$(u \cap V)v$] (uVv) at (4,2) {};
		\node[label=below:$u$] (u) at (-1,1) {};
		\node[label=below:$v$] (v) at (5,1) {};
		\node[label=below:$u \cap V$] (uV) at (0,0) {};
		\node[label=below:$U \cap v$] (Uv) at (4,0) {};
		\node (mid) at (2, 1) {};
		
		\draw (u) -- (uUv);
		\draw (u) -- (uV);
		\draw (v) -- (uVv);
		\draw (v) -- (Uv);
		\draw (U) -- (uUV);
		\draw (V) -- (UVv);
		\draw (uUV) -- (uUv);
		\draw (uUV) -- (UV);
		\draw (UVv) -- (uVv);
		\draw (UVv) -- (UV);
		\draw (mid) -- (uUv);
		\draw (mid) -- (uVv);
		\draw (mid) --(UV);
		\draw (mid) -- (uV);
		\draw (mid) -- (Uv);
	\end{tikzpicture}
\end{document}
```
- 

> [!def |] equivalent tower
> Let $G = G_{1}\supset G_{2}\supset\cdots\supset G_{r}=\{e\}$, and $G = H_{1}\supset H_{2}\supset\cdots\supset H_{s} = \{e\}$ be normal towers of subgroups. We say these towers are equivalent if there exists a permutation of the indices $i = 1, \cdots, r-1$ to $i'$ such that $G_{i} / G_{i+1}\sim H_{i'} / H_{i'+1}$.

> [! thm] 
> Let $G$ be a group. Two normal towers of subgroups ending with the trivial group have equivalent refinements.
- [[Solvability (Proof)#^d057e0|Proof]]

---

# More on Solvable Group

> [!thm |] 
> If $n\geq 5$, then $S_{n}$ is not solvable.
- [[Solvability (Proof)#^17e40b|Proof]]

> [! thm ] 
> Let $G$ be a finite $p$ - group. Then $G$ is solvable. If its order $>1$, then $G$ has a non-trivial center.
- [[Solvability (Proof)#^cabe9e|Proof]]

> [! cor ] 
> 






















