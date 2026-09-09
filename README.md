[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Solana](https://img.shields.io/badge/Solana-Mainnet-green.svg)](https://solana.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Datalake-blue.svg)](https://postgresql.org)
[![x402](https://img.shields.io/badge/Settlement-x402-purple.svg)](#)

---

# ⚡ SNTL DePIN Solves Sybil: Agent Physical ID Attestation

# SNTL Attestation — Spatiotemporal Agent ID

RF-layer, physics-backed identity for autonomous agents. Anchored by **UID, RSSI, Wallet, and SIWX**, with a **World State Chronicle** birth record (geolocation · time · power), minted as a **cNFT with 100% royalties burned**. Verification is free for life on the blockchain itself.

**SNTL solves Sybil for DePIN.**

---

## The elevator pitch

Anyone can generate an onchain ID for a fraction of a cent. Trust requires physical proof.

SNTL anchors digital agents to verifiable existence in space and time.

- Mint your permanent identity once — **$100 USDC**
- Verification is **free for life**

---

## ID anatomy

| Component | What it is |
|---|---|
| UID | Unique identifier of the agent |
| RSSI | RF-layer signal strength — physical proof of presence |
| Wallet | Blockchain address — the agent's economic identity |
| SIWX | Sign-In-With-X — live, re-verifiable proof of control |
| World State Chronicle | 2-year AI-enriched datalake: geolocation · time · power |
| cNFT | Compressed NFT, 100% royalties burned, no secondary market |
| Death Key | Localized one-way killswitch, issued with every ID |

---

## How it works

1. `GET /attestation` — pay **$100 USDC once** (x402)
2. Receive your **Spatiotemporal Agent ID** — a permanent cNFT
3. `GET /attestation/verify/:fingerprint` — **free on the blockchain, forever**

---

## Architecture of trust

- **The RF-Layer Anchor** — we don't just verify signatures; we verify physical existence. Spoofing and Sybil attacks become exponentially harder and vastly more expensive.
- **The World State Chronicle** — a massive, AI-enriched telemetry datalake. A blank ID has no context; SNTL IDs carry deep historical gravity.
- **Zero Speculation** — minted as a cNFT with 100% royalties permanently routed to a burn address. The ID cannot be profitably flipped; it is enterprise infrastructure, not a speculative asset.
- **One-Time Issuance, Free Verification** — paying once, verifying forever. Zero economic friction for third-party smart contracts to authenticate you.
- **The Cryptographic Death Key** — no admin backdoors, no recovery phrases. Every ID is issued with a localized one-way killswitch to permanently burn the attestation and protect ecosystem reputation.
- **Sybil Resistance for DePIN** — transient scripts with isolated keypairs carry no weight. SNTL IDs are anchored in reality.

---

## Endpoints

| Path | Method | Price | Description |
|---|---|---|---|
| `/attestation` | GET | $100 USDC | Issue a permanent Spatiotemporal Agent ID |
| `/attestation/verify/:fingerprint` | GET | Free | Verify an ID by fingerprint, on-chain, for life |
| `/.well-known/agent-card.json` | GET | Free | Machine-readable agent card |
| `/openapi.json` | GET | Free | API specification |
| `/health` | GET | Free | Service status 

Machine-readable mirrors: `/.well-known/agent-card.json` · `/openapi.json`

---
SNTL
[https://pop-os.tail08831d.ts.net](https://pop-os.tail08831d.ts.net)
