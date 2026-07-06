**[Back to Table of Contents](../README.md)**

# Thin Categories (7)  
Thinning of Functors

Suppose the following categories and functors are given:

- Locally small categories $\mathcal{C}$ and $\mathcal{D}$
- Thin categories $C_A = \mathcal{C}(A, f)$ and $C_B = \mathcal{C}(B, g)$
- Functor $F: \mathcal{C} \to \mathcal{D}$
- Functors to thin categories $T_1: \mathcal{C} \to C_A$ and $T_2: \mathcal{D} \to C_B$

Given $T = (T_1, T_2)$, we define the functor $T(F): T_1(\mathcal{C}) \to T_2(\mathcal{D})$ as follows.

**On objects**  
For any object $i$ in $\mathcal{C}$,
$$
T(F)(T_1(i)) := T_2(F(i)).
$$

**On morphisms**  
For any morphism $p : i \to j$ in $\mathcal{C}$,
$$
T(F)(f_{T_1(i)T_1(j)}) := g_{T_2(F(i))T_2(F(j))}.
$$

That $T(F)$ is a functor is guaranteed by Proposition 3-1 in "Thin Categories (3)". Moreover, since $T(F)$ is surjective on objects, it is **essentially surjective**, and satisfies
$$
T(F) \circ T_1 = T_2 \circ F.
$$

