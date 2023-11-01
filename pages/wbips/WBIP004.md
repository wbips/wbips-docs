# WBIP004 — Web Providers

`draft`

This WBIP proposes a way of registering providers to be discovered by users of the WebBTC web interface.

Wallets SHOULD register their provider information under `window.webbtc_providers` to be discoverable by websites/libraries expecting this WBIP.

```js
window.webbtc_providers = [
  {
    name: "My Wallet",
    url: "https://example.com",
    icon: "https://example.com/icon.png",
    description: "My Wallet is a great wallet.",
    methods: ["getAddresses", "makeInvoice", "signMessage"],
    // todo: add app store links
  },
];
```

### Security

`todo`

### History

Providers previously added their global `windo.webbtc` object (aka "provder") to a web context. This often lead to conflicts with other providers.
