# Medusa <-> NAVI Contract

## Medusa -> NAVI

Provides security classification, public/private boundary rules, access constraints, redaction requirements, and policy decisions relevant to the observations NAVI is permitted to process or emit.

## NAVI -> Medusa

NAVI may emit security-relevant pattern observations, repeated access anomalies, governance drift affecting security, suspected leakage patterns, or requests for classification review.

## Boundary

Medusa owns security policy. NAVI cannot downgrade classification, widen access, bypass redaction, or treat availability of data as permission to correlate it.

## Required behavior

- preserve classification end to end
- minimize sensitive data in explanations
- avoid cross-case correlation where policy forbids it
- quarantine payloads with ambiguous authorization
- route security-relevant escalations through the governed path
- retain evidence references without copying secrets into analytical prose where not required

## Safe failure

Unknown classification or authorization state results in reduced capability or blocked processing, never implicit permission.