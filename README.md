# POLYBRUTUS 17D — Exact 22-point Euclidean completion and an elevenfold graph mode

**Human author and scientific responsibility:** Gabriel St-Pierre, independent researcher.  
**Research status:** independently reproducible exact mathematical case study; no independent human peer review.  
**AI-use disclosure:** OpenAI ChatGPT (Astra) substantially assisted exact symbolic verification, implementation of a separate rational verifier, the chosen model spectrum, scientific drafting and release; AI is not an author.

## Mathematical certificates, normalized radius R=1

- **22 labelled points**, **231 exact pairwise squared distances**, minimal Euclidean affine embedding rank **17**.
- All **210/210** predecessor 16D labelled distances are exactly preserved, unchanged and in original order.
- Add one perpendicular unit vector, creating **21** new squared pair distances, each equal to **2**.
- Eight normalized distance classes `k=4d²/R²` with counts `{4:6,7:2,8:200,9:3,10:10,12:6,13:2,16:2}`.
- Exact sum of all pair squared distances: `1895 R²/4`.
- Exact coordinate-difference rank **17**, centered Euclidean distance Gram rank **17**, and positive-semidefinite identity `B=(HX)(HX)^T`. Eighteen storage-coordinate slots include one original simplex relation.
- In a **chosen ideal complete weighted-graph scalar-oscillator model**, with equal unit masses and `w_ij=R²/d_ij²`, the weighted Laplacian has eigenvalue **11 with exact multiplicity 11** and eigenvalue **21/2 with exact multiplicity 4**. These are abstract, dimensionless model properties, not measured frequencies.
- Two differently implemented programs verify **all 231** labelled squared distances, the minimal affine dimension and both exact graph root multiplicities; four negative-control variants are rejected.

## Reproduce

```sh
python -m pip install sympy==1.14.0
python src/verify_d17.py
python tests/independent_d17.py
```

The second checker reconstructs squared distances via rational rules without importing the primary or ancestor point generator. `prior/` contains the source and exact certificates of the predecessor lineage from the **frozen** `Topbrutus/polybrutus-d16@v0.1.0`, commit `c7700a46cb0b2c3d2556f50a207d86da84055ea0`.

**Included:** `src/verify_d17.py`, `tests/independent_d17.py`, `results/certificate_d17.json`, `SPECIFICATION_D17.md`, `PREUVE_D17.md`, `PROVENANCE.md`, `publication/POLYBRUTUS_17D_NOTE.pdf`, `.md`, GitHub Actions workflow and SHA-256 Git blob index. Source code MIT, scientific preprint CC BY 4.0.

**Predecessor:** [Polybrutus D16, DOI 10.5281/zenodo.24408979](https://doi.org/10.5281/zenodo.24408979).

**Scientific limits:** Orthogonal completion and spectral shift of uniformly attached graphs are known mathematical mechanisms. No novel universal theorem, new physical dimension, measured resonance or physical particle is claimed.
