# QCC 28.18084? | Could Be Top 1 public | Try It (originally "QCC 28.1277 | Frontier + Finer Chemistry Refit"; folder name keeps the old slug)

> Which notebook is which, with the content of each version range and the part of it that is mine: [NOTEBOOK_MAP.md](../../NOTEBOOK_MAP.md). Votes were refreshed on 2026-11-21 with `kaggle kernels list --mine`; the version count was not re-checked on that day.

Kaggle: [https://www.kaggle.com/code/asteriospanoras/qcc-28-18084-could-be-top-1-public-try-it](https://www.kaggle.com/code/asteriospanoras/qcc-28-18084-could-be-top-1-public-try-it) · medal: silver (as shown on the notebook, 2026-11-18) · votes: 53 (2026-11-21) · versions: 18 (no newer version found on 2026-11-20: version 19 does not exist)

Current title and address (read with `kaggle kernels list --mine` on 2026-11-18): "QCC 28.18084? | Could Be Top 1 public | Try It", `qcc-28-18084-could-be-top-1-public-try-it`. Former titles and addresses: first **QCC 27.307 | Frontier + Finer Chemistry Refit** (`qcc-27-307-frontier-finer-chemistry-refit`), then **QCC 27.3122 | Frontier + Finer Chemistry Refit** (`qcc-27-3122-frontier-finer-chemistry-refit`); on 2026-11-16 the old address answered with a redirect to the current one. The new title is the owner's choice.

## Status on 2026-11-17 to 2026-11-18 (versions 16 to 18)

* **Version 18** (submission 58485562, 2026-11-18 00:00 UTC) scored **28.18084** on the public leaderboard (read with `kaggle competitions submissions`). It ships boristown's DQI `5f901c55` (his six-product patch on Grant Prater's `575b043f`, which I reproduced from his patch script as a 75-operation byte patch, checked byte for byte against his file, and entered), with maoxin123's invsqrt `563d0583` (embedded in the notebook) and Atakan Aldemir's weights `703843d3` on the 4,022-Toffoli loaders. **This is a tie with boristown's public score, not a gain of mine; every file is another author's public work.**
* Version 16 embeds the invsqrt `563d0583`; version 17 tried a DQI `327b0751` with three more retained products from my own scan (-3 Toffolis); version 18 replaced it with boristown's six-product `5f901c55`. I list no board score for versions 16 and 17.
* The embedded invsqrt string and the byte patch are replaced here by `REMOVED_EMBEDDED_BINARY`; the full cells are on Kaggle.
* The notebook shows a silver medal and 52 votes on 2026-11-18 evening (the medal as I read it, not re-derived).

## Status on 2026-11-17 (versions 10 to 15)

