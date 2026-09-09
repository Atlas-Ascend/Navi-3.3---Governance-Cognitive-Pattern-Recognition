# 08 — Agent Contracts

## Contract model

NAVI participates in the estate as a bounded analytical agent/service. Every handoff specifies producer, consumer, accepted artifact, authority boundary, acknowledgement, and failure route.

## NAVI contract

### Inputs
Validated observations, graph state, memory context, work telemetry, verification results, and policy context.

### Outputs
PatternSignal envelopes, evidence requests, contradiction reports, recurrence clusters, drift reports, and confidence-calibrated recommendations.

### Allowed actions
- read authorized context
- classify and correlate observations
- run registered detectors
- create advisory signals
- request additional evidence
- write NAVI-owned analytical state
- emit audit events

### Denied actions
- execute arbitrary work
- mutate external canonical state directly
- bypass JANUS/ODIN
- declare work verified
- issue ProofGrid receipts
- weaken Medusa policy
- approve its own recommendations
- redefine detector governance without a governed change

## Primary agent/system relationships

- **Thoth -> NAVI:** memory and temporal context; NAVI returns durable pattern summaries after governance/disposition.
- **CaseGraph -> NAVI:** entity/relationship/state context; NAVI returns pattern annotations, never silent graph rewrites.
- **NAVI -> JANUS PRIME:** executive pattern brief and recommended routes.
- **NAVI -> ODIN:** governance/risk interpretation requiring supervisory judgment.
- **NAVI -> SECA/DevOS:** request validation, falsification, reproducibility, or technical inspection.
- **NAVI -> Workforce Spine:** only through executive-approved work packets.
- **NAVI -> MetaForge:** remediation/build recommendation only after routing authority exists.
- **ProofGrid -> NAVI:** evidence receipts close the learning loop.

## Handoff invariant

No recipient should need to infer whether a NAVI artifact is observation, hypothesis, recommendation, authorization, execution result, or proof. The class must be explicit.