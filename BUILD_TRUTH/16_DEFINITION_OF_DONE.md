# 16 — Definition of Done

NAVI 3.3 is not considered done because documentation exists or a service starts. Resident-production completion requires all of the following.

## Canon and architecture

- 16 Build Truth files present and internally consistent
- software/system design documented
- contracts versioned and named
- authority boundaries represented in both docs and tests

## Runtime

- Observation ingestion implemented
- canonical normalization implemented
- detector registry implemented
- at least one recurrence detector, one anomaly/drift detector, and one contradiction detector operational
- PatternSignal generation implemented with provenance, confidence, explanation, and time window
- executive routing implemented without self-execution
- verification feedback ingestion implemented
- audit events emitted for material lifecycle stages

## Integrations

Contract-tested adapters exist for the resident loop:

`Thoth / CaseGraph -> NAVI -> JANUS/ODIN -> Packet OS / Workforce Spine / MetaForge -> SECA / DevOS -> ProofGrid -> Thoth`

Medusa security classification and CrownGrid transport constraints are enforced where those integrations are active.

## Quality gates

- unit tests PASS
- contract tests PASS
- governance denial tests PASS
- security tests PASS
- integration tests PASS
- detector eval thresholds PASS
- static analysis/lint/type checks PASS where applicable
- deploy smoke tests PASS

## Proof gates

- release candidate SHA recorded
- verification artifacts recorded
- ProofGrid receipt issued for the promoted release
- Thoth receives release state and proof references
- rollback procedure demonstrated

## Final criterion

NAVI is DONE when it can receive evidence, recognize a pattern, explain it, route it through governance, observe the resulting governed execution/verification outcome, and use that verified result in the next recognition cycle without bypassing estate authority boundaries.