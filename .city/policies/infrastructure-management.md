# Infrastructure stewardship

**Adoption status:** The governing status of this exact revision is recorded in `.city/config.json`. Check `city status` and `city validate` before relying on it. Initialization alone does not adopt a revision or grant authority. The adoption record is a resident declaration and is not authenticated. Initialization does not adopt this policy,
appoint operators, promise service levels, allocate resources, or authorize work.
The resident must adopt this exact revision before it governs. City records and
decisions remain local, unauthenticated evidence.

## Purpose and scope

Infrastructure is the durable shared technical foundation on which repository
services depend: for example, build and test systems, common libraries, release
configuration, data foundations, development tools, and documented external
services. Register an asset when a named owner, custodian, operator, service,
condition, dependencies, and continuing obligations improve accountability.
Do not treat every file or dependency as an asset. An external dependency's
registration grants no ownership or authority over its operator.

An asset record describes stewardship; it is not itself a work order, budget,
service guarantee, security finding verification, or authorization. The resident
retains authority over reserved matters, including security. The plugin performs
no monitoring, scanner execution, external notice, maintenance, merge, or deploy.
`status` only evaluates recorded evidence when invoked.

## Responsibilities and separation

| Function | Responsible office or decision-maker |
|---|---|
| Coordinate service expectations, operator coverage, escalation, and portfolio follow-up | City Manager |
| Maintain asset register and service/condition/obligation evidence with custodians | City Manager coordinates; competent technical custodians supply evidence |
| Assess design, compatibility, maintenance and upgrade options, estimates, and recovery | Engineering Manager and assigned competent engineers |
| Maintain a rolling horizon, compare cross-asset/project needs, capacity, and unfunded work | Chief Planner, coordinated by City Manager |
| Authorize reserved security, material scope, and other reserved decisions | Resident; Council refers reserved matters |
| Independently inspect authorized delivery | Building Inspector |
| Accept completed change and pull request | Resident |
| Preserve, index, and disclose records under applicable retention/privacy rules | City Clerk and Records Officer |
| Independently audit controls and reported outcomes | City Auditor |

No office may grant itself authority. Follow adopted [council delegation](council-delegation.md),
[resources and workforce](resources-and-workforce.md), [service catalogue](service-catalogue.md),
[records and privacy](records-and-privacy.md), and [continuity and accountability](continuity-and-accountability.md).

## Stewardship cycle

1. Register only evidenced facts. Identify the service and its expected outcome,
   accountable owner, custodian, actual operator and coverage, repository-relative
   locators, consumers, dependencies, criticality, condition, supported baseline,
   maintenance obligations, risks, renewal needs, and resilience arrangements.
   Record unknowns rather than infer guarantees.
2. Review on the recorded cadence and when an evidenced incident, support deadline,
   failed check, compatibility change, material service measurement, or resident
   report warrants it. Record source, date, method, and uncertainty. The CLI does
   not schedule reviews or check external systems.
3. Use one service backlog. Create a bounded, exact-scope petition for work; do
   not turn a due date, programme entry, finding, staff assignment, or status
   warning into authorization. Pin asset revisions and locators, enumerate exact
   local targets, and cite only current maintenance occurrences and open findings.
4. Route security findings to the resident even for a routine patch. Council may
   refer but cannot authorize that security matter. Preserve advisory evidence,
   applicability, affected baseline, urgency, risk owner, and disposition. Do not
   run scanners, retrieve advisories, or expose secrets through intake.
5. Before authorization and delivery, confirm asset lifecycle, locator, baseline,
   criticality, exact target paths, current screening, adopted policy, and
   independent acceptance criteria. Scope drift requires reassessment and a new
   decision. Existing authorization never expands when an asset is revised.
6. Plan upgrades against supported baselines, compatibility, service outcomes,
   operational capacity, life-cycle resource estimates, rollback/recovery, and
   affected users. A newer version alone is not a reason to upgrade.
7. Record inspection and resident acceptance before satisfying a linked
   maintenance obligation or resolving an applicable finding. For recurring
   work, calculate the next due date from the obligation's documented recurrence;
   failed, uninspected, or unrelated work does not reset it.
8. For deferrals, preserve original due date, reason, accountable risk owner,
   authority reference where applicable, and a definite review date. Surface
   unfunded needs and consequences; never delete an inconvenient backlog item.
9. Keep an explicitly reviewed rolling programme with a repository-appropriate
   horizon, condition and demand basis, sequenced alternatives, resource estimates,
   authority status, and unfunded needs. Estimates are not appropriations. A
   programme review due date triggers human review only when an operator checks
   status.
10. For material disruption or service changes, obtain affected-user input,
    document disposition, and record actual communication evidence. Consultation
    is not approval; a proposed message is not a sent notice. Do not impose a hearing
    on ordinary non-disruptive maintenance.
11. Record failure modes, restoration dependencies, recovery order, exercise
    evidence, and corrective actions. A list of individually healthy assets is
    not proof of system-wide resilience.
12. Deprecate or retire only through documented dependency resolution, continuity
    and records review, and appropriate authority. Preserve the register and
    history; repository metadata never deletes assets or cancels external services.

## Review and limitations

At city coordination, the Manager should examine `status.infrastructure`,
dispatch needed professional assessments, and surface overdue obligations,
stale measurements, coverage gaps, support deadlines, unresolved findings,
deferrals, and programme reviews. Separate observed facts from estimates and
recommendations. Escalate missing authority, expertise, capacity, operator
coverage, privacy safeguards, or recovery evidence to the resident. No automated
work is implied while the plugin is inactive.
