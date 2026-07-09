**[Back to Table of Contents](README.md)**

# Thin Categories (4)  
Packed Arrows Functors, Strongly Connected Thin Categories, and Quotient Categories

## Definition of the Packed Arrows Functor

**Definition**  
Let $\mathcal{C}$ be a locally small category. There exists a functor $P$ between $\mathcal{C}$ and the strongly connected thin category $\mathcal{C}(Ob(\mathcal{C}), h)$ from Example 4 in Thin Categories (1), defined by $P(i) := i$ and $P(f : i \to j) := h_{ij} = Hom(i,j)$ for $i,j \in Ob(\mathcal{C})$. That $P$ is a functor follows from Proposition 3-1. Moreover, $P$ is the identity on objects (hence surjective), so it is an **essentially surjective** functor.

Henceforth, we call this the **packed arrows functor** (in this paper only), and denote the category $\mathcal{C}(Ob(\mathcal{C}), h)$ by $P(\mathcal{C})$, calling it the **packed arrows category** of $\mathcal{C}$.

## Proposition 4-1

**Proposition 4-1**  
The packed arrows functor $P$ satisfies the following:

1. $P$ is full if and only if the locally small category $\mathcal{C}$ is strongly connected.
2. $P$ is faithful if and only if the locally small category $\mathcal{C}$ is thin.

**Proof**  
1. $P$ is full $\iff$ for every $Hom(i,j)$ there exists $f : i \to j$ $\iff$ there is a morphism between any pair of objects $\iff$ $\mathcal{C}$ is strongly connected.  
2. $P$ is faithful $\iff$ every $Hom(i,j)$ is at most a singleton $\iff$ $\mathcal{C}$ is thin.

(Proof complete)

## Proposition 4-2

**Proposition 4-2**  
For a locally small category $\mathcal{C}$, $\mathcal{C}$ is equivalent to $P(\mathcal{C})$ if and only if $\mathcal{C}$ is a strongly connected thin category.

**Proof**  
In general, a functor is an equivalence if and only if it is fully faithful and essentially surjective. Since $P$ is essentially surjective, by Proposition 4-1 it is fully faithful precisely when $\mathcal{C}$ is strongly connected and thin. Moreover, since $P$ is the identity on objects (a bijection), the equivalence strengthens to an isomorphism of categories. (Proof complete)

## Proposition 4-3

**Proposition 4-3**  
If locally small categories $\mathcal{C}$ and $\mathcal{D}$ are equivalent, then their packed arrows categories $P(\mathcal{C})$ and $P(\mathcal{D})$ are also equivalent.

**Proof**  
Let $F : \mathcal{C} \to \mathcal{D}$ be a functor. Then there is an induced functor $P(F) : P(\mathcal{C}) \to P(\mathcal{D})$ defined by $P(F)(i) := F(i)$ and $P(F)(h_{ij}) := Hom(F(i), F(j))$ by Proposition 3-1. If $F$ is an equivalence, then $P(\mathcal{C})$ is strongly connected and thin, and $P(F)$ is essentially surjective, so by Lemma 3-1, $P(F)$ is an equivalence. (Proof complete)

## Proposition 4-4

**Proposition 4-4**  
If $i$ is a universal object in the locally small category $\mathcal{C}$, then $P(i) = i$ is also a universal object in $P(\mathcal{C})$.

**Proof**  
This follows by applying the propositions on universal objects in "Thin Categories (3)" to the fact that $P$ is an essentially surjective functor to a thin category. (Proof complete)

## Proposition 4-5 (Universal Property of the Packed Arrows Functor)

**Proposition 4-5**  
Let $\mathcal{C}$ be a locally small category and $\mathcal{D}$ a thin category. For any thinning functor $F : \mathcal{C} \to \mathcal{D}$, there exists a unique functor $\tilde{F} : P(\mathcal{C}) \to \mathcal{D}$ such that $F = \tilde{F} \circ P.$

In particular, if $F$ is essentially surjective, then $\tilde{F}$ is an equivalence.

