# Cost Curve & Pricing Strategy

**leader :**
AI-powered, policy-compliant travel recommendations that help users select the most suitable flight based on eligibility rules, framework agreements, fare limits, and traveler needs.

**Filler :**
AI-generated summaries, translations, smart notifications, and simple travel insights that improve the user experience at a low additional cost.
**Killer:**
Autonomous booking, continuous fare monitoring, automatic rebooking, and complex agentic workflows across multiple carriers and government systems.

**Killer usage :**
Approximately 20–30% of users.

**Bundle or add-on:**
Add-on, because the expected usage is below 70% and the feature has high inference and integration costs.

## Cost Model


| Feature | Complexity | Model Tier | Cost/Req | Volume % | Weighted Cost |
|---------|------------|------------|---------:|---------:|--------------:|
| Travel FAQs, summaries, and notifications | Low | Claude Haiku 4.5 | **$0.009** | **40%** | **$0.0036** |
| Travel-policy and eligibility validation | Medium | Claude Sonnet 5 | **$0.018** | **35%** | **$0.0063** |
| Multi-carrier recommendations and exception handling | Complex | Claude Opus 5 | **$0.045** | **25%** | **$0.0113** |
| **Blended** |  |  |  | **100%** | **$0.0212 ≈ $0.02** |


## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->
## Cascading Strategy

**Triage model:** Claude Haiku 4.5  
**Mid-tier model:** Claude Sonnet 5  
**Frontier model:** Claude Opus 5  

**Routing rule:**  
Route simple and repetitive requests (FAQs, summaries, translations, and notifications) to Claude Haiku 4.5. Route policy validation and eligibility checks to Claude Sonnet 5. Route complex travel recommendations, multi-carrier comparisons, exceptional cases, and multi-step reasoning to Claude Opus 5.

**Expected cascade ratio:** **40% / 35% / 25%**

- **40%** → Claude Haiku 4.5 (Low complexity)
- **35%** → Claude Sonnet 5 (Medium complexity)
- **25%** → Claude Opus 5 (High complexity)

**Blended cost per request:** **≈ $0.021 ($0.02)**

**Triage model:**
A small, cost-efficient language model for request classification, intent detection, FAQs, summaries, translations, and simple travel queries.
**Frontier model:**
An advanced reasoning model for complex travel recommendations, government policy interpretation, multi-carrier comparisons, and exceptional travel cases.
**Routing rule:**
Simple, repetitive, and low-risk requests are routed to the triage model. Requests involving complex policies, multiple travel constraints, low confidence, sensitive cases, or multi-step reasoning are routed to the frontier model.
**Expected cascade ratio:**
40% routed to the lower-cost model, with a future target of 60–70% where quality permits.

## Pricing Model

Current pricing:

N/A – The AI capability is not currently priced as a standalone service.

Proposed AI pricing:

**Strategy posture:**
Penetration
**Pricing model:**
Hybrid — subscription plus usage-based pricing
**Unit of work metered:**
Government travel request completed
**Base fee ($/user/month):**
 $10
**Price per unit:**
$20
**Estimated units/user/month:**
1
**Implied revenue/user/month:**
$30.00


Decision Note — Why this pricing structure fits the buyer and the value delivered:
The base fee provides predictable access to standard AI capabilities, while usage-based pricing aligns revenue with actual consumption. At an estimated 80 AI requests per user per month, the model generates approximately $40 per user while protecting margins as usage increases.

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
