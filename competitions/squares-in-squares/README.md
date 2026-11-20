# Kaggle Playground: Squares in Squares

Competition: [kaggle.com/competitions/squares-in-squares](https://www.kaggle.com/competitions/squares-in-squares) (pack n unit squares, n = 1 to 1,000, into the smallest enclosing square; the score is the sum over n of side / sqrt(n) - 1, lower is better). On 2026-11-17 the CLI listed 2,184 teams and me at rank 237 (not re-checked on 2026-11-20); that rank is a snapshot of the public board, which can move.

This is a side project, not the main work of this portfolio. **My part is small**: almost every packing in my public files was published by other authors first, and both the notebook and the dataset credit them.

## Notebook

[Squares 22.134 | Play with boxes best public lb](https://www.kaggle.com/code/asteriospanoras/squares-22-134-play-with-boxes-best-public-lb)
(17 votes on 2026-11-20, 12 on 2026-11-17; 29 public versions, v19 to v29 added on 2026-11-20, all in [`notebooks/squares-22-134-play-with-boxes-best-public-lb/`](notebooks/squares-22-134-play-with-boxes-best-public-lb/), outputs stripped).
It validates the packings of my dataset (overlap check, score) and can write the submission file. The packings are the per-puzzle best of the newest public outputs of many authors (Penguin, Nilanjan Saha, Sung Heo (kmmmvs), Areeb Ali, Nevska, samanyu1808, jazivxt, Malyshev Danil and others, credited in the notebook); what I add are a few puzzles shortened by basin hopping and certified with the competition metric (n=585, 632 and 914; 747, 748, 749 and 804 by a hair).

Public scores of my submissions (read with `kaggle competitions submissions squares-in-squares` on 2026-11-17; lower is better): 22.14620 (a validated copy of Malyshev Danil's Living Atlas packings, 2026-11-15), 22.13678 (a public base plus four own improvements, 2026-11-15), 22.13518 (2026-11-16), 22.13437 (2026-11-17 01:28 UTC, submission 58451256) 22.13377 (2026-11-17 10:30 UTC, submission 58465388: a merge that includes the newest public outputs of Penguin and others), then 22.13351 (Alex Chilton's starter-kit packings n=330 and 367, 12:10 UTC), 22.13335 (15:07 UTC, with a certified micro-shrink), 22.13202 (18:01 UTC, with Ross Wade's engine packings and a Hopper search for n=645) and **22.13193** (2026-11-17 18:50 UTC, submission 58479242, a merge that adds Areeb Ali's "The Last 1e-9"; read on 2026-11-20, the last submission in that list and the score the notebook's version 28 and 29 state). Not re-checked on 2026-11-20: the current public-board rank. The large steps of these days come from other authors' outputs that the merge takes over; my own hops are a small part of each step.

## Dataset

[Squares in Squares - Best Packings](https://www.kaggle.com/datasets/asteriospanoras/squares-in-squares-best) (862 downloads and 1 vote on 2026-11-17): the per-puzzle merge described above, rebuilt as new public outputs appear, . No data file is stored in this repository.

## Used by others

Found on 2026-11-17 by reading the latest source and Kaggle metadata of the 177 public notebooks of the competition (all of the list that `kaggle kernels list --competition squares-in-squares` returns, by run date, hotness and votes; sources with `kaggle kernels pull`), by my name, my account name and the slugs of my notebook and dataset, plus `kaggle kernels list --dataset asteriospanoras/squares-in-squares-best`. Outputs were not downloaded. **9 notebooks by 6 other authors**:

| Notebook | Author | Votes | What it uses or says (from the source or the Kaggle metadata) |
|---|---|---:|---|
| [S in S: Certified Portfolio Merge + Proj Quench](https://www.kaggle.com/code/nilanjansaha123/s-in-s-certified-portfolio-merge-proj-quench) | nilanjansaha123 | 32 | **uses**: my dataset and my notebook are both inputs |
| [Squares in Squares: Merge 28, Certify, Shrink](https://www.kaggle.com/code/areebbb/squares-in-squares-merge-28-certify-shrink) | areebbb | 22 | **uses**: my dataset and my notebook are both inputs; its tables name me as a source of the public front and list my dataset |
| [sis-submit v2 (certified + search)](https://www.kaggle.com/code/samanyu1808/sis-submit-v2-certified-search) | samanyu1808 | 19 | **uses**: my dataset is an input; its credits list "asteriospanoras" among the authors whose outputs are attached |
| [Certified Merge Projection Quench GPU Screen](https://www.kaggle.com/code/nilanjansaha123/certified-merge-projection-quench-gpu-screen) | nilanjansaha123 | 16 | **uses**: my notebook is an input |
| [Debut: top 150, 22.13x (v45)](https://www.kaggle.com/code/amirhezekiahespanto/debut-top-150-22-13x-v45) | amirhezekiahespanto | 5 | **uses**: my notebook is an input |
| [Squares GA Contact Certified Current Union](https://www.kaggle.com/code/penguin069/squares-ga-contact-certified-current-union) | penguin069 | 4 | **uses**: "179 strictly better per-puzzle rows from Asterios Panoras's Squares in Squares - Best Packings dataset, explicitly pinned to dataset version 6" |
| [Squares Public Neural Recovery Union](https://www.kaggle.com/code/penguin069/squares-public-neural-recovery-union) | penguin069 | 4 | credits me among "inherited public packing sources" in its notices |
| [Squares Neural Recovery Certified Union](https://www.kaggle.com/code/penguin069/squares-neural-recovery-certified-union) | penguin069 | 1 | the same credit |
| [Squares public merge fork](https://www.kaggle.com/code/parkera/squares-public-merge-fork) | parkera | 2 | describes itself as a "fork of the top public notebook *Squares 22.1367 | New Best + 4 Own Improvements* by Asterios Panoras" (the earlier title of my notebook); Kaggle also lists my dataset as its input |

Seven of these notebooks use a file or an input of mine (nilanjansaha123 x2, areebbb, samanyu1808, amirhezekiahespanto, penguin069 once, parkera), two credit me by name only; "uses" means attached as an input or named as a source in the text, not that a specific file was compared byte by byte. Public forks of my notebook by other users are not listed by Kaggle (`kaggle kernels list --parent ...` shows only forks of mine); parkera's notebook calls itself a fork in its text. Quotes are at most about twelve words.
