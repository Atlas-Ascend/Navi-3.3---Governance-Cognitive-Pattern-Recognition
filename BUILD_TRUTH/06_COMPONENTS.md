# 06 — Components

## Runtime components

### 1. Ingestion Gateway
Receives estate events and evidence envelopes, validates required metadata, rejects malformed payloads, and preserves source identity.

### 2. Normalizer
Maps heterogeneous source payloads into the canonical Observation schema while preserving original references.

### 3. Context Resolver
Hydrates relevant entity, case, temporal, repository, agent, and governance context without assuming ownership of that state.

### 4. Feature Extractor
Produces measurable features such as frequency, interval, rate of change, state-transition sequences, cross-source agreement, contradiction density, retry count, and verification history.

### 5. Detector Registry
Loads versioned detectors and makes their activation criteria, expected inputs, confidence method, and output class inspectable.

### 6. Temporal Analyzer
Detects recurrence, sequence motifs, escalation, decay, oscillation, stagnation, and trend inflection.

### 7. Relational Analyzer
Detects graph patterns, dependency concentration, handoff failure, recurring ownership gaps, and cross-system coupling.

### 8. Governance Interpreter
Maps detected patterns to policies, boundaries, escalation requirements, and denied-capability constraints.

### 9. Confidence Engine
Separates evidence strength, detector reliability, source agreement, temporal support, and uncertainty into an explicit confidence object.

### 10. Explainability Builder
Constructs human- and machine-readable reasons, supporting evidence references, counterevidence, and known limitations.

### 11. Signal Router
Publishes PatternSignal envelopes only to approved downstream consumers.

### 12. Feedback Calibrator
Consumes disposition and verification outcomes to measure false positives, false negatives, detector usefulness, and confidence calibration.

### 13. Audit Ledger Adapter
Emits immutable audit events for ingestion, detector runs, signal issuance, executive disposition, and feedback ingestion.

## Component rule

No component receives more authority than necessary for its role. Recognition and execution remain physically and logically separable.