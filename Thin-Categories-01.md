**[Back to Table of Contents](../README.md)**

# Thin Categories (1)  
A Reformulation of Thin Categories and Examples

## Preface

In standard category theory textbooks, a **thin category** (a category with at most one morphism between any two objects) is often briefly described as being essentially the same as a preordered set. However, in reality, thin categories can be formed even from collections that are not sets, making the concept broader than just ordered sets.

The author has reformulated the definition of thin categories to make it easier to understand even in cases that are not ordered sets, and has investigated their properties.

---

In this paper, a **class** is assumed to satisfy the following: unless it is empty, any element can be selected from it, and for any two elements, it is clearly determinable whether they are equal or not.

## Reformulation of Thin Categories (Definition)

To make thin categories easier to handle, we first consider the following structure.

**Definition**  
Let $A$ be a class. For any $i \in A$ and any $j \in A$, there is at most one thing (if it exists) denoted by $f_{ij}$. This (generalized binary operation) $f_{ij}$ satisfies the following two conditions:

1. If $A$ is non-empty, then for every $i \in A$, $f_{ii}$ exists.
2. For any $i,j,k \in A$, if $f_{ij}$ and $f_{jk}$ exist, then $f_{ik}$ necessarily exists, and the operation $\circ$ is defined by
$f_{jk} \circ f_{ij} := f_{ik}.$
   
In this definition, it can be shown that the operation $\circ$ is associative.

**Proof**  

$(f_{kl} \circ f_{jk}) \circ f_{ij} = f_{jl} \circ f_{ij} = f_{il} = f_{kl} \circ f_{ik} 
= f_{kl} \circ (f_{jk} \circ f_{ij})$.
(Proof complete)

Furthermore, for any $i,j \in A$,
$f_{ij} \circ f_{ii} = f_{ij} = f_{jj} \circ f_{ij}$ holds, so $f_{ii}$ can be regarded as the identity morphism at $i$.

Thus, $f_{ij}$ satisfies the definition of a morphism, and we can define a thin category with objects $i \in A$ and morphisms $f_{ij}$.

**Converse**  
Conversely, in any thin category $\mathcal{C}$, there is at most one morphism $f : i \to j$ for each pair of objects $i,j$. Therefore, such a morphism (when it exists) can be understood as the binary operation $f_{ij}$. This operation satisfies the two conditions in the definition above.

That is, the structure defined above is a **reformulation of thin categories**.

---

Henceforth, any thin category will be denoted by $\mathcal{C}(A,f)$ or $C_A$ using the notation from the definition above where $f$ is denoted as the collection of $f_{ij}(i \in A, j \in A)$.

## Basic Properties of Thin Category $C_A$

- $C_A$ is a **locally small category**, since for any $i,j \in A$, the hom-set $\mathrm{hom}(i,j) := \{f_{ij}\}$ is either empty or a singleton.
- If $f_{ji}$ exists for $f_{ij}$, then
  $f_{ji} \circ f_{ij} = f_{ii} \quad \text{and} \quad f_{ij} \circ f_{ji} = f_{jj},$
  so $f_{ji}$ is the inverse of $f_{ij}$, and $i$ and $j$ are **isomorphic objects** (essentially the same).
- When $A$ is the empty class, $C_A$ is the **empty category**.

## Examples

### Example 1: The Trivial Category

When $A$ is a set of cardinality 1, $A \simeq ${1}. Defining the operation by $f_{11} \circ f_{11} = f_{11}$ gives $\mathrm{hom}(C_A) \simeq ${f_{11}}. Thus, $C_A$ is isomorphic to the category $\mathbf{1}$ with one object and one morphism.

### Example 2: From Magmas and Semigroups to Thin Categories

Let $A$ and $B$ be sets, and let $f : A \times A \to B$ be a map with $(i,j) \mapsto f_{ij}$. Defining the operation by
$f_{jk} \circ f_{ij} := f_{ik}$
yields a thin category $\mathcal{C}(A,f)$.

