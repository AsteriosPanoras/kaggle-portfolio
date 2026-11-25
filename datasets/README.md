# Public Kaggle datasets

No data files are stored in this repository; the links go to the datasets on Kaggle.
Download counts are the ones Kaggle reported on 2026-11-25 (`kaggle datasets list --mine`; the Atlas was last updated on 2026-11-20, the Santa and Squares datasets on 2026-11-24; 2026-11-20: 16,100 for the Atlas; 2026-11-17 midday: 9,825 for the Atlas; 2026-11-15 evening: 7,737 for the Atlas and 56 for the HVAC code). A dataset is listed here only if its page opens without an account (checked on 2026-11-17; the Santa dataset and the S6E11 and Atlas pages again on 2026-11-20).

| Dataset | What it is | Licence | Downloads | Link |
|---|---|---|---:|---|
| QCC Circuit Atlas + Verified Refit Toolkit | "Every public circuit of Google's quantum contest, plus refit and analysis tools": a deduplicated, credited table of the circuit files published in the [Google Verifiable Quantum Circuit Compilation](https://www.kaggle.com/competitions/google-verifiable-quantum-circuit-compilation) competition (1,719 rows: who published each file first and every other source holding the same bytes), readable text versions of the invsqrt and chemistry circuits whose licence allows it, and small pure-numpy tools (simulator, liveness, splicing, chemistry loader check). Created 2026-11-12; version 2 adds `contributions/` (our verified results, with their gain and verification) and `tools/refit` (the chemistry weight refit); **version 3 (2026-11-15)** adds `best/`, described below. | Apache-2.0 | 22,113 (22 votes) | [kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) |
| Supervisory layer for HVAC: SB26 paper code | "Code, protocols and per-episode results of the paper 'Re-select or Learn?'" (see [research/smart-buildings-sb26.md](../research/smart-buildings-sb26.md)) | Apache-2.0 | 190 (2 votes) | [kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac](https://www.kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac) |
| Squares in Squares - Best Packings | the per-puzzle best merge of the newest public packings of the [Squares in Squares](https://www.kaggle.com/competitions/squares-in-squares) competition (a `submission.csv`, a per-puzzle side-length table and a README); rebuilt as new public outputs appear (last update 2026-11-17 01:27 UTC). Almost all packings are other authors' public work, credited in [my notebook](https://www.kaggle.com/code/asteriospanoras/squares-22-134-play-with-boxes-best-public-lb) | not stated in the listing I could read | 3,587 (2 votes) | [kaggle.com/datasets/asteriospanoras/squares-in-squares-best](https://www.kaggle.com/datasets/asteriospanoras/squares-in-squares-best) |
| Santa 2026 Elf Calculator: Programs + Experiments | `best_programs.csv`: the best verified program for each of the 1,000 puzzles of [Santa 2026](https://www.kaggle.com/competitions/santa-2026), with its length and its source (every program is another author's public work, Apache-2.0, credited line by line), the experiment tables behind my guide notebook and `elf_tools/` (an exact verifier and search tools); updated in place with every notebook version (last update 2026-11-20 10:21 UTC) | not stated in the listing I could read | 80,043 (39 votes) | [kaggle.com/datasets/asteriospanoras/santa-2026-elf-programs-and-experiments](https://www.kaggle.com/datasets/asteriospanoras/santa-2026-elf-programs-and-experiments) |
| S6E11 Public Board Files (pinned copies) | pinned copies of public submission files of other authors of Playground Series S6E11 (file names carry the author, e.g. `goodpjw2008_v6_submission.csv`) with a `SHA256SUMS` file, so that an analysis can rebuild its inputs exactly. The files are their authors' public work and keep their credits and terms | not stated in the listing I could read | 439 (2 votes) | [kaggle.com/datasets/asteriospanoras/s6e11-public-board-files](https://www.kaggle.com/datasets/asteriospanoras/s6e11-public-board-files) |
| GGA Visual Guide Tables | five small CSV files written or measured by me for the [Generalist Gaming Agent](https://www.kaggle.com/competitions/generalist-gaming-agent) guide notebook (timing, action space and practice-game profiles, real-run statistics of two public Gemma agents, the board scores of public notebooks as their authors state them); no competition files or game assets | CC BY 4.0 | 30 (3 votes) | [kaggle.com/datasets/asteriospanoras/gga-visual-guide-tables](https://www.kaggle.com/datasets/asteriospanoras/gga-visual-guide-tables) |

## Use by others

(Not rescanned on 2026-11-20: the lists below are those of 2026-11-17; the Santa dataset has not been scanned.)

* Atlas: `kaggle kernels list --dataset asteriospanoras/qcc-circuit-atlas` lists, besides my own notebooks, four public notebooks of other authors (ozertuu, evgendvorkin and mizeroluckygall x2); details in [competitions/google-qcc/evidence/USES.md](../competitions/google-qcc/evidence/USES.md).
* Squares in Squares - Best Packings: input of the public notebooks of nilanjansaha123, areebbb, samanyu1808 and parkera, and the source of rows in penguin069's notebook ([competitions/squares-in-squares/README.md](../competitions/squares-in-squares/README.md)).
* S6E11 Public Board Files: input of goodpjw2008's notebook ([competitions/playground-s6e11/README.md](../competitions/playground-s6e11/README.md)).
* HVAC paper code: Kaggle lists no notebook that uses it.

## QCC Circuit Atlas, version 6: `frontier/`

Version 6 (2026-11-19) adds a `frontier/` folder: two public file sets of other authors, the 28.23498 set (Koushik Rudra's notebook) and the 28.23837 set (ozertuu's), each as a folder of the 18 files of a submission (`invsqrt.kmb`, `dqi.kmb`, the chemistry `submission.npz` and 15 loader files), a `receipt.json` with SHA-256 values, and a `licenses/` folder with the licence and credit notices of their authors (Syed Asad Ali, Lera/marculera, Grant Prater, boristown, maoxin123, Leo Tang, Hayato Hikawa, Koushik Rudra, ozertuu and others). They are **other authors' work**, carried with their notices so that a notebook can rebuild a verified submission from the Atlas alone; this repository holds none of the files.

## QCC Circuit Atlas, version 3: `best/`

The two files of the 28.06018 release of the [Atlas Toolkit notebook](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-09535) (both already verified with the unchanged official verifiers and submitted; local GM 28.05956), with the NOTICE and LICENSE files of their authors:

| File in `best/` | What it is | Origin and credit |
|---|---|---|
| `invsqrt_44q_resolved_angles_090009609ee6.kmb` | Syed Asad Ali's v13 44-qubit invsqrt (`47b31838`, packaged by Ertugrul Ozer in his notebook 28.056) with the 34 non-Clifford rotations re-solved by the exact phase-margin LP: 29 angle literals change, every other op is identical; minimum phase margin 22,067,537 -> 22,102,972 units, cost 75170.13 vs 75170.62 | circuit: Syed Asad Ali (Apache-2.0; `SYED_NOTICE.txt`, `SYED_LICENSE.txt`); angle LP: ours |
| `chem_lera_c44_refit25.npz` | the `submission.npz` of `marculera/dfthc-c44-build` (8,143,44 table, 14,712-Toffoli loaders) with `W` and `H2_I` refitted at fixed words for 25 minutes by `tools/refit` (lambda_eff 46.92764 -> 46.92495; all gates keep at least 1.5e-9 Ha); the 15 loader files are not included, take them from `marculera/dfthc-c44-build` | table, words, loaders: Lera (marculera, Apache-2.0; `MARCULERA_NOTICE.txt`, `MARCULERA_LICENSE.txt`); refit: ours, method after prvsiyan |

Lineage (Apache-2.0 section 4): keep the NOTICE files with any redistribution of these files, and name `marculera/dfthc-c44-build` as the origin of the chemistry table and Syed Asad Ali as the original builder of the invsqrt circuit. The files themselves are on Kaggle only; this repository holds no circuit or weight files.

Public notebooks of other authors that list a dataset as an input:
`kaggle kernels list --dataset asteriospanoras/qcc-circuit-atlas` (see
[competitions/google-qcc/evidence/USES.md](../competitions/google-qcc/evidence/USES.md)).
