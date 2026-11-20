# Decision gates

Prepared 2026-11-20. Status: draft for review. No gate has been passed.

Each gate is a point where work stops until a decision is made on evidence. A gate states what evidence is needed, what counts as pass or fail, and exactly what a pass authorizes. Nothing downstream of a gate starts before that gate is approved in writing.

Metric codes (D1, W1 and so on) refer to VALIDATION-SCORECARD.md. Every threshold is an ASSUMPTION to be agreed at Gate 0.

## Standing rules, all gates

1. No application code, no installed dependencies, no changes to production systems. Only Gate 7 can reopen this, and only by a separate written decision.
2. No purchase or paid commitment without its own approval, even after a gate passes.
3. Existing research in `reports/` and `research_notes/` stays unchanged.
4. Thresholds are fixed at Gate 0. Changes go in the threshold change log with a reason.
5. Any compliance fail (C1 to C4, O6) stops the pilots at once, whatever gate is current.
6. A gate with missing evidence is not a pass. "We didn't get to it" is a hold.

## Gate overview

| Gate | Question | Earliest timing | Pass authorizes |
|---|---|---|---|
| 0 | Is the plan approved and are the thresholds agreed? | Week 0 | Desk research, recruiting, audit, vendor verification requests |
| 1 | Do owners describe this problem in their own words, and what can really be integrated? | Week 3 to 5 | Using the complaint log and matrix in the offer |
| 2 | Do interviewed owners rank this problem highly and pay for it today? | Week 4 | Finalizing packages and the pilot offer |
| 3 | Is the leak measurable in the wild? | Week 4 | Audit-led outreach as the sales channel |
| 4 | Can it be delivered legally and at a known cost? | Week 5 to 6 | Configuring the snapshot, presenting the offer, taking payment |
| 5 | Will strangers pay a published price? | Week 8 | Onboarding pilots |
| 6 | Is each pilot healthy at day 30? | Day 30 of each pilot | Continuing that pilot, onboarding the next |
| 7 | Business, service line, build, or stop? | After day 90 of the pilots | One of four outcomes |

## Gate 0: plan approval

**Evidence required**
- The five validation documents reviewed.
- Thresholds in the scorecard accepted or edited.
- A decision on each spending line in VALIDATION-PLAN.md section 9.
- Answers to the open questions at the end of this file.

**Pass:** written approval of the plan and thresholds.

**Pass authorizes:** owner-voice desk research, building the audit list, interview recruiting using the reviewed outreach message, written verification requests to booking platforms and GoHighLevel support, reading real messaging rates from the CCS agency account.

**Does not authorize:** presenting the offer, taking money, configuring pilot sub-accounts, engaging counsel on a paid basis unless that line was approved.

## Gate 1: owner voice and integration reality

**Evidence required**
- Complaint log (D7).
- Integration verification log with every claim in VALIDATION-PLAN.md section 6 marked confirmed, unverified or confirmed not possible.
- Live re-check of GoHighLevel plan prices and of the prices the offer cites as anchors.

**Pass**
- D7 passes, and lead response, follow-up or contracts and billing are among the three most frequent problem areas.
- Claims 1 to 8 and 11 resolved in writing.
- At least two booking platforms where the public booking link hand-off is confirmed to work.

**Fail or hold**
- Fewer than 25 items found after a real effort. That suggests owners are not talking about this, which is a finding.
- The dominant complaints are about something else entirely. Take that to Gate 2 as a question for the remaining interviews.
- GoHighLevel HIPAA posture unresolved: hold. Gate 4 cannot pass without it.

**Pass authorizes:** publishing the integration matrix inside the offer, quoting the logged complaints (paraphrased, without names) in sales material.

## Gate 2: interviews

**Evidence required:** interview tracker and tally, with warm and cold contacts reported separately.

**Pass**
- D1, D2 and D3 pass. The sample is big enough, varied enough and not dominated by friends.
- D4 passes on the cold-only tally as well as overall.
- D5 passes.
- D6 passes.

**Reposition**
- D4 fails but another problem shows up unprompted in 8 or more interviews. Stop, write up that problem, and decide whether to re-run this plan against it.

**Stop**
- D4 below 50% and no alternative problem recurring.
- D5 below 25%. Nobody is paying for this job today, in any form.

**Pass authorizes:** finalizing package contents and the pilot offer text, adjusting package scope (not headline prices) to what interviews showed.

## Gate 3: response-time audit

**Evidence required:** audit log for about 50 spas, with results disclosed to each spa.

**Pass:** D8 or D9 passes.

**Fail:** both fail. Independents already respond fast. Combined with a weak Gate 2, this ends the phase. Combined with a strong Gate 2, hold and work out why owners feel a pain the audit does not show (the leak may be in follow-up after first reply, not the first reply itself).

**Pass authorizes:** audit-led outreach as the primary pilot sales channel, using each spa's own result as the opening.

## Gate 4: compliance and cost readiness

This is the hard stop before any money or any lead data moves.

**Evidence required**
- C1: written legal sign-off on consent language, the missed-call text-back question, quiet hours, opt-out handling and which states are in scope.
- C2: GoHighLevel HIPAA posture and BAA confirmed in writing, with its real cost.
- A BAA template for CCS to sign with each spa.
- The cost model in VALIDATION-PLAN.md section 8 rebuilt with real GoHighLevel rates and the real CCS labour rate.
- An onboarding runbook written for at least one booking platform.
- Decisions on the six items listed in PILOT-OFFER.md under "items that need a decision".

