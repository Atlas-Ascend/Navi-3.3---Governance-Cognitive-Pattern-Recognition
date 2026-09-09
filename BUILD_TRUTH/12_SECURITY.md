# 12 — Security

## Security posture

NAVI is a high-context analytical subsystem and therefore must be treated as a privileged observer with constrained authority.

## Controls

- authenticate every source and downstream consumer
- authorize access by source, data class, purpose, and operation
- preserve Medusa security classifications end to end
- reject payloads that exceed the receiving contract or declared scope
- redact or tokenize secrets before analytical processing where possible
- never log credentials, tokens, private keys, or raw secrets
- isolate model-assisted analysis from direct privileged execution
- validate all structured model output before routing
- enforce allowlisted destinations and message types
- keep detector/configuration changes versioned and auditable
- quarantine malformed, suspicious, or policy-conflicting events
- make replay behavior explicit to prevent duplicate escalation

## Threats considered

- prompt or data injection through observation payloads
- poisoned evidence intended to manipulate pattern detection
- forged provenance
- unauthorized cross-case correlation
- sensitive-data leakage in explanations
- detector/configuration tampering
- privilege escalation through recommendation channels
- replay storms or duplicate events
- fabricated proof references

## Security boundary

NAVI may identify a security-relevant pattern and request review. Medusa owns security policy and classification decisions. NAVI cannot weaken or bypass Medusa controls.

## Safe failure

When authorization, provenance, or classification cannot be established, NAVI must reject, quarantine, or lower capability. It must not infer permission from availability.