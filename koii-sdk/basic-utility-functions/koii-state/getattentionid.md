# getAttentionId

This function gets the attention contract ID running on the bundler.

### Example Code

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();

async function testGetAttentionId() {
    const attentionContractID= await ktools.getAttentionId();
    console.log("attentionContractID :", attentionContractID);
}

testGetAttentionId();
```

### Example Code Output

![](https://lh5.googleusercontent.com/-9mQ3se03z2Lq3OSmxtT3xyV4iSw9qgye2pHX4Ckwk6M8UkrBaEqJKiaGchNxGqan0vrsDmXPRJQzUCvWgJlGhyRQHZM-USaIBZyuDU-I73ouQL4kgWmzVHL3wMfGse7hjZrS7-5)

### Returns

**Promise \<string>** - Attention contract ID running on the bundler as a string
