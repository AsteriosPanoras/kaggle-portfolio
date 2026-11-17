# Asterios Panoras: Kaggle portfolio

**Kaggle profile: [kaggle.com/asteriospanoras](https://www.kaggle.com/asteriospanoras)** · **Kaggle Notebooks Expert** (November 2026) · 5 bronze notebook medals

I work on exact, verifiable optimisation and on honest evaluation. In November 2026 I published, in the Google Quantum
AI *Verifiable Quantum Circuit Compilation* competition, public notebooks that held the best public notebook score
when released (27.31220 on 2026-11-14; 28.06018 on 2026-11-15, tied for the best public score of that day; **28.07502 on the evening of 2026-11-15**, a level other authors reach as well; from 2026-11-16 on my notebooks re-verified other authors' public files and scored 28.09535, 28.12769 and, on 2026-11-17, **28.14703**; those files are other authors' work, see the notes below) and a dataset
of every public circuit of the competition (9,825 downloads on 2026-11-17). Each improvement was proven exactly (on all
inputs where possible) and confirmed with the hosts' official verifiers, and other competitors adopted them within
hours: 68 public notebooks by 49 other authors use or credit my work in this competition (55 / 41 at the full all-versions scan of 15 Nov, plus 13 notebooks and 8 authors found by three latest-version scans on 16 and 17 Nov), 33 of them
shipping files I published first, byte for byte, or naming them in their receipts; 58 notebooks by 42 authors credit me by name in their text. In my other public projects (Playground S6E11, Squares in Squares) 21 further notebooks by 16 other authors use or credit my notebooks or datasets, see below. My first five public notebooks have won bronze medals (four in this competition, one in
Playground S6E11), which made me a Kaggle Notebooks Expert. Every claim below links to a Kaggle page
you can open without an account.

## Highlights

| Item | Competition | What it is | Score / rank | Votes | Link |
|---|---|---|---|---:|---|
| QCC \| LB:28.07502 wait daily reset :) (first published as "LB 25.367 \| Verified Portfolio + DQI Readout Fix", then titled "Atlas Toolkit + In-Notebook Chemistry Refit") | Google Verifiable Quantum Circuit Compilation | public solution notebook: the best public file of each task, re-verified; exact LP re-solve of the invsqrt rotation angles; chemistry weight refit run inside the notebook with the Atlas toolkit; its first versions introduced the DQI readout-window rewrite (-48 Toffolis) and the invsqrt splice at clean cuts | **silver medal** (as shown on my profile, 2026-11-16); public LB **28.09535** (version 18, 2026-11-16, other authors' public files re-verified); **28.07502** (version 15, submission 58404020, 2026-11-15 22:52 UTC; invsqrt `f67851ac` = jeffemerson's `9339eecc` with my LP-re-solved angles); earlier 28.06018 (version 10, tied for the best public score that day) and 25.40482 (version 5) | 44 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-lb-28-07502-wait-daily-reset) |
| QCC 28.1277 \| Frontier + Finer Chemistry Refit (formerly QCC 27.3122) | Google Verifiable Quantum Circuit Compilation | public solution notebook: the best public circuits, all re-verified (now files of other authors: maoxin123's invsqrt, Grant Prater's DQI, Atakan Aldemir's weights); versions 1-6 also ran my chemistry weight refit. The title still says 28.1277 until I rename it on Kaggle | **bronze medal** (earlier state); public LB **28.14703** (version 13, submission 58452966, 2026-11-17, other authors' files); 28.12769 (version 8, 2026-11-16); earlier 27.31220 (2026-11-14, best public notebook score that day) | 37 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-28-1277-frontier-finer-chemistry-refit) |
| QCC 28.12769 \| What Works, What Fails and Why (renamed by me on 16 Nov; first titled QCC 27.30) | Google Verifiable Quantum Circuit Compilation | analysis notebook: score anatomy, sixteen measured ideas, an exact numpy simulator, a detector library, and a section on what worked, what failed, and why; rebuilt around the 28.1277 portfolio (versions 15-20, all in this repository) | **bronze medal**; version 19 submitted the other authors' 28.1277 files (submission 58446073, 28.12769); version 13 the same files as the 28.06018 release (submission 58398329) | 18 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-28-12769-what-works-what-fails-and-why) |
| QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | Google Verifiable Quantum Circuit Compilation | the invsqrt dead-write fix (one Toffoli fewer per shot, exact), shipped in 14 public notebooks | **bronze medal**; public LB 27.30241 (2026-11-14) | 15 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-public-frontier-free-cz-fix-in-invsq) |
| QCC Circuit Atlas + Verified Refit Toolkit | Google Verifiable Quantum Circuit Compilation | dataset: every public circuit file, deduplicated by SHA-256 and credited, with tools; v2 adds our verified contributions and a refit toolkit; v3 adds `best/` (the two files of the 28.06 release, with their authors' licences and credits) | 9,825 downloads | 9 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) |
| S6E11 \| LB 0.95428 \| This Score Is Not Real (first titled "How Much of the Public Top Is Real?") | Playground Series S6E11 | analysis: public-leaderboard noise, the winner's curse, nested-CV replay of ladder steps; from version 11 also board-steered files whose public scores, as the notebook says, will likely not hold on the private part | **bronze medal**; public LB 0.9539 to 0.95419 (credited rebuilds of public files), then 0.95422, 0.95424 and 0.95428 (board-steered files, not evidence of a better model) | 29 | [notebook](https://www.kaggle.com/code/asteriospanoras/s6e11-lb-0-95428-this-score-is-not-real) · [README](competitions/playground-s6e11/README.md) |
| Squares 22.134 \| Play with boxes best public lb | Squares in Squares (Playground) | validates and scores a per-puzzle merge of the newest public packings; my own part is a few basin-hopping improvements (side project) | public LB 22.13377 (2026-11-17, lower is better); no medal claimed | 12 | [notebook](https://www.kaggle.com/code/asteriospanoras/squares-22-134-play-with-boxes-best-public-lb) · [README](competitions/squares-in-squares/README.md) |
| Squares in Squares - Best Packings | Squares in Squares | dataset: the per-puzzle merge behind the notebook, credited to the authors of the packings | 862 downloads | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/squares-in-squares-best) |
| S6E11 Public Board Files (pinned copies) | Playground Series S6E11 | dataset: pinned copies of public files of other authors used by the S6E11 notebook | 48 downloads | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/s6e11-public-board-files) |
| Supervisory layer for HVAC (paper code) | research | code, protocols and per-episode results of the paper "Re-select or Learn?" | 75 downloads | 2 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac) · [GitHub](https://github.com/AsteriosPanoras/supervisory-layer-hvac) |

### What I contributed to the 28.06 portfolio (15 Nov 2026)

Most of the circuits are other people's public work (Syed Asad Ali's v13 invsqrt and DQI, Lera's chemistry loaders, boristown's refitted weights), credited in every notebook. Mine:

