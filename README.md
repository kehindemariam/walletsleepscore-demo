# walletsleepscore — live demo

A live, in-browser demo of [walletsleepscore](https://github.com/kehindemariam/walletsleepscore).

**What it does:** scores any Pharos Pacific mainnet wallet across 7 activity metrics and renders a 0-100 sleep score with a gauge and bar chart.

**How it works:** the page makes fresh JSON-RPC calls to `https://rpc.pharos.xyz` — no backend, no indexer, no caching. Every visit re-queries the chain.

**The flow:**
1. `eth_blockNumber` — current block
2. `eth_getTransactionCount` — lifetime outbound txs
3. `eth_getBalance` — native balance
4. Binary search (~12 calls) — last active block
5. Last 10 blocks sampled — for interaction-diversity metric

**Visual style:** *analytics dashboard* — slate base, mint primary, radial gauge, horizontal bar chart. Distinct from the cyber/electric and terminal/hacker themes of the other demos in this campaign.

**Source:** https://github.com/kehindemariam/walletsleepscore