In particular, when $A = B$, i.e., for a magma $(A, *)$, defining the operation by
$
(j * k) \circ (i * j) := i * k
$
gives a thin category $\mathcal{C}(A,*)$.

Furthermore, if $(A,*)$ is a semigroup with unit $e$, then $\mathcal{C}(A,*)$ becomes a (thin) **monoidal category** with unit object $e$ and monoidal operation $*$.

### Example 3: Enrichment Examples

Let $f : A \times A \to B$ be a map from a set $A$ to a semigroup $(B,*)$ with unit $e$, satisfying the composition law and $f_{ii} = e$ for all $i$. Then $\mathcal{C}(A,f)$ is a (thin) **enriched category** over the monoidal category $\mathcal{C}(B,*)$.

**Metric Space Example**  
Let $A$ be a metric space with distance $d_{ij}$. Then $\mathcal{C}(A,d)$ is a thin category satisfying
$
d_{jk} \circ d_{ij} = d_{ik} \leq d_{jk} + d_{ij}.
$

Viewing the non-negative reals $\mathbb{R}_{\geq 0}$ as a monoidal category $\mathcal{C}(\mathbb{R}_{\geq 0}, +)$ with addition as the monoidal operation and $0$ as the unit, $\mathcal{C}(A,d)$ becomes a (thin) **enriched category** over it.

### Example 4: Construction from Any Locally Small Category

For any locally small category $\mathcal{C}$, let $\mathrm{Ob}(\mathcal{C})$ be the class of objects, and let $h_{ij} = \mathrm{hom}(i,j)$. Defining the operation by
$
h_{jk} \circ h_{ij} := h_{ik}
$
yields a thin category $\mathcal{C}(\mathrm{Ob}(\mathcal{C}), h)$.

**Note**  
The composition of morphisms in $h_{ij}$ and $h_{jk}$ lands in $h_{ik}$, but not every morphism in $h_{ik}$ can necessarily be expressed as such a composition.

**Note**  
For every pair $i,j \in \mathrm{Ob}(\mathcal{C})$, the set $h_{ij}$ exists. Therefore, $\mathcal{C}(\mathrm{Ob}(\mathcal{C}), h)$ is a **strongly connected category** in which there is a morphism between any pair of objects, and thus every pair of objects is isomorphic.

### Example 5: Another Reformulation via Relations

In the thin category $C_A$, the statement “morphism $f_{ij}$ exists” can be reinterpreted as the existence of a (generalized) relation $i \mathrel{f} j$ (unique when it exists). This relation satisfies:

1. If $A$ is non-empty, then $i \mathrel{f} i$ holds for all $i \in A$.
2. If $i \mathrel{f} j$ and $j \mathrel{f} k$, then $i \mathrel{f} k$.

Conversely, such a relation defines a thin category $\mathcal{C}(A,f)$.

---

Thus, a thin category $C_A$ can be described as a class equipped with a relation satisfying the above two conditions.

In particular, when $A$ is a **set**, the relation $i \mathrel{f} j$ satisfies the axioms of a preorder, so having a thin category $\mathcal{C}(A,f)$ is equivalent to $A$ being a preordered set.

Furthermore, $\mathcal{C}(A,f)$ being **skeletal** (i.e., $f_{ij}$ and $f_{ji}$ existing implies $i = j$) is equivalent to $A$ being a partially ordered set.

If $\mathcal{C}(A,f)$ is skeletal and strongly connected, then $A$ is a totally ordered set.

**Example with the Class of All Sets**  
Let $A = \mathbf{Set}$, the class of all sets, and consider the inclusion relation $i \subset j$. This satisfies the above conditions and is antisymmetric. Since $\mathbf{Set}$ is a proper class, $\mathcal{C}(\mathbf{Set}, \subset)$ is a **skeletal thin category that is not small**.
