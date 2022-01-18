# getOwnedTxs

Gets all the transactions where the wallet is the owner

### Parameters

**wallet \<string>** - Wallet address as a string

_\[Optional]_ **count \<number>** - The number of results to return

_\[Optional]_ **cursorId \<string>** - **** Cursor ID after which to query results, from data.transactions.edges\[n].cursor

### Example Code

{% hint style="warning" %}
In the below code example, change the`targetAddress` for the address for which you want to see the list of owned transactions.
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
async function testGetOwnedTxs() {
    const targetAddress = "TLzveBksdHu9920L38ybXEncNBwgA5tJxF1FidHlbA8";
    const transactions= await ktools.getOwnedTxs(targetAddress);
    console.log("Owned transactions :", transactions);
    console.log(transactions.data.transactions.edges);
}
 
testGetOwnedTxs();
```

### Example Code Output

![](https://lh3.googleusercontent.com/5NbdpLzOYygONoSGBqMRovpkuNZNmlX-DXFhrC3yHgTGz18QXm95CMzsRFoK1gB03cQ3bKPe38TDWTdweHbPnEJoAxCk59ieQKyGH-RxC56orItOfvFmmwibo3Ca9\_TOqSybHBTn)

### Returns

**Promise \<unknown>** - Object with transaction IDs as keys, and transaction data strings as values
