# Google Quantum AI: Verifiable Quantum Circuit Compilation

Competition: [kaggle.com/competitions/google-verifiable-quantum-circuit-compilation](https://www.kaggle.com/competitions/google-verifiable-quantum-circuit-compilation)

## The competition in brief

Teams submit three quantum circuits written in `kickmix`, a gate language whose circuits can be checked shot by shot
on a classical computer (reversible classical gates, phase gates and measurement-based uncomputation):

| Task | What the circuit computes | Cost (lower is better) |
|---|---|---|
| invsqrt | a fixed-point inverse square root, kicked into the phase | qubits x (Toffolis + T/4) |
| DQI | the decoder of Decoded Quantum Interferometry (Reed-Solomon syndromes over GF(2^12)) | repetition factor x qubits^2 x Toffolis |
| chemistry | block encoding of a molecular Hamiltonian (double-factorised / THC loaders) | lambda_eff x Toffolis x qubits |

The hosts' official verifiers simulate every circuit on many inputs and reject it on a single wrong shot (DQI
tolerates rare failures at a price). The score is the geometric mean of the three ratios reference cost / your cost,
so a 1 % cut in any task is worth the same. No quantum hardware is involved: the game is fewer qubits and Toffoli
gates, proven exactly.

## What I contributed (public, in order)

All dates UTC, from the run logs of the notebooks. Scores: "board" = public leaderboard score of the submission made
from that notebook version; "local" = geometric mean computed with the unchanged official verifiers inside the notebook
(default salt). The two differ slightly because the board draws its own random DQI shots.

