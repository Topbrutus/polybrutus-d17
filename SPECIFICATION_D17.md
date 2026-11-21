# Polybrutus D17 — Exact 22-point Euclidean specification

**Frozen source:** `Topbrutus/polybrutus-d16@v0.1.0`, commit `c7700a46cb0b2c3d2556f50a207d86da84055ea0`, DOI `10.5281/zenodo.24408979`.

Let `p1,...,p21` be the previous exact radius-one vectors in seventeen storage-coordinate slots, with an exact linear relation from the original centered simplex. Embed them in eighteen storage slots as `q_i=(p_i,0)` for `i=1,...,21`, then adjoin `q22=e18=(0,...,0,1)`.

The new radius-one vector is orthogonal to every predecessor vector. Hence

```
||q22-q_i||²=||q22||²+||q_i||²-2<q22,q_i>=2,
i=1,...,21.
```

All **210** predecessor labelled squared distances remain exactly unchanged. The new metric has **231** labelled pairwise distances and intrinsic affine rank exactly **17**, despite occupying eighteen storage slots.

For `k=4d²/R²`, class counts are `4:6,7:2,8:200,9:3,10:10,12:6,13:2,16:2`. The sum of pair squared distances equals `1895R²/4`. At unit radius the exact centroid is `(0,0,1/44,0,0,0,0,0,1/22,1/22,1/22,1/22,1/22,1/22,1/22,1/22,1/22,1/22)`.

For the **selected** ideal oscillator graph with weights `w_ij=R²/d_ij²` and equal scalar masses, the 22-by-22 Laplacian is
```
L17 = [ L16 + (1/2) I21     -(1/2) 1 ]
      [ -(1/2) 1ᵀ                 21/2 ].
```
Its exact characteristic polynomial has the factorization
```
chi22(z)=z(z-11)*chi21(z-1/2)/(z-1/2)
        =z(z-11)^11(z-21/2)^4 f6(z-15/2),
f6(z)=chiP7(z)/z.
```
Eigenvalue 11 has multiplicity exactly 11 and eigenvalue 21/2 multiplicity exactly 4. These are theoretical graph eigenvalues rather than physical measurements.
