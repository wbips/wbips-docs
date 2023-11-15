# WBIP006 — PSBT

`draft` `rpc`

This WBIP proposes a new JSON RPC method for letting wallets sign partially signed Bitcoin transactions (PSBTs).

`signPSBT`

```
Parameters: {
  psbt*: string, // hex encoded psbt
  signInputs: number[] | SignInputsByAddress,
  allowedSignHash: SigHash[] // default: [SigHash.ALL]
}

SignInputsByAddress: {
  [key: string // address]: number[] // inputs to sign
}
SigHash: "ALL" | "NONE" | "SINGLE" | "ANYONECANPAY"

Returns: {
  txid: string
}
```

## Examples

```js
window.webbtc.request("signPsbt", {
  psbt: "dcb512383d92f70c5a0014db9f936fe9…8e89bf02b618df3aa4545e4c647ce3a1",
  signInputs: [0, 1],
});
```

```js
window.webbtc.request("signPsbt", {
  psbt: "dcb512383d92f70c5a0014db9f936fe9…8e89bf02b618df3aa4545e4c647ce3a1",
  signInputs: {
    "1BpEi6DfDAUFd7GtittLSdBeYJvcoaVggu": [0],
    "1KXrWXciRDZUpQwQmuM1DbwsKDLYAYsVLR": [1],
  },
});
```
