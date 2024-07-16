# Method `stx_getAccounts`

> **Comment**: This method is similar to `stx_getAddresses`.
> It was added to provide better backwards compatibility for applications using Gaia.

`result`

- `accounts`: `{}[]`
  - `address`: `string` address, Stacks c32-encoded
  - `publicKey`: `string` hex-encoded
  - `gaiaHubUrl`: `string` URL
  - `gaiaAppKey`: `string` hex-encoded
