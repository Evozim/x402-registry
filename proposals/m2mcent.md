# M2MCent

## Basic details
- Project name: M2MCent
- What does it do? (2–3 sentences): Non-custodial x402 V2 facilitator and deterministic MCP microservice gateway on Base Mainnet (Chain ID 8453). Exposes live B2B DNS/TLS OSINT, Web-to-Markdown extraction, Base L2 wallet KYT/OFAC screening, real-time Base gas telemetry, and live ADS-B aviation tracking paid per call in Circle USDC via EIP-3009 Smart Escrow V2. Also provides public `/supported`, `/verify`, `/settle`, and `/discovery/resources` facilitator endpoints plus a Streamable-HTTP MCP server.
- Type: API and facilitator (plus remote MCP server `https://api.m2mcent.com/mcp`)
- Official website: https://m2mcent.com
- Logo URL: https://m2mcent.com/icon.svg
- Documentation or getting-started link: https://m2mcent.com/paywall (OpenAPI: https://api.m2mcent.com/openapi.json; x402 manifest: https://api.m2mcent.com/.well-known/x402.json; ERC-8004: https://m2mcent.com/.well-known/erc8004.json)
- Public support channel: https://github.com/Evozim/m2mcent/issues

## Networks and activity
- Networks: Base (`eip155:8453`)
- Public explorer or analytics link, if available: https://basescan.org/address/0x5d47070A36A37DAf417e64FF27a1e5B3F1c84efa (Smart Escrow V2) and https://www.x402scan.com/server/53aa9c89-64a0-4856-9766-cd14f74767f7
- App contract/program or receiving addresses, with their networks, if available:
  - Base (`eip155:8453`) Smart Escrow V2 (`payTo`): `0x5d47070A36A37DAf417e64FF27a1e5B3F1c84efa`
  - Base (`eip155:8453`) Safe Multi-Sig Treasury (`recipient`): `0x8aaBAB75bE8825d0f5D514a9a5cBa04B7bF84920`
- Proof that you represent the project: Submitted from the official repository owner account [`@Evozim`](https://github.com/Evozim/m2mcent), matching `did:web:m2mcent.com` and `https://m2mcent.com/.well-known/erc8004.json`.

## Payments — only if your product accepts payments
- Paid endpoint and HTTP method:
  - `POST https://api.m2mcent.com/gas-pulse-mcp/api/process` (`$0.005` USDC / `5000` atomic)
  - `POST https://api.m2mcent.com/adsb-flight-tracker-mcp/api/process` (`$0.005` USDC / `5000` atomic)
  - `POST https://api.m2mcent.com/b2b-company-enrich-mcp/api/process` (`$0.025` USDC / `25000` atomic)
  - `POST https://api.m2mcent.com/web3-wallet-kyt-mcp/api/process` (`$0.025` USDC / `25000` atomic)
  - `POST https://api.m2mcent.com/serp-markdown-crawler-mcp/api/process` (`$0.050` USDC / `50000` atomic)
- Facilitator used: M2MCent Facilitator (`https://api.m2mcent.com`, also compatible with Coinbase CDP Facilitator)
- Payment scheme/version: `exact`, `x402Version: 2` (EIP-3009 `TransferWithAuthorization`)
- Token contract/mint and decimals: Circle Native USDC on Base `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913` (`6` decimals)
- Successful payment transaction link for each supported network: https://basescan.org/tx/0xb120a98bdff33717cfd91a50ff8bc0389fa6bf7f251ce5da643062277a0155ec (Base Mainnet block `59394491`, status `CONFIRMED`, `5000` micro-USDC settled through Escrow `0x5d47070A36A37DAf417e64FF27a1e5B3F1c84efa` to Safe Treasury `0x8aaBAB75bE8825d0f5D514a9a5cBa04B7bF84920`)
- Facilitator applicants:
  - Supported: `https://api.m2mcent.com/supported`
  - Verify: `https://api.m2mcent.com/verify`
  - Settle: `https://api.m2mcent.com/settle`
  - Discovery: `https://api.m2mcent.com/discovery/resources`
  - Active Base Mainnet Relayer Signers: `0x704E000b518c6Cf928637eDDCaDD3d15da8773E2`, `0x67227069f2728d1EE0DfCeDA39B083329303c993`

## Disclosure
Affiliation: Submitted directly by the M2MCent maintainer (`@Evozim`).
