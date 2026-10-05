---
name: blockreq-rpc
description: "Use when writing, configuring, or debugging code that calls EVM JSON-RPC through BlockReq (blockreq.com) endpoints: picking the network host and URL, the public trial versus an API key, eth_subscribe over WSS, methods that need archive data or are limited to proof/debug/trace networks, Request Counting and plan limits, and errors such as chain-ID mismatch, 429, or unavailable historical state."
---

# BlockReq RPC

BlockReq serves JSON-RPC for 25 published networks; 24 are EVM networks with a documented JSON-RPC method set. Facts below are generated from BlockReq's catalogs; the full docs are at https://blockreq.com/docs/llms.txt.

## Endpoint URLs

Every network has its own host. Hosts are not guessable (for example `arbitrum-one-rpc.blockreq.com`, `polygon-bor-rpc.blockreq.com`), so look them up in [reference/networks.md](reference/networks.md) or https://blockreq.com/docs/networks.json.

- Private: `https://<host>/v1/rpc/<API key>`. Create an endpoint at https://blockreq.com/dashboard to get a key. Read it from an environment variable such as `BLOCKREQ_API_KEY`; never hard-code or commit it.
- Public trial: `https://<host>/v1/rpc/public`. Rate-limited, and it does not promise deep history, debug, or trace. Use it to try calls, not for production.
- WebSocket: `wss://<host>/v1/rpc/<API key>` or `wss://<host>/v1/rpc/public` on all 24 EVM networks.

## Which methods work where

- 24 EVM networks share the standard `eth_*`, `net_*`, and `web3_*` methods. Per-method availability: [reference/methods.md](reference/methods.md).
- `debug_traceBlockByNumber`, `debug_traceCall`, `debug_traceTransaction`, `eth_getProof`, `trace_block`, `trace_filter`, `trace_transaction` are documented only for archive networks in the ethereum, bsc, arbitrum, base, polygon families: Ethereum, Base, Arbitrum One, Polygon, BSC, Ethereum Sepolia, Base Sepolia, Arbitrum Sepolia, Polygon Amoy. Do not rely on them elsewhere.
- `eth_getBlobSidecarByTxHash`, `eth_getBlobSidecars`, `eth_getFinalizedBlock`, `eth_getFinalizedHeader`, `eth_getTransactionsByBlockNumber`, `eth_health` exist only on BSC.
- `eth_subscribe` and `eth_unsubscribe` need WSS; over HTTPS they fail.
- Arc serves full-node data: old-block state is not available, so query recent blocks.
- Polygon, Polygon Amoy: the public trial serves latest state only. `debug_traceBlockByNumber`, `debug_traceCall`, `debug_traceTransaction`, `eth_getFilterChanges`, `eth_getFilterLogs`, `eth_getProof`, `eth_newBlockFilter`, `eth_newFilter`, `eth_newPendingTransactionFilter`, `eth_uninstallFilter`, `trace_block`, `trace_filter`, `trace_transaction` need a private endpoint there.
- The Free plan does not include `debug_*`, `trace_*`, or `txpool_*`; they need a paid Request Pack or pay-as-you-go.

## Request Counting and plans

- Each authenticated JSON-RPC item counts as 1 Request, including reverts; each batch item counts on its own method; each delivered WSS notification counts as 1. HTTP `eth_getLogs` is 1 regardless of block range.
- Counts as 3: `eth_getBlockReceipts`, `eth_getProof`.
- Counts as 5: `debug_traceCall`, `debug_traceTransaction`, `trace_filter`, `trace_transaction`.
- Counts as 20: `debug_traceBlockByNumber`, `trace_block`.
- Zero: method not found and other non-execution errors, authentication or policy rejections, `429`, gateway `5xx`, and public-trial traffic.
- Free: 3,000,000 Requests per 30 days, 10 sustained / 30 burst requests per second, batch size 5, 2 WSS connections / 5 active subscriptions. After prepaid Requests: $3.90 per 1M Requests used. Plan limits: https://blockreq.com/docs/pricing/plans/index.md

## Errors

- `429`: you exceeded your plan's sustained or burst rate. Slow down and spread requests; the response is not counted.
- Gateway `5xx`: not counted; send the request again later.
- JSON-RPC method not found: the method is not served on that network; check [reference/methods.md](reference/methods.md).
- A revert is an execution result: it is counted, and sending the same call again returns the same revert.

## Examples

Replace the host with the one for your network. These use Ethereum (chain ID 1).

```bash
curl -s https://ethereum-rpc.blockreq.com/v1/rpc/$BLOCKREQ_API_KEY \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","method":"eth_chainId","params":[],"id":1}'
```

```typescript
// viem
import { createPublicClient, http, webSocket } from "viem";
import { mainnet } from "viem/chains";

const client = createPublicClient({
  chain: mainnet,
  transport: http(`https://ethereum-rpc.blockreq.com/v1/rpc/${process.env.BLOCKREQ_API_KEY}`),
});
const blockNumber = await client.getBlockNumber();

// eth_subscribe needs WSS
const ws = createPublicClient({
  chain: mainnet,
  transport: webSocket(`wss://ethereum-rpc.blockreq.com/v1/rpc/${process.env.BLOCKREQ_API_KEY}`),
});
ws.watchBlocks({ onBlock: (block) => console.log(block.number) });
```

```typescript
// ethers v6: a static network skips chain detection calls, which would also be counted
import { JsonRpcProvider } from "ethers";

const provider = new JsonRpcProvider(`https://ethereum-rpc.blockreq.com/v1/rpc/${process.env.BLOCKREQ_API_KEY}`, 1, {
  staticNetwork: true,
});
const balance = await provider.getBalance("0x0000000000000000000000000000000000000000");
```

```python
# web3.py
import os
from web3 import Web3

w3 = Web3(Web3.HTTPProvider(f"https://ethereum-rpc.blockreq.com/v1/rpc/{os.environ['BLOCKREQ_API_KEY']}"))
assert w3.eth.chain_id == 1
```

## Pitfalls

- Chain-ID mismatch: every host serves exactly one chain. Call `eth_chainId` once and compare it with networks.json before signing or sending.
- Historical reads on full-node networks fail for old blocks; archive-only workloads belong on archive networks.
- The public trial is not a free production tier: it is rate-limited and does not promise deep history, debug, or trace. Use a private endpoint.
- Proof, debug, and trace outside the archive families above are not documented; confirm in reference/methods.md first.

## MCP server

If your agent supports MCP, add https://mcp.blockreq.com/mcp (Streamable HTTP). It is public, free, and read-only, with the tools `list_chains`, `get_chain`, `search_docs`, `get_doc_page`, `get_method_reference`, `call_rpc`. Without credentials `call_rpc` uses the rate-limited public trial endpoint; connect with `Authorization: Bearer <API key>` (from the `BLOCKREQ_API_KEY` environment variable, never hard-coded) and it uses your own endpoint and quota; hosted clients such as Claude.ai connect to https://mcp.blockreq.com/mcp/account and sign in instead. Use it for lookups and checks, not production traffic. It cannot sign or send transactions.

## More

- Per-network OpenRPC: https://blockreq.com/docs/openrpc/index.json
- Full docs in one file: https://blockreq.com/docs/llms-full.txt
