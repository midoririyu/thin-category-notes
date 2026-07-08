**[Back to Table of Contents](../README.md)**

# Thin Categories (6)  
Constructing a New Thin Category by Imposing a Relation on Collections of Morphisms in a Thin Category

Fix an arbitrary class $A$.

## Definition and Properties of the Relation $\prec$

For thin categories $\mathcal{C}(A,f)$ and $\mathcal{C}(A,g)$, we write $f \prec g$ if $g_{ij}$ is defined whenever $f_{ij}$ is defined, for all $i,j \in A$.

This (generalized) relation $\prec$ satisfies the following properties:

1. $f \prec f$ (reflexivity)
2. If $f \prec g$ and $g \prec h$, then $f \prec h$ (transitivity)
3. If $\mathcal{C}(A,g)$ is strongly connected, then $f \prec g$ for any $\mathcal{C}(A,f)$.
4. If $\mathcal{C}(A,g)$ is discrete (i.e., $g_{ij}$ exists only when $i=j$, as the identity), then $g \prec f$ for any $\mathcal{C}(A,f)$.

(The proofs of 1–4 follow directly from the definition of $\prec$.)

Let $H_A$ be the collection of all possible "collections of morphisms" on $A$ (i.e., $H_A = \{f \mid f = \{f_{ij}\}_{i,j \in A}\}$).  
Since $\prec$ satisfies properties 1 and 2, we can apply Example 5 from "Thin Categories (1)" to obtain a thin category $\mathcal{C}(H_A, \prec)$.

By properties 3 and 4, in the category $\mathcal{C}(H_A, \prec)$, a discrete collection of morphisms $f$ is an **initial object**, and a strongly connected collection of morphisms $f$ is a **terminal object**.

## Induced Functor $\bar{F}$

Fix arbitrary classes $A$ and $B$. Suppose that for each $f,f' \in H_A$ and $g,g' \in H_B$, there exist full functors $F : \mathcal{C}(A,f) \to \mathcal{C}(B,g)$ and $F' : \mathcal{C}(A,f') \to \mathcal{C}(B,g')$.

We define a functor $\bar{F} : \mathcal{C}(H_A, \prec) \to \mathcal{C}(H_B, \prec)$ by
$$
\bar{F}(f) := F(f) = \{g_{F(i)F(j)}\}_{i,j \in A}, \quad \bar{F}(\prec_{ff'}) := \prec_{F(f)F'(f')}.
$$

First, since $F$ is a functor, for every $f_{ij}$ there exists $g_{F(i)F(j)}$, so $\bar{F}(f)$ is well-defined.

Furthermore, if $f_{ij}$ exists for all relevant $i,j$, and $f'_{ij}$ exists whenever $f_{ij}$ does, then by fullness of $F$, $f'_{ij}$ exists whenever $g_{F(i)F(j)}$ does, and by functoriality of $F'$, $g'_{F'(i)F'(j)}$ also exists. This shows that $\bar{F}(\prec_{ff'})$ is well-defined.

## Proposition 6-1

**Proposition 6-1**  
For any $g \in H_B$, suppose there exists a full and essentially surjective functor $F : \mathcal{C}(A,f) \to \mathcal{C}(B,g)$ with $f \in H_A$. Then $\bar{F} : \mathcal{C}(H_A, \prec) \to \mathcal{C}(H_B, \prec)$ is an equivalence.

**Proof**  
We show that $\bar{F}$ is a fully faithful and essentially surjective functor.

**(Faithfulness)**  
Since $\mathcal{C}(H_A, \prec)$ is thin, by Proposition 3-3-1 in "Thin Categories (3)", $\bar{F}$ is faithful.

**(Fullness)**  
By assumption, for $g \prec g'$ in $H_B$, there exist full functors $F,F'$ and $f,f' \in H_A$ such that for all $i,j \in A$,
$$
g_{F(i)F(j)} = F(f_{ij}), \quad g'_{F'(i)F'(j)} = F'(f'_{ij}).
$$
Thus, whenever $F(f)_{ij}$ exists, if $F'(f')_{ij}$ exists, we can choose $f,f'$ such that $f_{ij}$ exists precisely when $f'_{ij}$ does. This shows that $\bar{F}$ is full.

**(Essential Surjectivity)**  
Since $F$ is essentially surjective, for any $g_{kl}$ in $B$, there exist $i,j \in A$ such that $g_{kF(i)}$ and $g_{lF(j)}$ exist. By functoriality of $F$, $g_{F(i)F(j)}$ exists. This shows the existence of $\prec_{g \bar{F}(f)}$.

Conversely, by functoriality of $F$, for any $i,j \in A$ we can take $k = F(i)$ and $l = F(j)$. Thus if $g_{F(i)F(j)}$ exists, then $g_{kl} = g_{F(i)F(j)}$ exists, showing the existence of $\prec_{\bar{F}(f) g}$. Hence $\bar{F}$ is essentially surjective.

Therefore, $\bar{F}$ is fully faithful and essentially surjective, so it is an equivalence. (Proof complete)

## Corollary 6-1

**Corollary 6-1**  
For any $g \in H_B$, suppose there exists an equivalence $F : \mathcal{C}(A,f) \to \mathcal{C}(B,g)$ with $f \in H_A$. Then $\bar{F} : \mathcal{C}(H_A, \prec) \to \mathcal{C}(H_B, \prec)$ is an equivalence.

**Proof**  
Since an equivalence is essentially surjective, the result follows from Proposition 6-1. (Proof complete)
