**[Back to Table of Contents](../README.md)**

# Thin Categories (3)  
Properties of Functors from Locally Small Categories to Thin Categories (Thinning Functors), Natural Transformations, and Functor Categories

We consider functors from a locally small category $\mathcal{C}$ to a thin category $C(B,g)$ (so-called **thinning functors**).

## Proposition 3-1

**Proposition 3-1**  
A functor $T$ from a locally small category $\mathcal{C}$ to a thin category $C(B,g)$ exists if and only if there is a map $T: \rm{Ob}(\mathcal{C}) \to B$ and for every $i,j \in \rm{Ob}(\mathcal{C})$, the morphism $g_{T(i)T(j)}$ exists in $C_B$.

**Proof**  
Necessity is clear, so we show sufficiency.

By assumption, for each $i \in \rm{Ob}(\mathcal{C})$ there is a unique $T(i) \in B$, and for every $i,j \in \rm{Ob}(\mathcal{C})$, $g_{T(i)T(j)}$ exists.

Let $\rm{hom}(\mathcal{C})$ be the class of all morphisms in $\mathcal{C}$. Define
$T : \rm{hom}(\mathcal{C}) \to \rm{hom}(C_B), \quad T(f : i \to j) := g_{T(i)T(j)}.$
This is a well-defined map.

**(Well-definedness)**  
If $f_1 : i \to j$ and $f_2 : k \to l$ are the same morphism in $\rm{hom}(\mathcal{C})$, then $i = k$ and $j = l$, so $T(i) = T(k)$ and $T(j) = T(l)$. By uniqueness of morphisms in thin categories, $g_{T(i)T(j)} = g_{T(k)T(l)}$, hence $T(f_1) = T(f_2)$.

Moreover, this $T$ preserves composition and identity morphisms.

**(Proof)**  
$T(f_2 : j \to m) \circ T(f_1 : i \to j) = g_{T(j)T(m)} \circ g_{T(i)T(j)} = g_{T(i)T(m)} = T(f_2 \circ f_1 : i \to m)$
and
$T(f : i \to i) = g_{T(i)T(i)}.$
(End of proof of Proposition 3-1)

## Proposition 3-2

**Proposition 3-2**  
A functor $T$ from a thin small category $C_A$ to a thin small category $C_B$ exists if and only if there is a monotone map $T$ between the preordered sets $A$ and $B$.

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
$T$ is faithful if $T(f_1) = T(f_2)$ implies $f_1 = f_2$ for morphisms $f_1, f_2 : i \to j$. Since $C(B,g)$ is thin, $T(f_1) = g_{T(i)T(j)} = T(f_2)$ always holds. Thus $\rm{hom}(i,j)$ is at most a singleton, so $\mathcal{C}$ is thin.

**(Sufficiency)**  
Suppose $T$ is not faithful. Then there exist $f_1 \neq f_2 : i \to j$ with $T(f_1) = T(f_2)$, contradicting that $\mathcal{C}$ is thin. (Proof complete)

**Proof of Proposition 3-3-2**  
$T$ is full if for every $g_{T(i)T(j)}$ there exists $f : i \to j$ such that $T(f) = g_{T(i)T(j)}$. Since $\mathcal{C}$ is strongly connected, such an $f$ always exists. (Proof complete)

## Lemma 3-1

**Lemma 3-1**  
A functor $T : \mathcal{C} \to C(B,g)$ from a locally small category $\mathcal{C}$ is an equivalence if $\mathcal{C}$ is a strongly connected thin category and $T$ is essentially surjective.

**Proof**  
It is well-known that a functor is an equivalence if and only if it is fully faithful and essentially surjective. Applying Proposition 3-3 yields the result. (Proof complete)

## Proposition 3-4

**Proposition 3-4**  
Thin small categories $C_A$ and $C_B$ are equivalent if and only if there is a monotone map $T : A \to B$ between the preordered sets $A$ and $B$ satisfying:

- If $T(i) \leq T(j)$, then $i \leq j$.
- For every $k \in B$, there exists $i \in A$ such that $k \leq T(i)$ and $T(i) \leq k$.

