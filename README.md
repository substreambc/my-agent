[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Solana](https://img.shields.io/badge/Solana-Mainnet-green.svg)](https://solana.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Datalake-blue.svg)](https://postgresql.org)
[![x402](https://img.shields.io/badge/Settlement-x402-purple.svg)](#)

---

# ⚡ SNTL DePIN Oracle: agent-card.json 

simple UI for A2A 

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/4da4a9e0-8554-4af5-82a8-274b48cd73f3" />

{
  "x402Version": 2,
  "service": "SNTL Datalake Oracle",
  "description": "Pay-per-record access to the SNTL DePIN RF telemetry & yield-loss datalake. GET only, one record per call, USDC on Solana via x402. Real data only.",
  "payment": {
    "asset": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",
    "network": "solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp",
    "payTo": "AuBsRDd6aFyBb5HxZyrCT7QcAiuqbk67AwJaCXtywV8q"
  },
  "accepts": [
    {
      "resource": "/api/v2/stats",
      "price": "0",
      "method": "GET"
    },
    {
      "resource": "/api/v2/ledger/:wallet",
      "price": "0",
      "method": "GET"
    },
    {
      "resource": "/api/v2/chronicle",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/chronicle/power",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/chronicle/time",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/chronicle/space",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/geo",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/paid",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/target",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/architects",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/blink-ready",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/connected",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/threats/medium",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/threats/high",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/critical",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/medium",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/wallets/hvt-anomaly",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/pyramid/tier-1",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/pyramid/tier-2",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/pyramid/tier-3",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/dlq",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/threats/critical",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/rf/violations",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/threats/treasury",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/rf/phantoms",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/rf/hivemapper",
      "price": "1.00",
      "method": "GET"
    },
    {
      "resource": "/api/v2/escalation",
      "price": "1.00",
      "method": "GET"
    }
  ]
}


Machine-readable mirrors: `/.well-known/agent-card.json` · `/openapi.json`

