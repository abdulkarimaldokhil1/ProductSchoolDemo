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


## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| | | | Y/N | active / broken / missing |
| | | | Y/N | active / broken / missing |
| | | | Y/N | active / broken / missing |

**Broken loop identified by partner:**
**Fix plan:**

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
