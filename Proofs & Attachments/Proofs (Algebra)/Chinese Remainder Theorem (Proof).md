
Consider $f: x\in\mathbb{Z}\longmapsto (\overline{x}^{a}, \overline{x}^{b})\in \frac{\mathbb{Z}}{a\mathbb{Z}}\times\frac{\mathbb{Z}}{b\mathbb{Z}}$, then $f\in Hom(\mathbb{Z}, \frac{\mathbb{Z}}{a\mathbb{Z}}\times\frac{\mathbb{Z}}{b\mathbb{Z}})$ 
$x\in ker(f)\iff \overline{x}^{a}=\overline{0}^{a}$ and $\overline{x}^{b}=\overline{0}^{b} \iff$ $a|x$ and $b|x\iff ab|x\iff x\in ab\mathbb{Z}$ 
By [[005 First Isomorphism Theorem#^FirstIsomorphismThm|First Isomorphism Theorem]], $\overline{f}: \frac{\mathbb{Z}}{abZ}\rightarrow \frac{\mathbb{Z}}{aZ}\times\frac{\mathbb{Z}}{bZ}$ is injective.
Also, since $|\frac{\mathbb{Z}}{abZ}|=ab=|\frac{\mathbb{Z}}{aZ}|\times|\frac{\mathbb{Z}}{bZ}|$, then it is also surjective. Hence $\frac{\mathbb{Z}}{ab\mathbb{Z}}\sim \frac{\mathbb{Z}}{a\mathbb{Z}}\times \frac{\mathbb{Z}}{b\mathbb{Z}}$. ^4b767d

---

We prove by induction, for $n=1$, then it's obvious that any subgroup of $\mathbb{Z}$ is finitely generated.
Suppose that for $n-1$, the statement is true, then for $n$, 
Let $K$ be such a subgroup, then denote $K_{1}$ as the first components of $K$. Clearly, $K_{1}$ is a subgroup of $\mathbb{Z}$, then $K_{1}=m\mathbb{Z}$ for some $m\in\mathbb{Z}$. Write  $(k_{1}, \cdots, k_{n})=k(m, a_{2}, \cdots, a_{n})+(0, k_{2}-a_{2}, \cdots, k_{n}-a_{n})$. Since $(k_{2}-a_{2}, \cdots, k_{n}-a_{n})\in\mathbb{Z}^{n-1}$, then by induction it is finitely generated. Thus $K$ is finitely generated. ^5f1331

---

Call the absolute value of the non-zero element the size of that element. Call the upper left entry the pivot. We prove inductively that $A$ can be reduced to $$
\begin{pmatrix}
  d& 0\\
  0& \textbf{B}
\end{pmatrix}
$$ where $d$ divides every entry of $\textbf{B}$. First, note that the row and column operation is similar to that in Linear algebra except that we only multiply the row by $-1$. 
We first use interchanging operation in both row and column operation to **move the least size element**to the pivot. 
**Step 1:** Repeatly adding and subtracting the element in the first row and column with the pivot, reducing them to either $0$ or smaller in size than the pivot. At some point, the first column and row all have size zero except for the the pivot. 
**Step 2:** If the pivot point does not divide every element of $\textbf{B}$, say it doesn't divide element at index $(2,2)$, then add the second row to the first row, imitate step one to make every element in the first row $0$ except for the pivot and the $(1,2)$ element. Apply Euclidean Algorithmn to the $(1,2)$ element and the pivot until we obtain one **less than the pivot**, we pick that as the new pivot, then it must divide the $(1,2)$ element.
Although through this step, we change the pivot itself, but notice that the new pivot is smaller than before, since the pivot cannot be infinitely reduced, eventually we will arrive at a stage where the final pivot divides all other elements in $\textbf{B}$. ^345d52

---

Since $A$ is finitely generated group, then $A=\{a_{1}^{k_{1}}\dots a_{s}^{k_{s}}: k_{1}\in \mathbb{Z}\}$ for some $a_{1}, \cdots, a_{s}$. Define the map $\phi\in Hom(\mathbb{Z}^{s}, A)$ as $\phi(k_{1}, \cdots, k_{s})=a_{1}^{k_{1}}\cdots a_{s}^{k_{s}}$, notice that it is a surjective homomorphism. We call $I$ the kernel of $\phi$, then by [[005 First Isomorphism Theorem#^FirstIsomorphismThm|First Isomorphism Theorem]], $A\sim\frac{\mathbb{Z}^{s}}{I}$. Then it is technical to prove that $I$ can be chose as the form $\{0\}^{m}\times d_{1}\mathbb{Z}\times\cdots\times d_{r}\mathbb{Z}$, where $s=m+r$ and $d_{i}\mid d_{i+1}$. 
$I$ is the subgroup of $\mathbb{Z}^{s}$, then by previous [[Chinese Remainder Theorem (Proof)#^5f1331|proposition]], $I$ is finitely generated. Let $I_{1}, \cdots, I_{m}$ be generators of $I$, and denote $(i_{k1}, \cdots, i_{ks})$ the components of each $I_{k}$. Set $A$ be the matrix where the $k$ -th row is $I_{k}$, then from previous proposition, we can reduce it to Smith Normal Form, which gives us the proof. ^6a7cf2

---


