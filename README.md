# CNPJ

### Consulta de CNPJ e descoberta de processos para Claude, Cursor e agentes de IA

Consulta cadastral pública de CNPJ (razão social, nome fantasia, situação, CNAE, porte e sócios) e descoberta dos processos da empresa e dos sócios no Diário de Justiça (DJEN). Dados públicos da Receita Federal, grátis, sem login.

- 🇧🇷 **Dados públicos da Receita Federal**
- 🏢 **Cadastro completo**: razão social, nome fantasia, situação, CNAE, porte, município/UF e **sócios (QSA)**
- ⚖️ **Descobre processos** da empresa (e dos sócios) por nome no Diário de Justiça (DJEN)
- 🔒 **Somente leitura**
- ⚡ **Grátis, sem login, sem credencial**, funciona assim que instala
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=CNPJ&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_cnpj)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Adicionar conector personalizado** → cole **Nome** `CNPJ` e **URL** `https://api.mcp.ai/p_cnpj`.

### Cursor

[➕ Instalar CNPJ no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=cnpj&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jbnBqIn0=)

### VS Code (Copilot Chat)

[➕ Instalar CNPJ no VS Code](vscode:mcp/install?name=cnpj&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_cnpj%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_cnpj
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Consulte o CNPJ 33.000.167/0001-01 e liste os sócios
Quais processos da empresa do CNPJ 33.000.167/0001-01?
Inclua também os processos dos sócios
Qual a situação cadastral e o CNAE principal desse CNPJ?
```

---

## 2 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `cnpj_consultar` | Consulta cadastral de um CNPJ (grátis): razão social, nome fantasia, situação cadastral, CNAE principal, porte, município/UF e SÓCIOS (QSA). Útil pra identificar a empresa e seus sócios antes de buscar processos. |
| `cnpj_processos` | DESCOBERTA por CNPJ: resolve o CNPJ em razão social (e sócios) e busca os processos por NOME no Diário (DJEN) — grátis, com número de processo completo. Opcionalmente inclui os processos dos sócios. Com os números, enriqueça com as tools datajud. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)


---

## Como funciona

```
1. Instala o MCP no seu cliente (Claude / Cursor / VS Code)
2. Pergunta sobre qualquer CNPJ — sem login, sem cadastro
3. cnpj_consultar traz o cadastro + sócios (dados públicos da Receita Federal)
4. cnpj_processos resolve o CNPJ em nome e acha os processos no DJEN
5. Com os números de processo, enriqueça com as tools datajud
```

Combina bem com o **Legal MCP** e o **DataJud MCP** pra due diligence completa.

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**Precisa de login ou cadastro?**
Não. É grátis e funciona sem login, os dados de CNPJ são públicos da Receita Federal.

**De onde vêm os dados?**
Cadastro: base pública da Receita Federal. Processos: Diário de Justiça Eletrônico Nacional (DJEN), busca por nome.

**Acha TODOS os processos da empresa?**
A busca é por nome no DJEN (descoberta), ótima pra achar números de processo. Pra histórico completo de um processo, use o número com as tools do DataJud.

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills, tudo MIT.


---

## Suporte

- 📧 [cnpj@mcp.ai](mailto:cnpj@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/cnpj-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_cnpj` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