**Proof**  
1. **On objects**: Since $Ob(P(\mathcal{C})) = Ob(\mathcal{C})$, define $\tilde{F}(i) := F(i)$.  
2. **On morphisms**: For a morphism $h_{ij} = Hom_{\mathcal{C}}(i,j)$ in $P(\mathcal{C})$, define $\tilde{F}(h_{ij}) := g_{F(i)F(j)}$ (unique because $\mathcal{D}$ is thin). That $\tilde{F}$ is a functor follows from Proposition 3-1.  
3. **Factorization and uniqueness**: $(\tilde{F} \circ P)(f) = \tilde{F}(h_{ij}) = g_{F(i)F(j)} = F(f)$. Uniqueness follows from the uniqueness of morphisms in $\mathcal{D}$.

If $F$ is essentially surjective, then so is $\tilde{F}$. Since $P(\mathcal{C})$ is strongly connected and thin, $\tilde{F}$ is an equivalence by Lemma 3-1. (Proof complete)

## Quotient Categories
Let $\mathbf{CAT}$ be the collection of all locally small categories. We denote the equivalence of locally small categories $\mathcal{C}$ and $\mathcal{D}$ as $\mathcal{C} \sim \mathcal{D}$. The relation $\sim$ satisfies the following properties:

* **Reflexivity**: $\mathcal{C} \sim \mathcal{C}$
* **Symmetry**: If $\mathcal{C} \sim \mathcal{D}$, then $\mathcal{D} \sim \mathcal{C}$
* **Transitivity**: If $\mathcal{C} \sim \mathcal{D}$ and $\mathcal{D} \sim \mathcal{E}$, then $\mathcal{C} \sim \mathcal{E}$

Under this relation, we can consider the quotient class $\mathbf{CAT} / \sim$, where each equivalence class is defined as $｛\mathcal{C}｝ = ｛\mathcal{D} \in \mathbf{CAT} \mid \mathcal{C} \sim \mathcal{D}｝$.

Similarly, given a projection functor $P$, we can define a relation $\mathcal{C} \sim_P \mathcal{D}$ to mean that $P(\mathcal{C})$ and $P(\mathcal{D})$ are equivalent categories. This allows us to consider the quotient class $\mathbf{CAT} / \sim_P$. The fact that the relation $\sim_P$ satisfies reflexivity, symmetry, and transitivity follows directly from the properties of category equivalence:

* $P(\mathcal{C}) \sim P(\mathcal{C})$
* If $P(\mathcal{C}) \sim P(\mathcal{D})$, then $P(\mathcal{D}) \sim P(\mathcal{C})$
* If $P(\mathcal{C}) \sim P(\mathcal{D})$ and $P(\mathcal{D}) \sim P(\mathcal{E})$, then $P(\mathcal{C}) \sim P(\mathcal{E})$

Based on these setups, the following proposition holds:

**Proposition 4-6**  
$\mathbf{CAT}/\sim$ is a subclass (finer partition) of $\mathbf{CAT}/P$.

**Proof**  
By Proposition 4-3, the structure of $\mathbf{CAT}/\sim$ naturally embeds into the coarser quotient $\mathbf{CAT}/P$. (Proof complete)

---

### Quotient Categories of Small Categories

Let $\mathbf{Cat}$ be the collection of all small categories, and consider its quotient $\mathbf{Cat}/\sim$. Objects are small categories themselves, and a morphism from $\mathcal{C}$ to $\mathcal{D}$ is an equivalence class of functors
$[F]_{CD} := ｛F' : \mathcal{C} \to \mathcal{D} \mid F' \text{ is naturally isomorphic to } F｝.$

 **Proof of the Well-Definedness of $[F]_{CD}$ as a Morphism Under the Composition $[F]_{CD} \circ [F]_{CD} := [F]_{CE}$**

#### 1. Composition of Morphisms
Let $F, F': \mathcal{C} \to \mathcal{D}$ and $G, G': \mathcal{D} \to \mathcal{E}$ be pairs of naturally isomorphic functors. 

