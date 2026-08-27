<details>
<summary>MCP Gateway</summary>

- ✓ **startup** MCPG Gateway version: v0.4.9
- ✓ **startup** Starting MCPG with config: stdin, listen: 0.0.0.0:8080, log-dir: /tmp/gh-aw/mcp-logs/
- ✓ **startup** WASM compilation cache directory: /tmp/gh-aw/wazero-cache
- ✓ **startup** Environment validation passed
- ✓ **startup** Loaded 2 MCP server(s): [github safeoutputs]
- ✓ **startup** Guards sink server ID logging enrichment disabled (no sink server IDs configured)
- ✓ **startup** OpenTelemetry tracing disabled (no OTLP endpoint configured)
- ✓ **backend**
  ```
  Successfully connected to MCP backend server, command=docker
  ```
- 🔍 rpc **safeoutputs**→`tools/list`
- 🔍 rpc **safeoutputs**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"ttlMs":0,"cacheScope":"","tools":[{"description":"Create a new GitHub pull request to propose code changes. Use this after making file edits to submit them for review and merging. The PR will be created from the current branch with your committed changes. This is a write-once declaration for a real intended PR, not a sandbox or probe: do not call it with placeholder content, test titles/bodies, or auth experiments. If you are not ready to open the real PR, use noop or repo...`
- ✓ **backend**
  ```
  Successfully connected to MCP backend server, command=docker
  ```
- 🔍 rpc **github**→`tools/list`
- 🔍 rpc **github**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"ttlMs":0,"cacheScope":"","tools":[{"annotations":{"idempotentHint":false,"readOnlyHint":true,"title":"Get commit details"},"description":"Get details for a commit from a GitHub repository","inputSchema":{"properties":{"detail":{"default":"stats","description":"Level of detail to include for changed files. \"none\" omits stats and files entirely. \"stats\" (default) includes per-file metadata: filename, status, and lines-of-code counts (additions, deletions, changes), with ...`
- 🔍 rpc **github**→`prompts/list`
- 🔍 rpc **github**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"ttlMs":0,"cacheScope":"","prompts":[{"arguments":[{"name":"repo","description":"The repository to assign tasks in (owner/repo).","required":true}],"description":"Assign GitHub Coding Agent to multiple tasks in a GitHub repository.","name":"AssignCodingAgent","icons":[{"src":"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABmJLR0QA/wD/AP+gvaeTAAAC2UlEQVRIicWVMUyTaRjHf/+vVUpOJOdilOYoUvVreq2CDmLOwdlAS5xMbrrhBifjYG7QjYuJw108nZx1huLgYlw0QshxChUK2koxHHcuCmg...`
- ✓ **startup** Starting MCPG in ROUTED mode on 0.0.0.0:8080
- ✓ **startup** Routes: /mcp/<server> where <server> is one of: [github safeoutputs]
- ✓ **startup** TLS not configured — listening on http://0.0.0.0:8080 (set --tls-cert/--tls-key to enable)
- ✓ **backend**
  ```
  Successfully connected to MCP backend server, command=docker
  ```
- 🔍 rpc **github**→`tools/call` `search_repositories`
  
  ```json
  {"params":{"arguments":{"perPage":10,"query":"repo:vinayjain38/skills-agentic-workflows-that-read-the-room"},"name":"search_repositories"}}
  ```
- 🔍 rpc **github**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"_meta":{"io.modelcontextprotocol/serverInfo":{"icons":[{"mimeType":"image/png","src":"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABmJLR0QA/wD/AP+gvaeTAAADK0lEQVRIibWVQWhcVRSGv3Pfy0zGdBIMRWk7iziMTpORptpqiNSNG1dNizaFFlxIoYuCC7NwJdiVlhYprtwpighCF9GtuhCRtuCoaWdqGF7HkE4aWm1CpklmJpl3j4vMS99M2k4G9N+8d8659/8u9553H/zPkscVM5lMf03do6iOKbJXIAGgUBJ0GpHvolKfzOfzCx0BEonRWDRemRD0PaC3zSKXED1fLfdcLJUuV9oC0ukXdluxkyq81Ma4VX9Y4x4p5rOzjwSkUvsSdMkVYE+H5oHmjM9IoTA1FyRM8...`
- 🔍 rpc **github**→`tools/call` `get_file_contents`
  
  ```json
  {"params":{"arguments":{"owner":"vinayjain38","path":"notes/mona-notes.md","repo":"skills-agentic-workflows-that-read-the-room"},"name":"get_file_contents"}}
  ```
- 🔍 rpc **github**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"_meta":{"io.modelcontextprotocol/serverInfo":{"icons":[{"mimeType":"image/png","src":"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABmJLR0QA/wD/AP+gvaeTAAADK0lEQVRIibWVQWhcVRSGv3Pfy0zGdBIMRWk7iziMTpORptpqiNSNG1dNizaFFlxIoYuCC7NwJdiVlhYprtwpighCF9GtuhCRtuCoaWdqGF7HkE4aWm1CpklmJpl3j4vMS99M2k4G9N+8d8659/8u9553H/zPkscVM5lMf03do6iOKbJXIAGgUBJ0GpHvolKfzOfzCx0BEonRWDRemRD0PaC3zSKXED1fLfdcLJUuV9oC0ukXdluxkyq81Ma4VX9Y4x4p5rOzjwSkUvsSdMkVYE+H5oHmjM9IoTA1FyRM8...`
- 🔍 rpc **github**→`tools/call` `get_file_contents`
  
  ```json
  {"params":{"arguments":{"owner":"vinayjain38","path":"site/content/github-info.md","repo":"skills-agentic-workflows-that-read-the-room"},"name":"get_file_contents"}}
  ```
- 🔍 rpc **github**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"_meta":{"io.modelcontextprotocol/serverInfo":{"icons":[{"mimeType":"image/png","src":"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABmJLR0QA/wD/AP+gvaeTAAADK0lEQVRIibWVQWhcVRSGv3Pfy0zGdBIMRWk7iziMTpORptpqiNSNG1dNizaFFlxIoYuCC7NwJdiVlhYprtwpighCF9GtuhCRtuCoaWdqGF7HkE4aWm1CpklmJpl3j4vMS99M2k4G9N+8d8659/8u9553H/zPkscVM5lMf03do6iOKbJXIAGgUBJ0GpHvolKfzOfzCx0BEonRWDRemRD0PaC3zSKXED1fLfdcLJUuV9oC0ukXdluxkyq81Ma4VX9Y4x4p5rOzjwSkUvsSdMkVYE+H5oHmjM9IoTA1FyRM8...`
- 🔍 rpc **github**→`tools/call` `get_file_contents`
  
  ```json
  {"params":{"arguments":{"owner":"vinayjain38","path":"notes/mona-notes.md","repo":"skills-agentic-workflows-that-read-the-room"},"name":"get_file_contents"}}
  ```
- 🔍 rpc **github**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"_meta":{"io.modelcontextprotocol/serverInfo":{"icons":[{"mimeType":"image/png","src":"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABmJLR0QA/wD/AP+gvaeTAAADK0lEQVRIibWVQWhcVRSGv3Pfy0zGdBIMRWk7iziMTpORptpqiNSNG1dNizaFFlxIoYuCC7NwJdiVlhYprtwpighCF9GtuhCRtuCoaWdqGF7HkE4aWm1CpklmJpl3j4vMS99M2k4G9N+8d8659/8u9553H/zPkscVM5lMf03do6iOKbJXIAGgUBJ0GpHvolKfzOfzCx0BEonRWDRemRD0PaC3zSKXED1fLfdcLJUuV9oC0ukXdluxkyq81Ma4VX9Y4x4p5rOzjwSkUvsSdMkVYE+H5oHmjM9IoTA1FyRM8...`
- 🔍 rpc **github**→`tools/call` `get_file_contents`
  
  ```json
  {"params":{"arguments":{"owner":"vinayjain38","path":"site/content/github-info.md","repo":"skills-agentic-workflows-that-read-the-room"},"name":"get_file_contents"}}
  ```
- 🔍 rpc **github**←`resp` `{"jsonrpc":"2.0","id":1,"result":{"_meta":{"io.modelcontextprotocol/serverInfo":{"icons":[{"mimeType":"image/png","src":"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABmJLR0QA/wD/AP+gvaeTAAADK0lEQVRIibWVQWhcVRSGv3Pfy0zGdBIMRWk7iziMTpORptpqiNSNG1dNizaFFlxIoYuCC7NwJdiVlhYprtwpighCF9GtuhCRtuCoaWdqGF7HkE4aWm1CpklmJpl3j4vMS99M2k4G9N+8d8659/8u9553H/zPkscVM5lMf03do6iOKbJXIAGgUBJ0GpHvolKfzOfzCx0BEonRWDRemRD0PaC3zSKXED1fLfdcLJUuV9oC0ukXdluxkyq81Ma4VX9Y4x4p5rOzjwSkUvsSdMkVYE+H5oHmjM9IoTA1FyRM8...`
- ✓ **shutdown** Shutting down gateway...

</details>
