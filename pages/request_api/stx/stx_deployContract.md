# Method `stx_deployContract`

`params`

- `name`: `string`
- `clarityCode`: `string` Clarity contract code
- `clarityVersion?`: `number`

* `address?`: `string` address, Stacks c32-encoded, defaults to wallets current address
* `network?`: `'mainnet' | 'testnet' | 'devnet' | 'regtest'`
* `fee?`: `number | string` BigInt constructor compatible value
* `nonce?`: `number | string` BigInt constructor compatible value
* `attachment?`: `string` hex-encoded
* `sponsored?`: `boolean`, defaults to `false`

`result`

- `txid`: `string` hex-encoded
- `transaction`: `string` hex-encoded raw transaction
