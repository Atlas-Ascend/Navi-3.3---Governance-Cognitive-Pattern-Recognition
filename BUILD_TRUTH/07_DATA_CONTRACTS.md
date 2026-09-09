# 07 — Data Contracts

## Contract principles

All NAVI inputs and outputs are versioned envelopes with stable identifiers, provenance, timestamps, ownership, and explicit semantic class.

## Observation envelope

Required fields:

- `schema_version`
- `observation_id`
- `source_system`
- `source_record_id`
- `observed_at`
- `ingested_at`
- `entity_refs[]`
- `case_refs[]`
- `event_type`
- `payload`
- `evidence_refs[]`
- `security_classification`
- `correlation_id`

## PatternSignal envelope

Required fields:

- `schema_version`
- `signal_id`
- `detector_id`
- `detector_version`
- `pattern_class`
- `summary`
- `scope`
- `window_start`
- `window_end`
- `supporting_observation_ids[]`
- `counterevidence_ids[]`
- `confidence`
- `severity`
- `explanation`
- `governance_refs[]`
- `recommended_routes[]`
- `requires_verification`
- `created_at`

## ExecutiveDisposition envelope

JANUS/ODIN returns one of: `accepted`, `rejected`, `deferred`, `request_evidence`, `route_for_verification`, `route_for_execution`, or `no_action`, together with rationale and routing references.

## VerificationFeedback envelope

SECA/DevOS/ProofGrid may return verification status, receipt references, outcome class, observed effect, and whether the original signal was supported, contradicted, or unresolved.

## Contract invariant

A NAVI signal without evidence references, confidence, detector version, and time window is invalid and must not enter the executive path.