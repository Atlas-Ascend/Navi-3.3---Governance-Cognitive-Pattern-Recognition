# 11 — Governance

## Governance objective

NAVI 3.3 must improve recognition without collapsing the estate's separation of powers.

## Authority model

NAVI is analytical/advisory. JANUS/ODIN remain executive/governance authorities. Packet OS and Workforce Spine coordinate work. MetaForge builds. SECA/DevOS verify. ProofGrid records proof. Medusa enforces security/public-private policy. Thoth preserves memory.

## Mandatory controls

1. **No self-promotion:** NAVI cannot convert a recommendation into authorized work by itself.
2. **No proof substitution:** confidence and explanation are not verification receipts.
3. **No silent policy mutation:** detector thresholds and governance rules require explicit versioned change.
4. **No destructive autonomy:** deletion, destructive infrastructure actions, unrestricted shell, and privilege escalation are denied.
5. **Human/executive override:** authorized governance may reject or quarantine any signal.
6. **Conflict disclosure:** contradictory evidence must be surfaced rather than averaged away.
7. **Auditability:** material detector runs and promoted signals must be reproducible from retained inputs/configuration.
8. **Least privilege:** connectors receive only the permissions necessary for observation and approved outputs.

## Escalation classes

- `informational` — useful pattern, no immediate decision needed
- `attention` — executive review recommended
- `verification_required` — evidence insufficient for decision
- `governance_conflict` — policy or authority conflict requiring ODIN/JANUS
- `security_review` — Medusa involvement required
- `critical` — severe recurring pattern requiring immediate executive attention, but still not autonomous execution

## Governance invariant

Increasing confidence increases the quality of a recommendation; it never increases NAVI's authority.