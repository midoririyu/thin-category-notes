**[Back to Table of Contents](../README.md)**

# Thin Categories (11)  
Quotient Categories via Thinning Functors

Suppose a functor $T : \mathcal{C} \to \mathcal{C}(B,g)$ is defined from a locally small category $\mathcal{C}$ to a thin category $\mathcal{C}(B,g)$.

## Equivalence Relation on Morphisms

For any morphisms $f : i \to j$ and $f' : k \to l$ in $\mathcal{C}$, define the relation $fTf'$ by $T(f) = T(f')$.

This relation satisfies the conditions of an equivalence relation:

1. If $\mathcal{C}$ is non-empty, then $fTf$ holds for every $f \in \operatorname{hom}(\mathcal{C})$.
2. For any $f,f' \in \operatorname{hom}(\mathcal{C})$, $fTf'$ implies $f'Tf$.
3. For any $f,f',f'' \in \operatorname{hom}(\mathcal{C})$, if $fTf'$ and $f'Tf''$, then $fTf''$.

**Proof**  
1. Follows from $T(f) = T(f)$.  
2. If $T(f) = T(f')$, then $T(f') = T(f)$.  
3. If $T(f) = T(f')$ and $T(f') = T(f'')$, then $T(f) = T(f'')$. (Proof complete)

## Definition of the Quotient Category $\mathcal{C}/T$

Based on the above equivalence relation, for a morphism $f : i \to j$ in $\operatorname{hom}(\mathcal{C})$, define the equivalence class
$$
[f]^T_{ij} := \{f' \in \operatorname{hom}(\mathcal{C}) \mid T(f) = T(f')\}.
$$

For each pair $i,j \in \operatorname{Ob}(\mathcal{C})$, if a morphism $f : i \to j$ exists, then $[f]^T_{ij}$ is uniquely determined regardless of the choice of representative. Thus it can be regarded as a (generalized) binary operation on $i$ and $j$.

Moreover, if $[f_1]^T_{ij}$ and $[f_2]^T_{jk}$ exist, then $[f_2 \circ f_1]^T_{ik}$ necessarily exists, and we can define the operation
$$
[f_2]^T_{jk} \circ [f_1]^T_{ij} := [f_2 \circ f_1]^T_{ik}.
$$

For any object $i$ in $\mathcal{C}$, the class $[ \mathrm{id}_i ]^T := \{f \in \operatorname{hom}(\mathcal{C}) \mid T(f) = T(\mathrm{id}_i)\}$ is non-empty by the existence of the identity morphism.

Applying Definition 1 from "Thin Categories (1)" to the above facts, we obtain a thin category $\mathcal{C}(\operatorname{Ob}(\mathcal{C}), [f]^T)$ from $\mathcal{C}$. We denote this category by $\mathcal{C}/T$.

## Proposition 11-1

**Proposition 11-1**  
If the functor $T : \mathcal{C} \to \mathcal{C}(B,g)$ is full, then $\mathcal{C}/T$ and $T(\mathcal{C})$ are equivalent.

**Proof**  
Define a functor $\bar{T} : \mathcal{C}/T \to T(\mathcal{C})$ by $\bar{T}(i) := T(i)$ and $\bar{T}([f]^T_{ij}) := T(f)$. Since $T$ is full, for every $g_{T(i)T(j)}$ there exists $f : i \to j$, so $\bar{T}([f]^T_{ij})$ is defined. This also shows that $\bar{T}$ is full.

$\bar{T}$ is surjective on objects, hence essentially surjective. Since $\mathcal{C}/T$ is thin, by Proposition 3-3-1 in "Thin Categories (3)", $\bar{T}$ is faithful. Therefore $\mathcal{C}/T$ and $T(\mathcal{C})$ are equivalent. (Proof complete)

## Proposition 11-2

**Proposition 11-2**  
If the functor $T : \mathcal{C} \to \mathcal{C}(B,g)$ is full and essentially surjective, then $\mathcal{C}/T$ and $\mathcal{C}(B,g)$ are equivalent.

**Proof**  
Define a functor $\bar{T} : \mathcal{C}/T \to \mathcal{C}(B,g)$ by $\bar{T}(i) := T(i)$ and $\bar{T}([f]^T_{ij}) := T(f)$. Since $T$ is full, for every $g_{T(i)T(j)}$ there exists $f : i \to j$. Since $T$ is essentially surjective, $\bar{T}$ is also essentially surjective. As $\mathcal{C}/T$ is thin, $\mathcal{C}/T$ and $\mathcal{C}(B,g)$ are equivalent. (Proof complete)

## Case of Composite Functors

We write $\mathcal{C} \cong \mathcal{D}$ when two categories $\mathcal{C}$ and $\mathcal{D}$ are equivalent.

Suppose $T : \mathcal{C} \to \mathcal{C}(B,g)$ is a functor from a locally small category $\mathcal{C}$ to a thin category, and $S : T(\mathcal{C}) \to \mathcal{D}$ is a functor from the thin category $T(\mathcal{C})$ to another thin category $\mathcal{D}$.

Then we can consider the composite functor $S \circ T : \mathcal{C} \to \mathcal{D}$, which yields the thin categories $T(\mathcal{C})/S$ and $\mathcal{C}/(S \circ T)$.

If both $T$ and $S$ are full functors, then $S \circ T$ is also full. By the propositions above,
$$
\mathcal{C}/T \cong T(\mathcal{C}), \quad T(\mathcal{C})/S \cong S(T(\mathcal{C})), \quad \mathcal{C}/(S \circ T) \cong S(T(\mathcal{C})).
$$
Furthermore,
$$
T(\mathcal{C})/S \cong \mathcal{C}/(S \circ T) \cong S(\mathcal{C}/T)
$$
holds.
