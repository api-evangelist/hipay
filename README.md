# HiPay

HiPay is a European omnichannel payment platform headquartered in Levallois-Perret, France, listed on Euronext Growth Paris. Founded in 2011 and authorized as a Payment Institution by the ACPR, HiPay processes over €7.5 billion in transactions annually for merchants across Europe with offices in France, Italy, Belgium, and Portugal.

HiPay provides REST APIs covering the full payment lifecycle: online payments via hosted page, hosted fields, and direct server-to-server integration; in-store POS terminal management; payment card tokenization and Secure Vault storage; marketplace split payment management with KYC/KYB onboarding; settlement and financial reporting; Apple Pay web integration; and server-to-server webhook notifications for transaction status events.

**Developer Portal:** https://developer.hipay.com  
**OpenAPI Specifications:** https://github.com/hipay/openapi-hipay  
**Support:** https://support.hipay.com

## APIs

| API | Description | OpenAPI |
|-----|-------------|---------|
| Payment Gateway API (v3) | Order and transaction queries, available payment product discovery | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/enterprise/api-gateway.yml) |
| Enterprise Gateway API (v1) | Order creation, transaction retrieval, capture/refund/cancel | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/enterprise/gateway.yaml) |
| Enterprise HostedPage API | Hosted payment page creation and redirect | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/enterprise/hpayment.yaml) |
| Enterprise Finance API | Settlement listing, details, and file export | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/enterprise/settlement.yaml) |
| Enterprise Tokenization API | Card tokenization CRUD in HiPay Secure Vault | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/enterprise/tokenization.yaml) |
| Apple Pay Web API | Apple Pay payment session creation | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/enterprise/applepay-web.yaml) |
| POS API | In-store terminal wake-and-pay for omnichannel | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/omnichannel/pos_api.yaml) |
| Omnichannel Gateway API | In-store order and transaction management | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/omnichannel/omnichannel.yaml) |
| Marketplace API | Marketplace account management, KYC, transfers, withdrawals | [yaml](https://raw.githubusercontent.com/hipay/openapi-hipay/master/marketplace/marketplace.yaml) |

## Authentication

All HiPay APIs use HTTP Basic Authentication with API credentials obtained from the HiPay Enterprise or Professional back office. Credentials are encoded as `base64(API_login:API_password)` in the `Authorization` header. The Payment Gateway API v3 also supports an `X-API-KEY` header.

## Environments

| Environment | Notes |
|-------------|-------|
| Stage | Available for integration testing; credentials separate from production |
| Production | Live transaction processing; credentials from HiPay back office |

## Resources

- [apis.yml](apis.yml) — APIs.json 0.19 machine-readable catalog
- [plans/plans.yml](plans/plans.yml) — Commercial plan information
- [rate-limits/rate-limits.yml](rate-limits/rate-limits.yml) — Rate limit documentation
- [finops/finops.yml](finops/finops.yml) — FinOps cost model and optimization guidance
