# Method `stx_transferSip10Ft`

`params`

- `recipient`: `string` address, Stacks c32-encoded
- `asset`: `string` address, Stacks c32-encoded, with contract name suffix
- `amount`: `number | string` BigInt constructor compatible value

* `address?`: `string` address, Stacks c32-encoded, defaults to wallets current address
* `network?`: `'mainnet' | 'testnet' | 'devnet' | 'regtest'`
* `fee?`: `number | string` BigInt constructor compatible value
* `nonce?`: `number | string` BigInt constructor compatible value
* `postConditions?`: [`PostCondition[]`](./representations.md), defaults to `[]`
* `postConditionMode?`: `'allow' | 'deny'`
* `sponsored?`: `boolean`, defaults to `false`
* `broadcast?`: `boolean`, defaults to `true`

`result`

- `txid`: `string` hex-encoded
- `transaction`: `string` hex-encoded raw transaction
