# Bank of Ireland (UK) (bank-of-ireland-uk)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
