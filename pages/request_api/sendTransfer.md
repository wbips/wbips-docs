# Method `sendTransfer`

`rpc`

```
Parameters: {
  recipients: {
    address: string,
    amount: number
  }[]
}

Returns: {
  txid: string
}
```

> The above `recipients` parameter matches the legacy webbtc `sendTransfer` method.
> Wallets SHOULD support this parameter.

---

> The below parameters are still in development.

`draft`

```
Parameters: {
  memo?: string, // hex string used for OP_RETURN/OP_DROP (needs further specification)
}
```
