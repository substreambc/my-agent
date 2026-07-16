# SNTL LIVE Data Helium Network 1-year history tx sigs, Solana
Pay-per-query intelligence for DePIN infrastructure with MCP and MCP On-bording-helper "helium-mcp"  

Query an AI-classified datalake of enriched on-chain events — threat tiers (critical→low), anomaly scores, H3 geospatial hotspot resolution, forensic space·time·power chronicles, tiered LLM escalation verdicts, and scored wallet/audience segments.

**26 machine skills · 2 free · $0.01 USDC/call via x402 on Solana mainnet.**
No signup. No API key. No CDP.

Table Name               │     Live Row Count      │ Technical Classification
  ──────────────────────────┼─────────────────────────┼──────────────────────────────────────────────────────
    solana_raw_data         │         724,198         │ Raw ingested Solana transaction payloads
    enriched_events_base    │         483,140         │ AI-graded DePIN threat/anomaly events
    world_state_chronicle   │         406,453         │ Forensic causal chains and state transition history
    sentinel_logs           │         80,309          │ Agent/sentinel execution logs and heartbeat tracking
    unparsed_events         │         69,270          │ Ingestion staging queue
    events_lazy             │         62,145          │ Lazy-loaded DePIN intelligence events
    ai_escalation_ledger    │         46,906          │ AI threat tier escalations
    hotspot_location        │         38,262          │ Physical DePIN node geospatial coordinates

Built for agents that need to check a Solana/Helium wallet, tx, or program and get back a classified, on-chain-verifiable answer. **The protocol is the UI.**

---

## Quick start — free, no payment (JUST DOWNLOAD AGENT CARD AND DROP INTO YOUR FAVORITE AI)

```bash
# corpus depth + rail liveness
curl -s https://pop-os.tail08831d.ts.net/api/v2/stats

# enriched ledger for any wallet
curl -s https://pop-os.tail08831d.ts.net/api/v2/ledger/<WALLET>
```

## Paid call — x402

```bash
# 1. request → 402 with payment requirements
curl -i https://pop-os.tail08831d.ts.net/api/v2/threats/critical?limit=50

# 2. resubmit with X-PAYMENT header (gasless, via PayAI facilitator)
```

| | |
|---|---|
| Network | `solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp` |
| Asset | USDC `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v` |
| Price | $0.01 / call |
| Facilitator | https://facilitator.payai.network |
| Settlement proof | [`2TEnsbpux…7J939c`](https://solscan.io/tx/2TEnsbpuxLC3qsCLAf4MB2XfUbr2SF4B34vjpkV1Yzq2BeDqVuTzmEo6UX3SXFDkKRWMYtbSJ6K8GcuNZt7J939c) — live agent-to-agent settlement, verify it yourself |

---

## Discovery

| Surface | URL |
|---|---|
| Agent card | `https://pop-os.tail08831d.ts.net/.well-known/agent-card.json` |
| AI manifest | `https://pop-os.tail08831d.ts.net/.well-known/ai.json` |
| OpenAPI | `https://pop-os.tail08831d.ts.net/openapi.json` |
| llms.txt | `https://pop-os.tail08831d.ts.net/llms.txt` |

---

## The 26 skills

### 🆓 Free
| Skill | Endpoint |
|---|---|
| `stats` | `GET /api/v2/stats` — event counts by threat tier |
| `wallet-history` | `GET /api/v2/ledger/{wallet}` — enriched event ledger |

### Query primitives
| Skill | Endpoint |
|---|---|
| `query-datalake` | `POST /api/v2/query` — sandboxed SQL SELECT |
| `lookup-event` | `GET /api/v2/event/{signature}` |

### Threat intelligence
| Skill | Endpoint |
|---|---|
| `threats-critical` | `GET /api/v2/threats/critical` |
| `threats-high` | `GET /api/v2/threats/high` |
| `threats-medium` | `GET /api/v2/threats/medium` |
| `threats-low` | `GET /api/v2/threats/low` |
| `pending-loops` | `GET /api/v2/threats/pending` |
| `anomalies` | `GET /api/v2/anomalies` |

### Wallet / audience intelligence
| Skill | Endpoint |
|---|---|
| `architects` | `GET /api/v2/wallets/architects` |
| `target-wallets` | `GET /api/v2/wallets/target` |
| `hvt-anomaly` | `GET /api/v2/wallets/hvt-anomaly` |
| `wallet-pool` | `GET /api/v2/wallets/pool` |
| `connected` | `GET /api/v2/wallets/connected` |
| `blink-ready` | `GET /api/v2/wallets/blink-ready` |
| `anomaly-critical-wallets` | `GET /api/v2/wallets/critical` |
| `anomaly-medium-wallets` | `GET /api/v2/wallets/medium` |
| `paid` | `GET /api/v2/wallets/paid` |

### Engagement pyramid
| Skill | Endpoint |
|---|---|
| `tier-1` | `GET /api/v2/pyramid/tier-1` — 6–7 lists |
| `tier-2` | `GET /api/v2/pyramid/tier-2` — 4–5 lists |
| `tier-3` | `GET /api/v2/pyramid/tier-3` — 2–3 lists |

### Forensic substrate
| Skill | Endpoint |
|---|---|
| `world-state-chronicle` | `GET /api/v2/chronicle` |
| `geo-hotspots` | `GET /api/v2/geo` — H3 resolution |
| `escalation-ledger` | `GET /api/v2/escalation` — SLM 0.5B → SLM 3.5B → LLM |
| `unparsed-dlq` | `GET /api/v2/dlq` — failure-mode intelligence |

---

## SQL surface

`POST /api/v2/query` accepts read-only SQL.

| Guard | Value |
|---|---|
| Statements | `SELECT` only |
| Row cap | `LIMIT ≤ 100` |
| Tables | allow-listed |

```sql
SELECT transaction_id, threat_assessment, anomaly_score, summary
FROM enriched_events_base
WHERE threat_assessment = 'critical'
ORDER BY block_time DESC
LIMIT 50
```

Registry endpoints use pre-baked SQL; the only agent-controlled input is `?limit` (parsed and capped).

---

## MCP

Plug the rail into any MCP host:

```bash
yarn dlx @web3solutions33/helium-mcp
```

Repo: [substreambc/helium-mcp](https://github.com/substreambc/helium-mcp) · npm: [@web3solutions33/helium-mcp](https://www.npmjs.com/package/@web3solutions33/helium-mcp) · MIT

---

## Response shape

```json
{
  "endpoint": "/api/v2/threats/critical",
  "dataType": "threat-intel",
  "rowCount": 50,
  "rows": [ { "transaction_id": "...", "anomaly_score": 0.42, "threat_assessment": "critical", "summary": "..." } ]
}
```

---

## Notes

- Anomaly scores observed in the range `0..0.6`.
- Wallet segments are filtered to real Base58 addresses (EVM-null and System Program placeholders excluded).
- `unparsed-dlq` is published deliberately: coverage honesty over coverage theater.

---

**Web3 Solutions, LLC** · [https://pop-os.tail08831d.ts.net](https://pop-os.tail08831d.ts.net) · [https://pop-os.tail08831d.ts.net](https://pop-os.tail08831d.ts.net)
