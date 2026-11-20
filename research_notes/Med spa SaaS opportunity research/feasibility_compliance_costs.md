# Med spa lead-management SaaS: technical feasibility, compliance, operating costs, GTM benchmarks

Access date for every URL below: 2026-11-20. US focus. This is research, not legal advice; items marked LAWYER need counsel to confirm.

Labels used on every item:
- FACT = read on the vendor's/agency's own page during this session (URL given).
- FACT-2ND = reported by a third party (law firm, aggregator, competitor blog); not confirmed on the primary page. Treat as a lead to verify, not as a verified price or rule.
- ESTIMATE = my calculation, basis stated.
- ASSUMPTION = input I chose, not sourced.

Source-quality warning that applies to section A: most per-platform API detail comes from Supergood (sells an unofficial-API product, so has an interest in gaps looking large), Nirmitee (consultancy) and apis.io/API Evangelist (aggregators). Vendor developer portals for Boulevard, Zenoti and Vagaro returned almost no content to the fetch tool, so they could not be read directly.

---

## A1. Which booking/EMR platforms let a third party read availability and create/modify appointments and clients?

### Takeaway
Only a minority of the 15 platforms offer something a startup can build on without a commercial negotiation: Square (open, documented), Acuity (open, plan-gated), Mindbody (open sandbox, reviewed go-live, usage-billed), Pabau (reported open to all customers), Nextech (documented FHIR partner API, registration required) and Boulevard (real API but reported Enterprise-tier only). Zenoti, Vagaro, PatientNow, AestheticsPro and Jane are gated per customer or per partner; Mangomint, Aesthetic Record and Symplast have no public read/write booking API that I could find. No vendor's written partner terms were obtained.

### Cited Findings

