# Validation execution plan

Prepared 2026-11-20. Status: draft for review. Nothing in this plan has been started.

Companion files: CUSTOMER-INTERVIEW-GUIDE.md, PILOT-OFFER.md, VALIDATION-SCORECARD.md, DECISION-GATES.md. Source research: `reports/Med spa SaaS opportunity research.md` and `research_notes/` (unchanged by this plan).

## 1. What this phase has to answer

One question: is the lead-to-consult offer for independent med spas a repeatable, profitable business, or is it another customized agency service?

The research could not answer it. It found vendor data saying the leak exists and no owner saying so in their own words. So validation has to produce three kinds of evidence the research lacks:

1. Demand evidence. Owners describe the problem unprompted and pay a published price for the fix.
2. Outcome evidence. Pilots measurably improve response time and booked consults against a baseline.
3. Repeatability evidence. Each new customer takes less setup time than the last, runs on the same configuration, and stays profitable after labour is counted.

The third is what separates a business from an agency service. A pilot that hits its numbers through heavy custom work per spa is a fail for this purpose, even if the customer is happy. The scorecard tracks it explicitly.

## 2. Boundaries

These apply to the whole phase until a decision gate says otherwise.

| Boundary | What it means in practice |
|---|---|
| No application code | Configuration inside GoHighLevel (workflows, pipelines, forms) is the only build work, and only after Gate 4 |
| No dependencies installed | Nothing is installed anywhere |
| No changes to production systems | No edits to live client sub-accounts or live sites. Pilot configuration goes in a new, separate sub-account and snapshot |
| No purchases or paid commitments | Every item that costs money is listed in section 9 and needs its own approval |
| Research preserved | `reports/` and `research_notes/` are read-only. New findings go in new files under `validation/` |
| No outreach, no external commitments | No owner, vendor, lawyer or platform is contacted until Gate 0 is approved. Outreach scripts in this plan are drafts |

## 3. Labels used

Same scheme as the research report. FACT means a named source published it. ESTIMATE means arithmetic or a projection with the basis stated. ASSUMPTION means no source. RECOMMENDATION means a proposal for approval. Prices are marked official (read from the vendor page on 2026-11-20 through a summarising tool, so re-check live), third-party unverified, or estimate.

## 4. Workstreams at a glance

| Workstream | Output | Runs | Gate it feeds |
|---|---|---|---|
| A. Customer discovery | 15 to 20 logged interviews | Weeks 1 to 4 | Gate 2 |
| B. Competitive intelligence | Owner complaint log, verified integration matrix | Weeks 1 to 5 | Gate 1 |
| B2. Response-time audit | Measured first-response times for about 50 spas | Weeks 2 to 4 | Gate 3 |
| C. Market testing | Three published packages, pilot offer, offer test | Weeks 4 to 8 | Gate 5 |
| D. Operational feasibility | Cost model with real rates, compliance sign-off, onboarding runbook | Weeks 2 to 6 | Gate 4 |
| E. Scorecard | One tracker updated weekly | Whole phase | All gates |
| Paid pilots | 5 to 10 spas, 90 days each | Months 2 to 5 | Gates 6 and 7 |

Timings are ASSUMPTIONS and count from the day Gate 0 is approved.

## 5. Workstream A: customer discovery

Full questions and logging rules are in CUSTOMER-INTERVIEW-GUIDE.md. This section covers who and how.

### Who to recruit

Target 15 to 20 completed interviews. RECOMMENDATION for the sample:

| Criterion | Rule | Why |
|---|---|---|
| Business type | Independent med spa, 1 to 5 locations, not PE-owned, not a franchise | Matches the target segment in the research |
| Size | 3 to 15 staff | Solo suites rarely have a lead volume problem (ASSUMPTION) |
| Inquiry volume | At least 30 new inquiries a month, or any paid ads running | Below that there is little to fix |
| Role | Owner, practice manager or front-desk lead. Aim for at least 5 front-desk or manager voices | Owners describe the problem, front desk describes the workflow |
| Booking platform | At least 4 different platforms across the sample, with at least 3 interviews each on Mangomint, Vagaro and Boulevard if possible | Integration limits differ by platform |
| Relationship to CCS | No more than 5 of 20 are existing CCS clients or warm referrals | Friends say yes. Strangers show whether this is repeatable |
| Geography | At least 3 states | State texting rules and market maturity differ |

The cap on existing clients matters most. If the only people who see the problem and want the fix are people who already trust CCS, that is evidence of a good agency, not a product.

### Where to find them

