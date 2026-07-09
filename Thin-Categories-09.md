**[Back to Table of Contents](README.md)**

# Thin Categories (9)  
Constructing a Skeletal Thin Category from an Arbitrary Locally Small Category

Fix an arbitrary locally small category $\mathcal{C}$.

## Definition of the Equivalence Relation $S$

For any $i,j \in Ob(\mathcal{C})$, define the (generalized) relation $iSj$ by
$Hom(i,j) \neq \emptyset \quad \text{and} \quad Hom(j,i) \neq \emptyset.$
This relation satisfies the conditions of an equivalence relation:

1. If $\mathcal{C}$ is non-empty, then $iSi$ holds for every $i \in Ob(\mathcal{C})$.
2. For any $i,j \in Ob(\mathcal{C})$, $iSj$ implies $jSi$.
3. For any $i,j,k \in Ob(\mathcal{C})$, if $iSj$ and $jSk$, then $iSk$.

**Proof**  
1. Follows from the existence of identity morphisms: $Hom(i,i) \neq \emptyset$.  
2. Obvious.  
3. If $Hom(i,j) \neq \emptyset$, $Hom(j,i) \neq \emptyset$, $Hom(j,k) \neq \emptyset$, and $Hom(k,j) \neq \emptyset$, then there exist morphisms $f_1:i\to j$, $f_2:j\to i$, $g_1:j\to k$, $g_2:k\to j$. Thus $g_1\circ f_1:i\to k$ and $g_2\circ f_2:k\to i$ exist, so $Hom(i,k) \neq \emptyset$ and $Hom(k,i) \neq \emptyset$. (Proof complete)

The quotient class $Ob(\mathcal{C})/S$ is then formed from the equivalence classes
$[i] := ｛j \in Ob(\mathcal{C}) \mid iSj｝.$

## Construction of a Skeletal Thin Category

Following the standard construction of thin categories in "Thin Categories (5)", we define morphisms as follows.

For any $i,j \in Ob(\mathcal{C})$, if $Hom(i,j)$ is non-empty, choose any one element and designate it as the unique morphism $f_{[i][j]}$ between $[i]$ and $[j]$.  
If $Hom(i,j)$ is empty, then $f_{[i][j]}$ does not exist.

Then $\mathcal{C}(Ob(\mathcal{C})/S, ｛f_{[i][j]}｝(i,j \in Ob(\mathcal{C}))$ is a thin category.

**Proof**  
1. For any $i \in Ob(\mathcal{C})$, $Hom(i,i)$ is non-empty (by the existence of identities), so $f_{[i][i]}$ exists.  
2. If $f_{[i][j]}$ and $f_{[j][k]}$ exist, then $Hom(i,j)$ and $Hom(j,k)$ are both non-empty, so $Hom(i,k)$ is also non-empty. Thus, by definition, there exists a unique morphism $f_{[i][k]}$. That is, the composition $f_{[j][k]} \circ f_{[i][j]} := f_{[i][k]}$ is well-defined.

From 1 and 2, $f_{[i][j]}$ satisfies the conditions of Definition in "Thin Categories (1)", so $\mathcal{C}(Ob(\mathcal{C})/S, ｛f_{[i][j]}｝(i,j \in Ob(\mathcal{C}))$ is a thin category. (Proof complete)

Moreover, by definition, if both $f_{[i][j]}$ and $f_{[j][i]}$ exist, then $[i] = [j]$. That is, this category is **skeletal**.

When $\mathcal{C}$ is a small category, this becomes a partially ordered set.

## Thinning Functor

Using the above construction, define a map on objects by $T(i) = [i]$ and on morphisms by $T(f : i \to j) = f_{[i][j]}$. This yields a natural thinning functor
$T : \mathcal{C} \to \mathcal{C}(Ob(\mathcal{C})/S, ｛f_{[i][j]}｝(i,j \in Ob(\mathcal{C})).$
That $T$ is a functor follows from Proposition 3-1 in "Thin Categories (3)".

## Strongly Connected Version

Furthermore, defining
$h_{[i][j]} := ｛Hom(i',j') \mid i' \in [i] \text{ and } j' \in [j]｝$
as morphisms yields a strongly connected thin category $\mathcal{C}(Ob(\mathcal{C})/S, h)$.

**Proof**  
First, we show uniqueness of the morphism $h_{[i][j]}$, i.e., if $[i_1]=[i_2]$ and $[j_1]=[j_2]$, then $h_{[i_1][j_1]} = h_{[i_2][j_2]}$.

Let $Hom(i',j')$ be any element with $i' \in [i_1]$ and $j' \in [j_1]$. Then the conditions
$Hom(i_1,i') \neq \emptyset,\ Hom(i',i_1) \neq \emptyset,\ Hom(j_1,j') \neq \emptyset,\ Hom(j',j_1) \neq \emptyset$
and
$Hom(i_1,i_2) \neq \emptyset,\ Hom(i_2,i_1) \neq \emptyset,\ Hom(j_1,j_2) \neq \emptyset,\ Hom(j_2,j_1) \neq \emptyset$
imply
$Hom(i_2,i') \neq \emptyset,\ Hom(i',i_2) \neq \emptyset,\ Hom(j_2,j') \neq \emptyset,\ Hom(j',j_2) \neq \emptyset.$

Thus $i' \in [i_2]$ and $j' \in [j_2]$, so $Hom(i',j') \in h_{[i_2][j_2]}$, which shows $h_{[i_1][j_1]} \subseteq h_{[i_2][j_2]}$. The reverse inclusion follows similarly. Hence $h_{[i_1][j_1]} = h_{[i_2][j_2]}$.

Moreover, for any $i,j \in Ob(\mathcal{C})$, the set $h_{[i][j]}$ exists (even if empty), so the category is strongly connected. (Proof complete)

In particular, when $\mathcal{C}$ is a small category, $\mathcal{C}(Ob(\mathcal{C})/S, h)$ is a totally ordered set.
