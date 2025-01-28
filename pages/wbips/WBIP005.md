# WBIP005 — Default Bitcoin Methods

`draft` `rpc`

This WBIP proposes some default Bicoin for future JSON RPC parameter WBIPs. This WBIP defines the BTC related RPC methods that wallets MAY implement.

This WBIP mainly exists for backwards compatibility. Refer to the prior documentation for more legacy details.

[`getInfo`](https://balls.dev/webbtc/info/)

```
Parameters: None

Returns: {
  version: number | string,
  methods?: string[],
  supports?: string[]
}
```

[`getAddresses`](https://balls.dev/webbtc/addresses/getAddress/)

```
Parameters: {
  count: number
  types: string[],
  purposes: string[],
}

Returns: {
  address: string,
  type?: string,
  purpose?: string,
  publicKey?: string
}[]

Purpose: 'change' | 'ordinals' | etc
Type: 'p2pkh' | 'p2sh' | 'p2wpkh-p2sh' | 'p2wpkh' | 'p2tr'
```

> Web-applications SHOULD NOT have/need derivation control (as many extensions used to implement), rather the type/purpose control should be enough to cover all use-cases.

[`makeInvoice`](https://balls.dev/webbtc/invoices/makeInvoice/)

```
Parameters: {
  amount: string | number,
  memo?: string,
  label?: string,
  message?: string
}

Returns: {
  paymentRequest: string
}
```

[`signMessage`](https://balls.dev/webbtc/signatures/sign/)

```
Parameters: {
  message: string,
  address?: {}
}

Returns: {
  signature: string,
  messageHash?: string,
  address?: string
}
```

~[`verifyMessage`](https://balls.dev/webbtc/signatures/verify/)~

> `verifyMessage` is not included since technically a wallet / private-key isn’t needed for this. Wallets MAY still decide to implement this or a similar method.

[`sendPayment`](https://balls.dev/webbtc/transactions/send/)

```
Parameters: {
  paymentRequest: string
}

Returns: {
  txid: string
}
```

[`sendTransfer`](https://balls.dev/webbtc/transactions/sendTransaction/)

```
Parameters: {
  recipients: {
    address: string,
    amount: number
  }[]
}
Returns: {
  txid: string
}
```

---

Fields are required, unless they are marked with a `?`.
Exact type/usage definitions are assumed to be self-evident. This document follows a pseudo-definition similar to TypeScript.
