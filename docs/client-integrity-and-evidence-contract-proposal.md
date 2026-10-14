# Client Integrity and Evidence Contracts — SDK Proposal

**Status:** Proposed; not approved or implemented.
**Canonical proposal:** https://github.com/KyleAlexanderSteen/GAIA-Documentation/blob/docs/alignment-attunement-self-improvement/GAIA-Documentation/GAIA-Universal-Principles-Integrity-Knowledge-and-Flourishing.md

## Candidate client behavior

- Preserve server-defined operation status and distinguish accepted, running, completed, failed, denied, and unknown results.
- Expose source/provenance and uncertainty fields when defined by approved contracts without silently dropping them.
- Treat client-side success (for example, request submission) as distinct from downstream operation success.
- Validate versioned schemas and surface unknown fields/statuses safely according to compatibility policy.
- Avoid embedding privileged credentials or Master-only routes in public client packages.
- Redact secrets from exceptions and telemetry; provide correlation IDs for support and evidence tracing.
- Document retry/idempotency semantics so clients do not duplicate consequential actions.

## Adoption gate

Do not invent final types before GAIA-Core contracts and service ownership are approved. Add compatibility, error handling, status-transition, provenance-preservation, redaction, and retry tests after approval. No SDK code is changed by this proposal.