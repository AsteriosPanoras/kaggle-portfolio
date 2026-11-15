# Asterios Panoras: Kaggle portfolio

**Kaggle profile: [kaggle.com/asteriospanoras](https://www.kaggle.com/asteriospanoras)** · **Kaggle Notebooks Expert** (November 2026) · 5 bronze notebook medals

I work on exact, verifiable optimisation and on honest evaluation. In November 2026 I published, in the Google Quantum
AI *Verifiable Quantum Circuit Compilation* competition, public notebooks that held the best public notebook score
when released (latest: 27.31220 on 2026-11-14) and a dataset of every public circuit of the
competition (1,490 downloads). Each improvement was proven exactly (on all inputs where possible) and confirmed with
the hosts' official verifiers, and other competitors adopted them within hours: 41 public notebooks by 34 other authors use or credit my work
(counting every public version), 30 of them shipping files I published first, byte for byte. All five of my public notebooks have won bronze medals (four in this competition, one in Playground S6E11), which made me a Kaggle Notebooks Expert. Every claim below links to a Kaggle page
you can open without an account.

## Highlights

| Item | Competition | What it is | Score / rank | Votes | Link |
|---|---|---|---|---:|---|
| QCC 27.3122 \| Frontier + Finer Chemistry Refit | Google Verifiable Quantum Circuit Compilation | public solution notebook: chemistry weight refit run inside the notebook + the best public circuits, all re-verified | **bronze medal**; public LB **27.31220** (2026-11-14); best public notebook score that day | 15 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-3122-frontier-finer-chemistry-refit) |
| QCC 27.30 \| What Works, What Fails and Why | Google Verifiable Quantum Circuit Compilation | analysis notebook: score anatomy, sixteen measured ideas, an exact numpy simulator and a detector library | **bronze medal** | 12 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-what-works-what-fails-and-why) |
| QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | Google Verifiable Quantum Circuit Compilation | the invsqrt dead-write fix (one Toffoli fewer per shot, exact), adopted by 9 public notebooks | **bronze medal**; public LB 27.30241 (2026-11-14) | 14 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-public-frontier-free-cz-fix-in-invsq) |
| LB 25.367 \| Verified Portfolio + DQI Readout Fix | Google Verifiable Quantum Circuit Compilation | DQI readout-window rewrite (-48 Toffolis) and the invsqrt splice at clean cuts (-3 Toffolis), adopted by 17 public notebooks | **bronze medal**; public LB 25.40482 (best version) | 21 | [notebook](https://www.kaggle.com/code/asteriospanoras/lb-25-367-verified-portfolio-dqi-readout-fix) |
| QCC Circuit Atlas | Google Verifiable Quantum Circuit Compilation | dataset: every public circuit file, deduplicated by SHA-256 and credited, with tools | 1,490 downloads; v2 adds our verified contributions and a refit toolkit | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) |
| S6E11 \| How Much of the Public Top Is Real? | Playground Series S6E11 | analysis: public-leaderboard noise, the winner's curse, nested-CV replay of ladder steps | **bronze medal**; public LB 0.9539 | 13 | [notebook](https://www.kaggle.com/code/asteriospanoras/s6e11-how-much-of-the-public-top-is-real) |
| Supervisory layer for HVAC (paper code) | research | code, protocols and per-episode results of the paper "Re-select or Learn?" | 41 downloads | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac) · [GitHub](https://github.com/AsteriosPanoras/supervisory-layer-hvac) |

Votes as shown on Kaggle on 2026-11-15.

## Used by others

Details, dates and links for every row: [competitions/google-qcc/evidence/USES.md](competitions/google-qcc/evidence/USES.md).

* **41 public notebooks by 34 other authors** use or credit my work in at least one public version; 10 of them show it
  only in older versions (authors change files between versions), so every row lists the versions where it appears.
* **30 public notebooks by 26 authors** ship files I published first (identical SHA-256), e.g.
  the invsqrt splice `9c708f7b` (17 notebooks, including Alex Chilton's top-voted portfolio) and the dead-write fix
  `e46d90c3` (9 notebooks, including Atakan Aldemir's and maoxin123's frontier notebooks; the first within two hours of release).
* **3 further notebooks** ship manwithacat's invsqrt `1ba197b0`, which contains the same q21 edit as my dead-write
  fix plus a second edit (his notes say I found the q21 edit independently of the identity's earlier credit).
* **33 public notebooks by 28 authors** credit me by name in their text, e.g. *"the measured-CZ edit by
  Asterios Panoras"* (maoxin123) and a notebook titled
  [vqcc-v52-asterios-invsqrt-20261114](https://www.kaggle.com/code/xianyu3/vqcc-v52-asterios-invsqrt-20261114) (xianyu3).
* My chemistry weight refit (`54bc3e71`) is in manwithacat's notebooks, and `2913ca13` in Leo Tang's.
* **10 notebooks by 8 authors** cite the SHA-256 of my files in their receipts; Alex Chilton's portfolio (165 votes)
  attached my notebook's output as an input in versions 140-153.
* Public forks by other users: 0 visible. Notebooks of others with my dataset as input: 1
  ([mizeroluckygall](https://www.kaggle.com/code/mizeroluckygall/quantum-circuits-one-toffoli-less-in-invsqrt)).

### The notebooks that use or credit my work

41 public notebooks by 34 other authors; the 15 most voted are below, all of them in [competitions/google-qcc/evidence/USES.md](competitions/google-qcc/evidence/USES.md).

| # | Notebook (link) | Author | Votes | Date | Versions | What of mine it uses / how it credits me |
|---:|---|---|---:|---|---|---|
| 1 | [24-94-lb-verified-three-task-portfolio](https://www.kaggle.com/code/alexchilton/24-94-lb-verified-three-task-portfolio) | alexchilton | 165 | 2026-11-12 | 140-153 | file reuse; kernel input; text credit: invsqrt 9c708f7b (splice at clean cuts); notebook input: lb-25-367-verified-portfolio-dqi-readout-fix; notebook input: lb-25-367-verified-portfolio-dqi-readout-fix; cites our file(s): DQI 245527f6 (readout-window transpl |
| 2 | [the-dataset-is-public-now-enjoy](https://www.kaggle.com/code/heliosli/the-dataset-is-public-now-enjoy) | heliosli | 119 | 2026-11-12 | 43-44,53 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix) |
| 3 | [the-real-150k-was-the-friends-we-made](https://www.kaggle.com/code/manwithacat/the-real-150k-was-the-friends-we-made) | manwithacat | 94 | 2026-11-12 | 130-138 | file reuse; builds on; hash cited: invsqrt 9c708f7b (splice at clean cuts); chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin |
| 4 | [google-quantum-ai-deep-eda-with-analogies](https://www.kaggle.com/code/evgendvorkin/google-quantum-ai-deep-eda-with-analogies) | evgendvorkin | 64 | 2026-11-12 | 32-37 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); credit in text |
| 5 | [vqcc-hedge-wizardry-notebook](https://www.kaggle.com/code/manwithacat/vqcc-hedge-wizardry-notebook) | manwithacat | 62 | 2026-11-14 | 28-29 | file reuse; builds on; text credit; hash cited: chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say we found the q21 e |
| 6 | [quantum-circuits-retained-product-audit](https://www.kaggle.com/code/kirilltym/quantum-circuits-retained-product-audit) | kirilltym | 56 | 2026-11-12 | 6-12 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 7 | [qcc-v25-coded-word-chemistry](https://www.kaggle.com/code/maoxin123/qcc-v25-coded-word-chemistry) | maoxin123 | 54 | 2026-11-12 | 2 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 8 | [quantum-circuits-iso-gap-dqi-h5](https://www.kaggle.com/code/atakanaldemir/quantum-circuits-iso-gap-dqi-h5) | atakanaldemir | 51 | 2026-11-11 | 13-15 | text credit; hash cited: cites our file(s): DQI 245527f6 (readout-window transplant); DQI 245527f6 (readout-window transplant) |
| 9 | [qcc-gap-3-residue-repair-and-c43-native-compiler](https://www.kaggle.com/code/atakanaldemir/qcc-gap-3-residue-repair-and-c43-native-compiler) | atakanaldemir | 50 | 2026-11-14 | 14-15 | file reuse; text credit: invsqrt e46d90c3 (dead-write fix); cites our file(s): invsqrt e46d90c3 (dead-write fix) |
| 10 | [qai-fewer-toffolis-same-qubits-lb-27-30687](https://www.kaggle.com/code/areebbb/qai-fewer-toffolis-same-qubits-lb-27-30687) | areebbb | 47 | 2026-11-12 | — | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts); invsqrt e46d90c3 (dead-write fix) |
| 11 | [verifier-guided-quantum-circuit-optimization](https://www.kaggle.com/code/prvsiyan/verifier-guided-quantum-circuit-optimization) | prvsiyan | 44 | 2026-11-11 | 40-46 | file reuse; text credit: DQI 245527f6 (readout-window transplant); invsqrt 9c708f7b (splice at clean cuts); cites our file(s): DQI 245527f6 (readout-window transplant); invsqrt 9c708f7b (splice at clean cuts) |
| 12 | [quantum-ai-fast-runner-starter-notebook](https://www.kaggle.com/code/ozertuu/quantum-ai-fast-runner-starter-notebook) | ozertuu | 30 | 2026-11-12 | 16-59,61 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 13 | [quantum-circuits-from-zero-1-sqrt-x-explained](https://www.kaggle.com/code/sheroleg/quantum-circuits-from-zero-1-sqrt-x-explained) | sheroleg | 26 | 2026-11-12 | 7 | file reuse; text credit: invsqrt 9c708f7b (splice at clean cuts); cites our file(s): invsqrt 9c708f7b (splice at clean cuts) |
| 14 | [google-quantum-compilation-starter-notebook](https://www.kaggle.com/code/pablodiegoo/google-quantum-compilation-starter-notebook) | pablodiegoo | 25 | 2026-11-11 | 29-37,40-42,46 | file reuse; text credit: DQI 245527f6 (readout-window transplant); invsqrt 9c708f7b (splice at clean cuts); cites our file(s): DQI 245527f6 (readout-window transplant); invsqrt 9c708f7b (splice at clean cuts) |
| 15 | [qcc-reproducible-circuit-portfolio](https://www.kaggle.com/code/ahoirg/qcc-reproducible-circuit-portfolio) | ahoirg | 22 | 2026-11-14 | 5 | text credit; hash cited: cites our file(s): chemistry npz 54bc3e71 (W/H2_I refit, v4); invsqrt 1ba197b0 (manwithacat): our q21 measure-first edit (e46d90c3) plus a second edit; his notes credit the identity to K. Tymchishin / M. H. Hosen and say |

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
    notebooks/                    all public versions of my 4 notebooks, one folder each
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
