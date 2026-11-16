# Asterios Panoras: Kaggle portfolio

**Kaggle profile: [kaggle.com/asteriospanoras](https://www.kaggle.com/asteriospanoras)** · **Kaggle Notebooks Expert** (November 2026) · 5 bronze notebook medals

I work on exact, verifiable optimisation and on honest evaluation. In November 2026 I published, in the Google Quantum
AI *Verifiable Quantum Circuit Compilation* competition, public notebooks that held the best public notebook score
when released (27.31220 on 2026-11-14; 28.06018 on 2026-11-15, tied for the best public score of that day; **28.07502 on the evening of 2026-11-15**, a level other authors reach as well; on 2026-11-16 two further notebooks re-verified other authors' public files and scored 28.09535 and 28.12769, see the note below) and a dataset
of every public circuit of the competition (7,737 downloads on 2026-11-15). Each improvement was proven exactly (on all
inputs where possible) and confirmed with the hosts' official verifiers, and other competitors adopted them within
hours: 62 public notebooks by 46 other authors use or credit my work (55 / 41 at the full all-versions scan of 15 Nov, plus 7 notebooks and 5 authors found by two latest-version scans on 16 Nov), 33 of them
shipping files I published first, byte for byte, or naming them in their receipts. All five of my public notebooks have won bronze medals (four in this competition, one in
Playground S6E11), which made me a Kaggle Notebooks Expert. Every claim below links to a Kaggle page
you can open without an account.

## Highlights

| Item | Competition | What it is | Score / rank | Votes | Link |
|---|---|---|---|---:|---|
| QCC \| LB:28.07502 wait daily reset :) (first published as "LB 25.367 \| Verified Portfolio + DQI Readout Fix", then titled "Atlas Toolkit + In-Notebook Chemistry Refit") | Google Verifiable Quantum Circuit Compilation | public solution notebook: the best public file of each task, re-verified; exact LP re-solve of the invsqrt rotation angles; chemistry weight refit run inside the notebook with the Atlas toolkit; its first versions introduced the DQI readout-window rewrite (-48 Toffolis) and the invsqrt splice at clean cuts | **silver medal** (as shown on my profile, 2026-11-16); public LB **28.09535** (version 18, 2026-11-16, other authors' public files re-verified); **28.07502** (version 15, submission 58404020, 2026-11-15 22:52 UTC; invsqrt `f67851ac` = jeffemerson's `9339eecc` with my LP-re-solved angles); earlier 28.06018 (version 10, tied for the best public score that day) and 25.40482 (version 5) | 43 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-07502-wait-daily-reset) |
| QCC 28.1277 \| Frontier + Finer Chemistry Refit (formerly QCC 27.3122) | Google Verifiable Quantum Circuit Compilation | public solution notebook: the best public circuits, all re-verified (now the 28.1277 files of other authors); versions 1-6 also ran my chemistry weight refit | **bronze medal** (earlier state); public LB **28.12769** (version 8, 2026-11-16, other authors' files); earlier 27.31220 (2026-11-14, best public notebook score that day) | 21 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-28-1277-frontier-finer-chemistry-refit) |
| QCC 28.06018 \| What Works, What Fails and Why (first titled QCC 27.30) | Google Verifiable Quantum Circuit Compilation | analysis notebook: score anatomy, sixteen measured ideas, an exact numpy simulator, a detector library, and a section on the 28.06 portfolio of 15 November (what worked, what failed, and why); being updated on 16 Nov (this repository has versions up to 14) | **bronze medal**; version 13 submitted the same files as the 28.06018 release (submission 58398329) | 16 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-28-06018-what-works-what-fails-and-why) |
| QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | Google Verifiable Quantum Circuit Compilation | the invsqrt dead-write fix (one Toffoli fewer per shot, exact), shipped in 14 public notebooks | **bronze medal**; public LB 27.30241 (2026-11-14) | 15 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-public-frontier-free-cz-fix-in-invsq) |
| QCC Circuit Atlas + Verified Refit Toolkit | Google Verifiable Quantum Circuit Compilation | dataset: every public circuit file, deduplicated by SHA-256 and credited, with tools; v2 adds our verified contributions and a refit toolkit; v3 adds `best/` (the two files of the 28.06 release, with their authors' licences and credits) | 7,737 downloads | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) |
| S6E11 \| How Much of the Public Top Is Real? | Playground Series S6E11 | analysis: public-leaderboard noise, the winner's curse, nested-CV replay of ladder steps | **bronze medal**; public LB 0.9539 (a credited rebuild of a public file; later versions 0.95417 and 0.95419, same kind) | 18 | [notebook](https://www.kaggle.com/code/asteriospanoras/s6e11-how-much-of-the-public-top-is-real) |
| Supervisory layer for HVAC (paper code) | research | code, protocols and per-episode results of the paper "Re-select or Learn?" | 56 downloads | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac) · [GitHub](https://github.com/AsteriosPanoras/supervisory-layer-hvac) |

### What I contributed to the 28.06 portfolio (15 Nov 2026)

Most of the circuits are other people's public work (Syed Asad Ali's v13 invsqrt and DQI, Lera's chemistry loaders, boristown's refitted weights), credited in every notebook. Mine:

