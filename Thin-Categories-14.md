**[Back to Table of Contents](README.md)**

# Thin Categories (14)  
Coends and Ends in Thin Categories and Their Properties

First, we recall the definition of a coend (or co-integral) in a general category.

## Definition of Coend (in General Categories)

For a functor $S: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$, the **coend** $\int^c S(c,c)$ consists of an object $d \in Ob(\mathcal{D})$ and a family of morphisms $\omega_c: S(c,c) \to d$ indexed by objects (called a **co-wedge** or **dinatural transformation**), satisfying the following two conditions:

- **Co-wedge condition**: For every morphism $f: c \to c'$ in $\mathcal{C}$, the following diagram commutes:
  $\omega_{c'} \circ S(c,f) = \omega_c \circ S(f,c').$
- **Universal property**: For any object $d' \in Ob(\mathcal{D})$ and any co-wedge $\omega'_c: S(c,c) \to d'$, there exists a unique morphism $h: d \to d'$ such that $\omega'_c = h \circ \omega_c$ for all $c \in Ob(\mathcal{C})$.

## Coend in Thin Categories

When the target category $\mathcal{D}$ is thin, morphisms between any two objects are unique when they exist. Therefore, the commutativity condition is automatically satisfied as long as the relevant morphisms exist.

Thus, the definition of a coend in a thin category can be simplified as follows:

**Definition**  
An object $d \in Ob(\mathcal{D})$ is a coend $\int^c S(c,c)$ if it satisfies the following two conditions:

1. For every $c \in Ob(\mathcal{C})$, there exists a morphism $S(c,c) \to d$.
2. For any object $d' \in Ob(\mathcal{D})$, if there exists a morphism $S(c,c) \to d'$ for every $c \in Ob(\mathcal{C})$, then there exists a morphism $d \to d'$.

## Proposition 14-1

**Proposition 14-1**  
Let $\mathcal{D}$ be a thin locally small category. For a functor $S: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$, define the subclass $B \subseteq Ob(\mathcal{D})$ by
$B = ｛ S(c,c) \mid c \in Ob(\mathcal{C})｝.$

If the supremum $\sup B$ exists in $\mathcal{D}$ (choosing one if there are multiple), then $d = \sup B$ is isomorphic to the coend $\int^c S(c,c)$ of the functor $S$. If $\sup B$ does not exist, then the coend is not defined.

**Proof**  
We verify that $\sup B$ satisfies the simplified definition of a coend in thin categories, using the upper bound and least upper bound properties.

**Step 1: Co-wedge condition (upper bound property)**  
Let $d = \sup B$. By the upper bound property, there is a morphism from every element of $B$ to $d$. Since elements of $B$ are of the form $S(c,c)$, this means that for every $c \in Ob(\mathcal{C})$, there exists a morphism $S(c,c) \to d$. This satisfies condition 1 of the simplified definition.

**Step 2: Universal property (least upper bound property)**  
Let $d' \in Ob(\mathcal{D})$ be another co-wedge, i.e., suppose there exists a morphism $S(c,c) \to d'$ for every $c \in Ob(\mathcal{C})$. This means $d'$ is an upper bound of $B$. By the least upper bound property of $d = \sup B$, there exists a morphism $d \to d'$. Since $\mathcal{D}$ is thin, this morphism is unique, satisfying condition 2 of the simplified definition.

Thus $\sup B$ satisfies the conditions for a coend. If another coend exists, the universal property implies they are isomorphic:
$\int^c S(c,c) \cong \sup B.$
Conversely, if a coend exists but $\sup B$ does not, it would contradict the argument above. Hence, if $\sup B$ does not exist, neither does the coend. (Proof complete)

## Propositions on Integration in Thin Categories

We now show that analogous results to those in Lebesgue integration theory also hold in thin categories.

For simplicity, we write “there exists a morphism $a \to b$” simply as “$a \to b$”. We also use notation such as $\sup_i b_i := \sup｛b_i \in \mathcal{C} \mid i \in I｝$.

**Proposition 14-2** (Fatou’s Lemma analogue)  
$\int^c \sup_n \inf_{k \geq n} S_k(c,c) \to \sup_n \inf_{k \geq n} \int^c S_k(c,c).$

(In terms of the order $\leq$, this corresponds to $\int^c \liminf S_k(c,c) \leq \liminf \int^c S_k(c,c)$.)

**Proof of Proposition 14-2**

