# transferNft

Transfers the NFT ownership to a target address.

### Parameters

* **nftId \<string>** - NFT ID to transfer
* **qty \<number>** - Quantity of NFT balance to transfer
* **target \<string>** - Target address to transfer ownership to
* _\[Optional]_ **reward \<string>** - Custom reward for smartweave transaction

### Example Code

{% hint style="warning" %}
In the below code example, change the `nftID` & `targetAddress` as per your transfer requirements.
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();

async function testTransferNft() {
    const jwk = await ktools.loadFile("arweaveWallet.json");
    await ktools.loadWallet(jwk);
    
    const nftID = "bSTZSSoiX3LEqsacb2wRlQWw58zat9RJ8jQ8sYXo-jY";
    const targetAddress = "7b4ll1zwenRB8jzyESjFNcRls331buyNl231Pe0V9VI";
    const transferTx = await ktools.transferNft(nftID,1,targetAddress);
    console.log(transferTx);
}

testTransferNft();
```

### Example Code Output

![](https://lh4.googleusercontent.com/GTf8WWSxCuTnTT0nYOsUjuJDKUwwLtmpGukVYWx8CiZ-KBRiG68IYjN0MM9nPflTzw4bVI2YWlUY-AulCiBSrP6qH4LeH8dYt7o1IX0weDcmhYbtsmy143ZgMKBRWeBzAzkSGGM1)

### Returns

**Promise \<string>** - Arweave transaction ID of the NFT transfer transaction.
