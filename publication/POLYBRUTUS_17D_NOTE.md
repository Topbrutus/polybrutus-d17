# Polybrutus 17D: Exact Euclidean Completion and an Elevenfold Weighted-Graph Mode

**Research author:** Gabriel St-Pierre  
**Affiliation:** Independent researcher  
**Project:** Polybrutus-X72  
**Date:** 20 November 2026  
**Version:** 0.1.0  
**Status:** Reproducible computational mathematics preprint; not independently human peer reviewed  
**Parent research:** Polybrutus 16D, DOI 10.5281/zenodo.24408979  
**Frozen scientific code:** https://github.com/Topbrutus/polybrutus-d17/tree/v0.1.0 (upon release)

## Abstract

An exact **twenty-two-point labelled Euclidean distance configuration** is constructed with **minimal affine embedding dimension seventeen**, conservatively extending the archived Polybrutus 16D metric. All **210 predecessor pairwise squared distances** are preserved exactly. An additional orthogonal radius-R point contributes **21 new pairwise squared distances of value 2R²**, producing **231 labelled pair distances** distributed in eight normalized distance families. Exact coordinate-difference rank, centered Euclidean-distance Gram rank and positive-semidefinite Gram factorization establish the minimum affine dimension. A separately implemented rational-arithmetic verifier reconstructs all 231 labelled distances and independently verifies Gram rank 17.

For a **chosen ideal complete weighted-graph scalar-oscillator model**, with equal scalar masses and weights `w_ij=R²/d_ij²`, the exact Laplacian polynomial has an **eigenvalue 11 of multiplicity 11** and an **eigenvalue 21/2 of multiplicity 4**. The full characteristic polynomial is certified in two distinct programs. These are mathematical properties of the specified configuration and model graph, **not newly observed physical dimensions, resonances or universal mathematical theorems**.

## 1. Mathematical provenance

The Polybrutus programme begins with seven exact analytically defined points on a three-dimensional radius-R sphere. Its published seven-dimensional completion adjoined five vertices of a regular four-dimensional simplex in an orthogonal subspace, keeping the seven original points unchanged while giving twelve vertices and sixty-six labelled pair distances (DOI **10.5281/zenodo.24407952**).

From that point, successive publications extended the configuration by one orthogonal unit-radius point at each dimension, preserving every labelled predecessor distance: **8D** with 13 points and 78 pair distances (DOI 10.5281/zenodo.24408344); **9D** with 14 and 91 (10.5281/zenodo.24408448); **10D** with 15 and 105 (10.5281/zenodo.24408569); **11D** with 16 and 120 (10.5281/zenodo.24408650); **12D** with 17 and 136 (10.5281/zenodo.24408720); **13D** with 18 and 153 (10.5281/zenodo.24408769); **14D** with 19 and 171 (10.5281/zenodo.24408836); **15D** with 20 and 190 (10.5281/zenodo.24408887); and **16D** with 21 and 210 (10.5281/zenodo.24408979).

The present 17D case starts from the immutable public **`Topbrutus/polybrutus-d16@v0.1.0`** tag, commit **`c7700a46cb0b2c3d2556f50a207d86da84055ea0`**. The source programs and exact metric certificates from the predecessor are copied without modification into the new research release's `prior/` directory. No previously published point set, scientific source tag or old DOI is changed.

## 2. Exact twenty-two-point Euclidean construction

At normalized radius `R=1`, let `p1,...,p21` be the exact predecessor sixteen-dimensional points, stored in seventeen coordinate slots. The five centered regular-simplex vertices occupy a four-dimensional hyperplane of five coordinate slots and impose one exact linear constraint in this representation.

Embed each predecessor in eighteen slots by appending zero:

```
q_i=(p_i,0),         i=1,...,21.
```

Adjoin a perpendicular unit vector in the new eighteenth storage coordinate:

```
q22=e18=(0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1).
```

All twenty-two vectors have unit norm, and the new point is orthogonal to each of the preceding twenty-one vectors. Every old pairwise distance remains exactly unchanged, while each new pair obeys

```
||q22-q_i||²=||q22||²+||q_i||²-2<q22,q_i>=2.
```

For arbitrary radius `R>0`, multiply every coordinate by `R`, obtaining new squared distances `2R²`. The total number of unordered labelled pairs is `C(22,2)=231`, split into **210 retained old pairs and 21 new pairs**.

For `k=4d²/R²`, the complete exact normalized distance histogram is:

| k | 4 | 7 | 8 | 9 | 10 | 12 | 13 | 16 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Multiplicity | 6 | 2 | **200** | 3 | 10 | 6 | 2 | 2 |

All eight multiplicities sum to **231**. The sum of squared distances is exactly `1895R²/4`. At unit radius, the exact centroid in eighteen storage slots is

```
G=(0,0,1/44,0,0,0,0,0,1/22,1/22,1/22,1/22,1/22,1/22,1/22,1/22,1/22,1/22).
```

The metric's intrinsic affine dimension is **17**, not 18: the eighteen-slot representation contains one redundant centered-simplex direction.

## 3. Exact minimum affine embedding dimension

Let `X` denote the **22-by-18** exact coordinate matrix and `D` the **22-by-22 squared Euclidean distance matrix** of the labelled points. Define `H=I-11ᵀ/22`, the centering projector, and the centered Gram matrix:

