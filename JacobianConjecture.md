**[Back to Table of Contents](README.md)**

# Analyzing the Jacobian Conjecture Through the Lens of Universal Objects as Optimization.

In July 2026, a counterexample to the Jacobian Conjecture was discovered by Levent Alpöge and Claude Fable 5. In this article, we analyze this topic within the framework developed in [(12) Universal Objects as Optimization ](./Thin-Categories-12.md)—namely, the thinning (metric/order evaluation) of thick categories into thin categories, as well as the search for optimal solutions and universal objects.

---

## 1. Setup: The Original Category $\mathcal{C}$ and Localization $\mathcal{C}[W^{-1}]$

Let $\mathcal{C}$ be the category whose objects are complex affine spaces $\mathbb{C}^n$ and whose morphisms are polynomial maps between them.

In this category $\mathcal{C}$, we define $W$ as the class of genuine isomorphisms, consisting of polynomial automorphisms that possess global inverse maps. The object that universally realizes this class $W$ as isomorphisms is the **localization $\mathcal{C}[W^{-1}]$**. The localization functor $Q: \mathcal{C} \to \mathcal{C}[W^{-1}]$ satisfies the following universal property:

> **Universal Property**  
> If any functor $F: \mathcal{C} \to \mathcal{D}$ maps all morphisms in $W$ to isomorphisms, then there exists a unique functor $G: \mathcal{C}[W^{-1}] \to \mathcal{D}$ such that $F$ factors through $Q$ (i.e., $F = G \circ Q$).

In short, $\mathcal{C}[W^{-1}]$ represents the universal object that completely preserves the true global structure (invertibility).

---

## 2. Localization via the Thinning Functor $T'$ (Numerical Reduction and Conversion to Extremum Problems)

Following the context of [(12) Universal Objects as Optimization ](./Thin-Categories-12.md), we construct a **thinning functor $T'$** that projects the complex algebraic and geometric structure of the category $\mathcal{C}$ into the realm of evaluation values (metric and order).

For the Jacobian determinant $\det J_f$ of a polynomial map $f: \mathbb{C}^n \to \mathbb{C}^n$, the multiplicative functoriality of composition ($\det J_{f \circ g} = \det J_f \cdot \det J_g$) must align with an additive distance structure. To achieve this, we define the indicator $T(f)$ as the **logarithmic Jacobian**:

$$ T(f) = \log |\det J_f| $$

This preserves an additive monoidal metric structure under composition, yielding $T(f \circ g) = T(f) + T(g)$.

### Reinterpreting the Keller Condition as a First-Order Extremum Condition
The **Keller condition** in the Jacobian Conjecture (stating that $\det J_f$ is a non-zero constant $c \in \mathbb{C}^\times$ over the entire space) can be rephrased via the spatial gradient of the indicator:

$$ \nabla T(f) = \nabla (\log |\det J_f|) = 0 \quad (\text{zero gradient across the entire space}) $$

In variational calculus and optimization theory, this is precisely the first-order extremum condition signifying that the local variation energy is in a completely flat/stationary state.

Accordingly, we assign the metric distance (variational quantity) $d_{T(f_1)T(f_2)}$ between indicators based on whether they satisfy this extremum condition:

$$
d_{T(f_1)T(f_2)} = 
\begin{cases} 
0 & (\text{when } \nabla T(f_1) = \nabla T(f_2) = 0 \text{; i.e., both } T(f_1) \text{ and } T(f_2) \text{ are constants}) \\ 
\infty & (\text{otherwise}) 
\end{cases}
$$

Thus, the thinning functor $T'$ is formulated as:

$$ T': \mathcal{C} \to \mathcal{C}\left(\mathrm{Ob}(\mathcal{C}), \{\ge_{T(i)T(j)}\}\right) $$

---

## 3. Categorical Reformulation of the Jacobian Conjecture

Under this framework, the Jacobian Conjecture can be rephrased as follows:

> **Question (Agreement of Criteria / Pullback)**  
> When morphisms satisfying the extremum condition in the target category (polynomial having non-zero Jacobian) under the thinning functor $T'$ are pulled back to the original category $\mathcal{C}$, does this set coincide with the class of genuine isomorphisms $W$?  
> 
> In other words, through the localization functor $Q: \mathcal{C} \to \mathcal{C}[W^{-1}]$, does the criterion for being an isomorphism in $\mathcal{C}[W^{-1}]$ completely coincide with the criterion for candidate extrema in the target category under $T': \mathcal{C} \to \mathcal{C}\left(\mathrm{Ob}(\mathcal{C}), \{\ge_{T(i)T(j)}\}\right)$ where the distance between indicators is $0$?

If this were always true, the local extremum evaluation via the thinning functor $T'$ would function as a "noise-free universal filter" capable of flawlessly extracting the true global structure $W$ of the original category.

---

## 4. Interpretation of the Counterexample

The counterexample discovered by Alpöge and AI. (a 3-variable polynomial map with $\det J_f \equiv -2$) satisfies the local extremum condition in the thin category. However, when pulled back to the original category $\mathcal{C}$, it lacks global injectivity and thus fails to belong to $W$.

---

## 5. Analogy to the Incompleteness of the Method of Lagrange Multipliers and Remarks

This phenomenon shares the exact same logical structure as the **method of Lagrange multipliers** in mathematical analysis.

When setting $L = f - \lambda g$ in Lagrange multipliers, the first-order condition $\nabla L = 0$ (zero gradient) is merely a **necessary condition** for $f$ to have an extremum under the constraint $g = 0$. It cannot determine whether the identified candidate point is a genuine extremum (local maximum/minimum) or a false candidate such as a saddle point.

Similarly, my remark on the discovery by Alpöge and AI is that the Keller condition— "$\det J_f$ is a non-zero constant, i.e., $\nabla T(f) = 0$" —was merely a first-order necessary condition indicating local flatness, rather than something that guarantees global invertibility (belonging to $W$).

Ultimately, this discovery serves as a concrete demonstration that **a thinning functor is, in general, not omnipotent.**




