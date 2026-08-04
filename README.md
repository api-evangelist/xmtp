# XMTP

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

XMTP (Extensible Message Transport Protocol) is a decentralized, open messaging protocol for sending end-to-end encrypted messages between Ethereum wallet addresses and other decentralized identifiers. Built on the MLS (Messaging Layer Security) standard, XMTP enables developers to add secure, censorship-resistant messaging to Web3 applications, AI agents, and wallets without relying on centralized servers.

## Overview

- **Website**: https://xmtp.org
- **Documentation**: https://docs.xmtp.org
- **GitHub**: https://github.com/xmtp
- **Status**: https://status.xmtp.org
- **Community**: https://community.xmtp.org
- **Blog**: https://blog.xmtp.org

## APIs

This repository contains the APIs.json catalog for XMTP covering:

| API | Type | Description |
|-----|------|-------------|
| XMTP Network gRPC API | gRPC | Core protocol for sending/receiving encrypted messages |
| XMTP JavaScript/TypeScript SDK | SDK | Browser and Node.js client library |
| XMTP Agent SDK | SDK | Node.js SDK for building AI agents |
| XMTP Android SDK | SDK | Native Kotlin SDK for Android |
| XMTP iOS SDK | SDK | Native Swift SDK for iOS |
| XMTP React Native SDK | SDK | Cross-platform mobile SDK |
| XMTP App Chain RPC API | JSON-RPC | L3 appchain for identity and group management |

## Key Features

- **End-to-end encryption** using the MLS (Messaging Layer Security) standard
- **Decentralized** — no single point of control or failure
- **Wallet-native identity** — works with any EVM wallet (ECDSA signing on secp256k1)
- **Flexible identities** — supports ENS, Bluesky DIDs, passkeys, and more
- **Rich content types** — text, attachments, reactions, read receipts, transactions
- **AI agent support** — purpose-built SDK for autonomous agents
- **Quantum-resistant storage** — messages stored with post-quantum encryption
- **Multi-chain** — compatible with Ethereum, Base, Arbitrum, Optimism, Polygon, Avalanche, and more

## Network Architecture

XMTP operates as a three-layer system:

1. **XMTP Network** (Broadcast) — Node operators store and relay encrypted messages via gRPC
2. **XMTP App Chain** (L3) — Arbitrum-based chain settling to Base for identity, groups, and fees
3. **Client SDKs** — Platform-specific libraries wrapping the libxmtp Rust core

## Pricing

XMTP uses a usage-based, decentralized fee model paid in USDC:

- **Base fee**: ~$5 per 100,000 messages ($0.00005/message)
- **Storage fee**: Per-byte-day of message retention (60-day default)
- **Congestion fee**: Dynamic fee during high network load
- **Gas fees**: Fractions of a US cent for App Chain transactions

Fees go directly to independent node operators — not to XMTP Labs. SDKs and development tools are free and open source.

## Getting Started

```bash
# Install the XMTP JavaScript SDK
npm install @xmtp/xmtp-js

# Or install the browser SDK
npm install @xmtp/browser-sdk
```

See the [official documentation](https://docs.xmtp.org/chat-apps/intro/get-started) for full quickstart guides across all platforms.

## Repository Contents

- `apis.yml` — APIs.json 0.19 provider catalog
- `plans/plans.yml` — Pricing and access tiers
- `rate-limits/rate-limits.yml` — Network rate limits and constraints
- `finops/finops.yml` — Cost estimation and FinOps guidance