```
B=-(1/2)HDH.
```

The primary SymPy verifier proves all three equalities exactly:

```
rank([q2-q1,...,q22-q1])=17;
rank(B)=17;
B=(HX)(HX)^T.
```

The last equation is an exact positive-semidefinite factorization. The complete **labelled** squared-distance matrix uniquely determines `B`; therefore any Euclidean realization having precisely these **231 labelled distances** must have minimal affine dimension **seventeen**. This claim is about the rank of a mathematical configuration, **not the dimension of physical spacetime**.

The independently implemented rational verifier does not import the primary point generator. It reconstructs all squared distances from rational coefficients for the canonical seven original points, internal squared distances `5/2` of the five regular-simplex vertices, and the perpendicularity of all additional unit vectors. It confirms **231/231** labelled squared distances, every one of the **210** parent distances, and centered Gram rank **17**.

## 4. An elevenfold graph eigenvalue in a chosen model

For an illustrative **ideal** scalar-oscillator network, assign equal unit scalar masses to each of the twenty-two points and complete weighted-graph couplings `w_ij=R²/d_ij²`. This is a stipulated model, not an experimentally constructed physical system.

The newly added point has normalized squared distance `2` from each of the twenty-one old vertices; every newly created graph edge therefore has weight `1/2`. With `L16` denoting the old **21-by-21** Laplacian, the new **22-by-22** matrix is

```
L17=[ L16+(1/2)I21      -(1/2)1 ]
    [ -(1/2)1ᵀ             21/2 ].
```

The model separates into the uniform zero mode, one intergroup mode and all shifted previous nonuniform modes. The exact characteristic-polynomial recurrence is

```
chi22(z)=z(z-11)chi21(z-1/2)/(z-1/2).
```

The frozen sixteen-dimensional source provides

```
chi21(z)=z(z-21/2)^10(z-10)^4*f6(z-7),
f6(z)=chiP7(z)/z,
```

where `chiP7` is the original seven-point graph characteristic polynomial and `f6` contains its six nonzero modes. Substituting yields

```
chi22(z)=z(z-11)^11(z-21/2)^4*f6(z-15/2).
```

The primary program computes the **entire exact 22-by-22 characteristic polynomial** and verifies both the recurrence and this closed form. It also checks `f6(7/2)!=0` and `f6(3)!=0`, establishing that there are no additional hidden factors at the designated eigenvalues. Hence the graph mode at **11 has exact multiplicity eleven**, and that at **21/2 has exact multiplicity four**.

The independent rational-distance program reconstructs the complete graph on its own metric and verifies these exact multiplicities by the vanishing and nonvanishing of the characteristic polynomial's derivatives. They are dimensionless model eigenvalues, **not measured frequencies in hertz**.

## 5. Reproducibility and negative controls

The accompanying research archive contains `src/verify_d17.py` (complete exact geometry, rank, Gram and Laplacian), `tests/independent_d17.py` (separately implemented rational metric and spectral verification), `results/certificate_d17.json` (all **231 exact labelled squared distances**), predecessor code and certificates in `prior/`, a specification, proof, provenance, GitHub Actions workflow and SHA-256 Git-source blob index.

Reproduce the exact tests:

```sh
python -m pip install sympy==1.14.0
python src/verify_d17.py
python tests/independent_d17.py
```

Both programs must print PASS and the identical SHA-256 fingerprint of the generated JSON certificate. Four deliberately invalid variants are detected: one corrupted distance, a duplicate vertex causing affine rank loss, a tilted nonorthogonal addition and a permutation of labels preserving the distance histogram but altering the complete labelled metric.

The scientific release attaches a ZIP generated exclusively from the frozen source Git tag, this PDF note, and the exact certificate JSON. The archive hashes and source commit permit future verification of the deposited bytes and complete predecessor chain.

## 6. Scientific precedence, attribution and limits

Orthogonal Euclidean embedding extensions, centered squared-distance Gram ranks and uniformly joined graph Laplacians are established mathematical techniques. This preprint supplies one **specific reproducible Polybrutus 17D computational case study**, not a discovery of those general methods or a novel universal theorem. No actual seventeen-dimensional physical spacetime, measured resonance, new particle or validated physical model is established.

**Human research author and responsible investigator:** Gabriel St-Pierre, independent researcher, who originated the Polybrutus programme and directs the individually archived dimensional investigation.

**Generative AI disclosure:** OpenAI ChatGPT (Astra) substantially assisted source verification, symbolic mathematics, two software programs including an independently implemented rational verifier, the selected graph-spectral analysis, documentation, drafting and release preparation. The AI is **not listed as an author**. Independent human scientific peer review has not occurred.

**Licenses:** scientific manuscript and prose CC BY 4.0; source programs MIT.

**References:** canonical seven-point Polybrutus specification https://github.com/Topbrutus/polybrutus/blob/main/SPECIFICATION.md ; predecessor Polybrutus 16D https://doi.org/10.5281/zenodo.24408979 ; frozen source https://github.com/Topbrutus/polybrutus-d16/tree/v0.1.0 ; earlier dimensions and DOIs recorded in the `PROVENANCE.md` of the source archive.
