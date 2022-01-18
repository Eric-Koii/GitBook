# getNftState

This function returns all the details about a given NFT such as creator address, description etc.

### Parameters

**id \<string>** - The transaction id to process for which you have to see all the detailed info.

### Example Code

{% hint style="warning" %}
In the below code example, change the targetNft to the NFT ID for which you want to see the detailed info like creator address, title, description, attention gained, rewards earned etc.&#x20;
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
async function testGetNftState() {
    const targetNft = "gZIRmwBIL5nnkAxaFQbGICcUdrOOmBLzqd1LFhd3vSA";
    const nftState= await ktools.getNftState(targetNft);
    console.log("State of the NFT", targetNft);
    console.log(nftState);
}

testGetNftState();
```

### Example Code Output

![](https://lh3.googleusercontent.com/2QgocLUwDLOpq792O17TiMfC85Ci7ToRrD-sukm7majmVi-CE-d-KHV3HMrzeXF9hxl6Yb4sYa5LUaXDrNTqMH3HnAp2aAhM9M3sparoua2qJ2d7njV2HFyoXeBPPWqwHSnUEwJ0)

### Returns

**Promise \<any>** - All the information pertaining to a given NFT like the state of an NFT including views and reward.
