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
| 2026-11-11 | [LB 25.367 \| Verified Portfolio + DQI Readout Fix](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-07502-wait-daily-reset) (retitled twice since, now "QCC | LB:28.07502 wait daily reset :)") (v1) | **DQI readout-window transplant**: CSWAP readout windows (a `CSWAP` followed by measuring both outputs) rewritten as `CX`/`HMR`/`CZ` with no Toffoli, moved onto Atakan Aldemir's best DQI file: -48 Toffolis per shot (file `245527f6`) | board 25.36727 |
| 2026-11-11 22:58 | same notebook (v4) | **invsqrt splice at clean cuts**: two public 62-qubit circuits (WCao24's normaliser and Thomas Gamet's early prefix) joined where wires and phase agree on every sampled input, -3.0 Toffolis vs the best one (file `9c708f7b`) | local 25.3957, board 25.39570 |
| 2026-11-12 | same notebook (v5) | portfolio refresh with the new public chemistry loaders | local 25.40483 |
| 2026-11-12 | [QCC Circuit Atlas](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) (dataset) | every public circuit file of the competition, deduplicated by SHA-256, with first source, author and all copies; readable text of the circuits; numpy tools | 1,483 downloads at the first check on 2026-11-15, 7,737 at the evening check |
| 2026-11-12 | [QCC 27.30 \| Public Frontier + Free CZ Fix in invsq](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-public-frontier-free-cz-fix-in-invsq) (v1, then titled "QCC 25.449") | portfolio on maoxin123's 392k-Toffoli DQI decoder with our invsqrt splice | local 25.44954, board 25.44953 |
| 2026-11-14 09:47 | same notebook (v5) | **invsqrt dead-write fix**: a Toffoli whose target is only measured afterwards is replaced by measuring first plus a classically controlled `CZ`; exact on all 3,133,452 inputs and confirmed by the official verifier (invsqrt cost 78,765.51 -> 78,719.53, file `e46d90c3`) | local 27.3024, board 27.30241 |
| 2026-11-14 | [QCC 27.30 \| What Works, What Fails and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-06018-what-works-what-fails-and-why) | analysis notebook: the score and its exchange rates, sixteen measured ideas and why most failed, the diagnosis method, an exact numpy simulator (`kmsim`) and a detector library (`qccscope`); same submission as the 27.307 notebook | bronze medal (owner-reported) |
| 2026-11-14 14:28 | [QCC 27.3122 \| Frontier + Finer Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-28-1277-frontier-finer-chemistry-refit) (v2) | **chemistry weight refit** at fixed coded words (W and H2_I only, all error gates kept): lambda_eff 46.90701 -> 46.90659 (file `2913ca13`) | local 27.3067, board 27.30670 |
| 2026-11-14 20:59 | same notebook (v5) | the refit now runs inside the notebook (numpy GRG optimiser, ~22 min CPU) from the newest public chemistry file, plus manwithacat's new invsqrt circuit `1ba197b0` (our q21 edit plus one more) | local 27.31219, **board 27.31220** |
| 2026-11-15 | [QCC \| Atlas Toolkit + In-Notebook Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-07502-wait-daily-reset) (the first notebook above, retitled; v6 to v10) | the best public file of each task (Syed Asad Ali's v13 44-qubit invsqrt and 890-qubit DQI, Lera's chemistry loaders, boristown's refitted weights); **exact LP re-solve of the 34 invsqrt rotation angles** (29 angle literals change, cost 75170.62 -> 75170.13, about +6e-5 of score); the chemistry refit continues inside the notebook with the toolkit imported from the Atlas dataset | v10: local 28.0602, **board 28.06018** (submission 58394704, 17:23 UTC) |
| 2026-11-15 | [QCC 27.30 \| What Works, What Fails and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-06018-what-works-what-fails-and-why) (v13, v14) | new section "This round: what worked, what failed, and why" (the 28.06 portfolio); v13 submitted the same files as the release above, v14 has no submission | v13: board 28.06018 (submission 58398329, 19:23 UTC) |
| 2026-11-15 | [QCC \| LB:28.07502 wait daily reset :)](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-07502-wait-daily-reset) (the first notebook above; v12 to v16) | v13: jeffemerson's `9339eecc` invsqrt (Syed Asad Ali's v13 circuit plus his AND-merge cut), DQI `4b350932`, chemistry `881d9dae`; v15: the same with **my exact-LP re-solved invsqrt rotation angles** (file `f67851ac`, modeled cost 75082.14) | v13: board 28.07495 (submission 58400871, 20:49 UTC); **v15: board 28.07502** (submission 58404020, 22:52 UTC) |
| 2026-11-15 16:19 | [QCC Circuit Atlas + Verified Refit Toolkit](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) v3 | new folder `best/`: the invsqrt with the re-solved angles (`09000960`) and the refitted chemistry table (`5ea23cc0`), with the NOTICE and LICENSE files of their authors (Syed Asad Ali, Lera/marculera) and credits; the loaders of the chemistry circuit are not included (take them from `marculera/dfthc-c44-build`) | |
| 2026-11-16 13:58 | [QCC \| LB:28.07502 wait daily reset :)](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-07502-wait-daily-reset) (v17 to v19) | the notebook re-verifies the **28.09 stack of other authors** (boristown's invsqrt `f2cdab0b` and chemistry weights `0bd9c68f`, the C8 DQI line `ccc2ab84` with boristown's chain patch `00ac37d4`, Lera's loaders): v18 submitted. My LP angle re-solve is not in these files. v17 was not submitted (modeled 28.09488), v19 has no submission file. 43 votes, silver medal as shown on my profile | v18: board 28.09535 (submission 58432668, 13:58 UTC) |
| 2026-11-16 19:25 | [QCC 28.1277 \| Frontier + Finer Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-28-1277-frontier-finer-chemistry-refit) (formerly "QCC 27.3122 ...", v7 to v9) | re-verification of three **other authors' public files** (maoxin123's invsqrt `0af21cb8`, Balram Srinivasan's DQI `66b4f18b`, Atakan Aldemir's chemistry weights `703843d3`, on Lera's loaders); the same files as Pramit Das's public notebook, which scores the same. Nothing in these files is mine | v8: board 28.12769 (submission 58441659, 19:25 UTC) |
| 2026-11-16 | [QCC 28.06018 \| What Works, What Fails and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-06018-what-works-what-fails-and-why) | analysis notebook, **being updated on 16 Nov** (this folder has versions up to 14 only) | no new score listed here |

**Best public score: 28.07502 on 2026-11-15, 22:52 UTC** (the first notebook, now titled "QCC | LB:28.07502 wait daily reset :)", version 15; submission 58404020). Public stacks of other authors reach essentially the same level: kirderf's [vqcc-portfolio-28-08-reproduced](https://www.kaggle.com/code/kirderf/vqcc-portfolio-28-08-reproduced) prints a modeled geometric mean of 28.07503, equal or very slightly better, and it reuses the LP angle re-solve (credited to me) on jeffemerson's circuit together with ozertuu's chemistry refit, so this level is a shared result of several authors, not mine alone. Before that: **28.06018 on 2026-11-15** (version 10; submission 58394704), tied for the best public score of that day, and **27.31220 on 2026-11-14** (QCC 27.3122 notebook, version 5), the best public notebook score at the time, just above the previous best public notebook (27.31216). The jump from 27.31 to 28.06 came from Syed Asad Ali's v13 circuits and Lera's chemistry loaders; my part is listed in the table above.

**Note on the results of 16 Nov 2026.** The first notebook (version 18) scored 28.09535 and carries a silver medal on my profile (43 votes); the frontier notebook (version 8) scored 28.12769 (the same as Pramit Das's public notebook, which it cites). In both, **the files that produce the score are other authors' public files** (boristown, hayatohikawa, Syed Asad Ali, maoxin123, Balram Srinivasan, Atakan Aldemir, Lera), which the notebooks take over, re-verify with the unchanged official verifiers and credit. What is mine in this competition: the exact LP re-solve of the invsqrt rotation angles (adopted or credited by several other portfolios, but not part of the 28.09 and 28.12 files), the analysis notebook, the QCC Circuit Atlas dataset with the refit toolkit, and the earlier edits (readout windows, splice, dead-write fix, chemistry refits). The best public scores of those days therefore say little about my own contribution.

Medals: bronze for all four public notebooks of this competition (the first notebook, first published as LB 25.367 and now titled "QCC | LB:28.07502 wait daily reset :)"; QCC 28.1277 (formerly 27.3122); QCC 27.30 Free CZ Fix; QCC 27.30 What Works); with the S6E11 bronze they made me a Kaggle Notebooks Expert (November 2026); the competition closes on 2027-01-20.

## Notebooks in this folder: every public version

Each notebook has its own folder with **all of its public versions** (`v01.ipynb`, `v02.ipynb`, ...) and a README
listing, per version, what changed, the leaderboard score of the submission made from it, and the public notebooks
that use or credit it:

| Notebook | Versions | Folder |
|---|---:|---|
| QCC \| LB:28.07502 wait daily reset :) (first published as LB 25.367 \| Verified Portfolio + DQI Readout Fix, then titled Atlas Toolkit + In-Notebook Chemistry Refit; the first address redirects to the current one, the middle one no longer does) | 19 | [notebooks/qcc-lb-28-07502-wait-daily-reset](notebooks/qcc-lb-28-07502-wait-daily-reset/) |
| QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | 6 | [notebooks/qcc-27-30-public-frontier-free-cz-fix-in-invsq](notebooks/qcc-27-30-public-frontier-free-cz-fix-in-invsq/) |
| QCC 28.06018 \| What Works, What Fails and Why (first titled QCC 27.30) | 14 | [notebooks/qcc-28-06018-what-works-what-fails-and-why](notebooks/qcc-28-06018-what-works-what-fails-and-why/) |
| QCC 28.1277 \| Frontier + Finer Chemistry Refit (formerly QCC 27.3122; the old address redirects) | 9 | [notebooks/qcc-28-1277-frontier-finer-chemistry-refit](notebooks/qcc-28-1277-frontier-finer-chemistry-refit/) |

Sources were pulled with `kaggle kernels pull asteriospanoras/<slug>/<version>` on 2026-11-15 (updated in the evening of 2026-11-15; versions 12 to 16 of the first notebook added on 2026-11-16; versions 17 to 19 of it and versions 7 to 9 of the frontier notebook added on the night of 2026-11-16; the What Works folder is not refreshed here because that notebook was being updated on 16 Nov), outputs stripped. They
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
| 2026-11-11 | 25.36727 (Atlas Toolkit notebook v1, then titled LB 25.367) |
| 2026-11-12 | 25.39570 (Atlas Toolkit notebook v4) |
| 2026-11-12 | 25.40482 (Atlas Toolkit notebook v5) |
| 2026-11-12 | 25.44953 (QCC 27.30 Free CZ v1) |
| 2026-11-14 | 27.30241 (QCC 27.30 Free CZ v5) |
| 2026-11-14 | 27.30670 (QCC 27.3122 v2) |
| 2026-11-14 | 27.31220 (QCC 27.3122 v5) |
| 2026-11-15 | 28.05955 (a first run of the same design before the release: v13 circuits, re-solved angles, in-notebook chemistry refit) |
| 2026-11-15 | **28.06018** (first notebook v10) |
| 2026-11-15 | 28.06018 (What Works v13, same files) |
| 2026-11-15 | 28.07495 (first notebook v13, 20:49 UTC, submission 58400871) |
| 2026-11-15 | **28.07502** (first notebook v15, 22:52 UTC, submission 58404020; invsqrt `f67851ac`) |
| 2026-11-16 | 28.09535 (first notebook v18, 13:58 UTC, submission 58432668; other authors' files, re-verified) |
| 2026-11-16 | 28.12769 (frontier notebook v8, 19:25 UTC, submission 58441659; other authors' files, re-verified) |

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
