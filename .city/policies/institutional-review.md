# Institutional review and continuous improvement

**Adoption status:** The governing status of this exact revision is recorded in `.city/config.json`. Check `city status` and `city validate` before relying on it. Initialization alone does not adopt a revision or grant authority. The adoption record is a resident declaration and is not authenticated. Initialization alone does not appoint the Performance and Innovation Officer or authorize any change.

## Purpose and authority

The Performance and Innovation Officer identifies structural and procedural gaps by reviewing the city's own records and comparing relevant practices with real municipal institutions. The Officer makes recommendations only. The City Manager coordinates approved administrative follow-up; the City Council decides work orders only within adopted delegation; residents decide reserved matters, including governance, policy adoption, and changes to the office roster.

The review is not an audit, an appointment, a policy amendment, or delivery authorization. At the start of every city-coordination run, the City Manager dispatches the Officer to check `status`; the Officer conducts the review in the same run whenever `institutionalReview.available` and `institutionalReview.due` are true. The CLI has no scheduler: a review becomes visible during city activity, not while the plugin is inactive.

## Trigger thresholds

`status` reads these values from this adopted policy. Residents may petition to amend the thresholds; the changed policy takes effect only after a resident records the amendment with `amend`. The CLI accepts only positive whole-number thresholds and requires every trigger to appear exactly once.

| Trigger | Threshold | Unit |
|---|---:|---|
| periodic-volume | 10 | completed work orders |
| periodic-time | 90 | elapsed days |
| returned-or-rejected | 3 | council returns or rejections |
| inspection-failures | 3 | inspection returns to in-progress |
| referrals | 3 | council referrals |
| blocked | 3 | work orders entering blocked |

The review window starts at the last review's `coversThrough` timestamp, or at the current governance adoption's `recordedAt` timestamp when no review exists. Signals are counted only within that window. Trigger conditions are cumulative and do not expire independently.

## Evidence and recommendations

The Officer states the review window, trigger observations, records examined, scope limitations, and gaps in available data. For external comparisons, cite identifiable sources (prefer official municipal sources and primary documents); distinguish verified source material from general knowledge and uncertain analogy. Do not invent citations or assume that a practice fits every repository.

Each recommendation states the gap, evidence, applicability and uncertainty, cited precedent, likely impacts, and a route:

- `administrative`: an operational adjustment within existing adopted authority, sent to the City Manager.
- `council`: a bounded work proposal for City Council review under the adopted council-delegation policy.
- `resident`: a reserved decision, such as a charter or policy change, office appointment, expanded authority, or resource limit; refer it to the Clerk for resident consideration.

Any recommendation listing reserved matters must use the `resident` route. The Officer cannot edit governance, appoint offices, create authority, commit resources, or implement recommendations. A recorded review is evidence that a review was reported, not proof of the actor's identity or of external source accuracy.

## Unavailable signals

The current CLI does not maintain canonical records for all complaints, appeals, or audit findings as independent institutional-review signals. Staff requisitions are recorded but are tied to work orders and do not, by themselves, prove that an office is missing. Staff may refer these matters to the City Manager for consideration, but the Officer must not claim they are automatically counted.
