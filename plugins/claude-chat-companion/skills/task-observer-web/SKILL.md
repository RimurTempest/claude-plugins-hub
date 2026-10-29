---
name: task-observer-web
description: Revisa sessões de trabalho, observando correções, retrabalho e padrões que poderiam virar skills ou melhorar fluxos. Funciona no Claude Chat com relatório de handoff manual.
---

# Task Observer — revisão humana e handoff

Adaptação leve **para o navegador**, baseada no propósito do projeto "One Skill to Rule Them All" de Eoghan Henn / Rebelytics (CC BY 4.0): https://github.com/rebelytics/one-skill-to-rule-them-all

Não substitui o pacote original, seu protocolo completo de início de sessão ou scripts de observação. Em Claude Chat não há gravação automática dos arquivos de observações no sistema de arquivos. Utilize, quando pertinente, uma análise da conversa disponível.

Ao final de tarefas extensas ou quando solicitado:
1. Identifique situações observáveis: erro ou correção recorrente, decisão reutilizável, procedimento que funcionou.
2. Para cada item, detalhe **evidência da conversa**, **impacto**, **sugestão** e **nível de confiança**.
3. Diferencie conhecimento confirmado de interpretações.
4. Proponha mudanças em skills/instruções com revisão e autorização do usuário antes de aplicar.
5. Produza `RELATORIO_OBSERVACOES.md` para transferência manual; não diga que foi persistido automaticamente.
6. Não reproduza dados sensíveis, conteúdo corporativo restrito ou segredos; não instrua publicar sessões privadas em repositório público.

Handoff sugerido: `Contexto` → `Observações` → `Melhorias sugeridas` → `Aprovação necessária` → `Próxima sessão`.