* an **exact LP re-solve of the 34 rotation angles** of the invsqrt circuit (29 angle literals change, nothing else; cost 75170.62 -> 75170.13, about +6e-5 of score);
* an **in-notebook chemistry refit toolkit** (numpy refit of the DF-THC weights at fixed words, all error gates kept) imported from my dataset;
* the **QCC Circuit Atlas**, which supplies that toolkit and now the two files of the release with their licences and credits.

### Results of 16 Nov 2026, stated plainly

* The first notebook now shows a silver medal on my profile (43 votes). Its version 18 scored **28.09535** (submission 58432668) and the frontier notebook's version 8 scored **28.12769** (submission 58441659; Pramit Das's public notebook with the same files scored the same, and my notebook cites it).
* **The frontier files are other authors' public work**: the invsqrt `0af21cb8` (maoxin123), the DQI `66b4f18b` (Balram Srinivasan) and the chemistry weights `703843d3` (Atakan Aldemir) in the 28.1277 notebook; boristown's invsqrt and weights, the C8 DQI line and boristown's chain patch in the 28.09535 one. My notebooks take them over, re-verify them with the unchanged official verifiers and credit them. They do not contain my LP-re-solved angles.
* **What is mine** in this competition: the exact LP re-solve of the invsqrt rotation angles (adopted or credited by several other portfolios, see the list below), the analysis and its tools, the QCC Circuit Atlas dataset with the refit toolkit, and the earlier file edits (readout windows, splice, dead-write fix, chemistry refits).

Earlier contributions (11-14 Nov): the DQI readout-window rewrite, the invsqrt splice at clean cuts, the invsqrt dead-write fix and the chemistry weight refits; see [competitions/google-qcc/README.md](competitions/google-qcc/README.md).

Votes as shown by `kaggle kernels list --mine` on the night of 2026-11-16 for the three QCC notebooks updated that week (43, 21 and 16); the other numbers are those of 2026-11-15. The first notebook was renamed twice (`lb-25-367-verified-portfolio-dqi-readout-fix`, then `qcc-atlas-toolkit-in-notebook-chemistry-refit`, now `qcc-lb-28-07502-wait-daily-reset`); the first old address redirects to the current one, the middle one returned 404 on 2026-11-16.

## Used by others

Details, dates and links for every row: [competitions/google-qcc/evidence/USES.md](competitions/google-qcc/evidence/USES.md).

* **62 public notebooks by 46 other authors** use or credit my work (55 / 41 at the all-versions scan of 15 Nov, 7 / 5 more from the scans of 16 Nov, which read latest versions only); 12 of the first 55 show it
  only in older versions (authors change files between versions), so every row lists the versions where it appears.
