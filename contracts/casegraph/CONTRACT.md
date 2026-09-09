# Universal CaseGraph <-> NAVI Contract

## CaseGraph -> NAVI

Provides entity identifiers, relationship edges, case membership, state transitions, unresolved contradictions, provenance, and scoped graph snapshots.

## NAVI -> CaseGraph

May emit pattern annotations, contradiction annotations, recurrence clusters, and suggested investigative edges as separate governed analytical artifacts.

NAVI must not silently rewrite canonical graph relationships or convert inferred edges into asserted facts.

## Required fields

`contract_version`, `case_refs`, `entity_refs`, `edge_refs`, `state_transition_refs`, `snapshot_time`, `evidence_refs`, `security_classification`, `correlation_id`.

## Boundary

CaseGraph owns canonical relationship/state representation. NAVI recognizes higher-order structure over that representation and returns annotations with confidence and provenance.