# Bank of Ireland (UK) (bank-of-ireland-uk)

Bank of Ireland (UK) plc is the UK banking arm of Bank of Ireland Group plc, Ireland's oldest bank (founded 1783), headquartered in Dublin. In the United Kingdom it is authorised by the Prudential Regulation Authority and regulated by the Financial Conduct Authority and the PRA. As one of the nine CMA-mandated banks (the CMA9) it participates fully in the UK Open Banking programme under PSD2, publishing a public Open Data API and the OBIE Read/Write API family through its Developer Hub.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bank-of-ireland-uk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bank-of-ireland-uk/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Banking
- Open Banking
- PSD2
- OBIE
- CMA9
- United Kingdom
- Payments
- Account Information
- Open Data
- FAPI
- Fintech

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

### Bank of Ireland (UK) Open Data API

Public, unauthenticated OBIE Open Data API serving reference data for ATMs, branches, personal current accounts, business current accounts, unsecured SME loans and commercial credit cards. Confirmed live (HTTP 200) at the v2.2 base on 2026-07-23.

- **Human URL:** [https://developer.bankofireland.com/](https://developer.bankofireland.com/)
- **Base URL:** `https://openapi.bankofireland.com/open-banking/v2.2`

#### Tags

- Open Data
- ATMs
- Branches

#### Properties

- [OpenAPI](openapi/bank-of-ireland-uk-open-data-openapi.json) — OBIE Open Data Standard (shared specification)
- [Documentation](https://developer.bankofireland.com/)
- [API Reference](https://openbankinguk.github.io/opendata-api-docs-pub/v2.4.0/)
- [Open Licence](https://www.openbanking.org.uk/open-licence)

### Bank of Ireland (UK) Account & Transaction Information API

OBIE Read/Write Account & Transaction Information (AIS) API allowing authorised AISPs to access account, balance, transaction, standing order, direct debit and product data with customer consent. FAPI-secured (OAuth2/OIDC, PSD2 SCA, mTLS).

- **Human URL:** [https://developer.bankofireland.com/](https://developer.bankofireland.com/)
- **Base URL:** `https://api.obapi.bankofireland.com/open-banking/v3.1/aisp`

#### Tags

- Account Information
- AISP
- Read/Write

#### Properties

- [OpenAPI](openapi/bank-of-ireland-uk-account-info-openapi.yaml) — OBIE Read/Write Standard (shared specification)
- [Documentation](https://developer.bankofireland.com/)

### Bank of Ireland (UK) Payment Initiation API

OBIE Read/Write Payment Initiation (PIS) API enabling authorised PISPs to initiate domestic and international single, scheduled, standing-order and file payments with customer consent. FAPI-secured.

- **Human URL:** [https://developer.bankofireland.com/](https://developer.bankofireland.com/)
- **Base URL:** `https://api.obapi.bankofireland.com/open-banking/v3.1/pisp`

#### Tags

- Payments
- Payment Initiation
- PISP

#### Properties

- [OpenAPI](openapi/bank-of-ireland-uk-payment-initiation-openapi.yaml) — OBIE Read/Write Standard (shared specification)
- [Documentation](https://developer.bankofireland.com/)

### Bank of Ireland (UK) Confirmation of Funds API

OBIE Read/Write Confirmation of Funds (CBPII) API allowing authorised card-based payment instrument issuers to confirm the availability of funds with customer consent. FAPI-secured.

- **Human URL:** [https://developer.bankofireland.com/](https://developer.bankofireland.com/)
- **Base URL:** `https://api.obapi.bankofireland.com/open-banking/v3.1/cbpii`

#### Tags

- Confirmation of Funds
- CBPII
- Read/Write

#### Properties

- [OpenAPI](openapi/bank-of-ireland-uk-confirmation-funds-openapi.yaml) — OBIE Read/Write Standard (shared specification)
- [Documentation](https://developer.bankofireland.com/)

### Bank of Ireland (UK) Dynamic Client Registration API

OBIE Dynamic Client Registration (DCR) API documented on the Developer Hub for onboarding TPP applications using OBIE/eIDAS certificates.

- **Human URL:** [https://developer.bankofireland.com/](https://developer.bankofireland.com/)
- **Base URL:** `https://auth.obapi.bankofireland.com/oauth/as/b365/`

#### Tags

- Dynamic Client Registration
- Onboarding
- OAuth2

#### Properties

- [Documentation](https://eu1.anypoint.mulesoft.com/exchange/portals/bankofireland/pages/Getting%20Started/)

## Common Properties

- [Website](https://www.bankofirelanduk.com/)
- [Developer Portal](https://developer.bankofireland.com/)
- [Portal (MuleSoft Anypoint)](https://eu1.anypoint.mulesoft.com/exchange/portals/bankofireland/)
- [Status Page / FCA API Statistics](https://www.bankofirelanduk.com/personal/api-statistics/)
- [LinkedIn](https://www.linkedin.com/company/bank-of-ireland/)
- [Privacy Policy](https://www.bankofirelanduk.com/site-links/privacy/)
- [Support](https://www.bankofirelanduk.com/help-and-support/)
- [Open Licence](https://www.openbanking.org.uk/open-licence)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
