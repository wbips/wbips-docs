# Method `stx_transferSip10Nft`

`params`

- `recipient`: `string` address, Stacks c32-encoded
- `asset`: `string` address, Stacks c32-encoded, with contract name suffix
- `assetId`: `ClarityValue`

* `address?`: `string` address, Stacks c32-encoded, defaults to wallets current address
* `network?`: `'mainnet' | 'testnet' | 'devnet' | 'regtest'`
* `fee?`: `number | string` BigInt constructor compatible value
* `nonce?`: `number | string` BigInt constructor compatible value
* `postConditions?`: [`PostCondition[]`](./representations.md), defaults to `[]`
* `postConditionMode?`: `'allow' | 'deny'`
* `attachment?`: `string` hex-encoded
* `sponsored?`: `boolean`, defaults to `false`

`where`

- `ClarityValue`: `string | object` hex-encoded or JSON representation

`result`

- `txid`: `string` hex-encoded
- `transaction`: `string` hex-encoded raw transaction
