**[Back to Table of Contents](README.md)**

# Thin Categories (13)  
Kan Extensions with Thin Categories as Targets

We would like to consider Kan extensions with thin categories as targets, without assuming cocompleteness of the category (i.e., the existence of all (locally small) colimits).

## Definition of Upper Bounds (in General Categories)

We first recall the definition of an upper bound in a general category.

For a subclass $B$ of the objects of a locally small category $\mathcal{C}$, an object $a \in Ob(\mathcal{C})$ is said to satisfy the following two conditions:

1. **Upper bound property**: For every $b \in B$, there exists a morphism $b \to a$.
2. **Least upper bound property**: If there exists an object $a' \in Ob(\mathcal{C})$ such that $b \to a'$ for every $b \in B$, then there exists a morphism $a \to a'$.

When such an $a$ exists, it is called the **supremum** (or **upper bound**) of $B$, and is denoted by $\sup B$ or $\bigvee B$.

When $B$ is empty, condition 1 is vacuously true, and every object is an upper bound of the empty set. Thus, by condition 2, if there exists an object that receives a morphism from every object (i.e., an **initial object** $0$ or $\bot$), then it serves as $\sup B$.

Although the supremum is not necessarily unique as an object, if $a_1$ and $a_2$ are both suprema, then by condition 2 there exist morphisms $a_1 \to a_2$ and $a_2 \to a_1$, so $a_1$ and $a_2$ are isomorphic. It immediately follows that if $\mathcal{C}$ is skeletal, the supremum is unique.

**Proposition**  
Let $F$ be a functor between locally small categories $\mathcal{C}$ and $\mathcal{D}$, and suppose that $\sup B$ and $\sup F(B)$ exist for a subclass $B \subseteq Ob(\mathcal{C})$. Then there exists a morphism $\sup F(B) \to F(\sup B)$.

**Proof**  
By the upper bound property, for every $b \in B$ there is a morphism $b \to \sup B$. By functoriality of $F$, there is a morphism $F(b) \to F(\sup B)$. By the least upper bound property of $\sup F(B)$, there exists a morphism $\sup F(B) \to F(\sup B)$. (Proof complete)

When $\mathcal{C}$ is thin, the existence condition for morphisms automatically strengthens to uniqueness.

## Left Kan Extensions in Thin Categories

**Proposition**  
Let $\mathcal{C}$ be a thin locally small category. For functors $K: \mathcal{A} \to \mathcal{X}$ and $F: \mathcal{A} \to \mathcal{C}$, define the subclass $B_x$ ($x \in \mathcal{X}$) of $Ob(\mathcal{C})$ by
$B_x = ｛ F(a) \mid a \in \mathcal{A} \text{ and there exists a morphism } K(a) \to x ｝.$
If $\sup B_x$ exists, choose one such supremum and denote it by $Sup_K F(x)$. (Note that in this notes, we work under the assumption that we can make choices of elements from classes.)

Then the functor $Sup_K F : \mathcal{X} \to \mathcal{C}$ defined in this way is a left Kan extension $Lan_K F$ of $F$ along $K$. Conversely, any left Kan extension $Lan_K F$ is isomorphic (objectwise) to $Sup_K F$. If $\sup B_x$ does not exist for some $x \in \mathcal{X}$, then the left Kan extension of $F$ along $K$ does not exist (it fails).

**Proof**

First, we recall the general definition of a left Kan extension in an arbitrary category. A functor $L = Lan_K F: \mathcal{X} \to \mathcal{C}$ together with a natural transformation $\eta: F \Rightarrow L \circ K$ is a **left Kan extension** of $F$ along $K$ if, for any functor $M: \mathcal{X} \to \mathcal{C}$ and any natural transformation $\alpha: F \Rightarrow M \circ K$, there exists a unique natural transformation $\bar{\alpha}: L \Rightarrow M$ such that the following diagram commutes for every morphism $f$ in $\mathcal{A}$:

$(M \circ K)(f) \circ \alpha = \bar{\alpha} \circ \eta \quad \text{(i.e., } \bar{\alpha} \circ F(f) = M(K(f)) \circ \alpha\text{)}.$

