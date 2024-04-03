# WBIP007 — Batching

`draft` `rpc`

This WBIP proposes a new JSON RPC method for batching multiple requests into a single request.

The "batch" method is a special method that takes an array of requests and returns an array of responses.

`provider.request("batch", params: {}[]): Promise<{}[]>`

A request should have a `method` and `params` property.

The response should have a `result` and `error` property.
