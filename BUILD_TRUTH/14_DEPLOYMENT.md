# 14 — Deployment

## Deployment objective

NAVI 3.3 must run as a resident service without changing its contracts or governance depending on placement.

## Supported placement

- local EDEN/Hypernet node for private/local analysis
- Render background worker or private service for resident cloud execution
- containerized development/test runtime
- hybrid mode with CrownGrid routing between local and remote components

## Runtime topology

Recommended production topology:

`event sources -> CrownGrid/ingress -> NAVI worker -> state store/cache -> JANUS/ODIN route -> verification/execution systems`

NAVI should expose health, readiness, detector-registry version, contract version, queue depth, last successful ingestion, last emitted signal, and calibration metrics.

## Configuration

Configuration is environment-specific but schema-controlled. Secrets stay outside the repository. Detector enablement, thresholds, transport endpoints, persistence, and logging are explicit configuration surfaces.

## Release path

1. build and static checks
2. unit/contract/governance tests
3. integration fixture tests
4. evaluation suite
5. SECA/DevOS inspection
6. candidate artifact creation
7. controlled deployment
8. smoke/health verification
9. ProofGrid receipt for promoted release
10. Thoth registration of release state

## Rollback

Every deployment must be version-addressable and rollback-capable. A bad detector may be disabled independently of the entire service where possible.

## Promotion invariant

Deployment success is not equivalent to functional proof. Runtime health, contract checks, governed behavior, and verification evidence are all required before NAVI is considered resident-production ready.