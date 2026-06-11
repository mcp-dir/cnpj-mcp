---
name: cnpj-mcp
description: Consulta cadastral de CNPJ (razão social, situação, CNAE, sócios) e descoberta de processos judiciais da empresa e dos sócios via DJEN. Use sempre que o usuário mencionar um CNPJ, pedir dados de uma empresa, sócios, situação cadastral, ou processos de uma empresa. Grátis, sem login. Orquestra cnpj_consultar e cnpj_processos do servidor remoto em https://api.mcp.ai/p_cnpj.
---

# CNPJ — REST API skill

Você tem acesso à **CNPJ** REST API na MCP.AI.

> Consulta cadastral pública de CNPJ (razão social, nome fantasia, situação, CNAE, porte e sócios) e descoberta dos processos da empresa e dos sócios no Diário de Justiça (DJEN). Dados públicos da Receita Federal, grátis, sem login.

## Base URL

```
https://api.mcp.ai/api/cnpj
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/cnpj/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"cnpj":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/cnpj/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (2)

#### `cnpj_consultar`

Consulta cadastral de um CNPJ (grátis): razão social, nome fantasia, situação cadastral, CNAE principal, porte, município/UF e SÓCIOS (QSA). Útil pra identificar a empresa e seus sócios antes de busca _(POST /api/cnpj/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Sim | CNPJ (14 dígitos), com ou sem máscara. |

#### `cnpj_processos`

DESCOBERTA por CNPJ: resolve o CNPJ em razão social (e sócios) e busca os processos por NOME no Diário (DJEN) — grátis, com número de processo completo. Opcionalmente inclui os processos dos sócios. C _(POST /api/cnpj/processos)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Sim | CNPJ (14 dígitos), com ou sem máscara. |
| `incluir_socios` | boolean | Não | Se true, também busca os processos de cada sócio (QSA). Default false. |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_cnpj` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
