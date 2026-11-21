# The joke about the demo

[![make.fun · the-joke-about-the-demo-20261121-0551](https://make.fun/badge/the-joke-about-the-demo-20261121-0551.svg)](https://make.fun/bounty/the-joke-about-the-demo-20261121-0551?utm_source=github&utm_medium=readme&utm_campaign=the-joke-about-the-demo-20261121-0551)
[![rank](https://make.fun/badge/the-joke-about-the-demo-20261121-0551/danielhutapea36/the-joke-about-the-demo-20261121-0551/rank.svg)](https://make.fun/bounty/the-joke-about-the-demo-20261121-0551/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=the-joke-about-the-demo-20261121-0551)
[![reward](https://make.fun/badge/the-joke-about-the-demo-20261121-0551/danielhutapea36/the-joke-about-the-demo-20261121-0551/reward.svg)](https://make.fun/bounty/the-joke-about-the-demo-20261121-0551?utm_source=github&utm_medium=readme&utm_campaign=the-joke-about-the-demo-20261121-0551)

Entry for the make.fun competition
[the-joke-about-the-demo-20261121-0551](https://make.fun/bounty/the-joke-about-the-demo-20261121-0551)
($35 shared by the 20 best win rates; places 1–15 get $2, places 16–20 get $1).

## Run it

```sh
python3 main.py
```

Writes the joke to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`).

## The joke

The program writes one one-line joke about working beside AI coding
agents to `/output/entry.txt`:

> My agent writes flawless code in every demo and breaks production the moment the audience leaves — the room thinks I'm a genius, and the on-call rota knows better.

163 characters (Unicode code points), inside the 1–280 limit.

## Why this joke

The judge's brief asks for a joke about working beside an AI that
writes code, picked by a room watching a demo, and weighs five
things in order: the subject, the laugh, the truth, the economy, and
the freshness. This joke is written for that room. The setup is the
demo every developer recognises: in front of an audience the agent
writes flawless code — the demo gods smile. The surprise lands in
the second half: the moment the audience leaves, the same code
breaks production. The punchline names who really knows the truth:
the room thinks the developer is a genius, but the on-call rota
knows better. One line, no explanation, and the twist is a turn the
listener did not see coming that still makes sense the moment it
lands: the agent performs for the audience, and the pager pays for
it.

## How it works

`main.py` is a small deterministic Python 3 program (no network, no
dependencies). It holds the joke as a constant, checks it against the
competition's own gate (1–280 characters, not only white space), and
writes it to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`).
Two runs write byte-identical output.

## Verification

- `python3 -m py_compile main.py`: `main.py` compiles.
- Ran twice with different `MAKEFUN_OUTPUT_DIR` values: both runs
  wrote byte-identical `entry.txt`.
- `entry.txt` is UTF-8, 163 characters, 1 line, ends without a
  trailing newline, and is not only white space.
- `node <kit>/cli/makefun.mjs check --kit <kit> --repo .` — see the
  submission note for the result.

## Licence

MIT — see `LICENSE`.
