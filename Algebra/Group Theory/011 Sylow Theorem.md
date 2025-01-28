---
tags:
  - SylowP-Group
  - SylowTheorem
  - "#p-adic"
  - "#Algebra"
---
---

## Theorem 

Let $G$ be a finite group and $p\in\mathcal{P}$. Suppose that $|G|=p^{m}a$ for $m\in\mathbb{N}$ and $a\in\mathbb{N}-\{0\}$ such that $\text{gcd}(a,p)=1$, in other word, $p^{m}$ is the largest power of $p$ dividing $|G|$. Now we ca define the so-called Sylow $p$ - subgroup. ^34367b

#SylowP-Group 
>[! def |*] Sylow $p$ - subgroup
>One say that $S\leq G$ is a sylow $p$ - subgroup of $G$ if $|S|=p^{m}$.

We now state the **Sylow Theorems** first without proving.
#SylowTheorem
>[! thm | 1] Sylow First Theorem
>Let $G$ be a finite group, and let $p$ be a prime number such that $p^m$ is the largest number dividing $|G|$. Then there exists at least one Sylow $p$ - subgroup.

^e2ac95 z

- This theorem guarantees the existance of a Sylow subgroup for a finite group $G$.

#SylowTheorem
>[! thm | 2] Sylow Second Theorem
>Any $p$ - subgroup (subgroup of a $p$ - group) is contained in a Sylow $p$ - subgroups of $G$, and all Sylow $p$ - subgroups of $G$ are conjugate.

^8f99bb


>[! cor | *] 
>A Sylow $p$ - subgroup of $G$ is normal in $G$ if and only if it is the unique Sylow $p$ - subgroup of $G$.

#SylowTheorem 
>[! thm | 3] Sylow Third Theorem
>The number $n_{p}$ (the number of Sylow $p$ - subgroup of $G$) of $G$ is congruent to $1\text{ mod }p$, and it divides $a$.

^145814

---

## Motivation

