# Compounding System Design




## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | User feedback, booking corrections, support tickets, CSAT | Improved AI recommendations, updated business rules, and enhanced user experience | Y | active |
| Cross-Domain Transfer | Booking, traveler, payment, and carrier data | Better recommendations and smarter decisions across booking, payments, and traveler management | Y | active |
| Network Intelligence | Aggregated travel patterns across government entities and carriers | Demand forecasting, travel insights, and policy optimization | N | missing |

**Broken loop identified by partner:** Network Intelligence is missing. Travel patterns and performance data are collected but are not fed back into a centralized intelligence layer to continuously optimize recommendations, forecasting, and policy decisions.
**Fix plan:** Build a centralized analytics and AI feedback pipeline that aggregates anonymized travel, carrier, and payment data to generate demand forecasts, optimize policies, and continuously improve recommendations across the platform.

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** Booking data flows to financial claims, payment processing, traveler management, customer support, and product analytics. User feedback and operational metrics are reviewed by the product team to improve business rules and service quality.

**Where it silos:** Carrier performance insights, traveler behavior, and support feedback are not yet consolidated into a shared AI knowledge layer. Learning remains distributed across teams instead of continuously improving the entire platform.



## Governance Policy

**Scope:** AI capabilities used within the ERCAB platform for government travel request creation, booking recommendations, policy validation, traveler assistance, and customer support. Excludes: Internal analytics, development tools, offline reporting, and third-party AI systems that operate outside the ERCAB platform.

**Autonomy boundaries:** Generate government travel request draft, auto. Recommend available flights based on policy, auto. Approve or reject travel requests, human approval required. Cancel or refund issued tickets, human approval required. Modify travel policy or financial rules, never auto.

**Escalation triggers:** Travel request violates government travel policy or approval rules. User requests ticket cancellation, refund, or policy exception. AI confidence score falls below the defined threshold. Financial claim or payment validation fails. User requests to speak with a human agent. Multiple failed booking attempts for the same request. Missing or inconsistent traveler or government entity information.

**Audit cadence:** Real-time, AI errors, failed bookings, policy violations, confidence alerts (Operations Team). Weekly, User feedback, AI recommendations, model quality, support cases (Product Manager). Monthly, Governance compliance, AI performance, security and audit reports (AI Governance Lead).

**Regulatory exposure (EU AI Act / other):** Saudi Personal Data Protection Law (PDPL), National Cybersecurity Authority (NCA) Essential Cybersecurity Controls (ECC), Digital Government Authority (DGA) regulations, and internal government travel policies.. Risk tier: limited. Controls: Personal data masking where applicable, role-based access control (RBAC), audit logging, human approval for high-impact decisions, encrypted data transmission, policy validation before recommendations, and continuous monitoring of AI performance..

## Agent Topology

Travel Request Agent – Can create and validate government travel request drafts. Cannot approve or submit requests. Approval owner: Government employee.

Flight Recommendation Agent – Can search available flights, compare options, and recommend policy-compliant itineraries. Cannot issue tickets or override travel policies. Approval owner: Government employee.

Booking Agent – Can prepare booking details and reserve eligible itineraries. Cannot issue, cancel, or refund tickets without approval. Approval owner: Authorized booking officer.

Policy Validation Agent – Can verify compliance with government travel policies and highlight violations. Cannot approve policy exceptions. Approval owner: Business owner.

Financial Validation Agent – Can validate financial eligibility, payment status, and claim information. Cannot approve payments or financial claims. Approval owner: Financial officer.

Customer Support Agent – Can answer travel inquiries, explain policies, and provide booking status. Cannot make financial decisions or modify official records. Approval owner: Customer support supervisor.


## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|---|---|---|---|
| External AI tools used to compare flight options before booking | ERCAB Product Team | M | Govern |
| ChatGPT used to explain government travel policies | ERCAB Product Team | H | Govern |
| Word or Excel used to prepare travel request drafts before submission | ERCAB Product Team | M | Keep |

**Total tools found:** 3  
**Tools after triage:** 3  
**Estimated hidden spend:** $0/month

**Total tools found:** 3  
**Tools after triage:** 3  
**Estimated hidden spend:** $0/month




Shadow AI Audit (user-side), Module 5

## Discover, User-Side Workarounds
- Users manually compare flight options using external AI tools before booking. | source: Support ticket | signal: Capability gap | freq: M | spend: $$0/mo | decision: Build
- Users ask ChatGPT to explain government travel policies instead of using the platform. | source: Support ticket | signal: Workflow gap | freq: M | spend: $$0/mo | decision: Build
- Users manually prepare travel request drafts in Word or Excel before submitting them. | source: Support ticket | signal: Workflow gap | freq: M | spend: $$0/mo | decision: Build

## Pattern Assessment
- Workarounds found: 3
- Build candidates: 3
- Partner candidates: 0
- Ignore decisions: 0
- Adjacent spend: $0/mo
- Dominant signal: Workflow gap

## Action Plan
### Build
1. Flight comparison: Build an AI-powered comparison experience that evaluates available flights based on price, schedule, travel policy, and traveler preferences.
2. Policy assistant: Add an in-platform AI assistant that explains government travel policies, provides cited guidance, and escalates exceptions to authorized employees.
3. Travel request drafting: Enable users to generate a structured travel request draft from natural-language input, with human review before submission.

Suggested sequence: Start with travel request drafting, followed by the policy assistant, then launch intelligent flight comparison after validating data quality and recommendation accuracy.

### Partner
No external partnership is currently required. Core capabilities should be embedded within ERCAB, while approved model providers and carrier APIs may be used as enabling technology under existing security and governance controls.

### Ignore + Monitor
No workaround is currently classified as ignore. Continue monitoring support tickets, user interviews, AI tool usage, and workflow analytics to identify low-frequency workarounds that may not justify native development.

## Roadmap Brief
Based on your audit: 3 user-side workarounds discovered.
Decisions: 3 build · 0 partner · 0 ignore · 0 TBD.
Estimated adjacent spend: $0/mo across surveyed users.
Dominant signal: Workflow gap.

Recommended next step: Workflow gaps dominate, your users are stitching your product into multi-step pipelines. Strongest near-term move is partner integrations with the AI tools they already chain in.

Sequence the Build column by frequency × strategic relevance. Confirm Partner candidates with the external tools' partnership teams. Re-run this audit each quarter, workarounds shift fast.

