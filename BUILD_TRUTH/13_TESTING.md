# 13 — Testing

## Verification strategy

NAVI requires both software correctness tests and epistemic/pattern-quality evaluations.

## Test classes

### Contract tests
Validate Observation, PatternSignal, ExecutiveDisposition, and VerificationFeedback schema compatibility across versions.

### Unit tests
Cover normalization, feature extraction, detector logic, scoring, policy interpretation, routing, and idempotency.

### Temporal tests
Use synthetic timelines to prove recurrence, escalation, oscillation, stagnation, convergence, and decay detection.

### Contradiction tests
Verify that conflicting sources remain represented and are not silently collapsed into a single false certainty.

### Governance tests
Attempt prohibited paths including self-authorization, destructive execution, proof substitution, bypass of JANUS/ODIN, and policy weakening. All must fail closed.

### Security tests
Exercise malformed provenance, unauthorized data classes, injection content, replay events, forged receipt references, and unsafe model outputs.

### Integration tests
Validate Thoth, CaseGraph, JANUS/ODIN, Packet OS, Workforce Spine, MetaForge, SECA/DevOS, Medusa, CrownGrid, and ProofGrid adapters against contract fixtures.

### Calibration evals
Measure precision, recall where ground truth exists, false-positive rate, false-negative rate, confidence calibration, usefulness after executive disposition, and verification support rate.

## Regression corpus

Every significant false positive, missed pattern, governance failure, or contract break becomes a permanent regression fixture when legally and operationally appropriate.

## Promotion rule

A detector is not production-eligible because it produces convincing prose. It must pass deterministic tests, governance tests, and evaluation thresholds defined for its pattern class.