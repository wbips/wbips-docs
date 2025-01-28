# WBIP004 — Registering Web Providers

`draft`

> **todo:** also consider EIP inspired provider discovery (events/messages) as well as wallet standard

This WBIP proposes a way of registering providers to be discovered by users of the WebBTC web interface.

Wallets SHOULD register their provider information under `window.wbip_providers` to be discoverable by websites/libraries expecting this WBIP.

```js
if (!window.wbip_providers) window.wbip_providers = []; // SHOULD make sure the array exists

// SHOULD `.push`, NEVER overwrite the whole array
window.wbip_providers.push = {
  id: "MyWalletProvider",
  name: "My Wallet",
  icon: "data:image/svg+xml;base64,PHN2Z..ZnPgo=",

  webUrl: "https://example.com/wallet",

  chromeWebStoreUrl:
    "https://chrome.google.com/webstore/detail/hiro-wallet/xxxxxyyyyyzzzzz",
  mozillaAddOnsUrl:
    "https://addons.mozilla.org/en-US/firefox/addon/xxxxxyyyyyzzzzz",
  googlePlayStoreUrl:
    "https://play.google.com/store/apps/details?id=ixxxxxyyyyyzzzzz",
  iOSAppStoreUrl: "https://apps.apple.com/app/hiro-wallet/idxxxxxyyyyyzzzzz",

  methods: ["getAddresses", "makeInvoice", "signMessage"],
};
```

The `.id` is used to find the global provider object injected by the wallet.
E.g., `MyWalletProvider` would be found under `window.MyWalletProvider`.

### Types

```ts
interface Provider {
  id: string; // Path on global/window object
  name: string; // Name shown in UI components
  icon: string; // Data URI of an iamge to show in UI components

  webUrl?: string; // URL to website

  chromeWebStoreUrl?: string; // URL to Chrome Web Store Page
  mozillaAddOnsUrl?: string; // URL to Mozilla Add-Ons Page
  googlePlayStoreUrl?: string; // URL to Google Play Store Page
  iOSAppStoreUrl?: string; // URL to iOS App Store Page

  methods?: string[]; // List of methods supported by this provider
}
```

### Security

`todo`

### History

Providers previously added their global `window.btc` object (aka "provider") to a web context. This often lead to conflicts with other providers.

### `TODO`

- Should a `.provider` property be added, which references the actual provider object?
  This would make it easier to have the provider object live on a nested path, e.g., `window.MyWalletProvider` (with `id = 'mywallet.provider'`).
