# Method `getAddresses`

`draft` `rpc`

```
Parameters: {
  types?: string[],
  purposes?: string[],
  count?: number
}

Returns: {
  type?: string,
  purpose?: string,
  address: string,
  publicKey?: string
}[]
```

> Purposes: 'change' | 'ordinals' | etc
> Types: 'p2pkh' | 'p2sh' | 'p2wpkh-p2sh' | 'p2wpkh' | 'p2tr'