**Proof**  
Combine the characterization of equivalences with Proposition 3-2 and Proposition 3-3-1. (Proof complete)

**Corollary 3-1**  
Skeletal thin small categories $C_A$ and $C_B$ are equivalent if and only if there is a bijective monotone map $T : A \to B$ between the partially ordered sets $A$ and $B$.

**Proof**  
Apply the antisymmetry condition $i \leq j$ and $j \leq i$ implies $i = j$ to Proposition 3-4. (Proof complete)

## Preservation of Universal Objects

**Proposition 3-5** (Left Universal Objects)  
Let $T : \mathcal{C} \to C(B,g)$ be a functor from a locally small category $\mathcal{C}$. If $i$ is a (left) universal object in $\mathcal{C}$, then $T(i)$ is a (left) universal object in $T(\mathcal{C})$. In particular, if $T$ is essentially surjective, then $T(i)$ is a (left) universal object in $C(B,g)$.

**Proof**  
First, the definition of a (left) universal object $i$ in a category $\mathcal{C}$ is given as: "there exists a functor $G: \mathcal{C} \to \mathbf{Set}$ that is naturally isomorphic to the $Hom$ functor $h^i = Hom(i, -)$ represented by $i$, and for each object $x$ and any $v \in G(x)$, there uniquely exists a morphism $f \in Hom(i, x)$ such that $G(f)(u) = v$ holds." (Here, $u$ is the universal element in $G(i)$ corresponding to the identity morphism $id_i$ of $h^i$.)  
We show the proposition based on this definition.  

Taking any $x \in \mathrm{Ob}(\mathcal{C})$ such that $Hom(i, x) \neq \emptyset$, the image $Hom(T(i), T(x))$ is also not empty by the properties of a functor. Here, due to the thinness of $T(\mathcal{C})$, this morphism set is a singleton set consisting of a unique element. Therefore, by setting this singleton set as $G'(T(x))$, we define a functor $G': T(\mathcal{C}) \to \mathbf{Set}$. At this time, $G'$ is naturally isomorphic to the $Hom$ functor $h^{T(i)} = Hom(T(i), -)$ represented by $T(i)$.  

(Proof) By assumption, there exists a functor $G: \mathcal{C} \to \mathbf{Set}$ that is naturally isomorphic to the $Hom$ functor $h^i = Hom(i, -)$. That is, for any $x \in \mathrm{Ob}(\mathcal{C})$, a morphism in $\mathbf{Set}$  
$α_x: Hom(i, x) \to G(x)$ is defined, and  
for any morphism $f: x \to y$ in $\mathcal{C}$,  
$α_y \circ h^i(f) = G(f) \circ α_x$ holds. Note here that since the existence of $h^i(f): Hom(i, x) \to Hom(i, y)$ is guaranteed, by the functoriality of $T$, $h^{T(i)}(T(f)): Hom(T(i), T(x)) \to Hom(T(i), T(y))$ exists.  

Let $α_{T(x)}': Hom(T(i), T(x)) \to G'(T(x))$.  
(In fact, from the definition of $G'$, $α_{T(x)}'$ is the identity morphism.)  
$G'(T(f)): G'(T(x)) \to G'(T(y))$ is the same morphism as $h^{T(i)}(T(f)): Hom(T(i), T(x)) \to Hom(T(i), T(y))$, and  
for any morphism $f: x \to y$ in $\mathcal{C}$,  
$α_{T(y)}7 \circ h^{T(i)}(T(f)) = G'(T(f)) \circ α_{T(x)}'$ holds.  
In addition, for any $x \in \mathrm{Ob}(\mathcal{C})$, the inverse morphism of $α_{T(x)}':G'(T(x)) \to Hom(T(i), T(x))$ also exists (as the identity morphism). Thus, $G'$ is naturally isomorphic to $h^{T(i)}$. (End of Proof)  

