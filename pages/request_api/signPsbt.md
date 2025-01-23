# Method `signPsbt`

`rpc`

```
Parameters: {
  psbt: string, // base64 encoded string of the psbt
  broadcast?: boolean // whether to broadcast the transaction
}

Returns: {
  psbt: string, // base64 encoded string of the psbt,
  txid?: string, // txid if the transaction was broadcast
}
```

---

`draft`

```
Parameters: {
  account?: string, // first external account address

  sign?: {
    [address: string]: int[] // indices to sign
  },
}
```

> Alternative: `hex` for hex encoded PSBT
> Todo: `allowedSighash` (plural?) for sighash types

## Notes

### Signing

1. The wallet MAY try to sign all inputs if `sign` is NOT provided.
2. The wallet SHOULD try to sign the inputs potentially marked encoded in the PSBT.
3. The wallet SHOULD try to sign the inputs given by the `sign` object and respective address.
