# BlockReq EVM JSON-RPC methods

Generated from the templates behind BlockReq's API reference. The page for a method on another network is `https://blockreq.com/docs/build/api-reference/<network slug>/<method>/index.md`; network slugs and OpenRPC documents are in [networks.md](networks.md).

| Method | Description | Counts as | Networks |
| --- | --- | ---: | --- |
| [`debug_traceBlockByNumber`](https://blockreq.com/docs/build/api-reference/ethereum/debug_traceBlockByNumber/index.md) | Returns traces for all transactions in a block | 20 | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`debug_traceCall`](https://blockreq.com/docs/build/api-reference/ethereum/debug_traceCall/index.md) | Traces a call without submitting a transaction | 5 | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`debug_traceTransaction`](https://blockreq.com/docs/build/api-reference/ethereum/debug_traceTransaction/index.md) | Returns the detailed trace of a transaction execution | 5 | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`eth_blockNumber`](https://blockreq.com/docs/build/api-reference/ethereum/eth_blockNumber/index.md) | Returns the latest block number | 1 | all 25 |
| [`eth_call`](https://blockreq.com/docs/build/api-reference/ethereum/eth_call/index.md) | Executes a new message call without creating a transaction | 1 | all 25 |
| [`eth_chainId`](https://blockreq.com/docs/build/api-reference/ethereum/eth_chainId/index.md) | Returns the chain ID of the current network | 1 | all 25 |
| [`eth_estimateGas`](https://blockreq.com/docs/build/api-reference/ethereum/eth_estimateGas/index.md) | Estimates gas needed for a transaction | 1 | all 25 |
| [`eth_feeHistory`](https://blockreq.com/docs/build/api-reference/ethereum/eth_feeHistory/index.md) | Returns base fee per gas and effective priority fee history | 1 | all 25 |
| [`eth_gasPrice`](https://blockreq.com/docs/build/api-reference/ethereum/eth_gasPrice/index.md) | Returns the current gas price in wei | 1 | all 25 |
| [`eth_getBalance`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBalance/index.md) | Returns the balance of an account | 1 | all 25 |
| [`eth_getBlobSidecarByTxHash`](https://blockreq.com/docs/build/api-reference/bsc/eth_getBlobSidecarByTxHash/index.md) | Returns blob sidecars for a transaction hash | 1 | 1: bsc |
| [`eth_getBlobSidecars`](https://blockreq.com/docs/build/api-reference/bsc/eth_getBlobSidecars/index.md) | Returns all blob sidecars for a block | 1 | 1: bsc |
| [`eth_getBlockByHash`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockByHash/index.md) | Returns information about a block by hash | 1 | all 25 |
| [`eth_getBlockByNumber`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockByNumber/index.md) | Returns information about a block by block number | 1 | all 25 |
| [`eth_getBlockReceipts`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockReceipts/index.md) | Returns all transaction receipts in a block | 3 | all 25 |
| [`eth_getBlockTransactionCountByHash`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockTransactionCountByHash/index.md) | Returns the number of transactions in a block by hash | 1 | all 25 |
| [`eth_getBlockTransactionCountByNumber`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockTransactionCountByNumber/index.md) | Returns the number of transactions in a block by number | 1 | all 25 |
| [`eth_getCode`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getCode/index.md) | Returns the code at a given address | 1 | all 25 |
| [`eth_getFilterChanges`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getFilterChanges/index.md) | Polls for changes since last call | 1 | all 25 |
| [`eth_getFilterLogs`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getFilterLogs/index.md) | Returns all logs for a filter | 1 | all 25 |
| [`eth_getFinalizedBlock`](https://blockreq.com/docs/build/api-reference/bsc/eth_getFinalizedBlock/index.md) | Returns the latest finalized block | 1 | 1: bsc |
| [`eth_getFinalizedHeader`](https://blockreq.com/docs/build/api-reference/bsc/eth_getFinalizedHeader/index.md) | Returns the latest finalized block header (BSC fast finality) | 1 | 1: bsc |
| [`eth_getLogs`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getLogs/index.md) | Returns logs matching a filter | 1 | all 25 |
| [`eth_getProof`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getProof/index.md) | Returns account and storage Merkle proofs for an address at a block | 3 | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`eth_getStorageAt`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getStorageAt/index.md) | Returns the value from a contract storage slot | 1 | all 25 |
| [`eth_getTransactionByBlockHashAndIndex`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionByBlockHashAndIndex/index.md) | Returns transaction by block hash and index | 1 | all 25 |
| [`eth_getTransactionByBlockNumberAndIndex`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionByBlockNumberAndIndex/index.md) | Returns transaction by block number and index | 1 | all 25 |
| [`eth_getTransactionByHash`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionByHash/index.md) | Returns transaction details by hash | 1 | all 25 |
| [`eth_getTransactionCount`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionCount/index.md) | Returns the number of transactions sent from an address (nonce) | 1 | all 25 |
| [`eth_getTransactionReceipt`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionReceipt/index.md) | Returns the receipt of a transaction by hash | 1 | all 25 |
| [`eth_getTransactionsByBlockNumber`](https://blockreq.com/docs/build/api-reference/bsc/eth_getTransactionsByBlockNumber/index.md) | Returns all transactions for a block number | 1 | 1: bsc |
| [`eth_health`](https://blockreq.com/docs/build/api-reference/bsc/eth_health/index.md) | Returns node health status | 1 | 1: bsc |
| [`eth_maxPriorityFeePerGas`](https://blockreq.com/docs/build/api-reference/ethereum/eth_maxPriorityFeePerGas/index.md) | Returns a suggestion for a priority fee (tip) | 1 | all 25 |
| [`eth_newBlockFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_newBlockFilter/index.md) | Creates a filter for new blocks | 1 | all 25 |
| [`eth_newFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_newFilter/index.md) | Creates a new log filter | 1 | all 25 |
| [`eth_newPendingTransactionFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_newPendingTransactionFilter/index.md) | Creates a filter for pending transactions | 1 | all 25 |
| [`eth_sendRawTransaction`](https://blockreq.com/docs/build/api-reference/ethereum/eth_sendRawTransaction/index.md) | Submits a pre-signed transaction for broadcast | 1 | all 25 |
| [`eth_subscribe`](https://blockreq.com/docs/build/api-reference/ethereum/eth_subscribe/index.md) | Subscribes to EVM events over WebSocket | 1 | all 25 |
| [`eth_uninstallFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_uninstallFilter/index.md) | Uninstalls a filter | 1 | all 25 |
| [`eth_unsubscribe`](https://blockreq.com/docs/build/api-reference/ethereum/eth_unsubscribe/index.md) | Unsubscribe from a previously created subscription | 1 | all 25 |
| [`net_listening`](https://blockreq.com/docs/build/api-reference/ethereum/net_listening/index.md) | Returns `true` if the client is actively listening for network connections | 1 | all 25 |
| [`net_peerCount`](https://blockreq.com/docs/build/api-reference/ethereum/net_peerCount/index.md) | Returns the number of peers currently connected to the client | 1 | all 25 |
| [`net_version`](https://blockreq.com/docs/build/api-reference/ethereum/net_version/index.md) | Returns the current network ID as a string | 1 | all 25 |
| [`trace_block`](https://blockreq.com/docs/build/api-reference/ethereum/trace_block/index.md) | Returns all traces for a block (Erigon format) | 20 | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`trace_filter`](https://blockreq.com/docs/build/api-reference/ethereum/trace_filter/index.md) | Returns traces matching block and address filters | 5 | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`trace_transaction`](https://blockreq.com/docs/build/api-reference/ethereum/trace_transaction/index.md) | Returns trace for a single transaction (Erigon format) | 5 | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`web3_clientVersion`](https://blockreq.com/docs/build/api-reference/ethereum/web3_clientVersion/index.md) | Returns the client software version | 1 | all 25 |
| [`web3_sha3`](https://blockreq.com/docs/build/api-reference/ethereum/web3_sha3/index.md) | Returns the Keccak-256 hash of the given data | 1 | all 25 |
