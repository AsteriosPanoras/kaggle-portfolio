# S6E11 | Best LB 0.95528 | Step L x 1.5 (first titled "S6E11 | How Much of the Public Top Is Real?"; the folder was renamed to the current address)

Kaggle: [https://www.kaggle.com/code/asteriospanoras/s6e11-best-lb-0-95528-step-l-1-5](https://www.kaggle.com/code/asteriospanoras/s6e11-best-lb-0-95528-step-l-1-5) · medal: **bronze** (as stated before, not re-checked on 2026-11-20) · votes: 47 (2026-11-20; 29 on 2026-11-17) · versions: 41 (v17 to v41 added on 2026-11-20; the old addresses `s6e11-how-much-of-the-public-top-is-real` and `s6e11-lb-0-95422-this-score-is-not-real`, `s6e11-lb-0-95428-this-score-is-not-real` and `s6e11-lb-0-95504-will-the-top-survive-private` redirect to this one; the last one is the address of versions 37 to 39 under their title "S6E11 | LB 0.95504 | Will the Top Survive Private?", HTTP 200 after redirect on 2026-11-20)

## Scores of the submissions made from the versions

The scores in the table below are the public leaderboard scores (ROC-AUC) of files that the analysis notebook rebuilt from other authors' public files, credited in the notebook and checked by SHA-256 (v3: goodpjw2008's ladder file; v5 and v6: the public 'Bold, Then Bolder' and '2nd-Order Curved Ladder Probit' files; v9 and v10: a credited rebuild of the 0.95417 file and BhuvanNR's step-8 file). They measure the public ladder the notebook analyses, not a model of mine.

## Versions 11 to 16 (2026-11-16 to 2026-11-17)

From version 11 the notebook adds files that I chose by steering on a model of the public board (a model of the public score fitted on scored files). Their public scores (0.95422 to 0.95428) are real board numbers but, as the notebook's own text says, most of that gain will likely not survive the private leaderboard. See the competition README for the sources of the credited files and for the notebooks of other authors that use or credit this one.

## Versions 17 to 41 (2026-11-17 to 2026-11-20)

The same notebook was renamed again, and from version 40 it changed purpose. The "LB 0.95504" notebook in the title history is **versions 37 to 39 of this notebook**, not a separate notebook; the Kaggle title now reads "S6E11 | Best LB 0.95528 | Step L x 1.5".

* **Versions 17 to 36**: the long analysis notebook kept growing by one more board-steered file after another, each built from other authors' public files with the notebook's own model of the public board: 0.95442 (version 16's file, submission 58467208), 0.95447 (v19), 0.95452 (v23), 0.95479 (v25, with a TabM step by busyaprime), 0.95484 (v27), 0.95487 (v29, goodpjw2008's step E as it is), 0.95496 (v31) and **0.95504** (v35, goodpjw2008's step H as it is). Public scores read with `kaggle competitions submissions playground-series-s6e11` on 2026-11-20.
* **Versions 37 to 39** ("Will the top of the board survive private?"): the analysis is rebuilt around the 0.95504 file. Its first cell answers "no, not the very top": on the out-of-fold evidence the 0.95504 file is about 37 points (fifth decimal) below the 0.95442 file it grew from, while it is 62 points above it on the public board. It reports ten lead changes between goodpjw2008 and this notebook from 17 to 19 November, and that 9 of the 10 steps at the top gained less than one noise standard deviation. My own steps are included in that check.
* **Versions 40 and 41**: a three-cell notebook, "the best public file in one short cell". It rebuilds goodpjw2008's step L (0.95527) taken one and a half times, in logit-rank space, from his public files (pinned copies in my dataset *S6E11 Public Board Files*, every input checked by SHA-256) and compares the result byte for byte with the scored file. Submission 58608567 (version 40, 2026-11-20 10:31 UTC) scored **0.95528** on the public board. Step L is goodpjw2008's, the "x 1.5" move is Malyshev Danil's idea applied to it, and the zero-fraud zones are daoviet's idea: **none of these files is a model of mine**, they are steps of the public-board ladder.
* **The caveat stays**: these scores come from steering on the public part (20% of the test rows). The analysis of versions 37 to 39 says the very top will probably not hold on the private 80%, and the 0.95528 file is one more step of the same kind; it is a public-board result, not evidence of a better model. Version 40 sets `WRITE_SUBMISSION = True` in its source, so its output holds a `submission.csv`.

## Every public version

All versions are public on Kaggle (open the notebook, then "Version history"). The files here are their sources, outputs stripped.

| Version | File | Cells | Code lines | Leaderboard score of the submission made from it | What changed | Note |
|---:|---|---:|---:|---|---|---|
| 1 | [v01.ipynb](v01.ipynb) | 44 | 645 | — | first version |  |
| 2 | [v02.ipynb](v02.ipynb) | 44 | 645 | — | same sections, code/text revised |  |
| 3 | [v03.ipynb](v03.ipynb) | 44 | 644 | 0.95354 | same sections, code/text revised |  |
| 4 | [v04.ipynb](v04.ipynb) | 73 | 1200 | — | new sections: What each new notebook offers, and what its public tuning is likely to cost on private |  |
| 5 | [v05.ipynb](v05.ipynb) | 73 | 1212 | 0.95388 | same sections, code/text revised |  |
| 6 | [v06.ipynb](v06.ipynb) | 85 | 1498 | 0.95390 | same sections, code/text revised |  |
| 7 | [v07.ipynb](v07.ipynb) | 123 | 1917 | — | new sections: Each scored file is one linear equation about the public labels, Every step of the 0.95417 ladder: public score against OOF, How far can steering by the public board go? A simulation on the OOF rows, What the files are likely to score on private |  |
| 8 | [v08.ipynb](v08.ipynb) | 123 | 1922 | — | same sections, code/text revised |  |
| 9 | [v09.ipynb](v09.ipynb) | 123 | 1928 | 0.95417 | same sections, code/text revised |  |
| 10 | [v10.ipynb](v10.ipynb) | 123 | 1931 | 0.95419 | same sections, code/text revised |  |
| 11 | [v11.ipynb](v11.ipynb) | 127 | 2011 | 0.95422 (submission 58407451) | board-steered file added (public-board model); same sections | file chosen by steering on the public board; the notebook says its score will likely not hold on the private part |
| 12 | [v12.ipynb](v12.ipynb) | 130 | 2046 | — | same sections, code/text revised |  |
| 13 | [v13.ipynb](v13.ipynb) | 130 | 2056 | — | same sections, code/text revised |  |
| 14 | [v14.ipynb](v14.ipynb) | 130 | 2061 | 0.95424 (submission 58429512) | board-steered file `M + 2.0(A-O)` | same caveat |
| 15 | [v15.ipynb](v15.ipynb) | 132 | 2083 | 0.95428 (submission 58442141) | new section "v15: one step on top of the 0.95428 average" | same caveat |
| 16 | [v16.ipynb](v16.ipynb) | 132 | 2083 | 0.95442 (submission 58467208) | same sections, code/text revised | board-steered: goodpjw2008 0.95432 + BhuvanNR B, each + 0.4 RealMLP update |
| 17 | [v17.ipynb](v17.ipynb) | 134 | 2104 | — | first-cell title "LB 0.95442 \| Reverse engineering public" |  |
| 18 | [v18.ipynb](v18.ipynb) | 134 | 2109 | — | first-cell title "Top Public, Fully Explained" |  |
| 19 | [v19.ipynb](v19.ipynb) | 136 | 2123 | 0.95447 (submission 58472244) | first-cell title "Top Public, Fully Explained" | board-steered or other authors' step: 0.95442 file + 1.5 x goodpjw2008 step B |
| 20 | [v20.ipynb](v20.ipynb) | 136 | 2123 | — | first-cell title "Top Public, Fully Explained" |  |
| 21 | [v21.ipynb](v21.ipynb) | 138 | 2137 | — | first-cell title "Top Public, Fully Explained" |  |
| 22 | [v22.ipynb](v22.ipynb) | 138 | 2137 | — | first-cell title "Top Public, Fully Explained" |  |
| 23 | [v23.ipynb](v23.ipynb) | 138 | 2138 | 0.95452 (submission 58485223) | first-cell title "Top Public, Fully Explained" | board-steered or other authors' step: 0.95447 file + 1.5 x goodpjw2008 step C |
| 24 | [v24.ipynb](v24.ipynb) | 138 | 2138 | — | first-cell title "Top Public, Fully Explained" |  |
| 25 | [v25.ipynb](v25.ipynb) | 140 | 2151 | 0.95479 (submission 58489650) | first-cell title "Top Public, Fully Explained" | board-steered or other authors' step: 0.95452 file + busyaprime TabM step |
| 26 | [v26.ipynb](v26.ipynb) | 140 | 2151 | — | first-cell title "Top Public, Fully Explained" |  |
| 27 | [v27.ipynb](v27.ipynb) | 142 | 2166 | 0.95484 (submission 58501225) | first-cell title "Top Public, Fully Explained" | board-steered or other authors' step: 2 x goodpjw2008 step D + 0.3 TabM on the 0.95479 file |
| 28 | [v28.ipynb](v28.ipynb) | 142 | 2166 | — | first-cell title "Top Public, Fully Explained" |  |
| 29 | [v29.ipynb](v29.ipynb) | 144 | 2178 | 0.95487 (submission 58505572) | first-cell title "Top Public, Fully Explained" | board-steered or other authors' step: goodpjw2008 step E as it is |
| 30 | [v30.ipynb](v30.ipynb) | 144 | 2178 | — | first-cell title "Top Public, Fully Explained" |  |
| 31 | [v31.ipynb](v31.ipynb) | 146 | 2190 | 0.95496 (submission 58532258) | first-cell title "Top Public, Fully Explained" | board-steered or other authors' step: six steps along goodpjw2008 step F |
| 32 | [v32.ipynb](v32.ipynb) | 146 | 2190 | — | first-cell title "Top Public, Fully Explained" |  |
| 33 | [v33.ipynb](v33.ipynb) | 152 | 2236 | — | first-cell title "Top Public, Fully Explained" |  |
| 34 | [v34.ipynb](v34.ipynb) | 152 | 2236 | — | first-cell title "Top Public, Fully Explained" |  |
| 35 | [v35.ipynb](v35.ipynb) | 152 | 2236 | 0.95504 (submission 58556638) | first-cell title "Top Public, Fully Explained" | board-steered or other authors' step: goodpjw2008 step H as it is |
| 36 | [v36.ipynb](v36.ipynb) | 152 | 2236 | — | first-cell title "Top Public, Fully Explained" |  |
| 37 | [v37.ipynb](v37.ipynb) | 156 | 2285 | — | analysis rebuilt around the 0.95504 file ("Will the top of the board survive private?") |  |
| 38 | [v38.ipynb](v38.ipynb) | 159 | 2322 | — | analysis rebuilt around the 0.95504 file ("Will the top of the board survive private?") |  |
| 39 | [v39.ipynb](v39.ipynb) | 159 | 2420 | — | analysis rebuilt around the 0.95504 file ("Will the top of the board survive private?") |  |
| 40 | [v40.ipynb](v40.ipynb) | 3 | 46 | **0.95528** (submission 58608567) | three-cell notebook: the best public file in one short cell | goodpjw2008 step L taken 1.5 times (Malyshev Danil moved J and K the same way) |
| 41 | [v41.ipynb](v41.ipynb) | 3 | 46 | — | three-cell notebook: the best public file in one short cell | same as v40 |
