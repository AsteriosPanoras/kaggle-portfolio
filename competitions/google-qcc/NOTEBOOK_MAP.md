# Which notebook is which: a map of my Google QCC notebooks (state of 2026-11-21)

Competition: [google-verifiable-quantum-circuit-compilation](https://www.kaggle.com/competitions/google-verifiable-quantum-circuit-compilation)

I published **four public notebooks** in this competition (plus private helper notebooks, see the end). Each was
renamed several times and **its content changed with its title**: the same notebook began as a "run it" release, became
an analysis, then re-packaged other authors' public file sets, and the newest versions are explainers. This page
gives the identity of each notebook, what it contained in each phase, and what I did and did not contribute in each.
Nothing here claims a circuit that is not mine: **every circuit behind every score above 27.31 is other authors' public
work** (see [CONTRIBUTIONS.md](CONTRIBUTIONS.md), section 8).

Evidence labels as in CONTRIBUTIONS.md: **VERIFIED** (I read the source, log, receipt or Kaggle page myself),
**REPORTED** (another page of this repository says so), **Judgment** (my assessment).

## 1. Today's identity of the four notebooks

Addresses, titles and votes read with `kaggle kernels list --mine` on 2026-11-21 (VERIFIED). Older addresses redirect
on Kaggle; the folders in this repository keep the first address they were stored under.

| Short name used here | Address today | Title today | Votes | Medal (as last read) | Versions | Folder in this repo |
|---|---|---|---:|---|---:|---|
| **A. First notebook** | [qcc-lb-28-09535](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-09535) | QCC \| LB:28.09535 | 44 | silver | 19 | [qcc-lb-28-07502-wait-daily-reset](notebooks/qcc-lb-28-07502-wait-daily-reset/) |
| **B. Frontier notebook** | [qcc-28-18084-could-be-top-1-public-try-it](https://www.kaggle.com/code/asteriospanoras/qcc-28-18084-could-be-top-1-public-try-it) | QCC 28.18084? \| Could Be Top 1 public \| Try It | 53 | silver | 18 | [qcc-28-1277-frontier-finer-chemistry-refit](notebooks/qcc-28-1277-frontier-finer-chemistry-refit/) |
| **C. Analysis / credits notebook** | [qcc-33-25060-best-public-merge-and-credits](https://www.kaggle.com/code/asteriospanoras/qcc-33-25060-best-public-merge-and-credits) | QCC 33.25060 \| Best public merge and credits | 72 | silver (the owner reports 21+ votes before the rename; not re-checked) | 53 | [qcc-28-12769-what-works-what-fails-and-why](notebooks/qcc-28-12769-what-works-what-fails-and-why/) |
| **D. "Free CZ Fix" notebook** | [qcc-33-1933-ablation-floors-human-vs-ai-next](https://www.kaggle.com/code/asteriospanoras/qcc-33-1933-ablation-floors-human-vs-ai-next) | QCC 33.1933 \| Ablation, Floors, Human vs AI, Next? | 38 | bronze (earlier state, not re-checked) | 36 | [qcc-27-30-public-frontier-free-cz-fix-in-invsq](notebooks/qcc-27-30-public-frontier-free-cz-fix-in-invsq/) |

Row D, row C and its vote count were read again on 2026-11-25. Notebook C was renamed four times that day in the Kaggle interface (`qcc-33-06908-best-public-score-and-credits` -> `qcc-33-21880-best-public-score-and-credits`, a typo for 33.2118 that was corrected the same afternoon -> `qcc-33-2118-who-built-the-public-best-set` -> `qcc-33-25060-who-built-the-public-best-set` -> `qcc-33-25060-best-public-merge-and-credits`, the last two after the merge); the title no longer says "best public score", because the files are other authors' and the page is about who built them. the other rows are as of 2026-11-21. Notebook D was renamed three more times in the Kaggle interface (`qcc-33-1-` -> `qcc-33-1439-` -> `qcc-33-1702-` -> `qcc-33-1707-` -> `qcc-33-1933-ablation-floors-human-vs-ai-next`); each time the push folder had to use the new address, otherwise Kaggle would have created a second notebook.

Medals are shown on the owner's Kaggle profile; they were not re-derived on 2026-11-21 (the owner states medals only
through the Kaggle interface).

## 2. What each notebook was, phase by phase

### A. First notebook (versions 1 to 19, 2026-11-11 to 2026-11-16)

| Phase | Versions | Title at the time | Content | Part of it mine |
|---|---|---|---|---|
| 1 | 1-5 | LB 25.367 \| Verified Portfolio + DQI Readout Fix | public frontier files, the DQI readout-window transplant `245527f6`, the invsqrt splice `9c708f7b` | the transplant and the splice (methods and files) |
| 2 | 6-11 | QCC \| Atlas Toolkit + In-Notebook Chemistry Refit | chemistry weight refit run inside the notebook with the Atlas toolkit; release v10 scored **28.06018** | the refit port, the exact LP angle re-solve (`09000960`) |
| 3 | 12-16 | QCC \| LB:28.07502 wait daily reset :) | jeffemerson's `9339eecc` with my LP-re-solved angles (`f67851ac`); v15 scored **28.07502** | the angle re-solve |
| 4 | 17-19 | QCC \| LB:28.09535 | boristown's 28.095 stack, re-verified and submitted (28.09535) | assembly and checks only |

### B. Frontier notebook (versions 1 to 18, 2026-11-14 to 2026-11-18)

| Phase | Versions | Title at the time | Content | Part of it mine |
|---|---|---|---|---|
| 1 | 1-6 | QCC 27.307 / 27.3122 \| Frontier + Finer Chemistry Refit | maoxin123's frontier with my finer chemistry refit; v5 scored **27.31220** (best public notebook score when released, REPORTED) | the refit |
| 2 | 7-14 | QCC 28.1277 \| Frontier + Finer Chemistry Refit | Balram Srinivasan's DQI, maoxin123's invsqrt, Atakan Aldemir's weights; v13 scored **28.14703** with Grant Prater's DQI | none of the three files |
| 3 | 15-18 | QCC 28.18084? \| Could Be Top 1 public \| Try It | 4,022-Toffoli loaders (maoxin123), boristown's six-product DQI rebuilt from his patch script; v18 scored **28.18084** | assembly and checks only |

### C. Analysis / credits notebook (versions 1 to 53, 2026-11-11 to 2026-11-25)

| Phase | Versions | Title at the time | Content | Part of it mine |
|---|---|---|---|---|
| 1 | 1-5 | QCC 27.30 \| What Works, What Fails and Why | toolkit: exact simulator, cost anatomy, what works and what fails | analysis and tools |
| 2 | 6-20 | QCC 28.06018 / 28.12769 \| What Works, What Fails and Why | analysis rebuilt around the 28.06 and 28.1277 portfolios | analysis and tools |
| 3 | 21-27 | QCC 28.23162 \| What we tried, what failed and Why | score anatomy, sixteen ideas, three negative scans; v24 scored **28.23162** | analysis, negative scans |
| 4 | 28-35 | (same, then 28.24396) | **fast versions**: unpack another author's public file set, SHA-256 check, write `submission.zip`; scores 28.23498, 28.23837, 28.24094, 28.24396 | none: ties with the public notebooks of the same files |
| 5 | 36-38 | QCC 31.68159 / 31.69052 | fast versions of the ThemBones + almondlabs set (v36, 31.68159) and of the Almond Labs set (v38, 31.69052) | none: ties |
| 6 | 39-41 | QCC 31.69052 \| Best public score and credits | static page: who is responsible for each part of the best score, the ideas in plain words, 24 linked credits | the page and its checks |
| 7 | 42-45 | QCC 33.06908 \| Best public score and credits | v42 and v43 packaged tonylica's and Rithvik Redrouthu's sets (no submission); v44 combined, per task, Rithvik Redrouthu's invsqrt and chemistry with tonylica's DQI and scored **33.06908**; v45 is the final text with no submission file | none of the files; the choice of files is mine |
| 8 | 46-50 | QCC 33.06908 -> 33.21880 -> QCC 33.2118 \| Who Built the Public Best Set? | the page **runs** the three unmodified official verifiers on the 18 files of the best public set (v46-48: the 33.21180 set of zhuangbility; v49-50: the 33.24213 set of goodpjw2008, version 18), a DQI salt sweep (default and five more salts), a table of what 0.01 points are worth; new opening (picture, five cards, staircase chart), updated credits. v46 and v49 wrote `submission.zip` and were submitted (**33.21180**, submission 58882874, and **33.24213**, submission 58891190, 2026-11-25 13:58 UTC); v47, v48 and v50 write none (v50 is the final text) | the page, the verifier runs and the salt study; the files are other authors' |
| 9 | 51-53 | same (title: QCC 33.25060 \| Best public merge and credits) | **a merge of two public sets**, task by task: the chemistry (loaders and table) of goodpjw2008's version 19 (33.25057 in his notebook), the DQI `b183c793` of logiclab's *V58 Submission* (33.24216), the invsqrt `6b592145` that both ship; the page finds each member by SHA-256 in several source zips, runs the official verifiers and six salts. v51 failed on a slip of mine (a builder variable inside the notebook code, found in one minute, no submission lost); v52 wrote `submission.zip` and was submitted (**33.25060**, submission 58900425, 2026-11-25 17:05 UTC); v53 is the final text without a submission file | the merge itself, the page and the verifier runs; none of the circuits is mine |

### D. "Free CZ Fix" notebook (versions 1 to 36, 2026-11-12 to 2026-11-25)

| Phase | Versions | Title at the time | Content | Part of it mine |
|---|---|---|---|---|
| 1 | 1-6 | QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | the invsqrt dead-write fix (one Toffoli fewer per shot, exact), shipped in 14 public notebooks; v5 scored **27.30241** | the edit at that site |
| 2 | 7-13 | renamed during these versions to QCC 31.68 \| What we tried, what failed and why | measured experiments of 19-20 Nov on the public ThemBones files (110th inverse site, dead-tail DQI edits, invsqrt tightness, qubit census, chemistry loaders), pricing table; v12 re-packaged the 31.68159 set (**31.68159**, tie) | the experiments and their negative results |
| 3 | 14-15 | QCC 31.69052 \| What we tried, what failed and why | same page; v14 submitted the Almond Labs set (**31.69052**, tie); v15 reads Atlas only, no submission file | as above |
| 4 | 16-23 | QCC 33.1 \| Ablation, Floors, Human vs AI, Next? | explainer: system map, ablation by task and by idea, floors per lever, investment table, human insight vs AI search with four worked examples and research basis, then the earlier experiments; v18 submitted goodpjw2008's set (**33.10186**, tie with his public notebook); v21 submitted boristown's set (**33.10185** on the board), v22 maoxin123's 33.135 set (**33.13514**, tie with his public notebook); v19, v20 and v23 are final versions with no submission file | the explanation, the arithmetic and the experiments |
| 5 | 24-36 | QCC 33.1 -> 33.1439 -> 33.1702 -> 33.1707 -> 33.1933 \| Ablation, Floors, Human vs AI, Next? | same explainer; the three-line step: find the best public file set, push a version that writes `submission.zip` from that notebook's output (hash-checked), submit through the notebook, then push a final version with no submission file. Submitted: v25 (**33.13517**), v26 (33.13869), v27 (**33.14394**), v29 to v35 (33.17023, 33.17029 twice, 33.17033, 33.17067, 33.19326, **33.21011**); v28, v36 and the other versions are finals with no submission file; the staircase paragraph was extended each time | the explanation; the files are other authors' |

Versions 16, 18, 21, 22, 25 to 27 and 29 to 35 of D, and versions 42 to 44 of C, wrote a `submission.zip` into their output (needed to submit
through the notebook), and so did versions 46, 49 and 52 of C; the final versions (D v19, v20, v23, v24, v28, v36 and C v45, v47, v48, v50, v53) write none.

## 3. Where my notebooks stood on the public score

"Public notebook score" below means the score shown for notebooks of the competition at the time; "tie" means another
author's public notebook had the same files and the same score. Rank on the competition leaderboard is not claimed:
on 2026-11-21 the top of the leaderboard is 33.34845 (team Z³C¹oherence, VERIFIED with
`kaggle competitions leaderboard`; I found no public notebook with that score), above every public notebook I read.

| Date (UTC) | Notebook, version | Score | Position of the notebook score when released | Whose files |
|---|---|---|---|---|
| 2026-11-12 | D v1 | 25.44953 | **not first**: 78 teams had 25.44953 about 4 hours before my notebook (REPORTED) | other authors + my splice |
| 2026-11-14 | B v5 | **27.31220** | **best public notebook score when released** (REPORTED, README of 2026-11-17) | other authors + my refit and dead-write fix |
| 2026-11-15 | A v10 | **28.06018** | **tied for the best public score of that day** (REPORTED) | other authors + my LP angles |
| 2026-11-15 | A v15 | 28.07502 | a level other authors reach as well | other authors + my LP angles |
| 2026-11-16 to 11-18 | A v18, B v8/v13/v15/v18, C v19/v21/v22/v24 | 28.09535 to 28.23162 | ties with public files; **no lead of mine claimed** | other authors' files, re-verified |
| 2026-11-19 to 11-20 | C v28, v31, v34, v35 | 28.23498, 28.23837, 28.24094, 28.24396 | ties with the public notebooks of the same files | other authors' files |
| 2026-11-20 | C v36, D v12 | 31.68159 | tie | team ThemBones + almondlabs |
| 2026-11-20 | C v38, D v14 | 31.69052 | tie with Almond Labs (31.69054 in their notebook) | Almond Labs on ThemBones |
| 2026-11-21 | C v44 | 33.06908 | tie with three teams on the board; the combination was assembled by me from public files | Rithvik Redrouthu + tonylica |
| 2026-11-21 | D v18 | 33.10186 | tie with goodpjw2008's public notebook (33.10186) | goodpjw2008's set |
| 2026-11-21 | D v21 | 33.10185 | boristown's notebook [VQCC 33.102 LB \| DAG Splicing](https://www.kaggle.com/code/boristown/vqcc-33-102-lb-dag-splicing-visual-guide) reports 33.10189 locally; on the board the same set gave 33.10185 (noise of the DQI draw, about 0.00004) | boristown's set |
| 2026-11-21 | D v22 | **33.13514** | **tie with maoxin123's public notebook (33.13514), the public best of that day**; the top of the leaderboard (33.34845) is above it | maoxin123's 33.135 set |
| 2026-11-21 | D v25 | 33.13517 | goodpjw2008's set: maoxin123's loaders with the table of leotang09 and goodpjw2008, 33.13521 in his notebook | see section 5 |
| 2026-11-22 | D v26 | 33.13869 | Areeb Ali's set with 3,372-Toffoli loaders | see section 5 |
| 2026-11-22 | D v27 | **33.14394** | goodpjw2008's set: varianceofx's and mizeroluckygall's three-T invsqrt, 3,372 loaders, table refit with leotang09; the public best when submitted | see section 5 |
| 2026-11-22 | D v29 | 33.17023 | maoxin123's 33.17 set: 3,357-Toffoli loaders | see section 5 |
| 2026-11-22 | D v30 | 33.17029 | Areeb Ali's 33.17029 set (maoxin123's loaders with a refitted table) | see section 5 |
| 2026-11-22 | D v31 | 33.17029 | ozertuu's 33.17033 set; the board gave 33.17029 (same circuits, DQI shot draw) | see section 5 |
| 2026-11-23 | D v32 | 33.17033 | evgendvorkin's set: his DQI `1e6787a0` with the refitted table; the board confirmed his 33.17033 | see section 5 |
| 2026-11-23 | D v33 | 33.17067 | goodpjw2008's set: DQI `6f78ecdd` with zero-test cuts | see section 5 |
| 2026-11-24 | D v34 | 33.19326 | ozertuu's SOTA Apex set (reproduced by Areeb Ali in *The 26-Toffoli Cut*): shorter loaders and a refitted table | see section 5 |
| 2026-11-24 | D v35 | **33.21011** | goodpjw2008's *Shorter Chemistry Loaders* set (ten loaders re-solved by goodpjw2008, five by maoxin123, table `573d10be`); a tie with his public notebook | see section 5 |
| 2026-11-25 | C v46 | **33.21180** | the 33.21180 set of zhuangbility (Areeb Ali reproduced the same bytes): prvsiyan's invsqrt `6b592145`, DQI `6f78ecdd`, goodpjw2008's 3,333-Toffoli loaders, zhuangbility's table `6ac46e3e`; submission 58882874, a tie with their public notebooks | see section 5 |
| 2026-11-25 | C v49 | **33.24213** | goodpjw2008's version 18 (*Shorter Chemistry Loaders*, 3,315 Toffolis per pass, new values for the dead words, weights continued from evgendvorkin's refit; invsqrt and DQI as in the 33.21180 set); submission 58891190, a tie with his public notebook | see section 5 |
| 2026-11-25 | C v52 | **33.25060** | merge: goodpjw2008's version 19 chemistry (3,310 Toffolis per pass, T 13,120, lambda_eff 46.914304) + logiclab's DQI `b183c793` + prvsiyan's invsqrt `6b592145`; submission 58900425; +0.00003 over goodpjw2008's own 33.25057, inside the board's salt noise | see section 5 |