* **Version 13** (submission 58452966, 2026-11-17 02:35 UTC) scored **28.14703** on the public leaderboard (read with `kaggle competitions submissions`). It ships Grant Prater's DQI `61c8348d` (his merge of boristown's patches into Balram Srinivasan's `66b4f18b`), with maoxin123's invsqrt `0af21cb8` and Atakan Aldemir's chemistry weights `703843d3` on Lera's loaders. **These are other authors' public files, re-verified in the notebook with the unchanged official verifiers; none of them is mine.**
* Version 10 tried boristown's DQI `f425ea20` instead (submission 58447146, 28.08843): the DQI is sampled and that file drew one failed shot on the board. Version 12 went back to `66b4f18b` with a short note on this.
* **Version 15** takes the 4,022-Toffoli chemistry loaders of maoxin123 with Atakan Aldemir's weights and Grant Prater's DQI `575b043f`, the combination that newer public notebooks (Atakan Aldemir's, maoxin123's, Grant Prater's) report at about 28.151 locally. That work is theirs. I submitted it through the notebook (submission 58466298, 2026-11-17 10:59 UTC); its board score was 28.15096 (read on 2026-11-18).
* The title was renamed afterwards (see the top of this page).

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
| 10 | [v10.ipynb](v10.ipynb) | 11 | 110 | 28.08843 (submission 58447146) | DQI `f425ea20` (boristown) instead of `66b4f18b`; submission-file writing on | board draw of the DQI had one failed shot |
| 11 | [v11.ipynb](v11.ipynb) | 11 | 110 | — | same files; submission-file writing off |  |
| 12 | [v12.ipynb](v12.ipynb) | 11 | 110 | — | back to the DQI `66b4f18b`; a note on the DQI draw |  |
| 13 | [v13.ipynb](v13.ipynb) | 11 | 114 | **28.14703** (submission 58452966) | DQI `61c8348d` (Grant Prater); submitted |  |
| 14 | [v14.ipynb](v14.ipynb) | 11 | 114 | — | same files as v13; submission-file writing off |  |
| 15 | [v15.ipynb](v15.ipynb) | 11 | 95 | — | invsqrt `0af21cb8`, DQI `575b043f` (Grant Prater), 4,022-Toffoli loaders (maoxin123) with Atakan Aldemir's weights; title text "28.151"; submitted via the notebook (submission 58466298, 10:59 UTC) | board score 28.15096 (read on 2026-11-18) |
| 16 | [v16.ipynb](v16.ipynb) | 11 | 97 | — | invsqrt `563d0583` embedded in the notebook (maoxin123); other files as v15 | embedded binary data (invsqrt) removed |
| 17 | [v17.ipynb](v17.ipynb) | 11 | 105 | — | a DQI with three more retained AND products from my own scan on `575b043f` (-3 Toffolis, `327b0751`) | embedded binary data (invsqrt, patch) removed |
| 18 | [v18.ipynb](v18.ipynb) | 11 | 105 | **28.18084** (submission 58485562, 2026-11-18 00:00 UTC) | boristown's six-product DQI `5f901c55` (rebuilt as a byte patch on `575b043f`); submitted | other authors' files; a tie with the board; embedded binary data (invsqrt, patch) removed |

## Used by others (8 public notebooks)

| # | Notebook (link) | Author | Votes | Date | Versions | What of mine it uses / how it credits me |
|---:|---|---|---:|---|---|---|
| 1 | [the-real-150k-was-the-friends-we-made](https://www.kaggle.com/code/manwithacat/the-real-150k-was-the-friends-we-made) | manwithacat | 100 | 2026-11-12 | 130-139 | file reuse; builds on; hash cited: invsqrt 9c708f7b (splice at clean cuts); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin |
| 2 | [vqcc-hedge-wizardry-notebook](https://www.kaggle.com/code/manwithacat/vqcc-hedge-wizardry-notebook) | manwithacat | 71 | 2026-11-14 | 28-29 | file reuse; builds on; text credit; hash cited: chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say we found the q21 e |
| 3 | [qai-fewer-toffolis-same-qubits-lb-28-06015](https://www.kaggle.com/code/areebbb/qai-fewer-toffolis-same-qubits-lb-28-06015) | areebbb | 54 | 2026-11-12 | 1-23 | file reuse; builds on; text credit; hash cited; kernel input: invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes c |
| 4 | [qcc-reproducible-circuit-portfolio](https://www.kaggle.com/code/ahoirg/qcc-reproducible-circuit-portfolio) | ahoirg | 28 | 2026-11-14 | 5-8 | text credit; hash cited: cites our file(s): chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say |
| 5 | [28-09-lb-which-circuits-survive-private-salt](https://www.kaggle.com/code/alexchilton/28-09-lb-which-circuits-survive-private-salt) | alexchilton | 18 | 2026-11-15 | 1-7 | text credit: cites our file(s): DQI 245527f6 (readout-window transplant); DQI 5778cdd5 (two retained products); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a s |
| 6 | [verified-portfolio-bounded-chemistry-search](https://www.kaggle.com/code/junthewise/verified-portfolio-bounded-chemistry-search) | junthewise | 3 | 2026-11-15 | 1 | file reuse; text credit; hash cited; kernel input: chemistry npz 54bc3e71 (W/H2_I refit, v4); cites our file(s): invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say |
| 7 | [vqcc-t7421-submission](https://www.kaggle.com/code/leotang09/vqcc-t7421-submission) | leotang09 | 2 | 2026-11-14 | 27-32 | file reuse; text credit: chemistry npz 2913ca13 (W/H2_I refit); cites our file(s): chemistry npz 2913ca13 (W/H2_I refit) |
| 8 | [qcc-27-31216-reproduction-ahoirg](https://www.kaggle.com/code/rdaccel/qcc-27-31216-reproduction-ahoirg) | rdaccel | 0 | 2026-11-15 | 1 | text credit; hash cited: cites our file(s): chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say |
