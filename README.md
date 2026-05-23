# Alliance Data Systems (Bread Financial Holdings)

Alliance Data Systems Corporation (ADS) was a financial-and-marketing-services holding company built in 1996 from the merger of J.C. Penney's credit card processing unit and The Limited's World Financial Network National Bank, taken public on the NYSE in 2001. The company historically operated three segments: **Card Services** (private label and co-brand retail credit cards), **Epsilon** (data-driven marketing and CRM), and **LoyaltyOne** (the AIR MILES Reward Program in Canada and BrandLoyalty in the Netherlands).

The corporation no longer exists under the Alliance Data name. The remaining card-and-payments business **rebranded as Bread Financial Holdings, Inc. on March 23, 2022**, and the common stock began trading on the NYSE under the new ticker **BFH on April 4, 2022**.

## Corporate Timeline

| Date | Event |
|---|---|
| December 1996 | Alliance Data Systems formed via merger of JCPenney credit card unit and The Limited's World Financial Network National Bank |
| 2001 | IPO on NYSE under ticker ADS |
| July 2019 | **Epsilon** sold to Publicis Groupe for $4.4 billion |
| December 2020 | Acquired **Bread** (NYC-based BNPL platform) for $450 million |
| November 2021 | Spun off **LoyaltyOne** as Loyalty Ventures Inc. (NASDAQ: LTRN) — included AIR MILES + BrandLoyalty |
| March 23, 2022 | Rebranded as **Bread Financial Holdings, Inc.** |
| April 4, 2022 | Common stock starts trading on NYSE as **BFH** |

## Current Business (as Bread Financial)

Headquartered in Columbus, Ohio. 2024 scale per Wikipedia: ~$3.84B revenue, ~6,000 employees, $22.9B total assets, **135+ managed card programs** across partners including Victoria's Secret, Wayfair, Williams-Sonoma, Pottery Barn, Academy Sports + Outdoors, HP, PlayStation, and the Crypto.com Visa Card. Cards are issued through the regulated subsidiaries **Comenity Bank** and **Comenity Capital Bank**.

Bread Financial also publishes per its own business-solutions page: $27B in annual sales across 35.6M open unique customers with a 90% partner renewal rate.

Product lines:

- **Branded Credit Cards** — private label + co-brand cards for retail partners
- **Bread Pay** BNPL — SplitPay (4 interest-free payments) and Installments (3–48 months)
- **Direct-to-Consumer** — Bread Cashback and Bread Rewards proprietary cards, high-yield savings, CDs, IRAs, personal loans
- **Business Solutions** — branded credit cards and financing for merchants

## Developer Surface

The only public developer surface is under the **Bread Pay** BNPL brand:

| API / SDK | Purpose | URL |
|---|---|---|
| Bread Pay Platform API | Next-gen REST API (OAuth 2.0 client_credentials) for buyers, transactions, payment options | https://platform-docs.breadpayments.com/bread-developers |
| Bread Classic Merchant API | Legacy bread-classic API for carts, transactions, shipping | https://docs.breadpayments.com/bread-classic/reference |
| Bread JavaScript SDK | Browser SDK for modals, placements, prequalification | https://platform-docs.breadpayments.com/bread-onboarding/docs/bread-sdk-installation |
| Bread Financial Brand Partners iOS SDK | Native iOS Swift mobile SDK | https://github.com/bppub/breadfinancial-brand-partners-ios |
| Bread Financial Brand Partners Android SDK | Native Android Kotlin mobile SDK | https://github.com/bppub/breadfinancial-brand-partners-android |
| Bread Webhooks | Outbound transaction lifecycle events | https://platform-docs.breadpayments.com/bread-developers/docs |

Base URLs:

- Bread Pay Platform production: `https://api.platform.breadpayments.com/api`
- Bread Pay Platform preview/sandbox: `https://api-preview.platform.breadpayments.com/api`
- Bread JS SDK CDN: `https://connect.breadpayments.com/sdk.js` (preview: `https://connect-preview.breadpayments.com/sdk.js`)

Platform integrations: Shopify, Magento 2, WooCommerce, BigCommerce, Salesforce Commerce Cloud, Miva, Volusion, Turbify.

GitHub orgs: [github.com/bppub](https://github.com/bppub) (active publisher of mobile SDKs and platform releases), [github.com/breadfinance](https://github.com/breadfinance) (payment-icons library), [github.com/getbread](https://github.com/getbread) (legacy, includes `magento-v2-bread`).

The corporate/holding side (private-label card programs, savings products, personal loans) is delivered through B2B partner integrations rather than a public developer portal.

## Artifacts in this Repository

- [apis.yml](./apis.yml) — APIs.json index
- `openapi/` — OpenAPI 3.1 specs for [Bread Pay Platform](./openapi/bread-pay-platform-openapi.yml) and [Bread Classic Merchant](./openapi/bread-classic-merchant-openapi.yml)
- `capabilities/` — Naftiko capabilities for [transactions](./capabilities/bread-pay-platform-transactions.yaml), [buyers](./capabilities/bread-pay-platform-buyers.yaml), [classic](./capabilities/bread-classic-transactions.yaml), plus the [BNPL workflow composition](./capabilities/bnpl-checkout-workflow.yaml)
- `examples/` — request/response examples for create/get/authorize/refund transaction, get buyer, and Bread Classic cart + shipping
- `json-schema/` — entity schemas for Transaction, Buyer, Address, Amount, PaymentOption, Cart, CartItem, ClassicTransaction, Shipping
- `json-structure/` — JSON Structure variants of the same entities
- `json-ld/` — [alliance-data-systems-context.jsonld](./json-ld/alliance-data-systems-context.jsonld) mapping to schema.org and the bread:/ads: vocabularies
- `vocabulary/` — [alliance-data-systems-vocabulary.yml](./vocabulary/alliance-data-systems-vocabulary.yml) — corporate + operational + capability taxonomy
- `rules/` — Spectral rulesets for [Bread Pay Platform](./rules/bread-pay-platform-rules.yml) and [Bread Classic](./rules/bread-classic-merchant-rules.yml)
- `plans/` — [merchant + consumer plan layout](./plans/alliance-data-systems-plans-pricing.yml)
- `rate-limits/` — [throttling notes](./rate-limits/alliance-data-systems-rate-limits.yml)
- `finops/` — [FOCUS-aligned billing model](./finops/alliance-data-systems-finops.yml)

## Links

- [Bread Financial corporate](https://www.breadfinancial.com)
- [Bread Pay BNPL marketing site](https://www.breadpayments.com)
- [Business Solutions / BNPL](https://www.breadfinancial.com/en/business-solutions/buy-now-pay-later.html)
- [Newsroom](https://newsroom.breadfinancial.com)
- [Investor Relations](https://investor.breadfinancial.com)
- [SEC 8-K announcing the rebrand](https://www.sec.gov/Archives/edgar/data/0001101215/000110121522000058/form_8-k.htm)
- [Wikipedia: Bread Financial](https://en.wikipedia.org/wiki/Bread_Financial)
- [Developer portal (Bread Pay Platform)](https://platform-docs.breadpayments.com/bread-developers)
- [Legacy developer portal (bread-classic)](https://docs.breadpayments.com/bread-classic/reference)
- [Onboarding docs](https://platform-docs.breadpayments.com/bread-onboarding)
- [API Tracker profile](https://apitracker.io/a/breadpayments)
