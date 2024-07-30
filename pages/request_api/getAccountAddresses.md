# Method `getAccountAddresses`

`draft` `rpc`

```
Parameters: {
  types?: string[],
  count?: number,
  intentions?: string[],
}

Returns: {
  type?: string,
  address: string,
  publicKey?: string,
  intention?: string,
}[]
```

> **Intentions**: 'payment' | 'ordinal' | etc
>
> **Types**: 'p2pkh' | 'p2sh' | 'p2wpkh-p2sh' | 'p2wpkh' | 'p2tr'
