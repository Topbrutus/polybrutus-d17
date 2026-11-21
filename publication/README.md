# Polybrutus 17D — Controlled release checklist

This is an unreviewed exact mathematical case study. It does not claim new physical dimensions or mathematical universal novelty.

1. Verify `src/verify_d17.py` and `tests/independent_d17.py` locally with SymPy 1.14.0.
2. Create **private** GitHub `Topbrutus/polybrutus-d17`; run both checks in CI, require success.
3. Freeze the successful commit as tag `v0.1.0`; produce ZIP from `git archive v0.1.0` (not mutable worktree).
4. Verify ZIP/PDF/JSON size and SHA-256 and stage exactly **one** direct-REST Zenodo draft with parent DOI, author, CC BY 4.0 note license, source tag, and AI disclosure.
5. Verify draft metadata and all three remote checksums.
6. Make GitHub public; confirm frozen tag via public GitHub API; publish **that existing Zenodo draft**, not another.
7. Verify public DOI and all three files. Record DOI in README/CITATION/manifest and Memoria. Preserve frozen science tag.

No API tokens, private conversations or credentials are included in public source. Disable parallel GitHub automatic Zenodo harvesting to prevent duplicate records.
