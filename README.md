# Miguel Sánchez Durán

Senior software engineer in Dubai, with 15+ years of production experience. I build full-stack applications and applied AI tools, with a focus on evaluation, usable interfaces, and reproducible results.

[Website](https://miguelsanchez.co.uk) · [LinkedIn](https://www.linkedin.com/in/miguelsanchezduran/) · [Writing](https://miguelsanchez.co.uk/writing/)

## Featured work

### [Calibration Explorer](https://github.com/m-sanchez/calibration-explorer)

Check whether a classifier's confidence matches how often it is correct. Import prediction files, keep calibration, policy-validation, and test rows separate, and export an HTML report, experiment JSON, or prediction CSV.

The recorded UCI digits example retains all 1,797 original test rows. Temperature scaling leaves accuracy at 94.88% and reduces test negative log-likelihood from 0.17595 to 0.15753. This is one reference result, not a guarantee for other data. Confidence-only CSV inputs support measurement; fitting needs logits and known labels.

[Open the app](https://huggingface.co/spaces/m-sanchez/calibration-explorer) · [Website copy](https://miguelsanchez.co.uk/calibration-explorer/) · [Recorded evidence](https://github.com/m-sanchez/calibration-explorer/tree/v0.2.0/review)

### [Ocelin](https://github.com/m-sanchez/ocelin)

A local companion for Codex and Claude Code: find sessions across projects, inspect their history, and resume the intended conversation. It has a browser interface and an optional Windows app. Preview releases are labelled; the optional Ask Ocelin feature sends a compact snapshot to the configured model.

[See the workflow](https://miguelsanchez.co.uk/ocelin/) · [Downloads and release notes](https://github.com/m-sanchez/ocelin/releases)

### [Recorded routing study](https://github.com/m-sanchez/routing-study#the-real-model-arm)

In one recorded comparison using Claude Haiku 4.5, domain-specific prompts scored 67.75% against 82.75% for a generalist prompt under strict first-token scoring, the rule registered before the run. For every question the domain prompts lost to the generalist under that rule, the reply showed its working first, answered "No." with a full stop, or was cut off at the 256-token limit; none was a finished wrong answer. Scored on final answers, a rule chosen after reading the replies, the domain prompts scored 91% and the generalist 88%, and the difference was not significant (exact McNemar p=0.14, or 0.40 over the 372 distinct prompts). One model, 400 questions (372 distinct) and one recording: this is not evidence about routing in general. [Read the re-score analysis](https://github.com/m-sanchez/routing-study#re-scoring-the-real-model-arm-what-the-strict-scorer-measured).

## Inspect and reproduce

| Project | Evidence and reproduction |
| --- | --- |
| Calibration Explorer | [Tagged source, setup, reference provenance, and replay instructions](https://github.com/m-sanchez/calibration-explorer/tree/v0.2.0) |
| calibrated | [Numerical corrections and distribution status for v2.0.1](https://github.com/m-sanchez/calibrated/releases/tag/v2.0.1) |
| Routing study | [Recorded model transcript and replay](https://github.com/m-sanchez/routing-study#the-real-model-arm) under the registered scorer, a [post-hoc final-answer re-score](https://github.com/m-sanchez/routing-study#re-scoring-the-real-model-arm-what-the-strict-scorer-measured) of the same transcript, and a separately labelled synthetic study |
| Careful Machine | [Public reference implementation](https://github.com/m-sanchez/careful-machine-reference) and [interactive evidence demo](https://miguelsanchez.co.uk/careful-machine/) |

The Careful Machine repository illustrates an approach with public reference code and synthetic examples. It is not my employer's production system. Reproducing recorded output establishes repeatability; correctness and generalisation need additional evidence.

<details>
<summary>Smaller libraries and engineering tools</summary>

These repositories contain focused utilities with their own installation instructions, tests, and limitations.

- **Evidence and verification:** [grounded-claims](https://github.com/m-sanchez/grounded-claims), [careful-verifier](https://github.com/m-sanchez/careful-verifier), [u-pack](https://github.com/m-sanchez/u-pack).
- **Evaluation and calibration:** [calibrated](https://github.com/m-sanchez/calibrated), [ab-significance](https://github.com/m-sanchez/ab-significance), [probe-heads](https://github.com/m-sanchez/probe-heads), [frozen-eval](https://github.com/m-sanchez/frozen-eval), [silent-zero](https://github.com/m-sanchez/silent-zero).
- **Runtime and process controls:** [careful-router](https://github.com/m-sanchez/careful-router), [gpu-quiescence](https://github.com/m-sanchez/gpu-quiescence), [training-forge](https://github.com/m-sanchez/training-forge), [clean-room-guard](https://github.com/m-sanchez/clean-room-guard).

</details>

## Writing

- [Accuracy stayed the same. Confidence changed.](https://miguelsanchez.co.uk/writing/calibration-explorer-accuracy-and-confidence/)
- [Building AI That Cites or Refuses](https://miguelsanchez.co.uk/writing/building-ai-that-cites-or-refuses/)
- [How I Evaluate Production RAG Systems](https://miguelsanchez.co.uk/writing/evaluating-production-rag/)
- [What 15 Years of Software Engineering Taught Me About AI Engineering](https://miguelsanchez.co.uk/writing/software-engineering-lessons-for-ai/)

If you try a project, an issue describing the task, release, and point of confusion is useful feedback. Please omit private inputs and credentials.

[miguelsanchez.co.uk](https://miguelsanchez.co.uk) · contact@miguelsanchez.co.uk · Dubai
