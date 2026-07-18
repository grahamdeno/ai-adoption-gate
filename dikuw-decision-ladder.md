# DIKUW Decision Ladder

**Classify what an AI feature actually does before deciding how much to trust it.**

The DIKUW pyramid (Data, Information, Knowledge, Understanding, Wisdom) is a long-standing knowledge management model. Used as a decision ladder, it answers the single most skipped question in AI adoption: what rung does this feature's *output* operate on? The answer determines the human oversight the feature requires. The rule is simple: **the higher the rung, the more human stays in the loop.**

## The five rungs

- **Data.** Raw records with no context. Something happened and got captured.
- **Information.** Data organized to answer "what is true right now?"
- **Knowledge.** Patterns across information. "What tends to happen?"
- **Understanding.** Causes behind the patterns. "Why does it happen?"
- **Wisdom.** Judgment about what to do, weighing tradeoffs and consequences. "What should we do?"

## The ladder

Examples use a notional Army motor pool running vehicle readiness through a GCSS-Army style ERP. All details are fictional.

| Rung | Question answered | Notional motor pool example | Typical AI fit | Minimum trust controls |
|---|---|---|---|---|
| **Data** | What was recorded? | Raw inspection worksheet entries, usage readings, fault codes | Ingestion, extraction, validation | Data quality checks. One named source of truth. |
| **Information** | What is true right now? | The equipment status report: which vehicles are mission-capable today | Dashboards, roll-ups, summarization | Reconciliation rules. Freshness timestamps. The authoritative report is named, and AI summaries link back to it. |
| **Knowledge** | What patterns hold? | Recurring fault types by vehicle model; parts lead-time trends by supply class | Predictive analytics, anomaly detection | An analyst validates outputs before they inform decisions. Accuracy threshold documented. Drift monitored after go-live. |
| **Understanding** | Why is it happening? | Connecting readiness dips to dispatch tempo and missed preventive maintenance | Decision support, causal analysis | Human review required. AI proposes, the analyst disposes. Every output carries its reasoning. |
| **Wisdom** | What should we do? | Next quarter's fleet management plan; accepting risk on aging pacing items | Advisory input only | The decision stays human. AI input is labeled as input. A named person owns the outcome. |

## How to run the ladder

1. Write the proposed AI feature in one sentence.
2. Ask which rung the **output** operates on. Not the data it consumes. A feature that reads Data but outputs a recommendation is operating at Understanding or above.
3. Read across the table for the minimum controls at that rung.
4. If the controls cannot be met, the feature drops a rung or waits. That is a legitimate product decision, not a failure.

Rule of thumb: most "the AI will tell us what to do" proposals are Knowledge-rung features wearing a Wisdom costume. Split them.

## Worked example (notional)

**Proposal:** "A readiness assistant that predicts which vehicles will go non-mission-capable in the next 30 days and recommends which parts to order."

**Walk the ladder.** This is two features in one sentence. Predicting failures is pattern work: Knowledge rung. Recommending parts to order shapes a resourcing decision: Understanding rung, edging toward Wisdom, because ordering commits funds.

**Decision.** Split it. The prediction ships first, with an analyst validating output against the authoritative status report and a documented accuracy threshold before anyone briefs it. The ordering recommendation ships as advisory only: the maintenance chief approves every requisition, and the assistant's suggestion is labeled as a suggestion. Automated ordering is out of scope until the prediction earns trust in production.

**Result.** Go, with a smaller scope and controls on record. The feature got more shippable by getting more honest about its rung.

## Use with an AI assistant

Copy this entire file, then paste it with the following prompt:

```
You are helping me classify a proposed AI feature using the DIKUW decision ladder above.

My proposed feature: [one sentence]

Walk the feature up the ladder one rung at a time. Tell me which rung its OUTPUT
operates on, list the minimum trust controls from the table, and flag any part of
the feature that operates on a higher rung than the rest. If it spans rungs,
propose how to split it.
```

---

DIKUW is a general knowledge management model. This interpretation aligns with the PMI-CPMAI methodology. All examples are fictional. Licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
