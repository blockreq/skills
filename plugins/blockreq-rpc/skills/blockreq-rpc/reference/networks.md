# BlockReq networks

Generated from BlockReq's production catalog; the same data is in https://blockreq.com/docs/networks.json. Private URL: `https://<host>/v1/rpc/<API key>`; public trial: `https://<host>/v1/rpc/public`. WSS uses the same paths with `wss://`. Beacon networks serve REST at the host root, not JSON-RPC.

| Network | Protocol | Chain ID | Host | WSS | Data | Proof / debug / trace | Reference |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Ethereum | evm | `1` (`0x1`) | `ethereum-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/ethereum/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/ethereum.json) |
| Base | evm | `8453` (`0x2105`) | `base-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/base/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/base.json) |
| Arbitrum One | evm | `42161` (`0xa4b1`) | `arbitrum-one-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/arbitrum/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/arbitrum.json) |
| Polygon | evm | `137` (`0x89`) | `polygon-bor-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/polygon/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/polygon.json) |
| BSC | evm | `56` (`0x38`) | `bsc-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/bsc/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/bsc.json) |
| Robinhood Chain Mainnet | evm | `4663` (`0x1237`) | `robinhood-mainnet-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/robinhood/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/robinhood.json) |
| Optimism | evm | `10` (`0xa`) | `optimism-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/optimism/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/optimism.json) |
| Scroll | evm | `534352` (`0x82750`) | `scroll-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/scroll/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/scroll.json) |
| Linea | evm | `59144` (`0xe708`) | `linea-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/linea/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/linea.json) |
| Unichain | evm | `130` (`0x82`) | `unichain-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/unichain/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/unichain.json) |
| Blast | evm | `81457` (`0x13e31`) | `blast-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/blast/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/blast.json) |
| opBNB | evm | `204` (`0xcc`) | `opbnb-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/opbnb/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/opbnb.json) |
| Avalanche | evm | `43114` (`0xa86a`) | `avalanche-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/avalanche/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/avalanche.json) |
| Gnosis | evm | `100` (`0x64`) | `gnosis-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/gnosis/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/gnosis.json) |
| Berachain | evm | `80094` (`0x138de`) | `berachain-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/berachain/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/berachain.json) |
| Celo | evm | `42220` (`0xa4ec`) | `celo-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/celo/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/celo.json) |
| Sonic | evm | `146` (`0x92`) | `sonic-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/sonic/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/sonic.json) |
| Cronos | evm | `25` (`0x19`) | `cronos-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/cronos/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/cronos.json) |
| Arc | evm | `5042` (`0x13b2`) | `arc-rpc.blockreq.com` | yes | full | no | [docs](https://blockreq.com/docs/build/api-reference/arc/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/arc.json) |
| Ethereum Beacon Chain | beacon | `1` (`0x1`) | `ethereum-beacon-rpc.blockreq.com` | no | full | no |  |
| Ethereum Sepolia | evm | `11155111` (`0xaa36a7`) | `ethereum-sepolia-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/ethereum-sepolia/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/ethereum-sepolia.json) |
| Base Sepolia | evm | `84532` (`0x14a34`) | `base-sepolia-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/base-sepolia/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/base-sepolia.json) |
| Arbitrum Sepolia | evm | `421614` (`0x66eee`) | `arbitrum-sepolia-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/arbitrum-sepolia/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/arbitrum-sepolia.json) |
| Polygon Amoy | evm | `80002` (`0x13882`) | `polygon-amoy-bor-rpc.blockreq.com` | yes | archive | yes | [docs](https://blockreq.com/docs/build/api-reference/polygon-amoy/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/polygon-amoy.json) |
| Optimism Sepolia | evm | `11155420` (`0xaa37dc`) | `optimism-sepolia-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/optimism-sepolia/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/optimism-sepolia.json) |
| Gnosis Chiado | evm | `10200` (`0x27d8`) | `gnosis-chiado-rpc.blockreq.com` | yes | archive | no | [docs](https://blockreq.com/docs/build/api-reference/gnosis-chiado/index.md) · [OpenRPC](https://blockreq.com/docs/openrpc/gnosis-chiado.json) |
