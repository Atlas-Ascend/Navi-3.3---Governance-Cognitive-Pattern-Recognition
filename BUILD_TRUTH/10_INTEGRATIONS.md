# 10 — Integrations

## Integration doctrine

NAVI integrates through explicit, versioned contracts. It does not reach into another system's internal state and silently reinterpret ownership.

## Estate integrations

- **Thoth:** temporal memory, historical context, durable pattern summaries, calibration history.
- **Universal CaseGraph:** entity relationships, state transitions, unresolved contradictions, case scope.
- **JANUS PRIME:** primary executive consumer of pattern intelligence and routing recommendations.
- **ODIN:** governance/risk interpretation, supervisory escalation, policy conflict handling.
- **Packet OS:** work-state observations and downstream governed execution packets.
- **Workforce Spine:** task routing, handoff telemetry, throughput/failure recurrence.
- **MetaForge:** build/remediation target after executive authorization.
- **SECA:** audit, inspection, claim verification, quality-control feedback.
- **DevOS:** technical diagnosis, software verification, reproducibility, implementation feedback.
- **Medusa:** security classification, access policy, public/private boundary constraints.
- **CrownGrid:** transport/routing boundary for cross-estate messages.
- **ProofGrid:** proof receipts and outcome evidence.
- **VISHVARUPA:** organism-level orchestration context and resident-state topology.

## Integration requirements

Every adapter SHALL define: contract version, producer/consumer identity, authentication/authorization assumptions, idempotency key, retry semantics, timeout behavior, audit behavior, security classification, and degradation mode.

## Degradation rule

A failed integration must reduce capability, not governance. Missing context lowers confidence or blocks promotion; it never authorizes NAVI to invent absent evidence.