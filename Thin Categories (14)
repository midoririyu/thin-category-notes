**[Back to Table of Contents](../README.md)**

# Thin Categories (14)  
Coends and Ends in Thin Categories and Their Properties

First, we recall the definition of a coend (or co-integral) in a general category.

## Definition of Coend (in General Categories)

For a functor $S: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$, the **coend** $\int^c S(c,c)$ consists of an object $d \in \operatorname{Ob}(\mathcal{D})$ and a family of morphisms $\omega_c: S(c,c) \to d$ indexed by objects (called a **co-wedge** or **dinatural transformation**), satisfying the following two conditions:

- **Co-wedge condition**: For every morphism $f: c \to c'$ in $\mathcal{C}$, the following diagram commutes:
  $$
  \omega_{c'} \circ S(c,f) = \omega_c \circ S(f,c').
  $$
- **Universal property**: For any object $d' \in \operatorname{Ob}(\mathcal{D})$ and any co-wedge $\omega'_c: S(c,c) \to d'$, there exists a unique morphism $h: d \to d'$ such that $\omega'_c = h \circ \omega_c$ for all $c \in \operatorname{Ob}(\mathcal{C})$.

## Coend in Thin Categories

When the target category $\mathcal{D}$ is thin, morphisms between any two objects are unique when they exist. Therefore, the commutativity condition is automatically satisfied as long as the relevant morphisms exist.

Thus, the definition of a coend in a thin category can be simplified as follows:

**Definition**  
An object $d \in \operatorname{Ob}(\mathcal{D})$ is a coend $\int^c S(c,c)$ if it satisfies the following two conditions:

1. For every $c \in \operatorname{Ob}(\mathcal{C})$, there exists a morphism $S(c,c) \to d$.
2. For any object $d' \in \operatorname{Ob}(\mathcal{D})$, if there exists a morphism $S(c,c) \to d'$ for every $c \in \operatorname{Ob}(\mathcal{C})$, then there exists a morphism $d \to d'$.

## Proposition 14-1

**Proposition 14-1**  
Let $\mathcal{D}$ be a thin locally small category. For a functor $S: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$, define the subclass $B \subseteq \operatorname{Ob}(\mathcal{D})$ by
$$
B = \{ S(c,c) \mid c \in \operatorname{Ob}(\mathcal{C}) \}.
$$

If the supremum $\sup B$ exists in $\mathcal{D}$ (choosing one if there are multiple), then $d = \sup B$ is isomorphic to the coend $\int^c S(c,c)$ of the functor $S$. If $\sup B$ does not exist, then the coend is not defined.

**Proof**  
We verify that $\sup B$ satisfies the simplified definition of a coend in thin categories, using the upper bound and least upper bound properties.

**Step 1: Co-wedge condition (upper bound property)**  
Let $d = \sup B$. By the upper bound property, there is a morphism from every element of $B$ to $d$. Since elements of $B$ are of the form $S(c,c)$, this means that for every $c \in \operatorname{Ob}(\mathcal{C})$, there exists a morphism $S(c,c) \to d$. This satisfies condition 1 of the simplified definition.

**Step 2: Universal property (least upper bound property)**  
Let $d' \in \operatorname{Ob}(\mathcal{D})$ be another co-wedge, i.e., suppose there exists a morphism $S(c,c) \to d'$ for every $c \in \operatorname{Ob}(\mathcal{C})$. This means $d'$ is an upper bound of $B$. By the least upper bound property of $d = \sup B$, there exists a morphism $d \to d'$. Since $\mathcal{D}$ is thin, this morphism is unique, satisfying condition 2 of the simplified definition.

Thus $\sup B$ satisfies the conditions for a coend. If another coend exists, the universal property implies they are isomorphic:
$$
\int^c S(c,c) \cong \sup B.
$$
Conversely, if a coend exists but $\sup B$ does not, it would contradict the argument above. Hence, if $\sup B$ does not exist, neither does the coend. (Proof complete)

## Propositions on Integration in Thin Categories

We now show that analogous results to those in Lebesgue integration theory also hold in thin categories.

For simplicity, we write “there exists a morphism $a \to b$” simply as “$a \to b$”. We also use notation such as $\sup_i b_i := \sup\{b_i \in \mathcal{C} \mid i \in I\}$.

**Proposition 14-2** (Fatou’s Lemma analogue)  
$$
\int^c \sup_n \inf_{k \geq n} S_k(c,c) \to \sup_n \inf_{k \geq n} \int^c S_k(c,c).
$$
(In terms of the order $\leq$, this corresponds to $\int^c \liminf S_k(c,c) \leq \liminf \int^c S_k(c,c)$.)

**Proposition 14-3** (Lebesgue’s Dominated Convergence Theorem analogue)  
For functors $F_i: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$ indexed by $i \in I$,
$$
\sup_i \int^c F_i(c,c) \cong \int^c \sup_i F_i(c,c).
$$

**Proposition 14-4** (Fubini’s Theorem analogue)  
$$
\int^{(x,y)} F(x,y,x,y) \cong \int^x \int^y F(x,y,x,y) \cong \int^y \int^x F(x,y,x,y).
$$

(These follow from the interchange law for suprema: $\sup_i \sup_j a_{ij} \cong \sup_{(i,j)} a_{ij}$.)

## The Case of Ends

The definition of an **end** $\int_c S(c,c)$ in a thin category can also be simplified.

An object $d \in \operatorname{Ob}(\mathcal{D})$ is an end if it satisfies the following two conditions:

- **Lower bound property**: For every $c \in \operatorname{Ob}(\mathcal{C})$, there exists a morphism $d \to S(c,c)$.
- **Greatest lower bound property**: For any object $d' \in \operatorname{Ob}(\mathcal{D})$, if there exists a morphism $d' \to S(c,c)$ for every $c \in \operatorname{Ob}(\mathcal{C})$, then there exists a morphism $d' \to d$.

**Proposition 14-5**  
Let $\mathcal{D}$ be a thin locally small category. For a functor $S: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$, let $B = \{S(c,c) \mid c \in \operatorname{Ob}(\mathcal{C})\}$. If the infimum $\inf B$ exists in $\mathcal{D}$, then $\int_c S(c,c) \cong \inf B$. If $\inf B$ does not exist, the end is not defined.

**Proposition 14-6** (Fatou’s Lemma for Ends)  
$$
\inf_n \sup_{k \geq n} \int_c S_k(c,c) \to \int_c \inf_n \sup_{k \geq n} S_k(c,c).
$$

**Proposition 14-7** (Lebesgue’s Convergence Theorem for Ends)  
$$
\inf_i \int_c F_i(c,c) \cong \int_c \inf_i F_i(c,c).
$$

**Proposition 14-8** (Fubini’s Theorem for Ends)  
$$
\int_{(x,y)} F(x,y,x,y) \cong \int^x \int^y F(x,y,x,y) \cong \int^y \int^x F(x,y,x,y).
$$
