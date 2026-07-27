[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Solana](https://img.shields.io/badge/Solana-Mainnet-green.svg)](https://solana.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Datalake-blue.svg)](https://postgresql.org)
[![x402](https://img.shields.io/badge/Settlement-x402-purple.svg)](#)

---

# ⚡ SNTL DePIN Oracle

Solana, Helium Hotspot RF-backed ground truth for the Helium × Solana DePIN network — machine-payable, on-chain.

Pay-per-query datalake access via **MCP** and the `helium-mcp` onboarding helper.

> **Note:** Live stream access available upon request. Primary interface is the historical datalake.

Query an AI-classified datalake of enriched on-chain events:
- Threat tiers (critical → info)
- Anomaly scores
- H3 geospatial hotspot resolution
- RF physics propagation telemetry
- Forensic space·time·power chronicles
- Tiered LLM escalation verdicts
- Scored wallet segments

**Tiered x402 settlement on Solana mainnet.**
No signup. No API key. No CDP.

---

## 📊 Datalake Contents

| Table | Description |
| :--- | :--- |
| `solana_raw_data` | Raw ingested Solana transaction payloads |
| `enriched_events_base` | AI-graded DePIN threat/anomaly events |
| `world_state_chronicle` | Forensic causal chains and state transition history |
| `sentinel_logs` | Agent/sentinel execution logs and heartbeat tracking |
| `unparsed_events` | Ingestion staging queue |
| `events_lazy` | Lazy-loaded DePIN events |
| `ai_escalation_ledger` | AI threat tier escalations |
| `hotspot_location` | Physical DePIN node geospatial coordinates |

---

## 🚀 Quick Start — Free, No Payment Required

```bash
# Corpus depth + rail liveness
curl -s https://pop-os.tail08831d.ts.net/api/v2/stats

# Enriched ledger for any wallet
curl -s https://pop-os.tail08831d.ts.net/api/v2/ledger/<WALLET>
```

---

## 💰 Paid Calls — x402 Settlement

```bash
# 1. Request → receives 402 with payment requirements (LIMIT 1 enforced)
curl -i https://pop-os.tail08831d.ts.net/api/v2/threats/critical?limit=1

# 2. Resubmit with X-PAYMENT header (gasless, via PayAI facilitator)
```

| Parameter | Value |
| :--- | :--- |
| **Network** | `solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp` |
| **Asset** | USDC `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v` |
| **Price** | Tiered: $1.00 / $0.75 / $0.50 / $0.01 per record |
| **Facilitator** | https://facilitator.payai.network |
| **Settlement Proof** | [Live agent-to-agent settlement](https://solscan.io/tx/2TEnsbpuxLC3qsCLAf4MB2XfUbr2SF4B34vjpkV1Yzq2BeDqVuTzmEo6UX3SXFDkKRWMYtbSJ6K8GcuNZt7J939c) |

---

## 🔍 Discovery

| Surface | URL |
| :--- | :--- |
| **Agent2Agent (A2A) Agent Card** | https://pop-os.tail08831d.ts.net/.well-known/agent-card.json |
| **AI Manifest** | https://pop-os.tail08831d.ts.net/.well-known/ai.json |
| **OpenAPI** | https://pop-os.tail08831d.ts.net/openapi.json |
| **llms.txt** | https://pop-os.tail08831d.ts.net/llms.txt |

---

## 🎯 Skills

### 🆓 Free

| Skill | Endpoint | Description |
| :--- | :--- | :--- |
| `stats` | `GET /api/v2/stats` | Event counts by threat tier |
| `wallet-history` | `GET /api/v2/ledger/{wallet}` | Enriched event ledger |

---

### 🔴 Tier 1 — Critical Intelligence & RF Physics ($1.00 / call)

| Skill | Endpoint | Description |
| :--- | :--- | :--- |
| `rf-physics-violations` | `GET /api/v2/rf/violations` | FSPL vs RSSI deltas, deterministic signal spoofing |
| `phantom-devices` | `GET /api/v2/rf/phantoms` | Entity registrations lacking H3 geospatial coordinates |
| `treasury-anomalies` | `GET /api/v2/threats/treasury` | Unscheduled >100k token movements |
| `hivemapper-anomalies` | `GET /api/v2/rf/hivemapper` | Spatial/region physics violations |
| `threats-critical` | `GET /api/v2/threats/critical` | Enriched events tagged critical |

---

### 🟠 Tier 2 — High Threat & Forensic State ($0.75 / call)

| Skill | Endpoint | Description |
| :--- | :--- | :--- |
| `threats-high` | `GET /api/v2/threats/high` | Enriched events tagged high |
| `world-state-chronicle` | `GET /api/v2/chronicle` | Forensic causal chains and entropy flags |
| `geo-hotspots` | `GET /api/v2/geo` | H3 resolution with RF metadata (fresnel, gain) |

---

### 🟡 Tier 3 — Medium Threat & Wallet Intel ($0.50 / call)

| Skill | Endpoint | Description |
| :--- | :--- | :--- |
| `threats-medium` | `GET /api/v2/threats/medium` | Enriched events tagged medium |
| `hvt-anomaly` | `GET /api/v2/wallets/hvt-anomaly` | High-value target wallet extraction |
| `anomaly-critical-wallets` | `GET /api/v2/wallets/critical` | Wallets associated with critical events |
| `architects` | `GET /api/v2/wallets/architects` | Network architect wallets |
| `target-wallets` | `GET /api/v2/wallets/target` | Scored engagement targets |
| `wallet-pool` | `GET /api/v2/wallets/pool` | General wallet data |
| `connected` | `GET /api/v2/wallets/connected` | Graph-connected wallet clusters |
| `blink-ready` | `GET /api/v2/wallets/blink-ready` | Wallets with pending blink actions |
| `anomaly-medium-wallets` | `GET /api/v2/wallets/medium` | Wallets associated with medium events |
| `paid` | `GET /api/v2/wallets/paid` | Wallets with verified x402 settlement history |
| `tier-1` | `GET /api/v2/pyramid/tier-1` | Engagement pyramid (6–7 lists) |
| `tier-2` | `GET /api/v2/pyramid/tier-2` | Engagement pyramid (4–5 lists) |
| `tier-3` | `GET /api/v2/pyramid/tier-3` | Engagement pyramid (2–3 lists) |

---

### 🟢 Tier 4 — Low Threat & Infrastructure ($0.01 / call)

| Skill | Endpoint | Description |
| :--- | :--- | :--- |
| `query-datalake` | `POST /api/v2/query` | Sandboxed SQL SELECT |
| `threats-low` | `GET /api/v2/threats/low` | Enriched events tagged low/info |
| `pending-loops` | `GET /api/v2/threats/pending` | Unresolved state loops |
| `anomalies` | `GET /api/v2/anomalies` | General anomaly score feed |
| `escalation-ledger` | `GET /api/v2/escalation` | SLM 0.5B → SLM 3.5B → LLM verdicts |
| `unparsed-dlq` | `GET /api/v2/dlq` | Failure-mode data |
| `lookup-event` | `GET /api/v2/event/{signature}` | Direct signature lookup |

---
---

## 🗃️ SQL Surface

`POST /api/v2/query` accepts read-only SQL.

| Guard | Value |
| :--- | :--- |
| **Statements** | `SELECT` only |
| **Row cap** | `LIMIT 1` |
| **Tables** | Allow-listed |

```sql
SELECT transaction_id, threat_assessment, anomaly_score, summary
FROM enriched_events_base
WHERE threat_assessment = 'critical'
ORDER BY block_time DESC
LIMIT 1
```

Registry endpoints use pre-baked SQL. The only agent-controlled input is `?limit` (parsed and capped at **1**).

---
---

## 🤖 MCP

Plug the rail into any **MCP** host:

```bash
yarn dlx @web3solutions33/helium-mcp
```

**Repo**: [substreambc/helium-mcp](https://github.com/substreambc/helium-mcp)
**npm**: [@web3solutions33/helium-mcp](https://www.npmjs.com/package/@web3solutions33/helium-mcp)
**License**: MIT

---
---

## 📄 Response Shape

```json
{
  "endpoint": "/api/v2/rf/violations",
  "dataType": "rf-telemetry",
  "rowCount": 1,
  "rows": [
    {
      "hotspot_address": "...",
      "rssi_delta_dbm": -42.5,
      "physics_violation": true,
      "transmit_scale": 0.15
    }
  ]
}
```

---
---

## 📌 Notes

- Anomaly scores observed in the range `0..0.6`.
- Wallet segments are filtered to real Base58 addresses (EVM-null and System Program placeholders excluded).
- `unparsed-dlq` is published deliberately: coverage honesty over coverage theater.

---
**Web3 Solutions, LLC** · [https://pop-os.tail08831d.ts.net](https://pop-os.tail08831d.ts.net)
