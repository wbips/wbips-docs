# WBIP003 — Common RPC Parameter Conventions

`accepted` `rpc`

This WBIP RECOMMENDS conventions for future JSON RPC parameter WBIPs.

- RPC methods SHOULD use object parameters (aka named parameters).
- `amount` SHOULD be used for transferring sums of something. If `amount` is used, without more information, it MUST always refer to the smallest denomination of the currency (e.g. sat forBTC, milli-sat for LN).
- All actions that broadcast a transaction SHOULD return include `{ txid: string }` in the response data.
- Addresses SHOULD be strings and not require breaking down into hex / hash + version / public-key / scripts.
- Responses MAY return publickeys (this SHOULD be treated optionally), users/wallet SHOULD be able to control whether they want to leak their public keys or not.
- Ensure JSON serializability: E.g. bigint should be string (in any format a JavaScript constructor accepts)

---

> The below parameters are still in development.

`draft`

- `count` SHOULD be used for requesting a specific number of something (e.g. addresses)
