# loadWallet

Every crypto wallet has a public address and a private key (Used to access the wallet), this function is used for programmatically loading the wallet by reading the private key stored locally.

{% hint style="warning" %}
For developing frontend applications that interact with Finnie extension (login with Finnie), check out Koii-X
{% endhint %}

{% hint style="info" %}
KOII uses Arweave addresses, each public address contains 43 characters. All the information pertaining to the arweave address including transactions, Balance, and other tokens can be viewed on [arweave block explorer](https://viewblock.io/arweave).
{% endhint %}

For example, you can view all the information about the public address `7b4ll1zwenRB8jzyESjFNcRls331buyNl231Pe0V9VI` [here](https://viewblock.io/arweave/address/7b4ll1zwenRB8jzyESjFNcRls331buyNl231Pe0V9VI).

### Parameters

Path to your local wallet file that contains the private key

### Example Code

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
const walletKeyLocation = "<Path to your local wallet file>";

async function testLoadWallet() {
    const jwk = await ktools.loadFile(walletKeyLocation);
    await ktools.loadWallet(jwk);  
    console.log("Loaded wallet with address", await ktools.getWalletAddress());
}
  
testLoadWallet();
```

### Example Code Output

![](https://lh5.googleusercontent.com/rSZeHXs-ZPH9ybbeeAGa6DvfgRVvZRNFTGG1BuldIIv3nAMvQ6Sy-WHQwfEJ2HIqOjZUrF03KmX1B3whBa1Hmmx\_KVPwume8m4EH-ikatD9dA-08O0W41CXtli5voSOaOSqVmRab)

### Returns

**Promise \<String>** - Wallet Address&#x20;
