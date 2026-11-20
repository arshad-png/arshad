# GoHighLevel verification checklist

Prepared 2026-11-20. Status: prepared, not executed. The CCS GoHighLevel subscription plan is UNKNOWN.

## Rules for running this checklist

1. **Read only.** Look and record. Do not change any setting, create or delete a sub-account, buy or enable an add-on, start a trial, connect an integration, install a marketplace app, generate an API key or token, or edit a workflow, form or snapshot.
2. If a page can only be seen by enabling or purchasing something, record "not visible without a change" and stop there.
3. Do not open, export or screenshot client contact records, conversations or any patient information. Screenshots are of settings, plan and billing pages only, with payment card details cropped out.
4. Evidence is saved outside this repository if it shows billing details. Record here only the finding, its source type and the date.
5. Parts A to E are self-inspection by a CCS account admin. Part F item F4 and part G involve contacting GoHighLevel, which is vendor contact and is NOT AUTHORIZED under the current boundary.
6. Running parts A to F3 needs an explicit go-ahead. It has not been given.

## Source types

Every finding is recorded with exactly one source type. They are not interchangeable.

| Code | Source type | What it proves |
|---|---|---|
| ACCOUNT | Observed in the CCS account on the date recorded | What CCS has today |
| OFFICIAL DOC | GoHighLevel's own pricing page, help centre or developer documentation, with URL and date read | What GoHighLevel says publicly |
| WRITTEN VENDOR | A written reply from GoHighLevel to CCS, kept on file | What GoHighLevel has confirmed to CCS specifically |
| THIRD-PARTY | Blog, reseller, competitor or review site | A claim. Not evidence |

Where sources disagree, record each one. Do not pick. For anything touching HIPAA, only WRITTEN VENDOR plus legal review counts as settled.

## What the research currently says (context, not findings)

| Claim | Source type | Status |
|---|---|---|
| Plans listed at $97, $297 and $497 a month, plus an Enterprise tier with no public price | OFFICIAL DOC, read through a summarising tool on 2026-11-20 | Needs live re-check |
| Third parties name the $497 tier differently (Agency Pro, Pro with SaaS Mode, Founder) | THIRD-PARTY | Unverified |
| Annual prices in the research notes look transposed | Research note | Unverified |
| White-label resale with rebilling sits on the $497 tier | THIRD-PARTY | Unverified |
| AI Employee add-on at $50 or $97 per sub-account per month | OFFICIAL DOC, summarised | Needs live re-check |
| HIPAA compliance listed under the Enterprise tier | OFFICIAL DOC, summarised | Needs live re-check |
| A HIPAA add-on at $297 a month | THIRD-PARTY, from a competitor | Unverified |
| No two-way appointment sync with Mangomint, Boulevard, Vagaro or Aesthetic Record | THIRD-PARTY | Unverified |

None of this says what CCS has. It is not assumed that CCS has HIPAA eligibility, that an add-on exists for the CCS plan, or that an add-on would be sufficient.

## Part A. Subscription and billing

| # | Establish | Where to look | Finding | Source type | Date |
|---|---|---|---|---|---|
| A1 | Exact plan name as shown in the account | Agency settings, billing | | | |
| A2 | Billing tier and price actually charged | Billing, latest invoice | | | |
| A3 | Monthly or annual billing, renewal date | Billing | | | |
| A4 | Whether the plan is a current public plan or a legacy or grandfathered plan | Billing, compare with the live pricing page | | | |
| A5 | Add-ons currently active and their prices | Billing | | | |
| A6 | Whether the account is held directly with GoHighLevel or through a reseller or affiliate arrangement | Billing, account owner details | | | |
| A7 | Who the account owner and admins are | Team settings | | | |
| A8 | Live public plan prices, monthly and annual | Public pricing page, read in a browser | | | |

## Part B. Sub-accounts and agency features

| # | Establish | Finding | Source type | Date |
|---|---|---|---|---|
| B1 | Number of sub-accounts in use and the plan limit | | | |
| B2 | Whether new sub-accounts can be created on the current plan without a plan change | | | |
| B3 | Whether snapshots can be created and loaded into a new sub-account | | | |
| B4 | Whether white-label resale (SaaS mode or its current name) is available | | | |
| B5 | Whether rebilling of usage to sub-accounts is available, and whether markup can be set | | | |
| B6 | Whether a white-label domain and branded login are available | | | |
| B7 | Whether client-facing user roles and permissions can restrict what a spa's staff see | | | |
| B8 | Whether a per-sub-account data export is available to the client | | | |

B8 matters because the pilot offer promises the spa can export its own leads and consent records.

## Part C. LC Phone and messaging

These findings are required before any overage rate can be recommended. See GATE-0-DECISIONS.md section 2C.

| # | Establish | Finding | Source type | Date |
|---|---|---|---|---|
| C1 | Whether LC Phone is the active telephony provider, or a connected Twilio account | | | |
| C2 | Actual charge per outbound SMS segment | | | |
| C3 | Actual charge per inbound SMS segment | | | |
| C4 | Carrier surcharges per segment and how they are shown on the bill | | | |
| C5 | MMS charge | | | |
| C6 | Segment rules as billed: characters per segment, effect of emoji or special characters | | | |
| C7 | Voice charge per minute, inbound and outbound | | | |
| C8 | Monthly charge per local number | | | |
| C9 | A2P 10DLC brand registration charge | | | |
| C10 | A2P 10DLC campaign registration and vetting charge | | | |
| C11 | A2P 10DLC monthly campaign charge | | | |
| C12 | Whether each sub-account registers its own brand and campaign under the client's legal name and EIN | | | |
| C13 | Typical approval time shown for past registrations in the account | | | |
| C14 | Whether missed-call text-back is available natively | | | |
| C15 | Whether quiet hours or send windows can be enforced per workflow | | | |
| C16 | How STOP and opt-out are handled and whether the opt-out state can be seen and exported | | | |
| C17 | From existing sub-accounts, aggregate monthly segment counts only (no contact data), as a rough guide to usage per location | | | |
| C18 | GoHighLevel's messaging content policy, including any restricted categories relevant to injectables or weight-loss medication | | | |

