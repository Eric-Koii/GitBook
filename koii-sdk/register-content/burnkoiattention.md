# burnKoiAttention

Content creators can earn attention rewards in KOII (in perpetuity) by registering content with KOII network. Register once and get rewarded forever.

This function enables content to earn attention rewards for the content that has already been uploaded on Arweave.

### **Parameters**

* **reward**: (Optional) \<string> Custom reward for smartweave transaction
* **nftTxId:** \<string> ID of the NFT to be preregistered

### Example Code

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
const walletKeyLocation = "arweaveWallet.json";

async function testburnKoiAttention() {
    const jwk = await ktools.loadFile(walletKeyLocation);
    await ktools.loadWallet(jwk);
  
    let txId = "rnc8IO7O7fd8Hovvvmq2YZ4y1CI-O0tdRavSGj_meYE";
    var result = await ktools.burnKoiAttention(txId);
  
    console.log("transaction", result);
}


testburnKoiAttention();
```

### Example Code Output

![](https://lh6.googleusercontent.com/b\_D1pOrDLsje7riO-B0HSBE05i4fZ9UKYFOq636hOrdv2XJY-5J7x\_6ByhpEZ\_00T1sB6JJFNzrz9APqA3jm5LNCDrPjTjLURYMQDQlDk1dgjb7BgBTi71jHmqjmffHndVmeFKy8)

### Returns

**Promise \<string> -** Arweave transaction ID

