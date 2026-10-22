---
'@modelcontextprotocol/sdk': patch
---

`Client.listTools()` no longer drops the cached output-schema validators and task metadata when one of the listed tools has an output schema that fails to compile. The refresh still rejects, but the metadata from the last successful `listTools()` stays in place, so `callTool()`
keeps validating structured content instead of silently skipping it.
