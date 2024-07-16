# Method `signPsbt`

`draft` `rpc`

```
Parameters: {
  psbt: string, // base64 encoded string of the psbt
  sign: {
    [address: string]: int[] // index to sign
  },
  broadcast?: boolean // whether to broadcast the transaction
}
```

---

> Alternative: `hex` for hex encoded PSBT
> Todo: `allowedSighash` (plural?) for sighash types
