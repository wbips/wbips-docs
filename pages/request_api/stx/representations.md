Stacks methods may include "post-conditions" or "clarity values".
You can find definitions on how to construct them in JSON below.

## Post-conditions

### STX

```ts
{
  type: 'stx-postcondition',
  address: 'origin' | string | `${string}.${string}`, // Stacks c32-encoded, with optional contract name suffix
  condition: 'eq' | 'gt' | 'gte' | 'lt' | 'lte',
  amount: number | string // `bigint` compatible, amount in micro-STX
}
```

### Fungible token

```ts
{
  type: 'ft-postcondition',
  address: 'origin' | string | `${string}.${string}`, // Stacks c32-encoded, with optional contract name suffix
  condition: 'eq' | 'gt' | 'gte' | 'lt' | 'lte',
  asset: `${string}.${string}::${string}`, // Stacks c32-encoded address, with contract name suffix, with asset suffix
  amount: number | string // `bigint` compatible, amount in lowest integer denomination of fungible token
}
```

### Non-fungible token

```ts
{
  type: 'nft-postcondition',
  address: 'origin' | string | `${string}.${string}`, // Stacks c32-encoded, with optional contract name suffix
  condition: 'sent' | 'not-sent',
  asset: `${string}.${string}::${string}`, // address with contract name suffix with asset suffix, Stacks c32-encoded
  assetId: object, // Any Clarity value (represented as JSON)
}
```

## Clarity values

> **Comment**: For encoding larger than JS `Number` big integers, `string` is used.
> Values should be parseable by the JavaScript `BigInt` constructor.

### `int`

```ts
{
  type: 'int',
  value: number | string // `bigint` compatible
}
```

### `uint`

```ts
{
  type: 'uint',
  value: number | string // `bigint` compatible
}
```

### `buffer`

```ts
{
  type: 'buffer',
  value: string // hex-encoded string
}
```

### `bool` `true`

```ts
{
  type: 'true',
}
```

### `bool` `false`

```ts
{
  type: 'false',
}
```

### `address`

> (aka "standard principal")

```ts
{
  type: 'address',
  value: string // Stacks c32-encoded
}
```

### `contract`

> (aka "contract principal")

```ts
{
  type: 'contract',
  value: `${string}.${string}` // Stacks c32-encoded, with contract name suffix
}
```

### `ok`

> (aka "response ok")

```ts
{
  type: 'ok',
  value: object // Clarity value
}
```

### `err`

> (aka "response err")

```ts
{
  type: 'err',
  value: object // Clarity value
}
```

### `none`

> (aka "optional none")

```ts
{
  type: 'none',
}
```

### `some`

> (aka "optional some")

```ts
{
  type: 'some',
  value: object // Clarity value
}
```

### `list`

```ts
{
  type: 'list',
  value: object[] // Array of Clarity values
}
```

### `tuple`

```ts
{
  type: 'tuple',
  value: Record<string, object> // Record of Clarity values
}
```

### `ascii`

```ts
{
  type: 'ascii',
  value: string // ASCII-compatible string
}
```

### `utf8`

```ts
{
  type: 'utf8',
  value: string
}
```

## References

- [SIP030](https://github.com/janniks/sips/blob/main/sips/sip-030/sip-030-wallet-interface.md)
