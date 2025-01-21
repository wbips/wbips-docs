# Method `sendTransfer`

`rpc`

```
Parameters: {
  recipients: {
    address: string,
    amount: number
  }[]
}

Returns: { txid: string }
```

> The above `recipients` parameter matches the legacy webbtc `sendTransfer` method.
> Wallets SHOULD support this parameter.

---

`draft`

```
Parameters: {
  recipientAddress: string,
  amount: number,
  changeAddress?: string,

  account?: string,
}

Returns: { txid: string }
```

> The above parameters are still in development.

```
Parameters: {
  memo?: string, // hex string used for OP_RETURN/OP_DROP (needs further specification)
}
```
