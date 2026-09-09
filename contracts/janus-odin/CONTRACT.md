# JANUS / ODIN <-> NAVI Contract

## NAVI -> JANUS PRIME

Primary output: `PatternSignal` plus executive brief containing pattern class, severity, confidence, evidence chain, counterevidence, time window, governance refs, and recommended routes.

NAVI may recommend: no action, observe, request evidence, verify, investigate, create governed work, or escalate. Recommendation never equals authorization.

## JANUS PRIME -> NAVI

Returns `ExecutiveDisposition`: accepted, rejected, deferred, request_evidence, route_for_verification, route_for_execution, or no_action, with rationale and resulting packet/route refs.

## NAVI -> ODIN

Escalates governance conflicts, policy drift, authority ambiguity, repeated denied-action attempts, or high-severity patterns requiring supervisory judgment.

## ODIN -> NAVI

Returns governance disposition, applicable policy references, and whether promotion is allowed, blocked, constrained, or requires Medusa/security review.

## Boundary

JANUS/ODIN own executive/governance decisions. NAVI cannot approve its own recommendation, alter the returned disposition, or route around a rejected decision.