# KOII Bridge Server

### Introduction <a href="#introduction" id="introduction"></a>

A KOII Bridge allows you to migrate your NFTs from and to different blockchains. Currently, we only support Ethereum bridging. You could also find more example functions at atomicnft.com.



### Description <a href="#description" id="description"></a>

The bridge is basically divided in 2 parts, The first one includes bridging NFTs to other networks from Arweave and the second part includes bridging NFTs from other networks to Arweave.

#### Arweave To Ethereum <a href="#arweave-to-ethereum" id="arweave-to-ethereum"></a>

The Arweave To Ethereum bridge includes certain steps as indicated in the diagram. The steps are further explained below:

1. The first step to initiate the bridging from Arweave To Ethereum is by locking the NFT you own on the arweave network. Locking the NFT involves calling the lock function on your NFT smart contract. Refer to lockToken.js for code implementation.
2. The next step is to pay the 10 KOII fee for the bridging, which will be used to mint your new NFT on the ethereum. The transfer function must include the nftId and lockTx (Obtained from step 1). Refer to transferToken.js for code implementation.
3. The third and final step from the user end is to submit the arNFTId, arUserAddress, burnKOItx and lockedNFTtx to the server at the /mintEthToken endpoint. The exact JSON body to be passed in that endpoint is as right.

```json
{
  "arNFTId": "<Your Arweave NFT Id>",
  "arUserAddress": "<Your Arweave Wallet Address>",
  "burnKOItx": "<The txId received in step 2 after calling transfer token>",
  "lockedNFTtx": "<The lockedTx Id received in step 1>"
}
```

After submitting the transaction, the server will keep checking the transaction statuses, once they are succeeded and it is verified on the server that fee is paid. An NFT on the ethereum network is minted.

