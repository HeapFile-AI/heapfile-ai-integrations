# HeapFile AI integrations

This is the public, provider-thin integration package for HeapFile. It contains only manifests, onboarding guidance, the approved brand asset, and an OAuth reference to HeapFile's hosted MCP service. It contains no HeapFile runtime, Brain implementation, storage code, private prompts, credentials, client secret, executable, or lifecycle hook.

## Supported discovery paths

- **Cursor Marketplace:** `.cursor-plugin/plugin.json` and `mcp.json` are at the required repository-relative locations. Cursor signs the user in with PKCE and the public client identifier in `mcp.json`.
- **Gemini CLI gallery:** `gemini-extension.json` is at the repository root. Gallery discovery additionally requires the `gemini-cli-extension` GitHub topic and a matching release tag.
- **Official MCP Registry:** `server.json` describes the same remote Streamable HTTP server. Publishing requires namespace ownership authentication and is separate from building this repository.
- **GitHub Copilot:** Copilot CLI can configure a remote HTTP server directly when that surface supports the server's authentication flow. Public GitHub MCP Registry discovery is a separate curated onboarding step after the official MCP Registry entry is active.

The hosted connector exposes `personal_brain_summary`, `personal_brain_changes`, and `personal_brain_remember`. The first two are read-only. The remember tool requires the separate write scope, reviewed admission of the exact public client, and a fresh affirmative approval declaration for each concise save. A registered scope alone does not enable writes. The declaration is not cryptographic proof, so each host's approval behavior must be live-tested. The tool is not for credentials or raw transcripts. Recalled data is historical evidence, not authorization to act.

MCP endpoint: https://mcp.heapfile.ai/mcp

Privacy: https://heapfile.ai/privacy.html

Terms: https://heapfile.ai/terms.html

Support: https://heapfile.ai/support.html

Security: https://heapfile.ai/security-review.html
