# WBIP001 — Wallet API JSON RPC

`draft`

This WBIP proposes using JSON RPC 2.0 for interacting with wallets (be it via browser extensions or other methods).

### History

WebBTC has documented the `.request` method for extensability for a long time. Yet, it has not been used much. This WBIP proposes to make the request method more common and standardized. If the request method is the default/go-to way of interacting with wallets, it will be easier for developers to add new non-standard functions, without reinventing the wheel (or worse [creating a new standard](https://xkcd.com/927/)).

This WBIP introduces a new WBIP tag: "rpc" meant for future WBIPs adding definitions for JSON RPC methods or describing common rules to follow.

For proposing new request methods the following applies:

- The method parameters SHOULD be named for clarity and easier handling of default/optional values.

### Web Interface

For usage in web applications, wallets (e.g. browser extensions) SHOULD provide a global object on `window.webbtc`. This object SHOULD have at least the `.request` method for allowing to send JSON RPC requests to the wallet.

### Example WBIP

`todo: Code example; response wrapped?`
