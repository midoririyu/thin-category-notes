**[Back to Table of Contents](../README.md)**

# Thin Categories (3)  
Properties of Functors from Locally Small Categories to Thin Categories (Thinning Functors), Natural Transformations, and Functor Categories

We consider functors from a locally small category $\mathcal{C}$ to a thin category $\mathcal{C}(B,g)$ (so-called **thinning functors**).

## Proposition 3-1

**Proposition 3-1**  
A functor $T$ from a locally small category $\mathcal{C}$ to a thin category $\mathcal{C}(B,g)$ exists if and only if there is a map $T: \operatorname{Ob}(\mathcal{C}) \to B$ and for every $i,j \in \operatorname{Ob}(\mathcal{C})$, the morphism $g_{T(i)T(j)}$ exists in $\mathcal{C}_B$.

**Proof**  
Necessity is clear, so we show sufficiency.

By assumption, for each $i \in \operatorname{Ob}(\mathcal{C})$ there is a unique $T(i) \in B$, and for every $i,j \in \operatorname{Ob}(\mathcal{C})$, $g_{T(i)T(j)}$ exists.

Let $\operatorname{hom}(\mathcal{C})$ be the class of all morphisms in $\mathcal{C}$. Define
$$
T : \operatorname{hom}(\mathcal{C}) \to \operatorname{hom}(\mathcal{C}_B), \quad T(f : i \to j) := g_{T(i)T(j)}.
$$
This is a well-defined map.

**(Well-definedness)**  
If $f_1 : i \to j$ and $f_2 : k \to l$ are the same morphism in $\operatorname{hom}(\mathcal{C})$, then $i = k$ and $j = l$, so $T(i) = T(k)$ and $T(j) = T(l)$. By uniqueness of morphisms in thin categories, $g_{T(i)T(j)} = g_{T(k)T(l)}$, hence $T(f_1) = T(f_2)$.

Moreover, this $T$ preserves composition and identity morphisms.

**(Proof)**  
$$
T(f_2 : j \to m) \circ T(f_1 : i \to j) = g_{T(j)T(m)} \circ g_{T(i)T(j)} = g_{T(i)T(m)} = T(f_2 \circ f_1 : i \to m)
$$
and
$$
T(f : i \to i) = g_{T(i)T(i)}.
$$
(End of proof of Proposition 3-1)

## Proposition 3-2

**Proposition 3-2**  
A functor $T$ from a thin small category $\mathcal{C}_A$ to a thin small category $\mathcal{C}_B$ exists if and only if there is a monotone map $T$ between the preordered sets $A$ and $B$.

**Note**  
A monotone map $T : A \to B$ means that $i \leq j$ in $A$ implies $T(i) \leq T(j)$ in $B$.

**Proof**  
This follows by applying Proposition 3-1 to Example 5 in "Thin Categories (1)". (Proof complete)

## Proposition 3-3

**Proposition 3-3-1**  
$T$ is faithful if and only if $\mathcal{C}$ is a thin category.

**Proposition 3-3-2**  
If $\mathcal{C}$ is strongly connected, then $T$ is full.

**Proof of Proposition 3-3-1**  
**(Necessity)**  
$T$ is faithful if $T(f_1) = T(f_2)$ implies $f_1 = f_2$ for morphisms $f_1, f_2 : i \to j$. Since $\mathcal{C}(B,g)$ is thin, $T(f_1) = g_{T(i)T(j)} = T(f_2)$ always holds. Thus $\operatorname{hom}(i,j)$ is at most a singleton, so $\mathcal{C}$ is thin.

**(Sufficiency)**  
Suppose $T$ is not faithful. Then there exist $f_1 \neq f_2 : i \to j$ with $T(f_1) = T(f_2)$, contradicting that $\mathcal{C}$ is thin. (Proof complete)

**Proof of Proposition 3-3-2**  
$T$ is full if for every $g_{T(i)T(j)}$ there exists $f : i \to j$ such that $T(f) = g_{T(i)T(j)}$. Since $\mathcal{C}$ is strongly connected, such an $f$ always exists. (Proof complete)

