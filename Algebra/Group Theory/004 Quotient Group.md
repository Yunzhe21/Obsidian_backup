---
tags:
  - LeftCoset
  - RightCoset
  - LagrangeTheorem
  - "#QuotientGroup"
  - "#Algebra"
---
---

## Equivalent Relation

#EquivalentClasses
>[! def |*] Equivalent Classes
>Let $\sim$ be a equivalent relation on $\mathbb{X}$, $x\in \mathbb{X}$, define $Cl_{\mathbb{X}}(x)\coloneqq \{y\in \mathbb{X}: y\sim x\}$ 

<font color="#ff0000">Notation:</font> $\frac{\mathbb{X}}{\sim}=\{\text{equivalent classes}\}$ i.e. $\varphi \in \frac{\mathbb{X}}{\sim}\iff \exists x\in \mathbb{X}\ s.t.\ \varphi = Cl_{\mathbb{X}}(x)$ 

>[! def |*] System of Representation
>If for each $\varphi \in \frac{\mathbb{X}}{\sim}$, one picks $x_{\varphi}\in \varphi$. Then $R=\{x_{\varphi}:\varphi \in \frac{\mathbb{X}}{\sim}\subseteq \mathbb{X}\}$ is called a *system of representatives* of $\frac{\mathbb{X}}{\sim}$.

### Properties of system of represtentation:

Let $R\subseteq \mathbb{X}$ be the set of representation of $\frac{\mathbb{X}}{\sim}$
	1. The map $x\in R\longmapsto Cl_{\mathbb{X}}(x)\in\frac{\mathbb{X}}{\sim}$ is a bijection.
	2. $\mathbb{X}=\bigcup_{x\in R}Cl_{X}(x)$ 

---

## Fundamental equivalent relations in Group Theory

>[! def |*]
>Let $H\leq G$, one writes
>- $x\sim_{H} y$ if $\exists h\in H\ s.t.\ y=xh$ 
>- $x\prescript{}{H}{\sim} y$ if $\exists h\in H\ s.t.\ y=hx$ 

<font color="#ff0000">Fact:</font> Both of them are equivalent relationship.

<font color="#ff0000">Notation: </font>
- #LeftCoset $Cl_{\sim_{H}}(x)$ is denoted as $xH$
- #RightCoset $Cl_{\prescript{}{H}{\sim}}(x)$ is denoted as $Hx$ ^leftcosetRightcoset

Define map i: $x\longmapsto x^{-1}$, Note that $i^{-1}=i$
- Map i is bijective.
	- Simple.
- Note that $i(x)H=i(Hx)$ and $Hi(x)=i(xH)$.
	- $i(x)H = x^{-1}H = (H^{-1}x)^{-1} = (Hx)^{-1} i(Hx)$.
 
>[! prp |*]
>The map $\alpha:Hx\longmapsto i(x)H$ is well defined and bijective, with inverse map $\beta:\ xH\longmapsto Hi(x)$
- [[Quotient Group (Proof)#^8ef97a|Proof]] 

>[! lem |*]
>For any $x\in G$, the map $l_{x}$: $h\in H\ \longmapsto xh$ and map $r_{x}:\ h\in H\longmapsto hx$ are bijective.
- [[Quotient Group (Proof)#^bfbe4a|Proof]] 

#LagrangeTheorem 
>[! thm |*] Lagrange Theorem
>If $G$ is a *finite* group and and $H\leq G$, then $|H|\bigr ||G|$. In fact, $|G|=|\frac{G}{\sim_{H}}|\times |H|=|\frac{G}{\prescript{H}{}{\sim}}|\times |H|$. 

^870bfb

- [[Quotient Group (Proof)#^68f1ad|Proof]] 

---

## Quotient Groups

>[! lem |*]
>If $H\leq G$, then $H\lhd G$ $\iff$ $\forall x\in G,\ xHx^{-1}=H$ 
- [[Quotient Group (Proof)#^18e936|Proof]] 

<font color="#ff0000">Consequence:</font> If $H\lhd G$, then $xH=Hx$, i.e. $\frac{G}{\sim_{H}}=\frac{G}{\prescript{}{H}{\sim}}$.

<font color="#ff0000">Notation:</font>  #QuotientGroup
	If $H\lhd G$, then $\frac{G}{H}=\frac{G}{\sim_{H}}=\frac{G}{\prescript{}{H}{\sim}}$ 
	For $x\in G$, $\overline{x}^{H}=\overline{x}\coloneqq xH=Hx$ 

>[! lem |*]
>If $H\lhd G$, then the map $m: \frac{G}{H} \times \frac{G}{H}\longrightarrow \frac{G}{H}$ as $(\overline{x}, \overline{y})\longmapsto \overline{xy}$ is well defined.
- [[Quotient Group (Proof)#^854c43|Proof]]
- This is the motivation for an operation for quotient group. 

<font color="#ff0000">Notation:</font> If $H\lhd G$, then $\overline{x} \cdot \overline{y}=m(\overline{x}, \overline{y})=\overline{xy}$.

>[! thm |*] Quotient group is a group
>If $H\lhd G$, then $(\frac{G}{H}, \cdot)$ is a group with $\overline{e}=eH=He$.

>[! prp | *]
>If $H\lhd G$, the canonical projection $p:\ x\longmapsto \overline{x}$ is a group homomorphism. 
- Proof is obvious after we define the operation on quotient group.

<font color="#ff0000">Property of p:</font> p is surjective with $ker(p)=H$

---

<font color="#ff0000">Example:</font> $\mathbb{Z}$ is commutative, then its subgroups are normal in $\mathbb{Z}$, in fact, they are $m\mathbb{Z}$.
	If $m=0$, then $m\mathbb{Z}=\{0\}$, and $\frac{\mathbb{Z}}{0\mathbb{Z}}\sim \mathbb{Z}$ 
	If $m\neq 0$, then ${} \frac{\mathbb{Z}}{m\mathbb{Z}}=\{\bar{0}, \dots, \overline{m-1}\} {}$ and $|\frac{\mathbb{Z}}{m\mathbb{Z}}|=m$
	[[Quotient Group (Proof)#^eaaeda|Proof]]

<font color="#ff0000">Classification of cyclic group (up to isomorphism)</font>

Suppose that $G=\langle x\rangle=\{x^{k}|k\in \mathbb{Z}\}$, then
$\varphi_{x}$: $k\in \mathbb{Z}\longrightarrow x^{k}\in \langle x\rangle$ is a homomorphism from $\mathbb{Z}$ to $\langle x\rangle$.
Then since $ker(\varphi_{x})\lhd \mathbb{Z}$, $ker(\varphi_{x})=m\mathbb{Z}$ for a unique $m$
Conclusion: $G\sim \frac{\mathbb{Z}}{m\mathbb{Z}}$









