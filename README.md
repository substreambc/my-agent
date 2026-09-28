[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Solana](https://img.shields.io/badge/Solana-Mainnet-green.svg)](https://solana.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Datalake-blue.svg)](https://postgresql.org)
[![x402](https://img.shields.io/badge/Settlement-x402-purple.svg)](#)

---

# ⚡ SNTL DePIN Oracle: agent-card.json 

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/f76ae49a-e049-4ba0-a7ad-82697d520cb0" />
super simple UI for A2A 

## PROOF IS TRUST  

SNTL anchors physical/digital assets to verifiable existence in space and time.

- Mint your permanent SNTL-ID as a cNFT once — **$999.99 USDC**
- Verification is permanently attested to on the public ledger Solana blockchain. 

---

## ID anatomy

| Component | What it is |
|---|---|
| UID | Unique identifier of the asset physical/digital, vehicle, package, cargo, freight, or anything requiring unique attestation of existance, location, and uniqueness |
| RSSI | RF-layer signal strength — physical proof of presence |
| Wallet | Blockchain address — the agent's economic identity |
| SIWX | Sign-In-With-X — live, re-verifiable proof of control |
| World State Chronicle | 2-year AI-enriched datalake: geolocation · time · power |
| cNFT | Compressed NFT, 100% royalties burned, no secondary market 

---

## How it works

1. `GET /attestation` — pay **$.01 $999.99 USDC once** (x402)
2. Receive your **Spatiotemporal Agent ID** — a permanent cNFT and ID profile
3. `GET /attestation/verify/:fingerprint` — **on the blockchain**

---

## Architecture of trust

- **The RF-Layer Anchor** — we don't just verify signatures; we verify physical existence. Spoofing and Sybil attacks become exponentially more difficult and vastly more expensive.
- **The World State Chronicle** — a massive, AI-enriched telemetry datalake. A blank ID has no context; SNTL IDs carry deep historical gravity.
- **Zero Speculation** — minted as a cNFT with royalties: 100. SNTL cNFTs are part of the enterprise infrastructure, not a speculative asset.
- **One-Time Issuance**. Zero economic friction for third-party smart contracts to authenticate and positively ID your physical/digital asset.
- **Sybil Resistance for DePIN** — transient scripts with isolated keypairs carry no weight. SNTL IDs are anchored in Blockchain reality, assure uniqueness, and record the live position within 120ms; full history.

---

## Endpoints

| Path | Method | Price | Description |
|---|---|---|---|
| `/.well-known/agent-card.json` | GET | Free | Machine-readable agent card |
| `/openapi.json` | GET | Free | API specification |
| `/health` | GET | Free | Service status 

Machine-readable mirrors: `/.well-known/agent-card.json` · `/openapi.json`

