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
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** **The case:**
- **Ask:** ## M1 Baseline vs. Now
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)
