# QCC 28.12769 | What Works, What Fails and Why

Kaggle: [https://www.kaggle.com/code/asteriospanoras/qcc-28-12769-what-works-what-fails-and-why](https://www.kaggle.com/code/asteriospanoras/qcc-28-12769-what-works-what-fails-and-why) · medal: **bronze** · votes: 18 (2026-11-17 midday) · versions: 20

## Address history

First titled "QCC 27.30 | What Works, What Fails and Why" (`qcc-27-30-what-works-what-fails-and-why`), retitled on 2026-11-15 to "QCC 28.06018 | What Works, What Fails and Why" (`qcc-28-06018-what-works-what-fails-and-why`), and renamed by me on 2026-11-16 to "QCC 28.12769 | What Works, What Fails and Why" (`qcc-28-12769-what-works-what-fails-and-why`). Both older addresses redirect to the current one (HTTP 302, checked 2026-11-17). The folder of this repository was renamed to match.

## Versions 15 to 20 (2026-11-16)

* The notebook was rebuilt around the 28.1277 portfolio of 16 November: new figures (the invsqrt and DQI landscapes, the family tree of the submission), a refreshed embedded `qccscope` archive and the updated section on what worked and what failed.
* **Version 19** built and re-verified the 28.1277 files in the notebook and submitted them (submission 58446073, 2026-11-16 22:03 UTC): public score **28.12769**. These files are other authors' public work (maoxin123's invsqrt `0af21cb8`, Balram Srinivasan's DQI `66b4f18b`, Atakan Aldemir's chemistry weights `703843d3`), the same ones as in the frontier notebook; they are not mine.
* Versions 15 to 18 and 20 have submission-file writing switched off.
* Earlier: **Version 13** submitted the same files as the 28.06018 release of the first notebook (submission 58398329, 2026-11-15 19:23 UTC): public score 28.06018. **Version 14** is a no-file version.
* The section "This round: what worked, what failed, and why" separates what is other people's (Syed Asad Ali's v13 invsqrt and DQI, Lera's loaders with boristown's weights) from what is mine (the exact LP re-solve of the 34 rotation angles, +6e-5 points, and the Atlas refit toolkit run in the notebook).

## Every public version

All versions are public on Kaggle (open the notebook, then "Version history"). The files here are their sources, outputs stripped.

| Version | File | Cells | Code lines | Leaderboard score of the submission made from it | What changed | Note |
|---:|---|---:|---:|---|---|---|
| 1 | [v01.ipynb](v01.ipynb) | 28 | 429 | — | first version |  |
| 2 | [v02.ipynb](v02.ipynb) | 28 | 429 | 25.36727 | same sections, code/text revised |  |
| 3 | [v03.ipynb](v03.ipynb) | 42 | 593 | — | new sections: LB 25.36727 \| QCC analysis toolkit: exact simulator, cost anatomy, what works and what fai, Exchange rates: what one qubit, one Toffoli or one rotation is worth, The public frontier over time, The invsqrt landscape: 73 public circuits in qubits x Toffoli-equivalents ...; removed: LB 25.367 \| QCC toolkit: exact simulator, cost anatomy, what works and what fails |  |
| 4 | [v04.ipynb](v04.ipynb) | 42 | 593 | 25.36727 | new sections: LB 25.367 \| QCC toolkit: exact simulator, cost anatomy, what works and what fails; removed: LB 25.36727 \| QCC analysis toolkit: exact simulator, cost anatomy, what works and what fai |  |
| 5 | [v05.ipynb](v05.ipynb) | 42 | 593 | 25.36727 | same sections, code/text revised |  |
| 6 | [v06.ipynb](v06.ipynb) | 66 | 1004 | 25.44953 | new sections: Setup, Toolbox: `kmsim` (explained in [section 3](#s3)), The score, The kickmix instruction set, on one card ...; removed: LB 25.367 \| QCC toolkit: exact simulator, cost anatomy, what works and what fails, 1. The score in one table, The public frontier over time ... |  |
| 7 | [v07.ipynb](v07.ipynb) | 66 | 1030 | 27.30241 | new sections: Setup: rebuild the submission and verify it (about 15 minutes), invsqrt (46 qubits; one qubit = 2.2% of the cost), DQI (889 qubits; one qubit = 0.22% of the cost, about 860 Toffolis), Chemistry (the loaders are 55% of the Toffolis; the factorization sets the rest) ...; removed: Setup, Toolbox: `kmsim` (explained in [section 3](#s3)), The two phase streams ... | embedded code zip kept; local default paths removed |
| 8 | [v08.ipynb](v08.ipynb) | 66 | 1030 | — | same sections, code/text revised | embedded code zip kept; local default paths removed |
| 9 | [v09.ipynb](v09.ipynb) | 66 | 1030 | — | same sections, code/text revised | embedded code zip kept; local default paths removed |
| 10 | [v10.ipynb](v10.ipynb) | 66 | 1030 | — | new sections: A demo of <code style="background: #eef1f6; color: #111111; padding: 1px 5px; border-radiu, 5.0 <code style="background: #eef1f6; color: #111111; padding: 1px 5px; border-radius: 4px; removed: A demo of `qccscope`, our analysis library, 5.0 `kmsim`: an exact numpy simulator for these circuits | embedded code zip kept; local default paths removed |
| 11 | [v11.ipynb](v11.ipynb) | 66 | 1037 | 27.30670 | same sections, code/text revised | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle; embedded code zip kept; local default paths removed |
| 12 | [v12.ipynb](v12.ipynb) | 66 | 1037 | — | same sections, code/text revised | embedded binary data (refitted chemistry weights) removed; the full cell is on Kaggle; embedded code zip kept; local default paths removed |
| 13 | [v13.ipynb](v13.ipynb) | 72 | 1200 | 28.06018 | new sections: Setup: rebuild the submission and verify it (about 50 minutes), invsqrt (the 46-qubit line; one qubit = 2.2% of the cost), DQI (the 889-qubit line; one qubit = 0.22% of the cost, about 860 Toffolis), What worked on 14 November: the dead write, drawn and checked ...; removed: Setup: rebuild the submission and verify it (about 15 minutes), invsqrt (46 qubits; one qubit = 2.2% of the cost), DQI (889 qubits; one qubit = 0.22% of the cost, about 860 Toffolis) ... | embedded code zip kept; local default paths removed |
| 14 | [v14.ipynb](v14.ipynb) | 72 | 1200 | — | same sections, code/text revised | embedded code zip kept; local default paths removed |
| 15 | [v15.ipynb](v15.ipynb) | 75 | 1259 | — | rewritten around the 28.1277 portfolio: new figures (landscapes, family tree), embedded toolkit refreshed | embedded code zip kept; local default paths removed |
| 16 | [v16.ipynb](v16.ipynb) | 75 | 1259 | — | same sections, code/text revised |  |
| 17 | [v17.ipynb](v17.ipynb) | 75 | 1259 | — | same sections, code/text revised |  |
| 18 | [v18.ipynb](v18.ipynb) | 75 | 1259 | — | same sections, code/text revised |  |
| 19 | [v19.ipynb](v19.ipynb) | 75 | 1259 | 28.12769 (submission 58446073) | same; submission-file writing on, the 28.1277 files built and re-verified in the notebook |  |
| 20 | [v20.ipynb](v20.ipynb) | 75 | 1259 | — | same; submission-file writing off |  |

## Used by others (0 public notebooks)

Credits and reuse are listed for the whole competition in [evidence/USES.md](../../evidence/USES.md).
