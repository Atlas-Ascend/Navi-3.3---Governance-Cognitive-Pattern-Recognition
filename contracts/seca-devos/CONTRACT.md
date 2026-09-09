# SECA / DevOS <-> NAVI Contract

## NAVI -> SECA

Requests audit, inspection, falsification, policy-conformance checks, or claim verification for signals that require external validation.

## NAVI -> DevOS

Requests technical diagnosis, reproducibility checks, implementation verification, software-health inspection, or build/runtime investigation.

## SECA / DevOS -> NAVI

Return structured verification feedback containing request ID, result class, evidence refs, test/audit artifacts, limitations, confidence, and whether the original PatternSignal was supported, contradicted, partially supported, or unresolved.

## Boundary

NAVI may request verification but cannot dictate its result. SECA/DevOS verification outcomes remain distinguishable from NAVI confidence and explanation.

## Feedback use

NAVI may use verification outcomes to calibrate detectors, rank recurring defect classes, identify repeated verification failures, and improve executive signal quality. Calibration changes to production thresholds remain governed/versioned changes.