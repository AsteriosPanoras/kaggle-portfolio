# Public Kaggle datasets

No data files are stored in this repository; the links go to the datasets on Kaggle.
Download counts are the ones Kaggle reported in the evening of 2026-11-15 (`kaggle datasets list -m`).

| Dataset | What it is | Licence | Downloads | Link |
|---|---|---|---:|---|
| QCC Circuit Atlas + Verified Refit Toolkit | "Every public circuit of Google's quantum contest, plus refit and analysis tools": a deduplicated, credited table of the circuit files published in the [Google Verifiable Quantum Circuit Compilation](https://www.kaggle.com/competitions/google-verifiable-quantum-circuit-compilation) competition (1,719 rows: who published each file first and every other source holding the same bytes), readable text versions of the invsqrt and chemistry circuits whose licence allows it, and small pure-numpy tools (simulator, liveness, splicing, chemistry loader check). Created 2026-11-12; version 2 adds `contributions/` (our verified results, with their gain and verification) and `tools/refit` (the chemistry weight refit); **version 3 (2026-11-15)** adds `best/`, described below. | Apache-2.0 | 7,737 | [kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) |
| Supervisory layer for HVAC: SB26 paper code | "Code, protocols and per-episode results of the paper 'Re-select or Learn?'" (see [research/smart-buildings-sb26.md](../research/smart-buildings-sb26.md)) | Apache-2.0 | 56 | [kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac](https://www.kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac) |

## QCC Circuit Atlas, version 3: `best/`

The two files of the 28.06018 release of the [Atlas Toolkit notebook](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-07502-wait-daily-reset) (both already verified with the unchanged official verifiers and submitted; local GM 28.05956), with the NOTICE and LICENSE files of their authors:

| File in `best/` | What it is | Origin and credit |
|---|---|---|
| `invsqrt_44q_resolved_angles_090009609ee6.kmb` | Syed Asad Ali's v13 44-qubit invsqrt (`47b31838`, packaged by Ertugrul Ozer in his notebook 28.056) with the 34 non-Clifford rotations re-solved by the exact phase-margin LP: 29 angle literals change, every other op is identical; minimum phase margin 22,067,537 -> 22,102,972 units, cost 75170.13 vs 75170.62 | circuit: Syed Asad Ali (Apache-2.0; `SYED_NOTICE.txt`, `SYED_LICENSE.txt`); angle LP: ours |
| `chem_lera_c44_refit25.npz` | the `submission.npz` of `marculera/dfthc-c44-build` (8,143,44 table, 14,712-Toffoli loaders) with `W` and `H2_I` refitted at fixed words for 25 minutes by `tools/refit` (lambda_eff 46.92764 -> 46.92495; all gates keep at least 1.5e-9 Ha); the 15 loader files are not included, take them from `marculera/dfthc-c44-build` | table, words, loaders: Lera (marculera, Apache-2.0; `MARCULERA_NOTICE.txt`, `MARCULERA_LICENSE.txt`); refit: ours, method after prvsiyan |

Lineage (Apache-2.0 section 4): keep the NOTICE files with any redistribution of these files, and name `marculera/dfthc-c44-build` as the origin of the chemistry table and Syed Asad Ali as the original builder of the invsqrt circuit. The files themselves are on Kaggle only; this repository holds no circuit or weight files.

Public notebooks of other authors that list a dataset as an input:
`kaggle kernels list --dataset asteriospanoras/qcc-circuit-atlas` (see
[competitions/google-qcc/evidence/USES.md](../competitions/google-qcc/evidence/USES.md)).