```tikzcd
\mathcal{C} \ar[r, "F"] \ar[d, "T_1"] & \mathcal{D} \ar[d, "T_2"] \\
T_1(\mathcal{C}) \ar[r, "T(F)"] & T_2(\mathcal{D})

## Example: Thinning via the Packed Arrows Functor

Let $F: \mathcal{C} \to \mathcal{D}$ be a functor between locally small categories. Using the packed arrows functors
$$
P_\mathcal{C} : \mathcal{C} \to P(\mathcal{C}), \quad P_\mathcal{D} : \mathcal{D} \to P(\mathcal{D})
$$
defined in "Thin Categories (4)", set $P = (P_\mathcal{C}, P_\mathcal{D})$. Then the thinning of $F$ by $P$ is the functor
$$
P(F) : P(\mathcal{C}) \to P(\mathcal{D})
$$
given by
$$
P(F)(i) = F(i),\quad P(F)(\operatorname{hom}_\mathcal{C}(i,j)) = \operatorname{hom}_\mathcal{D}(F(i), F(j))
$$
for $i,j \in \operatorname{Ob}(\mathcal{C})$.

Since $P(\mathcal{C})$ is a strongly connected category, by Lemma 3-1 in "Thin Categories (3)", $P(F)$ is always an equivalence, regardless of the choice of $F$.

In particular, when $\mathcal{D}$ is a thin category, by the universal property of the packed arrows functor (Proposition 4-5 in "Thin Categories (4)"), for any thinning functor $F: \mathcal{C} \to \mathcal{D}$ there exists a unique functor $\tilde{F} : P(\mathcal{C}) \to \mathcal{D}$ such that
$$
F = \tilde{F} \circ P_\mathcal{C}.
$$
Looking at the domains and codomains of these functors, we also have
$$
P(F) = \tilde{F} \circ P_\mathcal{D}.
$$

\mathcal{C} \ar[r, "F"] \ar[d, "P_\mathcal{C}"] & \mathcal{D} \ar[d, "P_\mathcal{D}"] \\
P(\mathcal{C}) \ar[r, "P(F)"] \ar[ur, "\tilde{F}"] & P(\mathcal{D})



## General Properties of $T(F)$

**Proposition 7-1**  
If $F$ is an equivalence, then so is $T(F)$.

**Proof**  
By assumption, $F$ is full. Therefore, for any $i,j \in \operatorname{Ob}(\mathcal{C})$, there exists a morphism $p : i \to j$ in $\mathcal{C}$ such that the morphism $F(i) \to F(j)$ in $\mathcal{D}$ is given by $F(p)$.

Then, for any $i,j \in \operatorname{Ob}(\mathcal{C})$,
$$
g_{T_2(F(i))T_2(F(j))} = T_2(F(p)) = (T_2 \circ F)(p) = (T(F) \circ T_1)(p) = T(F)(T_1(p)).
$$
Thus $T(F)$ is full, and hence an equivalence. (Proof complete)

**Proposition 7-2**  
If $F$ is a (left) adjoint functor, then so is $T(F)$.

**Proof**  
Suppose $F: \mathcal{C} \to \mathcal{D}$ is left adjoint to $G: \mathcal{D} \to \mathcal{C}$. Then for every object $i \in \operatorname{Ob}(\mathcal{C})$, there exists a pair $(F(i), \eta_i)$ satisfying the following two conditions:

1. $\eta_i : i \to G(F(i))$ is a morphism in $\mathcal{C}$.
2. For every object $k \in \operatorname{Ob}(\mathcal{D})$ and every morphism $p : i \to G(k)$, there exists a unique morphism $q : F(i) \to k$ in $\mathcal{D}$ such that $p = G(q) \circ \eta_i$.

Let $T' = (T_2, T_1)$. We show that $T(F) : T_1(\mathcal{C}) \to T_2(\mathcal{D})$ is left adjoint to $T'(G) : T_2(\mathcal{D}) \to T_1(\mathcal{C})$.

1. For any object $T_1(i)$ in $T_1(\mathcal{C})$, define
   $$
   \bar{\eta}_{T_1(i)} := T_1(\eta_i) : T_1(i) \to T_1(G(F(i))).
   $$
   Since $T_1(G(F(i))) = T'(G)(T_2(F(i))) = T'(G)(T(F)(T_1(i)))$, $\bar{\eta}_{T_1(i)}$ is a morphism in $T_1(\mathcal{C})$ from $T_1(i)$ to $T'(G)(T(F)(T_1(i)))$.

2. Let $T_2(k)$ be an arbitrary object in $T_2(\mathcal{D})$, and let $\bar{p} : T_1(i) \to T'(G)(T_2(k))$ be an arbitrary morphism. We show that there exists a unique morphism $\bar{q} : T(F)(T_1(i)) \to T_2(k)$ in $T_2(\mathcal{D})$.

   **Existence**: By assumption, there exists a morphism $q : F(i) \to k$ in $\mathcal{D}$. Applying $T_2$, we obtain the morphism $g_{T_2(F(i)), T_2(k)}$ in $T_2(\mathcal{D})$, which we take as $\bar{q}$.

   **Commutativity**: In $T_1(\mathcal{C})$, consider the composite $\bar{p}$ and $T'(G)(\bar{q}) \circ \bar{\eta}_{T_1(i)}$. Since $\mathcal{D}$ (and thus $T_2(\mathcal{D})$) is thin, morphisms are unique when they exist between the same pair of objects. As both composites have the same domain $T_1(i)$ and codomain $T'(G)(T_2(k))$, we have
   $$
   \bar{p} = T'(G)(\bar{q}) \circ \bar{\eta}_{T_1(i)}.
   $$

3. **Uniqueness**: The uniqueness of $\bar{q}$ follows immediately from the fact that $T_2(\mathcal{D})$ is a thin category.

Thus, the pair of functors $(T(F), T'(G))$ satisfies the adjunction $T(F) \dashv T'(G)$. (Proof complete)

**Proposition 7-3**  
If $F$ and $F'$ are naturally isomorphic functors, then so are $T(F)$ and $T(F')$.

**Proof**  
Suppose $F$ and $F'$ are naturally isomorphic. Then for every object $i$ in $\mathcal{C}$, there exist morphisms $\alpha_i : F(i) \to F'(i)$ and $\alpha'_i : F'(i) \to F(i)$ such that for every morphism $f : i \to j$ in $\mathcal{C}$,
$$
\alpha_j \circ F(f) = F'(f) \circ \alpha_i.
$$

Define $T(\alpha_i) : T_2(F(i)) \to T_2(F'(i))$. Then $T(\alpha'_i) : T_2(F'(i)) \to T_2(F(i))$ is its inverse, and both exist by the functoriality of $T_2$. Moreover,
$$
T(\alpha_j) \circ T(F(f)) = T(F'(f)) \circ T(\alpha_i).
$$
This shows that $T(F)$ and $T(F')$ are naturally isomorphic. (Proof complete)





