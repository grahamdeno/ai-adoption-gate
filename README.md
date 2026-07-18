# AI Adoption Gate

**Trustworthy AI is a product decision, not a model decision.**

A lightweight set of decision gates for adopting AI features in regulated environments. Each artifact is a one-page decision aid a product owner, business analyst, or program lead can run in minutes, before capability excitement turns into a commitment nobody scoped.

This is Stage 7, Trust, in my [delivery decision chain](https://github.com/grahamdeno). The first six stages get working software shipped. This stage decides whether an AI feature deserves to be trusted with a decision, and under what controls.

## Why this exists

AI features fail in regulated environments for predictable reasons: the wrong problem, no usable data, no ROI case, or trust controls bolted on after the fact. Every one of those is a product decision that should have been made deliberately, early, and on record. These gates put those decisions on record.

## What's inside

| Artifact | Purpose | Status |
|---|---|---|
| [DIKUW Decision Ladder](dikuw-decision-ladder.md) | Classify what an AI feature actually does, and match it to the human oversight it requires | Available |
| AI Go/No-Go Gate | Business, data, and implementation feasibility checks before any build starts | Planned |
| Trustworthy AI Layer Checklist | Layer-by-layer trust questions for regulated delivery | Planned |
| Failure Pre-Mortem | Run the known AI project killers against your feature before Phase IV | Planned |
| Human-in-the-Loop Disposition Patterns | Who approves, who reviews, who audits, matched to risk | Planned |
| Lightweight Eval Template | Acceptance criteria for probabilistic features | Planned |
| Worked Example | One notional scenario run through every gate end to end | In progress |

Artifacts move from Planned to Available as they are built. This repo grows deliberately, not all at once.

## Method alignment

The structure and vocabulary here align with the PMI-CPMAI methodology (six-phase, data-first AI project management). All content is my own interpretation and my own templates. No course materials are reproduced.

## About the examples

Worked examples use a notional Army ground-maintenance scenario: a motor pool running vehicle readiness through a GCSS-Army style ERP. I ran motor pools as an Army maintenance warrant officer, so the pain points are authentic. The data, units, and systems details are entirely fictional. Nothing in this repo reflects any current or past employer, customer, or government work product.

## Use with an AI assistant

These artifacts are plain markdown and work in any AI assistant. No plugins, no platform-specific setup.

1. Open any Available artifact and copy the full file.
2. Paste it into whatever assistant your organization approves, along with a one-sentence description of your proposed AI feature.
3. Answer its questions. You will have a classified feature and a control list in under five minutes.

Each artifact includes its own prompt block at the bottom.

## Who this is for

Product owners, business analysts, and program leads who are accountable for what an AI feature does in production, especially in government, defense, healthcare, or financial delivery, where "the model said so" is not an acceptable answer.

## License

This work is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
Share and adapt freely with attribution, for noncommercial use, under the same license.
For commercial licensing, contact me via [LinkedIn](https://www.linkedin.com/in/grahamdenoyer/).
