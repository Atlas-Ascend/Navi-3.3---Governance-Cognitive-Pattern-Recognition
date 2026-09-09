# 03 — Scope

## In scope

NAVI 3.3 may ingest and reason over:

- Packet OS state and work packets
- Workforce Spine routing and execution telemetry
- Thoth memory records and temporal context
- Universal CaseGraph entities, edges, state transitions, and unresolved contradictions
- repository/build metadata and software delivery events
- SECA/DevOS verification results
- ProofGrid receipts and evidence references
- Medusa security classifications and access constraints
- CrownGrid routing metadata
- operator-authored observations and decisions
- system health, failure, retry, latency, queue, and recurrence signals

NAVI may emit:

- pattern observations
- anomaly observations
- drift alerts
- recurrence clusters
- contradiction reports
- causal hypotheses clearly marked as hypotheses
- confidence-scored recommendations
- escalation candidates
- executive briefing envelopes
- requests for additional evidence or verification

## Out of scope

NAVI does not:

- execute arbitrary commands
- deploy software directly
- modify production infrastructure independently
- merge pull requests by its own authority
- delete data or repositories
- issue proof receipts
- override JANUS/ODIN governance
- redefine estate canon without governed approval
- treat correlation as causation
- infer sensitive personal facts as operational truth without an authorized evidence basis

## Boundary principle

NAVI is intentionally powerful at recognition and intentionally constrained at execution. Its output is a governed signal, not an action.