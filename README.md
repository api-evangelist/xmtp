# XMTP

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
