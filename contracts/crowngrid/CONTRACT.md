# CrownGrid <-> NAVI Contract

## CrownGrid -> NAVI

Provides transport/routing envelopes for authorized cross-estate events and carries source identity, destination, correlation ID, message class, security classification, idempotency key, and retry metadata.

## NAVI -> CrownGrid

Publishes approved PatternSignal, evidence-request, disposition-feedback, and audit-oriented envelopes only to allowlisted destinations.

## Transport requirements

- message identity and idempotency
- delivery acknowledgement where required
- bounded retries
- dead-letter handling
- schema/version declaration
- producer/consumer identity
- security classification preservation
- correlation/causation references
- replay detection

## Boundary

CrownGrid owns estate routing; NAVI owns analytical semantics. NAVI cannot use CrownGrid to bypass JANUS/ODIN or Medusa. Transport success does not imply governance approval.