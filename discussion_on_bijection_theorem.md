Can we reformulate this in some theorem about bijection or something like that?

Yes. Here is the precise statement; everything in it is a set because $\mathcal D$ is essentially small, so “equivalent to giving” becomes an honest bijection.

Setup. $\mathcal D$ an essentially small triangulated category, $\Lambda$ a finite-rank lattice with a norm on $\Lambda_{\mathbb R}$, $v\colon K_0(\mathcal D)\to\Lambda$ a fixed group homomorphism. Put $\mathbb H=\{re^{i\pi\varphi}:r>0,\ \varphi\in(0,1]\}$.

Theorem. Let

$\mathcal S_1$ be the set of pairs $(Z,\mathcal P)$ with $Z\in\operatorname{Hom}(\Lambda,\mathbb C)$, $\mathcal P$ a slicing of $\mathcal D$, such that $Z(v(E))\in\mathbb R_{>0}e^{i\pi\varphi}$ for all $0\neq E\in\mathcal P(\varphi)$, and $\inf\{|Z(v(E))|/\|v(E)\|:0\ne E\in\mathcal P(\varphi),\ \varphi\in\mathbb R\}>0$;
$\mathcal S_2$ be the set of pairs $(\mathcal A,Z)$ with $\mathcal A$ the heart of a bounded t-structure on $\mathcal D$ and $Z\in\operatorname{Hom}(\Lambda,\mathbb C)$ such that $Z(v(E))\in\mathbb H$ for $0\ne E\in\mathcal A$, every object of $\mathcal A$ has a Harder–Narasimhan filtration by $Z$-semistable objects of strictly decreasing phase, and $\inf\{|Z(v(E))|/\|v(E)\|:0\ne E\in\mathcal A\ Z\text{-semistable}\}>0$.

Then the maps


$$F(Z,\mathcal P)=\big(\mathcal P((0,1]),\,Z\big),\qquad G(\mathcal A,Z)=\big(Z,\,\mathcal P\big)\ \text{with }\mathcal P(\varphi)=\{Z\text{-semistables of phase }\varphi\text{ in }\mathcal A\}\text{ for }\varphi\in(0,1],\ \mathcal P(\varphi+n)=\mathcal P(\varphi)[n],$$

are mutually inverse bijections $\mathcal S_1\rightleftarrows\mathcal S_2$. The same statement holds with the support property deleted from both sides (Bridgeland’s Prop. 5.3, in the language of pre-stability conditions), and with “support property” replaced by “locally finite” on both sides.

Proof, in the pieces already established.

*$F$ is well defined.* $\mathcal P((0,1])$ is the heart of the bounded t-structure $(\mathcal P(>0),\mathcal P(\le1))$ (first answers). For $0\ne E\in\mathcal A$ the HN factors have phases in $(0,1]$, so $Z(E)=\sum Z(A_i)\in\mathbb H$. Each HN factor $A_i\in\mathcal P(\varphi_i)$ is $Z$-semistable in $\mathcal A$: a subobject $F\subset A_i$ in $\mathcal A$ has $Z(F)=Z(A_i)-Z(A_i/F)$ with all phases of $A_i/F$ at most $\varphi_i$... more carefully, the rotation argument applied to the HN factors of $F$ (phases $\le\varphi_i$, since $\operatorname{Hom}(\mathcal P(>\varphi_i),A_i)=0$ forces $\varphi^+(F)\le\varphi_i$) gives $\varphi(F)\le\varphi_i$. So the slicing’s HN filtration is an HN filtration in the sense of $\mathcal S_2$. The two infima coincide because $|Z|$ and $\|v\|$ are invariant under shift.

