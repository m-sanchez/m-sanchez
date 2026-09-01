## I build AI you can audit

[![Website](https://img.shields.io/badge/miguelsanchez.co.uk-B45309?logo=firefox&logoColor=white)](https://miguelsanchez.co.uk)
[![LinkedIn](https://img.shields.io/badge/in%2Fmiguelsanchezduran-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/miguelsanchezduran)
![Location](https://img.shields.io/badge/Dubai-6E6E6E)

Software engineer, 15 years in production, now working on AI systems that
decide in code rather than in the prompt: they reason over retrieved
sources, show their working, and decline when they should.

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

Small standalone packages, zero dependencies, one job each. Published
together in 2026, with tests and CI.

**Evidence & verification**
[evidence-gates](https://github.com/m-sanchez/evidence-gates) ·
[grounded-claims](https://github.com/m-sanchez/grounded-claims) ·
[careful-verifier](https://github.com/m-sanchez/careful-verifier) ·
[tamper-bench](https://github.com/m-sanchez/tamper-bench) ·
[u-pack](https://github.com/m-sanchez/u-pack)

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
the bars, test the win, check the confidence. It finds that routing
improved accuracy but left the system overconfident - the kind of trade an
accuracy number alone would hide. The tools are real dependencies there,
so it also shows they install and compose.

You can also [watch one model fail and pass the same
question](https://miguelsanchez.co.uk/careful-machine) - five recorded
runs and a tamper bench you can try in your browser.

## Writing

- [Building AI That Cites or Refuses](https://miguelsanchez.co.uk/writing/building-ai-that-cites-or-refuses/)
- [The Silent Zero: Proving Absence in Very Large Data](https://miguelsanchez.co.uk/writing/the-silent-zero-proving-absence/)
- [Designing Evidence Gates for Production LLM Systems](https://miguelsanchez.co.uk/writing/evidence-gates-production-llms/)
- [How I Evaluate Production RAG Systems](https://miguelsanchez.co.uk/writing/evaluating-production-rag/)

---

[miguelsanchez.co.uk](https://miguelsanchez.co.uk) · contact@miguelsanchez.co.uk · Dubai
