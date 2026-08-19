---
name: tribunal_tjsp_segundo_grau-mcp
description: Skill da REST API do Tribunal TJSP: Processos do 2º Grau na MCP.AI: 1 endpoint em /api/tribunal_tjsp_segundo_grau. Tribunal TJSP: Processos do 2º Grau, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TJSP: Processos do 2º Grau — REST API skill

Você tem acesso à **Tribunal TJSP: Processos do 2º Grau** REST API na MCP.AI.

> Tribunal TJSP: Processos do 2º Grau, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tjsp_segundo_grau
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
curl -X POST https://api.mcp.ai/api/tribunal_tjsp_segundo_grau/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tjsp_segundo_grau/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tjsp_segundo_grau_consultar`

Tribunal TJSP: Processos do 2º Grau, consulta em fonte oficial. _(POST /api/tribunal_tjsp_segundo_grau/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `numero_processo` | string | Não | Parâmetro de consulta "numero_processo". |
| `nome_parte` | string | Não | Parâmetro de consulta "nome_parte". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `rg` | string | Não | Parâmetro de consulta "rg". |
| `advogado` | string | Não | Parâmetro de consulta "advogado". |
| `oab` | string | Não | Parâmetro de consulta "oab". |
| `carta_precatoria` | string | Não | Parâmetro de consulta "carta_precatoria". |
| `documento_delegacia` | string | Não | Parâmetro de consulta "documento_delegacia". |
| `pagina` | string | Não | Parâmetro de consulta "pagina". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tjsp_segundo_grau` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
