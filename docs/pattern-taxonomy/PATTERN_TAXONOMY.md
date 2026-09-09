# NAVI 3.3 Pattern Taxonomy

NAVI classifies patterns by semantic class so consumers can reason about what kind of claim is being made.

## Core pattern classes

### Recurrence
A materially similar event, state transition, failure mode, decision, behavior, or outcome repeats across a defined window.

### Sequence motif
A recurring ordered chain of events, e.g. `intake -> ambiguity -> reroute -> delay -> retry`.

### Escalation
Severity, frequency, cost, latency, conflict, or risk rises over successive observations.

### Decay
A previously strong signal or capability degrades over time.

### Oscillation
State repeatedly flips between alternatives without durable resolution.

### Stagnation
Expected progress fails to occur across a meaningful window.

### Anomaly
An observation or cluster deviates materially from a documented baseline.

### Contradiction
Sources, states, claims, proofs, or policies conflict in a way that cannot be reconciled automatically.

### Governance drift
Observed behavior or implementation progressively diverges from canonical policy, authority, or contract.

### Handoff failure
A producer emits expected work/context but acknowledgement, ownership, execution, or closure repeatedly breaks downstream.

### Bottleneck
A node, agent, repository, queue, approval surface, or dependency accumulates disproportionate waiting or failure.

### Convergence
Independent sources or subsystems produce mutually supporting signals that increase confidence in a shared interpretation.

### Fragmentation
Multiple competing representations of the same system, concept, workstream, or source of truth diverge without explicit lineage/governance.

### Opportunity pattern
A repeated combination of conditions is correlated with positive outcomes and may justify executive exploration.

### Proof gap
A material claim, completion state, or deployment lacks required verification or ProofGrid evidence.

### Recovery pattern
A repeated intervention is followed by verified restoration of a degraded state.

## Pattern metadata

Every pattern class supports: severity, confidence, scope, time window, entity/case refs, supporting observations, counterevidence, detector version, policy refs, recommended routes, and verification requirement.

## Claim discipline

Pattern classes describe structure in evidence. Causal claims require stronger evidence than recurrence, correlation, or convergence and must be explicitly labeled as causal hypotheses until verified.