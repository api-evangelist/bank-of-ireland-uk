---
name: Initiate a domestic payment (Bank of Ireland UK PIS)
description: Consent, authorise and execute a single domestic payment over the OBIE Payment Initiation API with idempotency.
api: openapi/bank-of-ireland-uk-payment-initiation-openapi.yaml
operations: [CreateDomesticPaymentConsents, GetDomesticPaymentConsentsConsentId, GetDomesticPaymentConsentsConsentIdFundsConfirmation, CreateDomesticPayments, GetDomesticPaymentsDomesticPaymentId]
---

# Initiate a domestic payment (PIS)

Use this when an authorised PISP initiates a single immediate domestic payment
for a Bank of Ireland (UK) customer.

## Preconditions
- TPP onboarded to the Bank of Ireland **(UK)** OBIE entity with OB/eIDAS certs.
- Base URL: `https://api.obapi.bankofireland.com/open-banking/v3.1/pisp`.

## Steps
1. Get a client-credentials token (`TPPOAuth2Security`, scope `payments`) over mutual-TLS.
2. **CreateDomesticPaymentConsents** — POST the consent with `Initiation`
   (creditor, amount, reference). Set an `x-idempotency-key` (unique, 24h validity,
   ≤40 chars). Capture the `ConsentId`.
3. Redirect the PSU through authorization-code + SCA (`PSUOAuth2Security`, scope
   `openid payments`); the `openbanking_intent_id` carries the `ConsentId`.
4. **GetDomesticPaymentConsentsConsentId** — confirm `Status` is `Authorised`.
5. (Optional) **GetDomesticPaymentConsentsConsentIdFundsConfirmation** — check funds are available.
6. **CreateDomesticPayments** — POST the payment referencing the `ConsentId`,
   re-using an `x-idempotency-key`. On selected operations attach a detached
   `x-jws-signature` (PS256). Capture `DomesticPaymentId`.
7. **GetDomesticPaymentsDomesticPaymentId** — poll payment `Status`.

## Conventions
- **Idempotency**: `x-idempotency-key` makes payment creation safely retryable
  for 24h; reuse with a changed payload returns 409.
- Send `x-fapi-interaction-id` on every call.
- Errors: `OBErrorResponse1` envelope; see errors/bank-of-ireland-uk-problem-types.yml.