* **33 public notebooks by 27 authors** ship files I published first (identical SHA-256) or name them in their receipts, e.g.
  the invsqrt splice `9c708f7b` (20 notebooks, including Alex Chilton's top-voted portfolio) and the dead-write fix
  `e46d90c3` (14 notebooks, including Atakan Aldemir's and maoxin123's frontier notebooks; the first within two hours of release).
* **5 further notebooks by 4 authors** ship manwithacat's invsqrt `1ba197b0`, which contains the same q21 edit as my dead-write
  fix plus a second edit (his notes say I found the q21 edit independently of the identity's earlier credit).
* **52 public notebooks by 39 authors** credit me by name in their text, e.g. *"the measured-CZ edit by
  Asterios Panoras"* (maoxin123), *"Syed Asad Ali (Apache-2.0) + Asterios Panoras angle LP"*
  ([hayatohikawa](https://www.kaggle.com/code/hayatohikawa/qcc-c8-milestone-public-repro-lb-28-066)) and a notebook titled
  [vqcc-v52-asterios-invsqrt-20261114](https://www.kaggle.com/code/xianyu3/vqcc-v52-asterios-invsqrt-20261114) (xianyu3).
* My chemistry weight refit `54bc3e71` is in notebooks of manwithacat, areebbb, junthewise, rdaccel and ahoirg, and `2913ca13` in Leo Tang's.
* The 28.06 release files (`09000960`, the invsqrt with my LP-re-solved angles) are quoted in the receipts or logs of
  [ozertuu](https://www.kaggle.com/code/ozertuu/vqcc-super-sota-verified-portfolio-28-091) (28.06018 SOTA, which also credits the LP angles and attaches my dataset),
  hayatohikawa and Atakan Aldemir within hours of the release.
* **26 notebooks by 21 authors** cite the SHA-256 of my files in their receipts or logs; Alex Chilton's portfolio (167 votes)
  attached my notebook's output as an input in versions 140-155.
* Public forks by other users: 0 visible. **8 notebooks by 8 authors** have one of my notebooks or my dataset attached as an input
  (e.g. [mizeroluckygall](https://www.kaggle.com/code/mizeroluckygall/quantum-circuits-one-toffoli-less-in-invsqrt) and
  [ozertuu](https://www.kaggle.com/code/ozertuu/vqcc-super-sota-verified-portfolio-28-091) attach the Atlas dataset).

**New on 2026-11-16** (details and quotes in [USES.md](competitions/google-qcc/evidence/USES.md)): I read the latest versions of the 40 most recently run notebooks of the competition.
* [kirderf/vqcc-portfolio-28-08-reproduced](https://www.kaggle.com/code/kirderf/vqcc-portfolio-28-08-reproduced) is new to the list. Its provenance column credits *"Asterios Panoras LP angle re-solve"* for the invsqrt, and its log prints a modeled geometric mean of 28.07503 for the whole portfolio. To be plain about it: that is equal to or very slightly above my 28.07502 (board, version 15). Both build on the same public pieces; the angle re-solve is my idea, the chemistry refit in that portfolio is ozertuu's, the merge cut is jeffemerson's. The members dataset it uses, `kirderf/vqcc-portfolio-28-08`, returned 404 to anonymous visitors, so I could not check it.
* The latest versions of [Atakan Aldemir](https://www.kaggle.com/code/atakanaldemir/qcc-terminal-readout-and-phase-folds) (*"Asterios Panoras supplied 29 inverse angle refinements"*), [ozertuu](https://www.kaggle.com/code/ozertuu/vqcc-super-sota-verified-portfolio-28-091) (credit in Task III), [boristown](https://www.kaggle.com/code/boristown/qcc-gap-3-residue-repair-and-c43-native-compiler) (*"LP angle refit by Asterios Panoras"*), [evgendvorkin](https://www.kaggle.com/code/evgendvorkin/google-quantum-ai-deep-eda-with-analogies) and [hayatohikawa](https://www.kaggle.com/code/hayatohikawa/qcc-c8-milestone-public-repro-lb-28-066) credit the LP angle re-solve in their own text; mizeroluckygall, alexchilton and jeffemerson (X-ray notebook) still credit my earlier edits. This was not a new all-versions scan.

* **Night scan, 2026-11-16** (latest versions of the 86 most recently run notebooks of others): six more notebooks credit me in text, by [adityaravi2](https://www.kaggle.com/code/adityaravi2/qcc-frontier-rebase-refit-validation-20261116), [balramsrinivasan](https://www.kaggle.com/code/balramsrinivasan/vqcc-28-10-gf24-closings-in-syed-v13-dqi), [drpatrickchan](https://www.kaggle.com/code/drpatrickchan/qcc-chem-refit-sub1-on-the-28-09-frontier), [koushikrudra](https://www.kaggle.com/code/koushikrudra/qcc-v54-best-verified), [maoxin123](https://www.kaggle.com/code/maoxin123/qcc-v27-a-44-qubit-invsqrt-on-the-28-09-frontier) and [masumhuq](https://www.kaggle.com/code/masumhuq/qai-per-task-max-composite-28-09). Most of these are credits in contributor lists ("measured-CZ / dead-write ideas by Asterios Panoras and James Barlow"), not use of one of my files. Four old addresses were confirmed as renamed (redirect). Details: [USES.md](competitions/google-qcc/evidence/USES.md).

### The notebooks that use or credit my work

62 public notebooks by 46 other authors in total (55 / 41 at the scan of 15 Nov); votes refreshed on 2026-11-16 night; the 15 most voted are below, all of them in [competitions/google-qcc/evidence/USES.md](competitions/google-qcc/evidence/USES.md).

| # | Notebook (link) | Author | Votes | Date | Versions | What of mine it uses / how it credits me |
|---:|---|---|---:|---|---|---|
| 1 | [24-94-lb-verified-three-task-portfolio](https://www.kaggle.com/code/alexchilton/24-94-lb-verified-three-task-portfolio) | alexchilton | 167 | 2026-11-12 | 140-155 | file reuse; kernel input; text credit: invsqrt 9c708f7b (splice at clean cuts); notebook input: lb-25-367-verified-portfolio-dqi-readout-fix; notebook input: lb-25-367-verified-portfolio-dqi-readout-fix; cites our file(s): DQI 245527f6 (readout-window transpl |
| 2 | [the-dataset-is-public-now-enjoy](https://www.kaggle.com/code/heliosli/the-dataset-is-public-now-enjoy) | heliosli | 125 | 2026-11-12 | 43-44,53-57 | file reuse; text credit; hash cited: invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; |
| 3 | [the-real-150k-was-the-friends-we-made](https://www.kaggle.com/code/manwithacat/the-real-150k-was-the-friends-we-made) | manwithacat | 99 | 2026-11-12 | 130-139 | file reuse; builds on; hash cited: invsqrt 9c708f7b (splice at clean cuts); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin |
| 4 | [google-quantum-ai-deep-eda-with-analogies](https://www.kaggle.com/code/evgendvorkin/google-quantum-ai-deep-eda-with-analogies) | evgendvorkin | 77 | 2026-11-12 | 32-38 | file reuse; text credit; hash cited: invsqrt 9c708f7b (splice at clean cuts); credit in text; invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say we f |
| 5 | [qcc-gap-3-residue-repair-and-c43-native-compiler](https://www.kaggle.com/code/boristown/qcc-gap-3-residue-repair-and-c43-native-compiler) | boristown | 76 | 2026-11-14 | 1-9 | text credit; hash cited: cites our file(s): invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say we found the q21 edit independently; invsq |
| 6 | [vqcc-hedge-wizardry-notebook](https://www.kaggle.com/code/manwithacat/vqcc-hedge-wizardry-notebook) | manwithacat | 64 | 2026-11-14 | 28-29 | file reuse; builds on; text credit; hash cited: chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say we found the q21 e |
| 7 | [quantum-circuits-retained-product-audit](https://www.kaggle.com/code/kirilltym/quantum-circuits-retained-product-audit) | kirilltym | 56 | 2026-11-12 | 6-12 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 8 | [qai-fewer-toffolis-same-qubits-lb-28-06015](https://www.kaggle.com/code/areebbb/qai-fewer-toffolis-same-qubits-lb-28-06015) | areebbb | 54 | 2026-11-12 | 1-23 | file reuse; builds on; text credit; hash cited; kernel input: invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes c |
| 9 | [qcc-v25-coded-word-chemistry](https://www.kaggle.com/code/maoxin123/qcc-v25-coded-word-chemistry) | maoxin123 | 54 | 2026-11-12 | 2 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 10 | [qcc-v27-a-44-qubit-invsqrt-on-the-28-09-frontier](https://www.kaggle.com/code/maoxin123/qcc-v27-a-44-qubit-invsqrt-on-the-28-09-frontier) | maoxin123 | 52 | 2026-11-16 | latest | text credit: measured-CZ / dead-write idea |
| 11 | [qcc-gap-3-residue-repair-and-c43-native-compiler](https://www.kaggle.com/code/atakanaldemir/qcc-gap-3-residue-repair-and-c43-native-compiler) | atakanaldemir | 52 | 2026-11-14 | 14-15 | file reuse; text credit: invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix) |
| 12 | [quantum-circuits-iso-gap-dqi-h5](https://www.kaggle.com/code/atakanaldemir/quantum-circuits-iso-gap-dqi-h5) | atakanaldemir | 51 | 2026-11-11 | 13-15 | text credit; hash cited: cites our file(s): DQI 245527f6 (readout-window transplant); DQI 245527f6 (readout-window transplant) |
| 13 | [verifier-guided-quantum-circuit-optimization](https://www.kaggle.com/code/prvsiyan/verifier-guided-quantum-circuit-optimization) | prvsiyan | 44 | 2026-11-11 | 40-46 | file reuse; text credit: DQI 245527f6 (readout-window transplant); invsqrt 9c708f7b (splice at clean cuts); cites our file(s): DQI 245527f6 (readout-window transplant); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a |
| 14 | [quantum-ai-fast-runner-starter-notebook](https://www.kaggle.com/code/ozertuu/quantum-ai-fast-runner-starter-notebook) | ozertuu | 42 | 2026-11-12 | 16-59,61,96-116 | file reuse; text credit; hash cited: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say w |
| 15 | [qcc-v27-4028-toffoli-coded-word-chemistry](https://www.kaggle.com/code/maoxin123/qcc-v27-4028-toffoli-coded-word-chemistry) | maoxin123 | 29 | 2026-11-14 | 2-4 | file reuse; text credit: invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix) |

## How to verify

* **Every claim links to a Kaggle page.** Notebook pages show the score of each version, its votes, inputs and outputs.
* **Hashes.** The circuits and weight files are identified by the first 8 hex digits of their SHA-256 (e.g.
  `e46d90c3`). Each of my notebooks prints the SHA-256 of every file it submits, and so do most notebooks in this
  competition. To check a reuse: open the other author's notebook, look at its log or receipt (or download its output
  and run `sha256sum`), and compare with the hash in the table and with the date of my notebook version.
* **Scores** come from the notebooks' own logs (official verifiers, default salt) and from the public leaderboard
  entries of the submissions made from them; both are listed in [competitions/google-qcc/README.md](competitions/google-qcc/README.md).

## Repository layout

```
README.md                         this page
competitions/
  google-qcc/                     Google Verifiable Quantum Circuit Compilation
    README.md                     the competition, my contributions, timeline, scores
    notebooks/                    all public versions of my 4 notebooks, one folder each (the first one under its current address, qcc-lb-28-07502-wait-daily-reset)
    evidence/                     USES.md + uses.csv: who used what, and how we know
  playground-s6e11/               Playground Series S6E11 (README + notebook source)
datasets/README.md                my public datasets (links only, no data)
research/smart-buildings-sb26.md  links to the public paper code
LICENSE                           Apache-2.0 (my code)
```

No circuit, weight or submission files are in this repository; the notebooks run on Kaggle with public inputs.

## Licence and credits

My code and text are under the [Apache License 2.0](LICENSE). The notebooks build on many other people's public work
(circuits, weights, code, datasets); that work keeps its authors' licences and terms, and each notebook credits its
authors with links. Thank you in particular to Syed Asad Ali, Atakan Aldemir, maoxin123, Heliosli, Areeb Ali,
Ertuğrul Özer, Ali Haydar Özdağ, prvsiyan, Lera (marculera), Alex Chilton, WCao24, Thomas Gamet, manwithacat (James
Barlow), Kirill Tymchishin and, for the S6E11 analysis, goodpjw2008, Areeb Ali, amanatar and the other authors credited
there. The competition data and verifiers belong to their hosts and are not included.
