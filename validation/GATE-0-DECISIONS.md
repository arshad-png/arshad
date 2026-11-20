# Gate 0 decisions

Recorded 2026-11-20. Repository: Hike SaaS Lab. Project: med spa lead-to-consult validation.

**Gate 0 status: NOT PASSED.** Some answers and decisions are recorded below. Several remain UNKNOWN (see GATE-0-OPEN-ITEMS.md). No downstream activity is authorized.

Status labels are defined in the repository README.

## 1. Answers recorded

Recorded exactly as given. Nothing has been filled in.

| Question | Answer given | Status | What is still not known |
|---|---|---|---|
| Does CCS currently have med spa clients? | Yes | CONFIRMED | How many, which booking platforms, which states, monthly inquiry volume |
| Which GoHighLevel plan is CCS on? | Other / not sure | UNKNOWN | Plan name, billing tier, features, LC Phone rates, HIPAA availability. See GHL-VERIFICATION-CHECKLIST.md |
| Who owns the interviews and the mystery-shop audit? | Not decided | UNKNOWN | Named person or people. See GATE-0-OPEN-ITEMS.md |
| Existing US lawyer for messaging and health-data compliance? | No | CONFIRMED (none exists) | Who will be engaged, cost, timing. This is a BLOCKED item for any live pilot. See COMPLIANCE-GATE.md |
| Initial pilot geography | United States | CONFIRMED | Which states. State-level texting and privacy rules need legal review before any state is treated as in scope |
| Weekly time available | Not established | UNKNOWN | Hours per week and for how many weeks |
| Validation budget | Not established | UNKNOWN | Any amount. No spending is authorized |
| Research repository name | Hike SaaS Lab | CONFIRMED | GitHub repository has not been renamed |

Questions asked at Gate 0 that have not been answered at all:

| Question | Status |
|---|---|
| Loaded hourly cost of the people who would onboard and support pilots | UNKNOWN |
| Product name, separate from the agency | UNKNOWN |

## 2. Commercial decisions

### A. 30-day money-back guarantee

**Status: APPROVED IN PRINCIPLE, CONDITIONAL.**

Conditions before it can be published or offered to anyone:

1. Eligibility, refund conditions, cancellation procedure and exclusions are defined (a draft for review is in PILOT-OFFER.md).
2. Qualified legal review of the guarantee wording.
3. Final commercial terms approved.

Until all three are met, the guarantee must not appear in any material shown to a prospect. The wording in PILOT-OFFER.md is a draft of business terms in plain language. It is not legal text and no legal terms have been written.

### B. 12-month pilot price lock

**Status: APPROVED IN PRINCIPLE, CONDITIONAL.**

Recorded scope of the decision:

1. The lock applies only to the agreed package, its features and its scope.
2. Included usage and additional usage are stated separately. The lock covers the package price and the included usage. It does not set a price for additional usage.
3. Third-party cost changes, new features and material scope changes are handled transparently, in writing, and are not absorbed silently or passed on silently.
4. Final commercial terms are required before any pilot agreement is issued.

### C. $0.02 SMS overage rate

**Status: DEFERRED. NOT APPROVED.**

$0.02 per segment is not a confirmed or approved customer price. It has been removed from the customer-facing draft. No overage rate will be recommended until all of the following are documented:

| Required before a recommendation | Current status |
|---|---|
| Actual LC Phone and SMS charges for the CCS account | UNKNOWN |
| Segment-based billing rules and carrier fees as GoHighLevel applies them | UNKNOWN |
| A2P 10DLC registration and campaign-related costs as GoHighLevel charges them | UNKNOWN |
| Expected usage per location | UNKNOWN. No measured data exists. The plan's figure of 5 to 10 segments per lead is an ESTIMATE |
| Gross margin at the proposed package prices | UNKNOWN. The existing model uses Twilio list prices as a proxy and an assumed labour rate |

## 3. Customer research safeguards

**Status: CONFIRMED.**

1. Existing CCS med spa clients are a potential warm-contact research pool.
2. Maximum 5 warm CCS contacts among 20 customer interviews.
3. At least 3 of the 5 proposed paid pilots must be spas with no CCS relationship.
4. Evidence from existing agency relationships is kept separate from evidence of independent product demand.
5. Interview source and relationship are recorded for every participant.
6. Positive interview comments alone are never reported as customer demand.
7. The evidence that counts is actual willingness to pay and operational problems that repeat across participants.

No one has been contacted and no interviews have been scheduled.

## 4. Authorization boundary

**Current authorization: documentation updates, analysis and preparation of decision materials only.**

