# getKoiiState

This endpoint returns the state of KOII. Balances, stakes, Koii tasks and all the other information can be programmatically accessed through this endpoint.

### Example Code

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();

async function testGetKoiiState() {
    const koiiState = await ktools.getKoiiState();
    console.log(koiiState);
}

testGetKoiiState();
```

### Example Code Output

![](https://lh6.googleusercontent.com/mHe7rku6WtxR1HSKOK\_uLgI\_1t1Ul9zNDsxBCe6DriJUmldfxdDL7x0bbuQfERVoLx1YVGG\_59w9VZ4FMBVVMqZz0YC0OEqnWU74eTWu35qsZBng0ja28LTrMphVYm2gamyrzAFT)

{% hint style="info" %}
&#x20;You can alternatively also visit [https://mainnet.koii.live/state](https://mainnet.koii.live/state) to check the Koii State.
{% endhint %}

### Returns

**Promise \<any> -** Information about the current Koii State.