| Channel | Method | Expected yield (ASSUMPTION) |
|---|---|---|
| Existing CCS network | Direct ask, capped at 5 | High reply rate, biased |
| Audit-led outreach | Email or call spas from the response-time audit after their result is recorded, share the result, ask for 20 minutes | Best cold channel, the result is a reason to talk |
| LinkedIn | Search owner, practice manager, med spa director by metro, short connection note | Low reply rate, wide reach |
| Instagram | Direct message to the business account, which owners often run themselves | Unknown |
| Facebook groups for med spa owners | Read group rules first. Ask the admin before posting a research request | Unknown, the research found no data on these groups |
| Local in person | Spas near CCS, visit at a quiet hour | High reply rate, small pool |

RECOMMENDATION: offer a thank-you worth about $50 (gift card or a copy of the audit findings report) for a completed 30-minute call. This is spending and needs approval under section 9. Some licensed providers may decline gifts, so offer the findings report as the alternative.

### Draft outreach message (not sent, for review)

Subject: 20 minutes on how your spa handles new inquiries?

Hi {{contact.first_name}},

I'm researching how independent med spas handle new inquiries, from the first form fill or missed call to a booked consult. I'm not selling anything on this call. I'm talking to about 20 owners and managers and will share what I learn with everyone who takes part.

Would you have 20 to 30 minutes in the next two weeks?

Arshad, Clear Choice Systems

Rules for outreach once approved: one message and one follow-up, no more. Email and phone only to business contact details the spa publishes. No automated text messages to anyone, since unsolicited marketing texts are exactly the risk this product has to manage.

### What the interviews must establish

1. The actual lead workflow, step by step, for the last real inquiry.
2. Who owns follow-up and how many attempts are made.
3. Current software and what each tool costs per month.
4. What they pay agencies, answering services or extra staff for the same job.
5. What they have tried and dropped, and why.
6. Price reaction to the three packages, asked only at the end.

## 6. Workstream B: competitive intelligence

### B1. Owner voice desk research

The research tools were blocked from Reddit, Capterra, G2 and Software Advice. A person in a normal logged-in browser is not. This is manual work.

| Source | What to read | Target |
|---|---|---|
| Reddit | r/medspa, r/aestheticnursing, r/Esthetics, r/PPC, r/smallbusiness. Search: leads, front desk, follow up, no show, Podium, Weave, GoHighLevel, agency, Boulevard, Mangomint, Zenoti | 25 logged items |
| Capterra, G2, Software Advice | One to three star reviews, most recent first, for Boulevard, Mangomint, Vagaro, Zenoti, Aesthetic Record, AestheticsPro, PatientNow, Podium, Weave, GoHighLevel | 25 logged items |
| Trustpilot, BBB | Podium, Birdeye, Weave, PatientNow, Aesthetix CRM | 10 logged items |
| Facebook groups | Only where membership is granted and rules allow reading for research. Paraphrase, never quote names | As available |

Log every item with: date read, URL, date posted, reviewer role if stated, product named, problem area (lead response, appointments, follow-up, retention, reporting, attribution, contracts and billing, integration, support), a short direct quote, and whether it is about a med spa specifically. Pass signal: at least 50 dated items. Read for disconfirming evidence too. Threads where owners say lead follow-up is fine, or that their platform's AI front desk solved it, are worth more than another complaint.

### B2. Response-time audit

RECOMMENDATION: measure the leak directly. No independent study of med spa response times exists.

Method: pick about 50 independent med spas across two or three metros. For each, submit the website contact form once and place one call during business hours that goes to voicemail if unanswered. Record time to first response by channel over 5 business days, and whether the response included a way to book.

Conduct rules: one form and one call per spa, a real name and a real question, no booked appointments that would hold a slot, and no deception beyond not announcing the research up front. After the 5 days, tell each spa what was done and share its result. That disclosure is also the best opening for an interview or pilot conversation.

### B3. Integration claims to verify

The research left conflicts and third-party claims open. Each needs a confirmed answer before any package promises it. "Confirmed" means a written reply from the vendor or the claim observed working in a real account. A sales rep saying yes on a call does not count.

