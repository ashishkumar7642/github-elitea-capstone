# payment-gateway-service
 
Core payment orchestration engine handling checkout transactions, tokenization, and webhooks for global web and mobile storefronts.
 
## Overview & Metadata
- **Service Owner:** Checkout & Payments Squad (`#team-checkout-core` on Slack)
- **Business Impact:** Critical (Tier 1 revenue-generating service)
- **Code Coverage Goal:** 85% minimum enforced on PR merges
 
## Architecture & Integrations
- **Upstream Dependencies:** Calls internal `Account-Service`, `Tax-Calculation-Service`, and AWS S3.
- **Downstream Consumers:** Consumed by `Storefront-Web-Client`, `Mobile-Checkout-BFF`, and `Subscription-Worker`.
- **External APIs:** Stripe API, PayPal REST SDK.
- **Observability / Logging:** Datadog APM, Winston JSON logger, Splunk log aggregator.
 
## Links & Operations
- **API Documentation:** [Swagger / OpenAPI Hub](https://api-docs.internal.company.com/payment-gateway)
- **JIRA Project Board:** [PAY-CORE Board](https://jira.internal.company.com/projects/PAY)
- **On-Call Rotation:** [PagerDuty Escalation Policy](https://pagerduty.internal.company.com/schedules/PAYMENT_OPS)
