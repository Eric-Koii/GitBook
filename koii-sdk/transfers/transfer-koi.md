# transfer (Koi)

Interact with the contract to transfer koi tokens from one wallet to another.

### Parameters

* qty \<number> - Amount of tokens to transfer
* target \<string> - Receiver's wallet address
* token \<string> - The token to be transferred (Koi in this case)
* (optional) reward: string Custom reward for smartweave transaction

{% hint style="info" %}
The same function can be used to [transfer AR tokens](transfer-ar.md) from one wallet to another, we just need to change the token type in the third parameter.
{% endhint %}

### Example Code

{% hint style="warning" %}
In the below code example, change the `qty` & `receiverAddress` as per your transfer requirements.
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();

async function transferKoii() {
  const jwk = await ktools.loadFile("arweaveWallet.json");
  await ktools.loadWallet(jwk);

  const qty = 5;
  const receiverAddress = "TLzveBksdHu9920L38ybXEncNBwgA5tJxF1FidHlbA8";
  const transferTxId = await ktools.transfer(qty, receiverAddress, "KOI");
  console.log("Your transaction is " + transferTxId);
}

transferKoii();
```

### Example Code Output

![](https://lh4.googleusercontent.com/alcHay2Mi4MQUsA0qzHC8q5oP3Nh9kVNivM6IZdTbqgVM5Uas6DWf6jMGJMPTTIkixUkHid1OWD\_avtVZGSHuLxM4y6SenA4RsVhXUx4yRW2qthwYFSfkpNuDWY8DV4pQn1-c1mZ)

### Returns

**Promise \<string>** - Transaction ID of the transfer transaction.
