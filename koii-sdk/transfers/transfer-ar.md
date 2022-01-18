# transfer (AR)

Interact with the contract to transfer AR tokens from one wallet to another.

### Parameters

* qty \<number> - Amount of tokens to transfer
* target \<string> - Receiver's wallet address
* token \<string> - The token to be transferred (AR in this case)
* (optional) reward: string Custom reward for smartweave transaction

{% hint style="info" %}
The same function can be used to [transfer koi tokens](transfer-koi.md) from one wallet to another, we just need to change the token type in the third parameter.
{% endhint %}

### Example Code

{% hint style="warning" %}
In the below code example, change the `qty` & `receiverAddress` as per your transfer requirements.
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();

async function transferAr() {
  const jwk = await ktools.loadFile("arweaveWallet.json");
  await ktools.loadWallet(jwk);

  const qty = 5;
  const receiverAddress = "TLzveBksdHu9920L38ybXEncNBwgA5tJxF1FidHlbA8";
  const transferTxId = await ktools.transfer(qty, receiverAddress, "AR");
  console.log("Your transaction is " + transferTxId);
}

transferAr();
```

### Example Code Output

![](https://lh3.googleusercontent.com/oXDbAp8cR5gwv8fsSw9L13i8E\_iDOlznmvYxiy7d7mDemlWjb-5URDr\_QTJVgQQEgBQlfGoH5eUHB4ZN0kCwB0POOOhCT2C6aySddC3L5jVhOAah7mzjZZMh1-FBPVoWU7JeteTS)

### Returns

**Promise \<string>** - Transaction ID of the transfer transaction.
