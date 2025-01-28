# WBIP002 — Namespaces

`accepted` `rpc`

This WBIP RECOMMENDS a naming convention for scoping JSON RPC methods.

JSON RPC methods, which do NOT strictly apply to the core Bitcoin base layer SHOULD be namespaced under a scope. Their RPC method names SHOULD be structured as follows: `<scope>_<method>`. Where `<scope>` can be a wrapping protocol (e.g. `lbtc` for Liquid Bitcoin).

RPC methods for Bictoin itself SHOULD NOT be namespaced (e.g. `getAddresses`).

It is RECOMMENDED to only add methods for protocols, which somehow relate to Bitcoin (especially RECOMMENDED for layer-2 protocols). These protocols may have their own token/currecny and may even be centralized.

Proposed prefixes:

- `brc20_` — for BRC-20 Ordinal tokens
- `lbtc_` — for Liquid Bitcoin
- `ln_` — for Lightning
- `ord_` — for Bitcoin Ordinal inscriptions
- `rgb_` — for RGB
- `stx_` — for Stacks

## Examples

- `lbtc_getAddresses` — Returns addresses from a Liquid Bitcoin wallet.
- `ln_makeInvoice` — Creates a Lightning BOLT-11 invoice.
- `stx_deployContract` — Deploys a smart contract on Stacks.

## Motivation

There are many layers on top of Bitcoin and many different protocols. This WBIP proposes a naming convention for scoping/naming JSON RPC methods. This is to avoid name collisions and to make it easier to find the right method.
