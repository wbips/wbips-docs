# Method `stx_transferStx`

> **Comment**: This method doesn't take post-conditions.

`params`

- `recipient`: `string` address, Stacks c32-encoded
- `amount`: `number | string` BigInt constructor compatible value
- `memo?`: `string`, defaults to `''`

* `address?`: `string` address, Stacks c32-encoded, defaults to wallets current address
* `network?`: `'mainnet' | 'testnet' | 'devnet' | 'regtest'`
* `fee?`: `number | string` BigInt constructor compatible value
* `nonce?`: `number | string` BigInt constructor compatible value
* `attachment?`: `string` hex-encoded
* `sponsored?`: `boolean`, defaults to `false`
* `broadcast?`: `boolean`, defaults to `true`

`result`

- `txid?`: `string` hex-encoded
- `transaction`: `string` hex-encoded raw transaction
