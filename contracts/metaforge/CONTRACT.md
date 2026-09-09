# MetaForge <-> NAVI Contract

## MetaForge -> NAVI

Provides build/remediation telemetry: build request, implementation scope, artifact refs, commit/branch refs, test outcomes, failure classes, rework cycles, and deployment candidate state.

## NAVI -> MetaForge

NAVI may recommend remediation/build work only through JANUS/ODIN-authorized routing. It may also submit non-executable diagnostic context attached to an authorized task.

## Pattern classes supported

- recurring build failure
- rework loop
- dependency churn
- architecture drift
- repeated defect class
- fix-regression cycle
- successful recovery pattern

## Boundary

MetaForge owns build production. NAVI recognizes repeated development structure but cannot change source code, merge, deploy, or self-approve remediation.