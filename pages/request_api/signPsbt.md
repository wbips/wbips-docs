# Method `signPsbt`

`draft` `rpc`

```
Parameters: {
  psbt: string, // base64 encoded string of the psbt
  sign?: {
    [address: string]: int[] // indices to sign
  },
  broadcast?: boolean // whether to broadcast the transaction
}
```

---

> Alternative: `hex` for hex encoded PSBT
> Todo: `allowedSighash` (plural?) for sighash types

## Notes

### Signing

1. The wallet MAY try to sign all inputs if `sign` is NOT provided.
2. The wallet SHOULD try to sign the inputs potentially marked encoded in the PSBT.
3. The wallet SHOULD try to sign the inputs given by the `sign` object and respective address.
