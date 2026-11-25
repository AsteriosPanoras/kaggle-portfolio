# Kaggle Playground Series S6E11: Predicting Credit Card Fraud

Competition: [kaggle.com/competitions/playground-series-s6e11](https://www.kaggle.com/competitions/playground-series-s6e11) (metric: ROC-AUC)

## Notebook

[S6E11 | Best LB 0.95528 | Step L × 1.5](https://www.kaggle.com/code/asteriospanoras/s6e11-best-lb-0-95528-step-l-1-5)
(first published as "S6E11 | How Much of the Public Top Is Real?", address `s6e11-how-much-of-the-public-top-is-real`; it was retitled several times, among them "S6E11 | LB 0.95428 | This Score Is Not Real" and, for versions 37 to 39, "S6E11 | LB 0.95504 | Will the Top Survive Private?" (`s6e11-lb-0-95504-will-the-top-survive-private`). **That is the same notebook, not a second one**; all old addresses redirect to the current one, checked on 2026-11-20).
Source: [`notebooks/s6e11-best-lb-0-95528-step-l-1-5/`](notebooks/s6e11-best-lb-0-95528-step-l-1-5/),
all 41 public versions (versions 1 to 16 pulled on 2026-11-17, 17 to 41 on 2026-11-20), outputs stripped. 47 votes on 2026-11-20 (29 on 2026-11-17, 18 on 2026-11-15); bronze medal (as stated before, not re-checked on 2026-11-20).

**What it is today.** Versions 1 to 39 are the analysis described below (public-board noise, the winner's curse, a nested-CV replay of ladder steps), extended on 2026-11-17 to 2026-11-19 with more board-steered files; versions 37 to 39 apply the method to the whole 0.95442 to 0.95504 race and conclude that the very top will probably not survive the private part. Versions 40 and 41 are a short notebook that rebuilds one public file, goodpjw2008's step L taken 1.5 times, with every input checked by SHA-256: public score **0.95528** (submission 58608567, 2026-11-20). That file is made of other authors' public steps; it is a public-board result, not a model of mine.

An analysis of the public leaderboard "ladders" (sequences of small blending steps, each kept because it raised the
public score). Using the public nested out-of-fold predictions of a top-band stack as a stand-in for the hidden test
labels, it draws many random public/private splits and measures:

* how large one ladder step is compared with the noise of the public score (about one noise standard deviation);
* which published steps still help when replayed on out-of-fold data (most are flat or negative; a second seed of the
  same model holds up);
* the winner's curse: choosing the best of many probes by public score guarantees a public gain even when nothing is
  better, and the private part does not repeat it.

Every input is a public file, found by name and checked by SHA-256; the notebook runs on CPU in about fifteen minutes and
trains no large model.

### Public scores of its submissions, and what they mean

Read with `kaggle competitions submissions playground-series-s6e11` on 2026-11-17 and, for the rows below the line, on 2026-11-20 (public score, ROC-AUC):

| Version | Public score | What the file is |
|---:|---:|---|
| 9, 10 | 0.95417, 0.95419 | credited rebuilds of other authors' public files (SHA-256 checked) |
| 11 | 0.95422 | a board-steered file: chosen with a model of the public board and my own earlier probes |
| 14 | 0.95424 | board-steered (Areeb Ali's *Steer, Then Mix* and goodpjw2008's 0.95421 file, credited in the notebook) |
| 15 | 0.95428 | board-steered, one step on top of an average of two 0.95427 files |
| 16 | 0.95442 | board-steered: goodpjw2008's 0.95432 and BhuvanNR's step B, each plus a 0.4 RealMLP update |
| 19, 23 | 0.95447, 0.95452 | the previous file plus 1.5 x goodpjw2008's steps B and C |
| 25, 27 | 0.95479, 0.95484 | with a TabM step (busyaprime) and goodpjw2008's step D |
| 29, 31, 35 | 0.95487, 0.95496, 0.95504 | goodpjw2008's step E as it is, six steps along his step F, his step H as it is |
| 40 | **0.95528** | goodpjw2008's step L taken 1.5 times (the lean notebook) |

**These public scores are not evidence of a better model.** The notebook's own text (version 16, and the analysis of versions 37 to 39 for the 0.95504 file) says so: it states that the file was built by steering on a model of the public board and that most of that score will likely not survive the private leaderboard (the private part is 80% of the test rows); it also writes a cross-validation-backed alternative file. The title ("This Score Is Not Real") is that point.

## Update of 2026-11-25

Read on 2026-11-25 (VERIFIED with `kaggle kernels list --mine`, `kaggle competitions submissions playground-series-s6e11`, `kaggle datasets list --mine`). My last submission there is of 2026-11-21.

* **Title and votes.** The notebook is now [S6E11 | LB 0.95552 | Will the Top Survive Private?](https://www.kaggle.com/code/asteriospanoras/s6e11-lb-0-95552-will-the-top-survive-private) with 58 votes (47 on 2026-11-20); same notebook, retitled again. Latest source: [`latest-2026-11-25.ipynb`](notebooks/s6e11-lb-0-95552-will-the-top-survive-private/latest-2026-11-25.ipynb), outputs stripped (last run 2026-11-21 20:53 UTC).
* **Scores of 2026-11-21** (the last day I submitted): each is **another author's public file taken rank for rank**, shown with an analysis in the notebook: 0.95534 (v44, residual100), 0.95540 (v46, goodpjw2008), 0.95542 (v48, dennis6886), 0.95547 (v49, Areeb Ali), 0.95551 (v50, Malyshev Danil) and **0.95552** (v51, Areeb Ali, submission 58687267). The notebook's own conclusion stays the same: public gaps of this size are mostly noise, and the very top is unlikely to survive on the 80% private part. None of these scores comes from a model of mine.
* **Dataset** [S6E11 Public Board Files (pinned copies)](https://www.kaggle.com/datasets/asteriospanoras/s6e11-public-board-files): 439 downloads and 2 votes, last updated 2026-11-20.

## Used by others

(The scan below is the one of 2026-11-17 and was not repeated on 2026-11-20; it refers to the notebook under its titles of that day.)

Public notebooks of other authors that credit or use this notebook or my dataset
[S6E11 Public Board Files (pinned copies)](https://www.kaggle.com/datasets/asteriospanoras/s6e11-public-board-files) (250 downloads on 2026-11-20; 48 on 2026-11-17).
Found on 2026-11-17 by reading the latest source (and Kaggle metadata) of 389 public S6E11 notebooks (the 300 most recently run, the 300 hottest and the 300 most voted, deduplicated; sources with `kaggle kernels pull`, found by my name, my account name, the slugs and titles of my notebook and dataset). Outputs were not downloaded. **12 notebooks by 11 other authors** (3 of them use a file of mine, 9 credit me by name); only what is visible in the source text or in the metadata is listed:

| Notebook | Author | Votes | How it uses or credits it (quote from the source) |
|---|---|---:|---|
| [S6E11 Split Then Push LB 0.95431](https://www.kaggle.com/code/areebbb/s6e11-split-then-push-lb-0-95431) | areebbb | 63 | **uses a file**: its input list names my notebook, and the source says "`A` ... is the `submission.csv` of asteriospanoras's S6E11 \| LB 0.95428 \| This Score Is Not Real" |
| [EDA Blend LB 0.95239 Credit Card Fraud](https://www.kaggle.com/code/saamhm/eda-blend-lb-0-95239-credit-card-fraud) | saamhm | 62 | **uses a file**: my notebook is a notebook input and the code reads `.../asteriospanoras/s6e11-how-much-of-the-public-top-is-real/submission.csv`; its credits list me |
| [S6E11 LM Ladder: Ladder Meets Stack LB 0.95432](https://www.kaggle.com/code/goodpjw2008/s6e11-lm-ladder-ladder-meets-stack-lb-0-95432) | goodpjw2008 | 56 | **uses my dataset**: `asteriospanoras/s6e11-public-board-files` is a dataset input; its credits name "the pinned copies in s6e11-public-board-files that make this version exact", my 0.95422 file and the 0.95424 file |
| [Credit Card Fraud LB 0.9542 Shallow Tree Stack](https://www.kaggle.com/code/alexchilton/credit-card-fraud-lb-0-9542-shallow-tree-stack) | alexchilton | 66 | credits me by name and link: "the noise of a public gap on out-of-fold rows" |
| [Fraud Signal Lab: GPT-2 and GLM Fusion](https://www.kaggle.com/code/malyshevdanil/fraud-signal-lab-gpt-2-and-glm-fusion) | malyshevdanil | 38 | lists me among its upstream credits |
| [S6E11 Fable and Two Families Forecast LB 0.95426](https://www.kaggle.com/code/bhuvannr2006/s6e11-fable-two-families-forecast-lb-0-95426) | bhuvannr2006 | 10 | credits "the noise analysis of the public board and the nested 4-of-5-folds gate used in section 6" |
| [S6E11 LM Ladder: Forecast the Board LB 0.95417](https://www.kaggle.com/code/bhuvannr2006/s6e11-lm-ladder-forecast-the-board-lb-0-95417) | bhuvannr2006 | 7 | credits "Asterios Panoras (the noise analysis of the public board)" |
| [S6E11 Fraud: What Worked, What Didn't](https://www.kaggle.com/code/mathsonchain/s6e11-fraud-what-worked-what-didn-t) | mathsonchain | 5 | cites my notebook and its result that the replayed ladder rungs gave +12 points on the public board and -8.2 in nested CV |
| [S6E11 Final-Pick Check: CV vs the Public Top](https://www.kaggle.com/code/kagankoral/s6e11-final-pick-check-cv-vs-the-public-top) | kagankoral | 5 | credits "Asterios Panoras: measuring the noise of a public gap on OOF rows" |
| [S6E11 Top-20 CPU Blend EDA LB 0.95440](https://www.kaggle.com/code/sriram00777/s6e11-top-20-cpu-blend-eda-lb-0-95440) | sriram00777 | 3 | credits me for "alternative references compared in this round" |
| [How GPT-2 Tokenizes Numbers](https://www.kaggle.com/code/azizdzhon/how-great-tokenizes-numbers-bpe-token-target) | azizdzhon | 0 | lists my notebook as a reference: "Reading the public leaderboard as noise and blending in logit-rank space" |
| [S6E11 Fraud Post-Mortem: 12 Days, 5 Machines](https://www.kaggle.com/code/markbarney/s6e11-fraud-post-mortem-12-days-5-machines) | markbarney | 0 | credits me and summarises my notebook: "explains why the top of this board is mostly luck" |

(`kaggle kernels list --dataset asteriospanoras/s6e11-public-board-files` lists exactly one notebook of another author, goodpjw2008's above. Public forks of my notebook: none visible.) Not counted: one notebook (mobeenfatimah's "getting high score on LB") shows the headline "How much of the public top is real?" in its header but names no source, so I make no claim about it. Quotes are at most about twelve words. Only authors' public pages are linked.

## Credits

The analysis stands on other people's public work, credited with links in the notebook: goodpjw2008 (nested OOF of a
top-band stack, OOF bank, ladder notebooks with every probe), Areeb Ali (*Three Ladders* notebooks), amanatar, Moran Z,
megayak, masayakawamata, daoviet and the other authors listed there. Their files keep their authors' licences.
