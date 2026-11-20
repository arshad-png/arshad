# US compliance gate

Prepared 2026-11-20. This document is preparation for legal review. It is not legal advice and contains no legal conclusions.

## Blocker

**Status: BLOCKED.**

CCS has no existing lawyer for US messaging and health-data compliance (CONFIRMED). No live pilot can start until a qualified US lawyer has reviewed the pilot design and given written sign-off.

Until the blocker is cleared:

- No live marketing messages are sent.
- No sensitive customer or patient data is processed.
- No pilot agreement, guarantee or consent wording is published or offered.
- The product is not described as HIPAA compliant, TCPA compliant or compliant with any law, in any material, to anyone.

Engaging a lawyer is a paid legal commitment and is NOT AUTHORIZED under the current boundary. It needs a budget decision first. See GATE-0-OPEN-ITEMS.md section 4.

## What clears the blocker

All four are required.

| # | Requirement | Status |
|---|---|---|
| 1 | A qualified US lawyer with telemarketing and messaging (TCPA) experience and health-privacy experience is engaged. This may be one person or two | BLOCKED |
| 2 | Written answers to the questions in this document | BLOCKED |
| 3 | Written sign-off on the consent wording, the opt-out handling, the data handling and the pilot agreement terms, including the 30-day guarantee | BLOCKED |
| 4 | Written confirmation from GoHighLevel of what its HIPAA-related option covers for the CCS account, reviewed by the lawyer for sufficiency | BLOCKED |

## What "qualified" should mean here

For the decision owner to check when choosing counsel. These are selection questions, not requirements invented by this document.

- Licensed in a US state and regularly advising on the TCPA and state telemarketing laws.
- Experience with SMS programmes run by a service provider on behalf of many small businesses.
- Experience with HIPAA business associate questions and with consumer health-data laws outside HIPAA.
- Able to say which states need separate advice.

## What the proposed product would do with data

Based on the pilot design in PILOT-OFFER.md. Nothing is built or configured. This inventory exists so a lawyer can assess the actual design.

### Data collected

| Data | Source | Why | Sensitivity |
|---|---|---|---|
| Lead name, mobile number, email | Website form, Meta lead form, Google lead form | To reply and follow up | Personal data |
| Treatment or service the lead asked about | Form field or free text | To route and report | Health-related when linked to a named person |
| Free-text message from the lead | Form, SMS reply | Conversation | May contain health information the lead volunteers |
| Caller number and time of a missed call | Tracking number | Missed-call text-back | Personal data |
| Consent record: wording shown, checkbox state, time, form version, IP address if available | Form | Proof of consent | Compliance record |
| Opt-out status and time | SMS reply | To stop messaging | Compliance record |
| Lead source, campaign, ad identifiers | Form and ad platform | Reporting by source | Marketing data linked to a person |
| Message history, inbound and outbound | SMS and email | Inbox and audit trail | May contain health information |
| Lead status: new, contacted, booked, showed, lost | Staff input, or booking platform event where available | Reporting | Appointment-related when linked to a named person |
| Spa staff names, emails, logins | Spa | Access | Personal data |
| Spa legal name, EIN, address | Spa | 10DLC registration | Business data |
| Monthly ad spend by source (Convert plus only) | Spa | Cost per showed consult | Business data |

### Data the design does not collect

Clinical charts, treatment notes, photos, prescriptions, payment card details, insurance details, government identifiers, date of birth. Voice calls are not recorded or transcribed in the pilot design. No AI model processes lead conversations in the pilot design.

Whether free-text replies from leads bring some of this in anyway is a question for counsel (question D4).

### Where data would be processed, stored and transmitted

| Stage | System | Vendor | Compliance support status |
|---|---|---|---|
| Capture | Website form | GoHighLevel form, or the spa's own site form passing data in | UNKNOWN |
| Capture | Meta lead form | Meta | UNKNOWN. Data originates on Meta's platform |
| Capture | Google Ads lead form | Google | UNKNOWN. Data originates on Google's platform |
| Storage | Contact record, conversations, pipeline, consent fields | GoHighLevel sub-account | UNKNOWN. See GHL-VERIFICATION-CHECKLIST.md part F |
| Transmission | SMS and missed-call handling | LC Phone and the underlying carriers | UNKNOWN. Whether covered by any GoHighLevel HIPAA option is not established |
| Transmission | Email | GoHighLevel's email service or a connected provider | UNKNOWN |
| Inbound events | Booked and showed status | Booking platform webhook or connector, where one exists | UNKNOWN per platform |
| Middleware | Connector such as Zapier, if a platform needs one | Third party | UNKNOWN. Not assumed to be usable |
| Reporting | Weekly report by email to the owner | GoHighLevel | UNKNOWN. The report is designed to show counts, not named leads |
| Access | CCS staff viewing spa sub-accounts for support | CCS | Access controls not yet defined |
| Export | Lead and consent export to the spa | GoHighLevel | UNKNOWN |

Design choices already made to reduce exposure, all subject to legal review: no treatment detail in automated messages, no conversion events sent back to ad platforms, reports show counts and not names, no AI conversation, no call recording, no reactivation of old patient lists.

## Does the intended configuration support the obligations

**Status: UNKNOWN.** It is not established that the intended GoHighLevel configuration and the vendors in the table above support the obligations a lawyer may identify. Three things have to be known first, in this order:

1. What the CCS account actually has (GHL verification checklist, parts A to F3).
2. What GoHighLevel confirms in writing (checklist F4 and part G).
3. What a lawyer says the obligations are, and whether items 1 and 2 meet them.

