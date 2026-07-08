**[Back to Table of Contents](../README.md)**

# Thin Categories (5)  
A Standard Method for Constructing (Thinning) a Thin Category from a Locally Small Category

One method for explicitly constructing a thin category from a locally small category $\mathcal{C}$ is the packed arrows category $\mathcal{C}(Ob(\mathcal{C}), Hom(i,j))(i,j \in Ob(\mathcal{C}))$ we have already seen. However, this has the very strong property of being strongly connected, which may make it impractical for many applications.

Below, we present a more standard method for constructing thin categories.

## Standard Construction of a Thinning

**Construction**  
For any $i,j \in Ob(\mathcal{C})$, if $Hom(i,j)$ is non-empty, choose any one entity $f_{ij}$'.  
If $Hom(i,j)$ is empty, then $f_{ij}$' does not exist.

Then $\mathcal{C}(Ob(\mathcal{C}), ｛f_{ij}'｝)(i,j \in Ob(\mathcal{C}))$ is a thin category.

**Proof**  
Suppose morphisms $f : i \to j$ and $g : j \to k$ exist in $\mathcal{C}$. Then the composite $g \circ f : i \to k$ exists. By assumption, $f_{ij}'$, $g_{jk}'$, and $g \circ f_{ik}'$ each exist uniquely. Define
$g_{jk}' \circ f_{ij}' := g \circ f_{ik}'.$
Then $f_{ij}'$ satisfies the conditions of Definition 1 in "Thin Categories (1)" as a generalized binary operation. Hence $\mathcal{C}(Ob(\mathcal{C}), ｛f_{ij}'｝)(i,j \in Ob(\mathcal{C}))$ is a thin category. (Proof complete)

**Example**  
If a proof of the proposition "A $\Rightarrow$ B" is accepted (even one such proof), then the proposition "A $\Rightarrow$ B" is established as true. In this way, one can construct a thin "propositional logic category" from a thick "category of proofs".

## Thinning Functor

Using the above construction, define a map on objects by $T(i) = i$ and on morphisms by $T(f : i \to j) = f_{ij}'$. This yields a **thinning functor**
$T : \mathcal{C} \to \mathcal{C}(Ob(\mathcal{C}),｛f_{ij}'｝)(i,j \in Ob(\mathcal{C})).$
That $T$ is a functor follows from Proposition 3-1 in "Thin Categories (3)".

**Remark**  
In particular, if we choose $f_{ij}'$ from an element of $Hom(i,j)$ and take $f_{ii}'$ to be the identity morphism $id_i$ in $\mathcal{C}$, then $C(Ob(\mathcal{C}),｛f_{ij}'｝)
(i,j \in Ob(\mathcal{C}))$ becomes a **subcategory** of $\mathcal{C}$.

## Composition of Thin Subcategories

Next, suppose $\mathcal{C}$ contains two thin subcategories $\mathcal{C}(Ob(\mathcal{C}),f)$ and $\mathcal{C}(Ob(\mathcal{C}), g)$.

For any objects $i,i',j,j',k,k',l,l',m,m'$ in $\mathcal{C}$, collect all morphisms that can be expressed as a finite composite of morphisms of the form $g_{jk} \circ f_{ij}$, $f_{j'k'} \circ g_{i'j'}$, $f_{lm}$, and $g_{l'm'}$. Let $\{f,g\}$ denote this collection of morphisms. Then we obtain a subcategory of $\mathcal{C}$ with objects $Ob(\mathcal{C})$ and morphisms $\{f,g\}$.

We call this (as a term coined in this paper) the **composite category** of $\mathcal{C}(Ob(\mathcal{C}),f)$ and $\mathcal{C}(Ob(\mathcal{C}),g)$.

## Mutually Prime Thin Categories and Direct Sum Decomposition

**Definition** (Term coined in this paper)  
Two thin categories $\mathcal{C}(A,f)$ and $\mathcal{C}(A,g)$ with the same objects are said to be **mutually prime** if, for $i \neq j$, either $f_{ij}$ does not exist, or $g_{ij}$ does not exist, or $f_{ij} \neq g_{ij}$, and for $i = j$, we have $f_{ii} = g_{ii} = \mathrm{id}_i$.

When $\mathcal{C}$ is the composite category of two mutually prime thin subcategories $\mathcal{C}(Ob(\mathcal{C}),f)$ and $\mathcal{C}(Ob(\mathcal{C}),g)$, we say that $\mathcal{C}$ is **directly sum decomposed** by $\mathcal{C}(Ob(\mathcal{C}),f)$ and $\mathcal{C}(Ob(\mathcal{C}),g)$.
