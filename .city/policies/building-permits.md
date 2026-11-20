# Building permits

**Adoption status:** The governing status of this exact revision is recorded in `.city/config.json`. Check `city status` and `city validate` before relying on it. Initialization alone does not adopt a revision or grant authority. The adoption record is a resident declaration and is not authenticated. This policy does not appoint qualified staff or grant tool permissions. It requires the development-applications, council-delegation, and workforce-delegation policies to be current as well.

## Purpose and municipal adaptation

This policy adapts Copenhagen's risk-proportionate building-case process to
repository delivery. It is not a statement of Danish law. The city baseline and
local project refinements are repository policies; `authorize` is the recorded
permit decision. A permit is neither authenticated identity nor a host-enforced
security boundary.

The Chief Planner assigns separate safety and structural classes from 1 to 4
and records the evidence and rationale in the current screening. Safety covers
security, permissions, secrets, and data integrity. Structural class covers
architecture, public interfaces, ownership boundaries, migrations, and the
blast radius of cross-project change.

| Class | Proportionate evidence and review |
|---|---|
| 1 | Contained and readily reversible. Lightweight screening is available. |
| 2 | Bounded material effects. Formal application when required by the development baseline. |
| 3 | Significant safety or structural effect. Formal application and a matching qualified professional statement for each class-3 dimension. |
| 4 | Highest repository risk or broad blast radius. Formal application, a matching qualified statement, independent verification by a different qualified staff member, and a resident authorization decision. |

Lightweight screening is limited to classes 1 and 2. A security impact is at
least safety class 2. Architecture, ownership-boundary, public-interface,
data-migration, and cross-project impacts are at least structural class 2.
These floors are minimums, not an automatic classification engine. A higher
class requires an evidence-based rationale. The CLI validates the declared
shape and floors, not the truth or professional adequacy of the classification.

## Qualified statements and independent verification

For each dimension classified 3 or 4, the Engineering Manager arranges an
active engineer whose filled requisition records the corresponding competency:
`permit-safety-class-3`, `permit-safety-class-4`,
`permit-structural-class-3`, or `permit-structural-class-4`.
The Manager records the statement and its scope/evidence with
`permit-statement`. A class-4 statement also needs `permit-verification` from
another active qualified staff member. The author cannot verify their own
statement; the assigned engineer cannot verify their own delivery.

These are local competency attestations, not Danish professional
certifications. All records remain `authenticated: false`. If no qualified
staff member exists, pause. For an outstanding class-3 safety statement before
delivery authorization, the Manager may seek the limited, HR-reviewed
pre-authorization appointment under `workforce-delegation.md`; this does not
authorize implementation, expenditure, or delivery. For any other staffing
need, seek a resident decision. Do not lower the class to avoid the requirement.

## Permit decision, scope, and terms

The adopted development policy must establish readiness before a work order
enters `awaiting-approval`. The City Council may authorize classes 1–3 under
its adopted delegation. A class-4 authorization is reserved to the resident.
The decision records class values from the current screening, permit conditions,
the affected-project consents when work crosses a project boundary, a
commencement deadline 30 days after issuance, and a 30-day inactivity limit.
Conditions have unique IDs and must state verifiable evidence.

The resident should amend this policy before changing these default periods.
The runtime checks lapse when `status` runs or when a lifecycle transition is
requested; it has no background scheduler. A lapsed permit cannot resume
delivery. The Council may grant at most two extensions of up to 30 days each
for classes 1–3; the resident decides class-4 extensions. Record the reason
with `permit-extend`. If the permit cannot be extended or the risk classification
has changed, return the case for fresh screening and authorization. Old decisions
are preserved and not retroactively changed.

Cross-project or ownership-boundary impacts require recorded consent in the
permit terms from each affected project outside the work-order scope. Project
records do not identify project stewards, so the decision must state who gave
consent and cite the evidence. Infrastructure-asset ownership consent must be
recorded in the permit decision evidence until a structured asset-consent
record is implemented.

## Completion, inspection, and acceptance

Before entering `inspection`, the Engineering Manager records a completion
notice for the active permit. It must identify every permit condition exactly
once, with evidence that it is met or a reasoned not-applicable disposition.
The Building Inspector independently checks the notice, the approved scope,
and the work. Failed inspection returns work to `in-progress`; a new completion
notice is required before the next inspection.

Only the resident accepts the inspected work through `complete`. This is the
Repository City analogue to completion notification and taking the work into
use; it does not claim that a real municipality issued an occupancy permit.

## Exceptions, unpermitted work, and appeals

There is no permit-free schedule in this policy. The existing routine classes
remain authorized delivery classes: they simplify Council deliberation but do
not bypass a recorded authorization, inspection, or resident acceptance.

Policy exceptions remain governed by
`authority-and-policy.md`: they require a policy-permitted, genuinely
authorized decision, rationale, scope, risk, expiry, and review. An exception
cannot waive this policy's class requirements, the charter, reserved matters,
or external obligations. This release does not automate neighbour consultation,
dispensation records, retroactive legalization, or remediation orders; the
Auditor must refer suspected unpermitted delivery to the resident and preserve
the finding through the existing records process. Do not describe an
unrecorded change as legalized.

Appeals use the existing independent appeal procedure. The City Auditor reviews
whether the process followed adopted rules; the resident retains the merits
decision. No office may inspect, authorize, and independently audit its own
work.

## Records and limits

Screenings, statements, verifications, completion notices, permit terms, and
decisions are appended to canonical work-order or decision records. Existing
orders without permits remain valid; this policy applies only to new
authorizations after adoption. Writes use the existing local mutation locks,
atomic replacement, conflict checks, and record-size limits.

The CLI validates record structure, references, current revisions, competency
labels, and separation of duties. It does not authenticate people, observe
actual work, schedule expiry jobs, enforce filesystem boundaries, or run Git,
merge, push, deployment, fines, or other external enforcement.
