# Method `getAddresses`

`rpc`

```
Parameters: {}


Returns: {
  addresses: {
    address: string,
    publicKey?: string,
    symbol?: string, // symbol of the coin/token
  }[],
}
```

---

`draft`

> **Note**: The following request parameters are still in development.

```
Parameters: {
  types?: string[],
  purposes?: string[],
  count?: number
}


Returns: {
  addresses: {
    address: string,
    publicKey?: string,
    path?: string,
    purpose?: string,
  }[],
}
```

> Purposes: `'payment' | 'change' | 'ordinals'` etc.
>
> Types: `'p2pkh' | 'p2sh' | 'p2wpkh-p2sh' | 'p2wpkh' | 'p2tr'`
