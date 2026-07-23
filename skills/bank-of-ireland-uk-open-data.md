---
name: Query Bank of Ireland (UK) Open Data (branches, ATMs, products)
description: Read public, unauthenticated OBIE Open Data - branch/ATM locations and product reference data - no credentials required.
api: openapi/bank-of-ireland-uk-open-data-openapi.json
operations: [GET /branches, GET /atms, GET /personal-current-accounts, GET /business-current-accounts, GET /unsecured-sme-loans, GET /commercial-credit-cards]
---

# Query Open Data (public, no auth)

Use this to read Bank of Ireland (UK) reference data with no credentials. This is
the OBIE Open Data Standard served live at
`https://openapi.bankofireland.com/open-banking/v2.2`.

## Content negotiation (important)
- Send **no `Accept` header** or `Accept: */*`. An explicit
  `Accept: application/json` returns **HTTP 406**.
- Use HTTP GET; HEAD is also supported. `If-Modified-Since` / `If-None-Match`
  enable conditional requests.

## Steps (each returns HTTP 200)
1. `GET /branches` — branch locations, opening hours, accessibility.
2. `GET /atms` — ATM locations and services (payload `BrandName` = "Bank of Ireland (UK) plc").
3. `GET /personal-current-accounts` — PCA product reference data.
4. `GET /business-current-accounts` — BCA product reference data.
5. `GET /unsecured-sme-loans` — unsecured SME loan products.
6. `GET /commercial-credit-cards` — commercial credit card products.

## Notes
- Data is licensed under the OBIE Open Licence (https://www.openbanking.org.uk/open-licence).
- v2.2 is live; v2.3/v3.0 paths returned 503 at review time.
