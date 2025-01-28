# Method `signPsbt`

`rpc`

```
Parameters: {
  psbt: string, // hex encoded psbt
  signInputs?: number[] | {
    index: number,
    address?: string,
    publicKey?: string,
    allowedSighash?: Sighash[] // default: [Sighash.ALL]
  }[],
  finalize?: boolean // default: true
  broadcast?: boolean // default: false
}

Sighash: "ALL" | "NONE" | "SINGLE" | "ANYONECANPAY"

Returns: {
  txid?: string
  psbt: string
}
```

## Notes

### Signing

1. The wallet MAY try to sign all inputs if `signInputs` is NOT provided.
2. The wallet SHOULD try to sign the inputs potentially marked encoded in the PSBT using the BIP32 derivation path.
3. The wallet SHOULD try to sign the inputs given by the `signInputs` object and respective address.

---

> The below parameters are still in development.

`draft`

```
Parameters: {
  account?: string, // first external account address
}
```

> Alternative?: `hex` for hex encoded PSBT
