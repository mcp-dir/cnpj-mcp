# CNPJ

### Brazilian CNPJ lookup and lawsuit discovery for Claude, Cursor and AI agents

Public CNPJ lookup (legal name, trade name, status, activity, size and partners) plus discovery of the company's and partners' lawsuits in the official gazette (DJEN). Public Receita Federal data, free, no login.

- 🇧🇷 **Public Receita Federal data**
- 🏢 **Full record**: legal name, trade name, status, activity (CNAE), size, city/state and **partners**
- ⚖️ **Discovers lawsuits** of the company (and partners) by name in the official gazette (DJEN)
- 🔒 **Read-only**
- ⚡ **Free, no login, no credentials**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=CNPJ&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_cnpj)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Add custom connector** → name `CNPJ`, URL `https://api.mcp.ai/p_cnpj`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=cnpj&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jbnBqIn0=)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=cnpj&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_cnpj%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_cnpj
```

---

## 2 tools

| Tool | Description |
|---|---|
| `cnpj_consultar` | Consulta cadastral de um CNPJ (grátis): razão social, nome fantasia, situação cadastral, CNAE principal, porte, município/UF e SÓCIOS (QSA). Útil pra identificar a empresa e seus sócios antes de buscar processos. |
| `cnpj_processos` | DESCOBERTA por CNPJ: resolve o CNPJ em razão social (e sócios) e busca os processos por NOME no Diário (DJEN) — grátis, com número de processo completo. Opcionalmente inclui os processos dos sócios. Com os números, enriqueça com as tools datajud. |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_cnpj` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
