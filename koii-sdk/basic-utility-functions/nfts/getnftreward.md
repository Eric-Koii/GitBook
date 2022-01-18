# getNftReward

This function returns attention rewards earned from an NFT in Koii.

### Parameters

**id \<string>** - The transaction id to process for which you have to see the earned attention rewards.

### Example Code

{% hint style="warning" %}
In the below code example, change the targetNft to the NFT ID for which you want to see the attention rewards gained.
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
async function testGetNftReward() {
    const targetNft = "gZIRmwBIL5nnkAxaFQbGICcUdrOOmBLzqd1LFhd3vSA";
    const nftReward = await ktools.getNftReward(targetNft);
    console.log("Attention rewards for the NFT", targetNft);
    console.log(nftReward);
}
testGetNftReward();
```

### Example Code Output

![](https://lh5.googleusercontent.com/bweOHnOrvdnxEg3GAtGql0rPBQPTB9ZQhimXY6cDWdFUP9fDQZWDVEeIvFzXq4O8LwL-rpo1E47qroLRqyGlbb3QV97J0ctYxQ5B-BWE80bzgo5MswSMJACTfVuJ4\_pJZ2VIZ5SY)

### Returns

**Promise\<null | number>** - Koii rewards earned from a given NFT

{% hint style="danger" %}
Koii rewards earned or null if the transaction is not a valid Koii NFT.
{% endhint %}
