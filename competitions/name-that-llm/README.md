# Kaggle Name That LLM

Competition: [kaggle.com/competitions/name-that-llm](https://www.kaggle.com/competitions/name-that-llm). Each text is a short answer written by one of 18 language models to one of 150 prompts; the task is to name the model. The best public score the notebook reports is 0.706 (another author's).

This was a short side project (my first submission there is dated 2026-11-17), and **it is an analysis notebook, not a score notebook of mine**: the leaderboard score in its title belongs to the public pipeline that the notebook copies unchanged in its second part (credited below); my part is the error analysis.

## Notebook

[0.704 | Which LLMs Look Alike? Error Map and Ideas](https://www.kaggle.com/code/asteriospanoras/0-704-which-llms-look-alike-error-map-and-ideas) (27 votes on 2026-11-20; last run 2026-11-19 21:16 UTC; 16 versions).
Source: [`notebooks/0-704-which-llms-look-alike-error-map-and-ideas/v16.ipynb`](notebooks/0-704-which-llms-look-alike-error-map-and-ideas/v16.ipynb), the **latest version only** (version 16, pulled 2026-11-20, outputs stripped; the 18 AI-assisted illustrations embedded in the first code cell are replaced by `REMOVED_EMBEDDED_BINARY`; the full notebook is on Kaggle).

**Part 1, the analysis** (CPU only, about 10 minutes, runs only in the interactive run): a simple proxy detector (character and word TF-IDF plus a linear SVM, prompt-grouped 5-fold CV) is used to map where fingerprints get confused. Findings, stated for the proxy only, not for the top pipeline: it gets 34% of the 18 classes right and the right family for 70% of the texts; the two GLM models, the three GPT-5.6 models and Gemini 3.7 vs 3.8 Flash are near coin flips for the text alone; 46% of its mistakes cross a family boundary; "prompt-group tricks" (centering, Hungarian assignment) gain up to 10 points when all 18 texts of a prompt are present and lose about 5 with two texts, and the gain disappears when a quarter of a group is wrong; the truth is in the top 3 for 65% of the texts, but a naive two-class fix did not help. A section of five ideas for improvement is marked **not tested**; no gain is claimed.

**Part 2, the pipeline** that produces the leaderboard score: the public notebook "0.706 | GLM Fable Routing + 256-Token Likelihood" by Omer Faruk Merey, built on lightningv08's 0.704 pipeline, copied without change to its code cells; the notebook lists the public datasets and notebooks of many other authors as inputs (for example the Kaggle users lucasboesen, nuridudak and dhruvtibarewal; the full credits are at its end). None of those inputs is mine.

## Scores

Read with `kaggle competitions submissions name-that-llm` on 2026-11-20: the submissions listed there, all of the pipeline above, scored **0.702** (2026-11-17, 2026-11-19 twice) and **0.703** (2026-11-19 21:15 UTC, described as "v14 = lightningv08 v12 pipeline"). The title's 0.704 is the pipeline author's public score; identical code spread over 0.012 across six submissions in one author's table, so one public number says little. I did not re-check the leaderboard rank on 2026-11-20 and make no rank claim, and I did not map each submission to a notebook version.

## Used by others

Not scanned.
