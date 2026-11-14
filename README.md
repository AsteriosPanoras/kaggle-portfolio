# Asterios Panoras: Kaggle portfolio

**Kaggle profile: [kaggle.com/asteriospanoras](https://www.kaggle.com/asteriospanoras)**

I work on exact, verifiable optimisation and on honest evaluation. In November 2026 I published, in the Google Quantum
AI *Verifiable Quantum Circuit Compilation* competition, public notebooks that held the best public notebook score
when released (latest: 27.31220 on 2026-11-14 <!-- OWNER: confirm "best public notebook score" -->), an analysis notebook that won a bronze medal, and a dataset of every public circuit of the
competition (1,483 downloads). Each improvement was proven exactly (on all inputs where possible) and confirmed with
the hosts' official verifiers, and other competitors adopted them within hours: 26 public notebooks by
22 other authors contain files I published first, byte for byte. Every claim below links to a Kaggle page
you can open without an account.

## Highlights

| Item | Competition | What it is | Score / rank | Votes | Link |
|---|---|---|---|---:|---|
| QCC 27.307 \| Frontier + Finer Chemistry Refit | Google Verifiable Quantum Circuit Compilation | public solution notebook: chemistry weight refit run inside the notebook + the best public circuits, all re-verified | public LB **27.31220** (2026-11-14); owner reports best public notebook score that day <!-- OWNER: confirm --> | 7 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-307-frontier-finer-chemistry-refit) |
| QCC 27.30 \| What Works, What Fails and Why | Google Verifiable Quantum Circuit Compilation | analysis notebook: score anatomy, sixteen measured ideas, an exact numpy simulator and a detector library | **bronze medal** (owner-reported) <!-- OWNER: confirm medals --> | 11 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-what-works-what-fails-and-why) |
| QCC 27.30 \| Public Frontier + Free CZ Fix in invsq | Google Verifiable Quantum Circuit Compilation | the invsqrt dead-write fix (one Toffoli fewer per shot, exact), adopted by 9 public notebooks | public LB 27.30241 (2026-11-14) <!-- OWNER: confirm medals --> | 13 | [notebook](https://www.kaggle.com/code/asteriospanoras/qcc-27-30-public-frontier-free-cz-fix-in-invsq) |
| LB 25.367 \| Verified Portfolio + DQI Readout Fix | Google Verifiable Quantum Circuit Compilation | DQI readout-window rewrite (-48 Toffolis) and the invsqrt splice at clean cuts (-3 Toffolis), adopted by 17 public notebooks | public LB 25.36727 (v1), 25.39570 (v4) <!-- OWNER: confirm medals --> | 21 | [notebook](https://www.kaggle.com/code/asteriospanoras/lb-25-367-verified-portfolio-dqi-readout-fix) |
| QCC Circuit Atlas | Google Verifiable Quantum Circuit Compilation | dataset: every public circuit file, deduplicated by SHA-256 and credited, with tools | 1,483 downloads | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas) |
| S6E11 \| How Much of the Public Top Is Real? | Playground Series S6E11 | analysis: public-leaderboard noise, the winner's curse, nested-CV replay of ladder steps | — <!-- OWNER: confirm medals --> | 11 | [notebook](https://www.kaggle.com/code/asteriospanoras/s6e11-how-much-of-the-public-top-is-real) |
| Supervisory layer for HVAC (paper code) | research | code, protocols and per-episode results of the paper "Re-select or Learn?" | 41 downloads | 1 | [dataset](https://www.kaggle.com/datasets/asteriospanoras/supervisory-layer-hvac) · [GitHub](https://github.com/AsteriosPanoras/supervisory-layer-hvac) |

Votes as listed by the Kaggle CLI on 2026-11-15.

## Used by others

Details, dates and links for every row: [competitions/google-qcc/evidence/USES.md](competitions/google-qcc/evidence/USES.md).

* **26 public notebooks by 22 authors** ship files I published first (identical SHA-256), e.g.
  the invsqrt splice `9c708f7b` (17 notebooks, including Alex Chilton's top-voted portfolio) and the dead-write fix
  `e46d90c3` (9 notebooks, including Atakan Aldemir's and maoxin123's frontier notebooks; the first within two hours of release).
* **3 further notebooks** ship manwithacat's invsqrt `1ba197b0`, which contains the same q21 edit as my dead-write
  fix plus a second edit (his notes say I found the q21 edit independently of the identity's earlier credit).
* **23 public notebooks by 20 authors** credit me by name in their text, e.g. *"the measured-CZ edit by
  Asterios Panoras"* (maoxin123) and a notebook titled
  [vqcc-v52-asterios-invsqrt-20261114](https://www.kaggle.com/code/xianyu3/vqcc-v52-asterios-invsqrt-20261114) (xianyu3).
* My chemistry weight refit (`54bc3e71`) is in manwithacat's notebooks, and `2913ca13` in Leo Tang's.
* Public forks by other users: 0 visible. Notebooks of others with my dataset as input: 1
  ([mizeroluckygall](https://www.kaggle.com/code/mizeroluckygall/quantum-circuits-one-toffoli-less-in-invsqrt)).

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
    notebooks/                    sources of my 4 public notebooks (outputs stripped)
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
