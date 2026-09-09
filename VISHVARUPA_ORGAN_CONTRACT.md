# NAVI 3.3 — VISHVARUPA Organ Contract

Status: SEEDED
Organism: VISHVARUPA
Organ class: Governance-aware cognitive pattern-recognition organ

## Mission
NAVI 3.3 detects recurring cognitive, governance, workflow, and decision patterns across the estate and converts them into bounded signals that can improve routing, oversight, and operator awareness.

## Authority
May detect, classify, compare, score, and surface patterns. May not issue final executive commands, diagnose humans, or convert correlations into verified causal claims without supporting evidence.

## Inputs
- Packet OS histories
- governance decisions
- workflow and handoff telemetry
- Mind-As-OS cognitive models
- SECA findings
- MAAT/Thoth state

## Outputs
- pattern detections
- anomaly/risk signals
- governance recommendations
- trend summaries
- candidate policy improvements

## Handoffs
Upstream: Mind-As-OS, Packet-OS, MAAT/Thoth, Ghost Atlas HQ, Runtime Observatory
Downstream: Atlas-Mind-LLM, Janus-Odin, SECA, RHSIE-3.3, Ghost Atlas Research Institute

## Events
Consumes: decision.recorded, packet.closed, workflow.failed, proof.rejected, state.updated
Emits: navi.pattern_detected, navi.anomaly_detected, navi.governance_recommendation, navi.research_candidate

## Proof requirements
Every pattern signal identifies its source window, features, confidence, competing explanations, and whether the result is descriptive, predictive, or causal. Causal status requires independent evidence.

## Definition of integrated
NAVI can observe real estate events, surface a bounded pattern signal to Atlas Mind/JANUS, and feed resulting governance or research work back through Packet OS with preserved provenance.