**Pass**
- C1 and C2 received.
- Rebuilt cost model shows a projected contribution margin of 40% or more at $297 at pilot scale (P6) and 60% or more at 50 spas (P7).
- Spending for the platform tier, HIPAA add-on and legal work approved.

**Fail**
- Counsel advises that the consent flow or data handling cannot be made compliant on GoHighLevel at a cost the margin can carry. Stop, or redesign as email-first and return to this gate.
- Rebuilt model shows margin under 25% at $297 with no credible route to improve it. The offer is an agency service at these prices. Reprice and return to Gate 2 evidence, or stop.

**Pass authorizes:** approved purchases only, configuring the snapshot in a new sub-account kept separate from client accounts, presenting the offer, taking payment for pilots.

## Gate 5: offer test

**Evidence required:** offer funnel, per-prospect log, objection tally.

**Pass:** W1, W2 and W3 pass. Five paid pilots at $297 or more, three of them cold, within about 100 qualified conversations.

**Partial**
- Five paid, fewer than three cold. Run the pilots, but treat the result as an agency finding until cold sales are shown. Gate 7 cannot return "repeatable business" on this evidence alone.
- Pilots sell only at $197. Run up to five to learn, and record that the price hypothesis failed at $297.

**Fail**
- Fewer than three paid after about 100 qualified conversations. Stop. Write up the objection tally.
- The most common objection is "my booking system already does this". Stop and record which platforms.

**Pass authorizes:** onboarding paid pilots, 10DLC registration per spa, messaging spend within the approved range.

## Gate 6: day-30 pilot health check

Run for each pilot at its day 30.

**Evidence required:** that pilot's rows in the pilot tracker, its onboarding and support hours, its custom request entries.

**Pass**
- O4: baseline captured.
- O1 passes.
- C3 and C4 pass.
- Staff are using the inbox (early read on R4).
- No refund requested.

**Fix before continuing**
- Onboarding took more than 8 hours: write down why before the next spa starts, and update the runbook.
- Custom work was done without being logged or priced: stop doing it and log it.

**Fail for that pilot:** refund requested, or staff never adopted the inbox. Complete the exit interview and record the reason. One failed pilot is data. A pattern across three is a Gate 7 input.

**Pass authorizes:** continuing that pilot and onboarding the next.

## Gate 7: build, continue, service line, or stop

Held once at least five pilots have reached day 90.

**Evidence required:** the full scorecard, the custom request log, the GoHighLevel limitation log, measured costs per pilot, and day-90 conversations with every pilot owner including those who cancelled.

### Outcome A: repeatable business, continue on GoHighLevel

All of:
- R1 and R2 pass.
- O1 passes, and O2 and O3 pass or show a consistent direction with raw counts reported.
- W2 passes. Strangers bought.
- P1, P2, P3, P4 and P5 pass. Setup got faster, the snapshot held, support stayed inside budget, no unlogged custom work.
- P6 passes on measured numbers, P7 passes on the model.
- P10 passes. The same runbook worked at least three times on one platform.

Next step: scale to 25 to 50 spas on GoHighLevel on one or two booking platforms, with the same scorecard. No build.

### Outcome B: build specific software

Everything in outcome A, plus all of:
- At least three pilots hit the same limitation in the GoHighLevel limitation log.
- That limitation blocks a sale, a result or retention, and is not just an annoyance.
- Custom software could remove it. For anything that needs booking-platform data, at least one platform has confirmed workable access in writing.
- Counsel has signed off on the health-data posture of a standalone component.
- A separate written decision approves a scoped build proposal with its own budget.

Next step: a scoped proposal for the smallest piece of software that removes that one limitation. This is the only route by which development starts, and it needs its own approval. Passing Gate 7 does not by itself authorize any code.

### Outcome C: keep it as an agency service line

Signals:
- Customers are happy and retained (R1 passes), and
- any of: W2 fails (only warm contacts bought), P3 fails (every spa needed a different setup), P4 or P5 fail (support or custom work is heavy), P6 fails at published prices.

Meaning: it is a good service that CCS can sell to clients at agency prices. It is not a product. Stop calling it one, fold it into the agency offer, and price it for the labour it really takes.

### Outcome D: stop

Any of:
- R1 below 60%.
- Outcome metrics flat against baseline in most pilots and owners say so.
- A compliance incident that cannot be designed out.
- The booking platforms' own AI front desks are cited by three or more pilots as the reason to cancel.

Next step: write up what was learned, keep the research and the logs, and close the phase.

### If the evidence is mixed

Do not average it into a pass. State which outcome each block points to and choose the more conservative one. Extending pilots by 60 days is acceptable once, with the specific metric that needs more data named in advance.

## Open questions to settle at Gate 0

1. Does CCS have existing med spa clients? How many, and on which booking platforms? This sets the warm-contact cap and where the first runbook is written.
2. Which GoHighLevel plan is the agency on today? If it is already the $497 tier, the platform line is not an added cost.
3. What is the real loaded hourly cost of the people who would onboard and support pilots? The cost model uses an assumed $40.
4. Who runs the interviews and the audit, and how many hours a week can go to this for six weeks?
5. Is there a budget for interview thank-you gifts, the AmSpa report and legal review?
6. Is there a lawyer CCS already uses for TCPA and health-data questions?
7. Are the three commercial commitments in the pilot offer acceptable as drafted: the 30-day money-back guarantee, the 12-month price lock and the $0.02 overage rate?
8. What is the product called? A name separate from the agency is recommended.
9. Which states are in scope for the first pilots?
