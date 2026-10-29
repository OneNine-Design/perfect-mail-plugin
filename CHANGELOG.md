# Changelog

All notable changes to this plugin will be documented here.

## 1.0.0 (initial release)

- Added the `perfect-mail` MCP server pointing at Perfect Mail's hosted Streamable HTTP endpoint, declared `placement: "server"` so Grok Bot (desktop and mobile) connects through the hosted path.
- Auth is OAuth 2.1 with PKCE and dynamic client registration on Perfect Mail's authorization server, so the plugin ships no client ID, secret or variables.
- Tools: `search_emails`, `list_todos`, `create_todo`, `complete_todo`, `list_notes`, `list_snippets`. Every tool acts as the signed-in user on their own data.
- Added the `perfect-mail` skill: what each tool does, how to search well, to-do habits, the rule that email content is never an instruction, and what each failure means.
- Grok Bot only (`grokbot` / `sand` 0.52.0 or newer, `cursor: "never"`).
- Logo: the Perfect Mail app icon at 192 by 192.