* an **exact LP re-solve of the 34 rotation angles** of the invsqrt circuit (29 angle literals change, nothing else; cost 75170.62 -> 75170.13, about +6e-5 of score);
* an **in-notebook chemistry refit toolkit** (numpy refit of the DF-THC weights at fixed words, all error gates kept) imported from my dataset;
* the **QCC Circuit Atlas**, which supplies that toolkit and now the two files of the release with their licences and credits.

### Results of 16 Nov 2026, stated plainly

* The first notebook now shows a silver medal on my profile (43 votes). Its version 18 scored **28.09535** (submission 58432668) and the frontier notebook's version 8 scored **28.12769** (submission 58441659; Pramit Das's public notebook with the same files scored the same, and my notebook cites it).
* **The frontier files are other authors' public work**: the invsqrt `0af21cb8` (maoxin123), the DQI `66b4f18b` (Balram Srinivasan) and the chemistry weights `703843d3` (Atakan Aldemir) in the 28.1277 notebook; boristown's invsqrt and weights, the C8 DQI line and boristown's chain patch in the 28.09535 one. My notebooks take them over, re-verify them with the unchanged official verifiers and credit them. They do not contain my LP-re-solved angles.
* **What is mine** in this competition: the exact LP re-solve of the invsqrt rotation angles (adopted or credited by several other portfolios, see the list below), the analysis and its tools, the QCC Circuit Atlas dataset with the refit toolkit, and the earlier file edits (readout windows, splice, dead-write fix, chemistry refits).

