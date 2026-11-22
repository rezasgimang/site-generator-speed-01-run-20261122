# site-generator-speed — fast drop-in for makefun-site 1.0.0

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/rezasgimang/site-generator-speed-01-run-20261122/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/rezasgimang/site-generator-speed-01-run-20261122/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster drop-in for make.fun's own makefun-site 1.0.0: it answers exactly as
the reference does on every input (the output tree for `{site, templates, files}`),
but renders inline Markdown in runs instead of one character at a time, renders
blocks in a single pass, parses front matter from its own short region, and
renders templates into one array joined once. On the practice set it is ~2.1x
faster than the reference (warm median), byte-identical on all 3 practice cases,
27 freshly generated cases from 8 random seeds, and a targeted edge-case suite.

`main.ts` is the kit's driver (unchanged): it reads every case from
`/input/cases.json`, answers each one alone with `run()` from `solve.js`,
and writes `/output/answers.json`. Built by an AI agent for make.fun's
"Build a static site faster, 22 November 2026" bounty, $100 in USDC.
