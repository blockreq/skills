# BlockReq EVM JSON-RPC methods

Generated from the templates behind BlockReq's API reference. The page for a method on another network is `https://blockreq.com/docs/build/api-reference/<network slug>/<method>/index.md`; network slugs and OpenRPC documents are in [networks.md](networks.md).

| Method | Description | Networks |
| --- | --- | --- |
| [`debug_traceBlockByNumber`](https://blockreq.com/docs/build/api-reference/ethereum/debug_traceBlockByNumber/index.md) | Returns traces for all transactions in a block | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`debug_traceCall`](https://blockreq.com/docs/build/api-reference/ethereum/debug_traceCall/index.md) | Traces a call without submitting a transaction | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`debug_traceTransaction`](https://blockreq.com/docs/build/api-reference/ethereum/debug_traceTransaction/index.md) | Returns the detailed trace of a transaction execution | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`eth_blockNumber`](https://blockreq.com/docs/build/api-reference/ethereum/eth_blockNumber/index.md) | Returns the latest block number | all 24 |
| [`eth_call`](https://blockreq.com/docs/build/api-reference/ethereum/eth_call/index.md) | Executes a new message call without creating a transaction | all 24 |
| [`eth_chainId`](https://blockreq.com/docs/build/api-reference/ethereum/eth_chainId/index.md) | Returns the chain ID of the current network | all 24 |
| [`eth_estimateGas`](https://blockreq.com/docs/build/api-reference/ethereum/eth_estimateGas/index.md) | Estimates gas needed for a transaction | all 24 |
| [`eth_feeHistory`](https://blockreq.com/docs/build/api-reference/ethereum/eth_feeHistory/index.md) | Returns base fee per gas and effective priority fee history | all 24 |
| [`eth_gasPrice`](https://blockreq.com/docs/build/api-reference/ethereum/eth_gasPrice/index.md) | Returns the current gas price in wei | all 24 |
| [`eth_getBalance`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBalance/index.md) | Returns the balance of an account | all 24 |
| [`eth_getBlobSidecarByTxHash`](https://blockreq.com/docs/build/api-reference/bsc/eth_getBlobSidecarByTxHash/index.md) | Returns blob sidecars for a transaction hash | 1: bsc |
| [`eth_getBlobSidecars`](https://blockreq.com/docs/build/api-reference/bsc/eth_getBlobSidecars/index.md) | Returns all blob sidecars for a block | 1: bsc |
| [`eth_getBlockByHash`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockByHash/index.md) | Returns information about a block by hash | all 24 |
| [`eth_getBlockByNumber`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockByNumber/index.md) | Returns information about a block by block number | all 24 |
| [`eth_getBlockReceipts`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockReceipts/index.md) | Returns all transaction receipts in a block | all 24 |
| [`eth_getBlockTransactionCountByHash`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockTransactionCountByHash/index.md) | Returns the number of transactions in a block by hash | all 24 |
| [`eth_getBlockTransactionCountByNumber`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getBlockTransactionCountByNumber/index.md) | Returns the number of transactions in a block by number | all 24 |
| [`eth_getCode`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getCode/index.md) | Returns the code at a given address | all 24 |
| [`eth_getFilterChanges`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getFilterChanges/index.md) | Polls for changes since last call | all 24 |
| [`eth_getFilterLogs`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getFilterLogs/index.md) | Returns all logs for a filter | all 24 |
| [`eth_getFinalizedBlock`](https://blockreq.com/docs/build/api-reference/bsc/eth_getFinalizedBlock/index.md) | Returns the latest finalized block | 1: bsc |
| [`eth_getFinalizedHeader`](https://blockreq.com/docs/build/api-reference/bsc/eth_getFinalizedHeader/index.md) | Returns the latest finalized block header (BSC fast finality) | 1: bsc |
| [`eth_getLogs`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getLogs/index.md) | Returns logs matching a filter | all 24 |
| [`eth_getProof`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getProof/index.md) | Returns account and storage Merkle proofs for an address at a block | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`eth_getStorageAt`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getStorageAt/index.md) | Returns the value from a contract storage slot | all 24 |
| [`eth_getTransactionByBlockHashAndIndex`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionByBlockHashAndIndex/index.md) | Returns transaction by block hash and index | all 24 |
| [`eth_getTransactionByBlockNumberAndIndex`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionByBlockNumberAndIndex/index.md) | Returns transaction by block number and index | all 24 |
| [`eth_getTransactionByHash`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionByHash/index.md) | Returns transaction details by hash | all 24 |
| [`eth_getTransactionCount`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionCount/index.md) | Returns the number of transactions sent from an address (nonce) | all 24 |
| [`eth_getTransactionReceipt`](https://blockreq.com/docs/build/api-reference/ethereum/eth_getTransactionReceipt/index.md) | Returns the receipt of a transaction by hash | all 24 |
| [`eth_getTransactionsByBlockNumber`](https://blockreq.com/docs/build/api-reference/bsc/eth_getTransactionsByBlockNumber/index.md) | Returns all transactions for a block number | 1: bsc |
| [`eth_health`](https://blockreq.com/docs/build/api-reference/bsc/eth_health/index.md) | Returns node health status | 1: bsc |
| [`eth_maxPriorityFeePerGas`](https://blockreq.com/docs/build/api-reference/ethereum/eth_maxPriorityFeePerGas/index.md) | Returns a suggestion for a priority fee (tip) | all 24 |
| [`eth_newBlockFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_newBlockFilter/index.md) | Creates a filter for new blocks | all 24 |
| [`eth_newFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_newFilter/index.md) | Creates a new log filter | all 24 |
| [`eth_newPendingTransactionFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_newPendingTransactionFilter/index.md) | Creates a filter for pending transactions | all 24 |
| [`eth_sendRawTransaction`](https://blockreq.com/docs/build/api-reference/ethereum/eth_sendRawTransaction/index.md) | Submits a pre-signed transaction for broadcast | all 24 |
| [`eth_subscribe`](https://blockreq.com/docs/build/api-reference/ethereum/eth_subscribe/index.md) | Subscribes to EVM events over WebSocket | all 24 |
| [`eth_uninstallFilter`](https://blockreq.com/docs/build/api-reference/ethereum/eth_uninstallFilter/index.md) | Uninstalls a filter | all 24 |
| [`eth_unsubscribe`](https://blockreq.com/docs/build/api-reference/ethereum/eth_unsubscribe/index.md) | Unsubscribe from a previously created subscription | all 24 |
| [`net_listening`](https://blockreq.com/docs/build/api-reference/ethereum/net_listening/index.md) | Returns `true` if the client is actively listening for network connections | all 24 |
| [`net_peerCount`](https://blockreq.com/docs/build/api-reference/ethereum/net_peerCount/index.md) | Returns the number of peers currently connected to the client | all 24 |
| [`net_version`](https://blockreq.com/docs/build/api-reference/ethereum/net_version/index.md) | Returns the current network ID as a string | all 24 |
| [`trace_block`](https://blockreq.com/docs/build/api-reference/ethereum/trace_block/index.md) | Returns all traces for a block (Erigon format) | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`trace_filter`](https://blockreq.com/docs/build/api-reference/ethereum/trace_filter/index.md) | Returns traces matching block and address filters | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`trace_transaction`](https://blockreq.com/docs/build/api-reference/ethereum/trace_transaction/index.md) | Returns trace for a single transaction (Erigon format) | 9: ethereum, base, arbitrum, polygon, bsc, ethereum-sepolia, base-sepolia, arbitrum-sepolia, polygon-amoy |
| [`web3_clientVersion`](https://blockreq.com/docs/build/api-reference/ethereum/web3_clientVersion/index.md) | Returns the client software version | all 24 |
| [`web3_sha3`](https://blockreq.com/docs/build/api-reference/ethereum/web3_sha3/index.md) | Returns the Keccak-256 hash of the given data | all 24 |
