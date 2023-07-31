---
slug: /filecoin-dev
title: Getting Filecoin RPC
---

# Getting Filecoin RPC

## [SDK](https://github.com/lavanet/lava-sdk)

:::caution 

Lava SDK is currently in Alpha. Please observe the documentation on both [frontend](https://docs.lavanet.xyz/sdk-frontend?utm_source=getting-filecoin-rpc&utm_medium=docs&utm_campaign=sdk-alpha) and [backend](https://docs.lavanet.xyz/sdk-backend?utm_source=getting-filecoin-rpc&utm_medium=docs&utm_campaign=sdk-alpha) use before getting started.

:::

### Input

```jsx
// Install lavaSDK with the following command:
// npm i @lavanet/lava-sdk
const { LavaSDK } = require("@lavanet/lava-sdk")

async function useFilecoinMainnet() {

  const filecoinMainnet = await new LavaSDK({
    privateKey: process.env.PRIVATE_KEY,
    chainID: 'FVM',
  });

  const filecoinBlockResponse =  await filecoinMainnet.sendRelay({
    method: "eth_blockNumber",
    params: [],
  });

  console.log(filecoinBlockResponse);
}

(async () => {
    await useFilecoinMainnet();
  })();
```

### Output

<iframe width="100%" src="/img/chains/filecoin_call.webm" frameborder="0" allow="autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

To learn more about our SDK visit the [Getting Started guide](https://docs.lavanet.xyz/sdk-getting-started?utm_source=getting-filecoin-rpc&utm_medium=docs&utm_campaign=sdk-alpha-launch)

<hr />

## [Gateway](https://gateway.lavanet.xyz)

To learn more about using the Lava Gateway visit the [Getting Started guide](/gateway-getting-started)

<hr />
<br />

## Supported APIs

### Specification 📑

https://raw.githubusercontent.com/lavanet/lava/main/cookbook/specs/spec_add_fvm.json


### Protocols 🔗

| Platform  |  jsonrpc/http | jsonrpc/wss 
| --------- | -------- | ------------- |
| Gateway   | ✅       |   ✅         
| SDK       | ✅       | 


### Methods 🛠️
<details>
<summary> List </summary>

- Filecoin.ChainGetBlock
- Filecoin.ChainGetBlockMessages
- Filecoin.ChainGetGenesis
- Filecoin.ChainGetMessage
- Filecoin.ChainGetNode
- Filecoin.ChainGetParentMessages
- Filecoin.ChainGetParentReceipts
- Filecoin.ChainGetPath
- Filecoin.ChainGetTipSet
- Filecoin.ChainGetTipSetAfterHeight
- Filecoin.ChainGetTipSetByHeight
- Filecoin.ChainHasObj
- Filecoin.ChainHead
- Filecoin.ChainNotify
- Filecoin.ChainReadObj
- Filecoin.ClientQueryAsk
- Filecoin.GasEstimateFeeCap
- Filecoin.GasEstimateGasLimit
- Filecoin.GasEstimateGasPremium
- Filecoin.MpoolGetNonce
- Filecoin.MpoolPending
- Filecoin.MpoolPush
- Filecoin.StateAccountKey
- Filecoin.StateAllMinerFaults
- Filecoin.StateCall
- Filecoin.StateChangedActors
- Filecoin.StateCompute
- Filecoin.StateDealProviderCollateralBounds
- Filecoin.StateDecodeParams
- Filecoin.StateGetActor
- Filecoin.StateGetReceipt
- Filecoin.StateListActors
- Filecoin.StateListMessages
- Filecoin.StateListMiners
- Filecoin.StateLookupID
- Filecoin.StateMarketBalance
- Filecoin.StateMarketDeals
- Filecoin.StateMarketParticipants
- Filecoin.StateMarketStorageDeal
- Filecoin.StateMinerActiveSectors
- Filecoin.StateMinerAvailableBalance
- Filecoin.StateMinerDeadlines
- Filecoin.StateMinerFaults
- Filecoin.StateMinerInfo
- Filecoin.StateMinerInitialPledgeCollateral
- Filecoin.StateMinerPartitions
- Filecoin.StateMinerPower
- Filecoin.StateMinerPreCommitDepositForPower
- Filecoin.StateMinerProvingDeadline
- Filecoin.StateMinerRecoveries
- Filecoin.StateMinerSectorAllocated
- Filecoin.StateMinerSectorCount
- Filecoin.StateMinerSectors
- Filecoin.StateNetworkName
- Filecoin.StateNetworkVersion
- Filecoin.StateReadState
- Filecoin.StateReplay
- Filecoin.StateSearchMsg
- Filecoin.StateSearchMsgLimited
- Filecoin.StateSectorExpiration
- Filecoin.StateSectorGetInfo
- Filecoin.StateSectorPartition
- Filecoin.StateSectorPreCommitInfo
- Filecoin.StateVMCirculatingSupplyInternal
- Filecoin.StateVerifiedClientStatus
- Filecoin.StateVerifiedRegistryRootKey
- Filecoin.StateVerifierStatus
- Filecoin.SyncState
- Filecoin.WalletBalance
- Filecoin.WalletValidateAddress
- Filecoin.WalletVerify
- Filecoin.EthAccounts
- Filecoin.EthBlockNumber
- Filecoin.EthCall
- Filecoin.EthChainId
- Filecoin.EthEstimateGas
- Filecoin.EthFeeHistory
- Filecoin.EthGasPrice
- Filecoin.EthGetBalance
- Filecoin.EthGetBlockByHash
- Filecoin.EthGetBlockByNumber
- Filecoin.EthGetBlockTransactionCountByHash
- Filecoin.EthGetBlockTransactionCountByNumber
- Filecoin.EthGetCode
- Filecoin.EthGetFilterChanges
- Filecoin.EthGetFilterLogs
- Filecoin.EthGetLogs
- Filecoin.EthGetMessageCidByTransactionHash
- Filecoin.EthGetStorageAt
- Filecoin.EthGetTransactionByHash
- Filecoin.EthGetTransactionCount
- Filecoin.EthGetTransactionHashByCid
- Filecoin.EthGetTransactionReceipt
- Filecoin.EthMaxPriorityFeePerGas

</details>
