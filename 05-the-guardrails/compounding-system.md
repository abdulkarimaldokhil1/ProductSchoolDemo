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
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
