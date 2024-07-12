# `.signMessage`

`draft` `rpc`

`signMessage`

```
Parameters: {
  message*: string, // message to sign
  address: string, // bitcoin address
}

Returns: {
  signature: string, // hex encoded bytes of the signature
  messageHash: string, // hex encoded bytes of the message hash
  address: string, // bitcoin address used to sign
}
```

## Examples

```js
window.btc.request("signMessage", {
  message: "Hello, world!",
  address: "1KXrWXciRDZUpQwQmuM1DbwsKDLYAYsVLR",
});
```

```js
window.btc.request("signMessage", {
  message: "Hello, world!",
  address: "1KXrWXciRDZUpQwQmuM1DbwsKDLYAYsVLR",
});
```
