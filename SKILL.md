Markdown
# SKILL — SNTL Attestation

Agent-operable manual for issuing and verifying Spatiotemporal Agent IDs.

## Overview

SNTL Attestation issues permanent spatiotemporal ID. An ID is a cNFT minted once, with 100% royalties burned, anchored by UID + RSSI + Wallet + SIWX, given weight and depth by a 2-year World State Chronicle. Verification is on-chain.

## Discovery

- Agent card: `GET /.well-known/agent-card.json`
- API spec: `GET /openapi.json`
- Health: `GET /health`

## Issue an ID

`GET /attestation`

The endpoint is protected by x402. 


A request without payment returns `402 Payment Required` with a machine-readable invoice 
(network, asset, payTo, price, facilitator).


Bundle: Solana mainnet · USDC · price $100 one-time · facilitator payai.


To obtain an ID:


1. Resolve the 402 challenge from the payment header.
2. Pay the exact amount via the x402 facilitator.
3. Retry `GET /attestation` with the payment proof.
4. On success you receive an attestation record of instantiation.  


Issuance is idempotent — if the fingerprint already has an ID, 
the existing record is returned as proof of existance.

## Verify an ID

`GET /attestation/verify/:fingerprint`

Free, no payment required. Returns the confirmed attestation record as live proof; if it exists, or a not-found result.

```EXAMPLE json 
{ 
  "exists": true, 
  "record": { 
    "fingerprint": "<hash_SWIX_RSSI_etc_wallet>",
    "wallet": "<payer_wallet>",
    "firstSeen": "2024-10-24T12:00:00.000Z",
    "lastSeen": "2024-10-24T12:00:00.000Z",
    "identityHash": "<sha256_hash>",
    "permanent": true,
    "royaltiesBurned": true
  } 
}


Attestation record fields
Field	Meaning
fingerprint	The unique identifier for the agent wallet account that paid issuance / holds the ID
firstSeen epoch (ISO 8601)
lastSeen	Last time the physical/digital asset interacted with the rail (ISO 8601)
identityHash	
Cryptographic hash anchoring the spatial/network fingerprint
permanent	

Boolean confirming the ID is permanently anchored
royaltiesBurned	Boolean confirming royalties: 100; no secondary market incentive.
Permanence: the record and its verification are on the Solana Blockchain public ledger. 


Secure on the holder side; the service never holds recovery material.
