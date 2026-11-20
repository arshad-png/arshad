# Hike SaaS Lab

The central research, validation, product strategy and decision repository.

Hike SaaS Lab holds the evidence and the decisions behind product ideas. It is not the production application repository. Each product that passes its decision gates gets its own separate implementation repository, created by a separate written decision.

## What belongs here

- Market research
- Customer evidence (interview notes, complaint logs, audit results)
- Validation plans and results
- Product hypotheses
- Go and no-go decisions
- Compliance and integration research
- Reusable product-development standards

## What does not belong here

- Application code
- Installed dependencies or build output
- Production configuration, credentials or exports from live accounts
- Customer or patient data. Interview notes use numbers, not business names, and never contain patient details

## Current contents

| Path | What it is | Status |
|---|---|---|
| `reports/Med spa SaaS opportunity research.md` | Research report, research date 2026-11-20 | Complete, kept intact |
| `research_notes/Med spa SaaS opportunity research/` | Source notes behind the report, five files | Complete, kept intact |
| `validation/VALIDATION-PLAN.md` | Validation execution plan | Draft, updated with Gate 0 answers |
| `validation/CUSTOMER-INTERVIEW-GUIDE.md` | Interview questions and logging rules | Draft |
| `validation/PILOT-OFFER.md` | Three packages and pilot terms | Draft, not for distribution |
| `validation/VALIDATION-SCORECARD.md` | Pass and fail criteria and trackers | Empty template |
| `validation/DECISION-GATES.md` | Gates 0 to 7 | Draft, Gate 0 not passed |
| `validation/GATE-0-DECISIONS.md` | Recorded Gate 0 answers and commercial decisions | Current |
| `validation/GATE-0-OPEN-ITEMS.md` | Open questions, ownership sheet, time and budget sheet | Current |
| `validation/GHL-VERIFICATION-CHECKLIST.md` | Read-only GoHighLevel account checklist | Prepared, not executed |
| `validation/COMPLIANCE-GATE.md` | US legal review blocker, questions for counsel, data inventory | Prepared, blocker open |

Active project: med spa lead-to-consult validation. Decision so far: no standalone SaaS development. Validation phase approved in principle, Gate 0 not yet passed.

## Status labels

| Label | Meaning |
|---|---|
| CONFIRMED | Stated by the decision owner or verified from a primary source |
| APPROVED IN PRINCIPLE | Direction agreed, final terms still to be settled |
| CONDITIONAL | Applies only once the listed conditions are met |
| DEFERRED | Decision postponed until the listed evidence exists |
| UNKNOWN | Not established. Never filled in with an assumption |
| BLOCKED | Cannot proceed until a named blocker is cleared |
| NOT AUTHORIZED | Must not be done under the current authorization |

Evidence labels used in research and plans: FACT, ESTIMATE, ASSUMPTION, RECOMMENDATION. See the label key in the research report.

## Current authorization boundary

As of 2026-11-20 the authorization covers documentation updates, analysis and preparation of decision materials. Nothing else.

NOT AUTHORIZED: customer outreach, vendor contact, mystery shopping, GoHighLevel account changes, paid services or purchases, legal commitments, live customer data processing, pilot launch, application development, pull requests and branch merges.

## Working rules for this repository

1. Research is preserved. Completed reports and notes are not edited. Corrections are documented separately and dated.
2. Every material claim carries an evidence label and a source or a stated basis.
3. Unknowns stay unknown until someone establishes them.
4. Thresholds are agreed before evidence arrives and changes are logged.
5. Evidence from existing agency relationships is recorded separately from evidence of independent demand.
6. No gate is passed on missing evidence.

Reusable product-development standards will be added here as they are agreed. None have been written yet.

## Repository name

The agreed name is Hike SaaS Lab. The GitHub repository is still named `arshad-png/arshad`. Renaming it is an account action for the repository owner and has not been done.
