# Goverment travel

> We are building an AI-powered government travel assistant for government employees and travel coordinators to identify the best compliant travel option faster, reduce manual effort, and improve spending efficiency.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** Goverment travel
- **AI Value Archetype:** Copilot
- **Vulnerability Scores:** _(add: Moat _/5 · Data _/5 · Platform _/5)_
- **Top Risk:** Limited conversion of proprietary data into continuously improving intelligence and automated decisions.
- **Confidence:** H
- **Prototype:** https://lovable.dev/projects/f4ba4f9e-cf25-4d93-ba18-caae46089776?magic_link=mc_fdeb3796-33cc-4ef1-89c6-73f29f7224ed
- **Kill Criteria:** We would stop or reconsider the bet if the AI recommendations are not sufficiently accurate or compliant, do not meaningfully reduce the time required to select a flight, or fail to achieve adoption and trust among government travel users.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:**
- **Weakest Loop:** Corrections Loop - Preferences Loop - Network Loop
- **Top Encroachment Threat:** Microsoft Copilot
- **Encroachment Defense:** The biggest opportunities for improvement are to transform user feedback and behavior from data that is analyzed periodically into machine learning loops that continuously improve recommendations, dec…
- **Vendor Portability:** Partial

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):**
- **Gross Margin (AI-adjusted):**
- **Pricing Model:**
- **Pricing Today → Tomorrow:**
- **Total AI COGS / unit:**
- **Cascading Strategy:** Triage: Claude Haiku 4.5; frontier: Claude Opus 5; ratio **40% / 35% / 25%**
- **Net Margin Shift:**
- **Break-even at:**

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:**
- **Golden Dataset:** 5 rows, __ adversarial
- **Confidence UX:** Show uncertainty / tiered confidence / human-in-the-loop trigger
- **HITL Architecture:** # HITL (Human-in-the-Loop) Architecture
- **Failure Mode Coverage:** *What failure mode did your partner find that you missed?*

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | |------|-------|--------|-----------|--------| | Recursive Learning | User feedback, booking corrections, support tickets, CSAT | Improved AI recommendations, updated busin…
- **Governance Posture:** AI capabilities used within the ERCAB platform for government travel request creation, booking recommendations, policy validation, traveler assistance, and customer support.…
- **Autonomy Boundaries:** Generate government travel request draft, auto. Recommend available flights based on policy, auto. Approve or reject travel requests, human approval required. Cancel or refund issued tickets, human approval required.…
- **Escalation Triggers:** Travel request violates government travel policy or approval rules. User requests ticket cancellation, refund, or policy exception. AI confidence score falls below the defined threshold.…
- **Audit Cadence:** Real-time, AI errors, failed bookings, policy violations, confidence alerts (Operations Team). Weekly, User feedback, AI recommendations, model quality, support cases (Product Manager).…
- **Shadow AI Audit (user-side):** 3 workarounds found · 3 build candidates · adjacent spend $0/month
- **Agent Boundaries:** Travel Request Agent – Can create and validate government travel request drafts. Cannot approve or submit requests. Approval owner: Government employee.
- **Regulatory Exposure:** Saudi Personal Data Protection Law (PDPL), National Cybersecurity Authority (NCA) Essential Cybersecurity Controls (ECC), Digital Government Authority (DGA) regulations, and internal government travel policies..…

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
| # | Initiative | Strategy Component | Why It Ships Now | Confidence |
|---|---|---|---|---|
| 4 | Explain why each flight option is recommended, compliant, or excluded | Contract | Explanation is essential for trust and can be implemented using rule citations and structured recommendation reasons. | H |
| 6 | Detect incomplete or inconsistent travel-request information before submission | Bet | A bounded validation copilot delivers immediate time savings using existing forms and deterministic checks. | H |
| 8 | Create a confidence score for every AI recommendation and policy response | Contract | Confidence tiers are required before exposing probabilistic outputs to users. | M |
| 9 | Escalate low-confidence responses and policy exceptions to an authorized employee | Contract | Prevents uncertain AI outputs from becoming operational decisions. | H |
| 10 | Require human approval for approval, rejection, cancellation, refund, and booking modification | Guardrails | These boundaries must be enforced before the pilot begins. | H |
| 18 | Create an audit log showing AI input, recommendation, confidence, source, model version, and final human decision | Guardrails | Government travel requires complete traceability from the first production interaction. | H |
| 19 | Build a golden evaluation dataset covering policies, booking scenarios, exceptions, refunds, and high-risk cases | Contract | A credible evaluation baseline is required before pilot approval. | H |
| 20 | Run automated regression tests before releasing changes to models, prompts, policies, or retrieval sources | Contract | Prevents silent quality degradation when the AI system changes. | H |
| 22 | Implement role-based access controls and tenant-level data isolation for government entities | Guardrails | Entity isolation and role enforcement are mandatory prerequisites. | H |
| 23 | Define data retention, privacy, security, and model-provider usage controls for traveler information | Guardrails | Controls must be approved before sending traveler information to model providers. | H |
| 24 | Prevent AI from independently changing policies, financial rules, eligibility decisions, or approval authorities | Guardrails | Directly implements the defined autonomy boundaries. | H |
| 25 | Measure reduction in travel-request processing time after introducing AI assistance | Bet | Processing-time reduction is a primary value and pilot success metric. | H |
| 26 | Measure reduction in support tickets and repeated beneficiary inquiries | Bet | Current support volumes must be baselined before launching the assistant. | H |
| 27 | Measure improvement in policy compliance and successful self-service completion | Contract | Establishes measurable reliability and trust outcomes. | H |
| 29 | Define pilot kill criteria based on accuracy, adoption, processing-time reduction, and user trust | Bet | Numeric success and failure thresholds must be agreed before investment expands. | H |



