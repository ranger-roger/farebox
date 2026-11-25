# Farebox Roadmap

What's shipped is on [STATUS](STATUS.md) and the [site](https://farebox.dev). This
is what's ahead — order and timing may shift. Items marked (lib-ready) build on
schemes that already exist in the x402 v2 libraries farebox uses.

## Near term

- **Fare log & stats** — per-fare receipts (payer, amount, tx hash), a
  `/__farebox/stats` endpoint, CSV export. See every fare you've collected.
- **Per-route pricing** — different fares for different routes on one farebox
  (`-r "GET /search=0.01" -r "POST /generate=0.05"`).
- **Splitter auto-flush** — fee-split deployments forward balances automatically
  once a threshold is reached.
- **`farebox init`** — config-file setup for multi-route deployments.

## Next

- **More EVM chains** — Arbitrum, Optimism, Polygon (native USDC via EIP-3009,
  same self-settlement model as Base).
- **Metered fares (lib-ready: `upto` scheme)** — authorize up to a max, charge
  actual usage. Built for LLM endpoints and per-token billing.
- **MCP-native mode** — per-tool pricing for MCP servers: each tool call can
  carry its own fare.
- **Discovery** — make farebox endpoints discoverable by paying agents (x402
  bazaar/discovery integration).

## Later

- **Batch settlement (lib-ready)** — thousands of fares settled in one
  transaction for high-throughput endpoints.
- **Holds & captures (lib-ready: auth-capture scheme)** — reserve a fare,
  capture on delivery; refundable flows.
- **Solana** — x402 SVM scheme support.
- **Hosted farebox** — managed deployments for operators who don't want to run
  anything, built on the same self-custodial settlement.

Suggestions and interop reports: [issues](https://github.com/ranger-roger/farebox/issues).
