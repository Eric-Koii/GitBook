# getBlockHeight

This function returns the current block height of the Arweave blockchain.

### Example Code

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
async function testGetBlockHeight() {
    const blockNumber= await ktools.getBlockHeight();
    console.log(blockNumber);
}

testGetBlockHeight();
```

### Example Code Output

![](https://lh4.googleusercontent.com/SAdIOq\_IZ0mWaOxWHgOk\_rE2UM89TpAK\_OscpczT6-fCbzDJLK2gv7mUNv4p4IIr8IaMLe4NEtnXO2fASu40MjQd9p5vAFBwT0qU31WjOAWqQ6IvTygBEfoBJgNRaBaJjOdm4kWi)

{% hint style="info" %}
You can check other details and info about the block from [https://viewblock.io/arweave/block/849444](https://viewblock.io/arweave/block/849444)
{% endhint %}

{% hint style="warning" %}
The block height could be different when you try to run the code, change the `849444` in the URL with the block height you have.
{% endhint %}

### Returns

**Promise \<unknown>** - Current block height of Arweave blockchain as a number.
