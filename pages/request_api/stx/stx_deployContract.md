# Method `stx_deployContract`

`params`

- `name`: `string`
- `clarityCode`: `string` Clarity contract code
- `clarityVersion?`: `number`

* `address?`: `string` address, Stacks c32-encoded, defaults to wallets current address
* `network?`: `'mainnet' | 'testnet' | 'devnet' | 'regtest'`
* `fee?`: `number | string` BigInt constructor compatible value
* `nonce?`: `number | string` BigInt constructor compatible value
* `postConditions?`: [`PostCondition[] | string[]`](./representations.md) JSON representation or hex serialized string, defaults to `[]`
* `postConditionMode?`: `'allow' | 'deny'`
* `sponsored?`: `boolean`, defaults to `false`
* `broadcast?`: `boolean`, defaults to `true`

`result`

- `txid`: `string` hex-encoded
- `transaction`: `string` hex-encoded raw transaction
