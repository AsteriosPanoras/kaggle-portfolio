# QCC 28.1277 | Frontier + Finer Chemistry Refit

Kaggle: [https://www.kaggle.com/code/asteriospanoras/qcc-28-1277-frontier-finer-chemistry-refit](https://www.kaggle.com/code/asteriospanoras/qcc-28-1277-frontier-finer-chemistry-refit) · medal: bronze (earlier state; not re-checked) · votes: 21 (2026-11-16 evening) · versions: 9

Former titles and addresses: first **QCC 27.307 | Frontier + Finer Chemistry Refit** (`qcc-27-307-frontier-finer-chemistry-refit`), then **QCC 27.3122 | Frontier + Finer Chemistry Refit** (`qcc-27-3122-frontier-finer-chemistry-refit`); on 2026-11-16 the old address answered with a redirect to the current one. The new title is the owner's choice.

## Status on 2026-11-16 (versions 7 to 9)

* **Version 8** (submission 58441659, 2026-11-16 19:25 UTC) scored **28.12769** on the public leaderboard (read with `kaggle competitions submissions`), the same value as the public notebook of Pramit Das that the text cites ([QCC public frontier 28.1277 verified portfolio](https://www.kaggle.com/code/pramitdas/qcc-public-frontier-28-1277-verified-portfolio)).
* **All three files are other authors' public work, re-verified in this notebook with the unchanged official verifiers**: the 44-qubit invsqrt `0af21cb8` (maoxin123), the 890-qubit DQI `66b4f18b` (Balram Srinivasan) and the chemistry weights `703843d3` (Atakan Aldemir) on Lera's loaders. They are the same files as in Pramit Das's notebook, so the score is the same by construction. None of these files is mine; what this notebook adds is the re-verification, the credits and the Atlas toolkit (refit code) it can run.
* Version 7 is the first with these files; version 9 is version 8 with the submission-file writing switched off (no `submission.zip` in the public output).
* Before that: the best submission of this notebook was version 5, 27.31220 on 2026-11-14.

## Every public version

All versions are public on Kaggle (open the notebook, then "Version history"). The files here are their sources, outputs stripped.

| Version | File | Cells | Code lines | Leaderboard score of the submission made from it | What changed | Note |
|---:|---|---:|---:|---|---|---|
| 1 | [v01.ipynb](v01.ipynb) | 11 | 63 | — | first version | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle |
| 2 | [v02.ipynb](v02.ipynb) | 11 | 67 | 27.30670 | same sections, code/text revised | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle |
| 3 | [v03.ipynb](v03.ipynb) | 11 | 67 | — | same sections, code/text revised | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle |
| 4 | [v04.ipynb](v04.ipynb) | 11 | 67 | — | same sections, code/text revised | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle |
| 5 | [v05.ipynb](v05.ipynb) | 11 | 92 | 27.31220 | new sections: Our change: refit the chemistry weights here; removed: Our change: refitted chemistry weights at fixed words | embedded code zip kept; local default paths removed |
| 6 | [v06.ipynb](v06.ipynb) | 11 | 92 | — | same sections, code/text revised | embedded code zip kept; local default paths removed |
| 7 | [v07.ipynb](v07.ipynb) | 11 | 110 | — | files of maoxin123 / Balram Srinivasan / Atakan Aldemir (`0af21cb8`, `66b4f18b`, `703843d3`) | |
| 8 | [v08.ipynb](v08.ipynb) | 11 | 110 | 28.12769 | same files, submitted | |
| 9 | [v09.ipynb](v09.ipynb) | 11 | 110 | — | same files; submission-file writing switched off | |

## Used by others (8 public notebooks)

| # | Notebook (link) | Author | Votes | Date | Versions | What of mine it uses / how it credits me |
|---:|---|---|---:|---|---|---|
| 1 | [the-real-150k-was-the-friends-we-made](https://www.kaggle.com/code/manwithacat/the-real-150k-was-the-friends-we-made) | manwithacat | 99 | 2026-11-12 | 130-139 | file reuse; builds on; hash cited: invsqrt 9c708f7b (splice at clean cuts); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin |
| 2 | [vqcc-hedge-wizardry-notebook](https://www.kaggle.com/code/manwithacat/vqcc-hedge-wizardry-notebook) | manwithacat | 64 | 2026-11-14 | 28-29 | file reuse; builds on; text credit; hash cited: chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say we found the q21 e |
| 3 | [qai-fewer-toffolis-same-qubits-lb-28-06015](https://www.kaggle.com/code/areebbb/qai-fewer-toffolis-same-qubits-lb-28-06015) | areebbb | 54 | 2026-11-12 | 1-23 | file reuse; builds on; text credit; hash cited; kernel input: invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes c |
| 4 | [qcc-reproducible-circuit-portfolio](https://www.kaggle.com/code/ahoirg/qcc-reproducible-circuit-portfolio) | ahoirg | 28 | 2026-11-14 | 5-8 | text credit; hash cited: cites our file(s): chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say |
| 5 | [28-09-lb-which-circuits-survive-private-salt](https://www.kaggle.com/code/alexchilton/28-09-lb-which-circuits-survive-private-salt) | alexchilton | 18 | 2026-11-15 | 1-7 | text credit: cites our file(s): DQI 245527f6 (readout-window transplant); DQI 5778cdd5 (two retained products); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a s |
| 6 | [verified-portfolio-bounded-chemistry-search](https://www.kaggle.com/code/junthewise/verified-portfolio-bounded-chemistry-search) | junthewise | 3 | 2026-11-15 | 1 | file reuse; text credit; hash cited; kernel input: chemistry npz 54bc3e71 (W/H2_I refit, v4); cites our file(s): invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say |
| 7 | [vqcc-t7421-submission](https://www.kaggle.com/code/leotang09/vqcc-t7421-submission) | leotang09 | 2 | 2026-11-14 | 27-32 | file reuse; text credit: chemistry npz 2913ca13 (W/H2_I refit); cites our file(s): chemistry npz 2913ca13 (W/H2_I refit) |
| 8 | [qcc-27-31216-reproduction-ahoirg](https://www.kaggle.com/code/rdaccel/qcc-27-31216-reproduction-ahoirg) | rdaccel | 0 | 2026-11-15 | 1 | text credit; hash cited: cites our file(s): chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say |