Since $\mathcal{C}$ is thin, as discussed in Thin Categories (3), if there exists a family of morphisms $\{T(a) \to T'(a)\}_{a \in \mathrm{Ob}(\mathcal{A})}$ between two functors $T, T': \mathcal{A} \to \mathcal{C}$, then there is **at most one** natural transformation from $T$ to $T'$, and its components are exactly these morphisms. Commutativity of the naturality squares holds automatically. Therefore, the definition of a left Kan extension when $\mathcal{C}$ is thin can be simplified as follows:

A functor $L = Lan_K F: \mathcal{X} \to \mathcal{C}$ is a left Kan extension of $F$ along $K$ if it satisfies the following two conditions:

1. For every $a \in \mathcal{A}$, there exists a morphism $F(a) \to L(K(a))$ in $\mathcal{C}$.
2. For any functor $M: \mathcal{X} \to \mathcal{C}$, if for every $a \in \mathcal{A}$ there exists a morphism $F(a) \to M(K(a))$, then for every $x \in \mathcal{X}$ there exists a morphism $L(x) \to M(x)$.

We now prove that $Sup_K F$ satisfies the above definition.

**1. $Sup_K F$ is a well-defined functor $\mathcal{X} \to \mathcal{C}$.**

Let $x \to y$ be a morphism in $\mathcal{X}$. We must show that there exists a morphism $Sup_K F(x) \to Sup_K F(y)$.

Take any $F(a) \in B_x$. By definition, there is a morphism $K(a) \to x$. Composing with $x \to y$ gives $K(a) \to y$, so $F(a) \in B_y$. Thus $B_x \subseteq B_y$.

Since $Sup_K F(y) \cong \sup B_y$ is an upper bound of $B_y$, there exists a morphism $F(a) \to Sup_K F(y)$ for every $F(a) \in B_x$. Hence $Sup_K F(y)$ is an upper bound of $B_x$.

Because $Sup_K F(x) \cong \sup B_x$ is the *least* upper bound, there exists a morphism $Sup_K F(x) \to Sup_K F(y)$. By Proposition 3-1, the existence of these morphisms automatically guarantees functoriality (preservation of composition and identities). Therefore, $Sup_K F: \mathcal{X} \to \mathcal{C}$ is a functor.

**2. Existence of the unit $\eta: F \Rightarrow Sup_K F \circ K$.**

For any $a \in \mathcal{A}$, set $x = K(a)$. Then the identity morphism $K(a) \to K(a)$ shows that $F(a) \in B_{K(a)}$. Since $Sup_K F(K(a))$ is an upper bound of $B_{K(a)}$, there exists a morphism $F(a) \to Sup_K F(K(a))$. This defines the components of $\eta$.

**3. Universal property.**

Let $M: \mathcal{X} \to \mathcal{C}$ be any functor and $\alpha: F \Rightarrow M \circ K$ any natural transformation (i.e., for every $a$ there is a morphism $F(a) \to M(K(a))$). We must show that for every $x \in \mathcal{X}$ there exists a morphism $Sup_K F(x) \to M(x)$.

Fix $x \in \mathcal{X}$ and take any $F(a) \in B_x$. Then there is $K(a) \to x$, and hence $M(K(a)) \to M(x)$ by functoriality of $M$. Composing with $F(a) \to M(K(a))$ (from $\alpha$) gives $F(a) \to M(x)$. Thus $M(x)$ is an upper bound of $B_x$. Since $Sup_K F(x)$ is the least upper bound, there exists a morphism $Sup_K F(x) \to M(x)$.

---

**Uniqueness (objectwise isomorphism)**

Conversely, suppose $M: \mathcal{X} \to \mathcal{C}$ is a left Kan extension of $F$ along $K$. Then $M(x) \cong Sup_K F(x)$ for every $x \in \mathcal{X}$.

**Proof.** Let $M$ be a left Kan extension. Then there exists $\eta: F \Rightarrow M \circ K$.

- **Step 1:** $M(x)$ is an upper bound of $B_x$.  
  For any $F(a) \in B_x$, we have $K(a) \to x$, hence $M(K(a)) \to M(x)$, and $F(a) \to M(K(a))$ by $\eta$. Their composite gives $F(a) \to M(x)$. Thus $M(x)$ is an upper bound of $B_x$.

- **Step 2:** There exists $Sup_K F(x) \to M(x)$.  
  This follows immediately because $M(x)$ is an upper bound and $Sup_K F(x)$ is the least one.

- **Step 3:** There exists $M(x) \to Sup_K F(x)$.  
  Since $Sup_K F$ itself satisfies the universal property of the left Kan extension (as shown above), the defining property of $M$ as a left Kan extension implies the existence of a morphism $M(x) \to Sup_K F(x)$.

Therefore, $M(x) \cong Sup_K F(x)$ for all $x$.

Finally, if $\sup B_x$ does not exist for some $x$, but $Lan_K F(x)$ existed, then by the above we would have $Lan_K F(x) \cong Sup_K F(x)$, a contradiction. Hence the left Kan extension fails to exist in that case.
(proof complete)

From this proposition, the necessary and sufficient condition for the existence of a left Kan extension with a thin category as target is that $\sup B_x$ exists for every $x \in \mathcal{X}$.

## Relation to the General Case

Next, let $\mathcal{C}$ be a general locally small category. Suppose that the left Kan extension $Lan_K F: \mathcal{X} \to \mathcal{C}$ of a functor $F: \mathcal{A} \to \mathcal{C}$ along $K: \mathcal{A} \to \mathcal{X}$ exists.

In a general category, the value $Lan_K F(x)$ at an object $x \in \mathcal{X}$ can be expressed as the **colimit** of the diagram consisting of the objects in the comma category $(K \downarrow x)$. That is, if we consider the collection of objects in $\mathcal{C}$

$B_x = ｛ F(a) \mid a \in \mathcal{A} \text{ such that there exists a morphism } K(a) \to x \text{ in } \mathcal{X} ｝,$

together with all morphisms between them induced by the comma category $(K \downarrow x)$, then $Lan_K F(x)$ is the colimit (universal cocone vertex) of this diagram.

Consequently, for every $a \in \mathcal{A}$ and every morphism $K(a) \to x$, there exists a **universal morphism** (the colimit leg)
$\iota_a: F(a) \to Lan_K F(x)　in \mathcal{C}$.

(We omit the detailed explanation of the comma category characterization of Kan extensions and the proof of the existence of these universal morphisms. Please refer to standard category theory textbooks for this background. From this perspective, it is important to note that $B_x$ is not merely a collection of objects, but rather the image of a diagram — i.e., a functor — whose domain is the comma category $(K \downarrow x)$.)

Even in this general setting, if $\sup B_x$ exists in $\mathcal{C}$ for each $x$, we can choose one such supremum and denote it by $Sup_K F(x)$, thereby defining a functor $Sup_K F: \mathcal{X} \to \mathcal{C}$.

As shown above, $Lan_K F(x)$ is one of the upper bounds of the collection $B_x$. Therefore, whenever $\sup B_x$ exists (i.e., whenever $Sup_K F(x)$ can be defined), the minimality of the supremum guarantees the existence of a morphism

$Sup_K F(x) \to Lan_K F(x)$

in $\mathcal{C}$.
Furthermore, if a thinning functor $T : \mathcal{C} \to \mathcal{D}$ to a thin category $\mathcal{D}$ is given, the following proposition holds.

**Proposition**  
If the left Kan extension $Lan_K (T \circ F) : \mathcal{X} \to \mathcal{D}$ of the composite functor $T \circ F$ along $K$ exists, then for every $x \in \mathcal{X}$ there exist morphisms
$Lan_K (T \circ F)(x) \to (T \circ Sup_K F)(x) \to (T \circ Lan_K F)(x).$

**Proof**

For each $x \in \mathcal{X}$, define the subclass $B'_x \subseteq \mathrm{Ob}(\mathcal{D})$ by

$B'_x = ｛ (T \circ F)(a) \mid a \in \mathcal{A} \text{ such that there exists a morphism } K(a) \to x \text{ in } \mathcal{X} ｝.$

If we set $Sup_K (T \circ F)(x) := \sup B'_x$ (choosing one supremum arbitrarily when multiple exist), then the resulting functor $Sup_K (T \circ F): \mathcal{X} \to \mathcal{D}$ is a left Kan extension of $T \circ F$ along $K$. This follows directly from the previous proposition.

Next, we show that for every $x \in \mathcal{X}$, there exists a morphism

$(Lan_K (T \circ F))(x) \ \to \ (T \circ Lan_K F)(x)$

in $\mathcal{D}$.

As established earlier, for any $a \in \mathcal{A}$ and any morphism $K(a) \to x$ in $\mathcal{X}$, there exists a universal morphism (colimit leg) in $\mathcal{C}$:

$\iota_a: F(a) \ \to \ (Lan_K F)(x).$

Applying the functor $T: \mathcal{C} \to \mathcal{D}$ (which preserves morphisms), we obtain a morphism in $\mathcal{D}$:

$T(\iota_a): (T \circ F)(a) \ \to \ (T \circ Lan_K F)(x).$

This shows that the object $(T \circ Lan_K F)(x)$ is an upper bound of the collection $B'_x$ in $\mathcal{D}$.

Since $Sup_K (T \circ F)(x) \cong \sup B'_x$ is the *least* upper bound, and $Lan_K (T \circ F)(x) \cong Sup_K (T \circ F)(x)$, there exists a morphism

$Lan_K (T \circ F)(x) \ \to \ (T \circ Lan_K F)(x).$

Moreover, from the relationship between the functor and the supremum shown previously, there also exists a morphism

$Lan_K (T \circ F)(x) \ \to \ (T \circ Sup_K F)(x).$

Combining these, we obtain the desired chain of morphisms in $\mathcal{D}$ for each $x \in \mathcal{X}$.
(proof complete)


This proposition shows that, when the order on the thin functor category $[\mathcal{X}, \mathcal{D}]$ is denoted by $\leq$, we have
$Lan_K (T \circ F) \leq T \circ Sup_K F \leq T \circ Lan_K F.$

Moreover, if we take the packed arrows functor as the thinning functor $T$, and if $Lan_K F$ exists, then $Lan_K (T \circ F) \cong Sup_K (T \circ F)$ is also defined since $T\circ\text{Lan}_KF=\text{Lan}_K (T\circ F)=\text{Lan}_KF$ as mapping of objects.

As a contrapositive, if $Lan_K (T \circ F)$ does not exist, then $Lan_K F$ does not exist either. This can sometimes serve as a simple criterion for the non-existence of Kan extensions.

It is easier to check the non-existence of a Kan extension in a thin category than in a thick one.

---

## Lower Bounds and Right Kan Extensions

Lower bounds and right Kan extensions can be treated analogously (proofs omitted).

For a subclass $B \subseteq Ob(\mathcal{C})$ of a locally small category $\mathcal{C}$, an object $a \in Ob(\mathcal{C})$ satisfies the following two conditions:

1. **Lower bound property**: For every $b \in B$, there exists a morphism $a \to b$.
2. **Greatest lower bound property**: If there exists an object $a' \in Ob(\mathcal{C})$ such that $a' \to b$ for every $b \in B$, then there exists a morphism $a' \to a$.

Such an $a$ is called the **infimum** (or **lower bound**) of $B$, denoted by $\inf B$ or $\bigwedge B$.

If $\mathcal{C}$ is skeletal, the infimum is unique.

Right Kan extensions can be defined using $\inf B_x$ as $Inf_K F$, and with a thinning functor $T : \mathcal{C} \to \mathcal{D}$, we obtain the inequality
$T \circ Ran_K F \leq T \circ Inf_K F \leq Ran_K (T \circ F).$

If the slogan "every concept in category theory is a Kan extension" is true, then "every concept with a thin category as target is an upper or lower bound."
