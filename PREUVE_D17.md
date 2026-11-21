# Polybrutus D17 — Proof, labelled metric, and model spectrum

## 1. Exact conservative metric

Take the frozen Polybrutus 16D radius-one point set with 21 labelled vectors and 210 pair distances. Append a zero coordinate to every predecessor and adjoin a unit basis vector orthogonal to the previous embedding. All predecessor squared distances are preserved. The 21 newly created squared distances are exactly 2. Hence `C(22,2)=231` pairs, with normalized `k=4d²` family counts `{4:6,7:2,8:200,9:3,10:10,12:6,13:2,16:2}`; squared-distance sum `1895/4`.

## 2. Intrinsic minimal affine dimension

Let `X` be the exact 22-by-18 coordinate array, `D` the exact 22-by-22 **squared Euclidean distance** matrix and `H=I-11ᵀ/22` the centering matrix. The main symbolic program proves without numerical approximation:

```
rank([q2-q1,...,q22-q1])=17
rank(B)=17
B=-H D H/2=(H X)(H X)^T
```

Thus `B` is positive semidefinite and has rank 17. Since every Euclidean realization of the same complete *labelled* squared-distance matrix gives the identical centered Gram, the minimal affine dimension is exactly 17. The additional storage-coordinate slot comes from the single original simplex hyperplane constraint, not an additional independent direction.

## 3. Chosen graph model

Define equal-mass scalar oscillator displacements and complete positive pair weights `w_ij=1/d_ij²` at unit radius. The new point joins each of the previous 21 with graph weight 1/2. The Laplacian block identity is

```
L17=[ L16+(1/2)I21  -(1/2)1 ]
    [ -(1/2)1ᵀ         21/2 ].
```

The characteristic polynomial therefore obeys

```
chi22(z)=z(z-11)*chi21(z-1/2)/(z-1/2).
```

From the frozen predecessor `chi21(z)=z(z-21/2)^10(z-10)^4 f6(z-7)`, where `f6(z)=chiP7(z)/z` is the six-nonzero-mode factor from the canonical seven-vertex graph, substitution yields

```
chi22(z)=z(z-11)^11(z-21/2)^4 f6(z-15/2).
```

The symbolic source computes the complete 22-by-22 exact characteristic polynomial and verifies this closed form and recurrence. It verifies that `f6(7/2)!=0` and `f6(3)!=0`, excluding extra multiplicity at either designated root: **11 exactly elevenfold, 21/2 exactly fourfold**.

The independently implemented rational verifier checks every one of 231 labelled squared distances and the centered Gram rank; it computes the same graph characteristic polynomial using rational weights and certifies both multiplicities by nonzero higher derivatives.

## 4. Falsification and limits

Four negative tests detect a corrupted pair distance, an identical duplicated vertex (rank drop), a tilted nonorthogonal new vertex, and a relabelling which preserves the histogram but violates the labelled pair metric.

The orthogonal addition is established Euclidean geometry; the model graph join is an established matrix operation. No novel universal mathematical result, physical extra dimension or experimentally measured resonance is inferred. No independent human peer review is claimed.