Recall [[004 Quotient Group#^870bfb|Lagrange Theorem]], which states that any subgroup of a finite group divides the order of the original group. Now, we want to ask whether **the reverse** is true, i.e. given a number that divides the order of a finite group, can we find such a subgroup?

The answer is unfortunely **NO**. However, if we restrict ourself to the power of prime numbers, we see that the [[011 Sylow Theorem#^e2ac95|Sylow First Theorem]] guaratees such an existence.

Since we've already known the existence of Sylow $p$ - subgroup for arbitrary finite group, we want to investigate what they really look like, and then [[011 Sylow Theorem#^8f99bb|Sylow Second Theorem]] tells is that all Sylows subgroups are conjugate and in fact, by conjugating, we can create all Sylow $p$ - subgroups.

The implication of [[011 Sylow Theorem#^145814|Sylow Third Theorem]] is relatively clear, which states the "size" of the set of all Sylow $p$ - subgroups.
 
---

## Proof of the First Theorem

#p-adic
>[! def |*] $p$ - adic valuation
>Fix $p\in\mathcal{P}$ and for $x\in\mathbb{Z}-\{0\}$, we denote $v_{p}(x)\in\mathbb{N}$ the unique natural number such that $x=p^{v_{p}(x)}u$, $u\in\mathbb{Z}$, $\text{gcd}(p,u)=\pm 1$. This defines a map $v_{p}:\mathbb{Z}-\{0\}\to\mathbb{N}$ called the $p$ - adic valuation.

Let $r=\frac{a}{b}\in\mathbb{Q}^{\times}$, with both $a$ and $b$ in $\mathbb{Z}-\{0\}$. Set ${} v_{p}(r)=v_{p}(a)-v_{p}(b)\in\mathbb{Z} {}$, and we can easily see that $v_{p}(r)$ is well-defined.

Thus we can extend the domain from $\mathbb{Z}-\{0\}$ to $\mathbb{Q}^{\times}$.

Now, we can state the basic property of $p$ - adic valuation without proof (the proof is easy).

>[! prp | 1]
> $\forall x,y\in\mathbb{Q}^{\times}$: $v_{p}(xy)=v_{p}(x)+v_{p}(y)$ and $v_{p}(x/y)=v_{p}(x)-v_{p}(y)$.


>[! prp | 2]
>If $x$ and $u$ both in $\mathbb{Z}-\{0\}$ are such that $v_{p}(x)>0$ and $v_{p}(u)=0$, then $v_{p}(x+u)=0$
- [[Sylow Theorem (Proof)#^0f4e05|Proof]]

>[! prp | 3]
>Prove that for $m\in\mathbb{N}$ and $a\in\mathbb{N}-\{0\}$:
> $$
\begin{pmatrix}
 p^{m}a\\
p^{m}
\end{pmatrix}=a\prod\limits_{j=1}^{p^{m}-1}\frac{p^{m-v_{p}(j)}a-\frac{j}{p^{v_{p}(j)}}}{p^{m-v_{p}(j)}-\frac{j}{p^{v_{p}(j)}}}$$
and deduce from the equality $$
v_{p}(\begin{pmatrix}
 p^{m}a\\
p^{m}
\end{pmatrix})=v_{p}(a) $$

^e49971

- [[Sylow Theorem (Proof)#^108ef1|Proof]]

**By the following sequence of lemmas, we will finish the proof.**

Write $|G|=p^{m}a$. Denote by $\mathfrak{U}$ the set of subsets of $G$ with cardinality $p^{m}$, which means $\mathfrak{U}=\{U\subset G, |U|=p^{m}\}$. ^552997


>[! lem | 1]
>For $U\in\mathfrak{U}$ and $g\in G$, set $gU=\{gu, u\in U\}$. Prove that $gU\in\mathfrak{U}$.
- [[Sylow Theorem (Proof)#^974644|Proof]]


>[! lem | 2]
>The map $G\times\mathfrak{U}\to\mathfrak{U}$ as $(g,U)\mapsto gU$ defines an action of $G$ on $\mathfrak{U}$.

^ce63c3

- [[Sylow Theorem (Proof)#^715c78|Proof]]

>[! lem | 3]
>If $U\in\mathfrak{U}$, then $|\text{Stab}_{G}(U)|\leq p^{m}$.

^77c63e

- [[Sylow Theorem (Proof)#^88c75f|Proof]]

>[! lem | 4]
> $|\text{Stab}_{G}(U)|=p^{m}$ if and only if $v_{p}(|\text{Stab}_{G}(U)|)=m$.
- [[Sylow Theorem (Proof)#^f73276|Proof]]

>[! lem | 5]
> $v_{p}(|\text{Stab}_{G}(U)|)=m$ if and only if the orbit $G.U$ of $U$ satisifies $v_{p}(|G.U|)=v_{p}(a)$.
- [[Sylow Theorem (Proof)#^329ba3|Proof]]

>[! lem | 6]
> $v_{p}(|\mathfrak{U}|)=v_{p}(a)$.

^950761

- [[Sylow Theorem (Proof)#^c2f6ac|Proof]]

>[! thm |*] 
>There exists at least one $U\in\mathfrak{U}$ such that $|\text{Stab}_{G}(U)|=p^{m}$.

^36a44a

- [[Sylow Theorem (Proof)#^0ce704|Proof]]

Check [[Sylow Theorems.canvas|Sylow Theorems]] canvas for an intuitive overview. Notice that lemma 4 and 5 are necessary but not crucial, so we exclude it from the canvas.

---

## Proof of the Second Theorem

Notation: $G$ is a finite group, $p\in\mathscr{P}$, and $|G| = p^{m}a$ where $\gcd(a, p) = 0$. Because of the previous Theorem, we obtain that $\textbf{S} = \{S\leq G: |S| = p^{m}\}$ is not empty, fix $S_{0}\in\textbf{S}$. Denote $n_{p} = |\textbf{S}|$ be the number of Sylow subgroup in $G$.

> [!lemma | 1]
> Let $H\leq G$ be a $p$ - subgroup, then the map $H\times \frac{G}{S_{0}}\to G/S_{0}$ as ${} (h, gS_{0})\mapsto hgS_{0} {}$ is indeed a group action on $G / S_{0}$.
- [[Sylow Theorem (Proof)#^910022|Proof]]

> [! lemma |2]
> $gS_{0}\in (G / S_{0})^{H}\iff H\leq gS_{0}g^{-1}$, where $(G / S_{0})^{H} = \{gS_{0}: hgS_{0} = gS_{0}, \forall h \}$.
- [[Sylow Theorem (Proof)#^cce8e7|Proof]]

> [!lemma |3]
> There exists $g\in G$ such that $H\leq gS_{0}g^{-1}$.
- [[Sylow Theorem (Proof)#^051d22|Proof]]

> [! thm| *] Sylow Second Theorem
> All Sylow $p$ -subgroups are conjugate to each other.
- This is straight forward once we set $H$ in Lemma 3 to a Sylow $p$ -group $S_{1}$, and realizing they have the same cardinality.

> [! cor | *]
> A Sylow $p$ - subgroup is normal in $G$ if and only if it is the only Sylow $p$ - subgroup in $G$.
- Proof is trivial

---

## Proof of the Third Theorem

> [! lem |1] 
> The map $G\times \textbf{S}\to \textbf{S}$ as ${} (g, S)\mapsto gSg^{-1} {}$ is a group action.
- Routine work, we just omit it.


> [! lem |2]
> $n_{p}$ divides $|G|$.
- [[Sylow Theorem (Proof)#^d8e193|Proof]]

> [! lem | 3]
> Restrict in the first variable the above action to $S_{0}\leq G$, then $\textbf{S}^{S_{0}} = \{S_{0}\}$.
- It is equivalent to say that if $S$ is a $p$ - Sylow subgroup such that $\forall s_{0}\in S_{0}$: $s_{0}Ss_{0}^{-1} = S$, then we must have $S = S_{0}$.
- [[Sylow Theorem (Proof)#^066a65|Proof]]

> [! thm |*] Sylow Third Theorem
> Deduce from this that $n_{p}\equiv 1\mod p$, and that $n_{p}$ divides $a$.
- [[Sylow Theorem (Proof)#^850a4a|Proof]]