## Lemma 3-1

**Lemma 3-1**  
A functor $T : \mathcal{C} \to \mathcal{C}(B,g)$ from a locally small category $\mathcal{C}$ is an equivalence if $\mathcal{C}$ is a strongly connected thin category and $T$ is essentially surjective.

**Proof**  
It is well-known that a functor is an equivalence if and only if it is fully faithful and essentially surjective. Applying Proposition 3-3 yields the result. (Proof complete)

## Proposition 3-4

**Proposition 3-4**  
Thin small categories $\mathcal{C}_A$ and $\mathcal{C}_B$ are equivalent if and only if there is a monotone map $T : A \to B$ between the preordered sets $A$ and $B$ satisfying:

- If $T(i) \leq T(j)$, then $i \leq j$.
- For every $k \in B$, there exists $i \in A$ such that $k \leq T(i)$ and $T(i) \leq k$.

**Proof**  
Combine the characterization of equivalences with Proposition 3-2 and Proposition 3-3-1. (Proof complete)

**Corollary 3-1**  
Skeletal thin small categories $\mathcal{C}_A$ and $\mathcal{C}_B$ are equivalent if and only if there is a bijective monotone map $T : A \to B$ between the partially ordered sets $A$ and $B$.

**Proof**  
Apply the antisymmetry condition $i \leq j$ and $j \leq i$ implies $i = j$ to Proposition 3-4. (Proof complete)

## Preservation of Universal Objects

**Proposition 3-5** (Left Universal Objects)  
Let $T : \mathcal{C} \to \mathcal{C}(B,g)$ be a functor from a locally small category $\mathcal{C}$. If $i$ is a (left) universal object in $\mathcal{C}$, then $T(i)$ is a (left) universal object in $T(\mathcal{C})$. In particular, if $T$ is essentially surjective, then $T(i)$ is a (left) universal object in $\mathcal{C}(B,g)$.

(Proof follows the standard argument using the representing property of the Hom functor and natural isomorphisms, adapted to the thin setting.)

**Note**  
Examples of left universal objects: initial objects, coproducts, coequalizers, etc.

**Proposition 3-6** (Right Universal Objects)  
If $T$ is essentially surjective, then (right) universal objects are also preserved.

**Note**  
Examples of right universal objects: terminal objects, products, equalizers, etc.

**Proposition 3-7**  
If $T$ is essentially surjective, then universal objects in $\mathcal{C}$ are mapped to universal objects in $\mathcal{C}(B,g)$.

## Adjunctions

**Proposition 3-8**  
Let $T : \mathcal{C}_A \to \mathcal{C}_B$ be a functor between thin categories with $T : A \to B$ injective on objects. Then there exists a functor $T' : T(\mathcal{C}_A) \to \mathcal{C}_A$ defined by $T'(T(i)) = i$ and $T'(g_{T(i)T(j)}) = f_{ij}$, and $T$ is left adjoint to $T'$ ($T \dashv T'$).

**Note**  
When $\mathcal{C}_A$ and $\mathcal{C}_B$ are skeletal (i.e., $A$ and $B$ are posets), $T$ and $T'$ form a Galois connection.

## Natural Transformations and Functor Categories

Given functors $T, T' : \mathcal{C} \to \mathcal{C}(B,g)$, the family
$$
\tau_{T,T'} := \{\tau_i := g_{T(i)T'(i)}\}_{i \in \operatorname{Ob}(\mathcal{C})}
$$
is the unique natural transformation from $T$ to $T'$, with each $\tau_i$ as its component.

If each $\tau_i$ has an inverse $g_{T'(i)T(i)}$, then $\tau_{T,T'}$ is a natural isomorphism ($T \cong T'$).

Let $\Phi$ be the collection of all functors from $\mathcal{C}$ to $\mathcal{C}(B,g)$. Then $\mathcal{C}(\Phi, \{\tau_{T,T'}\})$ is a thin category, and is precisely the **functor category** $[\mathcal{C}, \mathcal{C}(B,g)]$.