| # | Claim | Current status | How to confirm |
|---|---|---|---|
| 1 | Mangomint outbound webhooks: included or a $50 a month add-on | Conflict between its integrations page and a help article | Written reply from Mangomint support, plus a check inside a pilot spa's account |
| 2 | Mangomint has no inbound API for creating appointments | Official page lists webhooks only | Written reply |
| 3 | Boulevard API is Enterprise tier only | Stated on Boulevard's API page | Written reply on what a Premier-tier customer can expose, and whether its Zapier app triggers on new appointment and status change |
| 4 | Vagaro API and webhooks need Enterprise sales and Vagaro payments | Third-party reported | Written reply from Vagaro |
| 5 | Aesthetic Record Zapier app is read-only with two triggers | Third-party reported | Open the Zapier app listing and record triggers and actions |
| 6 | GoHighLevel has no two-way appointment sync with Mangomint, Boulevard, Vagaro or Aesthetic Record | Third-party reported, competitor sources | Check the GoHighLevel marketplace and each platform's integration list |
| 7 | GoHighLevel HIPAA: Enterprise tier only, or an add-on at a reported $297 a month | Official page lists it under Enterprise, add-on price is third-party unverified | Read inside the CCS agency account, confirm with GoHighLevel support in writing, get the BAA terms |
| 8 | GoHighLevel plan prices, including the annual prices that looked transposed in the notes | Needs live re-check | Read the live pricing page and the CCS billing page |
| 9 | Zenoti AI Lead Manager needs the AI Plus package | Official claim, price not public | Low priority, Zenoti spas are not the pilot target |
| 10 | Third-party AI receptionists that claim booking into Boulevard, Zenoti, Mangomint, Vagaro (Clara AI, AgentZap) | Vendor claim, no independent confirmation | Ask interviewees who use them. Do not contact these vendors posing as a buyer |
| 11 | Each booking platform exposes a public booking link that can be deep-linked by service | Assumed | Open the booking page of 3 real spas per platform |
| 12 | Show status can be read automatically on any pilot platform | Unknown | Follows from items 1, 3, 4, 5 |

Output: one matrix per platform with three columns kept strictly apart: confirmed capability, unverified claim, confirmed not possible. That matrix goes into the pilot offer as the published integration table.

## 7. Workstream C: market testing

Package definitions and the pilot terms are in PILOT-OFFER.md. Summary here.

### The three packages

| | Capture, $197 | Convert, $297 | Convert plus, $497 |
|---|---|---|---|
| The job | Every form and ad lead gets a reply and a follow-up | Adds the phone leak, the staff inbox and show tracking | Adds source-level cost reporting and a monthly review |
| Price label | Estimate, hypothesis | Estimate, hypothesis | Estimate, hypothesis |

### How price gets tested

The research proposed showing different prices to different prospects. RECOMMENDATION: do not do that. It conflicts with a transparent offer, and with 5 to 10 pilots it produces noise, not a result. Test price three other ways:

1. Interviews. Four price-sensitivity questions and a package choice at the end of each call (see the interview guide). 15 to 20 data points.
2. Published menu. All three packages shown to every prospect at the same prices. The signal is which one they choose, where they push back and what they ask to remove or add.
3. Two terms experiments that do not change the headline price: setup fee ($0 against $500) and commitment (month-to-month against 12 months prepaid at two months free). Alternate by prospect and record which arm each saw. These are honest because every prospect in the same arm gets the same published terms.

With samples this small, treat the result as direction, not proof. The scorecard says so.

### Offer test

After Gate 4: a one-page description of the offer (a document or PDF, not a new website, so nothing touches production), sent to audited spas and interviewees who asked to hear more. Target: about 100 qualified conversations and at least 5 paid pilots at $297 or more, at least 3 of them from spas with no prior CCS relationship.

## 8. Workstream D: operational feasibility

### Messaging costs

FACT (official list prices): Twilio outbound SMS is $0.0083 per segment and Telnyx $0.004, before carrier fees of about $0.0035 to $0.005 per segment. ESTIMATE: about $0.012 to $0.013 per segment all-in at Twilio list.

GoHighLevel bills messaging through its own phone system at its own rates, and with rebilling an agency can mark those up. Those rates were not retrieved in the research. RECOMMENDATION: before Gate 4, read the actual per-segment, per-minute and per-number rates from the CCS agency billing page and replace the proxy figures below.

| Cost line | Capture | Convert | Convert plus | Label |
|---|---|---|---|---|
| Included SMS segments per month | 1,000 | 2,000 | 3,000 | RECOMMENDATION |
| SMS cost at $0.012 to $0.013 | $12 to $13 | $24 to $26 | $36 to $39 | ESTIMATE, Twilio list as proxy |
| 10DLC campaign monthly fee | $1.50 to $10 | $1.50 to $10 | $1.50 to $10 | FACT, Telnyx schedule |
| Phone number rental and missed-call minutes | Read from account | Read from account | Read from account | Not sourced |
| Email sends | Negligible | Negligible | Negligible | ASSUMPTION |
| Variable cost before labour | About $14 to $23 | About $26 to $36 | About $38 to $49 | ESTIMATE |