Let $u'$ be the universal element of $G'(T(i))$ corresponding to the identity morphism $id_{T(i)}$ of $h^{T(i)}$. That is, $u'$ is $id_{T(i)}$ itself. At this time,  
in $G'(T(f)): Hom(T(i), T(x)) \to Hom(T(i), T(y))$,  
since $G'(f')(u') = f' \circ id_{T(i)} = f'$,  
for any morphism $v' = g_{T(i)T(x)} \in G'(T(x))$, the morphism $f'$ satisfying $G'(f')(u') = v'$ is $v' = g_{T(i)T(x)}$ itself,  
and by the thinness of $T(\mathcal{C})$, this is unique.  

From the above, $T(i)$ is a (left) universal object in $T(\mathcal{C})$.  
Furthermore, if $T$ is assumed to be essentially surjective, any $b \in B$ is isomorphic to some $T(x)$, so $g_{T(x)b}$ exists. By the functoriality of $T$, $g_{T(i)T(x)}$ can be obtained, and since $g_{T(i)b} = g_{T(x)b} \circ g_{T(i)T(x)}$ exists, $T(i)$ becomes a (left) universal object in the entire $C(B, g)$.
(End of Proof of Proposition 3-5)

**Note**  
Examples of left universal objects: initial objects, coproducts, coequalizers, etc.

**Proposition 3-6** (Right Universal Objects)  
If $T$ is essentially surjective, then (right) universal objects are also preserved.

**Proof**
The definition of a (right) universal object $i$ in a category $\mathcal{C}$ is given as: "there exists a functor $G: \mathcal{C} \to \mathbf{Set}$ that is naturally isomorphic to the $Hom$ functor $h^i = Hom(-, i)$ represented by $i$, and for each object $x$ and any $v \in G(x)$, there uniquely exists a morphism $f \in Hom(x, i)$ such that $G(f)(u) = v$ holds." (Here, $u$ is the universal element in $G(i)$ corresponding to the identity morphism $id_i$ of $h^i$.)  

We show the proposition based on this definition.  

First, assume that $T$ is an essentially surjective functor. At this time, any object $b$ in $C(B, g)$ can be made isomorphic to $T(x)$ by taking some object $x$ in $\mathcal{C}$. That is, $g_{bT(x)}$ exists. Since $g_{T(x)T(i)}$ exists by the functoriality of $T$, $g_{bT(i)} = g_{T(x)T(i)} \circ g_{bT(x)}$ exists.  
That is, $Hom(b, T(i))$ is not empty. Here, due to the thinness of $T(\mathcal{C})$, this morphism set is a singleton set consisting of a unique element. Therefore, by setting this singleton set as $G'(b)$, we define a functor $G': C(B, g) \to \mathbf{Set}$. At this time, $G'$ is naturally isomorphic to the $Hom$ functor $h^{T(i)} = Hom(-, T(i))$ represented by $T(i)$.  

(Proof) Let $\alpha_b': Hom(b, T(i)) \to G'(b)$.  
(In fact, from the definition of $G'$, $\alpha_b'$ is the identity morphism.)  
For any $b_1, b_2 \in B$,  
$G'(g_{b_1b_2}): G'(b_1) \to G'(b_2)$ is the same morphism as $h^{T(i)}(g_{b_1b_2}): Hom(b_1, T(i)) \to Hom(b_2, T(i))$, and  
$\alpha_{b_2}' \circ h^{T(i)}(g_{b_1b_2}) = G'(g_{b_1b_2}) \circ \alpha_{b_1}'$ holds.  
In addition, for any $\alpha_b'$, the inverse morphism $G'(b) \to Hom(b, T(i))$ also exists (as the identity morphism). Thus, $G'$ is naturally isomorphic to $h^{T(i)}$. (End of Proof)  

Let $u'$ be the universal element of $G'(T(i))$ corresponding to the identity morphism $id_{T(i)}$ of $h^{T(i)}$. That is, $u'$ is $id_{T(i)}$ itself. At this time,  
in $G'(g_{b_1b_2}): Hom(b_1, T(i)) \to Hom(b_2, T(i))$, since $G'(f')(u') = f'$○ $id_{T(i)} = f'$,  
for any morphism $v' = g_{bT(i)} \in G'(g_{bT(i)})$, the morphism $f'$ satisfying $G'(f')(u') = v'$ is $v'=g_{bT(i)}$ itself,  
and by the thinness of $C(B, g)$, this is unique.  

From the above, $T(i)$ is a (right) universal object in $C(B, g)$. 
(End of Proof)

**Note**  
Examples of right universal objects: terminal objects, products, equalizers, etc.

**Proposition 3-7**  
If $T$ is essentially surjective, then universal objects in $\mathcal{C}$ are mapped to universal objects in $C(B,g)$.

## Adjunctions

**Proposition 3-8**  
Let $T : C_A \to C_B$ be a functor between thin categories with $T : A \to B$ injective on objects. Then there exists a functor $T': T(C_A) \to C_A$ defined by $T'(T(i)) = i$ and $T'(g_{T(i)T(j)}) = f_{ij}$, and $T$ is left adjoint to $T'$ ($T \dashv T'$).

**Proof**  
First, the definition that a functor $T: \mathcal{C} \to \mathcal{D}$ is a left adjoint functor of $T': \mathcal{D} \to \mathcal{C}$ is given using the unit of adjunction (universal morphism) as follows.  
"For any object $i \in \mathrm{Ob}(\mathcal{C})$, there exists a pair $(T(i), \eta_i)$ that satisfies the following two conditions:  
1. $\eta_i: i \to T'(T(i))$ is a morphism in $\mathcal{C}$.  
2. For any object $k \in \mathrm{Ob}(\mathcal{D})$ and any morphism $f: i \to T'(k)$, there exists a unique morphism $g: T(i) \to k$ in \mathcal{D} such that $f = T'(g) \circ \eta_i$ holds."

   
In this proposition, let $\mathcal{C} = C_A$ and $\mathcal{D} = T(C_A)$, and the proof is carried out based on the above definition.

1. Existence of the unit of adjunction $\eta$  
For any $i \in A$, $T'(T(i)) = i$ is uniquely determined by the injectivity of $T$ with respect to objects.  
At this time, $\eta_i: i \to T'(T(i))$ is given as the identity morphism $id_i: i \to i$. Since $C_A$ is a category, the identity morphism always exists, and this is a morphism of $C_A$.

2. Verification of universality (unique factorization property)  
Consider any $k \in \mathrm{Ob}(T(C_A))$ and a morphism $f_{i T'(k)}$ in $C_A$.  
By the definition of the image, there exists $j \in A$ such that $k = T(j)$, and from the definition of $T'$, $T'(k) = j$ holds. Therefore, $f_{i T'(k)}=f_{ij}$.  
At this time, if the morphism $g_{T(i)T(j)}$ exists in $T(C_A)$, then from the definition of the functor $T'$ regarding morphisms, $T'(g_{T(i)T(j)}) = f_{ij}$, the following holds:  
$T'(g) \circ \eta_i = f_{ij} \circ id_i = f_{ij}.$

3. Verification of uniqueness  
The uniqueness of the morphism $g_{T(i)k}$ holds because $T(C_A)$ is a thin category.  

From the above, the adjunction relation $T \dashv T'$ with the identity morphism as the unit has been shown.  
(Proof complete)


**Note**  
When $C_A$ and $C_B$ are skeletal (i.e., $A$ and $B$ are posets), $T$ and $T'$ form a Galois connection.

## Natural Transformations and Functor Categories

Given functors $T, T' : \mathcal{C} \to C(B,g)$, the family
$\tau_{T,T'} := ｛\tau_i := g_{T(i)T'(i)}｝_{i \in \rm{Ob}(\mathcal{C})}$
is the unique natural transformation from $T$ to $T'$, with each $\tau_i$ as its component.

If each $\tau_i$ has an inverse $g_{T'(i)T(i)}$, then $\tau_{T,T'}$ is a natural isomorphism ($T \cong T'$).

Let $\Phi$ be the collection of all functors from $\mathcal{C}$ to $C(B,g)$. Then $\mathcal{C}(\Phi, ｛\tau_{T,T'}｝)$ is a thin category, and is precisely the **functor category** $[\mathcal{C}, C(B,g)]$.



