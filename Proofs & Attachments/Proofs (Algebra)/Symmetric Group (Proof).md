
Write $c_{1}=(a_{1}, \cdots, a_{r})$ and $c_{2}=(b_{1}, \cdots, b_{s})$ with respective support $S_{1},S_{2}$. By our assumption $S_{1}\cap S_{2}=\emptyset$. Let's consider three cases:
If $i$ is neither in $S_{1}$ or $S_{2}$, then $c_{1}\circ c_{2}(i)=i=c_{2}\circ c_{1}(i)$.
If $i$ is in $S_{1}$ not in $S_{2}$, then $c_{1}\circ c_{2}(i)=c_{1}(i)=c_{2}\circ c_{1}(i)$.
If $i$ is in $S_{2}$ not in $S_{1}$, the proof is identical. ^7f8f9c

---

Consider $\sigma\in\mathfrak(S)_{n}$, then ${} G:=\langle\sigma\rangle\leq\mathfrak{S}_{n} {}$. Notice that $G$ acts on $\{1, 2, \cdots, n\}$ by natural action $G\times \{1, \cdots. n\}\to \{1, \cdots, n\}:(g,i)\mapsto g(i)$. Hence $\{1, \cdots, n\}=\bigcup_{k=1}^{s}G.i_{k}$. Further, we write it as $\bigcup_{k=1}^{r}G.i_{k}\bigcup_{k=r+1}^{s}G.i_{k}$, where whenever $k\leq r$, $|G.i_{k}|=l_{k}\geq 2$. 
**Claim:** $G.i_{k}=\{i_{k}, \sigma(i_{k}), \cdots. \sigma^{l_{k}-1}(i_{k})\}$. Since $LHS\subseteq RHS$ is obvious, it is sufficient to prove $\left|\{i_{k}, \sigma(i_{k}), \cdots, \sigma^{l_{k}-1}(i_{k})\}\right |=l_{k}$. Suppose that there exists $0\leq l<l'\leq l_{k}-1$ such that $\sigma^{l}(i_{k})=\sigma^{l'}(i_{k})$, then $\sigma^{j}(i_{k})=:\sigma^{l'-l}(i_{k})=i_{k}$ for some ${} 1\leq j< l_{k}-1 {}$. Note that $l=qj+r$ with $r\in \{0, 1, \cdots, j-1\}$, then $\sigma^{l}(i_{k})=\sigma^{r}\circ(\sigma^{j}\circ\cdots\circ\sigma^{j})(i_{k})$, hence we would have $G.i_{k}\subseteq\{i_{k}, \cdots, \sigma^{j-1}(i_{k})\}$, then $|G.i_{k}|\leq j<l_{k}$, which is absurd.
Also, we **claim** that $\sigma^{l_{k}}(i_{k})=i_{k}$, if not, then $\sigma^{l_{k}}(i_{k})=\sigma^{l}(i_{k})$ for $1\leq l<l_{k}$, which implies that $\sigma^{j}(i_{k})=: \sigma^{l_{k}-l}(i_{k})=i_{k}$ with $0<j<l_{k}$, this is absurd.
Now, given these two claims, $\sigma=(i_{1}, \cdots, \sigma^{l_{1}-1}(i_{1}))\circ\cdots\circ(i_{r}, \cdots, \sigma^{l_{r}-1}(i_{r}))$, the verification is trivial.
Now, we sketch the proof of uniqueness of the decomposition. If ${} \sigma=c_{1}'\circ\cdots, c_{r'}' {}$ is another decomposition satisfying the condition. First check that $G.a_{i}=\text{Supp}(c_{i}')$ for $a_{i}\in \text{Supp}(c_{i}')$, and $G.x=\{x\}$ otherwise. Since the decomposition of $\{1, \cdots, n\}$ into $G$ -orbits is unique, $r=r'$ and $\text{Supp}(c_{i})=\text{Supp}(c_{i}')$. Finally because $\sigma$ decomposes over both families of cycles and by disjointness of the supports, it is easily seen that for any fixed $a_{i}\in \text{Supp}(c_{i})$, $c_{i}=c_{i}'$. ^114349

---

Following [[002 Morphism between Groups#^1444ff|Corollary]], we get $\sigma \circ (a_{1,1}, \cdots, a_{1,l_{1}})\circ\cdots\circ(a_{d,1}, \cdots, a_{d,l_{d}})\circ\sigma^{-1}=(\sigma(a_{1,1}), \cdots, \sigma(a_{1,l_{1}}))\circ\cdots\circ(\sigma(a_{d,1}), \cdots, \sigma(a_{d,l_{d}}))$        ^121b5a

---

$\epsilon(\sigma)=\prod\limits_{1\leq i<j\leq n}\frac{\sigma(j)-\sigma(i)}{|\sigma(j)-\sigma(i)|}=\frac{\prod\limits_{1\leq i<j\leq n}\sigma(j)-\sigma(i)}{\prod\limits_{1\leq i<j\leq n}|\sigma(j)-\sigma(i)|}$.
But $\prod\limits_{1\leq i<j\leq n}|\sigma(j)-\sigma(i)|=\prod\limits_{1\leq i>j\leq n}|\sigma(j)-\sigma(i)|$, hence $\prod\limits_{1\leq i\neq j\leq n}|\sigma(j)-\sigma(i)|=\left ( \prod\limits_{1\leq i<j\leq n}|\sigma(j)-\sigma(i)| \right)^{2}$, or in other words, 
$\prod\limits_{1\leq i<j\leq n}|\sigma(j)-\sigma(i)|=\left( \prod\limits_{1\leq\neq j\leq n} |\sigma(j)-\sigma(i)|\right)^{2}$. Finally, by bijectivity of $\sigma$: $\prod\limits_{1\leq i\neq j\leq n}|\sigma(j)-\sigma(i)|=\prod\limits_{1\leq k\neq l\leq n}|l-k|=\prod\limits_{1\leq i\neq j\leq n}|j-i|=\left(\prod\limits_{1\leq i<j\leq n}|j-i|\right)^{2}$, so 
$\left(\prod\limits_{1\leq i\neq j\leq n}|\sigma(j)-\sigma(i)|\right)^{\frac{1}{2}}=\prod\limits_{1\leq i<j\leq n}|j-i|=\prod\limits_{1\leq i<j\leq n}j-i$. We thus arrive, as requested, at the conclusion. ^cd0a05

---

Take $\sigma_{1},\sigma_{2}\in\mathfrak{S}_{n}$, and set $I_{1}=\text{Inv}(\sigma_{1}), J_{1}=I_{1}^{c}, I_{2}=\text{Inv}(\sigma_{2}), J_{2}=I_{2}^{c}$ 
Observe that $(i,j)\in\text{Inv}(\sigma_{1}\circ\sigma_{2})$ if and only if $\sigma_{1}(\sigma_{2}(i))>\sigma_{1}(\sigma_{2}(j))$, and in other word in one of the two disjoint cases: $(i,j)\in I_{2}$ and $(\sigma_{2}(j),\sigma_{2}(i))\in J_{1}$; $(i,j)\in J_{2}$ and $(\sigma_{2}(i), \sigma_{2}(j))\in I_{1}$.
In particular, $l(\sigma_{1}\circ\sigma_{2})=|(i,j)\in I_{2}, (\sigma_{2}(j), \sigma_{2}(i))\in J_{1}|+|(i,j)\in J_{2}, (\sigma_{2}(i), \sigma_{2}(j))\in I_{1}|$. However, $|(i,j)\in I_{2}, (\sigma_{2}(j), \sigma_{2}(i))\in J_{1}|+|(i,j)\in I_{2}, (\sigma_{2}(j), \sigma_{2}(i))\in I_{1}|=l(\sigma_{2})$, and $|(i,j)\in J_{2}, (\sigma_{2}(i),\sigma_{2}(j))\in I_{1}|+|(j,i)\in I_{2}, (\sigma_{2}(i), \sigma_{2}(j))\in I_{1}|=l(\sigma_{1})$.
From this we deduce: $l(\sigma_{1})+l(\sigma_{2})=l(\sigma_{1}\circ\sigma_{2})+2|(i,j)\in I_{2}, (\sigma_{2}(j),\sigma_{2}(i))\in I_{1}|$. Hence $(-1)^{l(\sigma_{1})}\times (-1)^{l(\sigma_{2})}=(-1)^{l(\sigma_{1})+l(\sigma_{2})}=(-1)^{l(\sigma_{1}\circ\sigma_{2})+\text{even integer}}=(-1)^{l(\sigma_{1}\circ\sigma_{2})}$, which is exactly $\epsilon(\sigma_{1})\epsilon(\sigma_{2})=\epsilon(\sigma_{1}\circ\sigma_{2})$. 
To prove surjectivity, just observe that $\text{Inv}(1\ 2)=\{(1, 2)\}$ nonempty. ^ae1553

---

If $\tau$ is a transposition, then it is conjugate to $(1\ 2)$ by some $\sigma\in\mathfrak{S}_{n}$, which means that $\tau=\sigma\circ (1\ 2)\circ\sigma^{-1}$, hence $\epsilon(\tau)=\epsilon(\sigma)\epsilon(1\ 2)\epsilon(\sigma)^{-1}=\epsilon(1\ 2)=-1$. Then if $c$ is a $r$ -cycle, then write $c=(a_{1}\ a_{2})\circ\cdots\circ(a_{r-1}\ a_{r})$, hence $\epsilon(c)=\epsilon(a_{1}\ a_{2})\cdots\epsilon(a_{r-1}\ a_{r})=(-1)^{r-1}$.  ^14be5a

---

By the [[005 First Isomorphism Theorem#^82b689|First Isomorphism Theorem]]: $\frac{|\mathfrak{S}_{n}|}{|\text{ker}(\epsilon)|}=|\text{Im}(\epsilon)|$, then $|\text{ker}(\epsilon)|=\frac{n!}{2}$. ^796b28

---

For $\sigma\in A_{n}$, write $\sigma=\iota_{1}\circ\cdots\circ\iota_{r}$, where $\iota_{i}$ are transposes. But since $1=\epsilon(\iota)=(-1)^{n}$, $n$ is even. If $n=0$, $\sigma=Id$. Otherwise, $\sigma=(\iota_{1}\circ\iota_{2})\cdots(\iota_{r-1}\circ\iota_{r})$. 
To prove $A_{n}\leq\langle 3-cycle\rangle$, it's sufficient to prove that if $(a,b)$ and $(c,d)\in\mathfrak{S}_{n}$, then $(a,b)\circ(c,d)\in\langle 3-cycle\rangle$. There are three cases to consider:
Firstly, $(a,b)=(c,d)$, then $(a,b)\circ(c,d)=Id\in\langle 3-cycle\rangle$.
Secondly, Suppose $|\text{Supp}(a,b)\cap\text{Supp}(c,d)|=1$, we can assume $b=c$, then $(a,b)(b,d)=(a,b,d)\in\langle 3-cycle\rangle$
Thridly, suppose $\{a,b\}\cap\{c,d\}=\emptyset$, then $(a,b)\circ(c,d)=(a,b)\circ(b,c)\circ(b,c)\circ(c,d)=(a,b,c)(b,c,d)\in\langle 3-cycle\rangle$.
Conversely, any $3-cycle$ has sign $1$, then $\langle 3-cycle\rangle\leq A_{n}$. ^9fa67b

---

Pick $(a,b,c)$ and $(d,e,f)\in A_{n}$. There exists $\sigma\in\mathfrak{S}_{n}$ such that ${} \sigma(a,b,c)\sigma^{-1}=(\sigma(a),\sigma(b),\sigma(c))=(d,e,f) {}$. 
If $\sigma\in A_{n}$, then there is nothing to prove. 
Otherwise, $\epsilon(\sigma)=-1$. Because $n\geq 5$, there exists $g\neq h\in\{1, \cdots, n\}$ such that $\{a,b,c\}\cap\{g,h\}=\emptyset$. Then we put $\sigma'=\sigma\circ\iota$, where $\tau = (g, h)$, we can see that  $\epsilon(\sigma')=\epsilon(\sigma)\epsilon(\iota)=1$. Notice that $\sigma'$ has the same affect as $\sigma$.  ^d41c8a

---

Take $\sigma_{1}, \sigma_{2}\in\mathfrak{S}_{n}$, $[\sigma_{1}, \sigma_{2}]=\sigma_{1}\sigma_{2}\sigma_{1}^{-1}\sigma_{2}^{-1}$, notice $\epsilon(\sigma_{1}\sigma_{2}\sigma_{1}^{-1}\sigma_{2}^{-1})=\epsilon(\sigma_{1})\epsilon(\sigma_{2})\epsilon(\sigma_{1})^{-1}\epsilon(\sigma_{2})^{-1}=1$, then $[\sigma_{1}, \sigma_{2}]\in A_{n}$, thus $[\mathfrak{S}_{n}, \mathfrak{S}_{n}]\leq A_{n}$. Conversely, for any $3-cycle$ $(a,b,c)$, $(a,b,c)=(a,b)(a,c)(a,b)^{-1}(a,c)^{-1}=[(a,b), (a,c)]\in [\mathfrak{S}_{n}, \mathfrak{S}_{n}]$, then $A_{n}\leq [\mathfrak{S}_{n}, \mathfrak{S}_{n}]$. Thus $A_{n}=[\mathfrak{S}_{n}, \mathfrak{S}_{n}]$ for $n\geq 2$.
Following the same argument above, we have $[A_{n}, A_{n}]\leq A_{n}$. Conversely for $n\geq 5$, we know that $[A_{n}, A_{n}]\lhd A_{n}$, and it contains a $3-cycle$, then $A_{n}=[A_{n}, A_{n}]$ for $n\geq 5$. ^31f993

---

$A_{n}$ is simple trivially for ${} n\leq 3 {}$. When $n=4$, we have subgroup $1, (1 2)(3 4), (1 3)(2 4), (1 4)(2 3)$ that is a normal subgroup in $A_{n}$.
Now suppose $n\geq 5$, let $H\lhd A_{n}$ and $H\neq\{1\}$, it is sufficient to show it contains a $3-cycle$. But it is obvious since $A_{n}$ is itself generated by $3-cycles$. ^2062e4

---

