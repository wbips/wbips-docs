# A brief history of WBIPs

During the advent of Ordinals, builders quickyl realized the current standards weren're complete enough to build new experiences on Bitcoin.
So, as it often happens, many projects invented their own standards and specs.

Realizing that this might divide the ecosystem, a group of developers and builders came together to create a yet another common standard for web wallets.

This time it should be boiled down to the most simple interaction — an RPC call.

Inspired by the somewhat hidden `.request` method of WebBTC, WBIPs aimed to be compatible with WebBTC (one of the first Bitcoin wallet integrations).
But, to not step on anybody's toes, WBIPs are considered a separate effort.

Builders, wallets, and developers might not agree on the different uses of Bitcoin or its layers.
However, WBIPs aim to be unopinionated and allow for flexible use.
Emphasis is also put on future upgradability and experimentation — to not repeat the cycle of new standards.

---

### RE WebBTC

These improvement proposals were intended to be a sort of v2 for WebBTC for a while.
But, to be less confusing, they are considered theiw own project now.

- Removal of .enable flow of WebBTC
  - The .enable flow is a solution to fingerprinting, which would already be harder to do via dynamic methods. So, a `.request` method should not need it

### RE CAIPs

The proposals were not added as CAIPs for a few reasons.
In general, this is a Bitcoin-first project and less general.

CAIPs seem to have a lot of overhead for the web-app developer.
e.g., Users should be able to switch/choose network/chain, or Wallet should be able to choose/switch on the users behalf.
Also, WBIPs should be usable without the developer needing to figure out what is in "review/final/etc.".
