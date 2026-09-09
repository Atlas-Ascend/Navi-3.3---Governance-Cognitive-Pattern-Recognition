# ProofGrid <-> NAVI Contract

## ProofGrid -> NAVI

Provides proof receipts and verification-linked outcome evidence that can be associated with prior NAVI signals, executive dispositions, work packets, builds, deployments, and audits.

## NAVI -> ProofGrid

NAVI may submit references to analytical claims and their evidence chain for downstream proof workflows, but cannot mint, approve, or upgrade a ProofGrid receipt.

## Required feedback

Where a ProofGrid receipt closes a NAVI-originated loop, NAVI should receive:

- original `signal_id`
- executive disposition reference
- execution/work references
- verification artifact references
- receipt ID
- proof status
- outcome timestamp
- supported/contradicted/unresolved classification

## Boundary

ProofGrid owns proof-class state. NAVI owns recognition and confidence. A 0.99 NAVI confidence score remains an analytical claim until external verification and proof policy say otherwise.

## Calibration use

NAVI may use proof outcomes to estimate detector precision, recurring success/failure patterns, and confidence calibration. Receipt contents remain immutable references from NAVI's perspective.