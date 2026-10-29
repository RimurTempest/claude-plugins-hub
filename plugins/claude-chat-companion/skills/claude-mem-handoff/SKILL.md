---
name: claude-mem-handoff
description: Cria resumos de continuidade e memórias portáteis quando o usuário pede para lembrar contexto, transferir um projeto entre conversas ou organizar decisões e pendências no Claude Chat.
---

# Claude-Mem — handoff manual para Chat

Este é um **fluxo alternativo**, não o software original claude-mem. Referência: https://github.com/thedotmack/claude-mem

No chat, não existem os hooks, a indexação nem o worker do plugin original. Não diga "salvei em memória" ou "vou lembrar automaticamente" se um mecanismo persistente não foi demonstrado. Não entre em APIs, contas ou repositórios sem autorização.

Quando o usuário pedir continuidade ou sumário de sessão:
1. Resuma objetivo e estado atual com dados confirmados.
2. Identifique decisões, artefatos com URLs fornecidas, bloqueios, próximos passos e instruções importantes.
3. Separe fatos de hipóteses; marque desconhecidos.
4. Minimize dados pessoais e segredos; nunca inclua tokens, cookies, senhas ou informações confidenciais de empresa.
5. Entregue um `HANDOFF.md` em Markdown para que o usuário copie ou adicione a um projeto autorizado, após revisão.

Formato sugerido:
`# Continuidade`, `## Objetivo`, `## Estado verificado`, `## Decisões`, `## Pendências`, `## Próxima ação`, `## Segurança`.

A transferência entre sessões depende do usuário anexar o handoff ou de uma integração comprovadamente conectada. Não alegue gravação automática.