- **Horizon 2 (Next):**
| # | Initiative | Strategy Component | Hypothesis | Kill Criteria | Confidence |
|---|---|---|---|---|---|
| 1 | Build an AI travel request assistant that drafts government travel requests from beneficiary inputs | Bet | A drafting copilot will reduce request-completion time without reducing data quality. | If we do not see at least a 30% reduction in median request-creation time by week 6, we stop or redesign the workflow. | M |
| 2 | Develop an AI policy assistant that answers travel-policy questions using approved regulations and source references | Bet | Grounded answers with citations will reduce repeated inquiries while maintaining policy accuracy. | If fewer than 85% of evaluated answers are correct, grounded, and citation-supported by week 6, we stop external rollout. | M |
| 3 | Provide AI-powered flight recommendations based on price, schedule, traveler preferences, and government policy | Bet | Policy-aware recommendations will shorten flight selection while preserving compliance. | If recommendations do not reduce selection time by 25% or achieve 70% top-three acceptance by week 6, we stop expanding the pilot. | M |
| 5 | Integrate the AI assistant with traveler profiles to reduce repetitive data entry | Bet | Pre-populating stable profile information will increase completion speed and reduce errors. | If profile integration does not reduce manually entered fields by 40% by week 6, we stop further integration work. | M |
| 7 | Validate travel requests against eligibility rules before routing them for approval | Contract | Pre-routing validation will reduce preventable rejection and rework. | If the validator fails to detect at least 90% of known eligibility issues by week 6, we stop automated exposure. | M |
| 11 | Capture user corrections, booking changes, support tickets, and satisfaction feedback for continuous improvement | Moat | Structured outcome signals will create the foundation for a proprietary learning loop. | If fewer than 50% of pilot interactions produce usable outcome or correction signals by week 6, we stop and fix instrumentation. | M |
| 15 | Provide AI-assisted comparison of compliant flights within approved price ceilings | Bet | A constrained comparison experience will deliver value with lower risk than unconstrained recommendations. | If fewer than 70% of pilot users complete selection without leaving the platform by week 6, we stop and revise the experience. | M |
| 16 | Create an AI support assistant for common booking, ticketing, cancellation, and refund inquiries | Bet | A bounded assistant will resolve repetitive questions and reduce human support demand. | If the assistant does not resolve at least 40% of eligible inquiries without escalation by week 6, we stop expansion. | M |
| 17 | Integrate AI recommendations with national carrier availability and pricing services | Bet | Real-time inventory will make AI recommendations actionable and reliable. | If fewer than 95% of recommendations remain bookable and price-consistent by week 6, we stop production exposure. | M |
| 21 | Create monitoring dashboards for recommendation quality, policy violations, latency, cost, and user satisfaction | Margin | Unified monitoring will reveal whether quality gains justify AI cost and complexity. | If the dashboard cannot attribute quality, latency, and cost to individual AI use cases by week 6, we stop scaling usage. | H |
| 28 | Pilot the AI travel assistant with selected government entities and compare results against the current process | Bet | A controlled pilot will demonstrate whether the copilot creates measurable operational value. | If the pilot does not improve at least two of accuracy, adoption, processing time, or trust by week 6, we stop broader rollout. | M |
| 30 | Integrate the AI assistant into Etimad Individuals web and mobile channels | Bet | Embedding the assistant in existing channels will achieve stronger adoption than a separate AI interface. | If embedded usage remains below 20% of eligible pilot journeys by week 6, we stop mobile expansion and reassess placement. | M |



- **Horizon 3 (Bet):**

| # | Initiative | Strategy Component | What Must Be True First | Confidence |
|---|---|---|---|---|
| 12 | Build a centralized travel intelligence layer using anonymized booking, carrier, payment, and traveler data | Moat | Data ownership, anonymization rules, common identifiers, quality standards, and cross-system access must be established. | M |
| 13 | Generate demand forecasts by destination, government entity, travel period, and carrier | Moat | The intelligence layer must contain sufficiently complete historical data, and forecast users and decisions must be identified. | L |
| 14 | Identify unusual booking patterns, repeated failures, duplicate requests, and potential policy violations | Guardrails | Event data must be standardized, false-positive tolerance agreed, and investigation ownership defined. | M |


- **Board Narrative:** **The case:**
- **Ask:** ## M1 Baseline vs. Now
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
