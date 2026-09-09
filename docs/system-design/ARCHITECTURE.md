# NAVI 3.3 Software Design

## Purpose

This document translates the Build Truth into an implementable resident service.

## Service boundaries

NAVI owns analytical state only: normalized observations, detector state, correlation windows, signal history, confidence calibration, and disposition/verification feedback. Source systems retain ownership of canonical domain state.

## Modules

### `ingestion`
Adapters receive versioned events and map them into `Observation`. Invalid payloads are rejected before entering analysis.

### `normalization`
Canonicalizes timestamps, source IDs, entity refs, case refs, evidence refs, classifications, and correlation IDs.

### `context`
Requests authorized context from Thoth and CaseGraph and never silently persists external canonical records as NAVI-owned truth.

### `features`
Computes detector-independent features: recurrence intervals, transition counts, disagreement ratios, retry/error rates, graph degrees, latency windows, and change rates.

### `detectors`
Plugin registry. Each detector declares `id`, `version`, accepted pattern class, required features, minimum evidence, scoring method, explainability method, and test/eval suite.

Initial detector families:

- recurrence / repeated motif
- temporal escalation / decay
- anomaly / baseline deviation
- contradiction / cross-source disagreement
- governance drift
- workflow handoff failure
- bottleneck / queue concentration
- convergence / correlated independent signals
- opportunity / repeated positive outcome pattern

### `governance`
Evaluates signal class, policy refs, required executive route, verification requirement, security review requirement, and denied actions.

### `confidence`
Produces a structured confidence object rather than a single magical scalar. Inputs include evidence quantity, source diversity, source reliability, detector calibration, temporal support, counterevidence, and model uncertainty.

### `explainability`
Produces a minimal causal-looking narrative only when causality is actually supported; otherwise uses correlation language. Every explanation includes evidence refs and limitations.

### `routing`
Outputs only approved envelopes to JANUS/ODIN, SECA/DevOS evidence requests, and Thoth feedback storage.

### `feedback`
Joins later disposition and verification data to original signals and updates detector metrics without allowing self-modifying production policy.

## Suggested runtime interfaces

```text
POST /v1/observations
GET  /v1/signals/{signal_id}
GET  /v1/patterns?entity=&case=&class=&from=&to=
POST /v1/dispositions
POST /v1/verification-feedback
GET  /health
GET  /ready
GET  /metrics
```

Equivalent event-bus messages may replace HTTP without changing semantic contracts.

## Storage

Minimum logical stores:

- observation index
- correlation/pattern state
- detector registry/config
- emitted signal ledger
- disposition ledger
- verification-feedback ledger
- calibration metrics

Use durable identifiers and append-oriented audit records. Cache is disposable; evidence linkage is not.

## Resident execution

NAVI should be able to run as a long-lived worker. Sources enqueue observations; worker batches or streams windows; detectors evaluate; outputs are emitted asynchronously. Critical executive alerts may use priority lanes but remain advisory.

## Model-assisted analysis

LLMs or statistical models may classify, cluster, summarize, or propose hypotheses, but structured outputs must pass schema validation and governance. A model cannot grant itself tools, authority, proof status, or bypass deterministic policy checks.

## Observability

Emit metrics for ingestion rate, reject rate, detector latency, signal count by class/severity, duplicate suppression, executive disposition rate, verification support rate, false positives, unresolved contradictions, queue depth, and adapter health.

## Evolution

NAVI evolves by adding versioned detectors and adapters, not by turning the core service into an unconstrained monolith. Every detector promotion must include fixtures, tests, eval results, and rollback metadata.