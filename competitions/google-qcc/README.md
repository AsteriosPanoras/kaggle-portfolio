# Google Quantum AI: Verifiable Quantum Circuit Compilation

Competition: [kaggle.com/competitions/google-verifiable-quantum-circuit-compilation](https://www.kaggle.com/competitions/google-verifiable-quantum-circuit-compilation)

**New: [NOTEBOOK_MAP.md](NOTEBOOK_MAP.md)** maps my four notebooks (titles, addresses, what changed in which version, where they stood on the public score, what was mine, what others adopted and what is left in today's best files, and the credit chain of the current best set).

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

A lineage study of what is really mine, what others adopted, its measured effect and what is left of it in today's
best files: [CONTRIBUTIONS.md](CONTRIBUTIONS.md).

All dates UTC, from the run logs of the notebooks. Scores: "board" = public leaderboard score of the submission made
from that notebook version; "local" = geometric mean computed with the unchanged official verifiers inside the notebook
(default salt). The two differ slightly because the board draws its own random DQI shots.

| Date | Notebook | Contribution | Score |
|---|---|---|---|
| 2026-11-11 | [LB 25.367 \| Verified Portfolio + DQI Readout Fix](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-09535) (retitled several times since, now "QCC | LB:28.09535") (v1) | **DQI readout-window transplant**: CSWAP readout windows (a `CSWAP` followed by measuring both outputs) rewritten as `CX`/`HMR`/`CZ` with no Toffoli, moved onto Atakan Aldemir's best DQI file: -48 Toffolis per shot (file `245527f6`) | board 25.36727 |
| 2026-11-11 22:58 | same notebook (v4) | **invsqrt splice at clean cuts**: two public 62-qubit circuits (WCao24's normaliser and Thomas Gamet's early prefix) joined where wires and phase agree on every sampled input, -3.0 Toffolis vs the best one (file `9c708f7b`) | local 25.3957, board 25.39570 |
| 2026-11-12 | same notebook (v5) | portfolio refresh with the new public chemistry loaders | local 25.40483 |
| 2026-11-12 | [QCC Circuit Atlas](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) (dataset) | every public circuit file of the competition, deduplicated by SHA-256, with first source, author and all copies; readable text of the circuits; numpy tools (version 6 of 2026-11-19 adds a `frontier/` folder with the 28.23498 and 28.23837 file sets of other authors, a receipt and their licence notices) | 1,483 downloads at the first check on 2026-11-15, 7,737 at the evening check, 16,100 on 2026-11-20 |
| 2026-11-12 | [QCC 27.30 \| Public Frontier + Free CZ Fix in invsq](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-public-frontier-free-cz-fix-in-invsq) (v1, then titled "QCC 25.449") | portfolio on maoxin123's 392k-Toffoli DQI decoder with our invsqrt splice | local 25.44954, board 25.44953 |
| 2026-11-14 09:47 | same notebook (v5) | **invsqrt dead-write fix**: a Toffoli whose target is only measured afterwards is replaced by measuring first plus a classically controlled `CZ`; exact on all 3,133,452 inputs and confirmed by the official verifier (invsqrt cost 78,765.51 -> 78,719.53, file `e46d90c3`) | local 27.3024, board 27.30241 |
| 2026-11-14 | [QCC 27.30 \| What Works, What Fails and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-23162-what-we-tried-what-failed-and-why) | analysis notebook: the score and its exchange rates, sixteen measured ideas and why most failed, the diagnosis method, an exact numpy simulator (`kmsim`) and a detector library (`qccscope`); same submission as the 27.307 notebook | bronze medal (owner-reported) |
| 2026-11-14 14:28 | [QCC 27.3122 \| Frontier + Finer Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-28-18084-could-be-top-1-public-try-it) (v2) | **chemistry weight refit** at fixed coded words (W and H2_I only, all error gates kept): lambda_eff 46.90701 -> 46.90659 (file `2913ca13`) | local 27.3067, board 27.30670 |
| 2026-11-14 20:59 | same notebook (v5) | the refit now runs inside the notebook (numpy GRG optimiser, ~22 min CPU) from the newest public chemistry file, plus manwithacat's new invsqrt circuit `1ba197b0` (our q21 edit plus one more) | local 27.31219, **board 27.31220** |
| 2026-11-15 | [QCC \| Atlas Toolkit + In-Notebook Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-09535) (the first notebook above, retitled; v6 to v10) | the best public file of each task (Syed Asad Ali's v13 44-qubit invsqrt and 890-qubit DQI, Lera's chemistry loaders, boristown's refitted weights); **exact LP re-solve of the 34 invsqrt rotation angles** (29 angle literals change, cost 75170.62 -> 75170.13, about +6e-5 of score); the chemistry refit continues inside the notebook with the toolkit imported from the Atlas dataset | v10: local 28.0602, **board 28.06018** (submission 58394704, 17:23 UTC) |
| 2026-11-15 | [QCC 27.30 \| What Works, What Fails and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-23162-what-we-tried-what-failed-and-why) (v13, v14) | new section "This round: what worked, what failed, and why" (the 28.06 portfolio); v13 submitted the same files as the release above, v14 has no submission | v13: board 28.06018 (submission 58398329, 19:23 UTC) |
| 2026-11-15 | [QCC \| LB:28.09535 (then titled LB:28.07502 wait daily reset)](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-09535) (the first notebook above; v12 to v16) | v13: jeffemerson's `9339eecc` invsqrt (Syed Asad Ali's v13 circuit plus his AND-merge cut), DQI `4b350932`, chemistry `881d9dae`; v15: the same with **my exact-LP re-solved invsqrt rotation angles** (file `f67851ac`, modeled cost 75082.14) | v13: board 28.07495 (submission 58400871, 20:49 UTC); **v15: board 28.07502** (submission 58404020, 22:52 UTC) |
| 2026-11-15 16:19 | [QCC Circuit Atlas + Verified Refit Toolkit](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) v3 | new folder `best/`: the invsqrt with the re-solved angles (`09000960`) and the refitted chemistry table (`5ea23cc0`), with the NOTICE and LICENSE files of their authors (Syed Asad Ali, Lera/marculera) and credits; the loaders of the chemistry circuit are not included (take them from `marculera/dfthc-c44-build`) | |
| 2026-11-16 13:58 | [QCC \| LB:28.09535 (then titled LB:28.07502 wait daily reset)](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-09535) (v17 to v19) | the notebook re-verifies the **28.09 stack of other authors** (boristown's invsqrt `f2cdab0b` and chemistry weights `0bd9c68f`, the C8 DQI line `ccc2ab84` with boristown's chain patch `00ac37d4`, Lera's loaders): v18 submitted. My LP angle re-solve is not in these files. v17 was not submitted (modeled 28.09488), v19 has no submission file. 43 votes, silver medal as shown on my profile | v18: board 28.09535 (submission 58432668, 13:58 UTC) |
| 2026-11-16 19:25 | [QCC 28.1277 \| Frontier + Finer Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-28-18084-could-be-top-1-public-try-it) (formerly "QCC 27.3122 ...", v7 to v9) | re-verification of three **other authors' public files** (maoxin123's invsqrt `0af21cb8`, Balram Srinivasan's DQI `66b4f18b`, Atakan Aldemir's chemistry weights `703843d3`, on Lera's loaders); the same files as Pramit Das's public notebook, which scores the same. Nothing in these files is mine | v8: board 28.12769 (submission 58441659, 19:25 UTC) |
| 2026-11-16 22:03 | [QCC 28.12769 \| What Works, What Fails and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-23162-what-we-tried-what-failed-and-why) (renamed by me; v15 to v20) | analysis notebook rebuilt around the 28.1277 portfolio (new landscape and family-tree figures); v19 built and re-verified the same **other authors' public files** as the frontier notebook and submitted them | v19: board 28.12769 (submission 58446073, 22:03 UTC) |
| 2026-11-17 02:35 | [QCC 28.1277 \| Frontier + Finer Chemistry Refit](https://www.kaggle.com/code/asteriospanoras/qcc-28-18084-could-be-top-1-public-try-it) (v10 to v15; the title still says 28.1277 until I rename it) | v13 re-verifies and submits **Grant Prater's DQI `61c8348d`** with maoxin123's invsqrt `0af21cb8` and Atakan Aldemir's chemistry weights `703843d3`, all public files of other authors; v10 (boristown's DQI `f425ea20`) scored 28.08843 because that DQI drew a failed shot on the board; v15 takes maoxin123's 4,022-Toffoli chemistry loaders and Grant Prater's `575b043f` and was submitted via the notebook (submission 58466298, 10:59 UTC; score pending when I updated this page, so none is listed) | v13: **board 28.14703** (submission 58452966, 02:35 UTC) |
| 2026-11-17 night | [QCC 28.18084? \| Could Be Top 1 public \| Try It](https://www.kaggle.com/code/asteriospanoras/qcc-28-18084-could-be-top-1-public-try-it) (the frontier notebook above, renamed; v16 to v18) | v18 re-verifies and submits boristown's six-product DQI `5f901c55` (reproduced from his patch script as a byte patch, checked against his file), maoxin123's invsqrt `563d0583` and Atakan Aldemir's weights `703843d3`, all other authors' public files; a tie with boristown's public score, not a gain of mine. v15's board score is 28.15096 (read on 2026-11-18) | v18: board 28.18084 (submission 58485562, 2026-11-18 00:00 UTC) |
| 2026-11-18 | [QCC 28.23162 \| What we tried, what failed and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-23162-what-we-tried-what-failed-and-why) (the analysis notebook above, renamed by me several times; v21 to v26) | v21 rebuilds the 28.18965 frontier of other authors (maoxin123's invsqrt `864f81cd`, boristown's DQI `5f901c55`, leotang09's weights `4d63be3d`) and adds section 8 with three negative scans (invsqrt angles at the LP optimum, rigid chemistry loaders, all 279,577 consecutive same-wire Toffoli pairs of the DQI scanned: the six products of `5f901c55` are all there are); v22 swaps in maoxin123's newer invsqrt `d0227f3c`; v24 uses ozertuu's merged DQI `15a4b740`; v25 ozertuu's newer DQI `e208d350`, clean locally (local 28.23174) but only 28.18862 on the board because the DQI lost shots on the board draw; v26 has submission writing off. All files are other authors' public work; my part is the rebuild, the re-verification, the credits and the scans | v21: board 28.18965 (submission 58505528, 10:30 UTC, a tie); v22: board **28.20041** (submission 58511777, 13:39 UTC; local 28.20043); v24: board **28.23162** (submission 58524618, 20:31 UTC; local 28.23163, a tie with the two public notebooks that use the same DQI); v25: board 28.18862 (submission 58524065, 20:08 UTC) |
| 2026-11-19 | [QCC 28.23162 \| What we tried, what failed and Why](https://www.kaggle.com/code/asteriospanoras/qcc-28-23162-what-we-tried-what-failed-and-why) (the analysis notebook; v27 to v30) | v27 rebuilds the 28.23162 set; **v28 is a fast version** (14 lines) that unpacks the file set of Koushik Rudra's public notebook, checks four SHA-256 values and writes `submission.zip` (invsqrt `ecf908fe`, DQI `4471b493`, chemistry `6ef06081`); v29 is the full analysis around that set, reading it from the new `frontier/` folder of the Atlas dataset, and errored (the Atlas zip was unpacked into a folder), v30 fixes it. **All files are other authors' public work** | v28: board **28.23498** (submission 58557425), a tie with Koushik Rudra's public notebook, not a gain of mine |
| 2026-11-19 | same notebook (v31 to v33) | v31 (fast): ozertuu's file set from his dataset *quantum-sim-linalg-cache* (invsqrt `acc7b9c8`, DQI `f56b04c7`, chemistry `6ef06081`); v32 (full analysis of that set) was cancelled by me; v33 is the full analysis of the 28.23498 set (its section 8 scans still refer to the older files) | v31: board **28.23837** (submission 58574793), a tie with that author's public notebook |
| 2026-11-20 | same notebook (v34, v35; both fast) | v34: the 28.24094 set: manwithacat's DQI `f6b555a6` (HW-31 clean inverses), ozertuu's invsqrt `acc7b9c8`, Manvender Singh's chemistry `6ef06081`; v35: Ghazaros Barseghyan's 28.24398 set from his notebook *vqcc-28-24398-leaf-port* (invsqrt `d0a9a694`, goodpjw2008's DQI `db0a845f`, chemistry `6ef06081`). Files of other authors, re-packaged and credited | v34: board **28.24094** (submission 58581362), a tie with the public notebooks of ozertuu and manwithacat; v35: submission 58608424, score pending when I wrote this, none listed |

**Best public score of a notebook of mine: 28.24396 on 2026-11-20** (the analysis notebook, version 35, submission 58608424, read with `kaggle competitions submissions`; before it 28.24094 with version 34 (submission 58581362), 28.23837 with version 31 and 28.23498 with version 28, 2026-11-19). **These are fast versions that only re-package the public file sets of Koushik Rudra, ozertuu and manwithacat, each a tie with those authors' public notebooks, not a gain of mine; the top scores of this competition come from other authors' circuits, and what is mine is the analysis, the tools, the Atlas and the earlier LP, readout and dead-write work.** Best score of a full analysis version: 28.23162 on 2026-11-18, 20:31 UTC (version 24, submission 58524618; before it, 28.20041 with version 22, submission 58511777). **That one is built from other authors' public files** (maoxin123's invsqrt `d0227f3c`, ozertuu's merged DQI `15a4b740`, leotang09's chemistry weights `4d63be3d`), which the notebook re-verifies and credits; it is the same level other authors' notebooks reach. Earlier: 28.18965 (version 21), 28.18084 (frontier notebook version 18, a tie with boristown's public score) and 28.14703 on 2026-11-17 (frontier notebook version 13). **Lesson of 18 Nov:** ozertuu's DQI `e208d350` was clean locally (local geometric mean 28.23174, 0 errors in 102,400 shots) yet my submission with it scored only 28.18862 (submission 58524065), because the DQI lost shots on the board's draw; only reuse DQI files that already have a board score. **Best score with my own file edits: 28.07502 on 2026-11-15, 22:52 UTC** (the first notebook, now titled "QCC | LB:28.07502 wait daily reset :)", version 15; submission 58404020). Public stacks of other authors reach essentially the same level: kirderf's [vqcc-portfolio-28-08-reproduced](https://www.kaggle.com/code/kirderf/vqcc-portfolio-28-08-reproduced) prints a modeled geometric mean of 28.07503, equal or very slightly better, and it reuses the LP angle re-solve (credited to me) on jeffemerson's circuit together with ozertuu's chemistry refit, so this level is a shared result of several authors, not mine alone. Before that: **28.06018 on 2026-11-15** (version 10; submission 58394704), tied for the best public score of that day, and **27.31220 on 2026-11-14** (QCC 27.3122 notebook, version 5), the best public notebook score at the time, just above the previous best public notebook (27.31216). The jump from 27.31 to 28.06 came from Syed Asad Ali's v13 circuits and Lera's chemistry loaders; my part is listed in the table above.

**Note on the results of 16 Nov 2026.** The first notebook (version 18) scored 28.09535 and carries a silver medal on my profile (43 votes); the frontier notebook (version 8) scored 28.12769 (the same as Pramit Das's public notebook, which it cites). In both, **the files that produce the score are other authors' public files** (boristown, hayatohikawa, Syed Asad Ali, maoxin123, Balram Srinivasan, Atakan Aldemir, Lera), which the notebooks take over, re-verify with the unchanged official verifiers and credit. What is mine in this competition: the exact LP re-solve of the invsqrt rotation angles (adopted or credited by several other portfolios, but not part of the 28.09 and 28.12 files), the analysis notebook, the QCC Circuit Atlas dataset with the refit toolkit, and the earlier edits (readout windows, splice, dead-write fix, chemistry refits). The best public scores of those days therefore say little about my own contribution.

Medals (kept as stated in the repository before; state of 2026-11-17, except the frontier notebook, which showed silver with 52 votes on 2026-11-18; not re-checked on 2026-11-20, the owner states medals only through the Kaggle UI): bronze for all four public notebooks of this competition (the first notebook, first published as LB 25.367 and now titled "QCC | LB:28.09535"; QCC 28.1277 (formerly 27.3122); QCC 27.30 Free CZ Fix; QCC 27.30 What Works); with the S6E11 bronze they made me a Kaggle Notebooks Expert (November 2026); the competition closes on 2027-01-20.

## Notebooks in this folder: every public version

Each notebook has its own folder with **all of its public versions** (`v01.ipynb`, `v02.ipynb`, ...) and a README
listing, per version, what changed, the leaderboard score of the submission made from it, and the public notebooks
that use or credit it:

| Notebook | Versions | Folder |
|---|---:|---|
| QCC \| LB:28.09535 (formerly QCC \| LB:28.07502 wait daily reset :), first published as LB 25.367 \| Verified Portfolio + DQI Readout Fix, then titled Atlas Toolkit + In-Notebook Chemistry Refit; the first address redirects to the current one, the middle one no longer does) | 19 | [notebooks/qcc-lb-28-07502-wait-daily-reset](notebooks/qcc-lb-28-07502-wait-daily-reset/) |
| QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | 6 | [notebooks/qcc-27-30-public-frontier-free-cz-fix-in-invsq](notebooks/qcc-27-30-public-frontier-free-cz-fix-in-invsq/) |
| QCC 28.23162 \| What we tried, what failed and Why (first titled QCC 27.30, then QCC 28.06018, then QCC 28.12769, among other renamings; the folder keeps the 28.12769 slug; the two oldest addresses redirected when checked) | 35 | [notebooks/qcc-28-12769-what-works-what-fails-and-why](notebooks/qcc-28-12769-what-works-what-fails-and-why/) |
| QCC 28.18084? \| Could Be Top 1 public \| Try It (formerly QCC 28.1277 \| Frontier + Finer Chemistry Refit, before that QCC 27.3122; the folder keeps the 28.1277 slug) | 18 | [notebooks/qcc-28-1277-frontier-finer-chemistry-refit](notebooks/qcc-28-1277-frontier-finer-chemistry-refit/) |

Sources were pulled with `kaggle kernels pull asteriospanoras/<slug>/<version>` on 2026-11-15 (updated in the evening of 2026-11-15; versions 12 to 16 of the first notebook added on 2026-11-16; versions 17 to 19 of it and versions 7 to 9 of the frontier notebook added on the night of 2026-11-16; versions 15 to 20 of the What Works notebook and versions 10 to 15 of the frontier notebook added on 2026-11-17; versions 21 to 26 of the What Works notebook and versions 16 to 18 of the frontier notebook added on 2026-11-18, with their address renamed as listed; versions 27 to 35 of the What Works notebook added on 2026-11-20), outputs stripped. They
run on Kaggle (they need the competition's `kickmix` package and other authors' public files as inputs). So that this
repository holds no circuit, weight or local-path data: embedded refitted chemistry weights and embedded invsqrt or DQI patch strings (base64 blobs) were
replaced by `REMOVED_EMBEDDED_BINARY` (the full cells are on Kaggle), local default paths inside embedded code zips
were removed, and links to earlier notebook names point to the current addresses. No circuit files (`.kmb`, `.kmx`),
weight files (`.npz`) or `submission.zip` are in this repository.

## My leaderboard progression

Which notebook each version belongs to, and what each notebook contained in each phase: [NOTEBOOK_MAP.md](NOTEBOOK_MAP.md).

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
| 2026-11-16 | 28.12769 (analysis notebook v19, 22:03 UTC, submission 58446073; the same files) |
| 2026-11-17 | **28.14703** (frontier notebook v13, 02:35 UTC, submission 58452966; Grant Prater's DQI `61c8348d` with maoxin123's invsqrt and Atakan Aldemir's weights, re-verified) |
| 2026-11-17 | 28.15096 (frontier notebook v15, 10:59 UTC, submission 58466298; other authors' files) |
| 2026-11-18 | 28.18084 (frontier notebook v18, 00:00 UTC, submission 58485562; boristown's DQI `5f901c55`, a tie with his public score) |
| 2026-11-18 | 28.18965 (analysis notebook v21, 10:30 UTC, submission 58505528; a tie with the public frontier) |
| 2026-11-18 | **28.20041** (analysis notebook v22, 13:39 UTC, submission 58511777; maoxin123's invsqrt `d0227f3c`, other authors' files, re-verified) |
| 2026-11-18 | 28.18862 (analysis notebook v25, 20:08 UTC, submission 58524065; ozertuu's DQI `e208d350` lost shots on the board draw) |
| 2026-11-18 | analysis notebook v24, 20:31 UTC, submission 58524618: board 28.23162 |
| 2026-11-19 | 28.23498 (analysis notebook v28, 11:19 UTC, submission 58557425; Koushik Rudra's file set, a tie with his public notebook) |
| 2026-11-19 | 28.23837 (analysis notebook v31, 18:35 UTC, submission 58574793; ozertuu's set, same bytes) |
| 2026-11-19 | 28.24094 (analysis notebook v34, 22:13 UTC, submission 58581362; manwithacat's DQI `f6b555a6`, ozertuu's invsqrt, other authors' chemistry) |
| 2026-11-20 | 28.24396 (analysis notebook v35, 10:27 UTC, submission 58608424; Ghazaros Barseghyan's 28.24398 set) |
| 2026-11-20 | 31.68159 (analysis notebook v36, 17:56 UTC, submission 58626935; team ThemBones' circuits with almondlabs' chemistry, a tie with the public file set) |
| 2026-11-20 | 31.68159 (Free CZ notebook v12, 20:05 UTC, submission 58633905; the same set) |
| 2026-11-20 | 31.69052 (analysis notebook v38, 20:21 UTC, submission 58634575; the Almond Labs 31.69054 set) |
| 2026-11-20 | 31.69052 (Free CZ notebook v14, 21:05 UTC, submission 58635907; the same bytes) |
| 2026-11-21 | **33.06908** (analysis notebook v44, 00:53 UTC, submission 58643150; per task: Rithvik Redrouthu's invsqrt and chemistry, tonylica's DQI; the combination is mine, every file is theirs; the same score as three other teams) |
| 2026-11-21 | **33.10186** (Free CZ notebook v18, 11:16 UTC, submission 58663801; goodpjw2008's file set, a tie with his public notebook of the same score; boristown's notebook of that day reports 33.10189) |
| 2026-11-21 | 33.10185 (Free CZ notebook v21, 13:03 UTC, submission 58669649; boristown's set, 33.10189 in his notebook) |
| 2026-11-21 | **33.13514** (Free CZ notebook v22, 13:46 UTC, submission 58670546; maoxin123's 33.135 set, a tie with his public notebook) |

## Evidence that other people used this work

See [`evidence/USES.md`](evidence/USES.md) (table with links) and [`evidence/uses.csv`](evidence/uses.csv).

On 2026-11-17: 68 public notebooks by 49 other authors use or credit my work (167 evidence rows); 58 notebooks by 42 authors credit me by name in their text, 33 notebooks by 27 authors ship files I published first (found by the all-versions scan of 15 Nov; later scans read latest versions and sources only, no outputs), and 13 notebooks by 11 authors have one of my notebooks or my dataset as an input. The six notebooks added on 2026-11-17 credit me by name; none of them says that it ships one of my files.

**Scan of 2026-11-18 (evening), five notebooks, source and Kaggle metadata read after `kaggle kernels pull`; not a full rescan, so the counts above are unchanged.** [maoxin123](https://www.kaggle.com/code/maoxin123/qcc-28-20-4-022-toffoli-chemistry-loaders) ("QCC 28.20 | 4,022-Toffoli chemistry loaders") credits in its text "the weight-refit work of prvsiyan, Asterios Panoras, Ertuğrul Özer (ozertuu)" and "measured-CZ / dead-write ideas by Asterios Panoras and James Barlow". ozertuu's [28.23163 SOTA Verified Compilation | Top Portfolio](https://www.kaggle.com/code/ozertuu/28-23163-sota-verified-compilation-top-portfolio) and [Quantum AI Fast Runner Starter Notebook](https://www.kaggle.com/code/ozertuu/quantum-ai-fast-runner-starter-notebook) both attach my dataset `asteriospanoras/qcc-circuit-atlas` as an input and name Asterios Panoras in their credits list. Balram Srinivasan's [VQCC cand 28199 submit](https://www.kaggle.com/code/balramsrinivasan/vqcc-cand-28199-submit) and Ratnachand Kancharla's [VQCC verified floor and circuit anatomy](https://www.kaggle.com/code/ratnachand/vqcc-verified-floor-and-circuit-anatomy) do not mention me in the notebook source; a credit in Balram's dataset README, if there is one, I did not check.

## Credits

Almost every circuit in these notebooks is other people's public work, credited with links inside each notebook. In
particular: Syed Asad Ali (from-source invsqrt, DQI and chemistry builders), Atakan Aldemir (DQI files, readout
windows, weight updates), maoxin123 (chemistry table, coded words and loaders; the 392k DQI decoder), Heliosli
(chemistry weights, public circuits dataset), Areeb Ali (product retention), Ertuğrul Özer (DQI extractor cutoff),
Ali Haydar Özdağ (invsqrt `4560ac0c`), prvsiyan (refit code), Lera (marculera), Alex Chilton (the verified-portfolio
practice), WCao24, Thomas Gamet, manwithacat (James Barlow), Kirill Tymchishin and the authors credited in their
notebooks. Their code and files keep their authors' licences.
