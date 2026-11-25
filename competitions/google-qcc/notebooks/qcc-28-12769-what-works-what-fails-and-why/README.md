# QCC 33.2118 | Who Built the Public Best Set? (was "QCC 33.06908 | Best public score and credits" until 2026-11-25; folder name keeps the old slug `qcc-28-12769-what-works-what-fails-and-why`; formerly "What we tried, what failed and Why")

> **State of 2026-11-25 (renamed; versions 46 to 48 added below).** The state line that follows is that of 2026-11-21. Address today: [qcc-33-25060-who-built-the-public-best-set](https://www.kaggle.com/code/asteriospanoras/qcc-33-25060-who-built-the-public-best-set), 72 votes, 48 versions.
>
> **State of 2026-11-21.** Address today: [qcc-33-06908-best-public-score-and-credits](https://www.kaggle.com/code/asteriospanoras/qcc-33-06908-best-public-score-and-credits) · 70 votes · 45 versions. The content changed over time (analysis, then fast re-packaging versions, then a static credits page): see [NOTEBOOK_MAP.md](../../NOTEBOOK_MAP.md), section 2C, for what each version range was and what part of it is mine.


Kaggle: [https://www.kaggle.com/code/asteriospanoras/qcc-33-06908-best-public-score-and-credits](https://www.kaggle.com/code/asteriospanoras/qcc-33-06908-best-public-score-and-credits) · medal: bronze (earlier state; not re-checked) · votes: 70 (2026-11-21) · versions: 45 (read on 2026-11-21)

## Address history

Addresses in order (the older ones are expected to redirect to the current one; I checked only the 2026-11-15 and 2026-11-16 ones, on 2026-11-17): `qcc-27-30-what-works-what-fails-and-why` -> `qcc-28-06018-...` -> `qcc-28-12769-...` -> `qcc-28-23162-what-we-tried-what-failed-and-why` -> `qcc-28-24396-...` -> `qcc-31-68159-what-we-tried-what-failed-and-why` -> `qcc-31-69052-best-public-score-and-credits` -> **`qcc-33-06908-best-public-score-and-credits`** (the last two renames on 2026-11-20 and 2026-11-21; the owner names it in the Kaggle interface). Older notes follow.

After the notes below, I renamed the notebook several more times in the Kaggle interface on 2026-11-18. The title now reads "QCC 28.23162 | What we tried, what failed and Why" (`qcc-28-23162-what-we-tried-what-failed-and-why`, read with `kaggle kernels list --mine` on 2026-11-18 evening); the older addresses are expected to redirect (I checked the 2026-11-15 and 2026-11-16 ones on 2026-11-17, not the newer ones).

First titled "QCC 27.30 | What Works, What Fails and Why" (`qcc-27-30-what-works-what-fails-and-why`), retitled on 2026-11-15 to "QCC 28.06018 | What Works, What Fails and Why" (`qcc-28-06018-what-works-what-fails-and-why`), and renamed by me on 2026-11-16 to "QCC 28.12769 | What Works, What Fails and Why" (`qcc-28-12769-what-works-what-fails-and-why`). Both older addresses redirect to the current one (HTTP 302, checked 2026-11-17). The folder of this repository was renamed to match.

## Versions 27 to 35 (2026-11-19 to 2026-11-20)

**Everything in these versions is other authors' public work. Another notebook's score is not a gain of mine: each of these submissions scored the same as the public notebook that uses the same file set, and the notebooks only re-package, hash-check and credit the files.** What is mine here: the packaging, the checks, the credits and the analysis text.

* **Version 27** (19 Nov; its text says "Update of 18 November"): rebuild of the 28.23162 set of 18 Nov (maoxin123's invsqrt `d0227f3c`, ozertuu's DQI `15a4b740`, leotang09's weights `4d63be3d`); submission-file writing off.
* **Version 28** (19 Nov, fast): a 14-line version that unpacks the file set of Koushik Rudra's public notebook *qcc-v60-frontier-verified*, checks the SHA-256 of four files (invsqrt `ecf908fe`, DQI `4471b493`, chemistry `6ef06081`, angle file `ed648708`) and writes `submission.zip`; it does not re-run the verifiers. Submission 58557425 scored **28.23498**, the same as Koushik Rudra's public notebook (a tie, not a gain of mine).
* **Version 29** (19 Nov): the full analysis notebook rebuilt around that 28.23498 set, reading it from the new `frontier/` folder of the QCC Circuit Atlas dataset. It errored on Kaggle because the Atlas zip was unpacked into a folder; **version 30** fixes that.
* **Version 31** (19 Nov, fast): the file set of ozertuu's dataset *quantum-sim-linalg-cache* (invsqrt `acc7b9c8`, DQI `f56b04c7`, chemistry `6ef06081`); submission 58574793 scored **28.23837**, a tie with that author's public notebook.
* **Version 32** (19 Nov): the full analysis of the 28.23837 set; the run was cancelled by me, so it has no score (the source is public).
* **Version 33** (19 Nov): the full analysis of the 28.23498 set. Its section 8 scans were run on the older files and the notebook says the newer file sets are not analysed yet.
* **Version 34** (20 Nov, fast): the 28.24094 set: manwithacat's DQI `f6b555a6` (his HW-31 clean inverses), ozertuu's invsqrt `acc7b9c8` and Manvender Singh's chemistry `6ef06081`; submission 58581362 scored **28.24094**, a tie with the public notebooks of ozertuu and manwithacat.
* **Version 35** (20 Nov, fast): Ghazaros Barseghyan's 28.24398 set from his notebook *vqcc-28-24398-leaf-port*: invsqrt `d0a9a694`, goodpjw2008's DQI `db0a845f` and chemistry `6ef06081`; submission 58608424 scored **28.24396** (2026-11-20, read with `kaggle competitions submissions`), a tie with the public notebooks of the same files, not a gain of mine.
* Versions 28, 31, 34 and 35 are tiny (about 2.4 KB each): they only copy a public file set and write `submission.zip`, so a score of one of them says nothing about analysis. Versions 27 to 33 embed the `qccscope` code zip as before; the 35 KB invsqrt string is removed in the sources here.
* The QCC Circuit Atlas dataset (version 6, 2026-11-19) holds a `frontier/` folder with the 28.23498 and 28.23837 file sets (as folders of the 18 files each), a `receipt.json` with SHA-256 values and the licence and credit notices of the authors; see [datasets/README.md](../../../../datasets/README.md). The files are their authors' work.

## Versions 21 to 26 (2026-11-18)

* **All files of these scores are other authors' public work**: maoxin123 (invsqrt), boristown, Grant Prater, Balram Srinivasan, ozertuu, Atakan Aldemir, manwithacat and vumaniacom (DQI lineage), leotang09 (chemistry weights), Lera/marculera (loaders), Syed Asad Ali and junmiaotiao. My part is the rebuild inside the notebook, the re-verification with the unchanged official verifiers, the credits and the negative scans.
* **Version 21** rebuilds the 28.18965 frontier set (maoxin123's invsqrt `864f81cd`, boristown's DQI `5f901c55`, leotang09's chemistry weights `4d63be3d`, Lera's loaders) and adds section 8, "17 and 18 November: what is left on the new frontier": three negative scans with counts (the invsqrt angles at the LP optimum, the chemistry loaders are rigid, and for the DQI all 279,577 consecutive Toffoli pairs on the same wires were scanned, 24 hold one product by a value check, and the six products of `5f901c55` are all of them). Submission 58505528, board **28.18965** (a tie with the public frontier, not a gain of mine).
* **Version 22** swaps in maoxin123's newer invsqrt `d0227f3c` (74,405.73), embedded in the notebook and SHA-checked (the embedded blob is replaced here by `REMOVED_EMBEDDED_BINARY`). Submission 58511777, board **28.20041** (local 28.20043).
* **Version 23** is version 22 with submission-file writing off.
* **Version 24** uses ozertuu's merged DQI `15a4b740` (public dataset `ozertuu/quantum-sim-linalg-cache`, 365,894.20 Toffolis; two other public notebooks show 28.23162 on the board with it). Local geometric mean 28.23163. Submitted last (submission 58524618, 2026-11-18 20:31 UTC): **board 28.23162**, the same as the two public notebooks that use this DQI (a tie, not a gain of mine).
* **Version 25** uses ozertuu's newer DQI `e208d350` (365,890.03 Toffolis, adds Atakan Aldemir's eight affine phase sites). Local geometric mean 28.23174, clean locally (0 errors in 102,400 shots), but the board scored the submission (58524065, 20:08 UTC) only **28.18862**: the DQI lost shots on the board's draw (one failed shot raises the DQI cost by about 0.46%). The lesson, kept in the notebook: a DQI file that is clean locally can still lose shots on the board, so reuse only DQI files that already have a board score.
* **Version 26** is version 25 with submission-file writing off (no submission file in the public output, as the publication rules require).
* Versions 21 to 26 embed the `qccscope` code zip as before; in versions 22 to 26 the 35 KB invsqrt string `INV_B64` is removed.
* The sections of the notebook that were not rewritten (the scans of section 8) were run on `864f81cd` and `5f901c55`, not on the newer files; the notebook says so.

## Versions 15 to 20 (2026-11-16)

* The notebook was rebuilt around the 28.1277 portfolio of 16 November: new figures (the invsqrt and DQI landscapes, the family tree of the submission), a refreshed embedded `qccscope` archive and the updated section on what worked and what failed.
* **Version 19** built and re-verified the 28.1277 files in the notebook and submitted them (submission 58446073, 2026-11-16 22:03 UTC): public score **28.12769**. These files are other authors' public work (maoxin123's invsqrt `0af21cb8`, Balram Srinivasan's DQI `66b4f18b`, Atakan Aldemir's chemistry weights `703843d3`), the same ones as in the frontier notebook; they are not mine.
* Versions 15 to 18 and 20 have submission-file writing switched off.
* Earlier: **Version 13** submitted the same files as the 28.06018 release of the first notebook (submission 58398329, 2026-11-15 19:23 UTC): public score 28.06018. **Version 14** is a no-file version.
* The section "This round: what worked, what failed, and why" separates what is other people's (Syed Asad Ali's v13 invsqrt and DQI, Lera's loaders with boristown's weights) from what is mine (the exact LP re-solve of the 34 rotation angles, +6e-5 points, and the Atlas refit toolkit run in the notebook).

## Every public version

All versions are public on Kaggle (open the notebook, then "Version history"). The files here are their sources, outputs stripped.

| Version | File | Cells | Code lines | Leaderboard score of the submission made from it | What changed | Note |
|---:|---|---:|---:|---|---|---|
| 1 | [v01.ipynb](v01.ipynb) | 28 | 429 | — | first version |  |
| 2 | [v02.ipynb](v02.ipynb) | 28 | 429 | 25.36727 | same sections, code/text revised |  |
| 3 | [v03.ipynb](v03.ipynb) | 42 | 593 | — | new sections: LB 25.36727 \| QCC analysis toolkit: exact simulator, cost anatomy, what works and what fai, Exchange rates: what one qubit, one Toffoli or one rotation is worth, The public frontier over time, The invsqrt landscape: 73 public circuits in qubits x Toffoli-equivalents ...; removed: LB 25.367 \| QCC toolkit: exact simulator, cost anatomy, what works and what fails |  |
| 4 | [v04.ipynb](v04.ipynb) | 42 | 593 | 25.36727 | new sections: LB 25.367 \| QCC toolkit: exact simulator, cost anatomy, what works and what fails; removed: LB 25.36727 \| QCC analysis toolkit: exact simulator, cost anatomy, what works and what fai |  |
| 5 | [v05.ipynb](v05.ipynb) | 42 | 593 | 25.36727 | same sections, code/text revised |  |
| 6 | [v06.ipynb](v06.ipynb) | 66 | 1004 | 25.44953 | new sections: Setup, Toolbox: `kmsim` (explained in [section 3](#s3)), The score, The kickmix instruction set, on one card ...; removed: LB 25.367 \| QCC toolkit: exact simulator, cost anatomy, what works and what fails, 1. The score in one table, The public frontier over time ... |  |
| 7 | [v07.ipynb](v07.ipynb) | 66 | 1030 | 27.30241 | new sections: Setup: rebuild the submission and verify it (about 15 minutes), invsqrt (46 qubits; one qubit = 2.2% of the cost), DQI (889 qubits; one qubit = 0.22% of the cost, about 860 Toffolis), Chemistry (the loaders are 55% of the Toffolis; the factorization sets the rest) ...; removed: Setup, Toolbox: `kmsim` (explained in [section 3](#s3)), The two phase streams ... | embedded code zip kept; local default paths removed |
| 8 | [v08.ipynb](v08.ipynb) | 66 | 1030 | — | same sections, code/text revised | embedded code zip kept; local default paths removed |
| 9 | [v09.ipynb](v09.ipynb) | 66 | 1030 | — | same sections, code/text revised | embedded code zip kept; local default paths removed |
| 10 | [v10.ipynb](v10.ipynb) | 66 | 1030 | — | new sections: A demo of <code style="background: #eef1f6; color: #111111; padding: 1px 5px; border-radiu, 5.0 <code style="background: #eef1f6; color: #111111; padding: 1px 5px; border-radius: 4px; removed: A demo of `qccscope`, our analysis library, 5.0 `kmsim`: an exact numpy simulator for these circuits | embedded code zip kept; local default paths removed |
| 11 | [v11.ipynb](v11.ipynb) | 66 | 1037 | 27.30670 | same sections, code/text revised | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle; embedded code zip kept; local default paths removed |
| 12 | [v12.ipynb](v12.ipynb) | 66 | 1037 | — | same sections, code/text revised | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle; embedded code zip kept; local default paths removed |
| 13 | [v13.ipynb](v13.ipynb) | 72 | 1200 | 28.06018 | new sections: Setup: rebuild the submission and verify it (about 50 minutes), invsqrt (the 46-qubit line; one qubit = 2.2% of the cost), DQI (the 889-qubit line; one qubit = 0.22% of the cost, about 860 Toffolis), What worked on 14 November: the dead write, drawn and checked ...; removed: Setup: rebuild the submission and verify it (about 15 minutes), invsqrt (46 qubits; one qubit = 2.2% of the cost), DQI (889 qubits; one qubit = 0.22% of the cost, about 860 Toffolis) ... | embedded code zip kept; local default paths removed |
| 14 | [v14.ipynb](v14.ipynb) | 72 | 1200 | — | same sections, code/text revised | embedded code zip kept; local default paths removed |
| 15 | [v15.ipynb](v15.ipynb) | 75 | 1259 | — | rewritten around the 28.1277 portfolio: new figures (landscapes, family tree), embedded toolkit refreshed | embedded code zip kept; local default paths removed |
| 16 | [v16.ipynb](v16.ipynb) | 75 | 1259 | — | same sections, code/text revised |  |
| 17 | [v17.ipynb](v17.ipynb) | 75 | 1259 | — | same sections, code/text revised |  |
| 18 | [v18.ipynb](v18.ipynb) | 75 | 1259 | — | same sections, code/text revised |  |
| 19 | [v19.ipynb](v19.ipynb) | 75 | 1259 | 28.12769 (submission 58446073) | same; submission-file writing on, the 28.1277 files built and re-verified in the notebook |  |
| 20 | [v20.ipynb](v20.ipynb) | 75 | 1259 | — | same; submission-file writing off |  |
| 21 | [v21.ipynb](v21.ipynb) | 76 | 1257 | 28.18965 (submission 58505528) | rebuilt the 28.18965 frontier set (invsqrt `864f81cd`, DQI `5f901c55`, weights `4d63be3d`); new section 8 with three negative scans; submitted | other authors' files; a tie with the board |
| 22 | [v22.ipynb](v22.ipynb) | 76 | 1258 | 28.20041 (submission 58511777; local 28.20043) | invsqrt `d0227f3c` (maoxin123, embedded) instead of `864f81cd`; submitted | embedded binary data (invsqrt) removed; embedded code zip kept |
| 23 | [v23.ipynb](v23.ipynb) | 76 | 1258 | — | same files as v22; submission-file writing off | embedded binary data (invsqrt) removed |
| 24 | [v24.ipynb](v24.ipynb) | 76 | 1260 | **28.23162** (submission 58524618; local 28.23163) | ozertuu's DQI `15a4b740` instead of `5f901c55`; submitted | embedded binary data (invsqrt) removed |
| 25 | [v25.ipynb](v25.ipynb) | 76 | 1260 | 28.18862 (submission 58524065; local 28.23174) | ozertuu's newer DQI `e208d350`; submitted | the DQI lost shots on the board draw; embedded binary data (invsqrt) removed |
| 26 | [v26.ipynb](v26.ipynb) | 76 | 1260 | — | same as v25; submission-file writing off | embedded binary data (invsqrt) removed |
| 27 | [v27.ipynb](v27.ipynb) | 77 | 1260 | — | rebuild of the 28.23162 set of 18 Nov; submission-file writing off | embedded binary data (invsqrt) removed |
| 28 | [v28.ipynb](v28.ipynb) | 2 | 14 | 28.23498 (submission 58557425) | fast version: unpacks and SHA-checks Koushik Rudra's file set | other authors' files; a tie with his public notebook |
| 29 | [v29.ipynb](v29.ipynb) | 80 | 1263 | — (errored) | full analysis around the 28.23498 set, files from the Atlas `frontier/` folder | errored on Kaggle (zip unpacked into a folder); fixed in v30 |
| 30 | [v30.ipynb](v30.ipynb) | 80 | 1267 | — | v29 with the fix | embedded binary data (invsqrt) removed |
| 31 | [v31.ipynb](v31.ipynb) | 2 | 17 | 28.23837 (submission 58574793) | fast version: ozertuu's 28.23837 file set | other authors' files; a tie with that author's public notebook |
| 32 | [v32.ipynb](v32.ipynb) | 80 | 1267 | — (cancelled) | full analysis around the 28.23837 set | cancelled by me |
| 33 | [v33.ipynb](v33.ipynb) | 80 | 1266 | — | full analysis of the 28.23498 set | newer file sets not analysed yet |
| 34 | [v34.ipynb](v34.ipynb) | 2 | 18 | 28.24094 (submission 58581362) | fast version: the 28.24094 set (manwithacat DQI `f6b555a6`, ozertuu invsqrt `acc7b9c8`, chemistry `6ef06081`) | other authors' files; a tie with the public notebooks of ozertuu and manwithacat |
| 35 | [v35.ipynb](v35.ipynb) | 2 | 14 | 28.24396 (tie, other authors' files) | fast version: Ghazaros Barseghyan's 28.24398 set (invsqrt `d0a9a694`, DQI `db0a845f`, chemistry `6ef06081`); submission 58608424 | other authors' files |
| 36 | — | — | — | 31.68159 (submission 58626935, 2026-11-20 17:56 UTC) | fast version: the public file set of almondlabs' notebook *VQCC 31.68159 Improved Chemistry Gauge and Loader* (team ThemBones' circuits with almondlabs' chemistry) | other authors' files; a tie with the public file set; **prvsiyan's notebook credits "V36" to me for loader work that is almondlabs' (see CONTRIBUTIONS.md, section 5)**; source not stored here, open Kaggle version history |
| 37 | — | — | — | — | intermediate version between the 31.68159 and 31.69054 packaging | not individually recorded here |
| 38 | — | — | — | 31.69052 (submission 58634575, 2026-11-20 20:21 UTC) | fast version: the Almond Labs 31.69054 set (invsqrt `be4ce1be`, DQI `8e0837e5`, chemistry `3f95076d`) | other authors' files; a tie; source not stored here |
| 39 | — | 22 | — | — | static page: who is responsible for each part of the best score, the ideas in plain words | the page and its checks are mine; the descriptions are the authors' |
| 40 | — | 22 | — | — | identical to 39 (a build error left the old text) | fixed in 41 |
| 41 | — | 22 | — | — | the same page with 24 credit rows, every one linked | |
| 42 | — | — | — | — | adds the 32.85306 notebook of tonylica as source (no submission made from it) | other authors' files |
| 43 | — | — | — | — | the 32.86114 set of Rithvik Redrouthu as source (no submission made from it) | other authors' files |
| 44 | — | — | — | **33.06908** (submission 58643150, 2026-11-21 00:53 UTC) | per task: invsqrt `d2148a7c` and chemistry from Rithvik Redrouthu, DQI `4b572141` from tonylica; submitted | other authors' files; the combination is mine; a tie with three teams on the board |
| 45 | [v45.ipynb](v45.ipynb) | 22 | 29 | — | final text: 33.06908 page, `WRITE_SUBMISSION = False`, no submission file in the output | other authors' files |
| 46 | — | — | — | **33.21180** (submission 58882874, 2026-11-25 11:02 UTC) | the 33.21180 set of zhuangbility (invsqrt `6b592145`, DQI `6f78ecdd`, loaders of goodpjw2008, table `6ac46e3e`); the page runs the official verifiers and a DQI salt sweep; submitted | other authors' files; a tie with the public notebooks |
| 47 | — | — | — | — | final text, same code, `WRITE_SUBMISSION = False` | — |
| 48 | [v48.ipynb](v48.ipynb) | — | — | — | final text with the board score, new opening (picture, cards, staircase chart), table of what 0.01 points are worth, salt reading; no submission file in the output | the page and the verifier runs; files are other authors' |
| 49 | — | — | — | **33.24213** (submission 58891190, 2026-11-25 13:58 UTC) | the 33.24213 set of goodpjw2008 (version 18): 3,315-Toffoli loaders, dead-word values, table `71e1c87f`; invsqrt and DQI as before; submitted | other authors' files; a tie with his public notebook |
| 50 | [v50.ipynb](v50.ipynb) | — | — | — | final text with the board score and the salt reading for the 33.24213 set; no submission file in the output | the page and the verifier runs; files are other authors' |
| 51 | — | — | — | — | the merge page: chemistry of goodpjw2008 v19 + DQI `b183c793` of logiclab + invsqrt `6b592145`; failed in one minute (builder variable inside notebook code) | — |
| 52 | — | — | — | **33.25060** (submission 58900425, 2026-11-25 17:05 UTC) | same page, fixed; wrote `submission.zip`; submitted | other authors' files; the merge is mine |
| 53 | [v53.ipynb](v53.ipynb) | — | — | — | final text with the board score and the salt reading of the merge; no submission file in the output | the page and the verifier runs |

## Used by others (0 public notebooks)

Credits and reuse are listed for the whole competition in [evidence/USES.md](../../evidence/USES.md).
