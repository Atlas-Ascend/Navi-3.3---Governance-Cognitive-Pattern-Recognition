# 05 — Architecture

## Architectural position

NAVI 3.3 is a resident analytical organ inside VISHVARUPA. It is downstream of sensing/memory and upstream of executive judgment.

```text
Sources
  |-- Thoth
  |-- Universal CaseGraph
  |-- Packet OS
  |-- Workforce Spine
  |-- Repo/build telemetry
  |-- SECA / DevOS
  |-- ProofGrid
  |-- Medusa / CrownGrid
  v
[Ingestion Gateway]
  v
[Normalization + Provenance]
  v
[Pattern Engine]
  |-- deterministic rules
  |-- temporal recurrence
  |-- anomaly detection
  |-- contradiction analysis
  |-- drift detection
  |-- convergence analysis
  |-- model-assisted classifiers
  v
[Governance Interpreter]
  v
[Confidence + Explainability]
  v
[Signal Router]
  |-- JANUS PRIME
  |-- ODIN
  |-- SECA / DevOS evidence request
  |-- Thoth memory writeback
  v
Execution occurs elsewhere
```

## Architectural layers

1. **Ingress** — validates source identity, schema, time, and provenance.
2. **Canonical observation layer** — converts source-specific payloads into normalized observations.
3. **Feature layer** — derives temporal, relational, frequency, severity, and state-transition features.
4. **Detector layer** — runs versioned detector plugins.
5. **Governance layer** — interprets results against policy and denied-capability constraints.
6. **Explainability layer** — assembles evidence chains and confidence rationale.
7. **Signal layer** — emits bounded PatternSignal envelopes.
8. **Feedback layer** — consumes executive dispositions and verification outcomes.

## State model

NAVI maintains detector configuration, pattern state, correlation windows, evidence references, confidence calibration data, and disposition feedback. Source-of-truth business/domain state remains in its owning system.

## Deployment model

The architecture is transport-agnostic. The same contracts may be implemented using local files/queues on EDEN, HTTP/events on Render, or estate message transport through CrownGrid. Runtime placement must never alter governance semantics.