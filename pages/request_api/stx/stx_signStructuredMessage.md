# Method `stx_signStructuredMessage`

`params`

- `message`: [`ClarityValue[] | string[]`](./representations.md), Clarity values or hex-encoded strings
- `domain`: [`ClarityValue | string`](./representations.md), Clarity **tuple** value or hex-encoded string (defined by SIP-018)

`result`

- `signature`: `string` hex-encoded
- `publicKey`: `string` hex-encoded
