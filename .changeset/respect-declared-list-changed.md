---
'@modelcontextprotocol/sdk': patch
---

`McpServer` now keeps `listChanged: false` when it was declared for `tools`, `resources` or `prompts` in the constructor's `capabilities`; before, the first registration overwrote it with `listChanged: true`. A declared capability without `listChanged` is still advertised with
`listChanged: true`.
