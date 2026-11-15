# Kaggle Playground Series S6E11: Predicting Credit Card Fraud

Competition: [kaggle.com/competitions/playground-series-s6e11](https://www.kaggle.com/competitions/playground-series-s6e11) (metric: ROC-AUC)

## Notebook

[S6E11 | How Much of the Public Top Is Real?](https://www.kaggle.com/code/asteriospanoras/s6e11-how-much-of-the-public-top-is-real)
(source: [`notebooks/s6e11-how-much-of-the-public-top-is-real/`](notebooks/s6e11-how-much-of-the-public-top-is-real/),
all 10 public versions pulled 2026-11-15, outputs stripped; 18 votes on 2026-11-15).

An analysis of the public leaderboard "ladders" (sequences of small blending steps, each kept because it raised the
public score). Using the public nested out-of-fold predictions of a top-band stack as a stand-in for the hidden test
labels, it draws many random public/private splits and measures:

* how large one ladder step is compared with the noise of the public score (about one noise standard deviation);
* which published steps still help when replayed on out-of-fold data (most are flat or negative; a second seed of the
  same model holds up);
* the winner's curse: choosing the best of many probes by public score guarantees a public gain even when nothing is
  better, and the private part does not repeat it.

Every input is a public file, found by name and checked by SHA-256; the notebook runs on CPU in about ten minutes and
trains no large model.

## Credits

The analysis stands on other people's public work, credited with links in the notebook: goodpjw2008 (nested OOF of a
top-band stack, OOF bank, ladder notebooks with every probe), Areeb Ali (*Three Ladders* notebooks), amanatar, Moran Z,
megayak, masayakawamata, daoviet and the other authors listed there. Their files keep their authors' licences.
