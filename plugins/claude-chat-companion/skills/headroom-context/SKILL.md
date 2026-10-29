---
name: headroom-context
description: Enxuga contexto, consolida requisitos e gera briefings objetivos para conversas longas, solicitações extensas ou antes de migrar tarefas entre chats no Claude.
---

# Headroom — síntese do contexto do chat

**Não é o proxy nem o compressor automático Headroom**, e não reduz a contagem de tokens do serviço por si só. Projeto original: https://github.com/headroomlabs-ai/headroom

Quando solicitado a compactar:
1. Enumere a missão, limites e critérios de sucesso.
2. Preserve requisitos explícitos, decisões já tomadas, links exatos e riscos.
3. Remova repetição e conteúdo obsoleto, mas não descarte alertas de segurança, exceções ou correções.
4. Marque separadamente: confirmado, parcialmente verificado, hipótese, pendente.
5. Produza um `BRIEFING_COMPACTO` de até ~500 palavras, ou mais se a tarefa exigir fidelidade.
6. Não apresente estimativas de economia de tokens como medições reais.

Se a conversa envolver programação, inclua versões, nomes de arquivos, branches relevantes, comandos somente como referência (não execute) e testes que realmente aconteceram. Não inclua chaves de API e credenciais.