One-time per spa: 10DLC brand registration and campaign vetting, $19.50 on the Telnyx schedule (official) to about $61 on the Twilio schedule (third-party unverified).

Two things to check that the research flagged but did not resolve. First, a 160-character text is one segment, but one emoji or smart quote switches the encoding and a long message can become three or four segments, so cadence copy has to be written to segment limits. Second, med spa content (injectables, weight-loss drugs) may sit close to carrier restricted categories. Read the carrier content policy before writing templates.

### Consent and compliance requirements

Research, not legal advice. Every row needs counsel before a pilot spa goes live.

| Requirement | What the offer has to do | Status |
|---|---|---|
| A2P 10DLC | Register a brand and campaign for each spa under the spa's own legal name and EIN. Sample messages and opt-in proof must match what is actually sent | Known process, per-spa lead time not sourced |
| TCPA prior express written consent for marketing texts | Unchecked consent checkbox on every form, naming the spa, message types, frequency, STOP and HELP, message and data rates. Keep a timestamped consent record per lead | Draft language to counsel |
| Meta and Google lead forms | Add the same consent language as a custom disclaimer and a required consent question on the form itself. A lead without recorded consent gets email and a staff call task, not an automated text | Design rule |
| Missed-call text-back | A caller who rang the spa is treated as an inquiry. Whether one informational text back is allowed without written consent is a legal question. Keep the text non-promotional | Counsel to confirm |
| Opt-out | STOP honoured immediately across all cadences. FCC revocation rules were rewritten in September 2026 and the effective date is disputed in the sources | Counsel to confirm current rule |
| Quiet hours | No automated texts outside 8am to 9pm in the lead's local time. Florida and other states are stricter in places | Design rule, counsel to confirm states |
| Texas SB 140 | Texts are covered by telephone solicitation law. A reported settlement exempts consent-based texts from registration and bond | Counsel to confirm before any Texas pilot |
| HIPAA | Whether a given med spa is a covered entity is disputed. A lead record naming a person and a treatment is sensitive either way. Safe design: act as a business associate, sign a BAA with the spa, and have a BAA chain to GoHighLevel | Blocked until claim 7 in section 6 is confirmed |
| Health data outside HIPAA | FTC Health Breach Notification Rule and Washington My Health My Data Act may apply where HIPAA does not | Counsel to confirm |
| Ad platform data | No conversion events with treatment detail sent back to Meta or Google during the pilot | Design rule |
| Message content | No treatment detail, results claims or pricing promises in automated texts. First reply acknowledges and offers the booking link | Design rule |
| Data ownership | The spa owns its leads and consent records and can export them at any time | Offer term |

RECOMMENDATION: no pilot spa is onboarded until the HIPAA row and the consent language have written sign-off. This is Gate 4.

### Onboarding requirements

Target: one repeatable runbook, the same for every spa on the same booking platform.

| Step | Owner | Target time by pilot 8 (ASSUMPTION) |
|---|---|---|
| Intake form: legal name, EIN, address, booking platform, booking link, lead sources, staff who will use the inbox | Spa | 15 minutes of spa time |
| 10DLC brand and campaign submission | CCS | 30 minutes, then carrier wait |
| Load snapshot into a new sub-account | CCS | 15 minutes |
| Connect lead sources: site form, Meta lead form, Google lead form, tracking number | CCS with spa access | 60 minutes |
| Add consent language to every form | CCS, spa approves | 30 minutes |
| Set booking link and business hours | CCS | 10 minutes |
| Staff training on the inbox and one-tap show confirmation | CCS with spa staff | 30 minutes |
| Baseline capture: two weeks of leads logged before automation is switched on | CCS | 20 minutes |
| Go-live check: test lead through every source | CCS | 20 minutes |

ESTIMATE: about 3.5 hours of CCS time per spa once the runbook is stable. The first three pilots will take longer, likely 8 to 12 hours each (ASSUMPTION). The scorecard tracks the trend, and the trend is the point.

### Support requirements

| Item | Capture | Convert | Convert plus |
|---|---|---|---|
| Channel | Email | Email and text | Email, text, scheduled call |
| First reply target | One business day | Same business day | Same business day |
| Reports | Monthly, automated | Weekly, automated | Weekly, automated, plus cost by source |
| Review call | None | None | 30 minutes a month |
| Cadence changes | Standard cadence only | Standard cadence only | Up to 3 treatment-specific cadences from a fixed library |
| Support time budget per spa per month (ASSUMPTION) | 0.5 hours | 1 hour | 2.5 hours |