| Date | Notebook | Contribution | Score |
|---|---|---|---|
| 2026-11-11 | [LB 25.367 \| Verified Portfolio + DQI Readout Fix](https://www.kaggle.com/code/asteriospanoras/lb-25-367-verified-portfolio-dqi-readout-fix) (v1) | **DQI readout-window transplant**: CSWAP readout windows (a `CSWAP` followed by measuring both outputs) rewritten as `CX`/`HMR`/`CZ` with no Toffoli, moved onto Atakan Aldemir's best DQI file: -48 Toffolis per shot (file `245527f6`) | board 25.36727 |
| 2026-11-11 22:58 | same notebook (v4) | **invsqrt splice at clean cuts**: two public 62-qubit circuits (WCao24's normaliser and Thomas Gamet's early prefix) joined where wires and phase agree on every sampled input, -3.0 Toffolis vs the best one (file `9c708f7b`) | local 25.3957, board 25.39570 |
| 2026-11-12 | same notebook (v5) | portfolio refresh with the new public chemistry loaders | local 25.40483 |
| 2026-11-12 | [QCC Circuit Atlas](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) (dataset) | every public circuit file of the competition, deduplicated by SHA-256, with first source, author and all copies; readable text of the circuits; numpy tools | 1,483 downloads |
| 2026-11-12 | [QCC 27.30 \| Public Frontier + Free CZ Fix in invsq](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-public-frontier-free-cz-fix-in-invsq) (v1, then titled "QCC 25.449") | portfolio on maoxin123's 392k-Toffoli DQI decoder with our invsqrt splice | local 25.44954, board 25.44953 |
| 2026-11-14 09:47 | same notebook (v5) | **invsqrt dead-write fix**: a Toffoli whose target is only measured afterwards is replaced by measuring first plus a classically controlled `CZ`; exact on all 3,133,452 inputs and confirmed by the official verifier (invsqrt cost 78,765.51 -> 78,719.53, file `e46d90c3`) | local 27.3024, board 27.30241 |
| 2026-11-14 | [QCC 27.30 \| What Works, What Fails and Why](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-what-works-what-fails-and-why) | analysis notebook: the score and its exchange rates, sixteen measured ideas and why most failed, the diagnosis method, an exact numpy simulator (`kmsim`) and a detector library (`qccscope`); same submission as the 27.307 notebook | bronze medal (owner-reported) |
| 2026-11-14 14:28 | [QCC 27.3122 \| Frontier + Finer Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-27-3122-frontier-finer-chemistry-refit) (v2) | **chemistry weight refit** at fixed coded words (W and H2_I only, all error gates kept): lambda_eff 46.90701 -> 46.90659 (file `2913ca13`) | local 27.3067, board 27.30670 |
| 2026-11-14 20:59 | same notebook (v5) | the refit now runs inside the notebook (numpy GRG optimiser, ~22 min CPU) from the newest public chemistry file, plus manwithacat's new invsqrt circuit `1ba197b0` (our q21 edit plus one more) | local 27.31219, **board 27.31220** |

**Best public score: 27.31220 on 2026-11-14** (QCC 27.3122 notebook, version 5). It was the best public notebook score at the time, just above the previous best public notebook (27.31216).

Medals: bronze for three of the four public notebooks of this competition (LB 25.367, QCC 27.30 Free CZ Fix, QCC 27.30 What Works); the competition closes on 2027-01-20.

## Notebooks in this folder: every public version

Each notebook has its own folder with **all of its public versions** (`v01.ipynb`, `v02.ipynb`, ...) and a README
listing, per version, what changed, the leaderboard score of the submission made from it, and the public notebooks
that use or credit it:

| Notebook | Versions | Folder |
|---|---:|---|
| LB 25.367 \| Verified Portfolio + DQI Readout Fix | 5 | [notebooks/lb-25-367-verified-portfolio-dqi-readout-fix](notebooks/lb-25-367-verified-portfolio-dqi-readout-fix/) |
| QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | 6 | [notebooks/qcc-27-30-public-frontier-free-cz-fix-in-invsq](notebooks/qcc-27-30-public-frontier-free-cz-fix-in-invsq/) |
| QCC 27.30 \| What Works, What Fails and Why | 12 | [notebooks/qcc-27-30-what-works-what-fails-and-why](notebooks/qcc-27-30-what-works-what-fails-and-why/) |
| QCC 27.3122 \| Frontier + Finer Chemistry Refit | 6 | [notebooks/qcc-27-3122-frontier-finer-chemistry-refit](notebooks/qcc-27-3122-frontier-finer-chemistry-refit/) |

Sources were pulled with `kaggle kernels pull asteriospanoras/<slug>/<version>` on 2026-11-15, outputs stripped. They
run on Kaggle (they need the competition's `kickmix` package and other authors' public files as inputs). So that this
repository holds no circuit, weight or local-path data: embedded refitted chemistry weights (base64 blobs) were
replaced by `REMOVED_EMBEDDED_BINARY` (the full cells are on Kaggle), local default paths inside embedded code zips
were removed, and links to earlier notebook names point to the current addresses. No circuit files (`.kmb`, `.kmx`),
weight files (`.npz`) or `submission.zip` are in this repository.

## My leaderboard progression

Public leaderboard scores of my submissions (higher is better). The October entries came from private experiments;
the November ones were each made from a public notebook version listed above.

| Date (UTC) | Public score |
|---|---|
| 2026-10-23 | 1.02199 |
| 2026-10-26 | 15.14394 |
| 2026-10-26 | 19.57899 |
| 2026-10-27 | 21.37712 |
| 2026-10-28 | 22.70030 |
| 2026-10-29 | 22.86838 |
| 2026-10-30 | 22.99563 |
| 2026-10-31 | 23.17996 |
| 2026-11-11 | 25.36727 (LB 25.367 v1) |
| 2026-11-12 | 25.39570 (LB 25.367 v4) |
| 2026-11-12 | 25.40482 (LB 25.367 v5) |
| 2026-11-12 | 25.44953 (QCC 27.30 Free CZ v1) |
| 2026-11-14 | 27.30241 (QCC 27.30 Free CZ v5) |
| 2026-11-14 | 27.30670 (QCC 27.3122 v2) |
| 2026-11-14 | **27.31220** (QCC 27.3122 v5) |

## Evidence that other people used this work

See [`evidence/USES.md`](evidence/USES.md) (table with links) and [`evidence/uses.csv`](evidence/uses.csv).

## Credits

Almost every circuit in these notebooks is other people's public work, credited with links inside each notebook. In
particular: Syed Asad Ali (from-source invsqrt, DQI and chemistry builders), Atakan Aldemir (DQI files, readout
windows, weight updates), maoxin123 (chemistry table, coded words and loaders; the 392k DQI decoder), Heliosli
(chemistry weights, public circuits dataset), Areeb Ali (product retention), Ertuğrul Özer (DQI extractor cutoff),
Ali Haydar Özdağ (invsqrt `4560ac0c`), prvsiyan (refit code), Lera (marculera), Alex Chilton (the verified-portfolio
practice), WCao24, Thomas Gamet, manwithacat (James Barlow), Kirill Tymchishin and the authors credited in their
notebooks. Their code and files keep their authors' licences.