*$G$ is well defined.* Shift-compatibility holds by construction. Hom-vanishing: for $\varphi,\psi\in(0,1]$ and $E\in\mathcal P(\varphi)$, $F\in\mathcal P(\psi)$, one has $\operatorname{Hom}(E[n],F[m])=\operatorname{Ext}^{m-n}_{\mathcal D}(E,F)$, which vanishes for $m<n$ (heart), for $m=n$ and $\varphi>\psi$ (standard: the image of a map $E\to F$ would have phase $\ge\varphi>\psi\ge$ phase of any subobject of $F$), and for $m\ge n+1$ the inequality $\varphi+n>\psi+m$ is impossible. HN filtrations in $\mathcal D$: filter $E$ by truncations with factors $H^i(E)[-i]$, finitely many by boundedness, then refine each by its HN filtration in $\mathcal A$; the resulting phases are strictly decreasing. Compatibility of $Z$ and the support property are immediate.

*$G\circ F=\mathrm{id}$.* Need: for $\varphi\in(0,1]$, the $Z$-semistables of phase $\varphi$ in $\mathcal P((0,1])$ are exactly $\mathcal P(\varphi)$. “$\supset$” was shown above. “$\subset$”: if $E\in\mathcal A$ is $Z$-semistable of phase $\varphi$ with top HN factor $A_1\in\mathcal P(\varphi_1)$, then $A_1\subset E$ in $\mathcal A$ gives $\varphi_1\le\varphi$ by semistability, while $Z(E)=\sum Z(A_i)$ with all phases $\le\varphi_1$ gives $\varphi\le\varphi_1$ with equality only if all $\varphi_i=\varphi_1$. Hence $E\in\mathcal P(\varphi)$.

*$F\circ G=\mathrm{id}$.* Need: $\mathcal P((0,1])=\mathcal A$ for $\mathcal P=G(\mathcal A,Z)$. “$\subset$” because $\mathcal A$ is extension-closed in $\mathcal D$ and generated... rather, every object of $\mathcal P((0,1])$ is an iterated extension of objects of $\mathcal A$, hence in $\mathcal A$; “$\supset$” by the HN filtration in $\mathcal A$. $\square$

Two refinements worth recording.

Equivariance. Both sides carry actions of $\operatorname{Aut}(\mathcal D)$ (acting on $\mathcal A$ or $\mathcal P$ and on $Z$ through $K_0$) and of $\widetilde{GL}^+_2(\mathbb R)$ on the right; on $\mathcal S_2$ only the subgroup $\mathbb C$ acts visibly, and $F,G$ are equivariant for it (the full $\widetilde{GL}^+_2$ action changes the heart by tilting, which is invisible on the $(\mathcal A,Z)$ side; this is one reason the slicing description is preferable globally).
Fibres over hearts. Composing with $(\mathcal A,Z)\mapsto\mathcal A$ gives a map $\operatorname{Stab}_\Lambda(\mathcal D)\to\{\text{bounded hearts}\}$ whose fibre over $\mathcal A$ is the set of $Z\in\operatorname{Hom}(\Lambda,\mathbb C)$ with $Z(\mathcal A\setminus0)\subset\mathbb H$, the HN property, and the support property. When $\mathcal A$ has finite length with finitely many simples $S_1,\dots,S_n$, the HN property is automatic and this fibre is the open set $\{Z:Z(S_i)\in\mathbb H\ \forall i\}\cong\mathbb H^n$, which is how one builds charts on $\operatorname{Stab}(\mathcal D)$ for quivers and for local Calabi–Yau threefolds. So the theorem is also the first step toward the manifold structure, not only a reformulation.

Can we use t-structures instead of their hearts A in theorem?

Yes, and nothing changes except the bookkeeping, because for bounded t-structures the heart determines the t-structure and vice versa.

Lemma (Bridgeland, Lemma 3.2). The maps


$$(\mathcal D^{\le0},\mathcal D^{\ge0})\ \longmapsto\ \mathcal A=\mathcal D^{\le0}\cap\mathcal D^{\ge0},\qquad \mathcal A\ \longmapsto\ \big(\langle\mathcal A[n]:n\ge0\rangle,\ \langle\mathcal A[n]:n\le0\rangle\big)$$

are mutually inverse bijections between bounded t-structures on $\mathcal D$ and full additive subcategories $\mathcal A\subset\mathcal D$ (closed under isomorphism) such that

