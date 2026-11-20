# Repository zoning

**Initialization status: Not adopted.** Initialization does not adopt this policy,
the zoning map, or any zone rule. The resident must adopt this policy revision.
To opt in before first adoption, copy this draft to
`.city/policies/zoning.md`. For an existing city, copy it there and amend the
charter and policy register.
The [development applications policy](../policies/development-applications.md)
must also be adopted to provide the conditional-review route. The map must be
explicitly recorded before zoning can assess a work order.

## Purpose and municipal adaptation

Zoning assigns permitted, conditional, and prohibited kinds of repository change
to repository-relative paths. It is separate from project delivery scope and
district ownership. A zone is not a team, permission boundary, or execution
sandbox. Repository paths are the limited equivalent of land-use geography;
change types and review requirements replace physical uses and development
standards. The adaptation and CLI contract are documented in
[`docs/zoning.md`](../../../../docs/zoning.md).

## Rules

- The Clerk maintains `.city/zoning.json` as the current local map. Zone paths
  must be normalized, repository-relative, outside `.city` and `.git`, and
  disjoint. A zone with no rule for a change type is **unknown**, never permitted.
- The Chief Planner proposes map changes and classifies change types against the
  exact work-order project directories and infrastructure targets. The Planner
  records reasons and evidence with `zoning-check`; the runtime validates record
  structure and declared scope, not the truth or completeness of that assessment.
- A `permitted` finding satisfies zoning only. It does not replace development
  screening, authorization, delivery inspection, or resident acceptance.
- A `conditional` finding requires a formal development application and an
  independent ready assessment. Its named requirements must be included in the
  application and reviewed by the Chief Planner.
- `prohibited` and `unknown` findings are not ready for authorization. Resolve
  the plan or scope, or propose a map amendment through the ordinary work-order,
  Council/resident decision, and Clerk recordkeeping process. There is no
  automatic variance or exemption in this policy.
- A change to the zoning map, work-order scope, or change-type classification
  makes the previous zoning finding stale. Reassess before the next authorization.
  Earlier authorizations are not retroactively invalidated.
- A map amendment is a policy decision, not a clerical self-approval. The
  `zoning-map` command records the map only; it does not verify the required
  decision or authenticate who applied it.

The zoning check covers declared project directory paths and exact registered
infrastructure targets. It does not inspect a Git diff, infer actual edits, or
enforce filesystem permissions. The independent Inspector must compare actual
changed paths and change types with the current adopted map and recorded
assessment.

## Separation of duties

The Chief Planner proposes and assesses; the City Council or resident makes
decisions within the adopted charter; the Clerk maintains records; the Building
Inspector independently inspects delivered changes; and the City Auditor may
review the policy's administration. No office may grant itself authority by
changing a zone or treating a local record as authenticated permission.
