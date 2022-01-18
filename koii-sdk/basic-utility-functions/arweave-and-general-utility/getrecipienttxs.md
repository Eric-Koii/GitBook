# getRecipientTxs

Gets all the transactions where the wallet is the recipient.

### Parameters

**wallet \<string>** - Wallet address as a string

_\[Optional]_ **count \<number>** - The number of results to return

_\[Optional]_ **cursorId \<string>** - **** Cursor ID after which to query results, from data.transactions.edges\[n].cursor

### Example Code

{% hint style="warning" %}
In the below code example, change`targetAddress` for the address for which you want to see the list of received transactions.
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

![](https://lh4.googleusercontent.com/xT2Kj1Jw29oP4AH1d\_LplQCcr4AYjfjZ2mCHSORUG63RcYDEClaxI002G6HFNraWDTpMZFuidth5CbQ5JxLzY82grVfYvNRemd-kdo7jPWOIWPMK4lD\_kSWdnx7w\_260gYJWRINC)

### Returns

**Promise \<unknown>** - Object with transaction IDs as keys, and transaction data strings as values
