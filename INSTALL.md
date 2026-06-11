# Instalação rápida

CNPJ é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_cnpj`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

Este MCP é **grátis e sem login** pra uso básico — funciona assim que você instala. (Login opcional via `app.mcp.ai` só dá limites maiores / histórico.)

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=CNPJ&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_cnpj)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Adicionar conector personalizado** → `CNPJ` / `https://api.mcp.ai/p_cnpj`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "cnpj": { "type": "http", "url": "https://api.mcp.ai/p_cnpj" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=cnpj&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jbnBqIn0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "cnpj": { "url": "https://api.mcp.ai/p_cnpj" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=cnpj&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_cnpj%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "cnpj": { "type": "http", "url": "https://api.mcp.ai/p_cnpj" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_cnpj
```

Dúvidas? [cnpj@mcp.ai](mailto:cnpj@mcp.ai)
