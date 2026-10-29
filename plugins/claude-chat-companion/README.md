# Claude Chat Companion — edição navegador

Plugin personalizado com **quatro skills em português**, criado para o **Claude Chat (claude.ai)**, sem hooks, executáveis, scripts, subagentes ou servidores MCP. Preparado para instalações via arquivo de plugin personalizado quando permitido pela conta do usuário.

## Recursos disponíveis

| Skill (caminho) | Entrega no Chat | Não faz |
|---|---|---|
| `omniroute-web-guide` | Diagnóstico do roteamento e caminhos remotos autorizados | Trocar modelo, operar OmniRoute ou interceptar sessão |
| `claude-mem-handoff` | `HANDOFF.md` de continuidade | Gravar memória automaticamente ou iniciar worker |
| `headroom-context` | `BRIEFING_COMPACTO` para copiar para outra sessão | Ativar proxy, medir ou reduzir automaticamente tokens |
| `task-observer-web` | `RELATORIO_OBSERVACOES.md` com revisão humana | Persistir logs ou operar scripts no navegador |

## Origem, autoria e escopo

Trata-se de uma **adaptação independente**, não uma distribuição dos quatro produtos originais. O pacote usa apenas novos documentos Markdown e um manifesto JSON. Não configura um roteador ativo nem uma memória persistente automática.

- [OmniRoute — projeto de diegosouzapw](https://github.com/diegosouzapw/OmniRoute)
- [Claude-Mem — projeto de thedotmack](https://github.com/thedotmack/claude-mem)
- [Headroom — projeto de headroomlabs-ai](https://github.com/headroomlabs-ai/headroom)
- [Task Observer / One Skill to Rule Them All — Rebelytics](https://github.com/rebelytics/one-skill-to-rule-them-all) (CC BY 4.0; inspiração metodológica com crédito; *não* inclui o bundle oficial)

Para usar o **Task Observer original**, a documentação do autor recomenda importar o pacote completo `.skill`; no Claude Chat, o modo suportado é por documento de handoff, sem log persistente automático.

## Instalação via Claude Chat (plano pago e função liberada)

1. Na conta Claude, abra **Plugins** na barra lateral (ou **Personalizar → Plugins**, conforme o estágio da atualização do menu).
2. Procure a opção de **adicionar/importar plugin personalizado**. A Anthropic documenta envio de arquivos de plugin personalizados pelo navegador.
3. É necessário disponibilizar um pacote `.plugin` / ZIP com o **conteúdo desta pasta como raiz**. O **repositório GitHub sozinho** e o `marketplace.json` do Claude Code não garantem instalação direta na conta pessoal.
4. Após a importação, confira se aparecem as quatro skills, e teste com "Crie um briefing compacto desta conversa".
5. Não ative conectores, serviços ou compartilhamento de dados não autorizados.

Este projeto está **preparado no GitHub**, mas a instalação final deve ser confirmada na conta Claude — ela não é concluída pelo simples commit.

## Segurança e restrições

Sem instalação local; sem chaves; sem cookies, tokens, senhas, dados corporativos ou acesso a infraestrutura. Os documentos gerados para continuidade devem ser revisados antes de enviar a serviços externos.

## Estrutura

```text
.claude-plugin/plugin.json
skills/
  omniroute-web-guide/SKILL.md
  claude-mem-handoff/SKILL.md
  headroom-context/SKILL.md
  task-observer-web/SKILL.md
```