### Results of 17 Nov 2026, stated plainly

* The frontier notebook now ships Grant Prater's DQI `61c8348d` (his merge of boristown's patches into Balram Srinivasan's GF24 closings) together with maoxin123's invsqrt `0af21cb8` and Atakan Aldemir's chemistry weights `703843d3`. I submitted it through the notebook (version 13, submission 58452966, 2026-11-17 02:35 UTC) and the public score is **28.14703**. **None of the three files is mine**; the notebook re-verifies them with the unchanged official verifiers and credits their authors. Its Kaggle title still says 28.1277 until I rename it in the interface.
* I renamed the analysis notebook to "QCC 28.12769 | What Works, What Fails and Why" (the old addresses redirect). Its version 19 submitted the 28.1277 files and scored 28.12769 (submission 58446073).
* Newer public notebooks of other authors (Atakan Aldemir's, maoxin123's and Grant Prater's) reach about 28.151 locally by adding maoxin123's 4,022-Toffoli chemistry loaders. That is their work. A new version of my frontier notebook with those files (version 15) has been submitted through the notebook (submission 58466298); its score was still pending when I updated this repository, so I list none.
* Votes on 2026-11-17 midday: 44 (first notebook), 37 (frontier), 18 (analysis), 15 (Free CZ Fix), 29 (S6E11), 12 (Squares).

Earlier contributions (11-14 Nov): the DQI readout-window rewrite, the invsqrt splice at clean cuts, the invsqrt dead-write fix and the chemistry weight refits; see [competitions/google-qcc/README.md](competitions/google-qcc/README.md).

Votes, downloads and last-run times are those of `kaggle kernels list --mine` and `kaggle datasets list --user asteriospanoras` on 2026-11-17 midday. The first notebook was renamed twice (`lb-25-367-verified-portfolio-dqi-readout-fix`, then `qcc-atlas-toolkit-in-notebook-chemistry-refit`, now `qcc-lb-28-07502-wait-daily-reset`); the first old address redirects to the current one, the middle one returned 404 on 2026-11-16.

## Used by others

**Summary of 2026-11-17.** Google QCC: 68 notebooks by 49 other authors (58 notebooks / 42 authors credit me by name; 33 / 27 ship files I published first). Playground S6E11: 12 notebooks by 11 authors credit or use my notebook or dataset. Squares in Squares: 9 notebooks by 6 authors use or credit my notebook or dataset. Where a notebook only credits me in its text, this page says so; "uses" means a file, a notebook input or a dataset input that I could see in its source or Kaggle metadata.

Details, dates and links for every row: [competitions/google-qcc/evidence/USES.md](competitions/google-qcc/evidence/USES.md).

* **68 public notebooks by 49 other authors** use or credit my work (55 / 41 at the all-versions scan of 15 Nov, 13 / 8 more from the scans of 16 and 17 Nov, which read latest versions only); 12 of the first 55 show it
  only in older versions (authors change files between versions), so every row lists the versions where it appears.
* **33 public notebooks by 27 authors** ship files I published first (identical SHA-256) or name them in their receipts, e.g.
  the invsqrt splice `9c708f7b` (20 notebooks, including Alex Chilton's top-voted portfolio) and the dead-write fix
  `e46d90c3` (14 notebooks, including Atakan Aldemir's and maoxin123's frontier notebooks; the first within two hours of release).
* **5 further notebooks by 4 authors** ship manwithacat's invsqrt `1ba197b0`, which contains the same q21 edit as my dead-write
  fix plus a second edit (his notes say I found the q21 edit independently of the identity's earlier credit).
* **58 public notebooks by 42 authors** credit me by name in their text, e.g. *"the measured-CZ edit by
  Asterios Panoras"* (maoxin123), *"Syed Asad Ali (Apache-2.0) + Asterios Panoras angle LP"*
  ([hayatohikawa](https://www.kaggle.com/code/hayatohikawa/qcc-c8-milestone-public-repro-lb-28-066)) and a notebook titled
  [vqcc-v52-asterios-invsqrt-20261114](https://www.kaggle.com/code/xianyu3/vqcc-v52-asterios-invsqrt-20261114) (xianyu3).
* My chemistry weight refit `54bc3e71` is in notebooks of manwithacat, areebbb, junthewise, rdaccel and ahoirg, and `2913ca13` in Leo Tang's.
* The 28.06 release files (`09000960`, the invsqrt with my LP-re-solved angles) are quoted in the receipts or logs of
  [ozertuu](https://www.kaggle.com/code/ozertuu/vqcc-super-sota-verified-portfolio-28-091) (28.06018 SOTA, which also credits the LP angles and attaches my dataset),
  hayatohikawa and Atakan Aldemir within hours of the release.
* **27 notebooks by 22 authors** cite the SHA-256 of my files in their receipts, logs or source; Alex Chilton's portfolio (167 votes)
  attached my notebook's output as an input in versions 140-155.
* Public forks by other users: 0 visible. **13 notebooks by 11 authors** have one of my notebooks or my dataset attached as an input
  (e.g. [mizeroluckygall](https://www.kaggle.com/code/mizeroluckygall/quantum-circuits-reference-package-to-28-147), [evgendvorkin](https://www.kaggle.com/code/evgendvorkin/google-quantum-ai-deep-eda-with-analogies) and
  [ozertuu](https://www.kaggle.com/code/ozertuu/quantum-ai-fast-runner-starter-notebook) attach the Atlas dataset; an attachment shows the input was added, not that a file was submitted).

**New on 2026-11-16** (details and quotes in [USES.md](competitions/google-qcc/evidence/USES.md)): I read the latest versions of the 40 most recently run notebooks of the competition.
* [kirderf/vqcc-portfolio-28-08-reproduced](https://www.kaggle.com/code/kirderf/vqcc-portfolio-28-08-reproduced) is new to the list. Its provenance column credits *"Asterios Panoras LP angle re-solve"* for the invsqrt, and its log prints a modeled geometric mean of 28.07503 for the whole portfolio. To be plain about it: that is equal to or very slightly above my 28.07502 (board, version 15). Both build on the same public pieces; the angle re-solve is my idea, the chemistry refit in that portfolio is ozertuu's, the merge cut is jeffemerson's. The members dataset it uses, `kirderf/vqcc-portfolio-28-08`, returned 404 to anonymous visitors, so I could not check it.
* The latest versions of [Atakan Aldemir](https://www.kaggle.com/code/atakanaldemir/qcc-terminal-readout-and-phase-folds) (*"Asterios Panoras supplied 29 inverse angle refinements"*), [ozertuu](https://www.kaggle.com/code/ozertuu/vqcc-super-sota-verified-portfolio-28-091) (credit in Task III), [boristown](https://www.kaggle.com/code/boristown/qcc-gap-3-residue-repair-and-c43-native-compiler) (*"LP angle refit by Asterios Panoras"*), [evgendvorkin](https://www.kaggle.com/code/evgendvorkin/google-quantum-ai-deep-eda-with-analogies) and [hayatohikawa](https://www.kaggle.com/code/hayatohikawa/qcc-c8-milestone-public-repro-lb-28-066) credit the LP angle re-solve in their own text; mizeroluckygall, alexchilton and jeffemerson (X-ray notebook) still credit my earlier edits. This was not a new all-versions scan.

* **Scan of 2026-11-17 (midday)** (latest versions of the 47 notebooks created or run since the morning of 16 Nov; sources and Kaggle metadata, no outputs): six more notebooks credit me by name in their text, by [alexchilton](https://www.kaggle.com/code/alexchilton/28-12-lb-which-circuits-survive-private-salt) (names my invsqrt `e46d90c3`, my chemistry refit `54bc3e71` and states that my notebook scored 28.1470), [maoxin123](https://www.kaggle.com/code/maoxin123/qcc-28-14-4-022-toffoli-chemistry-loaders) ("measured-CZ / dead-write ideas by Asterios Panoras and James Barlow"), [mizeroluckygall](https://www.kaggle.com/code/mizeroluckygall/quantum-circuits-reference-package-to-28-147) (credits me for the 28.1470 combination and the Atlas dataset, which it attaches), [tuantran225](https://www.kaggle.com/code/tuantran225/vqcc-portfolio-2814), [vumaniacom](https://www.kaggle.com/code/vumaniacom/qcc-verified-portfolio-and-where-the-gap-to-32-is) and [aiokajima](https://www.kaggle.com/code/aiokajima/quantum-pramit-281277-reproduction-public) (a mention of my re-verification notebook). Three of the six are new authors. **Credits by name only**: none of the six says that it ships one of my files. Four notebooks of other authors now also list the Atlas dataset or my first notebook as an input. The other recent notebooks I read (for example Atakan Aldemir's *Shared Products and Controlled Refits*) do not name me; outputs were not read, so I may have missed uses there. Details: [USES.md](competitions/google-qcc/evidence/USES.md).
* **Night scan, 2026-11-16** (latest versions of the 86 most recently run notebooks of others): six more notebooks credit me in text, by [adityaravi2](https://www.kaggle.com/code/adityaravi2/qcc-frontier-rebase-refit-validation-20261116), [balramsrinivasan](https://www.kaggle.com/code/balramsrinivasan/vqcc-28-10-gf24-closings-in-syed-v13-dqi), [drpatrickchan](https://www.kaggle.com/code/drpatrickchan/qcc-chem-refit-sub1-on-the-28-09-frontier), [koushikrudra](https://www.kaggle.com/code/koushikrudra/qcc-v54-best-verified), [maoxin123](https://www.kaggle.com/code/maoxin123/qcc-v27-a-44-qubit-invsqrt-on-the-28-09-frontier) and [masumhuq](https://www.kaggle.com/code/masumhuq/qai-per-task-max-composite-28-09). Most of these are credits in contributor lists ("measured-CZ / dead-write ideas by Asterios Panoras and James Barlow"), not use of one of my files. Four old addresses were confirmed as renamed (redirect). Details: [USES.md](competitions/google-qcc/evidence/USES.md).

### The notebooks that use or credit my work

68 public notebooks by 49 other authors in total (55 / 41 at the scan of 15 Nov); votes refreshed on 2026-11-17 midday; the 15 most voted are below, all of them in [competitions/google-qcc/evidence/USES.md](competitions/google-qcc/evidence/USES.md).

| # | Notebook (link) | Author | Votes | Date | Versions | What of mine it uses / how it credits me |
|---:|---|---|---:|---|---|---|
| 1 | [24-94-lb-verified-three-task-portfolio](https://www.kaggle.com/code/alexchilton/24-94-lb-verified-three-task-portfolio) | alexchilton | 167 | 2026-11-12 | 140-155 | file reuse; kernel input; text credit: invsqrt 9c708f7b (splice at clean cuts); notebook input: lb-25-367-verified-portfolio-dqi-readout-fix; notebook input: lb-25-367-verified-portfolio-dqi-readout-fix; cites our file(s |
| 2 | [the-dataset-is-public-now-enjoy](https://www.kaggle.com/code/heliosli/the-dataset-is-public-now-enjoy) | heliosli | 125 | 2026-11-12 | 43-44,53-57 | file reuse; text credit; hash cited: invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix); invsqrt 1ba197b0 (manwithacat): our q21 measure-first |
| 3 | [the-real-150k-was-the-friends-we-made](https://www.kaggle.com/code/manwithacat/the-real-150k-was-the-friends-we-made) | manwithacat | 100 | 2026-11-12 | 130-139 | file reuse; builds on; hash cited: invsqrt 9c708f7b (splice at clean cuts); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes c |
| 4 | [google-quantum-ai-deep-eda-with-analogies](https://www.kaggle.com/code/evgendvorkin/google-quantum-ai-deep-eda-with-analogies) | evgendvorkin | 80 | 2026-11-12 | 32-38 | dataset input; file reuse; text credit; hash cited: invsqrt 9c708f7b (splice at clean cuts); credit in text; invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the  |
| 5 | [qcc-gap-3-residue-repair-and-c43-native-compiler](https://www.kaggle.com/code/boristown/qcc-gap-3-residue-repair-and-c43-native-compiler) | boristown | 77 | 2026-11-14 | 1-9 | text credit; hash cited: cites our file(s): invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say we found the q21  |
| 6 | [vqcc-hedge-wizardry-notebook](https://www.kaggle.com/code/manwithacat/vqcc-hedge-wizardry-notebook) | manwithacat | 71 | 2026-11-14 | 28-29 | file reuse; builds on; text credit; hash cited: chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tym |
| 7 | [quantum-circuits-retained-product-audit](https://www.kaggle.com/code/kirilltym/quantum-circuits-retained-product-audit) | kirilltym | 56 | 2026-11-12 | 6-12 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 8 | [qcc-v27-a-44-qubit-invsqrt-on-the-28-09-frontier](https://www.kaggle.com/code/maoxin123/qcc-v27-a-44-qubit-invsqrt-on-the-28-09-frontier) | maoxin123 | 56 | 2026-11-16 | latest | text credit: measured-CZ / dead-write idea |
| 9 | [qcc-v25-coded-word-chemistry](https://www.kaggle.com/code/maoxin123/qcc-v25-coded-word-chemistry) | maoxin123 | 54 | 2026-11-12 | 2 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 10 | [qai-fewer-toffolis-same-qubits-lb-28-06015](https://www.kaggle.com/code/areebbb/qai-fewer-toffolis-same-qubits-lb-28-06015) | areebbb | 54 | 2026-11-12 | 1-23 | file reuse; builds on; text credit; hash cited; kernel input: invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 |
| 11 | [qcc-gap-3-residue-repair-and-c43-native-compiler](https://www.kaggle.com/code/atakanaldemir/qcc-gap-3-residue-repair-and-c43-native-compiler) | atakanaldemir | 52 | 2026-11-14 | 14-15 | file reuse; text credit: invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix) |
| 12 | [quantum-circuits-iso-gap-dqi-h5](https://www.kaggle.com/code/atakanaldemir/quantum-circuits-iso-gap-dqi-h5) | atakanaldemir | 51 | 2026-11-11 | 13-15 | text credit; hash cited: cites our file(s): DQI 245527f6 (readout-window transplant); DQI 245527f6 (readout-window transplant) |
| 13 | [verifier-guided-quantum-circuit-optimization](https://www.kaggle.com/code/prvsiyan/verifier-guided-quantum-circuit-optimization) | prvsiyan | 44 | 2026-11-11 | 40-46 | file reuse; text credit: DQI 245527f6 (readout-window transplant); invsqrt 9c708f7b (splice at clean cuts); cites our file(s): DQI 245527f6 (readout-window transplant); invsqrt 1ba197b0 (manwithacat): our q21 measure-fir |
| 14 | [quantum-ai-fast-runner-starter-notebook](https://www.kaggle.com/code/ozertuu/quantum-ai-fast-runner-starter-notebook) | ozertuu | 44 | 2026-11-12 | 16-59,61,96-116 | dataset input; file reuse; text credit; hash cited: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit t |
| 15 | [qcc-terminal-readout-and-phase-folds](https://www.kaggle.com/code/atakanaldemir/qcc-terminal-readout-and-phase-folds) | atakanaldemir | 38 | 2026-11-14 | 6-14 | file reuse; text credit; hash cited: invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his  |

## In my other public projects

Found on 2026-11-17 by reading the latest source and Kaggle metadata of public notebooks (S6E11: 389 notebooks; Squares in Squares: all 177 in the competition list). Only what is visible in the source text or metadata is listed; the rows with quotes are in the competition READMEs.

| Project | Notebooks / authors | Uses a file or an input of mine | Credits me by name only | Details |
|---|---|---|---|---|
| Playground S6E11, my notebook "S6E11 \| LB 0.95428 \| This Score Is Not Real" and my dataset *S6E11 Public Board Files* | 12 notebooks by 11 authors | 3: [areebbb](https://www.kaggle.com/code/areebbb/s6e11-split-then-push-lb-0-95431) (its `A` file is my notebook's submission file), [saamhm](https://www.kaggle.com/code/saamhm/eda-blend-lb-0-95239-credit-card-fraud) (reads my notebook's output), [goodpjw2008](https://www.kaggle.com/code/goodpjw2008/s6e11-lm-ladder-ladder-meets-stack-lb-0-95432) (attaches my dataset and credits "the pinned copies") | 9, e.g. [alexchilton](https://www.kaggle.com/code/alexchilton/credit-card-fraud-lb-0-9542-shallow-tree-stack), [bhuvannr2006](https://www.kaggle.com/code/bhuvannr2006/s6e11-fable-two-families-forecast-lb-0-95426) (two notebooks), [mathsonchain](https://www.kaggle.com/code/mathsonchain/s6e11-fraud-what-worked-what-didn-t) | [competitions/playground-s6e11/README.md](competitions/playground-s6e11/README.md) |
| Squares in Squares, my notebook "Squares 22.134 \| Play with boxes best public lb" and my dataset *Squares in Squares - Best Packings* | 9 notebooks by 6 authors | 7, e.g. [nilanjansaha123](https://www.kaggle.com/code/nilanjansaha123/s-in-s-certified-portfolio-merge-proj-quench) and [areebbb](https://www.kaggle.com/code/areebbb/squares-in-squares-merge-28-certify-shrink) (both attach my dataset and my notebook), [samanyu1808](https://www.kaggle.com/code/samanyu1808/sis-submit-v2-certified-search), [penguin069](https://www.kaggle.com/code/penguin069/squares-ga-contact-certified-current-union) ("179 strictly better per-puzzle rows from Asterios Panoras's ... dataset") | 2 ([penguin069](https://www.kaggle.com/code/penguin069/squares-public-neural-recovery-union)'s other notebooks, in notices) | [competitions/squares-in-squares/README.md](competitions/squares-in-squares/README.md) |

areebbb is in both rows, so these are 21 notebooks by 16 distinct authors. In the Squares project my own part is small (a few basin-hopping improvements on top of a merge of other authors' public packings, credited), and in S6E11 the notebook's point is that public-board scores are noisy. The HVAC paper code dataset has no public notebook of another author that uses it.

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
  playground-s6e11/               Playground Series S6E11 (README + all 16 versions of the notebook)
  squares-in-squares/             Squares in Squares (README + all 18 versions of the notebook)
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
