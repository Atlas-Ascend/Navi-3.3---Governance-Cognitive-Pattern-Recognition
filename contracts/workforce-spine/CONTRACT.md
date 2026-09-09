# Workforce Spine <-> NAVI Contract

## Workforce Spine -> NAVI

Provides routing and execution telemetry: task acceptance, ownership changes, handoff latency, queue depth, retries, abandonment, completion claims, blocked dependencies, and worker/role availability.

## NAVI -> Workforce Spine

NAVI does not assign work directly. It emits executive-facing findings such as bottleneck, repeated handoff failure, ownership ambiguity, routing churn, or capacity imbalance. JANUS/ODIN decides whether those findings become work-routing changes.

## Pattern classes supported

- bottleneck
- handoff failure
- repeated reassignment
- queue concentration
- starvation
- routing oscillation
- recurrent dependency block
- capacity mismatch

## Boundary

Workforce Spine owns task routing and execution state. NAVI may diagnose routing structure but cannot seize tasks, change ownership, or modify execution policy without an authorized downstream artifact.