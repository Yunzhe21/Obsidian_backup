---
tags:
  - Homomorphism
  - Isomorphism
  - "#Automorphism"
  - "#InnerAutomorphism"
  - Conjugation
  - "#SymmetricGroup"
  - Endomorphism
  - "#Algebra"
---
---

## Group Homomorphism

#Homomorphism 
>[! def | *] Homomorphism
>Let $(G, \cdot)$ and $(G, \cdot)$ be groups. A map $f$: $G\rightarrow G^{'}$ is called *homomorphism* if $\forall x,\ y\in G, \ f(x\cdot y) = f(x)\cdot f(y)$.

### Two easy consequence of the definition

>[! prp | 1]
>If $f\in Hom(G, G^{'})$, then $f(e)=e'$ 

^6ae026

- [[Morphism between Groups (Proof)#^f976d1|Proof]] 

>[! prp | 2]
>If $f\in Hom(G, G')$, then $f(x^{-1})=f(x)^{-1}$ 
- [[Morphism between Groups (Proof)#^7f32eb|Proof]] 

### Important example

Q: What is $Hom(\mathbb{Z}, \mathbb{Z})$? 

A: Define map $m_{a}:\ x\longmapsto a\cdot x$, a is an integer. <font color="#ff0000">In fact</font>, $Hom(\mathbb{Z}, \mathbb{Z})=\{m_{a}:\ a\in \mathbb{Z}\}$ 
		[[Morphism between Groups (Proof)#^1e47dc|Proof]] ^HomZZ

<font color="#ff0000">Notation:</font> #Endomorphism If $G'=G,\ Hom(G, G')=End(G)$. ^End

### Property of Group Homomorphism

>[! prp | 1]
>Take $f_{1}\in Hom(G_{1}, G_{2})$ and $f_{2}\in Hom(G_{2},G_{3})$, then $f_{2}\cdot f_{1}\in Hom(G_{1}, G_{3})$. 
- [[Morphism between Groups (Proof)#^ba977e|Proof]] ^HomomorphismComposition

>[! prp |2]
>Take $f\in Hom(G,G')$, $H\leq G$ and $f^{-1}$ then
> 1. $Im(f)=f(G)\leq G'$ 
> 2.  $ker(f)\leq G$ 
- [[Morphism between Groups (Proof)#^f2c310|Proof]] 

>[! prp | 3]
>Take $Hom(G, G')$, then **a)** $f$ is injective $\iff$ $ker(f)=\{e\}$; **b)** f is surjective $\iff$ $Im(f)=G'$
- [[Morphism between Groups (Proof)#^ab512f|Proof]] ^InjuectiveAndSurjective

---

## Isomorphism 

#Isomorphism 
>[! def |*] Isomorphism
> $f\in Hom(G, G')$ is called an *isomorphism* if it's bijection.

<font color="#ff0000">Notation:</font> $Iso(G,G')=\{\text{Isomorphisms between G and G'}\}$ (often $\emptyset$)

### Property of Isomorphisms

>[! prp |1]
>If $f\in Iso(G, G')$, then $f^{-1}: G'\rightarrow G\in Iso(G',G)$ 
- [[Morphism between Groups (Proof)#^604f47|Proof]] 

<font color="#ff0000">Terminology:</font> $G$ and $G'$ are isomorphic if $Iso(G, G')\neq \emptyset$ 

<font color="#ff0000">Notation:</font> $Aut(G)=Iso(G,G)$ is called #Automorphism of $G$ ^automorphism

>[! prp |2]
>If $G$ is a group, then $(Aut(G), \cdot)\leq (\mathfrak{S}_{G}, \cdot)$ 
- [[Morphism between Groups (Proof)#^e0d463|Proof]] ^AutomorphismAndSymmetricGroup

>[! prp | 3]
> $Aut(\mathbb{Z})=\{m_{1}, m_{-1}\}$ 
- [[Morphism between Groups (Proof)#^cbc4c2|Proof]] ^AutomorphismOfZ

---

## Conjugation and inner automorphism

>[! def |*] 
>For $G$ a group and $x\in G$, define $\iota_{x}$: $y\longmapsto xyx^{-1}$, $y\in G$.

>[! prp |1]
> $\iota_{x}\in Aut(G)$ 
- [[Morphism between Groups (Proof)#^8fda91|Proof]]

#InnerAutomorphism 
>[! def |*] Inner Automorphism
>An element $\varphi \in Aut(G)$ is called an *inner automorphism* if $\exists x\in G\ s.t.\ \varphi = \iota_{x}$

^a10ff0

<font color="#ff0000">Notation:</font> $Inn(G)=\iota (G)\subseteq Aut(G)$ 
	$Inn(G) = \{\iota_{x} |\ x\in G\}$  

>[! prp | 2]
> $Inn(G)\leq Aut(G)$ 
- [[Morphism between Groups (Proof)#^72bd4e|Proof]]

### Conjugation

>[! def |*] Conjugation
>If $G$ is a group. One says that ${} y$ and ${} y'\in G$ are *conjugate* if $\exists \varphi \in Inn(G)\ s.t.\ y'=\varphi(y)$, i.e. $\exists x\in G\ s.t.\ y'=xyx^{-1}$

Next is a crucial observation:

>[! prp |*]
>The conjugate relation on $G$ is an equivalent relation
- [[Morphism between Groups (Proof)#^86b54f|Proof]]  

<font color="#ff0000">Notation:</font> $Cl_{G}(x)=\{gxg^{-1}:\ g\in G\}$

<font color="#ff0000">Important Fact:</font> These Classes form a partition of G  ^partition

---

## Important Example (Symmetric Group)

#SymmetricGroup
Recall that $\mathfrak{S}_{n}=\{\text{bijections}:\ \{1, \dots, n\}\longrightarrow \{1, \dots, n\}\}$ , and if $a_{1}, \dots, a_{r}$ are distinct elements of  $\{1, \dots, n\}$, one denote $(a_{1}, \dots, a_{r})$ the element of $\mathfrak{S}_{n}$ defined by:
	$a_{1}\rightarrow a_{2}$
	$\dots$
	$a_{r-1}\rightarrow a_{r}$
	$x\rightarrow x$ if $x\in\{1, \dots, n\}-\{a_{1}\dots a_{r}\}$ 

A permutation of this form is called a "r-cycle".

>[! prp |*]
>If $c\in\mathfrak{S}$  is a r-cycle, then $Cl_{\mathfrak{S}_{n}}(c)=\{All\ r-cycles\}$
- [[Morphism between Groups (Proof)#^269474|Proof]]

>[! cor | *] 
>If $\varphi=c_{1}\circ c_{2}\dots \circ c_{n}$, then if $\tau\in\mathfrak{S}$, $\tau\varphi\tau^{-1}=\iota_{\tau}(c_{1})\dots\iota_{\tau}(c_{n})$, and $\sigma (1, \cdots, r)\sigma^{-1}=(\sigma(1), \cdots, \sigma(r))$
- The proof is given in the above proposition.

 