## Hello there!

[![Website](https://img.shields.io/badge/miguelsanchez.co.uk-B45309?logo=firefox&logoColor=white)](https://miguelsanchez.co.uk)
[![LinkedIn](https://img.shields.io/badge/in%2Fmiguelsanchezduran-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/miguelsanchezduran)
![Location](https://img.shields.io/badge/Dubai-6E6E6E)

I am a Senior software engineer, 15+ years in production, now working on AI
systems that decide in code rather than in the prompt: they reason over
retrieved sources, show their working, and decline when they should.

## Start here

### [clawdeck](https://github.com/m-sanchez/clawdeck)

A local dashboard for Claude Code: sessions, events, cost, worktrees and
reviews in one loopback web app. No build step, zero dependencies, and a
real security boundary (per-launch token, Host checks, an action
allowlist, no shell endpoint). A complete developer tool, not a snippet.

### [careful-machine-reference](https://github.com/m-sanchez/careful-machine-reference)

A small reference implementation of the pattern the tools below share: the
model proposes, deterministic code certifies, and each design rule is a
test you can run. Companion code for *The Careful Machine* (forthcoming,
2026).

## The tools

Small standalone packages, zero dependencies, one job each, with tests and
CI. The reliability and control tools came out of one body of production
work; the ML-evaluation utilities are fresh implementations of standard
methods, written to test the same systems more rigorously. Published
together, in a short burst in 2026.

Eleven of them are on npm under the `@m-sanchez` scope:

```bash
npm install @m-sanchez/<name>
```

`gpu-quiescence` is Python: `pip install gpu-quiescence`. Every package
also has tagged releases if you would rather pin to git.

Every package carries a `CLAIMS.md`: each falsifiable claim on its README
mapped to the test that enforces it. If a claim has no test, it does not
stay on the README.

**Evidence & verification**
[grounded-claims](https://github.com/m-sanchez/grounded-claims) - the
verification kit: a check chain where the LLM judge is structurally
advisory, plus the turn-level gates ·
[careful-verifier](https://github.com/m-sanchez/careful-verifier) -
browser-safe claim verification, and the tamper bench that drives the
[live demo](https://miguelsanchez.co.uk/careful-machine) ·
[u-pack](https://github.com/m-sanchez/u-pack)

*(evidence-gates and tamper-bench were folded into grounded-claims and
careful-verifier on 2026-09-01; both archived, history intact.)*

**ML evaluation & calibration**
[calibrated](https://github.com/m-sanchez/calibrated) - is the model's
confidence honest? (ECE, Brier, temperature scaling) ·
[ab-significance](https://github.com/m-sanchez/ab-significance) - did B
beat A, or is it noise? (paired McNemar + bootstrap) ·
[probe-heads](https://github.com/m-sanchez/probe-heads) - probing with
train/val/holdout hygiene ·
[frozen-eval](https://github.com/m-sanchez/frozen-eval) ·
[silent-zero](https://github.com/m-sanchez/silent-zero)

**Runtime & process controls**
[careful-router](https://github.com/m-sanchez/careful-router) ·
[gpu-quiescence](https://github.com/m-sanchez/gpu-quiescence) ·
[training-forge](https://github.com/m-sanchez/training-forge) ·
[clean-room-guard](https://github.com/m-sanchez/clean-room-guard)

[routing-study](https://github.com/m-sanchez/routing-study) puts four of
them together in one reproducible experiment: route to specialists, freeze
the bars, test the win, check the confidence. It is a controlled synthetic
study - the harness deliberately includes overconfident specialists - that
shows why routing has to be evaluated on calibration as well as accuracy:
the eval catches a system that clears the accuracy bar while failing
calibration. The tools are real pinned dependencies there, so it also
shows they install and compose. A real-model arm was recorded on
2026-09-02: 400 questions to claude-haiku-4-5, and routing lost by 15
points, with calibration worse too. The transcript is committed, so the
table in that README is the one a replay reproduces rather than one I
typed.

You can also [watch one model fail and pass the same
question](https://miguelsanchez.co.uk/careful-machine) - five recorded
runs and a tamper bench you can try in your browser.

## What you can rerun

| Repo | Command | What it pins | Prints | Time |
|---|---|---|---|---|
| [routing-study](https://github.com/m-sanchez/routing-study) | `git clone https://github.com/m-sanchez/routing-study && cd routing-study && npm ci && npm test && npm run study` | `test/pinned.test.ts` (the per-domain table: timeline 208/300 for both systems) and `test/study.test.ts` (the dispatch invariant) | `     timeline: 69.3% and 69.3% are identical by construction` | about 29 s |
| [calibrated](https://github.com/m-sanchez/calibrated) | `git clone https://github.com/m-sanchez/calibrated && cd calibrated && npm ci && npm test && npm run demo` | `test/claims.test.ts` (runs the demo and matches its lines) | `after (T=4.45)         ECE 0.006   Brier 0.204   accuracy 71.6%` | about 11 s |
| [routing-study](https://github.com/m-sanchez/routing-study) | `git clone https://github.com/m-sanchez/routing-study && cd routing-study && npm ci && npm run real` | `test/real.test.ts` (the replay is held to the pinned summary and to the sha256 of the transcript) | `ab-significance: on the 400 examples both models scored: A 82.8%, B 67.8%; McNemar p=0.0000, B-A -15.0pp [-19.8, -10.3]. A is better, beyond noise and beyond the declared bar.` | about 41 s |

Times are from one laptop; the last row includes the clone, the other two
cover the npm steps only. The calibrated line is matched as printed by
`test/claims.test.ts`; the routing-study lines are rendered from figures
pinned by `test/pinned.test.ts` and `test/real.test.ts`. A different line is
a bug report either way. The real-model arm replays from a committed
transcript, so it needs no API key and spends nothing.

## Using one of these?

These are weeks old. If one of them earns a place in your build, or fails
to, an issue on the repo is the feedback I most want. Every package has
tagged releases and an install-proof job, so what you get from the
registry is what the tests ran against.

## Writing

- [Building AI That Cites or Refuses](https://miguelsanchez.co.uk/writing/building-ai-that-cites-or-refuses/)
- [The Silent Zero: Proving Absence in Very Large Data](https://miguelsanchez.co.uk/writing/the-silent-zero-proving-absence/)
- [Designing Evidence Gates for Production LLM Systems](https://miguelsanchez.co.uk/writing/evidence-gates-production-llms/)
- [How I Evaluate Production RAG Systems](https://miguelsanchez.co.uk/writing/evaluating-production-rag/)
- [Building Reliable Agentic AI Systems](https://miguelsanchez.co.uk/writing/reliable-agentic-ai-systems/)
- [What 15 Years of Software Engineering Taught Me About AI Engineering](https://miguelsanchez.co.uk/writing/software-engineering-lessons-for-ai/)

---

[miguelsanchez.co.uk](https://miguelsanchez.co.uk) · contact@miguelsanchez.co.uk · Dubai
