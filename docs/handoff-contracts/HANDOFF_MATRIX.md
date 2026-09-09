# NAVI 3.3 Estate Handoff Matrix

| Producer | Consumer | Artifact | NAVI authority | Required response | Failure route |
|---|---|---|---|---|---|
| Thoth | NAVI | memory/context envelope | read/analyze | correlation acknowledgement | lower confidence / request context |
| CaseGraph | NAVI | graph/state envelope | read/analyze | graph-context acknowledgement | contradiction/evidence request |
| Packet OS | NAVI | work-state observation | read/analyze | pattern signal if warranted | audit + retry/quarantine |
| Workforce Spine | NAVI | routing/execution telemetry | read/analyze | bottleneck/handoff signal | JANUS attention route |
| SECA | NAVI | audit/inspection outcome | ingest feedback | calibration update | unresolved verification state |
| DevOS | NAVI | technical verification/diagnostic | ingest feedback | calibration + technical pattern | JANUS/MetaForge route only if authorized |
| ProofGrid | NAVI | proof receipt/outcome evidence | ingest proof refs | close feedback loop | preserve unverified state |
| Medusa | NAVI | security classification/policy | enforce | constrained analysis/routing | security review |
| CrownGrid | NAVI | routed message envelope | consume permitted transport | acknowledgement | dead-letter/retry |
| NAVI | JANUS PRIME | PatternSignal / executive brief | recommend only | disposition | ODIN escalation where applicable |
| NAVI | ODIN | governance/risk pattern | advise only | governance disposition | halt promotion |
| NAVI | SECA | verification request | request only | verification result | unresolved signal |
| NAVI | DevOS | technical validation request | request only | diagnostic/verification result | unresolved signal |
| JANUS/ODIN | Packet OS | authorized work packet derived from signal | none after handoff | work lifecycle | normal Packet OS governance |
| Packet OS | Workforce Spine | executable governed task | none | execution state | routing/retry controls |
| Workforce Spine | MetaForge | authorized build/remediation task | none | build artifacts | DevOS/SECA inspection |
| ProofGrid | Thoth | accepted proof reference | none | durable memory registration | proof-state exception |
| Thoth | NAVI | verified historical outcome | read/analyze | future calibration | lower confidence if missing |

## Universal handoff envelope

Each integration should transport at minimum:

- `contract_version`
- `message_id`
- `correlation_id`
- `producer`
- `consumer`
- `artifact_type`
- `created_at`
- `security_classification`
- `authority_context`
- `payload_ref` or payload
- `evidence_refs[]`
- `ack_required`
- `idempotency_key`

## Handoff law

NAVI never hides authority transitions. The point where a PatternSignal becomes governed work must be visible as a new artifact authored/authorized by the executive layer.