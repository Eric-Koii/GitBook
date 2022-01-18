# validArId

This function checks if a given Arweave wallet address (or) transaction ID is valid.

### Parameters

**arId \<any>** - The Arweave ID to validate, could be a Wallet address (or) Transaction ID.

### Example Code

{% hint style="warning" %}
In the below code example, change the targetAddress to the Arweave wallet address (or) transaction ID for which you want to see the validity and other info.&#x20;
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();

async function testValidArId() {
    let targetAddress = "gZIRmwBIL5nnkAxaFQbGICcUdrOOmBLzqd1LFhd3vSA"
    const isValidAr= await ktools.validArId(targetAddress);
    console.log(isValidAr);
}

testValidArId();
```

### Example Code Output

![](https://lh5.googleusercontent.com/RdRy6ZOaSOtEnB4BijO563b734509i48eu9\_JciAL\_5L6LIgR-rgkv038BpRGPLJkV2GqDcPaCueNWu60y-HAOU89Hn5t1lt4ci4Pf7aoTggavRMJLh\_zeecDhgCCHh0NuHpdLht)

### Returns

Boolean (true or false) - Validity of txId
