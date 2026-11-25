# Kaggle Santa 2026: The Elf Calculator

Competition: [kaggle.com/competitions/santa-2026](https://www.kaggle.com/competitions/santa-2026) (1,000 puzzles; for each, write a program for a small register calculator that produces all target values; the score is the total number of instructions over all puzzles, **lower is better**; there is no hidden test set, so the locally replayed number is the leaderboard number).

This is a recent side project. **Every program in the notebook and in the dataset is other authors' public work**, merged per puzzle, replayed by an exact verifier and credited program by program; my part is the verification, the merge, the guide text, the measured negative results and the tools. Another author's score is not mine.

## Notebook

[Santa 2026 | Best public score + dataset + fails](https://www.kaggle.com/code/asteriospanoras/santa-2026-best-public-score-dataset-fails) (85 votes on 2026-11-20; last run 2026-11-20 10:22 UTC; the notebook is updated in place, about one documented change per version, and had about 217 versions on 2026-11-20).
Source: [`notebooks/santa-2026-best-public-score-dataset-fails/v217.ipynb`](notebooks/santa-2026-best-public-score-dataset-fails/v217.ipynb), the **latest version only** (version 217, pulled 2026-11-20 about 11:10 UTC, outputs stripped; the notebook had moved on to version 218 by the time I finished); the earlier versions are on Kaggle, not in this repository.

What it is: a practical guide to shortening elf programs (what a program is, where the instructions go, why shared intermediate values decide everything, the public techniques: per-puzzle merge, graph rewrites, joint recipes, the multiplier-frontier optimizer, register allocation), a one-click replay that verifies all 1,000 programs and writes the submission, three reusable helper functions (exact replay, per-puzzle merge, per-puzzle comparison) and a section of 17 measured ideas, one of which gave a gain, with the reasons for the rest. Its own text credits 25 to 26 public sources by name (Tony Li, konbu17, Elias T.-H. Shieh, Nilanjan_Saha123, Atakan Aldemir, Ertuğrul Özer, Roman Rozen, Bikram Basnet, Pratham Jain, alex chilton and others, listed in its section 0) and says that the leaderboard leader's method is not public.

## Scores (public leaderboard, lower is better)

Read with `kaggle competitions submissions santa-2026` on 2026-11-20 (the notebook submits itself, one submission per version):

| Notebook version | Public score | Time (UTC) |
|---|---:|---|
| 196 | 135,761 | 2026-11-20 07:34 |
| 198 | 135,596 | 08:21 |
| 208 | 134,638 | 10:05 |
| 210 | 134,634 | 10:22 |
| 216 | 134,568 | 11:03 |
| 218 | **134,556** | 11:10 |

The notebook states that the best single public file at the time of version 210 had 134,636 instructions (Ertuğrul Özer's) and that its merged set was 134,634; for version 217 it states 134,568 against a best single public file of 134,570 (version 218 scored 134,556 a few minutes later; the numbers keep moving). In both cases the merge is two instructions below the best single public file, and almost all of that comes from other authors' programs. I did not re-check the leaderboard rank on 2026-11-20 and make no rank claim. A different number (137.706) that a Kaggle notebook output showed for a related run is not repeated here because I could not verify which file it belongs to.

## Dataset

[Santa 2026 Elf Calculator: Programs + Experiments](https://www.kaggle.com/datasets/asteriospanoras/santa-2026-elf-programs-and-experiments) (9,593 downloads and 6 votes on 2026-11-20): `best_programs.csv` (the best verified program for every puzzle, its length and its source, i.e. the credit), the experiment tables behind the guide (`experiments.csv`, `headroom_independent_build.csv`, `practice_structure_costs.csv`, `public_lineage.csv`, `history.csv`) and `elf_tools/` (an exact verifier, DAG-aware exact searches, cone re-synthesis, joint-cut and suffix passes). The programs are other authors' public work under Apache-2.0, credited line by line in `best_programs.csv`. They are on Kaggle only; this repository holds no program file.

## Update of 2026-11-25

Read on 2026-11-25 with `kaggle kernels list --mine`, `kaggle competitions submissions santa-2026` and `kaggle datasets list --mine` (VERIFIED on that day). **Every program is still other authors' public work**; nothing below is a claim of a new program.

* **Votes.** The guide notebook [Santa 2026 | Best public score + dataset + fails](https://www.kaggle.com/code/asteriospanoras/santa-2026-best-public-score-dataset-fails) has 100 votes (85 on 2026-11-20); its last run is of 2026-11-20 15:28 UTC, so it was not updated after the 11-20 version stored here.
* **Two more public notebooks**, both built on the same dataset and both writing no submission file unless you copy them and set `WRITE_SUBMISSION = True`: [Santa 2026 | 🎄 Best Public Score, a Gift per Run](https://www.kaggle.com/code/asteriospanoras/santa-2026-best-public-score-a-gift-per-run) (47 votes; its text names 130,193 instructions for its version; latest source [`latest-2026-11-25.ipynb`](notebooks/santa-2026-best-public-score-a-gift-per-run/latest-2026-11-25.ipynb)) and [Santa 2026 | 📈 Best Score + Changes + Gaps + Loss](https://www.kaggle.com/code/asteriospanoras/santa-2026-best-score-changes-gaps-loss) (29 votes; the best public programs for all 1,000 puzzles plus a digest of what changed in the last 24 hours and who found it; latest source [`latest-2026-11-25.ipynb`](notebooks/santa-2026-best-score-changes-gaps-loss/latest-2026-11-25.ipynb), outputs stripped).
* **Scores.** The submissions of 2026-11-24 are labelled "best public file, copied (credits in best_programs.csv)" and come about once an hour: 128,319 (v164, 16:32 UTC), 128,311 (v166), 128,308 (v168), 128,297 (v170), 128,295 (v172), 128,294 (v174) and **128,291** (v176, 23:51 UTC, submission 58855070; lower is better). The run time of the 📈 notebook (23:51) matches the last submission, so I take the submissions to come from that notebook; I did not map each submission to a notebook version. The scores are other authors' programs; the best score of my notebook's submissions moved from 134,556 on 2026-11-20 to 128,291 on 2026-11-24. I make no rank claim.
* **Dataset.** [Santa 2026 Elf Calculator: Programs + Experiments](https://www.kaggle.com/datasets/asteriospanoras/santa-2026-elf-programs-and-experiments): 80,043 downloads and 39 votes (9,593 and 6 on 2026-11-20); last updated 2026-11-24.
* Private working notebooks of mine for this competition are not part of this repository.

## Used by others

Not scanned. I made no search for notebooks of other authors that use or credit the notebook or the dataset, so I claim no uses here (the dataset's download count is the only usage figure, and a download shows interest, not use).
