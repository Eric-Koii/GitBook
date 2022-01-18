# getKoiBalance

This function returns the KOII balance of a given address.

{% hint style="info" %}
This wallet's private key needs to be loaded to retrieve the balance, this function does not take the address as a parameter and return the balance.
{% endhint %}

### Example Code

{% hint style="warning" %}
In the below code example, replace `<walletKeyLocation>` on line 4 with the local path to your wallet key file.
{% endhint %}

```javascript
const knode = require("@_koi/sdk/node");
const ktools = new knode.Node();
async function testGetKoiiBalance() {
    const jwk = await ktools.loadFile(<walletKeyLocation>);
    await ktools.loadWallet(jwk);
    const koiibalance = await ktools.getKoiBalance();
    console.log("KOII balance of given address is ", koiibalance);
}

testGetKoiiBalance();
```

### Example Code Output

![](https://lh6.googleusercontent.com/vcn-PvIp-n4byKCzN4pQkTD\_Mjn-Ob2KQkfW1VeP7zqUc7yky0HP52Kou4Y8e34GrXj004qWXJpcNJ3gWp98PXv4AVpxxXK2g17jNCBxI4vjwuvZRat6-IDRJbhinRQ3kRADKEKE)

### Returns

**Promise \<Number>** - Koii balance of a given address as a number.
