---
name: Read a customer's accounts and transactions (Bank of Ireland UK AIS)
description: Consent-driven read of a PSU's account, balance and transaction data over the OBIE Account & Transaction Information API.
api: openapi/bank-of-ireland-uk-account-info-openapi.yaml
operations: [CreateAccountAccessConsents, GetAccountAccessConsentsConsentId, GetAccounts, GetAccountsAccountId, GetAccountsAccountIdBalances, GetAccountsAccountIdTransactions]
---

# Read accounts and transactions (AIS)

Use this when an authorised AISP needs to read a Bank of Ireland (UK) customer's
account information with the customer's consent.

## Preconditions
- TPP enrolled on the FCA/OBIE Open Banking Directory and onboarded to the Bank
  of Ireland **(UK)** entity (separate from ROI).
- OB/eIDAS transport certificate for mutual-TLS; access tokens are certificate-bound.
- Base URL: `https://api.obapi.bankofireland.com/open-banking/v3.1/aisp`.

## Steps
1. Obtain a client-credentials token (`TPPOAuth2Security`, scope `accounts`) at
   `https://api.obapi.bankofireland.com/oauth/as/token.oauth2` over mutual-TLS.
2. **CreateAccountAccessConsents** — POST the consent with the requested
   `Permissions[]`. Capture the returned `ConsentId`.
3. Redirect the PSU through the authorization-code flow (`PSUOAuth2Security`,
   scope `openid accounts`) at
   `https://auth.obapi.bankofireland.com/oauth/as/b365/authorization.oauth2` for
   PSD2 SCA; the `openbanking_intent_id` claim carries the `ConsentId`.
4. **GetAccountAccessConsentsConsentId** — confirm consent `Status` is `Authorised`.
5. **GetAccounts** — list the consented accounts; take each `AccountId`.
6. **GetAccountsAccountIdBalances** and **GetAccountsAccountIdTransactions** —
   read balances and transactions per account. Page via the `Links.Next` cursor.

## Conventions
- Send `x-fapi-interaction-id` (RFC4122 UUID) on every call; the ASPSP echoes it.
- Errors return the `OBErrorResponse1` envelope (see errors/bank-of-ireland-uk-problem-types.yml).
- Rate limit signalled by HTTP 429 — back off and retry.
