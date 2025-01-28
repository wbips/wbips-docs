# Method `stx_callContract`

Calls a Stacks smart contract (Clarity) function.

`params`

- `contract`: `string.string` address with contract name suffix, Stacks c32-encoded
- `functionName`: `string`
- `functionArgs`: [`ClarityValue[]`](./representations.md), defaults to `[]`

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
