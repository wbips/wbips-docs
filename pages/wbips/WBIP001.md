# WBIP001 — Wallet API JSON RPC

`draft`

This WBIP proposes using JSON RPC 2.0 for interacting with wallets (be it via browser extensions or other methods).

### History

WebBTC has documented the `.request` method for extensability for a long time.
Yet, it has not been used much.
This WBIP proposes to make the request method more common and standardized.
If the request method is the default/go-to way of interacting with wallets, it will be easier for developers to add new non-standard functions, without reinventing the wheel (or worse [creating a new standard](https://xkcd.com/927/)).

This WBIP introduces new WBIP tags: "rpc" and "event" meant for future WBIPs adding definitions for JSON RPC methods, listenable events, or respectively describing common rules to follow.

For proposing new request methods the following applies:

- The method parameters SHOULD be named for clarity and easier handling of default/optional values; opposed to an parameter array.

### Web Interface

For usage in web applications, wallets (e.g. browser extensions) MAY provide a provider object.
The provider object MAY be injected into the global/window object (e.g. `window.btc`) or re-use an existing compatible interface (e.g. the WebBTC object).

This object SHOULD have at least the `.request` method for allowing to send JSON RPC requests to the wallet.
This object MAY also include the `.listen` and `.unlisten` methods for listening to events.

### Specification

- `provider.request(method: string, params: {}): Promise<>`
- `provider.listen(event: string, listener: (args: any) => void): void`
- `provider.unlisten(event: string, listener: (args: any) => void): void`

### Open Thoughts

- The `.listen` could return a callable unsubscribe function.
- The response from the `.request` method could be a promise that resolves with the result or rejects with an error.
