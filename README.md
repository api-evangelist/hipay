# HiPay

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