## Part D. Workflows, forms, reporting and integrations

| # | Establish | Finding | Source type | Date |
|---|---|---|---|---|
| D1 | Workflow triggers available: form submitted, Meta lead form, Google lead form, missed call, inbound message, appointment status | | | |
| D2 | Whether a workflow can stop automatically when a contact replies, books or opts out | | | |
| D3 | Whether forms support an unchecked, required consent checkbox with custom wording, and whether submission time, form version and IP are stored | | | |
| D4 | Whether a consent record per contact can be reported and exported | | | |
| D5 | Whether Meta lead forms connect natively and whether custom consent questions on the Meta form are captured as fields | | | |
| D6 | Whether Google Ads lead forms connect natively or need a webhook | | | |
| D7 | Shared inbox: new-lead alerts, assignment, and whether time to first response is measured | | | |
| D8 | Pipeline stages and whether stage changes can be reported by lead source | | | |
| D9 | Reporting: leads by source, response time, booked and showed, and whether a scheduled report can be emailed to a client | | | |
| D10 | Whether ad spend can be recorded against a source to compute cost per showed consult | | | |
| D11 | Call tracking numbers and source attribution on calls | | | |
| D12 | Marketplace listings for Mangomint, Boulevard, Vagaro, Aesthetic Record, Zenoti. Read the listing only, do not install | | | |
| D13 | Inbound webhook trigger availability, to receive events from a booking platform | | | |
| D14 | Whether conversation AI or other AI features are active or default-on. The pilot design excludes them | | | |

## Part E. API access and restrictions

| # | Establish | Finding | Source type | Date |
|---|---|---|---|---|
| E1 | Whether API access is included on the current plan, and at which level (agency, sub-account) | | | |
| E2 | Rate limits stated in the developer documentation | | | |
| E3 | Whether outbound webhooks are available on the current plan | | | |
| E4 | Any plan restriction on private integrations or marketplace apps | | | |
| E5 | Terms of service clauses relevant to reselling, to health data and to automated messaging | | | |

Do not generate keys or tokens. Record availability only.

## Part F. HIPAA-related availability and requirements

Nothing in this part is to be inferred. Record what is seen and its source type.

| # | Establish | Finding | Source type | Date |
|---|---|---|---|---|
| F1 | Whether any HIPAA option is visible in the CCS account, and on which plan it is offered | | | |
| F2 | What GoHighLevel's official documentation says the HIPAA option covers and does not cover: which features, which sub-accounts, which data | | | |
| F3 | Whether the documentation says a business associate agreement is signed, with whom (agency, each sub-account, or both), and how | | | |
| F4 | Written confirmation from GoHighLevel to CCS of F1 to F3 for the CCS account specifically. NOT AUTHORIZED today, vendor contact | | | |
| F5 | Whether LC Phone SMS and voice are covered by that option, or excluded | | | |
| F6 | Whether email sending is covered | | | |
| F7 | Whether third-party connections (Meta, Google, Zapier, marketplace apps) are covered or excluded | | | |
| F8 | Whether AI features are covered or excluded | | | |
| F9 | Price, as shown in the account or official documentation | | | |
| F10 | Whether the option applies to the whole agency or must be enabled per sub-account | | | |
| F11 | Any stated customer responsibilities (access controls, audit logs, user training) | | | |

Interpretation rules:

- A HIPAA option being available does not make a configuration compliant.
- An add-on being purchasable does not mean it is sufficient for the pilot design.
- Whether a given med spa is a covered entity, and what CCS's obligations would be, are questions for a lawyer. See COMPLIANCE-GATE.md.
- No material may describe the product as HIPAA compliant on the basis of this checklist.

## Part G. Written questions for GoHighLevel (prepared, not sent)

Sending these is vendor contact and is NOT AUTHORIZED today.

1. Which plan is the CCS account on, and is it a current or legacy plan?
2. Is a HIPAA option available on this plan? If not, which plan is required?
3. Does GoHighLevel sign a business associate agreement? With the agency, with each sub-account, or both?
4. Which features and data flows does it cover? Specifically: contact records, forms, conversations, SMS and voice through LC Phone, email, workflows, reporting, AI features, marketplace apps, API and webhooks.
5. Which are excluded?
6. What does it cost, and is the cost per agency or per sub-account?
7. What are the agency's responsibilities under it?
8. What are the current LC Phone rates for the CCS account for SMS segments, carrier surcharges, voice minutes and numbers?
9. What are the current A2P 10DLC charges and typical approval times?
10. Are there content restrictions on messages about aesthetic treatments or weight-loss medication?

## Summary to complete after the checklist is run

| Question | Answer | Source type |
|---|---|---|
| Can the pilot design be delivered on the current plan without a plan change | UNKNOWN | |
| Real cost per SMS segment including carrier fees | UNKNOWN | |
| Real 10DLC cost per spa, one-time and monthly | UNKNOWN | |
| Is a HIPAA option available to CCS | UNKNOWN | |
| Has GoHighLevel confirmed its scope in writing | UNKNOWN | |
| Has a lawyer reviewed whether it is sufficient | UNKNOWN | |
| Findings that conflict with the research report | | |