For any object $i$ in $\mathcal{C}$, there exists an isomorphism $\alpha_i: F(i) \to F'(i)$ with its inverse $\alpha'_i: F'(i) \to F(i)$ such that for any morphism $f: i \to j$ in $\mathcal{C}$, the following diagram commutes:
$\alpha_j \circ F(f) = F'(f) \circ \alpha_i$

Similarly, for any object $k$ in $\mathcal{D}$, there exists an isomorphism $\beta_k: G(k) \to G'(k)$ with its inverse $\beta'_k: G'(k) \to G(k)$ such that for any morphism $g: k \to l$ in $\mathcal{D}$, the following diagram commutes:
$\beta_l \circ G(g) = G'(g) \circ \beta_k.$

Consequently, for any object $i$ in $\mathcal{C}$, the morphism $\beta_{F(i)}: G(F(i)) \to G'(F(i))$ has an inverse $\beta_{F(i)}': G'(F(i)) \to G(F(i))$, and the following relation holds:
$\beta_{F(j)} \circ G(F(f)) = G'(F'(f)) \circ \beta_{F(i)}.$

This demonstrates that the composite functors $G \circ F$ and $G' \circ F'$ from $\mathcal{C}$ to $\mathcal{E}$ are naturally isomorphic.

#### 2. Existence of Identity Morphisms
Let $[F]_{CC} := ｛ F' : \mathcal{C} \to \mathcal{C} \mid F' \text{ is a functor naturally isomorphic to } F ｝$. 

For any morphism $[F]_{CD}$, this class satisfies both $[F]_{DD} \circ [F]_{CD} = [F]_{CD}$ and $[F]_{CD} \circ [F]_{CC} = [F]_{CD}$, thereby serving as the identity morphism. (Proof complete)

Similarly, we can define the packed arrows quotient $\mathbf{Cat}/P$, where morphisms are classes
$[F]^P_{CD} := ｛F' : \mathcal{C} \to \mathcal{D} \mid P(F') \text{ is naturally isomorphic to } P(F)｝.$

In this case, for any two functors $F, F' : \mathcal{C} \to \mathcal{D}$, the family $\alpha_i = Hom(F(i), F'(i))$ shows that $P(F)$ and $P(F')$ are always naturally isomorphic. Thus $[F]^P_{CD}$ is simply the set of **all** functors from $\mathcal{C}$ to $\mathcal{D}$. Therefore, $\mathbf{Cat}/P$ coincides with the packed arrows category $P(Cat)=C(Cat,Fct(C,D))(C,D\in Cat)$.

**Proposition 4-7**  
$\mathbf{Cat}/\sim$ is a subcategory of $\mathbf{Cat}/P$.

**Proof**  
The morphisms of $\mathbf{Cat}/\sim$ form a subclass of those of $\mathbf{Cat}/P$. (Proof complete)

## Proposition 4-8

**Proposition 4-8**  
Let $\mathbf{Sct}$ be the collection of all strongly connected thin small categories, and let $\mathbf{Sct}/\sim$ be its quotient. Then $\mathbf{Sct}/\sim$ is equivalent to $\mathbf{Cat}/P$, and can be viewed as a subcategory of it.

**Proof**  
Both $\mathbf{Cat}/P$ and $\mathbf{Sct}/\sim$ are strongly connected thin categories by construction.

Define a functor $t : \mathbf{Cat}/P \to \mathbf{Sct}/\sim$ by $t(\mathcal{C}) = P(\mathcal{C})$ and $t([F]^P_{CD}) = [F]_{P(C)P(D)}$. For any strongly connected thin category $\mathcal{C}$, we have $t(\mathcal{C}) = P(\mathcal{C}) = \mathcal{C}$, so $t$ is essentially surjective on objects.

By Lemma 3-1, $t$ is an equivalence.

Since $\mathbf{Sct}$ is a subclass of $\mathbf{Cat}$, $\mathbf{Sct}/\sim$ is a subcategory of $\mathbf{Cat}/\sim$, and combined with Proposition 4-7, it is a subcategory of $\mathbf{Cat}/P$. (Proof complete)
