# Audit Ledger MCP client examples

Audit Ledger records evidence of agent actions. Teams can inspect the resulting audit trail.

This repository holds small, working examples for the hosted **Audit Ledger** MCP server. It is maintained by Elite AI Empire. The server itself is hosted; nothing here runs it.

- Product: https://eliteagenticsolutions.com/products/audit-ledger/
- MCP endpoint (streamable HTTP): `https://empireaudit.eliteaiempire.com/mcp`
- OpenAPI: https://eliteagenticsolutions.com/products/audit-ledger/openapi.json
- Pricing, machine readable: https://eliteagenticsolutions.com/products/audit-ledger/pricing.json
- Discovery file: https://eliteagenticsolutions.com/products/audit-ledger/.well-known/mcp.json

## Tools

| Tool | What it does |
|---|---|
| `auditledger_plans` | Returns each plan with its monthly price in US dollars (null means contact sales), taken from the same data file the pricing page is built from. Pricing: {"unit |
| `auditledger_about` | What Audit Ledger does and what is free Pricing: {"unit": "call", "price_usd": 0, "free_quota": "200 per day per IP", "note": "Keyed volume pricing is published |
| `auditledger_pricing` | Where prices live and what costs nothing Pricing: {"unit": "call", "price_usd": 0, "free_quota": "200 per day per IP", "note": "Keyed volume pricing is publishe |
| `usage_get` | Usage for the calling key (last 30 days) |
| `get_checkout_link` | Get the published plan page (standalone tiers need an account) plus a no-account checkout option: Empire Security Complete includes Audit Ledger. Does not creat |

## Try it

```bash
bash examples/initialize.sh
python3 examples/client.py
```

`examples/client.py` uses only the Python standard library. It sends `initialize` and `tools/list` and prints the result. No key is needed for the public read tools. Tools that need an account say so in their description.

## Registry

Listed in the official MCP registry. Server manifest: `server.json`.

## Licence

MIT. See `LICENSE`.
