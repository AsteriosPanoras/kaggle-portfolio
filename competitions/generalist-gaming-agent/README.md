# Kaggle Generalist Gaming Agent

Competition: [kaggle.com/competitions/generalist-gaming-agent](https://www.kaggle.com/competitions/generalist-gaming-agent) (deadline 2027-03-01). One offline agent plays 32 real-time browser games across 10 genres for 10 minutes of game time each; it sees raw screen frames and answers with mouse and keyboard input. Four games ship with the data, 28 stay hidden; the public board averages 16 of the 32 and the private board (the other 16) decides the ranking.

This is a recent side project (my first submission there is dated 2026-11-23). **It is an explanation notebook, not an agent of mine**: every agent I submitted is another author's public agent, unchanged, and the score belongs to that author.

## Notebook

[GGA | Visual Guide + Best Agent + Real Game Stats](https://www.kaggle.com/code/asteriospanoras/gga-visual-guide-best-agent-real-game-stats) (5 votes on 2026-11-25).
Latest source: [`notebooks/gga-visual-guide-best-agent-real-game-stats/latest-2026-11-25.ipynb`](notebooks/gga-visual-guide-best-agent-real-game-stats/latest-2026-11-25.ipynb), outputs stripped.

What it is: a visual guide, computed from the competition files without running a model in its first twelve sections (the game clock, the action space, the four practice games, what a score means, the two official starter notebooks, compute and time, who should join, untested ideas, limits and credits), then a comparison of the public agents on the board and what two of them actually do on the practice games (measured on the competition GPU; the games' own scores cannot be read). Its inputs are my own dataset of tables [`gga-visual-guide-tables`](https://www.kaggle.com/datasets/asteriospanoras/gga-visual-guide-tables) and two public datasets of other authors (`dfranzen/pennyroyal-v253`, `carsonrodrigues/py312-portable`).

## Scores of my submissions

Read with `kaggle competitions submissions generalist-gaming-agent` on 2026-11-25 (higher is better):

| Time (UTC) | Submission | Public score |
|---|---|---|
| 2026-11-23 22:16 | the host's Gemma 4 31B starter, unchanged (a timing baseline; analysis notebook v5) | 0.093 |
| 2026-11-24 22:46 | alexchilton's 0.138 agent (host Gemma, start step, no wait), unchanged (v6) | pending when read |
| 2026-11-24 23:46 | lightningv08's V13 agent (Qwen 125B plus four practice-game controllers), unchanged (v9) | pending when read |

The notebook itself says the top score then on the board is 0.291 and that it comes with hand-written controllers for the four practice games. I claim no rank and no agent of my own.

## Used by others

Not scanned.
