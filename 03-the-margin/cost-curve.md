# Cost Curve & Pricing Strategy

**leader :**

**Filler :**

**Killer:**

**Killer usage :**

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $1.00 | Complex travel recommendations, policy validation, fare comparison, and exception handling. |
| Inference (cascading/triage) | $0.20 | Classification, routing, summaries, FAQs, and low-complexity requests handled by a smaller model. |
| Infrastructure | $0.20 |  API gateway, monitoring, security, integrations, and model orchestration.|
| Data/storage |  $0.10| Logs, embeddings, travel-policy knowledge base, and conversation storage. |
| Human-in-the-loop |  $0.10|  Limited review of exceptional, sensitive, or low-confidence cases.|
| **Total AI COGS** | $1.60|  Based on 80 AI requests per user per month at a blended cost of $0.02 per request. |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:**
A small, cost-efficient language model for request classification, intent detection, FAQs, summaries, translations, and simple travel queries.
**Frontier model:**
An advanced reasoning model for complex travel recommendations, government policy interpretation, multi-carrier comparisons, and exceptional travel cases.
**Routing rule:**
Simple, repetitive, and low-risk requests are routed to the triage model. Requests involving complex policies, multiple travel constraints, low confidence, sensitive cases, or multi-step reasoning are routed to the frontier model.
**Expected cascade ratio:**
40% routed to the lower-cost model, with a future target of 60–70% where quality permits.

## Pricing Model

**Current pricing:**
$40 per user/month, used as an internal value or funding proxy for the AI-enabled ERCAB service.
**Proposed AI pricing:**
Core AI capabilities should remain included in the standard service with reasonable usage limits. High-cost capabilities, such as autonomous booking, continuous fare monitoring, and complex agentic workflows, should be controlled through quotas or usage-based charging.
**Model:** seat-based / usage-based / outcome-based / hybrid
Hybrid — seat-based for standard AI capabilities and usage-based for high-cost workflows.

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | Gross margin decreases from 46% to 38%. AI COGS increases from $1.60 to $4.80 per user/month. | Increase model cascading, route simple requests to lower-cost models, optimize prompts and token usage, and reserve the frontier model for complex cases. |
| Heaviest segment doubles | Gross margin decreases from 46% to 42%. AI COGS increases to $3.20 per heavy user/month. | Introduce usage limits and monitoring, apply usage-based controls for high-cost workflows, and separate heavy AI features from the standard service. |
| Model provider raises prices 50% | AI COGS increases from $1.60 to $2.40, reducing gross margin from 46% to approximately 44%. | Use a multi-model strategy, negotiate enterprise pricing, reduce provider dependency, and prepare a fallback model that can be activated if prices increase. |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
