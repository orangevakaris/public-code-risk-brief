# Public Code Risk Brief

`Public Code Risk Brief` is a small, pay-per-request review service for public GitHub repositories.

For **0.25 USDC on Base**, the service returns a concise, evidence-linked brief covering:

- the repository's architecture and trust boundaries;
- high-risk implementation paths worth reviewing first;
- dependency, CI, and configuration risks visible in the public source; and
- a prioritized remediation checklist.

This is a source-review service, not a security certification, penetration test, or guarantee that a repository is safe.

## Request a brief

1. Open a [new request](https://github.com/orangevakaris/public-code-risk-brief/issues/new?template=paid-risk-brief.yml).
2. Send **at least 0.25 USDC on Base** to:

   ```text
   0xf88990ca1dDF070dD74b6a7a3F2277863ACC23C8
   ```

3. Add the Base transaction hash to the request.

The service verifies the USDC `Transfer` event on Base before fulfillment. Each payment transaction can fund one request only. Fulfillment is posted as a comment on the issue, normally within 24 hours.

## Boundaries

- Public repositories and public commit URLs only.
- Do not include credentials, private keys, private source, personal data, or instructions to execute code.
- No deployed-contract probing, denial-of-service testing, or other live-target testing is performed.
- Requests that require private access, contain secrets, or are outside the stated scope are not processed. If the payment is valid but the request is ineligible, the issue will explain why; blockchain transfers cannot be reversed by this service.

## Payment details

- Network: Base mainnet (chain ID `8453`)
- Asset: native USDC
- USDC contract: `0x833589fCD6EDb6E08f4c7C32D4f71b54bda02913`
- Minimum payment: `0.25 USDC` (`250000` base units)

Payment validation uses a public Base RPC receipt and requires a successful USDC `Transfer` log whose recipient and amount match this request.

## Privacy

Issue contents and delivery comments are public. Use this service only for material that is already public.