| Platform | Dev doc URL | Access model | Fees / restrictions | Label |
|---|---|---|---|---|
| Zenoti | https://docs.zenoti.com/ | Customer-gated. Official docs only say to email apisupport@zenoti.com for access help. Third party says production API keys are generated inside the Zenoti backend by an existing customer; no self-serve developer signup. | No Zenoti fee published. Another integrator (TouchMD) charges its own one-time setup + recurring maintenance fee for its Zenoti link. No partner-program terms found. | FACT for support route — [Zenoti docs](https://docs.zenoti.com/docs/support); FACT-2ND for key model — [Supergood](https://supergood.ai/docs/zenoti-api); FACT-2ND TouchMD — [TouchMD help](https://help.touchmd.com/?p=105274) |
| Boulevard | https://developers.joinblvd.com/ | Developer portal with sandbox business ID + API key; Admin, Client and Tokenization APIs (GraphQL). Reported as limited to Enterprise-tier customers; app is created and installed per business. | Enterprise plan is custom-priced. Public pricing page lists Essentials $143/mo (1 location), Premier $234/mo/location (promo, normally $293), Prestige $328/mo/location (promo, normally $410), Enterprise custom; it does not state which plan includes API access and only mentions "the industry's most powerful APIs" under Enterprise. Rate limits not publicly documented. | FACT plan prices — [Boulevard pricing](https://www.joinblvd.com/pricing); FACT-2ND Enterprise gating — [apis.io](https://apis.io/plans/boulevard/boulevard-plans-pricing/), [Supergood](https://supergood.ai/docs/boulevard-api), [API Evangelist](https://providers.apievangelist.com/providers/boulevard/) |
| Mangomint | https://www.mangomint.com/learn/webhooks-integration/ | Outbound webhooks only ("send event data from Mangomint to other third-party applications"). No public REST API, developer portal or OpenAPI spec reported. Custom API access reported only on Unlimited tier via sales. | Webhooks reported as a $50/mo add-on, Standard and Unlimited plans only (single secondary source, not confirmed on Mangomint's site). | FACT webhooks exist — [Mangomint](https://www.mangomint.com/learn/webhooks-integration/); FACT-2ND rest — [Supergood](https://supergood.ai/api-report-card/mangomint), [API Evangelist](https://providers.apievangelist.com/providers/mangomint/) |
| Vagaro | https://docs.vagaro.com/ (titled "Enterprise Business API V2") | Not on by default. Vagaro's page says to enable APIs & webhooks you must "contact our Enterprise Sales Team". Third parties describe a request form, approval up to 7 business days, eligibility limited to paid non-trial accounts with Vagaro credit card processing enabled. | Conflict: two secondary sources say $10/mo incl. 5,000 calls; a third says no listed price, provisioned via enterprise sales. No official price found. | FACT sales-gated — [Vagaro](https://www.vagaro.com/pro/updates/webhooks); FACT-2ND — [Supergood](https://supergood.ai/api-report-card/vagaro), [AgentZap](https://agentzap.ai/blog/how-to-enable-vagaro-api-and-webhooks-complete-setup-guide-2026), [apis.io](https://apis.io/plans/vagaro/vagaro-plans-pricing/) |
| AestheticsPro | None public | No developer docs/SDK. Only an outbound webhook feed enabled by a Client Success Manager on Executive or Enterprise edition. A G2 reviewer described the lead API as having zero documentation. | $25 per location per month API access fee, plus $0.02 per task over 5,000 per billing cycle (as described by an integrating CRM vendor). | FACT-2ND — [Supergood](https://supergood.ai/api-report-card/aestheticspro), [Aesthetix CRM help](https://help.aesthetixcrm.com/en/articles/1457-overview-of-aestheticspro-integration-with-aesthetix-crm) |
| Aesthetic Record | None public | Effectively no public API. ~25 prebuilt partner connections (Cherry, Shopify, Stripe, Zapier). One documented Leads endpoint; token via support. Integrations are switched on by a practice Admin; a new lead vendor applies by email; no published application/review process for non-lead integrations. | No fees found. | FACT-2ND — [Supergood](https://supergood.ai/api-report-card/aesthetic-record), [Nirmitee](https://nirmitee.io/blog/aesthetic-record-api-integration-guide/) |
| PatientNow | No public portal found | Three REST APIs reported (Essentials, VISH, Pro); webhooks on Essentials. Essentials credentials live in the customer's account plus a vendor-issued gateway key; Pro keys issued by PatientNow staff; no sandbox. | "Gated access, partial coverage, or paid tiers" reported; no price found. | FACT-2ND — [Supergood](https://supergood.ai/api-report-card/patientnow) |
| Nextech | https://nextechsystems.github.io/selectapidocspub and https://nextechsystems.github.io/practiceplusapidocspub | Documented FHIR partner API (STU3 3.0.1, plus an R4 "Nextech Partner API" OpenAPI spec). OAuth 2.0 bearer token + practice ID header. Appointment search supported. Access through a developer registration form; Practice+ credentials come from a Nextech representative. | Rate limit 20 requests/second per endpoint. No fee published in the docs read. | FACT — [Nextech Select API docs](https://nextechsystems.github.io/selectapidocspub), [Practice+ docs](https://nextechsystems.github.io/practiceplusapidocspub) (read via search summary, not full-page fetch) |
| Symplast | None found | No official public API reference found. Integrations are partner-built (EntityMed describes a bidirectional link that books into Symplast; also Red Spot Interactive, Digital Limelight Media, Birdeye). | None found. | FACT-2ND — [EntityMed](https://entitymed.com/blog/entitymed-integration-with-symplast), [Birdeye](https://birdeye.com/integration/symplast) |
| Pabau | Postman reference (public, per secondary source); marketplace terms at https://www.pabau.com/partners/developer-terms | REST API reported open to every customer; keys and webhook subscriptions created in an in-app "Private Apps Developer Hub". Separate App Marketplace requires review/approval. | Marketplace apps must route payments through Pabau Payments. Pabau is UK-origin; US med spa share not researched. | FACT-2ND — [Supergood](https://supergood.ai/api-report-card/pabau); developer terms — [Pabau](https://www.pabau.com/partners/developer-terms) |
| Jane App | https://developers.jane.app | Partner-gated. Sources disagree on how public the docs are: one says vetted partners only with no self-serve signup; another describes a quick-start, API reference and sandbox. No webhooks reported (polling). | None found. | FACT-2ND, conflicting — [Supergood](https://supergood.ai/api-report-card/jane-app), [Nirmitee](https://nirmitee.io/blog/jane-app-api-integration-guide/) |
| Mindbody | https://developers.mindbodyonline.com/ | Open developer signup; sandbox "always free"; go-live requires Mindbody review of the application, then per-site activation by each business. Webhooks available. | Official FAQ: free API access under 5,000 calls per billing cycle. Overage rate conflicts in secondary sources (~$0.002 vs ~$0.003 per call; one says 1,000 free calls/day per site). Billing starts on go-live day. Webhook deliveries do not count as API calls. | FACT — [Mindbody developer FAQ](https://developers.mindbodyonline.com/resources/faqs), [Webhooks docs](https://developers.mindbodyonline.com/WebhooksDocumentation); FACT-2ND overage — [Carly](https://www.usecarly.com/blog/mindbody-api/) |
| Moxie (med spa, joinmoxie.com) | Not found | NOT VERIFIED. Search returned a "Public API fundamentals" help article on help.withmoxie.com (per-workspace X-API-KEY, webhooks), but withmoxie.com appears to be a different product (a freelancer business tool), not the med spa platform. Do not rely on it. | Unknown. | See Gaps |
| Square Appointments | https://developer.squareup.com/docs/bookings-api/what-it-is | Open, self-serve OAuth. Bookings API reads availability and creates/updates/cancels bookings. | Seller-level writes require each seller to have a paid Appointments Plus or Premium subscription (active or trial); on the free plan only buyer-level bookings can be created/updated/cancelled. Cannot create team members or make them bookable via API; cannot create a booking with a non-zero cancellation fee. | FACT — [Square Bookings API](https://developer.squareup.com/docs/bookings-api/what-it-is) |
| Acuity Scheduling | https://developers.acuityscheduling.com/ | Open docs; API key (User ID + key from Integrations > API) or OAuth2 (scope api-v1); webhooks. | Plan-gated; sources conflict on the minimum tier (top "Premium", formerly Powerhouse, vs "Emerging Entrepreneur or higher"). Reported limits: 10 requests/second, 20 concurrent connections per IP. | FACT OAuth docs exist — [Acuity](https://developers.acuityscheduling.com/docs/oauth2); FACT-2ND plan/limits — [Nango](https://nango.dev/docs/integrations/all/acuity-scheduling), [RapidDev](https://rapidevelopers.com/bubble-integrations/acuity-scheduling) |

### Inferences
- A product that depends on writing appointments cannot assume uniform coverage. A realistic v1 supports 2 to 4 systems with true two-way sync and falls back to "lead + booking link + webhook/Zapier" for the rest.
- Per-customer gating (Zenoti, Vagaro, PatientNow, AestheticsPro) means each sale carries an onboarding step that depends on the spa asking its own vendor for keys, sometimes at extra monthly cost to the spa ($10 to $50/mo reported). That lengthens time-to-value.
- Boulevard gating to Enterprise (if confirmed) would exclude most single-location independents on Boulevard from a third-party integration.
- Unofficial routes exist as a category (Supergood sells exactly this), which signals both demand and terms-of-service/fragility risk. LAWYER: review each platform's ToS before any unofficial access.

### Gaps
- No vendor's partner agreement, revenue-share or marketplace listing fee was found for any of the 15.
- Boulevard, Zenoti and Vagaro portals could not be read directly; object-level capability (availability read, appointment create/modify, client create) is unconfirmed for all platforms except Square.
- Moxie (joinmoxie.com) API status unknown.
- Marketplaces/partner directories of Zenoti, Boulevard and Mangomint as distribution channels: not researched.

---

## A2. Meta Lead Ads, Instagram messaging, Google Ads lead forms, Google Business Profile messaging/calls

### Takeaway
Meta lead retrieval and Instagram DMs are technically accessible but require Business Verification plus App Review for Advanced Access; Google Ads lead forms can be received by a simple webhook with a shared key and no API token. Google Business Profile chat and call history were permanently removed on July 31, 2024, so that channel does not exist.

### Cited Findings
- FACT: Meta requires Business Verification for any app requesting Advanced Access — [Meta permissions reference](https://developers.facebook.com/docs/permissions), [Meta access levels](https://developers.facebook.com/documentation/development/graph-api/overview/access-levels).
- FACT: `leads_retrieval` is among the permissions subject to a separate "access verification" for apps that use other businesses' data to provide them a service (tech providers); it is independent of App Review — [Meta access verification](https://developers.facebook.com/docs/development/release/access-verification/).
- FACT: To request Advanced Access the app must have made at least 1 successful API call with each permission within 30 days before submitting — [Meta App Review docs](https://developers.facebook.com/documentation/resp-plat-initiatives/individual-processes/app-review/submission-guide).
- FACT: Instagram/Messenger standard messaging window is 24 hours after the user's message; the Human Agent feature (`human_agent` tag) allows a person to reply within 7 days and must be requested in App Review, intended only where a custom inbox handles escalations — [Meta Human Agent feature](https://developers.facebook.com/documentation/development/features-reference/human-agent), [Messenger Platform and IG Messaging policy](https://developers.facebook.com/documentation/business-messaging/messenger-platform/policy).
- FACT: Google Ads lead form webhook: Google POSTs JSON including a `google_key` to validate against the key configured in Google Ads; dedupe on `lead_id`; parse leniently; webhook URL up to 2048 characters; one schema for Search and YouTube/Discovery — [Google Ads webhook implementation](https://developers.google.com/google-ads/webhook/docs/implementation).
- FACT: If the webhook fails, leads remain downloadable as CSV for 30 days; exporting lead form data via the Google Ads API requires a developer token — [Google Ads Help](https://support.google.com/google-ads/answer/12080108).
- FACT: Google removed chat and call history from Business Profiles on July 31, 2024 (new chats stopped July 15, 2024); the `BUSINESS_CONVERSATIONS` metric is gone from the Performance API — [Google Business Profile Help](https://support.google.com/business/answer/14919056); Business Messages API shutdown — [Google developers notice](https://developers.google.com/business-communications/business-messages/resources/release-notes/update-on-gbm).

### Inferences
- Plan for Meta approval as a multi-step gate (business verification, access verification as a tech provider, App Review per permission). No official turnaround time was found.
- An AI auto-reply on Instagram DMs must operate inside the 24-hour window; the 7-day tag is for humans.
- Google "messaging" has to be replaced by call tracking numbers and website chat/SMS capture.

### Gaps
- Exact permission set for Lead Ads webhooks (e.g., pages_manage_ads, pages_show_list, ads_management) and current Lead Ads/IG messaging rate limits were not retrieved from Meta docs.
- Google Ads API developer-token access level needed for lead export, and Google Business Profile API access-request process, not found.
- Google Local Services Ads lead API not researched.

---

## B1. A2P 10DLC registration, fees, timelines; Twilio/Telnyx/Bandwidth list prices

### Takeaway
Registration cost per spa is small (about $20 to $61 one-time and $1.50 to $10 per month per campaign) and message cost is roughly 0.85 to 1.3 cents per outbound segment including carrier fees; the real exposure is approval friction and T-Mobile non-compliance fines of up to $10,000 per violation.

### Cited Findings
10DLC registration (per brand = per spa):
- FACT: Brand registration $4.50 one-time; campaign review (vetting) $15 per review, and campaigns may be re-reviewed on resubmission — [Telnyx 10DLC fees](https://support.telnyx.com/en/articles/5634625-10dlc-fees-and-charges).
- FACT: Monthly campaign fees (TCR schedule dated 7/22/2025): standard use cases incl. marketing, mixed, customer care, account notifications $10; low-volume mixed $1.50; sole proprietor $2; agents and franchises $30; charity $3; emergency $5. Billed three months upfront, then monthly — [Telnyx 10DLC fees](https://support.telnyx.com/en/articles/5634625-10dlc-fees-and-charges).
- FACT: T-Mobile pass-through: number pool request (50+ numbers per brand) $50 one-time; high-volume review (>200,000 messages/day) $5,000, currently waived. Fines: $10,000 per violation for text-enabling a number before ownership verification and for third-or-later content violations; $1,000 for long-code program evasion; $2,000 fraud; $500 to $1,000 illegal content/SHAFT — [Telnyx 10DLC fees](https://support.telnyx.com/en/articles/5634625-10dlc-fees-and-charges).
- FACT-2ND: Twilio's schedule: Sole Proprietor brand $4.50 one-time; Standard brand $46 one-time (includes secondary vetting); $15 per campaign vetting; campaign $2/mo (sole prop) or $10/mo (standard). TCR raised brand fee from $4.00 to $4.50 effective August 1, 2025; monthly campaign fees unchanged. Twilio's help article returned 403 to direct fetch — reported via search of [Twilio support article](https://support.twilio.com/hc/en-us/articles/1260803965530) and [Vonage notice](https://api.support.vonage.com/hc/en-us/articles/5702346174620-Key-Dates-Suppliers-Third-Party).
- FACT-2ND: Bandwidth lists low-volume campaigns at $1.50/campaign/month; its page showed brand registration at $4 as of February 2026 (conflicts with $4.50 elsewhere) — [Bandwidth 10DLC guide](https://www.bandwidth.com/blog/how-to-register-with-10dlc-to-avoid-unnecessary-costs-in-2022/).

Twilio list prices (pay-as-you-go, US):
- FACT: SMS $0.0083 per segment outbound and inbound (long code, toll-free, short code); MMS $0.022 out / $0.0165 in (long code). Long-code carrier fees per SMS: AT&T $0.0035 out/in; T-Mobile $0.0045 out, $0.0025 in; Verizon $0.005 out; US Cellular $0.005 out; others $0.0042 out. MMS carrier fees $0.007 to $0.01. Failed-message fee $0.001. Long code $1.15/mo; toll-free $2.15/mo; random short code $1,000/mo billed quarterly. Compliance Toolkit $0.015 per outbound SMS — [Twilio US SMS pricing](https://www.twilio.com/en-us/sms/pricing/us).
- FACT: Voice: local outbound $0.0140/min; local inbound $0.0085/min; toll-free inbound $0.0220/min; recording $0.0025/min, storage $0.0005/min/month, transcription $0.05/min; Media Streams $0.0044/min; ConversationRelay $0.07/min; SIP $0.0040/min — [Twilio US voice pricing](https://www.twilio.com/en-us/voice/pricing/us).

Telnyx list prices:
- FACT: 10DLC SMS $0.004 per part + carrier fee, outbound and inbound; MMS $0.015 out / $0.005 in + carrier fee; toll-free SMS $0.0055 + carrier fee. Carrier fees: AT&T $0.0035, T-Mobile $0.0045 out / $0.0025 in, Verizon $0.0045 out, US Cellular $0.005 out. Numbers $1.00/number/month (from a summary block on the page, not the full numbers rate card) — [Telnyx messaging pricing](https://telnyx.com/pricing/messaging).

Bandwidth list prices:
- FACT: Outbound SMS $0.004 (10DLC), $0.007 (toll-free), $0.008 (short code); MMS $0.015 (10DLC); voice outbound $0.0100/min, inbound $0.0055/min. Inbound SMS, number rental and carrier surcharges not listed; rest is quote-based — [Bandwidth pricing](https://www.bandwidth.com/pricing/).

### Inferences
- ESTIMATE: all-in outbound SMS segment is about $0.0118 to $0.0133 on Twilio and about $0.0075 to $0.009 on Telnyx (base + AT&T/T-Mobile/Verizon carrier fee).
- Each spa needs its own brand and campaign (the ISV registers on the spa's behalf using the spa's EIN and opt-in evidence). Standard-brand one-time cost on Twilio is about $61 ($46 + $15); a low-volume/sole-prop path is about $19.50.
- Med spa content (injectables, weight-loss drugs such as GLP-1s) sits close to carrier restricted-content categories; rejected campaigns cost another $15 per re-review. Not verified against a carrier content policy in this session.

### Gaps
- Approval timelines for brand and campaign vetting: no primary source retrieved.
- Twilio's own 10DLC fee table could not be fetched (403); figures above are via search summary.
- Toll-free verification requirements and timelines not researched. RCS business messaging requirements not researched (Twilio lists RCS at $0.0083/segment + carrier fee).
- Volume-discount tiers omitted.

---

## B2. TCPA, AI voice, consent rules, state mini-TCPAs

### Takeaway
AI voices are "artificial or prerecorded" under the TCPA (FCC, Feb 2024), so outbound AI calls to cell phones need prior express consent, and prior express written consent if they are marketing. The one-to-one consent rule is dead (vacated Jan 24, 2025). Revocation rules were rewritten by FCC 26-67 (adopted Sept 30, 2026) and the effective date is not settled in the sources. LAWYER review is essential before launch.

### Cited Findings
- FACT: FCC Declaratory Ruling adopted Feb 8, 2024 holds that AI-generated voices are "artificial or prerecorded voice" under the TCPA and 47 CFR 64.1200 — [FCC](https://www.fcc.gov/document/fcc-makes-ai-generated-voices-robocalls-illegal).
- FACT: FCC NPRM (Federal Register Sept 10, 2024) proposes defining "AI-generated call", requiring specific consent and an in-call AI disclosure. Proposed only; finalization not confirmed — [Federal Register](https://www.federalregister.gov/documents/2024/09/10/2024-19028/implications-of-artificial-intelligence-technologies-on-protecting-consumers-from-unwanted-robocalls).
- FACT-2ND (unverified): one vendor blog cites a June 5, 2026 FCC declaratory ruling on AI calls; no primary source found — [dev.to post](https://dev.to/alfredo_romero_fc4afdcb68/tcpa-2026-the-new-compliance-rules-every-ai-voice-agency-must-follow-1a4).
- FACT-2ND: The Eleventh Circuit vacated the FCC one-to-one consent rule on Jan 24, 2025 (Insurance Marketing Coalition v. FCC), the same day the FCC had postponed it — [National Law Review](https://natlawreview.com/article/eleventh-circuit-vacates-tcpa-one-one-consent-rule-immediately-after-fcc-postpones), [McGuireWoods](https://www.mcguirewoods.com/client-resources/alerts/2025/1/delayed-one-to-one-consent-rule-gives-companies-reprieve-plus-other-tcpa-updates/).
- FACT-2ND: Revocation-of-consent rules (revoke by any reasonable means; honor within 10 business days) took effect April 11, 2025, except the "revoke-all" provision, which was waived to April 11, 2026 and then to January 31, 2027 — search summary of law-firm sources incl. [Cullen and Dykman](https://www.cullenllp.com/blog/fcc-substantially-revises-tcpa-consent-revocation-rules-set-to-take-effect-january-2027/).
- FACT: FCC 26-67 (Report and Order + FNPRM) adopted Sept 30, 2026, released Oct 1, 2026 — [FCC order text](https://docs.fcc.gov/public/attachments/FCC-26-67A1.txt).
- FACT-2ND: FCC 26-67 (a) lets a caller treat a revocation in reply to an informational message as covering only that category of informational messages; (b) leaves telemarketing unchanged, so a marketing opt-out still covers all future marketing from that caller; (c) lets callers designate an exclusive revocation method, otherwise "any reasonable means" still applies. Effective-date sources conflict: 30 days after Federal Register publication "which has not yet occurred" vs published Oct 26, 2026 — [Nixon Peabody](https://www.nixonpeabody.com/insights/alerts/2026/10/07/fcc-scraps-revoke-all-and-lets-businesses-pick-how-consumers-opt-out), [Nelson Mullins](https://www.nelsonmullins.com/insights/alerts/fcc-download/all/fcc-adopts-overhaul-of-tcpa-consent-revocation-rules-revoke-all-narrowed-exclusive-opt-out-methods-permitted-and-fraud-alert-exemption-expanded), [Day Pitney](https://www.daypitney.com/the-fcc-changes-certain-consent-revocation-rules), [Crowell](https://www.crowell.com/en/insights/client-alerts/fcc-officially-adopts-amendments-to-tcpa-rules).
- FACT-2ND: Texas SB 140 (effective Sept 1, 2025) extends "telephone solicitation" in Bus. & Com. Code ch. 302 to text/graphic/image messages. Chapter 302 requires registration ($200 fee), a $10,000 security bond and quarterly reports; violations actionable via the Texas DTPA. A November 2025 settlement in litigation by text marketers means consent-based marketing texts are exempt from ch. 302 registration/bond/reporting; No-Call list rules still apply. Quiet-hours start (8 a.m. vs 9 a.m.) is stated inconsistently — [Paul Hastings](https://www.paulhastings.com/insights/ph-privacy/marketing-texts-in-texas-sb-140-broadens-state-telemarketing-regulations), [Varnum](https://www.varnumlaw.com/insights/texas-sb-140/), [Kelley Drye](https://www.kelleydrye.com/viewpoints/blogs/ad-law-access/texas-mini-tcpa-law-faqs-for-marketing-texts), [National Law Review](https://natlawreview.com/article/texas-sb-140-and-text-marketing-what-state-just-told-court-and-what-it-means-your).
- FACT-2ND: Florida FTSA as amended by HB 761 (signed May 2023): autodialer definition narrowed to systems that both select and dial; for text claims the consumer must first reply "STOP" and the sender has 15 days to cease before suit. Courts split on retroactivity — [Greenberg Traurig](https://www.gtlaw.com/en/insights/2023/5/florida-legislature-passes-bill-that-would-narrow-liability-under-florida-telephone-solicitation-act), [ABA](https://www.americanbar.org/groups/litigation/resources/newsletters/consumer/summer2024-federal-state-courts-diverge-retroactivity-standing-floridas-telephone-solicitation-act/).
- FACT: Washington ESHB 1051 became law in 2023 (C 103 L 23) and concerns robocalls/automatic dialing and announcing devices, not texts. A separate bill, HB 1103 (2025-26), would bar texts to Washington numbers on the do-not-call registry; its passage was not confirmed — [WA Legislature HB 1051 session law](https://lawfilesext.leg.wa.gov/biennium/2023-24/Pdf/Bills/Session%20Laws/House/1051-S.sl.pdf), [HB 1103 bill analysis](https://lawfilesext.leg.wa.gov/biennium/2025-26/Htm/Bill%20Reports/House/1103%20HBA%20CPB%2025.htm).

### Inferences
- Inbound AI receptionist calls (the consumer dials the spa) are not the TCPA's outbound target; the risk concentrates in outbound AI callbacks to web/ad leads and automated marketing texts. A Meta/Google lead form that names the spa and includes clear written consent language for automated/AI calls and texts is the practical control. LAWYER to draft the consent language.
- Speed-to-lead texting of a fresh ad lead is defensible only if the form captured consent; reactivation blasts to old client lists are the highest-risk use.
- Product must enforce per-state quiet hours, STOP handling across channels, and a consent record per contact. Treat the telemarketing opt-out as global.
- Because the spa is the "seller" and the SaaS is the platform that initiates messages, both can be named in suits; contract indemnities and E&O coverage matter.

### Gaps
- Oklahoma Telephone Solicitation Act: nothing retrieved. Not verified.
- Washington: status of HB 1103 and any CEMA (commercial electronic mail/text) rulings not verified. The brief's "Washington HB 1051" reference appears to concern robocalls, not texts.
- Whether the Sept 2024 AI-call NPRM was finalized, and the FCC 26-67 effective date, are unresolved.
- Federal quiet hours, DNC registry scrub duties, and other states (e.g., Maryland, Virginia, Connecticut) not researched.

---

## B3. HIPAA, BAAs, FTC HBNR, Washington MHMDA, tracking tech

### Takeaway
Whether a given med spa is a HIPAA covered entity is disputed in the sources and fact-specific, so the safe design assumption is that the product is a business associate for at least some customers and needs BAAs up and down the chain. BAA availability is mostly an enterprise-tier feature at voice-AI vendors, which sets a fixed cost floor.

### Cited Findings
- FACT: HHS: a software vendor is not a business associate merely by selling software if it has no access to PHI; an entity that creates, receives, maintains or transmits PHI on behalf of a covered entity is — [HHS business associate FAQs](https://www.hhs.gov/hipaa/for-professionals/faq/Business-Associates/index.html).
- FACT-2ND, conflicting: A med spa is a covered entity when it is a health care provider that transmits health information electronically in connection with HIPAA standard transactions (claims, eligibility). Some commentators say a cash-only spa may fall outside; others say e-prescribing or a diagnosing/prescribing clinician brings it in. State law may impose similar duties regardless — [HIPAA Journal](https://www.hipaajournal.com/hipaa-compliance-for-medical-spas/), [Paubox](https://www.paubox.com/blog/hipaa-compliance-for-wellness-retreats-and-medical-spas), [Accountable](https://www.accountablehq.com/post/hipaa-compliance-checklist-for-medical-spas-and-aesthetic-injector-practices). LAWYER.
- FACT: Twilio requires Security Edition or Enterprise Edition to sign a BAA; only listed HIPAA-eligible products are covered; contact sales — [Twilio HIPAA](https://www.twilio.com/en-us/hipaa), [Twilio HIPAA accounts doc](https://www.twilio.com/docs/iam/twilio-editions/hippa). Edition price not published.
- FACT: AWS BAA is self-service in AWS Artifact with no additional fee; PHI only on HIPAA-eligible services in accounts designated as HIPAA accounts — [AWS blog](https://aws.amazon.com/blogs/security/introducing-the-self-service-business-associate-addendum), [AWS HIPAA eligible services](https://aws.amazon.com/compliance/hipaa-eligible-services-reference/).
- FACT: Microsoft: HIPAA BAA is included by default via the Product Terms for covered entities/business associates; no separate contract — [Microsoft Learn](https://learn.microsoft.com/azure/compliance/offerings/offering-hipaa-us).
- FACT: Google Cloud supports HIPAA under a BAA, same pricing as other customers; arranged via account manager (page does not state a BAA fee) — [Google Cloud HIPAA](https://docs.cloud.google.com/docs/security/compliance/hipaa).
- FACT: OpenAI API: PHI requires an executed BAA and Modified Retention provisioning; an enterprise agreement is not required; request via baa@openai.com or self-serve with established usage history — [OpenAI help](https://help.openai.com/en/articles/8660679).
- FACT-2ND: Anthropic: BAA available on commercial/API agreements and Claude for Enterprise; not on Free/Pro/Max; some features out of scope — [Paubox toolkit](https://www.paubox.com/hubfs/gated-assets/ai-healthcare-toolkit/ai-healthcare-hipaa-toolkit.pdf), [dev.to](https://dev.to/jvancedev/which-ai-tools-will-sign-a-hipaa-baa-in-2026-and-the-we-pay-for-it-trap-8lg). Anthropic's own page not read.
- FACT-2ND: Deepgram BAA "on request" for qualifying customers; plan tier unconfirmed — [dev.to](https://dev.to/jvancedev/which-ai-tools-will-sign-a-hipaa-baa-in-2026-and-the-we-pay-for-it-trap-8lg).
- FACT: ElevenLabs: Enterprise plan includes BAAs for HIPAA customers; self-serve tiers ($6 to $990/mo) not stated to include one — [ElevenLabs API pricing](https://elevenlabs.io/pricing/api).
- FACT: Vapi: HIPAA is a paid, organization-wide add-on (Usage-only plan or any Success Package); BAA sent from the dashboard; only HIPAA-compliant providers selectable; mutually exclusive with Zero Data Retention; price not on the docs page — [Vapi HIPAA docs](https://docs.vapi.ai/security-and-privacy/hipaa).
- FACT-2ND, conflicting: Vapi HIPAA add-on $2,000/mo and ZDR $1,000/mo in most 2026 sources; older sources say $1,000/mo. vapi.ai/pricing returned 403 — [usagepricing.com](https://usagepricing.com/blueprint/vapi), [Emitrr](https://emitrr.com/blog/vapi-pricing/).
- FACT: Retell: HIPAA/BAA and custom BAA appear as plan features; Enterprise described as "HIPAA-ready"; no separate HIPAA price listed; which plan column carries the BAA was not clear from the page text — [Retell pricing](https://www.retellai.com/pricing).
- FACT: Bland: BAA not included on Start or Build; included on Enterprise (custom price) — [Bland pricing](https://www.bland.ai/pricing).
- FACT: FTC Health Breach Notification Rule amendments effective July 29, 2024 make the rule applicable to health apps and similar technologies not covered by HIPAA; the rule does not apply to HIPAA-covered businesses — [Federal Register](https://www.federalregister.gov/documents/2024/05/30/2024-10855/health-breach-notification-rule), [FTC guidance](https://www.ftc.gov/business-guidance/resources/complying-ftcs-health-breach-notification-rule-0).
- FACT-2ND: Washington My Health My Data Act covers "consumer health data" outside HIPAA, including data of non-residents collected in Washington; any violation is actionable under the Consumer Protection Act (private right of action). Remedy descriptions vary (actual damages; treble up to $25,000) — [IAPP](https://iapp.org/resources/article/washington-my-health-my-data-act-overview), [BakerHostetler](https://www.bakerlaw.com/insights/examining-the-private-right-of-action-in-washingtons-my-health-my-data-act), [DWT tracker](https://www.dwt.com/gcp/state-privacy-laws-tracker/broad-state-privacy-law-tracker/washington).
- FACT-2ND: HHS OCR tracking-technology bulletin: on June 20, 2024 the N.D. Tex. vacated the part treating IP address + visit to an unauthenticated public health page as PHI (AHA v. Becerra); HHS dropped its appeal (Aug 2024); remaining guidance stands. Nothing newer than late 2024 found — [AHA](https://www.aha.org/news/headline/2024-08-29-hhs-will-not-appeal-aha-court-victory-online-tracking-case), [Holland & Knight](https://www.hklaw.com/en/insights/publications/2024/06/american-hospital-assn-v-becerra-are-tracking-tools-ok-again).

### Inferences
- A lead record such as "Jane Doe, phone, interested in Botox/semaglutide consult at Spa X" is health-related information tied to a named person. If the spa is a covered entity, the tool that receives and stores it on the spa's behalf fits the HHS business-associate definition. If the spa is not a covered entity, the same data likely falls under FTC HBNR/FTC Act and state laws such as MHMDA instead. Either way it is regulated; the regime differs. LAWYER.
- Syncing with the spa's EMR (appointments, treatment types) moves the product firmly into PHI handling.
- Sending lead events back to Meta/Google (Conversions API, offline conversions) for a health service is the highest-risk data flow under MHMDA and FTC enforcement, independent of the vacated OCR bulletin.
- BAA chain for a voice product: telephony (Twilio Security/Enterprise Edition) + voice platform (Vapi add-on or Retell/Bland/ElevenLabs enterprise) + LLM (OpenAI/Anthropic BAA) + STT/TTS + cloud (free on AWS/Azure). The fixed cost is driven by the telephony and voice-platform tiers.

### Gaps
- Twilio Security/Enterprise Edition price; Telnyx and Bandwidth BAA policies; Retell's exact BAA tier; Deepgram and Anthropic primary pages; Vapi HIPAA price on a primary page.
- SMS is unencrypted; whether appointment-reminder and marketing texts fit HIPAA treatment/marketing rules for a given spa was not researched. LAWYER.
- Other state health-data laws (e.g., Nevada SB 370, Connecticut) not researched.

---

## B4. Call recording consent for AI receptionists

### Takeaway
All-party-consent states require a recording disclosure at minimum, and California wiretap (CIPA) suits now target AI voice vendors as third-party interceptors, so a generic "this call may be recorded" line may not be enough; disclose the AI and the vendor's role. I did not find an authoritative current state list.

### Cited Findings
- FACT-2ND: A Jan 2026 Bloomberg Law piece lists California, Florida, Illinois, Maryland, Massachusetts, Montana, New Hampshire, Pennsylvania and Washington as all-party-consent states; the same list is internally inconsistent about Washington, so verify against statutes — [Bloomberg Law](https://news.bloomberglaw.com/ip-law/ai-notetaking-poses-wiretapping-discovery-and-ethical-pitfalls).
- FACT-2ND: CIPA sections 631/632 claims have been brought over an AI voice assistant answering consumer calls (Domino's ordering assistant) and over an AI vendor (Cresta) recording/transcribing/analyzing calls; plaintiffs argue a generic monitoring notice does not disclose third-party AI use. In the Otter.ai case the court treated the vendor's capability to use data for its own purposes as sufficient to implicate CIPA — [Fisher Phillips](https://www.fisherphillips.com/en/insights/insights/ai-call-monitoring-lawsuits-are-heating-up), [Epstein Becker Green](https://www.ebglaw.com/insights/publications/eavesdropping-by-algorithm-how-courts-are-applying-decades-old-privacy-laws-to-ai), [Paul Hastings](https://www.paulhastings.com/insights/ph-privacy/ai-transcription-tools-when-a-robot-is-listening-courts-may-find-it-is-wiretapping).
- FACT-2ND: Defense wins exist: Lisota v. Heartland Dental (N.D. Ill., Jan 2026); Thele v. Google dismissed for lack of standing (July 2026). Chatbot wiretap filings rose from 2 in 2021 to 30 in 2025 per a Baker Botts review — same sources as above and [Stacker](https://stacker.com/stories/ai/chatbot-privacy-lawsuits-ai-wiretapping-claims-and-legal-fight-over-customer).

### Inferences
- Default product behavior should be an opening disclosure on every call: AI assistant, call recorded/transcribed, on behalf of the spa. Contractually bar sub-processors from using call audio for their own model training (the "capability" theory). LAWYER.

### Gaps
- No statute-verified state list; no state AI-disclosure ("bot disclosure") laws researched (e.g., California, Utah).

---

## C1. Per-unit operating costs

### Takeaway
Variable costs are low and well documented (about 1 cent per SMS segment, 7 to 14 cents per AI voice minute). Fixed compliance costs (HIPAA tiers, SOC 2 tooling and audit, insurance) are the larger and less transparent items.

### Cited Findings
- FACT: SMS, MMS, voice minute and number prices for Twilio, Telnyx, Bandwidth — see B1 (URLs there).
- FACT: Retell pay-as-you-go: voice infra $0.055/min; TTS $0.015/min (platform voices, Cartesia, OpenAI and others) or $0.040/min (ElevenLabs Flash) up to $0.10/min; LLM per minute e.g. Claude 5.5 Haiku $0.0032, GPT 6.1 Terra $0.032, Claude 5.5 Sonnet $0.064; telephony $0.015/min (none for own SIP); overall $0.07 to $0.31/min; 20 concurrent calls included, extra $8 per concurrent call per month; number $2.00/mo; branded caller ID +$0.10 per outbound call — [Retell pricing](https://www.retellai.com/pricing).
- FACT: Bland: Start $0 platform, $0.14/min, transfer $0.05/min, 10 concurrent, 100 calls/day; Build $299/mo, $0.12/min, transfer $0.04/min, 50 concurrent, 2,000 calls/day; Enterprise custom with BAA; telephony billed separately — [Bland pricing](https://www.bland.ai/pricing).
- FACT: ElevenLabs Agents: Speech Engine $0.08/min (burst $0.16/min); TTS $0.04 to $0.08 per 1K characters; plans $0, $6, $22, $99, $299, $990/mo, Enterprise custom — [ElevenLabs API pricing](https://elevenlabs.io/pricing/api).
- FACT-2ND: Vapi platform fee $0.05/min plus at-cost pass-through of STT/LLM/TTS/telephony; HIPAA add-on $2,000/mo (conflict with $1,000/mo in older sources). Primary pricing page blocked — [Vapi docs: pricing and success packages](https://docs.vapi.ai/billing/pricing-and-success-packages), [usagepricing.com](https://usagepricing.com/blueprint/vapi).
- FACT: Twilio ConversationRelay (build-your-own voice agent) $0.07/min; Media Streams $0.0044/min — [Twilio voice pricing](https://www.twilio.com/en-us/voice/pricing/us).
- FACT: Anthropic API list prices per million tokens (input / output): Claude Haiku 5.5 $0.10 / $0.50 (prompts up to 100K tokens); Claude Sonnet 5.5 $2 / $10 (cache hits $0.10); Claude Opus 5.5 $4 / $20 — [Anthropic pricing](https://platform.claude.com/docs/en/about-claude/pricing).
- FACT: AWS and Azure BAAs carry no extra fee; Google Cloud HIPAA at standard pricing — see B3.
- FACT-2ND (third-party estimates; vendors do not publish): Vanta about $7,500 to $30,000+/yr or from about $10,000/yr SOC 2 only; Drata startup tier $7,500 to $15,000/yr, marketplace listing from $8,700 platform + $5,800 audit subscription; a SOC 2 Type II audit example about $12,000 from a CPA partner; first-year lean SOC 2 Type 1 budget $15,000 to $40,000 all-in — [UnderDefense on Vanta](https://underdefense.com/blog/vanta-pricing/), [UnderDefense on Drata](https://underdefense.com/blog/drata-pricing/), [soc2auditors.org](https://soc2auditors.org/insights/soc-2-compliance-for-startups/).
- FACT-2ND: Insurance: early-stage package with $1M limits across GL + tech E&O + cyber about $2,000 to $4,000/yr (Corgi); cyber alone for 1 to 50 employees $1,000 to $5,000/yr; SaaS-startup E&O average $929/yr (limit unstated) — [Corgi](https://www.corgi.insure/blog/startup-insurance-cost-by-stage), [MoneyGeek](https://www.moneygeek.com/insurance/business/tech-it/saas/), [Secureframe](https://secureframe.com/blog/cyber-insurance-costs.md).

### Inferences
- ESTIMATE: Retell all-in voice minute = $0.055 + $0.015 + $0.0032 + $0.015 = $0.088 (cheapest listed stack) to $0.055 + $0.040 + $0.032 + $0.015 = $0.142 (ElevenLabs Flash voice, mid LLM).
- ESTIMATE: insurers will likely price health-data handling and TCPA exposure above generic SaaS; the ranges above are generic startup figures, not quotes for this risk profile.

### Gaps
- OpenAI and Google LLM list prices, standalone STT prices (e.g., Deepgram), email-sending prices (e.g., Amazon SES), and HIPAA-eligible hosting cost for a small production stack were not retrieved. No verified figure.
- HIPAA-specific add-on price at Vanta/Drata; penetration-test cost; legal budget for TCPA/HIPAA counsel: not found.

---

## C2. Rough cost-to-serve per med spa per month

### Takeaway
ESTIMATE: at 300 leads, 1,500 outbound SMS segments and 400 AI voice minutes, variable cost-to-serve is roughly $56 to $112 per spa per month before fixed compliance overhead; fixed HIPAA/SOC 2/insurance overhead plausibly adds tens of dollars per customer until the base reaches the low hundreds of customers.

### Cited Findings (inputs; all list prices cited in B1 and C1)
ASSUMPTIONS (mine, not sourced): 300 leads/mo; 1,500 outbound SMS segments; 500 inbound SMS segments; no MMS; 400 inbound AI voice minutes; 2 local numbers; 1 10DLC campaign; blended outbound carrier fee $0.0045 and inbound $0.0025 per segment; SMS conversation AI = 300 leads x 8 LLM calls x 3,000 input tokens + 150 output tokens = 7.2M input and 0.36M output tokens, no prompt caching; email and hosting excluded (no verified price).

| Line | Low-cost stack | Higher-cost stack |
|---|---|---|
| SMS out 1,500 | Telnyx 1,500 x ($0.004 + $0.0045) = $12.75 | Twilio 1,500 x ($0.0083 + $0.0045) = $19.20 |
| SMS in 500 | Telnyx 500 x ($0.004 + $0.0025) = $3.25 | Twilio 500 x ($0.0083 + $0.0025) = $5.40 |
| Voice 400 min (Retell) | 400 x $0.0882 = $35.28 | 400 x $0.142 = $56.80 |
| Numbers x2 | 2 x $1.00 = $2.00 | 2 x $1.15 = $2.30 |
| 10DLC campaign | low-volume mixed $1.50 | standard $10.00 |
| LLM for SMS | Haiku 5.5: 7.2 x $0.10 + 0.36 x $0.50 = $0.90 | Sonnet 5.5: 7.2 x $2 + 0.36 x $10 = $18.00 |
| Total variable | about $55.68 | about $111.70 |

One-time per spa: brand $4.50 + vetting $15 = $19.50 (Telnyx schedule) or about $61 with a $46 standard brand (Twilio schedule, FACT-2ND).

### Inferences
- ESTIMATE: at a $300 to $500/mo price point (see D3 comparables) variable gross margin would be roughly 63% to 89%, before support labor, which is typically the larger cost for SMB onboarding and was not modeled.
- ESTIMATE of fixed overhead, using FACT-2ND figures: Vapi HIPAA add-on $2,000/mo (if Vapi is used) + compliance platform about $10,000/yr + SOC 2 audit about $12,000/yr + insurance about $3,000/yr is about $4,080/mo, i.e. about $82 per customer at 50 customers, $20 at 200. Excludes Twilio Security/Enterprise Edition (price unknown) and legal.
- Voice minutes dominate. Doubling to 800 minutes adds $35 to $57; usage-based or minute-capped pricing protects margin (Boulevard caps its add-on at 200 minutes, see D3).

### Gaps
- Real usage per spa (minutes, messages per lead) is unverified; the brief's example volumes were used as given.
- Support/onboarding labor, payment processing, email, hosting, monitoring not included.

---

## D1. Vertical/SMB SaaS benchmarks

### Takeaway
The only primary benchmark retrieved is SaaS Capital's 2025 survey (median NRR 101%, GRR 91% across 1,000+ private B2B SaaS companies, retention rising with ACV); SMB-specific churn and CAC figures found are from low-quality aggregator pages and should be treated as directional only.

### Cited Findings
- FACT: SaaS Capital 2025 retention benchmarks (1,000+ private B2B SaaS companies): median net revenue retention 101%, median gross revenue retention 91%; higher ACV correlates with higher retention; $25K to $50K ACV band median NRR 102% (top quartile 111%, bottom 97%). Companies with NRR below 90% report a median ACV of $21,017 — [SaaS Capital](https://www.saas-capital.com/research/saas-retention-benchmarks-for-private-b2b-companies/), [SaaS Capital blog](https://www.saas-capital.com/blog-posts/what-is-a-good-retention-rate-for-a-private-saas-company/).
- FACT: ChartMogul guidance: with ARPA under $100/mo aim for monthly customer churn below 3.5%; over $100, below 2.5% (a target, undated); measured median monthly customer churn for ARPA under $25 is 6.1%. 2023 Retention Report (about 2,100 companies): 41.1% of businesses with ARPA over $500/mo have net retention over 100% vs 2.7% for ARPA under $10 — [ChartMogul churn page](https://chartmogul.com/lp/saas-churn), [ChartMogul blog](https://chartmogul.com/blog/good-customer-churn-rate/), [ChartMogul SaaS Retention Report](https://chartmogul.com/saas-retention-report/).
- FACT-2ND (weak sources, inconsistent segment definitions, 2026): SMB monthly logo churn about 3% to 7%; about 4.1% monthly in the $500 to $5,000 ACV band (about 39% annualized); CAC payback medians about 11 to 12 months for SMB and about 15 months for vertical SaaS; Benchmarkit 2026 median GRR 84% (different sample) — [unbuiltlab](https://unbuiltlab.com/learn/benchmarks/saas-cac-benchmarks), [knowledgelib](https://knowledgelib.io/finance/industry-benchmarks/saas-industry-benchmarks-2026/2026), [Phoenix Strategy Group](https://phoenixstrategy.group/blog/benchmarking-saas-kpis-industry-standards-2026).

### Inferences
- A $3.6K to $6K ACV product sits well below the ACV bands where SaaS Capital's medians apply; expect materially worse logo retention than 91% GRR. A planning range of 2.5% to 4% monthly logo churn is consistent with the ChartMogul target and the weak aggregator data. ESTIMATE.

### Gaps
- OpenView, Tidemark and a16z vertical-SaaS material: not retrieved. No sourced figures for typical CAC in dollars, sales cycle length, or vertical-SaaS-specific churn. SaaS Capital GRR by ACV band is in a PDF chart not read.

---

## D2. Channels to reach med spa owners

### Takeaway
AmSpa is the central association channel but publishes no exhibitor or vendor pricing; costs must be requested from sales. Most other channels in the brief could not be sourced in this session.

### Cited Findings
- FACT: AmSpa directs prospective Medical Spa Show exhibitors to sales@americanmedspa.org; no public rate sheet. The 2026 exhibit hall was described as sold out — [AmSpa](https://www.americanmedspa.org/news/rooted-in-partnership-exhibitors-show-up-and-show-out-at-medical-spa-show/).
- FACT-2ND: Medical Spa Show 2027 listed for April 15 to 18, 2027, Wynn Las Vegas (third-party listings; venue not confirmed by AmSpa) — [KokoQuest](https://www.kokoquest.com/tradeshows/medical-spa-show-2027), [Tradefest](https://tradefest.io/en/event/medical-spa-show).
- FACT: AmSpa has tiered vendor affiliates; Symplast joined as a "Platinum Vendor Affiliate" and offered a member deal — [AmSpa news](https://www.americanmedspa.org/news/symplast-joins-amspa-as-platinum-vendor-affiliate-offers-deal-for-members/).
- FACT-2ND: AmSpa 2026 practice membership "Plus" tier listed at $845 (member side, not vendor) — AmSpa 2026 membership rates page via search (https://www.americanmedspa.org/?p=19623).
- FACT-2ND: Agencies as a channel: GoHighLevel agency plans $97 / $297 / $497 per month; SaaS Mode (white-label resale with rebilling) on the $497 plan; AI Employee add-on $50 or $97 per sub-account per month — [Carly](https://www.usecarly.com/blog/gohighlevel-pricing/), [saascrmreview](https://saascrmreview.com/?p=18883). Official HighLevel page not read.

### Inferences
- Vendor-affiliate status with a member discount (the Symplast pattern) is the visible AmSpa playbook for software vendors.
- Med spa marketing agencies already hold the lead-gen budget and often run GoHighLevel; they are both the most efficient reseller channel and the most direct competitor.

### Gaps
- AmSpa booth and vendor-affiliate prices (unpublished). Facebook groups, podcasts, consultants, Allergan/Galderma practice-consulting programs, aesthetic reps/distributors, and booking-platform marketplaces: no reliable sources retrieved. The only Galderma ASPIRE reference found was a 2020 article about its rewards program.

---

## D3. How comparable tools price

### Takeaway
Published comparables cluster at a flat monthly fee per location: about $109 to $600/mo for AI receptionist/lead tools, with included-minute caps and overage; broader communication suites (Podium, Weave) run $249 to $599/mo on 12-month contracts. Incumbent booking platforms price their own AI front desk far lower as an add-on.

### Cited Findings
- FACT-2ND: Boulevard built-in AI receptionist ("Beau") $125/mo per location including 200 minutes, overage $0.60/min; Boulevard's own pricing page does not list it — [Futuro roundup](https://www.futurocorp.com/blogs/best-ai-receptionist-for-med-spas), [Storydrips comparison](https://storydrips.com/blog/ai-receptionist-for-med-spas-compared); absence on [Boulevard pricing](https://www.joinblvd.com/pricing) is FACT.
- FACT-2ND: Zenoti AI Receptionist requires its "AI Plus" package at custom pricing (one source says included in a platform starting about $400/mo; conflict). Mangomint AI receptionist requires its $70/mo Phone add-on — [Prospyr](https://prospyrmed.com/blog/post/med-spa-software-with-ai-receptionist), [Zenoti blog](https://www.zenoti.com/thecheckin/how-ai-receptionists-are-revolutionizing-appointment-management-for-wellness-brands).
- FACT-2ND: Independent med spa AI receptionists: typical $200 to $600/mo single location; MedspAI Starter $299/mo per location; Emitrr $149/mo flat; Wellgrow Scale $499/mo; AgentZap from $109/mo with per-minute model; AutoMeit $297/mo flat, no per-minute fees, no contract — [egma.ai guide](https://egma.ai/blog/ai-receptionist-for-med-spas-complete-guide/), [Futuro](https://www.futurocorp.com/blogs/best-ai-receptionist-for-med-spas), [AutoMeit pricing](https://automeit.ai/pricing/), [AgentZap](https://agentzap.ai/industries/med-spa).
- FACT-2ND: Podium Core $399/mo, Pro $599/mo, Signature quoted; AI Employee add-on priced on demo; 12-month contracts; setup fee negotiated — [eesel on Podium](https://www.eesel.ai/blog/podium-pricing) (cites Podium's pricing page), [Podium pricing](https://podium.com/pricing) (not fetched).
- FACT-2ND: Weave from about $199 to $249 per location per month (sources conflict), annual contract, setup about $500 to $750; higher bundles custom with 12 to 24 month terms — [Pabau on Weave](https://pabau.com/blog/weave-pricing/), [Capterra](https://www.capterra.com/p/141842/Weave/pricing/), [CostBench](https://www.costbench.com/software/business-phone/weave/).
- FACT: Boulevard platform itself: per-location flat fee, annual billing saves 10%, usage-based texting, email $0.01 after allowance — [Boulevard pricing](https://www.joinblvd.com/pricing).

### Inferences
- The market norm is flat per-location pricing with a usage cap; per-seat pricing did not appear in any comparable. Setup fees and annual contracts are common in the larger suites and absent in the smaller AI-receptionist vendors.
- An incumbent add-on at $70 to $125/mo sets a price anchor for "answering the phone"; a third-party tool must justify $300+ on lead-source capture, multi-channel follow-up and reporting the incumbent does not do.

### Gaps
- RepeatMD, Liine, Workee and other named med spa tools: no pricing found. Nearly all figures are from competitor or affiliate pages, not vendor price lists.

---

## D4. Major business risks

### Takeaway
The three structural risks are (1) dependence on booking platforms that gate APIs and now sell their own AI receptionist, (2) messaging/voice regulatory and carrier exposure, and (3) low-ACV SMB churn in a category where GoHighLevel agencies and many small vendors already sell similar bundles.

### Cited Findings
- Platform dependency: Boulevard API reported Enterprise-only; Zenoti keys customer-generated; Vagaro requires enterprise sales approval and payments enabled; Mangomint has no public API — URLs in A1.
- Incumbent bundling: Boulevard, Zenoti and Mangomint each market a native AI receptionist (FACT-2ND, URLs in D3).
- Carrier/deliverability: T-Mobile fines up to $10,000 per violation and $15 per campaign re-review (FACT, [Telnyx](https://support.telnyx.com/en/articles/5634625-10dlc-fees-and-charges)).
- Regulatory flux: one-to-one rule vacated 2025; revocation rules rewritten Sept 30, 2026 with FNPRM pending; AI-call NPRM outstanding; Texas SB 140 litigated and settled within months of taking effect; CIPA suits against AI voice vendors (URLs in B2, B4).
- Commoditization: GoHighLevel white-label SaaS Mode at $497/mo for an agency with AI Employee at $50 to $97 per sub-account (FACT-2ND, URLs in D2); many AI receptionist vendors at $109 to $499/mo (D3).
- Meta/Google dependency: Google removed Business Profile chat and call history outright in July 2024 (FACT, [Google](https://support.google.com/business/answer/14919056)); Meta access hinges on App Review and access verification (A2).

### Inferences
- The combination of gated APIs plus native AI add-ons suggests incumbents treat the front desk as their own expansion product; a third party's durable position is likely cross-platform (multi-location groups on mixed systems, agencies) or pre-booking (ad lead to booked consult), where the booking system has less data.
- SMB churn math (D1) plus $56 to $112 variable cost means payback depends mostly on CAC and onboarding labor, neither of which could be sourced.

### Gaps
- No data on med spa software churn specifically, nor on how often booking platforms have revoked third-party access.

---

## Not found / gaps (consolidated)

1. Partner-program terms, revenue share, marketplace fees for all 15 booking/EMR platforms; object-level API capability for all except Square; direct reads of Boulevard, Zenoti, Vagaro portals.
2. Moxie (joinmoxie.com) API: unverified; the help article found appears to belong to a different product named Moxie.
3. Meta Lead Ads webhook permission list and rate limits; Meta review turnaround; Google Ads API token level for lead export; Google Business Profile API access process; Local Services Ads.
4. 10DLC approval timelines; Twilio's own 10DLC fee page (403); toll-free verification; RCS; Bandwidth inbound/number/carrier fees.
5. Oklahoma Telephone Solicitation Act; Washington HB 1103 status and CEMA case law; FCC 26-67 effective date; whether the 2024 AI-call NPRM was finalized; the claimed June 5, 2026 FCC AI ruling (unverified).
6. Twilio Security/Enterprise Edition price; Vapi pricing page (403) and confirmed HIPAA add-on price ($2,000 vs $1,000 conflict); Retell BAA tier; Telnyx/Bandwidth/Deepgram/Anthropic BAA terms from primary pages.
7. Statute-verified list of all-party recording-consent states; state AI/bot disclosure laws.
8. OpenAI/Google LLM prices, STT prices, email prices, HIPAA-eligible hosting cost; Vanta/Drata official prices (not published); insurance quotes specific to health-data + TCPA exposure; legal budget.
9. OpenView, Tidemark, a16z vertical SaaS benchmarks; dollar CAC, sales cycle, vertical-specific churn; SaaS Capital GRR by ACV band.
10. AmSpa exhibitor and vendor-affiliate pricing (unpublished); Facebook groups, podcasts, consultants, Allergan/Galderma practice-consulting programs, distributors/reps, platform marketplaces as channels.
11. Pricing for RepeatMD, Liine, Workee; official pages for Podium, Weave, GoHighLevel, and the Boulevard/Zenoti/Mangomint AI add-ons.
12. Real per-spa usage data (leads, messages per lead, call minutes) to replace the stated assumptions in C2.