$\operatorname{Hom}(\mathcal A,\mathcal A[n])=0$ for $n<0$;
every object of $\mathcal D$ is a finite iterated extension of objects of the form $A[n]$, $A\in\mathcal A$, $n\in\mathbb Z$.

Here $\langle\ \rangle$ denotes extension closure.

Proof sketch. Given a bounded t-structure with heart $\mathcal A$, condition 1 is orthogonality ($\mathcal A\subset\mathcal D^{\le0}$, $\mathcal A[n]\subset\mathcal D^{\ge1}$ for $n<0$), and condition 2 is the filtration of $E$ by truncations with factors $H^i(E)[-i]$, finite by boundedness; moreover $\mathcal D^{\le0}=\langle\mathcal A[n]:n\ge0\rangle$ because $\mathcal D^{\le0}$ is extension-closed and contains the $\mathcal A[n]$, $n\ge0$, while conversely every $E\in\mathcal D^{\le0}$ has $H^i(E)=0$ for $i>0$ and is filtered by $H^i(E)[-i]$ with $-i\ge0$. Same for $\mathcal D^{\ge0}$. So the composite “t-structure $\to$ heart $\to$ t-structure” is the identity. Conversely, given $\mathcal A$ with 1 and 2, set $\mathcal D^{\le0},\mathcal D^{\ge0}$ as above; shift-stability is clear, orthogonality follows from 1 by dévissage, and the truncation triangle for $E$ is obtained by taking a filtration as in 2, reordering it so that the shifts decrease (possible by 1, using the same argument as for HN filtrations with $\mathbb Z$ in place of $\mathbb R$), and cutting between $n\ge0$ and $n<0$; the heart is then $\mathcal A$ again, since an object of $\langle\mathcal A[n]:n\ge0\rangle\cap\langle\mathcal A[n]:n\le0\rangle$ has a $\mathbb Z$-HN filtration whose phases are both $\ge0$ and $\le0$. $\square$

Note that boundedness is essential: $(\mathcal D,0)$ and $(0,\mathcal D)$ are distinct t-structures with the same heart $0$, and on $\mathcal D(\mathrm{Mod}\,R)$ there are many unbounded t-structures with heart $0$ or with hearts that do not generate.

The theorem with t-structures. Replace $\mathcal S_2$ by


$$\mathcal S_2'=\Big\{\big((\mathcal D^{\le0},\mathcal D^{\ge0}),Z\big):\ \text{bounded t-structure},\ Z\in\operatorname{Hom}(\Lambda,\mathbb C),\ Z(v(E))\in\mathbb H\text{ for }0\ne E\in\mathcal D^{\le0}\cap\mathcal D^{\ge0},\ \text{HN and support on the heart}\Big\}.$$

The Lemma gives a bijection $\mathcal S_2'\to\mathcal S_2$, $(t,Z)\mapsto(\operatorname{heart}(t),Z)$, and composing with $F,G$ from the previous theorem gives mutually inverse bijections


$$\mathcal S_1\ \rightleftarrows\ \mathcal S_2',\qquad (Z,\mathcal P)\mapsto\big((\mathcal P(>0),\mathcal P(\le1)),Z\big),$$

with inverse sending $(t,Z)$ to the slicing whose $\mathcal P(\varphi)$, $\varphi\in(0,1]$, are the $Z$-semistables of phase $\varphi$ in the heart of $t$. One can of course cut at any $\varphi_0$ instead of $0$: $(\mathcal P(>\varphi_0),\mathcal P(\le\varphi_0+1))$ with $Z$ replaced by $e^{-i\pi\varphi_0}Z$, which is the $\mathbb C$-action on $\operatorname{Stab}(\mathcal D)$ seen on the t-structure side.

Going further: slicings as families of t-structures. Pushing this to its conclusion, a slicing is the same thing as a family of bounded t-structures $t_\varphi=(\mathcal D_\varphi^{\le0},\mathcal D_\varphi^{\ge0})$, $\varphi\in\mathbb R$, such that

