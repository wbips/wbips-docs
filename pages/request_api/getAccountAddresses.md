# Method `getAccountAddresses`

`draft` `rpc`

```
Parameters: {
  account: string, // first external address of the account
  intentions?: string[],
  //
  includeAddresses?: string[],
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

> **Intentions**: 'payment' | 'ordinal' | etc

> Only use "current" addresses https://github.com/TowoLabs/walletconnect-docs/blob/main/docs/advanced/multichain/rpc-reference/bitcoin-rpc.md

- Wallets SHOULD return "current" addresses (either UTXO holding, or change addresses) as well as unused addresses up to the gap-limit.
- Wallets MAY also return address objects for optional `includeAddresses` (which can be considered not-"current"), as well as the `account` (account address, which is typically the first non-external address of the account)
