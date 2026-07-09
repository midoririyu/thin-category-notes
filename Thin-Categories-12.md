**[Back to Table of Contents](README.md)**

# Thin Categories (12)  
Reducing the Problem of Finding Universal Objects in General Categories to Optimization Problems in (Enriched Monoidal) Thin Categories

Following Example 5 in "Thin Categories (1)", consider the thin category $\mathcal{C}([0,\infty], \geq)$ whose objects are the non-negative real numbers together with $\infty$, and whose morphisms are given by the usual order $\geq$ (with the convention that $\infty \geq r$ and $\infty \geq \infty$ for any non-negative real $r$).

## Thinning Functor via Distance

Now consider a functor $T$ from a locally small category $\mathcal{C}$ to the thin category $\mathcal{C}([0,\infty], \geq)$. For each pair of objects $i,j \in Ob(\mathcal{C})$, there is a uniquely determined evaluation value (distance) $d_{T(i)T(j)} \in [0,\infty]$ associated with the morphism $T(i) \geq T(j)$, satisfying the following conditions:

1. $d_{T(i)T(j)} < \infty$ (when $Hom_{\mathcal{C}}(i,j) \neq \emptyset$)
2. $d_{T(i)T(j)} = \infty$ (when $Hom_{\mathcal{C}}(i,j) = \emptyset$)
3. $d_{T(i)T(i)} = 0$
4. For composition of morphisms in $\mathcal{C}$, $d_{T(i)T(j)} + d_{T(j)T(k)} \geq d_{T(i)T(k)}$ holds.

In particular, when $\mathcal{C}$ is a small category ($Ob(\mathcal{C})$ is a set), the thin category $\mathcal{C}(Ob(\mathcal{C}),｛\geq_{T(i)T(j)}｝(i,j \in Ob(\mathcal{C})))$ constructed via this functor $T$ carries the structure of a Lawvere generalized metric space.

Furthermore, define a functor
$T' : \mathcal{C} \to \mathcal{C}(Ob(\mathcal{C}),｛\geq_{T(i)T(j)}｝(i,j \in Ob(\mathcal{C})))$
that acts as the identity on objects and sends each morphism to the corresponding (distance-valued) relation. That $T'$ is a functor follows from Proposition 3-1 in "Thin Categories (3)". Since $T'$ is surjective on objects, it is essentially surjective as a functor. By the propositions on universal objects in "Thin Categories (3)", universal objects (initial objects, terminal objects, etc.) in $\mathcal{C}$ remain universal after being mapped by $T'$.

(Note that $T'$ encodes the existence or non-existence of morphisms in $\mathcal{C}$ via whether the corresponding distance is finite or infinite.)

Finding universal objects in a thin category reduces to finding upper or lower bounds in an ordered set — that is, finding objects that realize the maximum or minimum distance. Thus, abstract universality problems in a general category $\mathcal{C}$ can be translated into optimization problems in a metric space.

---

This discussion can be carried out analogously for $\mathcal{C}([0,\infty], \leq)$. In this case, condition 4 is replaced by
$4'. \quad d_{T(i)T(j)} \wedge d_{T(j)T(k)} \leq d_{T(i)T(k)}$
(where $\wedge$ denotes the minimum). In either case, the problem reduces to finding shortest paths, maximum flows, or maximum capacities.

## Probabilistic Version

As a variant of the above, consider a functor $T$ from a locally small category $\mathcal{C}$ to the thin category $\mathcal{C}([0,1], \geq)$. For each pair of objects $i,j \in Ob(\mathcal{C})$, let $p_{T(i)T(j)} \in [0,1]$ be the evaluation value (probability) associated with the morphism $T(i) \geq T(j)$. This is assumed to satisfy:

1. $p_{T(i)T(j)} > 0$ (when $Hom_{\mathcal{C}}(i,j) \neq \emptyset$)
2. $p_{T(i)T(j)} = 0$ (when $Hom_{\mathcal{C}}(i,j) = \emptyset$)
3. $p_{T(i)T(i)} = 1$
4. For composition of morphisms in $\mathcal{C}$, $p_{T(i)T(j)} \cdot p_{T(j)T(k)} \leq p_{T(i)T(k)}$ holds (where $\cdot$ is ordinary multiplication).

One can define the thin category $\mathcal{C}(Ob(\mathcal{C}),｛\geq_{T(i)T(j)}｝(i,j \in Ob(\mathcal{C})))$ under this setting and consider extremal problems (maxima and minima) within it. This corresponds to extremal problems in a probabilistic category, such as maximizing or minimizing reliability or sustainability in communication systems or other structures.

---

The method above only provides **candidates** for universal objects, since even if $T'(i)$ is universal in $T'(\mathcal{C})$, $i$ need not be universal in $\mathcal{C}$. Nevertheless, with a good choice of $T'$, the approach can be practically useful.

Whether it is Lagrange multipliers or the computation of homology, these are historical achievements of human ingenuity in constructing a suitable $T'$.

Humans — and AI as well — generally cannot handle thick categories directly. Ultimately, we must map them to manageable thin categories before performing computations.
