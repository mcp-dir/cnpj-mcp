# Ferramentas

CNPJ expõe 2 ferramentas (todas somente leitura).

### 1. `cnpj_consultar`
**Input**: `cnpj`

Consulta cadastral de um CNPJ (grátis): razão social, nome fantasia, situação cadastral, CNAE principal, porte, município/UF e SÓCIOS (QSA). Útil pra identificar a empresa e seus sócios antes de buscar processos.

### 2. `cnpj_processos`
**Input**: `cnpj`, `incluir_socios` (opcional)

DESCOBERTA por CNPJ: resolve o CNPJ em razão social (e sócios) e busca os processos por NOME no Diário (DJEN) — grátis, com número de processo completo. Opcionalmente inclui os processos dos sócios. Com os números, enriqueça com as tools datajud.

## Prompts de exemplo

```
Consulte o CNPJ 33.000.167/0001-01 e liste os sócios
Quais processos da empresa do CNPJ 33.000.167/0001-01?
Inclua também os processos dos sócios
Qual a situação cadastral e o CNAE principal desse CNPJ?
```
