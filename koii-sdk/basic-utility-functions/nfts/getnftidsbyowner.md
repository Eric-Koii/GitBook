# getNftIdsByOwner

This function returns an array of strings for a list of all the NFTs owned by a given address.

### Parameters

**owner \<string>** - Wallet address of the owner for which the array of NFT IDs has to be returned.

### Example Code

{% hint style="warning" %}
In the below code example, change the ownerAddress to the address for which you want to see the list of NFTs.
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
async function testGetNftIdsByOwner() {
    const ownerAddress = "7b4ll1zwenRB8jzyESjFNcRls331buyNl231Pe0V9VI";
    const nfts = await ktools.getNftIdsByOwner(ownerAddress);
    console.log(nfts);
}

testGetNftIdsByOwner();
```

### Example Code Output

![](https://lh3.googleusercontent.com/ryGqRX7pnlzXjAnU0K8NXfvlwwZlwSwc64cU224nhLpc5GqE3gMdZyT05hk9DvPzJ6QA7dKosQx4ecpsy3p-l9QNNE\_0AIjpjuXLYjdXFYR9bAGXGxkjJVHPzNRw465FKWL-XYLO)

{% hint style="success" %}
In the above example, one of the NFT owned by the address `7b4ll1zwenRB8jzyESjFNcRls331buyNl231Pe0V9VI` is `gZIRmwBIL5nnkAxaFQbGICcUdrOOmBLzqd1LFhd3vSA` which can be accessed via the leaderboard.&#x20;



[https://koi.rocks/content-details/gZIRmwBIL5nnkAxaFQbGICcUdrOOmBLzqd1LFhd3vSA](https://koi.rocks/content-details/gZIRmwBIL5nnkAxaFQbGICcUdrOOmBLzqd1LFhd3vSA)
{% endhint %}

### Returns

**Promise\<string\[]>** - Array containing the NFTs with the address as owner address.
