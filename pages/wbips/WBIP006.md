# WBIP006 — PSBT

`draft` `rpc`

This WBIP proposes a new JSON RPC method for letting wallets sign partially signed Bitcoin transactions (PSBTs).

`signPsbt`

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
}

Sighash: "ALL" | "NONE" | "SINGLE" | "ANYONECANPAY"

Returns: {
  txid: string
}
```

## Examples

```js
window.WalletProvider.request("signPsbt", {
  psbt: "dcb512383d92f70c5a0014db9f936fe9…8e89bf02b618df3aa4545e4c647ce3a1",
  signInputs: [0, 1],
});
```

```js
window.WalletProvider.request("signPsbt", {
  psbt: "dcb512383d92f70c5a0014db9f936fe9…8e89bf02b618df3aa4545e4c647ce3a1",
  signInputs: [
    {
      index: 0,
      address: "1BpEi6DfDAUFd7GtittLSdBeYJvcoaVggu",
    },
    {
      index: 1,
      address: "1KXrWXciRDZUpQwQmuM1DbwsKDLYAYsVLR",
    },
  ],
});
```
