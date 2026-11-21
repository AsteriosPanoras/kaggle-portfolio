# What I actually contributed to the public in Google QCC: a lineage study

Competition: [google-verifiable-quantum-circuit-compilation](https://www.kaggle.com/competitions/google-verifiable-quantum-circuit-compilation).
State of 2026-11-18, 21:00 UTC. The public top is **28.23162/28.23163**: maoxin123's invsqrt `d0227f3c` (74,405.67),
ozertuu's merged DQI `15a4b740` (345,256,821,434) and leotang09's chemistry weights `4d63be3d` (294,642,170.57) on
maoxin123's 4,022-Toffoli loaders and Lera's table. **None of these three files is mine.** Credit lines only show
the last changes, so I also compared the files themselves (section 4.1). That test found **none of my edits in their
bytes**: each edit is either absent or its site was rewritten by a later author. The test cannot rule out influence
that left no bytes behind.

**Addendum of 2026-11-20.** The public top moved on after this study (28.23498, 28.23837, 28.24094 and, in other authors' notebooks, 28.24398), again with other authors' files: Koushik Rudra's, ozertuu's, manwithacat's, Manvender Singh's and Ghazaros Barseghyan's sets. My analysis-notebook versions 28, 31, 34 and 35 only re-package and hash-check those public file sets (ties with the public notebooks of the same files), so they add **no new contribution** to the table below, and I did not repeat the byte comparison of section 4.1 on the newer files (not done on 2026-11-20). The one new item of mine is in the Atlas: its version 6 holds a `frontier/` folder with the 28.23498 and 28.23837 file sets, a receipt with SHA-256 values and the authors' licence notices.

**Addendum of 2026-11-21.** The public top moved from 31.69 to **33.10** (goodpjw2008's 33.10186, boristown's 33.10189, with other authors' files again: Rithvik Redrouthu's 37-qubit invsqrt, tonylica's DQI, ozertuu's chemistry table, boristown's recompiled loader). My notebooks only re-packaged or combined public file sets (scores 31.68159, 31.69052, 33.06908 and 33.10186, all ties with other authors' files), so they add **no new contribution** to the table above. Two new checks, both small: (1) **file identity (VERIFIED)**: none of my 11 published file hashes (`9c708f7b`, `e46d90c3`, `245527f6`, `5778cdd5`, `54bc3e71`, `2913ca13`, `5a753866`, `5ea23cc0`, `f67851ac`, `09000960`, `f05297b4`) is among the 18 members of the 33.10186 set; the byte-level edit test of section 4.1 was **not** repeated on the newer files. (2) **who credits what (VERIFIED, scan of 117 notebooks, [USES.md](evidence/USES.md))**: 21 notebooks credit the LP angle re-solve as prior art (Almond Labs among them), the Atlas is an input of several, and the wrong "V36 loaders" credit of section 5 has spread to nine more notebooks. The map of my four notebooks, version by version, is in [NOTEBOOK_MAP.md](NOTEBOOK_MAP.md).

This page looks past the scores of my notebooks and asks: which ideas and files were mine, did others adopt them, how
much did each one measurably change the score, and what is left of it in today's best files. It covers only public
work. Sources: SHA-256 lineage in my [QCC Circuit Atlas](https://www.kaggle.com/datasets/asteriospanoras/qcc-circuit-atlas)
(`circuits.csv`, `contributions/`), the run logs and receipts of my notebook versions (all versions are in
[notebooks/](notebooks/)), the credit lines in other authors' public notebooks (pulled with `kaggle kernels pull`), and
[evidence/USES.md](evidence/USES.md).

**Evidence labels.** **VERIFIED**: I read the source text, log, receipt or Atlas row myself for this study.
**REPORTED**: someone else's text or an earlier scan in this repository says it, and I did not re-read the original
for this study. **UNVERIFIED**: plausible but not shown. **Judgment**: my assessment, not a measurement.

## 1. How the points are computed

Score = geometric mean of three ratios REF/cost (REF: invsqrt 2,076,774.23; DQI 24,439,463,583,672.93; chemistry
3,355,599,588.32). If one task's cost goes from `c_old` to `c_new` at a portfolio score `G`, the score changes by
`G * ((c_old / c_new)^(1/3) - 1)`. With today's three files (`G` = 28.23163), **a 1 % cost cut in any one task is worth
0.0947 points**; one executed Toffoli in the 44-qubit invsqrt (cost = 44 x Toffoli-equivalents) is worth 0.0056 points.

## 2. Contributions, with their effect when released

"Effect when released" is the change against the file it was applied to, on the day of release, through the formula
above. It is **not** a counterfactual: it does not say what the public score would be today without me (see section 4).

| # | Date (UTC) | What | Mine? | Evidence | Cost change (official verifier) | Effect when released (points) | Adopted by | In today's top files? | Class |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 11 Nov | DQI readout-window transplant `245527f6`: two decoder regions with CSWAP readout windows moved from the `e9f54be3` line (Atakan Aldemir's technique) onto Atakan Aldemir's `bb4287e7` | the transplant only | Atlas `contributions/dqi` (VERIFIED) | mean Toffoli 394,165.16 -> 394,116.88 (-0.0123 %) | +0.0010 at 25.367 | Atakan Aldemir rebuilt the same bytes the same evening and wrote "byte-identical to asteriospanoras's 245527f6 composition, independently rebuilt" (REPORTED, USES.md); 2 other notebooks ship it (Atlas, VERIFIED) | No: the whole decoder line was replaced by Syed Asad Ali's decoders on 12 Nov | B |
| 2 | 11 Nov 22:58 | invsqrt splice at clean cuts `9c708f7b`: shortest-path search over cuts where wires and phase agree, 16 pieces of 7 public 62-qubit circuits (mainly WCao24's normaliser and Thomas Gamet's early prefix) | yes (method and file) | Atlas `contributions/invsqrt`, `tools/splice_dp.py` (VERIFIED) | 93,739.35 -> 93,555.26 (-0.196 %) | **+0.0166** at 25.396 | shipped by 21 other notebooks of 18 authors (Atlas `all_sources`, VERIFIED); in the public top 25.4048 of 12 Nov (REPORTED, session notes) | No: superseded on 12 Nov evening by Syed Asad Ali's 46-qubit invsqrt (80,162.76, about -14 %) | C (judgment) |
| 3 | 12 Nov | two more retained AND products in maoxin123's 392k DQI (`5778cdd5`), extending Areeb Ali's retention method | the extension only | Atlas row, first source my notebook (VERIFIED) | -1.6 Toffolis per shot of 392,016 | +0.00004 at 25.45 | cited by alex chilton and Thomas Gamet (REPORTED, USES.md); reused from an unsubmitted output (REPORTED, session notes) | No: superseded the same evening | D |
| 4 | 14 Nov 09:47 | invsqrt dead-write fix `e46d90c3`: in Atakan Aldemir's `dcde7078`, `CCX q16 q20 q21` whose target is only X-measured later becomes `HMR q21 b61; CZ q16 q20 if b61` | the edit at this site; **not** the identity | Atlas `contributions/invsqrt`; official verifier and exact simulation on all 3,133,452 inputs (VERIFIED) | 78,765.51 -> 78,719.53 (-0.058 %) | **+0.0053** at 27.297 (board 27.29709 -> 27.30241) | shipped by 8 other notebooks of 7 authors (Atlas, VERIFIED); manwithacat's `1ba197b0` = this edit plus one more, which was the public top 27.31616 that evening (VERIFIED, USES.md hash match) | **No, superseded (byte test, VERIFIED, section 4.1).** maoxin123's credit for `d0227f3c` names "measured-CZ / dead-write ideas by Asterios Panoras and James Barlow" (VERIFIED text). But in `d0227f3c`, and already in Syed Asad Ali's 44-qubit `47b31838`, the whole q21 block around the site is gone, so the edited operations have nothing to sit on | A (judgment) |
| 5 | 14 Nov | chemistry W/H2_I refits at fixed words `2913ca13`, `54bc3e71`, `5a753866` (numpy port of prvsiyan's GRG refit) | the refits; the method is prvsiyan's | Atlas `contributions/chemistry_refits` (VERIFIED) | lambda_eff -9.0e-6, -6.7e-7, -3.1e-7 relative | +0.00008, +0.000006, +0.000003 | `54bc3e71` was in manwithacat's public top 27.31616 (REPORTED, USES.md); `2913ca13` shipped by leotang09 (REPORTED, USES.md) | No: today's weights `4d63be3d` are leotang09's refit of `703843d3` on boristown's seed line (VERIFIED, credit text in public notebooks) | D |
| 6 | 15 Nov | refit of Lera's c44 weights (`5ea23cc0`, in Atlas `best/`) | the refit | Atlas `best/README.md` (VERIFIED) | lambda_eff 46.92764 -> 46.92495 (-0.0057 %) | +0.0005 at 28.06 | none found | No: boristown's refit of the same weights was better the same day, and my 28.06018 release used his (VERIFIED, README) | D |
| 7 | 15 Nov | exact LP re-solve of the 34 invsqrt rotation angles (the phase is linear in the angles): `09000960` on Syed Asad Ali's v13, then `f67851ac` on jeffemerson's `9339eecc` | yes | notebook text and receipts (VERIFIED) | 75,170.62 -> 75,170.13 (-0.00065 %) | +0.00006 (board, `f67851ac` vs the same portfolio without it: 28.07495 -> 28.07502, VERIFIED) | credited by kirderf, Atakan Aldemir ("29 inverse angle refinements"), boristown, ozertuu, evgendvorkin, hayatohikawa (REPORTED, 16 Nov scan); kirderf's portfolio builds on it (REPORTED) | **No (byte test, VERIFIED, section 4.1).** None of the 29 re-solved angle values appears in `f2cdab0b`, `563d0583`, `864f81cd` or `d0227f3c`, which have a different rotation set (43-48 `Z_POW`). My scan of `563d0583` also found its angles already at the LP optimum; they are credited to ozertuu's angle refit | A (judgment) |
| 8 | 12-15 Nov | **QCC Circuit Atlas** dataset: every public circuit file deduplicated by SHA-256 with sources, authors, copies, kmx text, tools (`kmsim`, `qccscope`, splice, refit toolkit) | yes (dataset and tools; the refit method is prvsiyan's) | `kaggle datasets list` on 18 Nov 21:03 UTC: 10,706 downloads, 14 votes (VERIFIED) | none (not a file of the submission) | none directly | 5 public notebooks of 3 other authors attach it (ozertuu x2, mizeroluckygall x2, evgendvorkin; `kaggle kernels list --dataset`, VERIFIED). ozertuu's Fast Runner (version pulled 18 Nov 01:13 UTC) imported `refit.grg2` from it and ran a 3-minute chemistry refit (VERIFIED source); his evening version no longer imports it but still attaches the dataset | Not a file; ozertuu's 28.23163 notebook attaches the dataset and credits me in its list, but its source does not call it (VERIFIED) | B (judgment) |
| 9 | 14-18 Nov | analysis notebook: 19 measured ideas, 4 walls, an exact simulator, a detector library, three negative scans on the 28.19 frontier, a board-draw table | yes | [analysis notebook](https://www.kaggle.com/code/asteriospanoras/qcc-28-23162-what-we-tried-what-failed-and-why), v21-v26 (VERIFIED) | none | none | bronze medal, 28 votes; **no public notebook found that cites a negative result to skip work** (searched the pulled notebooks; aiokajima only mentions the re-verification). **Update of 2026-11-21 (VERIFIED):** manwithacat's public dataset `vqcc-chemistry-negative-results` records five of these results as ledger rows NR-0305 to NR-0309, with a link to this notebook | n/a | D |
| 10 | 15-18 Nov | releases that re-verified other authors' files (28.07495 to 28.23162), including a byte-patch reproduction of boristown's `5f901c55` | assembly and checks only | READMEs and receipts (VERIFIED) | none of mine | ties with the public scores of the same files | the notebooks have 44, 52 and 28 votes | the 28.23162 files are other authors' | B |

How the classes are meant: **A** easy for others to find, my gain is mostly time saved for everyone; **B** an
assembly or integration of others' work, my gain is time saved by assembling and re-verifying; **C** a strong
improvement (large measured effect and/or adopted and credited); **D** a modest effect whose value is hard to prove.
All class assignments are judgments; the reasons follow.

## 3. Why each class

* **Splice (C).** The largest measured effect of mine (+0.0166, about 18 % of a 1 % task cut) and the most copied file
  (21 notebooks, 18 authors). It needed a search tool, not a one-line edit, and nobody published the same file before
  it (the Atlas "first source" column is scan order, not priority, so "first" is UNVERIFIED). It lasted less than a
  day: Syed Asad Ali's new circuits made it obsolete. Strong but short-lived.
* **Dead-write fix (A).** Measured +0.0053, widely shipped, and still named in the credit chain of today's invsqrt.
  But it is one instance of a standard identity (measurement-based uncomputation, Gidney 2018); manwithacat credits
  the identity to Kirill Tymchishin (proof) and Md. Hamid Hosen (rewrite) and writes that I "found the same q21 edit
  independently" (VERIFIED); boristown's notebook says it was "reproduced independently from our prior local
  dcde7078" and claims no invention (VERIFIED). Any dead-write detector finds it. My file was the first public one we
  can date (09:47 UTC; earlier private copies are possible). Value: a few hours earlier for everyone.
* **LP angle re-solve (A).** Arithmetic on a linear phase; worth +0.00006. Others' angle refits reach the same
  optimum, and on the current line the optimum is already met (credited to ozertuu). Widely credited, small in points.
* **DQI readout transplant (B).** The rewrite was Atakan Aldemir's; I moved it onto his newer file, and he produced
  the same bytes the same day.
* **Atlas (B).** It indexes other people's files. Its value is time saved: provenance, deduplication, credits, and a
  refit toolkit that at least one top author ran inside his notebook. Downloads do not show use.
* **Chemistry refits, retained products, tools, negative results (D).** Effects of 1e-4 points or less, or no
  measurable effect; no evidence that anyone skipped work because of the negative scans.
* **Re-verification releases (B).** These notebooks held or tied the best public score on several days (27.31220 on
  14 Nov, 28.06018 tied on 15 Nov), but from 16 Nov on the scoring files are other authors' work.

## 4. Today's frontier and the counterfactual

Credit lines named two things of mine as possible ancestors of today's invsqrt: the dead-write edit and the LP angles.
The byte-level test below finds **neither in the bytes** (VERIFIED). The dead-write site no longer exists in the
44-qubit line, and the LP angle values are absent. The DQI and chemistry files contain no edit of mine either
(VERIFIED, below). So today's top files carry **0 points** of my edits as bytes. **What the public score would be
without my participation cannot be proven**: others found the dead-write edit independently, and the splice and the
readout transplant were stepping stones that others built on for a day or less. I do not give a number for it.

### 4.1 Lineage test at the byte level

Method (18 Nov, VERIFIED: I ran it on the files with the circuit reader `qc.ir`, without kickmix). For each edit I
compared operation sequences in two ways:
* **Exact k-grams:** runs of k consecutive operations with their qubit numbers.
* **Canonical k-grams:** the qubits renamed in order of first use, so that a change of layout (62 -> 46 -> 44 qubits;
  892 -> 890) does not hide a shared run.

I measured two things: how much of one file's runs appear in the other (lineage), and whether the operations at the
edited site appear in the later files. Labels: **SURVIVES**, **NOT FOUND**, **SUPERSEDED** (the site was replaced by
a different construction), **INCONCLUSIVE**.

| Edit | Method | Result | What it proves, and what it does not |
|---|---|---|---|
| invsqrt dead-write fix `e46d90c3` (op 3292 of `dcde7078`) | Canonical 16-gram chain over 13 files; site windows k = 6-24 covering the edited ops; dead-write detector (CCX whose target is next touched only by `HMR`) | **SUPERSEDED.** Chain: `d0227f3c` shares 96 % of its canonical 16-grams with `864f81cd`, 77 % with `563d0583`, 75 % with `f2cdab0b`, but only 42 % with `dcde7078`/`e46d90c3`, which is the background level (it equals its share with any file of the 46/44-qubit family). The windows around the edit match **0 times** at every k in `47b31838`, `9339eecc`, `09000960`, `f2cdab0b`, `563d0583`, `864f81cd` and `d0227f3c`. The flanking blocks do match (`e46d90c3` ops 3260-3282 = `d0227f3c` 2944-2965; 3295-3310 = 2972-2987). The 7 operations between them (`CX 16 21; CX 17 21; CX 18 21; CX 18 16; HMR q21; CZ q16 q20 if b61; CX 18 16`) have no counterpart: the 44-qubit line does not compute q21 there at all. Dead writes: 1 in `dcde7078`, 0 in every later file | The site of my edit was removed whole by a stronger rewrite: first visible in Syed Asad Ali's v13 `47b31838`, then carried into maoxin123's `f2cdab0b` line. My edit is not in the bytes. Whether my file led anyone to the larger rewrite cannot be shown. manwithacat's `1ba197b0` did build on the edit (same flanks; it moves the measurement of q21 earlier), but that file is not an ancestor of today's line by this test |
| invsqrt splice `9c708f7b` (62 qubits) | Canonical 16-grams against `d0227f3c`, `47b31838` and 62-qubit controls | **NOT FOUND.** 1 % of `d0227f3c`'s canonical 16-grams occur in `9c708f7b`, against 0-7 % for unrelated 62-qubit files | The 44-qubit line is a new synthesis. The splice was a stepping stone and has no bytes in it |
| LP-re-solved angles `09000960`, `f67851ac` | Exact 128-bit angle values; the top 44 bits as a coarse check | **NOT FOUND.** 0 of the 29 re-solved values in `f2cdab0b`, `563d0583`, `864f81cd`, `d0227f3c`, even at the coarse level (both files agree with each other on 27 of 29) | Today's line has a different rotation set (43-48 `Z_POW`, against 39), so these angles cannot carry over |
| DQI readout-window transplant `245527f6` (892 qubits) | Exact 24-grams of `245527f6` looked up in `15a4b740`, split by the file's region tags | **NOT FOUND.** Overall 4.8 % shared, almost all in the decoder-independent frame: `mask_projection` 99.9 %, `restore_masks` 100 %. The decoder sections share 0.0-1.2 % (`aligned_route` 0.09 %, `inverse12 products` 0.42 %, `gf_iadd` 1.2 %). `15a4b740` and `575b043f` have **0 `CSWAP`** and no region tags | The construct the transplant changed (CSWAP readout windows in the tagged 892-qubit decoder) does not exist in the 890-qubit line. Limit: I located the two transplanted regions only through the section split, not op by op (the parent `bb4287e7` is not local and was not downloaded) |
| DQI two retained AND products `5778cdd5` | Op-level diff against its parent `4c81b726` (the kmx parsed locally): 2 sites, ops 51,461,550 (+2) and 51,468,298 (+4), product `q12*q828` kept on `q858`, uncomputed with `HMR`/`CZ_IF`. Then 24-gram (qubits) and 48-gram (types only) lookup of both sites in `15a4b740` | **NOT FOUND.** 0 of 54 and 0 of 79 qubit-level windows at the two sites. Type-only windows match 58/78 and 10/103, but 81 % of all type-only 48-grams match anyway (generic CX runs), so that says nothing. The file as a whole shares 5.2 % (the same frame sections) | The retained products are not present in the current DQI. Products in today's files are boristown's and Grant Prater's (section 5). `e208d350` was not scanned (ozertuu's variant of the same 890-qubit line; REPORTED) |
| chemistry refits `2913ca13`, `54bc3e71`, `5a753866` (14 Nov) | L2 distance of the concatenated `W` and `H2_I` arrays over 32 local weight files of shape (8,143,44) | **NOT FOUND.** Distance 15.46 to `4d63be3d`, against 0.10-0.29 inside today's family. Different words and `U` | These refits belong to the older 14,728-Toffoli table. Today's weights sit on another table |
| chemistry refit `5ea23cc0` (Lera's c44) | Same distances, plus the direction of each later step from the shared start `906fa220` (the public coded-word table) | **NOT FOUND (side branch).** Nearest to `4d63be3d` is `703843d3` (0.105), then `bdae290f` (boristown, 0.147). `5ea23cc0` is 0.291 from it. The steps from `906fa220` to `bdae290f`, `703843d3` and `4d63be3d` have cosine **-0.19, -0.15, -0.11** with my step, and `bdae290f` is farther from my file (0.252) than from the start (0.154) | No trace of my step in the current weights; boristown's refit started from the table, not from mine. A continuous refit forgets its start only partly, so a small influence from a common start cannot be excluded. But the measured directions point away from my file, not towards it |

**What this changes.** The two "UNVERIFIED" cells of section 2 (rows 4 and 7) are now answered: no bytes of mine. The
dead-write site was **superseded**, not inherited: Syed Asad Ali's 44-qubit construction no longer has the block
the edit was in. Independent rediscovery does not apply to it, because no later file performs the same rewrite at
that site. **Points still in today's files from my edits: 0** (formula of section 1). The values "when released"
in section 2 stand. The test covers bytes only: it cannot show ideas, checks or time saved that others passed on
without copying a file.

**Indirect effects (judgment; not provable and not counted above).** What may remain of the work is less in the bytes
than in the way the search runs:
* *The measured-CZ pattern is now ordinary.* Today's invsqrt `d0227f3c` has 593 classically controlled `CZ` sites
  after a measurement and no dead write left (both VERIFIED by reading the file, section 4.1). The identity is Gidney's, and others found the same edit independently, so I do not claim the
  file; but a dead-write check as a routine step of every release is how the sites got closed, and it is named in the
  credit chain of the invsqrt.
* *Searching started from the same shared index.* The Atlas is attached to the notebooks of three other authors,
  and ozertuu's Fast Runner version of 18 Nov 01:13 ran its refit tool (VERIFIED). A shared, deduplicated list of
  every public file, with sources, spared each author the same bookkeeping. That is time saved, not a score, and I
  cannot measure it.
* *One change can unlock another.* The splice, the readout transplant and the retention extension were published
  with exact checks and were reused by 21 notebooks; later files were built on top of files that already carried them
  (Atlas lineage). Whether the later gains would have come a day later without them is unknowable from the public
  record. I list it as a possibility, not as a result.

## 5. Credited to me, but not (or not only) mine

* Balram Srinivasan's package credits `f05297b4` as a "finer weights refit by Asterios Panoras". My log shows that
  my in-notebook refit left lambda_eff unchanged (46.92158337179646 before and after): `f05297b4` is Atakan Aldemir's
  `703843d3` weights re-saved, with **no gain** (VERIFIED).
* leotang09 writes that pair-window retention on `5f901c55` was "first published by Asterios Panoras". The six
  products are boristown's patch on Grant Prater's file, and the pair-window lemma is Grant Prater's; my notebook only
  reproduced and re-verified it (VERIFIED, my README and section 8 of the analysis notebook).
* ozertuu credits me for "the GRG2 ... chemistry weight optimization toolkit": the method is prvsiyan's
  `refit_grg.py`; mine is the numpy port and packaging.
* "measured-CZ / dead-write ideas": the identity is not mine; the edit at this site is mine, found independently.
* prvsiyan (read 2026-11-20) credits "Asterios Panoras (V36 of his notebook)" with re-encoding 56 angle-word rows of the ThemBones table so that loaders k5, k6, k7 need one Toffoli fewer per pass, and takes "his" loaders and words. **Wrong attribution (VERIFIED from the logs):** version 36 of my notebook re-packaged the public file set of almondlabs' notebook *VQCC 31.68159 Improved Chemistry Gauge and Loader* (its `submission.zip`, member for member, sha256 of the zip `a45c95bf`), which already contained that loader recompilation. The work is almondlabs'; mine was the packaging.
* **The same wrong attribution has spread (read on 2026-11-21, VERIFIED from the sources).** jeffemerson's *Cheaper Chem Loaders* notebook credits "**Asterios Panoras**: the V36 table that refit was measured on"; aiokajima's *Alex 31.68 reproduction* and alex chilton's *33.10 LB* notebook write "with Asterios Panoras' re-encoded loaders k5-k7, one Toffoli fewer per pass each"; abdelghanicharouiti's *Quantum Omni* notebooks anchor "all 18 almondlabs/Panoras V36 members"; bhaviklimani's *Widle verified* notebook credits "Asterios Panoras" for a DQI component and quotes the baseline sha256 `a45c95bf...`, which is the zip of almondlabs' set that my version 36 only re-packaged; prvsiyan's latest version still lists "earlier loader recoding" under my name. In all of them the loader work, the table and the DQI are **almondlabs'** (or ThemBones' and others'), not mine. I have not commented on those notebooks; I list the cases here so that the record is clear.

## 6. Superseded

The splice, the readout transplant and the retained products (Syed Asad Ali's 12 Nov decoders and circuits), the
14 Nov refits (later weights by Atakan Aldemir, boristown, leotang09), the c44 refit (boristown's, same day). On
12 Nov my "25.449" portfolio was not first: 78 teams had 25.44953 on the board about 4 hours before my notebook
(REPORTED, session notes). A DQI file with three retained products that I built on 18 Nov (`327b0751`) uses the same
sites as boristown's `5f901c55`, so it adds nothing.

## 7. Process contribution

* **Volume.** 4 public notebooks, 69 public versions (19 + 6 + 26 + 18), 8 days (11-18 Nov), 22 board scores listed in
  the [progression](README.md#my-leaderboard-progression) for those days, plus the 10,706-download Atlas.
* **Verification discipline.** Every submitted file passed the unchanged official verifiers inside the notebook;
  every input file is pinned by SHA-256 and credited with its licence; invsqrt edits were also checked exactly on all
  3,133,452 inputs. Public notebooks keep `WRITE_SUBMISSION = False`, so the output holds no `submission.zip`. One
  private-kernel test submission on 17 Nov wasted a daily slot; since then every submission goes through the public
  notebook only.
* **Lessons.** The DQI is sampled and the board draws its own shots from the file hash: boristown's `f425ea20` was
  clean locally but lost a shot on the board (28.0884), and ozertuu's `e208d350` gave 28.18862 on the board against
  28.23174 locally. Only reuse DQI files that already have a board score.

## 8. What is NOT mine

The circuits and weights behind every score above 27.31 are other authors' public work: **Syed Asad Ali** (from-source
invsqrt, DQI and chemistry builders), **Lera (marculera)** (DF-THC table, coded words, loaders), **maoxin123** (44-qubit
invsqrt line, 392k DQI, 4,022-Toffoli loaders), **boristown** (refits, chain and product-cache patches, `5f901c55`),
**Grant Prater** (merged decoder, pair-window lemma), **Balram Srinivasan** (GF(2^24) closings, converter), **Atakan
Aldemir** (DQI readout windows, `dcde7078`, `703843d3` weights), **Ertuğrul Özer (ozertuu)** (merged DQI `15a4b740`,
angle refits, DQI extractor cutoff, the fast runner), **leotang09** (`4d63be3d` weights), **manwithacat (James Barlow)**
(measure-out edits, retention, tools), **vumaniacom** (retention), **junmiaotiao** (frontier datasets), **Ali Haydar Özdağ**
(64-row table, `4560ac0c`), **WCao24** and **Thomas Gamet** (the circuits my splice joined), **prvsiyan** (refit method),
**Areeb Ali** (product retention), **team ThemBones (Danish Ali)** (the 31.68 circuits: 39-qubit invsqrt, 901-qubit DQI, 405-qubit chemistry), **almondlabs** (chemistry gauge and loader recompilation, the 31.69054 set), and the authors they credit. Where I rebuilt or re-verified their files, that is all
I did.
