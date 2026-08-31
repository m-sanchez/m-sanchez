## I build AI you can actually audit.

[![Website](https://img.shields.io/badge/miguelsanchez.co.uk-B45309?logo=firefox&logoColor=white)](https://miguelsanchez.co.uk)
[![LinkedIn](https://img.shields.io/badge/in%2Fmiguelsanchezduran-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/miguelsanchezduran)
![Location](https://img.shields.io/badge/Dubai-6E6E6E)
![Experience](https://img.shields.io/badge/15%2B_years_in_production-2F6F44)

Senior software engineer building production AI systems where models
propose and software decides what can ship. Fifteen years of systems
engineering under the AI work: architecture, correctness, failure modes,
security, testing, operability.

## Flagships

### [clawdeck](https://github.com/m-sanchez/clawdeck)

A complete local developer tool: event ingestion with a durable spool and
idempotent replay, a single-writer leased store, SSE streaming, process
lifecycle with PID-ownership checks, OTEL telemetry, GitHub/GitLab
connectors that degrade instead of crashing, and a loopback security
boundary (per-launch bearer, anti-rebinding Host checks, a named-action
allowlist, no shell endpoint). Zero runtime dependencies, real CI.

### [careful-machine-reference](https://github.com/m-sanchez/careful-machine-reference)

The reference architecture for the pattern the tools below share: a model
proposes, deterministic components certify, and the design principles are
executable invariants. Contract, authority, capability, scope, evidence,
claim, certification-or-refusal, narration, replay - each a boundary you
can locate in the types and the tests. Companion code for *The Careful
Machine* (forthcoming, 2026).

## AI systems toolkit

The tools below were extracted from one body of work and published in
2026, then hardened into installable, CI-proven packages. The calibration
and significance work is standard ML statistics, implemented carefully
from the public literature. Each tool is standalone and zero-dependency.

**Evidence & verification**
[evidence-gates](https://github.com/m-sanchez/evidence-gates) ·
[grounded-claims](https://github.com/m-sanchez/grounded-claims) ·
[careful-verifier](https://github.com/m-sanchez/careful-verifier) ·
[tamper-bench](https://github.com/m-sanchez/tamper-bench) ·
[u-pack](https://github.com/m-sanchez/u-pack)

**ML evaluation & calibration**
[calibrated](https://github.com/m-sanchez/calibrated) - is the model's
confidence honest (ECE, Brier, temperature scaling) ·
[ab-significance](https://github.com/m-sanchez/ab-significance) - did B
really beat A (paired McNemar + bootstrap) ·
[probe-heads](https://github.com/m-sanchez/probe-heads) - reproducible
probing with train/val/holdout hygiene ·
[frozen-eval](https://github.com/m-sanchez/frozen-eval) ·
[silent-zero](https://github.com/m-sanchez/silent-zero)

**Runtime & process controls**
[careful-router](https://github.com/m-sanchez/careful-router) ·
[gpu-quiescence](https://github.com/m-sanchez/gpu-quiescence) ·
[training-forge](https://github.com/m-sanchez/training-forge) ·
[clean-room-guard](https://github.com/m-sanchez/clean-room-guard)

Watch one model fail and pass the same question:
[five recorded runs and a live tamper bench](https://miguelsanchez.co.uk/careful-machine)
where you try to trick the verifier in your own browser.

## Writing

- [Building AI That Cites or Refuses](https://miguelsanchez.co.uk/writing/building-ai-that-cites-or-refuses/)
- [The Silent Zero: Proving Absence in Very Large Data](https://miguelsanchez.co.uk/writing/the-silent-zero-proving-absence/)
- [Designing Evidence Gates for Production LLM Systems](https://miguelsanchez.co.uk/writing/evidence-gates-production-llms/)
- [How I Evaluate Production RAG Systems](https://miguelsanchez.co.uk/writing/evaluating-production-rag/)

## Working rules

Evidence before confidence · a person owns the decision · least data,
shortest time. The full set, each with the control that enforces it:
[miguelsanchez.co.uk/ethics](https://miguelsanchez.co.uk/ethics)

---

[miguelsanchez.co.uk](https://miguelsanchez.co.uk) · contact@miguelsanchez.co.uk
