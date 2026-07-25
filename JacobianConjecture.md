**[Back to Table of Contents](README.md)**

In this document, we analyze the Jacobian Conjecture—for which a counterexample was discovered in July 2026 by Levent Alpöge and Claude Fable 5—within the framework of "thinning" enriched categories, as discussed in  **[Thin-Categories-12](Thin-Categories-12.md
)**.

---

## 1. Setup: The Original Category $\mathcal{C}$ and Universal Properties of Isomorphisms

Let $\mathcal{C}$ be the category whose objects are affine spaces $\mathbb{C}^n$ (composed of complex vectors) and whose morphisms are polynomial maps between them.

In this category, we define the class of polynomial automorphisms—polynomial maps having a global inverse—as the class of isomorphisms $W$.

To characterize this class $W$ categorically, we consider the localization $\mathcal{C}[W^{-1}]$. The localization functor

$Q: \mathcal{C} \to \mathcal{C}[W^{-1}]$

satisfies the following universal property:

> **Universal Property** > The localization functor $Q: \mathcal{C} \to \mathcal{C}[W^{-1}]$ satisfies two key conditions:
> 1. It maps all morphisms in $W$ to isomorphisms.
> 2. **Universality:** For any category $\mathcal{D}$ and any functor $F: \mathcal{C} \to \mathcal{D}$ that maps all morphisms in $W$ to isomorphisms, there exists a unique functor $G: \mathcal{C}[W^{-1}] \to \mathcal{D}$ such that  $F = G \circ Q.$

In other words, $\mathcal{C}[W^{-1}]$ serves as the most universal object that forcibly realizes all morphisms in $W$ as genuine isomorphisms in $\mathcal{C}$.

---

## 2. Localization (Numerical Reduction) via the Thinning Functor $T$'

We define the thinning functor $T$' as an operation that strips away topological and algebraic-geometric information (such as global bijectivity) of a polynomial map $f$, projecting it down to local linear information given by differentiation—specifically, the Jacobian determinant $\det J_f$.

Specifically, we fix the condition that $\det J_f$ is a non-zero constant across the entire space ($c \in \mathbb{C}^\times$), known as the **Keller condition**, as our target condition in the thin category.

---

## 3. Categorical Reformulation of the Jacobian Conjecture

Let $W$ be the class of globally invertible polynomial maps, and $K$ be the class of morphisms satisfying the Keller condition ($\det J_f \in \mathbb{C}^\times$).

From the chain rule of differentiation and the multiplicative property of determinants, $W \subseteq K$ always holds. Therefore, the Jacobian Conjecture can be reformulated in categorical terms as follows:

> **Question** > Does $K \subseteq W$ hold? (That is, is $K = W$?)

If this were always true, the thinning functor $T$' would act as a "universal filter" preserving global structure entirely, functioning as a projection onto the universal object $\mathcal{C}[W^{-1}]$.

---

## 4. Conclusion by Alpöge and AI: Demonstrating the Limits of the Thinning Functor $T$'

The discovery in July 2026 by Levent Alpöge and Claude Fable 5 provided a negative answer to this question. The polynomial map $f$ in 3 variables with degree around 7 that they found exhibits the following properties:

1. **Behavior in the Thin Category (The World of $T$'):** $\det J_f \equiv -2$ (a non-zero constant). It fully satisfies the Keller condition and is locally perfectly invertible.
2. **Behavior in the Original Category $\mathcal{C}$:** Three distinct input points collide at the same output point (non-injective). Thus, it lacks an inverse morphism and does not belong to $W$.
3. **Behavior in the Localization $\mathcal{C}[W^{-1}]$:** While its image under $T$' appears isomorphic, the absence of an inverse morphism in $\mathcal{C}$ means it cannot be regarded as a true isomorphism even after localization.

---

## 5. Conclusion: The Presence of "Noise (False Optimal Solutions)" in Thinning

This counterexample demonstrates that because the thinning functor $T$' fails to capture global topological information, a structural gap is introduced—allowing spurious isomorphisms ("noise" pretending to be universal objects) to pollute the thinned domain.

Even with the universal framework of localization $\mathcal{C}[W^{-1}]$, the thinning functor $T$' alone cannot eliminate this noise. Consequently, the breakdown of the Jacobian Conjecture serves as a concrete instance of the principle outlined in **[Thin-Categories-12](Thin-Categories-12.md
)**.: **one cannot generally reconstruct global structures (universal isomorphism) directly from local representations (thinning).**




