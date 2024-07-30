# Method `getAddresses`

`draft` `rpc`

`todo: update to other spec`

```
Parameters: {
  types?: string[],
  intentions?: string[],
  count?: number
}

Returns: {
  addresses: {
    address: string,
    path?: string,
    publicKey?: string,
    intention?: string,
  }[],
}
```

> Purposes: 'change' | 'ordinals' | etc
> Types: 'p2pkh' | 'p2sh' | 'p2wpkh-p2sh' | 'p2wpkh' | 'p2tr'
