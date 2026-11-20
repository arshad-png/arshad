# Competitor research: all-in-one practice management / booking / EMR platforms used by US medical spas

Access date for every URL below: **2026-11-20**. Market: US.

**Claim labels**
- **FACT** = taken from the vendor's own site, docs or press release (or a primary review page I could open).
- **THIRD-PARTY REPORTED** = from review aggregators, competitor blogs, comparison articles or search-result snippets; unverified.
- **ASSUMPTION** = my own inference.

**Method caveats (read first)**
- Pages were read through a fetch tool that summarises page content. Prices and plan names below are as that tool returned them from the official page; where the tool said it paraphrased feature wording, I say so. Dollar figures should be re-checked on the live page before being quoted in anything customer-facing.
- Capterra, Software Advice and G2 review pages returned HTTP 403 to direct fetches. Review quotes from those sites therefore come from search-result snippets and are labelled THIRD-PARTY REPORTED (snippet), not verified against the full review.
- No Reddit thread could be retrieved (three differently worded searches returned zero reddit.com results). There are **no Reddit or Facebook-group quotes** in these notes.
- A "Q-Site Medspa Survey" page (qsite-dashboard.pages.dev/emr.html) appeared in search results claiming 152 respondents and ~50% dissatisfaction among Aesthetic Record users, but the host is outside this session's allowed network domains and could not be opened; it is unverified and of unknown authorship.

---

## Per-product competitor profiles

### Takeaway
Seventeen platforms were profiled. Six publish full pricing (Mangomint, Boulevard, Vagaro, AestheticsPro, Aesthetic Record, GlossGenius, Jane, PocketSuite); the rest are partly or wholly "contact sales". Almost every vendor shipped or announced an AI receptionist in 2025-2026, but most are paid add-ons and several do not actually complete a booking or do not answer the phone.

### Cited Findings