The full list of 50 submissions (including the October ones) with their descriptions is `kaggle competitions submissions` (VERIFIED on 2026-11-21);
the scores of my November notebooks are in the [progression table](README.md#my-leaderboard-progression).

## 4. What I offered, what helped others, what is left in the final solutions

Sources: [CONTRIBUTIONS.md](CONTRIBUTIONS.md) (lineage study of 2026-11-18, with the byte-level test of section 4.1),
[evidence/USES.md](evidence/USES.md), and the scan of 2026-11-21 below.

| What I contributed | Date | Adopted or credited by (examples) | In the files of the best public sets today |
|---|---|---|---|
| DQI readout-window transplant `245527f6` | 11 Nov | rebuilt byte for byte by Atakan Aldemir (REPORTED); 2 notebooks ship it | **no**: decoder line replaced on 12 Nov |
| invsqrt splice at clean cuts `9c708f7b` | 11 Nov | 21 notebooks of 18 authors ship it; the public top of 12 Nov (REPORTED) | **no**: superseded the same week |
| invsqrt dead-write fix `e46d90c3` (-1 Toffoli) | 14 Nov | 8 notebooks ship it; manwithacat's `1ba197b0` contains it plus one edit | **no** (byte test, VERIFIED, 18 Nov): the site no longer exists in the 44-qubit line |
| exact **LP re-solve of the invsqrt rotation angles** | 15 Nov | credited as prior art by Almond Labs (21 Nov scan, VERIFIED), by almondlabs' earlier notebook, by hayatohikawa and by ThemBones in the credits of their release (REPORTED); **the credit is also in the NOTICE file of ThemBones' public generators dataset, which is copied into `rupam2020/qcc-no-bodies-milestone` (an input of the two top public notebooks of 2026-11-21) and four more datasets** (VERIFIED, [USES.md](evidence/USES.md), datasets section) | **the idea, not the bytes**: ThemBones' invsqrt solves its 33 angles by an LP for the largest margin; none of my angle values is in the files (byte test of 18 Nov; none of my 11 file hashes is among the 18 members of the 33.10186 set, VERIFIED 21 Nov) |
| chemistry weight refits `54bc3e71`, `2913ca13`, `5a753866` (numpy port of prvsiyan's method) | 14 Nov | notebooks of manwithacat, areebbb, junthewise, rdaccel, ahoirg, leotang09 (REPORTED) | **no**: later weights by other authors; the refit method lives on in the 31.69 and 33.10 chemistry files as other authors' work |
| **QCC Circuit Atlas** dataset and tools (`kmsim`, `qccscope`, refit toolkit, `frontier/`) | 12-20 Nov | attached as input by **10 notebooks of 6 other authors** on 2026-11-21 (ahoirg, kawh1111, mizeroluckygall, ozertuu x3, priyanshurajpgiit x2, thomasgamet); its `kmsim` simulator is reused unmodified in cosmorin's dataset and listed in manwithacat's toolkit; the Atlas `frontier/` folder holds the 28.23-31.69 file sets with credits | n/a (not a circuit); 16,100+ downloads |
| analysis and **negative results** (110th site, dead-tail DQI edits, invsqrt tightness, qubit census, chemistry loaders, 19-20 Nov) | 14-21 Nov | manwithacat's public dataset [vqcc-chemistry-negative-results](https://www.kaggle.com/datasets/manwithacat/vqcc-chemistry-negative-results) **catalogues five of them** (rows NR-0305 to NR-0309: LP optimum of the invsqrt angles, no rotation or T gate droppable, 0 of 1,548 Toffolis removable, the DQI retained-product scan, the chemistry loader greedy search) with a link to my notebook, tier "author-reported", dated 2026-11-19 (VERIFIED 2026-11-21); I found no notebook that cites one to skip work; goodpjw2008's 33.10186 notebook reports its own independent negative checks (e.g. the table size C 46 to 45 stalls at error_2 21.6 mHa) | n/a |
| the practice of **submitting through the public notebook with hash-pinned inputs and `WRITE_SUBMISSION = False`** | 11 Nov on | not measured (Alex Chilton's verified-portfolio notebooks already used hash pinning before mine) | n/a |

**Plain summary.** I was early with several small, exact edits that others adopted within hours; every one of them was
superseded by a better file from another author within days, and **no byte of my edits is in the best public files of
2026-11-21** (VERIFIED for the file hashes; the byte test of section 4.1 of CONTRIBUTIONS.md was not repeated on the
31.68 to 33.10 files, so influence that left no bytes behind cannot be excluded or measured). What remains visible is
credit for the **LP angle re-solve as an idea** (Almond Labs, almondlabs, ThemBones), use of the **Atlas** as an
input, and the **public record of what fails**.

## 5. Credit chain of the 33.25060 merge (and of the earlier sets it builds on), so that no credit is lost

| Part | Author (public notebook) | Link |
|---|---|---|
| DQI `b183c793` of the merge (10.5 Toffolis per shot fewer than `6f78ecdd`, by the title of the notebook; origin and design not traced, the notebook only packs files from datasets I cannot open) | logiclab | [Quantum Circuit Compilation V58 Submission](https://www.kaggle.com/code/logiclab/quantum-circuit-compilation-v58-submission) |
| chemistry of the merge, version 19: 2,261 of 2,400 dead words with new values, loaders 3,310 Toffolis per pass, lambda_eff 46.914304, table `38823b9b` | goodpjw2008 (weights continued from evgendvorkin) | [QCC \| Shorter Chemistry Loaders \| LB 33.25057](https://www.kaggle.com/code/goodpjw2008/qcc-shorter-chemistry-loaders-lb-33-25057) |
| 33.24213 set (version 18): thirteen of the fifteen loaders re-solved or rebuilt (3,315 Toffolis per pass), new values for 1,922 "dead words" (rotations of orbitals with amplitude exactly zero), weights refit continued from evgendvorkin's public refit (lambda_eff 46.914311390), table `71e1c87f`; my notebook C (v49) scored 33.24213 with the same bytes | goodpjw2008 (weights: starting from evgendvorkin) | [QCC \| Shorter Chemistry Loaders \| LB 33.24213](https://www.kaggle.com/code/goodpjw2008/qcc-shorter-chemistry-loaders-lb-33-24213) |
| 33.21180 set: chemistry table `6ac46e3e` (weights refitted on goodpjw2008's table, lambda_eff 46.914325 to 46.914320967) and the first public notebook with the whole set; my notebook C (v46) scored 33.21180 with the same bytes | zhuangbility; Areeb Ali reproduced the files | [QCC \| V17 Loaders and Our Refit \| LB 33.21180](https://www.kaggle.com/code/zhuangbility/qcc-v17-loaders-and-our-refit-lb-33-21180); [QAI \| Cut the Gates, Keep the Chemistry \| 33.21180](https://www.kaggle.com/code/areebbb/qai-cut-the-gates-keep-the-chemistry-33-21180) |
| ten chemistry loaders re-solved, 3,333 Toffolis per pass (version 17), loader `angle_k_14` `962ed332` | goodpjw2008 | [QCC \| Shorter Chemistry Loaders \| LB 33.21179](https://www.kaggle.com/code/goodpjw2008/qcc-shorter-chemistry-loaders-lb-33-21179) |
| invsqrt `6b592145` (37 qubits, 0.03 cheaper than `bb676b95`; what it changes was traced by no one I read) | prvsiyan | [Verifier-Guided Quantum Circuit Optimization](https://www.kaggle.com/code/prvsiyan/verifier-guided-quantum-circuit-optimization) |
| salt study of the circuits | alexchilton | [33.21 LB \| Which Circuits Survive Private Salt?](https://www.kaggle.com/code/alexchilton/33-21-lb-which-circuits-survive-private-salt) |
| 33.21011 set: ten chemistry loaders re-solved (3,334 Toffolis per pass), refitted weights and table `573d10be`; the set that scored 33.21011 for my version 35 | goodpjw2008 | [QCC \| Shorter Chemistry Loaders \| LB 33.21011](https://www.kaggle.com/code/goodpjw2008/qcc-shorter-chemistry-loaders-lb-33-21011) |
| same circuits with the table `14e3e699` (33.21010, 33.210) | Areeb Ali; Mizero Lucky Gall | [QAI \| The 26-Toffoli Cut \| LB 33.21010](https://www.kaggle.com/code/areebbb/qai-the-26-toffoli-cut-lb-33-21010); [Quantum Circuits \| 33.210 Shorter Chem Loaders](https://www.kaggle.com/code/mizeroluckygall/quantum-circuits-33-210-shorter-chem-loaders) |
| the 33.2101 notebook of the same day (its output could not be downloaded on 2026-11-25, so I did not compare it) | ozertuu | [Google Quantum AI VQCC 33.2101 SOTA Apex](https://www.kaggle.com/code/ozertuu/google-quantum-ai-vqcc-33-2101-sota-apex) |
| five chemistry loaders of the 33.21 set; the 3,357-Toffoli loaders (33.17) | maoxin123 | [QCC 33.17 \| 3,357-Toffoli chemistry loaders](https://www.kaggle.com/code/maoxin123/qcc-33-17-3-357-toffoli-chemistry-loaders) |
| shortened loaders (3,372 Toffolis per pass) and the "26-Toffoli cut" | Areeb Ali | as above |
| DQI `6f78ecdd`: zero-test cuts (rewrites by goodpjw2008, evgendvorkin and ozertuu) on tonylica's `4b572141` | goodpjw2008 and others | as above; evgendvorkin: [Deep EDA with Analogies](https://www.kaggle.com/code/evgendvorkin/google-quantum-ai-deep-eda-with-analogies) |
| invsqrt `bb676b95`: three T gates fewer than Rithvik Redrouthu's `d2148a7c` | varianceofx; mizeroluckygall | (notebook links not recorded here; see goodpjw2008's notebook above) |
| table refits: leotang09, goodpjw2008, ozertuu | leotang09; ozertuu | (see the notebooks above) |
| 33.135 chemistry: 15 loaders recompiled to 3,375 Toffolis per pass, refitted weights | maoxin123 | [QCC 33.135 \| 3,375-Toffoli chemistry loaders](https://www.kaggle.com/code/maoxin123/qcc-33-135-3-375-toffoli-chemistry-loaders) (on the word table `fc4b4c01`: Team ThemBones' design, Almond Labs' table, ozertuu's refit) |
| set assembled, dead-word loader chain, verification (33.10186) | goodpjw2008 | [QCC \| Dead-Word Loader Chain DP \| LB 33.10186](https://www.kaggle.com/code/goodpjw2008/qcc-dead-word-loader-chain-dp-lb-33-10186) |
| invsqrt `d2148a7c` (37 qubits) and five chemistry loaders | Rithvik Redrouthu | [Shut up and Calculate \| VQCC 32.86114](https://www.kaggle.com/code/rithvikredrouthu/shut-up-and-calculate-vqcc-32-86114) |
| DQI `4b572141` and the generator dataset | tonylica | [Quantum AI 32.85306 Ready](https://www.kaggle.com/code/tonylica/quantum-ai-32-85306-ready) |
| recompiled loader 6 | boristown | [VQCC 33.102 LB \| DAG Splicing](https://www.kaggle.com/code/boristown/vqcc-33-102-lb-dag-splicing-visual-guide) |
| chemistry table `fc4b4c01` | ozertuu | [VQCC milestone public score 31.69497](https://www.kaggle.com/code/ozertuu/vqcc-milestone-public-score-31-69497) |
| loader family of the combination | rupam2020 | [No Bodies VQCC verified portfolio](https://www.kaggle.com/code/rupam2020/no-bodies-vqcc-verified-portfolio) |
| 31.69 improvements (LEND29, livescan + LDH, loader recompilation, refit and gauge) | Almond Labs | [31.69054 notebook](https://www.kaggle.com/code/almondlabs/almond-labs-qcc-31-69054-demonstrable-advantage) |
| the 31.68 circuits, the base of all of the above | team ThemBones (Danish Ali) | [Gift from ThemBones](https://www.kaggle.com/code/danishlynxthembones/gift-from-thembones-vqcc-31-67924) |

**A caution about the numbers of the 33.17 to 33.21 sets, now measured.** The DQI file `6f78ecdd` has zero-test cuts: it removes checks that the public tests do not exercise. In notebook C (version 46, run on Kaggle on 2026-11-25) I ran the official DQI verifier on the file at six salts: the default salt draws 4 failed shots out of 102,400 (the three files then score 33.04428), `s1`, `s4` and `s5` draw none (33.21180, the same as the board gave these bytes), `s2` draws one and `s3` two; mean over the six draws 33.15980. So the gap of 0.17 between the local score of the receipts (33.0426) and the board (33.21011, 33.21180) is a draw effect of the DQI file, not a different circuit. The private part of the board uses its own salt that nobody knows; its score for these files can land anywhere in that range, and the board number is the clean-draw case. I did not re-derive the circuits. The same six salts on the 33.24213 set (notebook C, version 49) give the same failed-shot counts (4, 0, 1, 2, 0, 0, since the DQI file is the same) and scores from 33.07446 to 33.24213, mean 33.19008; the board gave 33.24213, the clean-draw case. With the merge (notebook C, version 52) the DQI `b183c793` draws 1, 1, 1, 2, 1 and 0 failed shots at the default salt and s1 to s5 (scores 33.15686 to 33.25061, mean 33.20113); the board gave 33.25060, the clean-draw case.

boristown's 33.10189 set (his notebook, read 2026-11-21) uses the same invsqrt and DQI and a chemistry of his own: a multi-block DAG splice of the loaders, a zero-conflict recompile of loader 6 and an FP64 refit of the weights (T = 13,290). I did not submit it.

The Atlas dataset keeps the licence and credit notices of the sets it holds in `frontier/licenses/`. Where I
re-packaged a set (my notebooks C and D), the credits sit in the notebook and in this table; if a name or role is wrong
or missing, say so in the comments of the notebook and I will correct it.

## 6. Private helper notebooks (not public, no votes)

`qcc-gold-dqifail1`, `qcc-gold-dqifail2`, `qcc-dqi-failure-hunt`, `qcc-lp2-ver`, `qcc-lp2-conv`: private notebooks used
for DQI failure hunts and verifier runs on 11-15 Nov. They are not part of the portfolio. Since 17 Nov no submission
is made from a private notebook (a private-kernel test submission wasted a daily slot).
