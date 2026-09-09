# 04 — Requirements

## Functional requirements

NAVI 3.3 SHALL:

1. accept versioned evidence envelopes from approved estate systems;
2. normalize events into a common observation model;
3. correlate observations across entity, system, case, repository, agent, and time dimensions;
4. detect recurrence, anomaly, contradiction, drift, escalation, convergence, bottlenecks, and opportunity patterns;
5. distinguish observed facts, derived features, hypotheses, recommendations, and verified outcomes;
6. attach source references, timestamps, pattern window, confidence, severity, and governing policy references to outputs;
7. support deterministic rule patterns and probabilistic/model-assisted patterns;
8. produce machine-readable and human-readable pattern reports;
9. route recommendations to JANUS/ODIN rather than self-executing them;
10. ingest verification outcomes to calibrate future confidence.

## Non-functional requirements

- **Explainability:** every material pattern must expose why it fired.
- **Traceability:** every conclusion must resolve to source evidence IDs.
- **Idempotency:** duplicate input events must not generate uncontrolled duplicate actions.
- **Observability:** ingestion, evaluation, emission, rejection, and failure paths must be logged.
- **Determinism where possible:** identical deterministic inputs/rules produce identical outputs.
- **Isolation:** source failures must not corrupt canonical NAVI state.
- **Versioning:** schemas, detectors, policies, and scoring strategies are versioned.
- **Safety:** denied capabilities remain denied regardless of model suggestion.
- **Portability:** runtime must support local EDEN nodes and remote/container deployment without changing contracts.

## Minimum viable resident state

A compliant resident-state implementation can ingest observation envelopes, execute a detector registry, create pattern signals with provenance/confidence, route them to a mock executive consumer, and preserve the resulting verification feedback loop.