#### 1. Zenoti — https://www.zenoti.com
- **Positioning:** FACT — press release line "This isn't AI added to software — it's a new kind of business infrastructure." — [Zenoti press, 28 Apr 2026](https://www.zenoti.com/press/zenoti-expands-its-ai-workforce-purpose-built-ai-agents-for-every-medspa-workflow)
- **Target customers:** FACT — "More than 11,000 medspas worldwide run on Zenoti"; pricing page says "Multi-location pricing is customized based on your footprint and needs." — [press](https://www.zenoti.com/press/zenoti-expands-its-ai-workforce-purpose-built-ai-agents-for-every-medspa-workflow), [pricing](https://www.zenoti.com/pricing). THIRD-PARTY REPORTED — described as an enterprise platform that "may be more than independent salons need" — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- **Core features:** FACT — Appointment book, POS, payments, Text2Pay, memberships & packages, gift cards, loyalty, online booking (Webstore), social booking, Reserve with Google, marketing automation, reputation management, AI phone line, abandoned-cart recovery, waitlist, BI — [pricing page](https://www.zenoti.com/pricing)
- **Lead / follow-up / AI:** FACT — AI Lead Manager "Collects leads from ads, calls, web, and text into one inbox, scores them by intent, and responds 'in under 90 seconds'" and follows up until the lead books; AI Receptionist "Answers every call the front desk misses, 24/7" and books/reschedules/upsells (vendor claim: converts 1 in 3 missed calls); AI Concierge monitors phone/SMS/web interactions; AI Retention Manager flags at-risk clients; AI Digital Marketer handles SEO, ads, listings, review responses — [press](https://www.zenoti.com/press/zenoti-expands-its-ai-workforce-purpose-built-ai-agents-for-every-medspa-workflow), [pricing](https://www.zenoti.com/pricing)
- **Pricing:** FACT — not public. Page wording: "Get a Quote", "Find the right plan for your business." AI agents require the "AI Plus package". Voice/SMS/messaging are billed by usage with optional base packs — [pricing](https://www.zenoti.com/pricing)
- **Pricing, third-party reported, unverified:** $300/mo starting (Software Advice listing); $300-$600/mo for med spas/salons; $350/$450/$500 per location per month (attributed to The Salon Business); $600/mo (attributed to an r/MedSpa thread, not opened by me); implementation $2,000-$5,000; add-ons per location per month: SMS $139, SMS+MMS $169, ezRepute Pro $189, Smart Bot $150-$400; SMS credits 5k/$180 — all via a competitor's blog — [Pabau blog, updated 6 Oct 2026](https://pabau.com/blog/zenoti-pricing/)
- **Strengths:** FACT — broadest AI agent line-up found, including a dedicated lead agent; documented public API including Leads (Opportunities) endpoints — [docs.zenoti.com](https://docs.zenoti.com/)
- **Weaknesses:** THIRD-PARTY REPORTED — "Pricing isn't transparent and can be expensive for smaller practices" — [PatientNow comparison](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives); "Entry plans cap teams under 10" — [AmSpa article authored by GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/)
- **Documented complaints:** THIRD-PARTY REPORTED (snippets/paraphrase, no verbatim quotes retrieved) — extra charges for add-ons, setup and ongoing features exceed expectations (Capterra summary); "high and unclear costs, problematic and disruptive updates, and payment integration challenges" (GetApp summary); glitchy desktop/mobile sync, slow and confusing setup/migration, navigation needing multiple tabs — [Pabau blog](https://pabau.com/blog/zenoti-pricing/). Ratings ~4.4/5 from ~1,250 Capterra reviews (snippet).
- **Integrations / API:** FACT — public API docs cover appointments (list, details, check-in, no-show), service bookings (create, reserve slot, confirm, reschedule), guests (create/search/update), Leads/Opportunities (create/retrieve/list/edit + notes), invoices, memberships; webhooks for guest, appointment, invoice, membership events; API key generated by creating a backend app in Zenoti; cost of API access not stated — [docs.zenoti.com](https://docs.zenoti.com/). FACT — Zapier listing exists — [Zapier](https://zapier.com/apps/webhook/integrations/zenoti). FACT — Spakinect (Good Faith Exams) integrates with Zenoti, Boulevard and Aesthetic Record — [AmSpa](https://www.americanmedspa.org/?p=21395)
- **Recent moves:** FACT — AI Workforce launched 30 Sep 2025; expanded for medspas 28 Apr 2026; fitness expansion 3 Feb 2026; Medvelle (inventory/procurement) partnership 29 Oct 2026 — [Zenoti press](https://www.zenoti.com/press)

#### 2. Boulevard — https://www.joinblvd.com
- **Positioning:** not found as a single tagline. FACT — medspa landing page: "Handle calls with our AI receptionist, add a personal touch with two-way texting, and streamline follow-up with automated reminders." — [Boulevard](https://www.joinblvd.com/lp/grow-your-medspa)
- **Target customers:** FACT — Essentials "for small teams with simple operations at one location" (up to 5 providers); Premier/Prestige per location; Enterprise custom — [pricing](https://www.joinblvd.com/pricing)
- **Core features:** FACT — scheduling, payments, online booking, two-way texting, automated reminders, AI-assisted email marketing ("Boulevard Marketing uses AI to suggest subject lines, email copy, and even generate custom imagery"), forms/charting add-on, ePrescribe add-on, reporting — [medspa page](https://www.joinblvd.com/lp/grow-your-medspa), [pricing](https://www.joinblvd.com/pricing)
- **Lead / follow-up / AI:** FACT — AI receptionist "Beau" answers calls 24/7, filters spam, answers routine questions, **sends an appointment link** rather than booking in-call, and for medspas captures caller name, contact info and interest and passes it to staff; interactions land in the same inbox used for client texting. The page does not describe Beau sending/receiving texts. No dedicated lead pipeline or "lead management" feature is named on the medspa page — [Beau page](https://www.joinblvd.com/features/ai-receptionist), [medspa page](https://www.joinblvd.com/lp/grow-your-medspa)
- **Pricing (official, monthly; annual saves 10%):** FACT — Essentials **$143/mo** for 1 location (up to 5 providers, 250 free texts, 1,000 free email blasts); Premier **$234/mo per location** ("normally $293", limited-time fall pricing for new customers); Prestige **$328/mo per location** ("normally $410"; includes Forms add-on, 2,500 texts, 10,000 email blasts); Enterprise custom. Add-ons: Messages & Text Marketing "pay based on texts sent and received"; Automated Campaigns "Free to send; pay only for results"; email blasts $0.01 each beyond allowance; Forms from $65/mo per location; QuickBooks $45/mo per location; ePrescribe $45 per prescriber — [pricing](https://www.joinblvd.com/pricing) (tool noted feature wording was paraphrased). Beau: **$149/month per location including 100 minutes, $0.50/minute after** — [Beau page](https://www.joinblvd.com/features/ai-receptionist)
- **Pricing, third-party reported, unverified:** campaigns "$2 per completed appointment" — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/); "they charge $2 per follow-up email", texts "$50 to $200+", medspa tier $369-$421/mo — [PatientNow](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives). These two competitor sources disagree on what the $2 is charged for.
- **Strengths:** THIRD-PARTY REPORTED — "Polished interface, strong client experience" — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/). Ratings 4.6/390 (Software Advice), 4.4/100 (G2) (snippets).
- **Weaknesses:** THIRD-PARTY REPORTED — "There's no lead nurturing or social posting"; only five campaign types; confirmation texts, same-day reminders and review requests carry separate charges — [PatientNow (competitor)](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives). THIRD-PARTY REPORTED — in testing, Beau "doesn't complete bookings, reschedules or cancellations during the conversation" and ended a call when the caller only wanted to reschedule — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- **Documented complaints:** THIRD-PARTY REPORTED (search snippets) — "Boulevard was the most expensive of the platforms I reviewed when looking to make the switch over a year ago" (Software Advice); 1-star Capterra UK review dated May 2026 warning of a 1-year contract that they "won't let you cancel"; a reviewer said charting was promised but "wasn't launched until after they signed the contract"; full-price charges per location and extra costs for texts/email tools — [Software Advice](https://www.softwareadvice.com/retail/boulevard-profile/reviews/), [Capterra UK](https://www.capterra.co.uk/reviews/180087/boulevard)
- **Integrations / API:** FACT — "open APIs ... Available for Enterprise tier only"; Developer Portal at developers.joinblvd.com — [Boulevard API page](https://joinblvd.com/products/api). THIRD-PARTY REPORTED — Admin API, Client API, Tokenization API (GraphQL); data includes clients, appointments, staff, locations, memberships; webhooks created in the platform — [Extole partner docs](https://docs.extole.com/docs/boulevard-blvd), [apis.io](https://apis.io/plans/boulevard/boulevard-plans-pricing/). FACT — a Boulevard app exists on Zapier (template "Send appointment details to endpoint") — [Zapier](https://zapier.com/templates/details/326c716c3b939e8d6644f3a0d5954bb39216eecff73112ec73920cf22c9c55a6). FACT — QuickBooks add-on — [pricing](https://www.joinblvd.com/pricing). Meta lead ads, Cherry, CareCredit, RepeatMD, Podium: not named on the pages read.
- **Recent moves:** FACT — Beau AI receptionist live with published pricing — [Beau page](https://www.joinblvd.com/features/ai-receptionist); marketing partnership with Medical Marketing Whiz, Aug 2026 — [AmSpa](https://www.americanmedspa.org/news/medical-marketing-whiz-announces-partnership-with-boulevard-to-help-med-spas-and-wellness-clinics-streamline-operations/). Funding/acquisitions in 2026: not found.

#### 3. Mangomint — https://www.mangomint.com
- **Positioning:** FACT — pricing page headline "One plan, affordable pricing"; Mira described as "the AI receptionist that turns calls and texts into bookings" — [pricing](https://www.mangomint.com/pricing/), [features](https://www.mangomint.com/features/)
- **Target customers:** THIRD-PARTY REPORTED — reviews are "heavily weighted toward medical spa, salon, and massage businesses" (search summary of [Capterra](https://capterra.com/p/187593/Mangomint/reviews/))
- **Core features (all included in the single plan):** FACT — calendar & scheduling, payments/POS, online booking, Express Booking, mobile apps, client management, **web chat**, memberships & packages, forms & charting, gift cards, **automated flows**, campaigns, offers & discounts, virtual waiting room, retail & inventory, staff management, reporting, multi-location, integrations — [pricing](https://www.mangomint.com/pricing/)
- **Lead / follow-up / AI:** FACT — Phone add-on: "Call and text your clients from one number on any device"; Mira AI receptionist handles calls and texts and books, reschedules and cancels — [pricing](https://www.mangomint.com/pricing/), [features](https://www.mangomint.com/features/). Lead capture pipeline, missed-call text-back and marketing attribution: not found on the pages read.
- **Pricing (official):** FACT — **Locations: $120/mo each; Users: $10/mo each.** Add-ons: Phone **$70/mo per line**; Marketing "starting at $30/mo" by credits (3,500 credits $30; 6,000 $50; 15,000 $100; 35,000 $200; 60,000 $300); Payroll $50/mo + $8 per worker. Free onboarding, free data transfer, no contracts — [pricing](https://www.mangomint.com/pricing/). FACT — new model effective 1 Aug 2026; Essentials/Standard/Unlimited tiers retired; HIPAA now in base plan — [Mangomint pricing update](https://www.mangomint.com/blog/pricing-update-2026/) (via search summary)
- **Pricing, third-party reported, unverified:** Mira "$300 per month", requires the Phone add-on — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/). Outdated figures still circulating: "Starter from $165/month", "Unlimited from $375/month" — [PatientNow](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives)
- **Strengths:** THIRD-PARTY REPORTED — 4.9 on Capterra (298 reviews) and G2; praised for interface and support — search summaries of [Capterra](https://capterra.com/p/187593/Mangomint/reviews/), [G2](https://www.g2.com/products/mangomint)
- **Weaknesses:** THIRD-PARTY REPORTED — "No EMR/charting" — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/); contradicted by Mangomint's own list, which includes "Forms & Charting" — [pricing](https://www.mangomint.com/pricing/). A Zenoti comparison rates its charting as basic with limited photo and multi-location support (search summary).
- **Documented complaints:** THIRD-PARTY REPORTED (snippets) — "I often have complex reporting questions and the team is often able to find a work around or add in that report to the interface for me" (Capterra); limited loyalty programmes and multi-location customisation (G2 summary); "charges extra for add-ons, and becomes very expensive quickly"; "cannot write half syringes into inventory" — [Capterra](https://capterra.com/p/187593/Mangomint/reviews/), [G2](https://www.g2.com/products/mangomint)
- **Integrations / API:** FACT — listed integrations: Shopify, Mailchimp, **Webhooks** ("Use Webhooks to send event data from Mangomint to other third-party applications"), Docovia (Good Faith Exams), Doxy.me. No public API or Zapier app mentioned — [integrations](https://www.mangomint.com/integrations/). Conflict: integrations page shows Webhooks as "Included"; a help article (via search summary, probably pre-August 2026) says $50/month add-on on Standard/Unlimited — [help article](https://mangomint.com/learn/webhooks-integration). Webhooks are outbound only; no inbound write API found.
- **Recent moves:** FACT — single-plan repricing 1 Aug 2026 — [pricing update](https://www.mangomint.com/blog/pricing-update-2026/); Mira AI receptionist launched (date not found).

#### 4. Vagaro — https://www.vagaro.com/pro
- **Target customers:** FACT — priced by bookable calendar from "Just Me" to "7+" — [pricing](https://www.vagaro.com/pro/pricing)
- **Core features:** FACT — booking, marketplace listing, text and email marketing, forms, online store, memberships, payroll, branded app — [pricing](https://www.vagaro.com/pro/pricing)
- **Lead / follow-up / AI:** FACT — "Vera Receptionist" is an AI **chatbot** that "responds to messages from your Vagaro Listing Page and your text marketing number", checks availability and sends booking/reschedule/cancel links; "Released Aug 24, 2026" — [Vagaro update](https://www.vagaro.com/pro/updates/vera-receptionist). THIRD-PARTY REPORTED — Vera is not a phone receptionist; Fill My Books charges 5% of booking value for returning clients and 20% for new clients — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- **Pricing (official):** FACT — one location "$30.00", "Exclusive rate for the first 6 months" "$23.99/ mo."; per-calendar amounts for 2-7+ not shown in fetched content. Add-ons: Text Marketing "Starting at $20/mo."; Email Marketing "Free to Start"; Forms "$10/mo"; Online Shopping Cart "$10/mo"; Vagaro MySite "$20/mo"; Branded App "$100/mo"; Fill My Books "Fees apply"; Payroll "$34/mo + $5/employee"; Check-In App "$10/mo."; QuickBooks "$10/mo"; Xero "$30/mo"; Data Lake "$40/mo" — [pricing](https://www.vagaro.com/pro/pricing). Vera Receptionist price: not found.
- **Pricing, third-party reported, unverified:** extra calendars $10/mo; processing 2.2% + $0.19 or 2.6% + $0.10 — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/)
- **Strengths:** low entry price (FACT, pricing page); THIRD-PARTY REPORTED — Capterra ~4.7 from ~3,700 reviews, G2 4.6 (snippets)
- **Weaknesses:** THIRD-PARTY REPORTED — "limited HIPAA support"; "Add-on costs stack up" — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/), [PatientNow](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives)
- **Documented complaints:** THIRD-PARTY REPORTED (snippets) — July 2026 Trustpilot reviewer objected to a binding contract that kept charging for a year; refund refused; "missing features", "hidden fees", "high fees and costs for basic features" (G2 summary). Trustpilot US 3.9 from 671 reviews — [Trustpilot](https://www.trustpilot.com/review/vagaro.com/location/us), [G2](https://www.g2.com/products/vagaro)
- **Integrations / API:** FACT — public APIs "programmatically retrieve information and make changes to your Vagaro account"; webhooks for appointments (booked/modified), customers, employees, transactions, form responses, business locations — [docs.vagaro.com](https://docs.vagaro.com/), [webhook intro](https://docs.vagaro.com/public/docs/introduction). Access process, cost and whether appointments can be written via API: not found.
- **Recent moves:** FACT — Vera Receptionist released 24 Aug 2026 — [Vagaro](https://www.vagaro.com/pro/updates/vera-receptionist)

#### 5. AestheticsPro — https://www.aestheticspro.com
- **Target customers:** FACT — Pro-Plus includes 2 users (max 3); Executive and Enterprise unlimited users and multi-location — [pricing](https://www.aestheticspro.com/Software-Pricing/)
- **Core features:** FACT — mobile app, client portal with online booking, telemedicine, "AP ERx*", "AP Texting*", "AP Marketing Suite*" (AI-assisted content, automated outreach, social scheduling, performance insights), "Kai AI Suite*", 500+ form EMR library. Asterisked items "require an additional fee" (fees not published) — [pricing](https://www.aestheticspro.com/Software-Pricing/)
- **Lead / follow-up / AI:** FACT — lead management is not listed on the pricing page; Kai AI Concierge (AI receptionist for calls, texts, chats) is marked "Coming soon" — [pricing](https://www.aestheticspro.com/Software-Pricing/), [AI suite](https://aestheticspro.com/ai-suite/). THIRD-PARTY REPORTED — offers email campaigns, text messaging, lead management, review management and loyalty (search summary of a third-party review).
- **Pricing (official):** FACT — Pro-Plus **$160/month** (2 users; additional user $85/mo, up to 3); intro offer **$99/mo.** for Pro-Plus first year, requires AP Payments, US only; Executive **$285/month**; Enterprise **$350/month** (adds "custom API solutions" and custom reporting) — [pricing](https://www.aestheticspro.com/Software-Pricing/)
- **Strengths:** FACT — published flat pricing with unlimited users at $285 — [pricing](https://www.aestheticspro.com/Software-Pricing/). FACT — AmSpa Platinum Vendor Affiliate — [AmSpa](https://www.americanmedspa.org/?p=21599)
- **Weaknesses:** THIRD-PARTY REPORTED — texting, marketing and e-prescribing each carry unpublished fees — [Zenoti comparison (competitor)](https://www.zenoti.com/thecheckin/zenoti-vs-aestheticspro)
- **Documented complaints:** THIRD-PARTY REPORTED (snippet) — a Capterra reviewer called the company "absolutely terrible" and objected to a price of nearly $2,000 a month for fewer features — [Capterra](https://www.capterra.com/p/93446/AestheticsPro/reviews/). No further verbatim complaints retrieved.
- **Integrations / API:** FACT — integrations page says it integrates with Zapier and "if your system supports webhooks, AestheticsPro can help power your automation and reporting"; "custom API solutions" only on Enterprise — [integrations](https://aestheticspro.com/AP-Integrations/), [pricing](https://www.aestheticspro.com/Software-Pricing/). Public API documentation: not found.
- **Recent moves:** FACT — Kai AI Suite launched; AI phone/text concierge announced as coming soon — [AI suite](https://aestheticspro.com/ai-suite/)

#### 6. Aesthetic Record — https://www.aestheticrecord.com
- **Target customers:** FACT — per-user pricing from $15; Enterprise tier for franchise/multi-location — [pricing](https://www.aestheticrecord.com/pricing/)
- **Core features:** FACT — photo management, procedure charting, medical director oversight, automated reminders, memberships, patient portal and wallet, packages, eGift cards, online booking and eCommerce, reputation management, inventory — [pricing](https://www.aestheticrecord.com/pricing/)
- **Lead / follow-up / AI:** FACT — "external leads integration" and "LeadAR integration" only on Accelerator; "2-Way Texting" and third-party CRM integrations carry a footnote (extra cost implied, not defined). **LeadAR Start Plan $97**: lead and patient sync, centralised inbox, social post scheduling, Smart Lists, mass SMS and email campaigns — [pricing](https://www.aestheticrecord.com/pricing/). ASSUMPTION — LeadAR's feature list resembles a white-labelled GoHighLevel-style CRM; not confirmed.
- **Pricing (official):** FACT — Essentials **$15/month per user** + "$399 Startup & Onboarding Investment" (limits: 2 GB, 250 SMS, 300 emails per user per month); Accelerator **$19/month per user** + $399 (400 SMS, 600 emails); Enterprise "Contact Us". ePrescribing $31-$45 per prescriber (term mapping unclear). ChartSmart AI: Starter $30/month (50 charts), Pro $50/month (100), Unlimited $75/month. 14-day trial — [pricing](https://www.aestheticrecord.com/pricing/)
- **Strengths:** THIRD-PARTY REPORTED (snippet) — "Aesthetic record offers all the necessary features of the more costly platforms for a fraction of the price" — [Capterra](https://www.capterra.com/p/162938/Aesthetic-Record/reviews/)
- **Weaknesses:** THIRD-PARTY REPORTED — "AI, texting, and CRM are paid add-ons"; upfront onboarding fee; steeper learning curve — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/). PatientNow targets its users over "endless add-ons and limited patient engagement options" — [PatientNow (competitor)](https://www.patientnow.com/lp/patientnow-vs-aestheticrecord)
- **Documented complaints:** THIRD-PARTY REPORTED (snippets) — Capterra 3.5 from 75 reviews; a reviewer wanted more reporting, website and scheduling features; a reviewer warned funds can be held up for weeks during setup; a 1.0 review from August 2024 tells people not to use it — [Capterra](https://www.capterra.com/p/162938/Aesthetic-Record/reviews/)
- **Integrations / API:** FACT — RepeatMD, TouchMD, JOYA, PatientFi, ASPIRE Galderma Rewards, Constant Contact, ActiveCampaign, Mailchimp, Zoho, HubSpot (Accelerator) — [pricing](https://www.aestheticrecord.com/pricing/). FACT — Zapier app "Aesthetic Record EMR" exists, including a LeadConnector (GoHighLevel) pairing and a Podium pairing — [Zapier](https://zapier.com/apps/aesthetic-record-emr/integrations). THIRD-PARTY REPORTED — no developer portal or public API; Zapier app is read-only ("two triggers and no actions"); no documented route exposes appointments, charts or notes; Leads API by partnership via partnerships@aestheticrecord.com — [Nirmitee guide, last checked 18 Nov 2026](https://nirmitee.io/blog/aesthetic-record-api-integration-guide/). THIRD-PARTY REPORTED — a CRM vendor says its AR connection only moves data into its CRM, with no push back — [Aesthetix CRM help](https://help.aesthetixcrm.com/en/articles/40-aesthetic-record-integration)
- **Recent moves:** FACT — ChartSmart AI and LeadAR listed as priced products — [pricing](https://www.aestheticrecord.com/pricing/)

#### 7. PatientNow — https://www.patientnow.com
- **Positioning:** FACT — "Transform every visit, accelerate your clinic's growth journey." — [PatientNow](https://www.patientnow.com/)
- **Target customers:** FACT — med spas, plastic surgery, dermatology, weight loss, IV therapy, multi-location; "more than 5,000 aesthetic practices" — [PatientNow](https://www.patientnow.com/), [AmSpa](https://www.americanmedspa.org/news/patientnow-acquires-recura-an-ai-practice-growth-engine/)
- **Core features:** FACT — EMR, RxPhoto, online booking, payments, text-to-pay, text/email reminders, memberships and loyalty, email and text campaigns, automatic review requests, Insights hub with marketing ROI reporting, QuickBooks sync, "Comms Hub" (EMR and phone in one) — [PatientNow](https://www.patientnow.com/)
- **Lead / follow-up / AI:** FACT — lead capture connects website visitors and inquiries to a pipeline; **Recura AI** answers calls, follows up and moves conversations toward booking; AI flags patients due for rebooking — [PatientNow](https://www.patientnow.com/). FACT (vendor claim) — "AI agents answer calls and texts 24/7, and follow up with leads in under 30 seconds"; "Built-in lead generation, drip campaigns, reputation management, and social posting" — [PatientNow comparison](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives)
- **Pricing:** FACT — no figures on the homepage. FACT (vendor's own comparison article, not a pricing page) — "PatientNow starts at $410/mo for Essentials" — [PatientNow comparison](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives). Review sites list "contact vendor" (snippets).
- **Strengths:** ASSUMPTION — the most complete native lead-to-booking story among EMR-first vendors after buying Recura; based on the vendor's own claims above.
- **Weaknesses / documented complaints:** FACT (Trustpilot page opened) — TrustScore 2.1, 9 reviews, all 1-star. Quotes: "Very Expensive, Poor Value, and a Frustrating Contract Experience" (20 Oct 2026); "I was charged an additional $213.20 payment processing non-usage fee without anyone clearly informing me" (16 Oct 2026); "Misleading contract that locked me in for an extra year and longer if I hadn't caught it" (6 Aug 2026); "left our practice without a functional system for over three months" (23 Sep 2025); "the company refused to release me from the contract, despite months of poor service" (7 May 2025) — [Trustpilot](https://www.trustpilot.com/review/patientnow.com). THIRD-PARTY REPORTED (snippets) — BBB: not accredited, 13 complaints in 3 years; Capterra 3.9 from ~298 reviews; G2 3.0 from 20; a reviewer cited customer support and "lack of a real EMR" — [BBB](https://prod.bbb.org/us/co/englewood/profile/healthcare-management/patientnow-1296-1000124614/complaints), [Capterra](https://www.capterra.com/p/92269/PatientNOW/reviews/)
- **Integrations / API:** FACT — QuickBooks sync; integrations page exists; no API mentioned on homepage — [PatientNow](https://www.patientnow.com/). Public API: not found.
- **Recent moves:** FACT — acquired Recura (AI voice/text sales, reception and booking) announced 6 Nov 2025; Recura continues to sell standalone to non-PatientNow customers — [AmSpa](https://www.americanmedspa.org/news/patientnow-acquires-recura-an-ai-practice-growth-engine/)

#### 8. Nextech — https://www.nextech.com
- **Positioning:** FACT — "Transform your specialty practice" — [Nextech](https://www.nextech.com/)
- **Target customers:** FACT — ophthalmology, plastic surgery, dermatology, med spa, orthopaedics — [Nextech](https://www.nextech.com/)
- **Core features:** FACT — Practice Management, Nextech EHR, Nextech Cora (AI scribe), Nextech Payments, **Nextech CRM**, **TouchMD**, RCM services, patient portal — [Nextech](https://www.nextech.com/). CRM feature detail: not found (med spa page returned 404).
- **Pricing:** FACT — not public; calls to action are "Schedule a demo" and "Request info" — [Nextech](https://www.nextech.com/)
- **Weaknesses / complaints:** THIRD-PARTY REPORTED (snippets) — Capterra summary: "pricing is excessive, with costly modules, ongoing fees, and unexpected charges"; Software Advice value score 3.7 vs 4.1 overall; a reviewer said scheduling, HIPAA forms and intake were poorly designed for TRT/peptide/wellness practices; a February 2026 TouchMD review says Nextech bought TouchMD "last year" and would integrate only for an extra fee — [Capterra](https://www.capterra.com/p/122691/Nextech-Practice/), [Software Advice](https://www.softwareadvice.com/medical/nextech-profile/)
- **Integrations / API:** FACT — "Developers Portal" link in site navigation; details not retrieved — [Nextech](https://www.nextech.com/)
- **Recent moves:** THIRD-PARTY REPORTED — TouchMD acquisition (single reviewer account; date and terms not confirmed).

#### 9. Symplast — https://symplast.com
- **Positioning:** FACT — "You Deserve the Best. Plastic Surgery EHR & Practice Management Platform."; "The #1 KLAS-rated operating system for aesthetic medicine" — [Symplast](https://symplast.com/)
- **Target customers:** FACT — aesthetic practices, "built by plastic surgeons" — [Symplast](https://symplast.com/)
- **Core features:** FACT — EHR, patient app (messaging, media, forms, payments), insurance billing, practice management, payments and financing, media management, **CRM: "Lead capture, follow-up, and patient re-engagement"**, AI Scribe, ambient listening, chatbot — [Symplast](https://symplast.com/)
- **Pricing:** FACT — not public; three unpriced packages: Launch, Growth (adds a "growth execution team"), Velocity (invite-only) — [Symplast](https://symplast.com/)
- **Pricing, third-party reported, unverified:** $300/mo starting (Software Advice/Capterra listing); ~$999/mo for 10 users plus $1,000-$10,000 onboarding (ITQlick estimate) — [Software Advice](https://www.softwareadvice.com/medical/symplast-profile), [ITQlick](https://www.itqlick.com/symplast/pricing)
- **Complaints:** THIRD-PARTY REPORTED (snippet) — support hard to reach; only ~25 Capterra reviews — [Capterra](https://www.capterra.com/p/178244/Symplast/reviews/)
- **Integrations / API:** not found.

#### 10. Pabau — https://pabau.com
- **Target customers:** FACT — plans by user count: Solo (1), Team (2-3), Medium (4-5), Group (6-15), Enterprise (16+); regional pricing for UK, US, CA, AU, EU — [pricing](https://pabau.com/pricing/)
- **Core features (every plan):** FACT — scheduling and online booking, patient portal, forms/photos, payments/POS, packages and memberships, marketing tools and automation, inventory, reporting, **lead management** — [pricing](https://pabau.com/pricing/)
- **Lead / follow-up / AI:** FACT — add-on "Engage Plus: AI agents for calls and messages, plus WhatsApp and a cloud phone system"; priced per location; messages and AI call minutes use Pabau credits; 3 months free. Also Marketing Plus, Care Plus, Insights Plus add-ons — [pricing](https://pabau.com/pricing/)
- **Pricing:** FACT — no dollar amounts appeared in the fetched pricing page content; annual billing "saves up to 20%" — [pricing](https://pabau.com/pricing/). THIRD-PARTY REPORTED, unverified — Startup plan $59/month (Capterra listing); Solo £118/month per location ex VAT on a Pabau subscription page (GBP, not USD) — [Capterra](https://www.capterra.com/p/140062/Pabau-CRM/pricing/), [pulse.pabau.com](https://pulse.pabau.com/plans/)
- **Complaints:** THIRD-PARTY REPORTED (snippets) — "frequent technical glitches and instability"; "unclear and costly pricing structure"; refund refused; "constant connect issues, non existent customer support". Capterra 4.7 from 658 reviews — [Capterra](https://www.capterra.com/p/140062/Pabau-CRM/)
- **Integrations / API:** FACT — native webhooks under Setup > Developer & Other > Webhooks for Appointments, Clients, **Leads**, Invoice, Payments, Forms; appointment webhooks fire on booked/cancelled/rescheduled; lead webhooks on added/won/lost/updated; an inbound lead endpoint with api_key accepts leads (documented for Facebook leads); API keys page and API documentation exist — [Pabau webhooks](https://support.pabau.com/en/pabau2/how-to-set-up-webhooks), [Facebook Leads API](https://support.pabau.com/en/pabau2/facebook-leads-api), [Zapier](https://zapier.com/apps/pabau-1/integrations)
- **Note:** ASSUMPTION — UK-origin product; US med spa adoption level not established.

#### 11. Moxie — https://www.joinmoxie.com
- **Positioning:** FACT — "The Clinical-Grade Operating System for Medspas" — [Moxie](https://www.joinmoxie.com/)
- **Target customers:** FACT — aspiring owners launching a medspa, solo providers, multi-provider practices — [Moxie](https://www.joinmoxie.com/)
- **Core features:** FACT — charting/EMR, e-prescribing, scheduling and payments, memberships and packages, inventory, compliance tools, payroll, Practice 360 financial reporting, MAIA "AI booking assistant" (OpenAI), AI scribe, done-for-you marketing services (Meta campaigns, local SEO), group purchasing ("up to 55%" supply savings), Moxie Capital — [Moxie](https://www.joinmoxie.com/), [Scale](https://www.joinmoxie.com/scale)
- **Lead / follow-up / AI:** FACT — lead management, CRM and two-way texting are not mentioned on the homepage or Scale page; retention is described as "automated reminders, follow-ups, and post-care notes"; marketing "tracks patients from first click to lifetime spend" — [Scale](https://www.joinmoxie.com/scale)
- **Pricing:** FACT — not public; /pricing returns 404. A 2024 Moxie blog says Moxie Suite "scales with your business needs" and "Unlike fixed monthly fees, you only pay for the features and support you require." — [Moxie blog, updated 5 Jul 2024](https://www.joinmoxie.com/post/best-medical-spa-software). Third-party price: not found (search results confuse it with other products named Moxie).
- **Strengths:** ASSUMPTION — bundles services a software-only vendor cannot (launch coaching, medical director matching, supply discounts, marketing agency), based on the features above.
- **Weaknesses / complaints:** not found. No independent reviews, Trustpilot page or Reddit thread retrieved; Moxie's own review page shows only positive Google reviews — [Moxie reviews page](https://joinmoxie.com/post/join-moxie-reviews)
- **Integrations / API:** FACT — Stripe, Cherry, Affirm, OpenAI named — [Scale](https://www.joinmoxie.com/scale). API: not found.
- **Recent moves:** THIRD-PARTY REPORTED (multiple outlets) — $25M Series C announced March 2026, led by Viewpoint Ventures with SignalFire, Lachy Groom, Haystack; ~$51M total — [AmSpa](https://americanmedspa.org/news/moxie-raises-25m-series-c-to-bring-clinical-grade-operating-infrastructure-to-independent-aesthetic-practices), [BeautyMatter](https://beautymatter.com/articles/medspa-in-a-box-moxie-raises-25-million-series-c)

#### 12. Portrait — https://www.portraitcare.com
- **Positioning:** FACT — "The operating system for independent practices." — [Portrait](https://www.portraitcare.com/)
- **Target customers:** FACT — independent aesthetic practices and med spas; "1,200+ independent practices" — [Portrait](https://www.portraitcare.com/)
- **Core features:** FACT — group-purchasing Marketplace (toxins, fillers, GLP-1s, skincare; up to 60% savings on select products), Core EHR (scheduling, charting, inventory, payments, online booking, automated patient messaging); beta "AI-powered patient campaigns"; "Copilot" (answers patients at any hour and helps book) is "coming soon". CRM, lead management, memberships, reporting: not mentioned — [Portrait](https://www.portraitcare.com/)
- **Pricing (official):** FACT — membership "Free to join", "No commitment"; Core tier: "EHR for $249/mo*" with footnote "The EHR is complimentary for all members for a limited time."; Bronze and above "EHR included at no cost"; Bronze-Diamond require a credit package, "Packages start at $2,000"; AI tools tiered (Silver "Essential AI tools" to Platinum "Full suite of AI tools") — [pricing](https://www.portraitcare.com/pricing)
- **Complaints:** not found. **Integrations/API:** not found.
- **Recent moves:** ASSUMPTION — the tiered marketplace/free-EHR model appears to be a repositioning from an earlier "one-time implementation fee, no revenue share" offer seen on older site pages (search summary of [Portrait](https://www.portraitcare.com/powered-by-portrait)); dates not confirmed. Funding in 2025-2026: not found.

#### 13. Jane App — https://jane.app
- **Target customers:** ASSUMPTION — allied-health and wellness clinics generally; not med-spa specific. THIRD-PARTY REPORTED — "no native photo markup or aesthetic consent workflows" — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/)
- **Core features:** FACT — online booking, telehealth, secure messaging, email reminders, intake forms, charting, AI Scribe, invoices and payments, gift cards; Thrive adds waitlist automation, return-visit reminders, packages & memberships, ratings and reviews — [pricing](https://jane.app/pricing)
- **Lead / follow-up:** lead capture, two-way texting, missed-call text-back, AI receptionist: not found on the pricing page.
- **Pricing (official, USD):** FACT — "Balance" "USD $59 / month" ("Limited to 20 appointments / month"); "Practice" "USD $79 / month"; "Thrive" "USD $99 / month"; per-additional-practitioner amounts not shown in fetched content. Add-ons: AI Scribe "$15 /month per opted-in practitioner"; Group Telehealth $15; Insurance Billing "$20 / month +$5 / $2.50 per additional full / part-time practitioner"; Jane Websites "$59 / month per clinic" — [pricing](https://jane.app/pricing)
- **Integrations / API:** FACT — Jane Developer Platform APIs let approved "Technology Partners" build practitioner-authorised "Jane Extensions"; OAuth 2.0 PKCE — [developers.jane.app](https://developers.jane.app). THIRD-PARTY REPORTED — no self-serve signup; partner review required; sources conflict on whether webhooks exist — search summary of [Jane integrations blog](https://jane.app/blog/jane-integrations-our-program-our-partners-and-how-to-work-with-us)
- **Complaints:** not found.

#### 14. Mindbody — https://www.mindbodyonline.com/business
- **Target customers:** ASSUMPTION — fitness/wellness first; THIRD-PARTY REPORTED "fitness/wellness focus" — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/)
- **Core features:** FACT — booking, payments, branded widgets, website, Mindbody app listing; Ultimate adds "automated email and text campaigns", "AI front desk support", "a built-in sales pipeline", "Lead management dashboard" — [pricing](https://www.mindbodyonline.com/business/pricing)
- **Lead / follow-up / AI:** FACT — Email/SMS marketing and lead management dashboard only on Ultimate; AI Concierge included on Ultimate, add-on on Accelerate — [pricing](https://www.mindbodyonline.com/business/pricing). THIRD-PARTY REPORTED — AI Concierge works over text and web chat and follows up by text after missed calls, but "doesn't answer the phone" — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- **Pricing (official):** FACT — Starter **$79 USD/month per location**; Accelerate and Ultimate not priced ("Let's talk") — [pricing](https://www.mindbodyonline.com/business/pricing). Conflict: AmSpa/GlossGenius article says $99/mo per location.
- **Complaints:** THIRD-PARTY REPORTED (snippets) — "locked them into a contract they were never aware of" (Capterra); a medical spa operator on Trustpilot said the rep's promise of new clients via the consumer app drove a 1-year signing (Mindbody replied 31 Mar 2026); "continued price increases, declining customer service"; Capterra ~4.0 from ~2,997 reviews — [Capterra](https://capterra.com/p/40229/MINDBODY/reviews/), [Software Advice](https://www.softwareadvice.com/club-management/mindbody-profile/reviews/). THIRD-PARTY REPORTED, unverified — 12-month auto-renewing terms with early-termination penalties; BBB 103 complaints in 3 years — [vibefam](https://vibefam.com/mindbody-pricing/)
- **Integrations / API:** FACT — "100+ third-party integrations" — [pricing](https://www.mindbodyonline.com/business/pricing). Public API details not retrieved in this session.

#### 15. Meevo (Millennium Systems International) — https://www.meevo.com
- **Positioning:** FACT — "AI-powered salon, spa and med spa software built to grow your business and keep you in control." — [Meevo](https://www.meevo.com/)
- **Target customers:** FACT — salons, spas, med spas, single to multi-location and franchise — [Meevo](https://www.meevo.com/)
- **Core features:** FACT — online booking, memberships, med spa charting with lot/expiry tracking, automated confirmations and waitlist texts, Marketing Suite (email, online presence, social posting), MeevoIQ (Front Desk, Marketing and Insights Advisors; AI Receptionist that answers calls and books; Voice to Chart). Lead management not mentioned — [Meevo](https://www.meevo.com/)
- **Pricing:** not found (pricing URL returned 404; homepage lists no prices).
- **Integrations / API:** FACT — "MeevoXchange Marketplace" with partner integrations and "API developer tools"; no detail — [Meevo](https://www.meevo.com/)
- **Complaints:** not found.

#### 16. GlossGenius — https://glossgenius.com
- **Target customers:** FACT — Standard for businesses starting out; Gold up to 9 staff; Platinum 10+; "Practice Essentials" and "Practice Advanced" for aesthetics practices — [pricing](https://glossgenius.com/pricing)
- **Core features:** FACT — booking website, unlimited client notifications, email and text marketing, inventory, packages and memberships, forms and waivers, Google booking and reviews, waitlist, "Google marketing analytics" (Platinum), EMR/compliance tools on Practice plans — [pricing](https://glossgenius.com/pricing)
- **Lead / follow-up / AI:** FACT — "Reception" add-on **$50/month**, "answers calls and texts and books appointments" — [pricing](https://glossgenius.com/pricing). THIRD-PARTY REPORTED — free until 30 Nov 2026, then $50/mo with 100 minutes and 200 texts, overages $0.50/min and $0.05/message; limited rollout; in testing it sometimes talked over callers — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/). Lead pipeline/CRM: not found.
- **Pricing (official, monthly / billed annually):** FACT — Standard $28 / $24; Gold $56 / $48; Platinum $168 / $148; **Practice Essentials $168 / $148**; **Practice Advanced $298 / $248**. Processing: tap/dip/swipe 2.4% + $0.15; online invoicing 2.9% + $0.30; card-on-file/keyed 3.4% + $0.15. Payroll $40/month + $6/seat — [pricing](https://glossgenius.com/pricing) (tool noted it summarised feature wording). Conflict: a GlossGenius-authored AmSpa article says "$148/mo" and "Flat 2.6% processing" — [AmSpa](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/)
- **Weaknesses:** FACT (self-described) — "fewer native integrations than enterprise tools" — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/)
- **Complaints:** THIRD-PARTY REPORTED (snippets) — Trustpilot reviewer says account was shut down after ~$11,000 in client payments; March 2026 Capterra reviewer reports unauthorised charges and an unhelpful support response; Capterra 4.8 from ~348 reviews — [Trustpilot](https://au.trustpilot.com/review/glossgenius.com), [Capterra](https://www.capterra.com/p/174830/GlossGenius/reviews/)
- **Integrations / API:** public API not found.
- **Recent moves:** FACT — med spa "Practice" tiers and AI Reception add-on on the pricing page — [pricing](https://glossgenius.com/pricing)

#### 17. PocketSuite — https://pocketsuite.io
- **Target customers:** ASSUMPTION — solo and small service businesses across many verticals; the fetched pricing page was oriented to pet businesses ("Pet family and pet profiles", kennel scheduling), so med spa fit is weak.
- **Core features (Premium):** FACT — "Business number for 2-way texting and calls"; "Online lead form, online booking, live chat"; "Google leads, Google reviews, integration with Google Business Profile 'Book Now' button"; "Digital forms and contracts"; "Packages, & subscriptions/recurring billing"; "Group texting, scheduled messaging, automated text marketing"; "Buy Now Pay Later" — [pricing](https://pocketsuite.io/pricing)
- **Pricing (official):** FACT — Premium "$49.99/mo"; Team "$99.99/mo"; Facility "$149.99/mo"; Enterprise "Contact Us" (adds "Lead routing capabilities"); "Free 30-day trial" — [pricing](https://pocketsuite.io/pricing)
- **Integrations / API:** FACT — "Google Calendar / iCalendar sync, GoogleMaps, Zapier integration, QuickBooks integration" — [pricing](https://pocketsuite.io/pricing); Zapier API documentation article exists — [PocketSuite support](https://support.pocketsuite.io/hc/en-us/articles/41955941230605)
- **Complaints:** not found. EMR/charting: not found.

#### Other notable platforms surfaced (not profiled in depth)
- THIRD-PARTY REPORTED — Fresha ($19.95/mo; AI Concierge "$99.95 per location/month" with 200 minutes and 500 messages), Square Appointments (free plan; $49/mo per location), Phorest (Front Desk AI over SMS only; AmSpa Platinum Vendor Affiliate) — [AmSpa/GlossGenius](https://www.americanmedspa.org/news/best-medical-spa-software-in-2026-features-and-pricing-compared/), [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- THIRD-PARTY REPORTED — Podium "Avery" covers calls, texts, social and web chat for medspas but reviewers could not confirm it books/reschedules directly; custom pricing — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- Names seen in search results but not researched: Prospyr, OptiMantra, DaySmart Spa, RxPhoto, Aesthetix CRM.

### Inferences
- ASSUMPTION — the category splits into (a) booking-first tools adding charting (Boulevard, Mangomint, Vagaro, GlossGenius, Mindbody, Meevo), (b) EMR-first tools adding growth features (Aesthetic Record, AestheticsPro, PatientNow, Nextech, Symplast), and (c) "business-in-a-box" operators whose software is bundled with purchasing, financing and services (Moxie, Portrait).
- ASSUMPTION — PocketSuite and Jane are marginal competitors for a med spa lead tool; neither markets to med spas specifically.

### Gaps
- No verbatim Capterra/G2/Software Advice reviews could be opened (HTTP 403); snippets only.
- Per-calendar Vagaro prices, Jane per-practitioner prices and Pabau USD prices did not appear in fetched content.

---

## Which platforms already bundle lead management and follow-up well, and where do reviewers say that part is weak?

### Takeaway
Zenoti (AI Lead Manager) and PatientNow (Recura AI) make the strongest explicit lead-response claims; Pabau, Symplast and Mindbody Ultimate list lead management natively; Aesthetic Record sells it as a $97 bolt-on. Boulevard, Mangomint, Vagaro, GlossGenius, Jane, Moxie and Portrait do not describe a lead pipeline on the pages read, and competitor write-ups single out Boulevard for having "no lead nurturing".

### Cited Findings
- FACT — Zenoti AI Lead Manager collects leads "from ads, calls, web, and text into one inbox", scores by intent, responds "in under 90 seconds", and follows up until booking — [Zenoti press](https://www.zenoti.com/press/zenoti-expands-its-ai-workforce-purpose-built-ai-agents-for-every-medspa-workflow). AI agents require the "AI Plus package" — [Zenoti pricing](https://www.zenoti.com/pricing)
- FACT (vendor claim) — PatientNow/Recura: "follow up with leads in under 30 seconds"; one practice cut follow-up time "from 48 hours to 30 seconds" (not independently verified) — [PatientNow](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives), [AmSpa](https://www.americanmedspa.org/news/patientnow-acquires-recura-an-ai-practice-growth-engine/)
- FACT — Pabau lists "Lead management" as a core feature in every plan and exposes lead webhooks (added/won/lost) — [Pabau pricing](https://pabau.com/pricing/), [Pabau webhooks](https://support.pabau.com/en/pabau2/how-to-set-up-webhooks)
- FACT — Symplast lists CRM with "Lead capture, follow-up, and patient re-engagement" — [Symplast](https://symplast.com/)
- FACT — Mindbody restricts "Lead management dashboard", email/SMS marketing and sales pipeline to its top (unpriced) Ultimate tier — [Mindbody pricing](https://www.mindbodyonline.com/business/pricing)
- FACT — Aesthetic Record: leads integration only on Accelerator; LeadAR Start $97 for inbox, Smart Lists and mass SMS/email; 2-way texting flagged as extra — [AR pricing](https://www.aestheticrecord.com/pricing/)
- FACT — Boulevard's Beau captures medspa lead details and "passes it to staff to follow up"; it sends a booking link rather than booking — [Beau page](https://www.joinblvd.com/features/ai-receptionist)
- THIRD-PARTY REPORTED — Boulevard: "There's no lead nurturing or social posting" — [PatientNow (competitor)](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives)
- THIRD-PARTY REPORTED — AI receptionist limits: Mindbody AI Concierge and Phorest do not answer phones; Vagaro Vera is chat/text only; Boulevard Beau does not complete bookings; Podium Avery not confirmed to book; GlossGenius Reception in limited rollout — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- FACT — AestheticsPro's AI phone/text concierge is "Coming soon"; lead management not on its pricing page — [AestheticsPro pricing](https://www.aestheticspro.com/Software-Pricing/)
- FACT — Moxie's Scale page does not mention lead management, CRM or two-way texting; lead generation is delivered as a marketing service — [Moxie Scale](https://www.joinmoxie.com/scale)
- FACT — Portrait's patient-facing Copilot is "coming soon" — [Portrait](https://www.portraitcare.com/)
- THIRD-PARTY REPORTED — PatientNow, the vendor with the boldest follow-up claims, has a 2.1 Trustpilot score dominated by contract and billing complaints, not product complaints about follow-up — [Trustpilot](https://www.trustpilot.com/review/patientnow.com)

### Inferences
- ASSUMPTION — reviewer complaints located are overwhelmingly about price, add-ons, contracts and support. I found almost no reviewer text specifically criticising lead follow-up; the "weak lead nurturing" evidence comes from competitors' marketing, so it is suggestive, not proven.
- ASSUMPTION — the booking-first tools most popular with independents (Boulevard, Mangomint, Vagaro, GlossGenius) treat a "lead" as a caller or chat to convert, not a pipeline record with source, stage and attribution. That is the clearest feature gap for a third-party lead tool.
- ASSUMPTION — missed-call text-back as a named, standalone feature was confirmed only for Mindbody (third-party) and implied by Zenoti's "missed calls" agent; elsewhere it is subsumed into paid AI receptionists costing roughly $50-$300/month plus usage.

### Gaps
- Marketing attribution (lead source to revenue) was confirmed only as vendor claims for PatientNow ("Marketing ROI"), Moxie ("first click to lifetime spend") and GlossGenius Platinum ("Google marketing analytics"). No independent assessment found.
- Native Meta/Google lead-ad ingestion was confirmed only for Pabau (Facebook leads endpoint) and PocketSuite ("Google leads"); Zenoti says "ads" without naming platforms.

---

## Which have open APIs or marketplaces, and which are closed?

### Takeaway
Zenoti, Vagaro and Pabau have publicly documented APIs and/or webhooks covering appointments; Boulevard has a real API but restricts it to Enterprise; Mangomint offers outbound webhooks only; Aesthetic Record and Jane are partner-gated; no public API was found for Moxie, Portrait, PatientNow, Symplast or GlossGenius.

### Cited Findings
- FACT — **Zenoti: open, read and write.** Booking create/reserve/confirm/reschedule, guest create/update, opportunities (leads) create/edit, webhooks; self-generated API key — [docs.zenoti.com](https://docs.zenoti.com/)
- FACT — **Vagaro: public APIs and webhooks** (appointments, customers, transactions, form responses) — [docs.vagaro.com](https://docs.vagaro.com/), [webhooks](https://docs.vagaro.com/public/docs/introduction). Write scope and access terms not confirmed.
- FACT — **Pabau: webhooks for appointments and leads, inbound lead endpoint, API keys** — [Pabau support](https://support.pabau.com/en/pabau2/how-to-set-up-webhooks), [Facebook Leads API](https://support.pabau.com/en/pabau2/facebook-leads-api)
- FACT — **Boulevard: APIs "Available for Enterprise tier only"** — [Boulevard](https://joinblvd.com/products/api). FACT — a Boulevard Zapier app exists — [Zapier](https://zapier.com/templates/details/326c716c3b939e8d6644f3a0d5954bb39216eecff73112ec73920cf22c9c55a6); which plans can use it: not found.
- FACT — **Mangomint: outbound webhooks only**; no public API or Zapier app listed — [Mangomint integrations](https://www.mangomint.com/integrations/)
- THIRD-PARTY REPORTED — **Aesthetic Record: closed.** No developer portal; read-only Zapier (two triggers, no actions); Leads API by partnership only; no route to appointments — [Nirmitee](https://nirmitee.io/blog/aesthetic-record-api-integration-guide/). FACT — Zapier app and LeadConnector pairing exist — [Zapier](https://zapier.com/apps/aesthetic-record-emr/integrations/leadconnector)
- FACT — **Jane: partner-gated** Developer Platform for approved Technology Partners — [developers.jane.app](https://developers.jane.app)
- FACT — **AestheticsPro: Zapier integration; "custom API solutions" on Enterprise ($350/mo)** — [integrations](https://aestheticspro.com/AP-Integrations/), [pricing](https://www.aestheticspro.com/Software-Pricing/)
- FACT — **Meevo: MeevoXchange Marketplace and API developer tools** (no detail) — [Meevo](https://www.meevo.com/)
- FACT — **Mindbody: "100+ third-party integrations"** — [Mindbody pricing](https://www.mindbodyonline.com/business/pricing)
- FACT — **PocketSuite: Zapier integration** — [PocketSuite pricing](https://pocketsuite.io/pricing)
- FACT — **Nextech: Developers Portal link exists** — [Nextech](https://www.nextech.com/)
- Not found — any public API or webhooks for Moxie, Portrait, PatientNow, Symplast, GlossGenius.

### Inferences
- ASSUMPTION — for a third-party lead/follow-up tool that needs to *write* appointments, only Zenoti is confirmed open on the pages read. Vagaro and Pabau are likely workable but write access needs testing. Boulevard is workable only for Enterprise accounts, which excludes most single-location independents.
- ASSUMPTION — for Mangomint and Aesthetic Record (both popular with independents), a third-party tool can realistically only *read* events (webhooks / Zapier triggers) and must hand off booking via the platform's own booking link. This is the same pattern Boulevard's own Beau uses.
- ASSUMPTION — the business-in-a-box vendors (Moxie, Portrait) are the most closed; their customers are unlikely prospects for an integrated third-party tool.

### Gaps
- Boulevard Developer Portal content, Vagaro API reference and Nextech/Mindbody developer docs were not readable in this session; scopes and costs are unconfirmed.
- GoHighLevel, Podium, Weave, RepeatMD, Cherry and CareCredit integrations were confirmed only where stated above (AR: RepeatMD, PatientFi, LeadConnector/Podium via Zapier; Moxie: Cherry, Affirm). For all other vendors: not found.

---

## What price range does a single-location med spa actually pay per month?

### Takeaway
On published list prices, a single-location med spa pays roughly $100-$450/month for core software before usage, and adding texting, forms, phone and an AI receptionist typically adds $100-$400+; enterprise-style vendors (Zenoti, PatientNow) are third-party reported at about $300-$600/month and up.

### Cited Findings
- FACT — Mangomint: $120 per location + $10 per user; Phone $70/line; Marketing from $30 — [pricing](https://www.mangomint.com/pricing/). ASSUMPTION (my arithmetic) — 1 location, 5 users, 1 phone line, lowest marketing tier = $120 + $50 + $70 + $30 = $270/month, before Mira.
- FACT — Boulevard: $143 (Essentials), $234 promo/$293 list (Premier), $328 promo/$410 list (Prestige, includes forms); Beau $149 — [pricing](https://www.joinblvd.com/pricing), [Beau](https://www.joinblvd.com/features/ai-receptionist). ASSUMPTION (my arithmetic) — Prestige at list + Beau = $559/month before text overages.
- FACT — GlossGenius Practice plans $168-$298 monthly; Reception $50 — [pricing](https://glossgenius.com/pricing)
- FACT — AestheticsPro $160-$350 (intro $99), with texting, marketing, eRx and AI at unpublished extra fees — [pricing](https://www.aestheticspro.com/Software-Pricing/)
- FACT — Aesthetic Record $15-$19 per user + $399 onboarding; LeadAR $97; ChartSmart AI $30-$75; eRx $31-$45 per prescriber — [pricing](https://www.aestheticrecord.com/pricing/)
- FACT — Vagaro from $30 for one calendar plus add-ons ($10-$100 each) — [pricing](https://www.vagaro.com/pro/pricing)
- FACT — Jane $59-$99; Mindbody Starter $79 per location; PocketSuite $49.99-$149.99; Portrait EHR $249/mo at Core tier (currently waived) — [Jane](https://jane.app/pricing), [Mindbody](https://www.mindbodyonline.com/business/pricing), [PocketSuite](https://pocketsuite.io/pricing), [Portrait](https://www.portraitcare.com/pricing)
- FACT (vendor article) — PatientNow "starts at $410/mo for Essentials" — [PatientNow](https://www.patientnow.com/resources/compare/med-spa-boulevard-alternatives)
- THIRD-PARTY REPORTED, unverified — Zenoti $300-$600/month per location plus add-ons — [Pabau blog](https://pabau.com/blog/zenoti-pricing/); Symplast from $300/month — [Software Advice](https://www.softwareadvice.com/medical/symplast-profile); typical med spa EMR $50-$300 per provider per month — [OptiMantra guide](https://optimantra.com/blog/how-much-should-you-pay-for-a-medspa-emr-your-2025-pricing-guide)
- AI receptionist add-on prices: FACT — Boulevard Beau $149/location + $0.50/min over 100 min; GlossGenius Reception $50. THIRD-PARTY REPORTED — Mangomint Mira $300; Fresha $99.95 — [Beau](https://www.joinblvd.com/features/ai-receptionist), [GlossGenius](https://glossgenius.com/pricing), [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)

### Inferences
- ASSUMPTION — a realistic all-in monthly software bill for an independent single-location med spa on a mainstream platform is about $250-$600, of which the conversational/AI layer is $50-$300. A standalone lead and follow-up tool is therefore competing against an incremental $50-$300 add-on from the incumbent, not against the whole bill.
- ASSUMPTION — usage-based text pricing (Boulevard, Zenoti, Mangomint credits) makes true cost hard to predict, which matches the recurring "add-ons" complaint theme.

### Gaps
- No verified data on what med spas actually pay (invoices, survey). All "actual" figures are list prices or third-party estimates.
- Moxie, Nextech, Symplast, Meevo, Zenoti and Pabau (USD) pricing is not public.

---

## Recent moves in 2025-2026: AI features launched, acquisitions, pricing changes

### Takeaway
2025-2026 was dominated by AI receptionist and AI lead-response launches across nearly every vendor, one notable acquisition aimed squarely at lead conversion (PatientNow-Recura), one major repricing (Mangomint) and one sizeable funding round (Moxie).

### Cited Findings
- FACT — Zenoti launched its AI Workforce 30 Sep 2025 and expanded it for medspas 28 Apr 2026 (AI Lead Manager, AI Receptionist, AI Concierge, AI Scribe, others); Medvelle partnership 29 Oct 2026 — [Zenoti press](https://www.zenoti.com/press/zenoti-expands-its-ai-workforce-purpose-built-ai-agents-for-every-medspa-workflow), [Zenoti press index](https://www.zenoti.com/press)
- FACT — PatientNow acquired Recura, 6 Nov 2025; Recura still sells standalone — [AmSpa](https://www.americanmedspa.org/news/patientnow-acquires-recura-an-ai-practice-growth-engine/)
- FACT — Mangomint moved to a single plan ($120/location + $10/user) effective 1 Aug 2026, folding HIPAA into the base plan — [Mangomint](https://www.mangomint.com/blog/pricing-update-2026/); Mira AI receptionist launched (third-party reported $300/mo) — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- FACT — Boulevard Beau AI receptionist at $149/location; Boulevard running "limited-time fall pricing" discounts on Premier/Prestige — [Beau](https://www.joinblvd.com/features/ai-receptionist), [pricing](https://www.joinblvd.com/pricing)
- FACT — Vagaro released Vera Receptionist (AI chatbot) 24 Aug 2026 — [Vagaro](https://www.vagaro.com/pro/updates/vera-receptionist)
- FACT — GlossGenius added med spa "Practice" tiers and a $50 AI Reception add-on — [pricing](https://glossgenius.com/pricing); third-party reported free until 30 Nov 2026 — [The Salon Business](https://thesalonbusiness.com/best-ai-receptionists-for-salons/)
- FACT — AestheticsPro Kai AI Suite; AI phone/text concierge "Coming soon" — [AestheticsPro](https://aestheticspro.com/ai-suite/)
- FACT — Aesthetic Record ChartSmart AI ($30-$75/mo) and LeadAR ($97) — [AR pricing](https://www.aestheticrecord.com/pricing/)
- FACT — Pabau "Engage Plus" AI agents for calls and messages — [Pabau pricing](https://pabau.com/pricing/)
- FACT — Mindbody AI Concierge included in Ultimate — [Mindbody pricing](https://www.mindbodyonline.com/business/pricing)
- FACT — Portrait: tiered marketplace model with free/"$249/mo" EHR; Copilot coming soon — [Portrait pricing](https://www.portraitcare.com/pricing)
- THIRD-PARTY REPORTED — Moxie raised a $25M Series C (March 2026, Viewpoint Ventures lead) — [AmSpa](https://americanmedspa.org/news/moxie-raises-25m-series-c-to-bring-clinical-grade-operating-infrastructure-to-independent-aesthetic-practices)
- THIRD-PARTY REPORTED — Nextech acquired TouchMD (per a February 2026 reviewer; unconfirmed) — [Capterra](https://www.capterra.co.uk/software/1040567/touchmd)
- FACT — adjacent deals: Fresh Clinics acquired Spakinect (Oct 2026; integrations with Zenoti, Boulevard, Aesthetic Record retained); AscendPoint acquired Medical Marketing Whiz (Oct 2026) — [AmSpa](https://www.americanmedspa.org/?p=21395), [AmSpa](https://www.americanmedspa.org/?p=21406)

### Inferences
- ASSUMPTION — "AI receptionist" is now table stakes in incumbents' marketing, which narrows the window for a standalone AI-answering product; the less-served area is structured lead pipeline, multi-touch follow-up and source attribution on top of platforms that have only webhooks.
- ASSUMPTION — PatientNow keeping Recura standalone shows a vendor-neutral lead-conversion layer is considered commercially viable, and Recura is a direct competitor to the planned product.

### Gaps
- Launch dates for Mangomint Mira, Boulevard Beau and GlossGenius Reception were not found.
- No 2026 funding or acquisition news found for Boulevard, Zenoti, Mangomint, Vagaro or Portrait.

---

## Not found / gaps

- **Reddit and Facebook-group evidence:** none retrieved. Searches for r/MedSpa, r/Esthetics and r/aestheticnurses content returned no reddit.com results. One Reddit figure ($600/mo for Zenoti) appears only second-hand via a competitor blog.
- **Verbatim review-site quotes:** Capterra, Software Advice and G2 blocked direct access (403). Only Trustpilot (PatientNow) was read directly. All other review quotes are search snippets and should be re-verified.
- **Unreachable source:** qsite-dashboard.pages.dev (Q-Site Medspa Survey) is outside the session's allowed network domains; it would need to be allowed in network settings to be read.
- **Pricing not public / not found:** Zenoti (contact sales), Moxie (not published; /pricing 404), Nextech (demo only), Symplast (three unpriced packages), Meevo (not found), Pabau USD figures (not shown), Mindbody Accelerate/Ultimate ("Let's talk"), PatientNow official pricing page (only a $410 figure in a vendor article), Vagaro Vera price, AestheticsPro add-on fees, Aesthetic Record two-way texting fee, Jane per-additional-practitioner fees.
- **Conflicts left unresolved:** Mangomint webhooks included vs $50/mo add-on; Boulevard "$2 per completed appointment" vs "$2 per follow-up email"; GlossGenius $168 monthly (pricing page) vs $148 and flat 2.6% (GlossGenius-authored article); Mindbody $79 (pricing page) vs $99 (article); whether Mangomint has charting (vendor says yes, a competitor article says no).
- **Features not confirmed either way:** missed-call text-back as a discrete feature for Boulevard, Mangomint, Vagaro, GlossGenius, AestheticsPro, Aesthetic Record, Moxie, Portrait; marketing attribution depth for all vendors; Meta/Google lead-ad native connectors for most vendors.
- **Integrations not confirmed:** GoHighLevel, Podium, Weave, RepeatMD, Cherry, CareCredit for most vendors (only those listed in the profiles were found).
- **API details not confirmed:** Boulevard (portal content unreadable), Vagaro write scope and access cost, Nextech, Mindbody, Meevo, GlossGenius, Symplast, PatientNow, Moxie, Portrait.
- **Independent complaints not found for:** Moxie, Portrait, Meevo, Jane, PocketSuite.
- **Market share / customer counts:** only vendor-stated figures (Zenoti 11,000+ medspas worldwide; PatientNow 5,000+ practices; Portrait 1,200+ practices). No independent share data.
