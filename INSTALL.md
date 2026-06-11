# Instalação rápida

Banco do Brasil MCP é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_bb`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=Banco%20do%20Brasil%20MCP&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_bb)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Adicionar conector personalizado** → `Banco do Brasil MCP` / `https://api.mcp.ai/p_bb`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "bb": { "type": "http", "url": "https://api.mcp.ai/p_bb" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=bb&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9iYiJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "bb": { "url": "https://api.mcp.ai/p_bb" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=bb&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_bb%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "bb": { "type": "http", "url": "https://api.mcp.ai/p_bb" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_bb
```

Dúvidas? [bb@mcp.ai](mailto:bb@mcp.ai)
