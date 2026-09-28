# order-fulfillment-service
 
Core order orchestration microservice responsible for cart checkout, warehouse dispatch, and invoice generation.
 
## Overview & Metadata
- **Service Owner:** Logistics & Supply Chain Engineering Team (`#eng-logistics-team` on Slack)
- **Business Impact:** Critical (Tier 1 core customer-facing checkout system)
- **Code Coverage Goal:** 80% (enforced via JaCoCo in CI gate)
 
## Architecture & Integrations
- **Upstream Dependencies:** Calls internal `inventory-mgmt-service`, `payment-gateway-service`, and `notification-service`.
- **Downstream Consumers:** Consumed by `web-storefront-bff`, `mobile-app-gateway`, and `warehouse-sync-cron`.
- **External APIs:** SendGrid Email API, FedEx Shipping REST API.
- **Observability / Logging:** Datadog APM, Prometheus Actuator metrics, Logstash / ELK stack.
 
## Links & Operations
- **API Documentation:** [Swagger / OpenAPI UI](https://api-docs.internal.company.com/order-fulfillment/swagger-ui/index.html)
- **JIRA Project Board:** [LOG-ORDER Board](https://jira.internal.company.com/projects/LOG)
- **On-Call Rotation:** [PagerDuty Escalation Policy](https://pagerduty.internal.company.com/schedules/LOGISTICS_ONCALL)
