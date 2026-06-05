# Alliance Data Systems (Bread Financial Holdings) (alliance-data-systems)

Alliance Data Systems Corporation (ADS) was a Plano/Columbus-based financial and marketing services holding company built in 1996 from the merger of J.C. Penney's credit card processing unit and The Limited's World Financial Network National Bank, taken public on the NYSE in 2001. The company historically operated three segments — Card Services (private label and co-brand retail credit cards), Epsilon (data-driven marketing and CRM), and LoyaltyOne (the AIR MILES Reward Program in Canada and BrandLoyalty in the Netherlands). In July 2019 ADS sold Epsilon to Publicis Groupe for $4.4 billion. In December 2020 ADS acquired Bread, a New York-based BNPL platform, for $450 million. In November 2021 ADS spun off LoyaltyOne as Loyalty Ventures Inc. (LTRN). On March 23, 2022 the remaining card-and-payments business rebranded as Bread Financial Holdings, Inc., with the common stock starting to trade on NYSE under the new ticker BFH on April 4, 2022. Today Bread Financial is a tech-forward financial services company headquartered in Columbus, Ohio (Wikipedia 2024 figures&#58; $3.84B revenue, ~6,000 employees, $22.9B total assets, 135+ managed card programs across partners including Victoria's Secret, Wayfair, Williams-Sonoma, Academy Sports, HP, PlayStation, and the Crypto.com Visa Card). The developer surface lives under the Bread Pay BNPL brand at developer-facing properties docs.breadpayments.com (legacy "bread-classic" Merchant API) and platform-docs.breadpayments.com (next-generation "BreadPay Platform" APIs, OAuth 2.0 Client Credentials, hosted on https://api.platform.breadpayments.com/api), plus a JavaScript Bread SDK (preview + production CDN), iOS/Android mobile SDKs published as the Bread Financial Brand Partners SDKs on github.com/bppub, and platform integrations for Shopify, Magento 2, WooCommerce, BigCommerce, Salesforce Commerce Cloud, Miva, Volusion, and Turbify. The corporate/holding side (private-label and co-brand cards issued through Comenity Bank and Comenity Capital Bank, plus high-yield savings, CDs, IRAs, and personal loans) is delivered through B2B partner integrations rather than a public developer portal.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/alliance-data-systems/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/alliance-data-systems/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Fintech
- Buy Now Pay Later
- BNPL
- Bread Pay
- Private Label Credit
- Co Brand Credit Cards
- Loyalty Programs
- Marketing
- Data Driven Marketing
- Payments
- Lending
- Savings
- Personal Loans
- Consumer Banking
- Retail Finance
- Fortune 500
- NYSE BFH
- Comenity Bank
- Rebrand

## Timestamps

- **Created:** 2026-04-19
- **Modified:** 2026-05-23

## APIs

### Bread Pay Platform API

Next-generation BreadPay Platform REST API for managing buyers, merchant accounts, payment options, transaction lifecycle (authorize, cancel, capture, refund), and payment-product servicing. Hosted at api.platform.breadpayments.com with a preview environment at api-preview.platform.breadpayments.com. Authentication is OAuth 2.0 Client Credentials Flow with credentials issued from the Bread Merchant Portal.

- **Human URL:** [https://platform-docs.breadpayments.com/bread-developers](https://platform-docs.breadpayments.com/bread-developers)
- **Base URL:** `https://api.platform.breadpayments.com/api`

#### Tags

- Buy Now Pay Later
- BNPL
- Payments
- Transactions
- Buyers
- Merchants

#### Properties

- [Documentation](https://platform-docs.breadpayments.com/bread-developers)
- [Concepts](https://platform-docs.breadpayments.com/bread-developers/docs)
- [Authentication](https://platform-docs.breadpayments.com/bread-developers/docs/api-access)
- [API Reference](https://platform-docs.breadpayments.com/bread-developers/reference)
- [OpenAPI](openapi/bread-pay-platform-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bread-pay-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-pay-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Sandbox Base U R L](https://api-preview.platform.breadpayments.com/api)
- [Production Base U R L](https://api.platform.breadpayments.com/api)
- [Capability](capabilities/bread-pay-platform-transactions.yaml)
- [Capability](capabilities/bread-pay-platform-buyers.yaml)

### Bread Classic Merchant API

Legacy "bread-classic" REST API for managing Bread checkout transactions, carts, shipping (carrier + tracking) and capture/refund/cancel actions from the original Bread BNPL product, still documented at docs.breadpayments.com for merchants on the prior integration. The Merchant API helps manage completed transactions and carts, which can also be created directly in the browser via the Bread JavaScript SDK.

- **Human URL:** [https://docs.breadpayments.com/bread-classic/reference/getting-started-with-your-api](https://docs.breadpayments.com/bread-classic/reference/getting-started-with-your-api)
- **Base URL:** `https://api.breadpayments.com`

#### Tags

- Buy Now Pay Later
- BNPL
- Merchant
- Transactions
- Carts
- Shipping
- Legacy

#### Properties

- [Documentation](https://docs.breadpayments.com/bread-classic/reference)
- [Getting Started](https://docs.breadpayments.com/bread-classic/reference/getting-started-with-your-api)
- [Checkout](https://docs.breadpayments.com/bread-classic/docs/bread-checkout)
- [Testing](https://docs.breadpayments.com/bread-classic/docs/testing-bread)
- [Managing Transactions](https://docs.breadpayments.com/bread-classic/docs/managing-bread-transactions)
- [OpenAPI](openapi/bread-classic-merchant-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bread-classic-merchant.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-classic-merchant.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Capability](capabilities/bread-classic-transactions.yaml)

### Bread JavaScript SDK

Browser-side JavaScript SDK that exposes the BreadPayments object for rendering the Bread modal, embedded placements, prequalification, and cart/checkout flows on merchant sites. Loaded from Bread CDNs in preview and production environments and initialized with a merchant integrationKey plus buyer object.

- **Human URL:** [https://platform-docs.breadpayments.com/bread-onboarding/docs/bread-sdk-installation](https://platform-docs.breadpayments.com/bread-onboarding/docs/bread-sdk-installation)
- **Base URL:** `https://connect.breadpayments.com`

#### Tags

- SDK
- JavaScript
- Web
- Checkout
- Placements
- Prequalification

#### Properties

- [Documentation](https://platform-docs.breadpayments.com/bread-onboarding/docs/bread-sdk-installation)
- [Preview C D N](https://connect-preview.breadpayments.com/sdk.js)
- [Production C D N](https://connect.breadpayments.com/sdk.js)
- [Unified S D K Overview](https://platform-docs.breadpayments.com/bread-onboarding/docs/unified-sdk-overview)
- [Postman Collection](collections/bread-classic-merchant.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-classic-merchant.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/bread-pay-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-pay-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bread Financial Brand Partners iOS SDK

Official Bread Financial mobile SDK for iOS published as breadfinancial-brand-partners-ios on the bppub GitHub organization. Provides batch prescreen, unified prequalification, placement rendering, application callbacks, and customer status events for native iOS apps.

- **Human URL:** [https://github.com/bppub/breadfinancial-brand-partners-ios](https://github.com/bppub/breadfinancial-brand-partners-ios)
- **Base URL:** `https://github.com/bppub`

#### Tags

- SDK
- Mobile
- iOS
- Swift
- Prequalification
- Placements

#### Properties

- [Repository](https://github.com/bppub/breadfinancial-brand-partners-ios)
- [Alternate Swift Repo](https://github.com/bppub/breadfinancial-brand-partners-ios-swift)
- [Documentation](https://platform-docs.breadpayments.com/bread-onboarding)
- [Postman Collection](collections/bread-classic-merchant.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-classic-merchant.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/bread-pay-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-pay-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bread Financial Brand Partners Android SDK

Official Bread Financial mobile SDK for Android (Kotlin) published as breadfinancial-brand-partners-android on the bppub GitHub organization. Provides batch prescreen, unified prequalification, placement rendering, application callbacks, and customer status events for native Android apps.

- **Human URL:** [https://github.com/bppub/breadfinancial-brand-partners-android](https://github.com/bppub/breadfinancial-brand-partners-android)
- **Base URL:** `https://github.com/bppub`

#### Tags

- SDK
- Mobile
- Android
- Kotlin
- Prequalification
- Placements

#### Properties

- [Repository](https://github.com/bppub/breadfinancial-brand-partners-android)
- [Documentation](https://platform-docs.breadpayments.com/bread-onboarding)
- [Postman Collection](collections/bread-classic-merchant.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-classic-merchant.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/bread-pay-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-pay-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bread Webhooks

Outbound webhook system for the BreadPay Platform that notifies merchant systems of transaction lifecycle events. Documented under the BreadPay developer site with setup, concepts, validation, and client implementation guides.

- **Human URL:** [https://platform-docs.breadpayments.com/bread-developers/docs](https://platform-docs.breadpayments.com/bread-developers/docs)
- **Base URL:** `https://platform-docs.breadpayments.com/bread-developers/docs`

#### Tags

- Webhooks
- Events
- Transactions
- Eventing

#### Properties

- [Documentation](https://platform-docs.breadpayments.com/bread-developers/docs)
- [Postman Collection](collections/bread-classic-merchant.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-classic-merchant.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/bread-pay-platform.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bread-pay-platform.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.breadfinancial.com)
- [Former Website](https://www.alliancedata.com)
- [B N P L Website](https://www.breadpayments.com)
- [Business Solutions](https://www.breadfinancial.com/en/business-solutions.html)
- [Buy Now Pay Later](https://www.breadfinancial.com/en/business-solutions/buy-now-pay-later.html)
- [Newsroom](https://newsroom.breadfinancial.com)
- [Investor Relations](https://investor.breadfinancial.com)
- [S E C Rebrand Filing](https://www.sec.gov/Archives/edgar/data/0001101215/000110121522000058/form_8-k.htm)
- [Wikipedia Page](https://en.wikipedia.org/wiki/Bread_Financial)
- [Developer Portal](https://platform-docs.breadpayments.com/bread-developers)
- [Classic Developer Portal](https://docs.breadpayments.com/bread-classic/reference)
- [Onboarding Docs](https://platform-docs.breadpayments.com/bread-onboarding)
- [GitHub Organization](https://github.com/bppub)
- [Integrations Git Hub Organization](https://github.com/breadfinance)
- [Legacy Git Hub Organization](https://github.com/getbread)
- [A P I Tracker](https://apitracker.io/a/breadpayments)
- [LinkedIn](https://www.linkedin.com/company/bread-financial)
- [Plans](plans/alliance-data-systems-plans-pricing.yml)
- [Rate Limits](rate-limits/alliance-data-systems-rate-limits.yml)
- [Fin Ops](finops/alliance-data-systems-finops.yml)
- [Vocabulary](vocabulary/alliance-data-systems-vocabulary.yml)
- [J S O N L D Context](json-ld/alliance-data-systems-context.jsonld)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