If the answer is no, the options are to redesign (for example email-first, or collecting no treatment field), to change vendor, or to stop. Those are decisions for Gate 4.

## Questions for counsel

Prepared for review. Not sent to anyone.

### A. TCPA and consent

1. For automated texts sent to a person who submitted a web form or ad lead form, what level of consent is required, and does it differ between a first reply to their inquiry and later follow-up messages?
2. Is the draft consent wording sufficient? It names the spa, the message types, the frequency, STOP and HELP, and that message and data rates may apply, with an unchecked checkbox.
3. Who is the sender for consent purposes: the spa, CCS, or both? Does the consent need to name CCS as a service provider?
4. When a person calls the spa and the call is missed, may one automated text be sent back without prior written consent? If so, what must it contain or avoid?
5. What consent records must be kept, in what form and for how long?
6. If a spa already holds leads collected before the pilot, can they be loaded and messaged? The design assumes no.
7. Do the follow-up messages count as marketing, as informational, or as a mix, and does it matter for the cadence?
8. What liability does CCS carry as the party operating the messaging for the spa, and how should the pilot agreement allocate it?

### B. Opt-out handling

1. What are the current federal rules on revoking consent, including the status and effective date of the FCC's 2026 revocation order? The research found conflicting sources.
2. Which words or methods of opting out must be honoured beyond STOP?
3. How fast must an opt-out take effect, and does it apply across all of a spa's messaging or only this programme?
4. May a confirmation message be sent after an opt-out, and what may it say?
5. If a lead opts out by text, may the spa still email or call them?

### C. A2P 10DLC

1. Is it correct that each spa must be registered as its own brand under its own legal name and EIN, with CCS acting as the service provider?
2. What must the registered campaign description and sample messages contain, and how closely must live messages match them?
3. Are there content restrictions relevant to med spas, for example injectables or weight-loss medication, that affect what may be sent?
4. Who bears carrier fines for a violation, and how should the agreement deal with that?
5. What must each spa's website privacy policy and terms contain to support registration?

### D. State messaging rules

1. Which states have their own telemarketing or texting laws that would apply to this programme, and what do they add (registration, bonds, quiet hours, frequency limits, private rights of action)?
2. Specifically: Texas (SB 140 and the reported 2025 settlement), Florida, Oklahoma, Washington. The research could not resolve Oklahoma or Washington.
3. Does the law of the spa's state or the lead's state apply, and how should leads from out of state be handled?
4. What quiet hours should be enforced, and in whose time zone?
5. Are there states to exclude from the first pilots?

### E. Privacy and health-data exposure

1. Is a typical independent med spa a HIPAA covered entity? What facts decide it (for example whether it bills insurance electronically)? The research found sources that disagree.
2. If a spa is a covered entity, is CCS a business associate when it handles lead records containing a name and a treatment interest?
3. If a spa is not a covered entity, which laws apply to the same data? Specifically the FTC Health Breach Notification Rule and state consumer health-data laws such as Washington's My Health My Data Act.
4. Leads may volunteer health information in free-text replies. Does that change the answer, and what should the design do about it?
5. Is the safest course for CCS to act as a business associate in every case? What does that require of CCS in practice (agreements, safeguards, training, breach procedures)?
6. Is the intended GoHighLevel configuration, with whatever HIPAA-related option GoHighLevel confirms in writing, sufficient? Which data flows fall outside it?
7. May treatment interest be included in an SMS or email to the lead, or must messages stay generic?
8. Are Meta and Google lead forms an acceptable source for this data, and what must be disclosed on them?
9. May any data be sent back to ad platforms for optimisation? The design assumes no.
10. What breach notification duties would CCS have, to whom and how fast?
11. What may CCS staff see when supporting a spa, and what access controls and logs are needed?
12. What must the agreement say about data ownership, export and deletion at the end of a pilot?

### F. Commercial terms and marketing claims

1. Review the draft 30-day money-back guarantee: eligibility, refund conditions, cancellation procedure, exclusions. Are there state consumer or auto-renewal laws that apply to a month-to-month business subscription?
2. Review the draft 12-month price lock, including how third-party cost changes and scope changes are handled.
3. What claims may be made about results? The offer says no number of bookings is guaranteed.
4. What may be said, if anything, about compliance in sales material?
5. Does running a response-time audit (submitting an inquiry as a prospective customer and later disclosing it) raise any legal issue?
6. Do interview recordings need consent beyond a verbal yes, and does it vary by state?
7. What insurance should be in place before the first pilot?

### G. Future features, for awareness only

Not in the pilot. Listed so counsel can flag anything that changes the pilot design.

1. AI-generated voice or AI text conversation with leads.
2. Call recording and transcription.
3. Reactivation messages to lapsed patients.
4. Automated replies to Instagram and Facebook messages.

## Representations rule

Until this gate is cleared and the lawyer has approved specific wording:

- Do not say or write that the product is HIPAA compliant.
- Do not say or write that it is TCPA compliant or A2P compliant.
- Do not say a business associate agreement will be signed. Whether one is needed, and whether the vendor chain supports it, is not established.
- It is accurate to say: compliance review is in progress and no live pilot will start before it is complete.

## Record of sign-off

| Item | Reviewed by | Date | Outcome | Document on file |
|---|---|---|---|---|
| Consent wording | | | | |
| Opt-out handling | | | | |
| Missed-call text-back | | | | |
| States in scope | | | | |
| Health-data posture | | | | |
| GoHighLevel configuration sufficiency | | | | |
| Pilot agreement terms | | | | |
| 30-day guarantee wording | | | | |
| 12-month price lock wording | | | | |
| Permitted compliance statements | | | | |
