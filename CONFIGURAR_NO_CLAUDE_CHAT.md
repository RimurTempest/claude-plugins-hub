# Instrução para criar este plugin no Claude Chat

## Objetivo

Criar um plugin personalizado na conta Claude usando somente o navegador. O plugin será **Claude Chat Companion** e terá quatro skills em português para uso no Chat.

## Como usar

1. Acesse https://claude.ai e entre na sua conta pessoal.
2. Abra **Plugins** (ou **Personalizar → Plugins**, segundo a versão da interface).
3. Se existir **Adicionar → Criar com Claude**, use o texto abaixo. A criação guiada pode abrir uma sessão do Cowork na nuvem; não execute nada que instale aplicativos no computador corporativo.
4. Confirme se o Claude apresentou uma prévia com as **quatro skills**, sem hooks, scripts ou servidores MCP.
5. Salve somente depois de revisar conteúdo e permissões. Se a opção de criação não existir no seu plano, interrompa e registre o bloqueio; não substitua por execução de terminal.

## Prompt pronto para colar no Claude

> Crie um único plugin personalizado para a minha conta Claude, chamado `claude-chat-companion`, contendo exatamente quatro skills compatíveis com o **Chat na web**. Use **apenas documentos Markdown e o manifesto JSON de plugin**, sem hooks, servidores MCP, subagentes, scripts, instalação local, serviços em segundo plano, chamadas pagas ou alterações de configuração do navegador. O conteúdo já foi escrito e publicado neste repositório público:
>
> https://github.com/RimurTempest/claude-plugins-hub/tree/main/plugins/claude-chat-companion
>
> Consulte cada SKILL.md e preserve seu conteúdo essencial e restrições:
>
> 1. https://github.com/RimurTempest/claude-plugins-hub/blob/main/plugins/claude-chat-companion/skills/omniroute-web-guide/SKILL.md
> 2. https://github.com/RimurTempest/claude-plugins-hub/blob/main/plugins/claude-chat-companion/skills/claude-mem-handoff/SKILL.md
> 3. https://github.com/RimurTempest/claude-plugins-hub/blob/main/plugins/claude-chat-companion/skills/headroom-context/SKILL.md
> 4. https://github.com/RimurTempest/claude-plugins-hub/blob/main/plugins/claude-chat-companion/skills/task-observer-web/SKILL.md
>
> Mostre-me a prévia dos arquivos e peça minha aprovação antes de salvar. Estas skills são adaptações de fluxos para o chat, não são os produtos originais. Não alegue que memória persistente automática, proxy de compressão, roteamento OmniRoute ou log automático de observações foram ativados. Se não conseguir abrir as fontes, informe e não invente seu conteúdo. Preserve as atribuições aos autores originais. Não acesse dados corporativos nem peça tokens/senhas. Não faça downloads ou instalações no computador corporativo.

## Testes depois de salvar

- `/claude-mem-handoff`: solicitar handoff de uma conversa fictícia; saída apenas textual.
- `/headroom-context`: pedir briefing compacto de 10 linhas; verificar se não promete reduzir tokens automaticamente.
- `/task-observer-web`: pedir observações sobre uma tarefa simulada; verificar se exige revisão humana.
- `/omniroute-web-guide`: perguntar se uma skill altera o endpoint do Claude Chat; a resposta correta é **não**.

O nome exato das skills no menu pode depender da versão da interface; se não forem listadas, use `+` ou `/` e procure pelos nomes.

**Estado:** conteúdo publicado no GitHub; importação na conta Claude ainda não comprovada.
