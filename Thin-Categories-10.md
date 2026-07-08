**[Back to Table of Contents](../README.md)**

# Thin Categories (10)  
Connected Components of (Thin) Categories

Fix an arbitrary locally small category $\mathcal{C}$.

## Equivalence Relation Defining Connected Components

For any $i,j \in Ob(\mathcal{C})$, define the (generalized) relation $iSj$ by  
"there exists a finite sequence of objects $i=x_0, x_1, \dots, x_n=j$ such that for each $t=1,\dots,n$, there is a morphism from $x_{t-1}$ to $x_t$ or from $x_t$ to $x_{t-1}$."

This relation satisfies the conditions of an equivalence relation:

1. If $\mathcal{C}$ is non-empty, then $iSi$ holds for every $i \in Ob(\mathcal{C})$.
2. For any $i,j \in Ob(\mathcal{C})$, $iSj$ implies $jSi$.
3. For any $i,j,k \in Ob(\mathcal{C})$, if $iSj$ and $jSk$, then $iSk$.

**Proof**  
1. Follows from the existence of the identity morphism (the sequence $i \to i$).  
2. Reverse the given sequence.  
3. Concatenate the two sequences. (Proof complete)

The equivalence class
$[i] := \{j \in Ob(\mathcal{C}) \mid iSj\}$
is called the **connected component containing $i$**.

The basic properties of these equivalence classes are
$Ob(\mathcal{C}) = \bigcup_{i \in Ob(\mathcal{C})} [i], \quad [i] \cap [j] \neq \emptyset \iff [i] = [j].$

For each $i \in Ob(\mathcal{C})$, we can define a subcategory $\mathcal{C}_{[i]}$ of $\mathcal{C}$ whose objects are the elements of $[i]$ and whose morphisms are all morphisms $f : i' \to j'$ with $i',j' \in [i]$.

## Correspondence of Connected Components via Functors

Suppose $F : \mathcal{C} \to \mathcal{D}$ is a functor between locally small categories.

Define $F[i] := ｛F(i') \mid i' \in [i]｝$. Then similarly,
$F(Ob(\mathcal{C})) = \bigcup_{i \in Ob(\mathcal{C})} F[i], \quad F[i] \cap F[j] \neq \emptyset \iff F[i] = F[j].$

Define a map $\Phi$ from the collection of connected components of $\mathcal{C}$ to that of $F(\mathcal{C})$ by $\Phi([i]) = F[i]$. This is a well-defined function.

**Proof**  
Assume $[i]=[j]$. For any $i',j' \in [i]=[j]$, there exists a finite sequence connecting $i'$ to $j'$ with the required property. Since $F$ is a functor, applying $F$ yields a corresponding sequence in $F(\mathcal{C})$, showing $F(i'), F(j') \in F[i] = F[j]$. Thus $[i]=[j]$ implies $F[i]=F[j]$, so $\Phi$ is well-defined. (Proof complete)

## Proposition 10-1

**Proposition 10-1**  
If $F$ is full, then the collections of connected components of $\mathcal{C}$ and of $F(\mathcal{C})$ are in bijection (as classes).

**Proof**  
It suffices to show that $\Phi$ has an inverse. Assume $F[i]=F[j]$. For any $F(i'),F(j') \in F[i]=F[j]$, the fullness of $F$ lifts the connecting sequence back to $\mathcal{C}$, yielding $[i]=[j]$. (Proof complete)

## Proposition 10-2

**Proposition 10-2**  
If $F: \mathcal{C} \to \mathcal{D}$ is a full and essentially surjective functor, then the collections of connected components of $\mathcal{C}$ and of $\mathcal{D}$ are in bijection (as classes).

**Proof**  
Since $F$ is essentially surjective, for every $k \in \mathcal{D}$ there exists $i \in \mathcal{C}$ such that $k \in F[i]$. Thus $\mathcal{D} = \bigcup F[i]$. Applying Proposition 10-1 yields the result. (Proof complete)

## Corollary 10-1

**Corollary 10-1**  
If $F: \mathcal{C} \to \mathcal{D}$ is an equivalence, then the collections of connected components of $\mathcal{C}$ and of $\mathcal{D}$ are in bijection (as classes).

**Proof**  
An equivalence is a full and essentially surjective functor. (Proof complete)

## Case When $\mathcal{D}$ Is Thin

When $\mathcal{D}$ is thin, we can examine what the connected components look like.

- If $F$ is the packed arrows functor, then $F(\mathcal{C})$ is strongly connected, so it has only one connected component.
- If $F$ is the standard thinning functor from "Thin Categories (5)", then $F$ is full, so the collections of connected components of $\mathcal{C}$ and $F(\mathcal{C})$ are in bijection.

To compare $\mathcal{C}$ and $F(\mathcal{C})$ more finely from a topological viewpoint, one might consider the classifying space of the nerve or the Alexandrov topology, but we will not discuss that in this paper.




