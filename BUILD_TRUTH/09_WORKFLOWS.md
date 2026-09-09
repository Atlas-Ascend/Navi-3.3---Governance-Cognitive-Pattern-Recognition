# 09 — Workflows

## Primary pattern workflow

1. An approved source emits an Observation envelope.
2. Ingestion validates schema, identity, timestamps, and provenance.
3. Normalization maps the payload into NAVI canonical form.
4. Context Resolver obtains authorized temporal, graph, case, and policy context.
5. Feature Extractor derives measurable attributes.
6. Registered detectors evaluate the observation/context window.
7. Governance Interpreter evaluates policy implications and denied-action boundaries.
8. Confidence Engine calculates confidence and uncertainty.
9. Explainability Builder assembles supporting evidence, counterevidence, and rationale.
10. Signal Router emits a PatternSignal to JANUS/ODIN or requests verification/evidence where warranted.
11. Executive disposition determines whether the signal is rejected, deferred, investigated, or translated into governed work.
12. Execution occurs through Packet OS / Workforce Spine / MetaForge or another authorized system.
13. SECA/DevOS verify implementation or claim quality.
14. ProofGrid records proof-class receipts where applicable.
15. Thoth stores durable context and outcomes.
16. NAVI consumes feedback for calibration and recurrence analysis.

## Failure workflow

Malformed input -> quarantine -> audit event -> source notification.  
Detector error -> isolate detector -> preserve other detector runs -> emit diagnostic event.  
Low confidence -> no forced escalation; route as informational or request evidence.  
Conflicting signals -> contradiction report -> JANUS/ODIN resolution.  
Policy conflict -> stop recommendation promotion -> ODIN/Medusa review.

## Closed-loop invariant

Every promoted pattern must have a path to later disposition and verification so NAVI can distinguish useful recognition from noise.