Anything outside the package is logged as a custom request in the scorecard, not quietly done. A pilot spa that asks for custom work gets a yes or no and a line in the log. That log is the main evidence on the agency-service question.

### Delivery cost per customer

ESTIMATE, steady state, per spa per month. Labour is costed at an assumed $40 an hour loaded rate, which is a stand-in. Replace it with the real CCS figure.

| Line | Capture $197 | Convert $297 | Convert plus $497 |
|---|---|---|---|
| Messaging and telecom | $14 to $23 | $26 to $36 | $38 to $49 |
| Support labour | $20 | $40 | $100 |
| Onboarding labour, 3.5 hours spread over 12 months | $12 | $12 | $12 |
| Platform cost share, $497 a month over 10 spas | $50 | $50 | $50 |
| HIPAA add-on share, reported $297 a month over 10 spas, unverified | $30 | $30 | $30 |
| Total | $126 to $135 | $158 to $168 | $230 to $241 |
| Contribution margin | About 31% to 36% | About 43% to 47% | About 52% to 54% |

Three readings of that table. The platform and HIPAA shares fall fast with scale: at 50 spas they drop from $80 to $16 per spa and Convert moves to about 65% margin. If CCS already pays for the $497 tier for its agency work, the platform line is not an added cost. And Capture at $197 is thin at pilot scale, which is itself a finding: it may only make sense as a self-serve tier with near-zero support.

Not in the table because no figure exists yet: sales time per closed customer, payment processing fees, legal fees, insurance, refunds. The pilots measure the first one.

## 9. Spending that needs separate approval

Nothing here has been bought or committed. Each line is a request to consider at the gate shown.

| Item | Amount | Label | Needed by |
|---|---|---|---|
| AmSpa State of the Industry report | $995 as reported in the notes, confirm at purchase | Third-party unverified | Gate 1, optional |
| Interview thank-you gifts, 20 at about $50 | About $1,000 | Estimate | Gate 0 |
| Legal review: consent language, HIPAA posture, BAA, state texting rules | Not found, must be quoted | None | Gate 4 |
| GoHighLevel $497 tier, if CCS is not already on it | $497 a month | Official, re-check live | Gate 4 |
| GoHighLevel HIPAA add-on | Reported $297 a month | Third-party unverified | Gate 4 |
| 10DLC registration per pilot spa | $19.50 to about $61 one-time, $1.50 to $10 a month | Official and third-party | Gate 5 |
| Messaging usage during pilots | About $14 to $49 per spa per month | Estimate | Gate 5 |

## 10. Timeline

| Week | Work |
|---|---|
| 0 | Gate 0: approve this plan, agree thresholds, approve or decline the spending lines |
| 1 to 2 | Desk research on owner voice. Integration verification requests sent. Interview recruiting starts. Audit list built |
| 2 to 4 | Interviews. Response-time audit runs. Real GoHighLevel rates read from the agency account |
| 3 to 5 | Counsel engaged. Integration matrix completed. Gate 1 and Gate 3 reviews |
| 4 | Gate 2: interview review |
| 5 to 6 | Gate 4: compliance and cost readiness. Snapshot configured in a separate sub-account |
| 6 to 8 | Offer test. Gate 5: pilots sold |
| Months 2 to 5 | Pilots run 90 days each. Gate 6 at day 30 of each pilot |
| End | Gate 7: build, continue, keep as a service line, or stop |

## 11. Risks to the validation itself

| Risk | Mitigation |
|---|---|
| Sample bias toward people who already like CCS | Cap of 5 warm contacts in interviews, at least 3 cold pilots |
| Leading the witness in interviews | No pitch until the last third of the call, ask about the last real inquiry, not opinions |
| Small samples read as proof | Scorecard reports counts, not percentages alone, and labels pricing results as directional |
| Pilots succeed through unbilled custom work | Hours and custom requests logged per spa, margin computed after labour |
| Pilot spas with tiny lead volume show no measurable change | Qualify on at least 30 inquiries a month before selling a pilot |
| Baseline is missing, so improvement cannot be shown | Two-week baseline is a condition of the pilot |
| Compliance shortcut under time pressure | Gate 4 is a hard stop with written sign-off |
| Thresholds moved after the evidence arrives | Thresholds agreed in writing at Gate 0 |