| Activity | Status |
|---|---|
| Documentation updates, analysis, decision materials | Authorized |
| Customer outreach, including to existing CCS clients | NOT AUTHORIZED |
| Vendor contact, including GoHighLevel support and booking platforms | NOT AUTHORIZED |
| Mystery shopping (response-time audit) | NOT AUTHORIZED |
| GoHighLevel account changes or configuration | NOT AUTHORIZED |
| Paid services or purchases | NOT AUTHORIZED |
| Legal commitments, including engaging counsel | NOT AUTHORIZED |
| Live customer data processing | NOT AUTHORIZED |
| Sending live marketing messages | NOT AUTHORIZED |
| Pilot launch | NOT AUTHORIZED |
| Application development | NOT AUTHORIZED |
| Pull requests and branch merges | NOT AUTHORIZED without explicit instruction |

Read-only inspection of the CCS GoHighLevel account by a CCS account holder is prepared as a checklist. It has not been run. It needs an explicit go-ahead because it sits outside "documentation".

## 5. Repository identity

**Status: CONFIRMED.** The repository is named Hike SaaS Lab and is the central research, validation, product strategy and decision repository. It is not automatically the production application repository. Each approved product gets its own implementation repository. See the README.

## 6. Inconsistencies found in the existing documents

Found during this review. Each is fixed in the validation documents or recorded as open.

| # | Where | Inconsistency | Handling |
|---|---|---|---|
| 1 | PILOT-OFFER.md | The customer-facing draft said "No setup fee during the pilot" while the internal terms table tests a $500 setup fee on alternating prospects | Fixed. The draft now states it is the no-setup-fee arm and that a second arm exists |
| 2 | PILOT-OFFER.md | Guarantee, price lock and $0.02 overage were written into customer-facing text as if settled | Fixed. Each now carries its Gate 0 status. $0.02 removed from the customer-facing draft |
| 3 | PILOT-OFFER.md | "We sign a business associate agreement with you before any lead data flows" presumed the HIPAA posture was resolved | Fixed. Marked BLOCKED pending legal review and vendor verification |
| 4 | VALIDATION-PLAN.md | Cost model included a "HIPAA add-on share" line at a reported $297 a month, which implies an add-on exists for the CCS plan and is sufficient | Fixed. Line now UNKNOWN. Margins restated as excluding it |
| 5 | VALIDATION-PLAN.md | Cost model assumed the $497 GoHighLevel tier | Flagged. CCS plan is UNKNOWN, so the platform line may be higher, lower or zero |
| 6 | VALIDATION-PLAN.md, DECISION-GATES.md | A Gate 0 pass was written to authorize recruiting, the audit and written requests to vendors in one step. The current authorization allows none of these | Fixed. Gate 0 is now recorded as not passed, and its pass conditions and authorizations are restated |
| 7 | VALIDATION-PLAN.md | Timeline ran in weeks from Gate 0 as if time were available. Weekly availability is not established | Fixed. Timeline marked as unscheduled sequence, not a commitment |
| 8 | VALIDATION-PLAN.md | Draft outreach message was signed with a named person. The interview owner is not decided | Fixed. Signature removed from the draft pending the ownership decision |
| 9 | VALIDATION-PLAN.md, VALIDATION-SCORECARD.md | Gate 4 and scorecard margin thresholds (P6, P7) were set next to a cost model built on proxy rates | Flagged. Thresholds stand, but the model must be rebuilt on real rates before Gate 4 is judged |
| 10 | VALIDATION-PLAN.md, CUSTOMER-INTERVIEW-GUIDE.md | Relationship was recorded only as "warm or cold" | Fixed. Source channel and a relationship category are now recorded separately |
| 11 | VALIDATION-PLAN.md | 10DLC fees were taken from Telnyx and Twilio schedules. GoHighLevel applies its own charges | Flagged. Real figures come from the GHL verification checklist |
| 12 | Research report, section 7 | The plan table lists done-for-you 10DLC setup under the middle tier only, though no tier can text without registration | Not a factual error, a design choice in a recommendation. Report left intact. The pilot offer includes registration in every package |

## 7. Corrections to the research report

**None made.** The research report and research notes are unchanged. No factual error requiring correction was found in this review. The conflicts the report itself lists (PatientNow and Recura acquisition date, Mangomint webhook pricing, GlossGenius and Mindbody prices, GoHighLevel annual prices) remain open and are to be resolved by live re-checks, not by editing the report.

## 8. Files changed in this update

| File | Change |
|---|---|
| `README.md` | New. Repository identity and purpose |
| `validation/GATE-0-DECISIONS.md` | New. This file |
| `validation/GATE-0-OPEN-ITEMS.md` | New. Open questions, ownership sheet, time and budget sheet |
| `validation/GHL-VERIFICATION-CHECKLIST.md` | New. Read-only checklist |
| `validation/COMPLIANCE-GATE.md` | New. Legal review blocker, questions, data inventory |
| `validation/VALIDATION-PLAN.md` | Updated |
| `validation/CUSTOMER-INTERVIEW-GUIDE.md` | Updated |
| `validation/PILOT-OFFER.md` | Updated |
| `validation/VALIDATION-SCORECARD.md` | Updated |
| `validation/DECISION-GATES.md` | Updated |
| `reports/`, `research_notes/` | Unchanged |

Earlier versions of every updated file remain in the git history.