$\mathcal D^{\le0}_{\varphi+1}=\mathcal D^{\le0}_\varphi[1]$ (and hence for $\mathcal D^{\ge0}$);
$\mathcal D^{\le0}_\varphi\subset\mathcal D^{\le0}_\psi$ for $\psi\le\varphi$;
for every $E$, the function $\varphi\mapsto\tau_\varphi^{\le0}E$ (the aisle truncation) changes value at only finitely many $\varphi$.

Given a slicing, $t_\varphi=(\mathcal P(>\varphi),\mathcal P(\le\varphi+1))$; given such a family, $\mathcal P(\varphi)=\big(\bigcap_{\psi<\varphi}\mathcal D^{\le0}_\psi\big)\cap\mathcal D^{\ge1}_\varphi$, and the finiteness condition is exactly the existence of finite HN filtrations, with the jump points of $\varphi\mapsto\tau^{\le0}_\varphi E$ being the HN phases. This is the “t-stability” viewpoint of Gorodentsev–Kuleshov–Rudakov and it is what makes the first answer’s slogan precise: a stability condition is a bounded t-structure for every real number, varying in a locally finite way, together with a central charge that singles out the phases.

No: in direction (B) there is no second notion of semistability to compare. $\mathcal P(\varphi)$ was defined as the set of $Z$-semistable objects of $\mathcal A$ of phase $\varphi$ (shifted), so “an object of $\mathcal D$ is $\mathcal P$-semistable iff it is a shift of a $Z$-semistable object of $\mathcal A$” is true by definition and proves nothing. The equivalence of the two notions is a theorem only in direction (A), where $\mathcal P$ is given first and $\mathcal A=\mathcal P((0,1])$ is derived from it.

What B5 has to supply is different in kind: Definition 5.5(3) demands a filtration for every object $E\in\mathcal D$, while the hypothesis only speaks about objects of $\mathcal A$. An object such as $E=M\oplus N[1]$ with $M,N\in\mathcal A$, or a non-split extension $N[1]\to E\to M$... more generally any $E$ with two nonzero cohomology objects, is not in $\mathcal A$, not in any $\mathcal A[n]$, and nothing in the hypotheses mentions it. The only link between such an $E$ and $\mathcal A$ is the t-structure: $E$ is built from the $H^i_{\mathcal A}(E)[-i]$ by the truncation triangles. So one must (i) take that filtration, (ii) refine each factor by the HN filtration of $H^i_{\mathcal A}(E)$ in $\mathcal A$, shifted, and (iii) observe that the phases come out strictly decreasing. There is no semistability statement that could replace (i)–(iii), because the issue is existence of a filtration, not the nature of its factors.

Two remarks that may make B5 feel less ad hoc.

The refinement lemma is a completely formal fact — “an extension of filtered objects is filtered” — and it has nothing to do with stability. If you prefer, quote it as standard (it is used silently in Bridgeland’s paper, in the proof that $\mathcal P((0,1])$ is a heart and in Prop. 5.3), and keep only step (iii), which is the one line $\psi-i>-i\ge1-i'\ge\psi'-i'$.
Why the phases do not interleave, so no reordering is ever needed. All factors coming from $H^i_{\mathcal A}(E)[-i]$ have phases in $(-i,1-i]$, and these intervals for different $i$ are disjoint and decrease with $i$. That is exactly what the restriction “phases in $(0,1]$” on the abelian side buys: the HN structure on $\mathcal D$ is the concatenation of the $\mathbb Z$-indexed HN structure given by the t-structure (factors $H^i[-i]$, phases “$\approx -i$”) and the $(0,1]$-indexed one given by $Z$ inside each $H^i$. Had one allowed phases in an interval of length $>1$ on the abelian side, the shifted factors would interleave and one would need Hom-vanishing to reorder them — and Hom-vanishing would fail.

So the honest summary of (B) is: axioms (1) and (2) and Definition 5.8(1),(2) are definitional or Schur-type one-liners, and axiom (3) is the formal propagation of HN filtrations from the heart to $\mathcal D$ through the bounded t-structure. If you like, we can now do (C), where the forward semistability equivalence from (A) and the recovery $\mathcal P((0,1])=\mathcal A$ are combined to show the two maps are inverse.
