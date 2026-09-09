# Packet OS <-> NAVI Contract

## Packet OS -> NAVI

Provides governed work-state observations including packet creation, assignment, queue state, dependency state, retries, timeouts, completion claims, closure, and exception events.

## NAVI -> Packet OS

NAVI does not author executable packets directly. It may emit a recommendation to JANUS/ODIN that can later be translated into a governed Packet OS artifact.

Where policy explicitly permits non-executable analytical packets, NAVI may submit an evidence-request or investigation recommendation tagged `advisory_only=true`.

## Pattern classes supported

- recurrence
- stagnation
- retry storm
- dependency deadlock
- queue bottleneck
- closure without proof
- repeated reassignment
- incomplete handoff

## Boundary

Packet OS owns atomic work state. NAVI observes and interprets packet behavior but cannot mark packets complete, cancel work, alter priority, or bypass packet governance.