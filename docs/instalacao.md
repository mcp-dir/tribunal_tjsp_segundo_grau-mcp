# Instalação detalhada

Tribunal TJSP: Processos do 2º Grau é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_tribunal_tjsp_segundo_grau`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_tribunal_tjsp_segundo_grau` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_tribunal_tjsp_segundo_grau` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_tribunal_tjsp_segundo_grau` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.tribunal_tjsp_segundo_grau` (ou `servers.tribunal_tjsp_segundo_grau` no VS Code) do config do cliente e reinicie.
