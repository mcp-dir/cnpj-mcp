# Instalação detalhada

CNPJ é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_cnpj`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_cnpj` | nenhuma (grátis) |
| Cursor | `https://api.mcp.ai/p_cnpj` | nenhuma |
| VS Code (Copilot) | `https://api.mcp.ai/p_cnpj` | nenhuma |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.cnpj` (ou `servers.cnpj` no VS Code) do config do cliente e reinicie.