In a thin category, $\int^c (\cdot) \cong \sup_c (\cdot)$. Therefore, the domain of the desired morphism is $\sup_c \sup_n \inf_{k \geq n} S_k(c,c)$, and the codomain is $\sup_n \inf_{k \geq n} \sup_c S_k(c,c)$.

First, we recall a basic property of  infima (monotonicity / preservation of morphisms):

For any $a \in A$ and $b \in B$, if $a \to b$, then $\inf A \to \inf B$.

(Proof.)Since $ \inf A \to a$ (by the lower bound property), so $\inf A \to b$ by composition. Then, by the greatest lower bound property of $\inf B$, we have $\inf A \to \inf B$.  (Proof of property is completed)

For any $c' \in \mathcal{C}$, we have $S_k(c',c') \to \sup_c S_k(c,c)$. By the property of infima above,

$\inf_{k \geq n} S_k(c',c') \ \to \ \inf_{k \geq n} \sup_c S_k(c,c).$

Taking the supremum over $c' \in \mathcal{C}$ yields

$\sup_{c'} \inf_{k \geq n} S_k(c',c') \ \to \ \inf_{k \geq n} \sup_c S_k(c,c).$

Finally, taking the supremum over $n$ gives the desired morphism.  
(Proof of Proposition 14-2 is completed)

### Basic Lemma (Exchange and Associativity of Suprema)

For index classes $I$ and $J$,

$\sup_{(i,j) \in I \times J} a_{i,j} \ \cong \ \sup_{i \in I} \sup_{j \in J} a_{i,j}.$

**Proof of the Basic Lemma**
By the upper bound property, for any $i,j$ we have the chain $a_{i,j} \to \sup_j a_{i,j} \to \sup_i \sup_j a_{i,j}$. By the least upper bound property, $\sup_{(i,j)} a_{i,j} \to \sup_i \sup_j a_{i,j}$.

Conversely, $a_{i,j} \to \sup_{(i,j)} a_{i,j}$. Taking the supremum first over $j$ for fixed $i$ gives $\sup_j a_{i,j} \to \sup_{(i,j)} a_{i,j}$. Then taking the supremum over $i$ yields $\sup_i \sup_j a_{i,j} \to \sup_{(i,j)} a_{i,j}$.

Since morphisms exist in both directions, the two objects are isomorphic.  (Proof of the Basic Lemma is completed)

**Proposition 14-3** (Lebesgue’s Dominated Convergence Theorem analogue)  
For functors $F_i: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$ indexed by $i \in I$,
$\sup_i \int^c F_i(c,c) \cong \int^c \sup_i F_i(c,c).$

**Proof of Proposition 14-3**
In a thin category, $\int^c (\cdot) \cong \sup_c (\cdot)$. By the Basic Lemma, suprema can be freely exchanged and associated. Therefore, the two sides are isomorphic.  (Proof  complete)


**Proposition 14-4** (Fubini’s Theorem analogue)  
$\int^{(x,y)} F(x,y,x,y) \cong \int^x \int^y F(x,y,x,y) \cong \int^y \int^x F(x,y,x,y).$

**Proof of Proposition 14-4**
Rewriting coends as suprema, the statement becomes
$\sup_{(x,y)} F(x,y,x,y) \ \cong \ \sup_x \sup_y F(x,y,x,y) \ \cong \ \sup_y \sup_x F(x,y,x,y),$

which is a direct consequence of the Basic Lemma.  (Proof  complete)


## The Case of Ends

The definition of an **end** $\int_c S(c,c)$ in a thin category can also be simplified.

An object $d \in Ob(\mathcal{D})$ is an end if it satisfies the following two conditions:

- **Lower bound property**: For every $c \in Ob(\mathcal{C})$, there exists a morphism $d \to S(c,c)$.
- **Greatest lower bound property**: For any object $d' \in Ob(\mathcal{D})$, if there exists a morphism $d' \to S(c,c)$ for every $c \in Ob(\mathcal{C})$, then there exists a morphism $d' \to d$.

**Proposition 14-5**  
Let $\mathcal{D}$ be a thin locally small category. For a functor $S: \mathcal{C}^{\mathrm{op}} \times \mathcal{C} \to \mathcal{D}$, let $B = ｛S(c,c) \mid c \in Ob(\mathcal{C})｝$. If the infimum $\inf B$ exists in $\mathcal{D}$, then $\int_c S(c,c) \cong \inf B$. If $\inf B$ does not exist, the end is not defined.

**Proposition 14-6** (Fatou’s Lemma for Ends)  
$\inf_n \sup_{k \geq n} \int_c S_k(c,c) \to \int_c \inf_n \sup_{k \geq n} S_k(c,c).$

(In terms of the order $\leq$, this corresponds to $\limsup \int_c S_k(c,c) \leq \int_c \limsup S_k(c,c)$.)

**Proposition 14-7** (Lebesgue’s Convergence Theorem for Ends)  
$\inf_i \int_c F_i(c,c) \cong \int_c \inf_i F_i(c,c).$

**Proposition 14-8** (Fubini’s Theorem for Ends)  
$\int_{(x,y)} F(x,y,x,y) \cong \int_x \int_y F(x,y,x,y) \cong \int_y \int_x F(x,y,x,y).$


### Coends and Ends Order Interchange in Thin Categories

In thin categories, the following holds for interchanging the order of coends and ends:

**Proposition 14-9**(Weak Duality in Thin Categories)

$\int^y \int_x F(x,y,x,y) \to \int_x \int^y F(x,y,x,y).$

When morphisms are represented by the order relation $\leq$, this becomes  
$\int^y \int_x F(x,y,x,y) \leq \int_x \int^y F(x,y,x,y).$

**Proof**  
It suffices to show that  $\sup_y \inf_x F(x,y,x,y) \to \inf_x \sup_y F(x,y,x,y).$
Fix arbitrary $x'$ and $y'$.

By the lower bound property of the infimum,  
$\inf_x F(x,y',x,y') \to F(x',y',x',y').$

By the upper bound property of the supremum,  
$F(x',y',x',y') \to \sup_y F(x',y,x',y).$

Composing these gives  $\inf_x F(x,y',x,y') \to \sup_y F(x',y,x',y).$

Since $x'$ is arbitrary, $\inf_x F(x,y',x,y')$ is one of the lower bounds of the family $｛\sup_y F(x',y,x',y)|x'｝$.  

Therefore, by the greatest lower bound property of the infimum,  
$\inf_x F(x,y',x,y') \to \inf_{x'} \sup_y F(x',y,x',y).$

Furthermore, $\inf_{x'} \sup_y F(x',y,x',y)$ is one of the upper bounds of the family $｛\inf_x F(x,y',x,y')|y'｝$.  

Thus, by the least upper bound property of the supremum,  
$\sup_{y'} \inf_x F(x,y',x,y') \to \inf_{x'} \sup_y F(x',y,x',y).$
(Proof complete)

**Proposition 14-10.** (An Example of Strong Duality in Thin Categories)

Suppose that the end and the coend coincide, i.e.,

$\int_x F(x,y,x,y) \ \cong\ \int^x F(x,y,x,y)$ holds.

Then $\int^y \int_x F(x,y,x,y) \ \cong\ \int_x \int^y F(x,y,x,y).$

**Proof**

It suffices to show the existence of a morphism
$\int_x \int^y F(x,y,x,y) \ \to\ \int^y \int_x F(x,y,x,y),$
that is,
$\inf_x \sup_y F(x,y,x,y) \ \to\ \sup_y \inf_x F(x,y,x,y).$

By the universal property of the infimum,
$\inf_x \sup_y F(x,y,x,y) \ \to\ \sup_x \sup_y F(x,y,x,y).$

By the basic lemma on the interchange of suprema (suprema commute),
$\sup_x \sup_y F(x,y,x,y) \ \cong\ \sup_y \sup_x F(x,y,x,y).$

Moreover, by the assumption, for each fixed $y$ we have $\sup_x F(x,y,x,y) \cong \inf_x F(x,y,x,y)$. 

Therefore, $\sup_y \sup_x F(x,y,x,y) \ \cong\ \sup_y \inf_x F(x,y,x,y).$

Composing these morphisms yields $\inf_x \sup_y F(x,y,x,y) \ \to\ \sup_y \inf_x F(x,y,x,y).$

The morphism in the opposite direction follows from the proposition 14-9.
Thus, morphisms exist in both directions, and we obtain the desired isomorphism.(Proof complete)

**Note**  

The interchange of ends and coends in thin categories, as seen in Propositions 14-9 and 14-10, has interesting connections to duality in optimization theory and von Neumann’s minimax theorem in game theory.

The existence of the morphism $\sup_y \inf_x F \to \inf_x \sup_y F$ shown in Proposition 14-9 is a general fact that holds for any function (or poset-valued function), since $\sup_y \inf_x F \leq \inf_x \sup_y F$ is always true.

On the other hand, the equality shown in Proposition 14-10 does not hold in general. In ordinary analysis, additional structures—such as convexity, continuity, or complete distributivity—are typically required for the equality to hold.
