---
name: omniroute-setup
description: Guia para verificar a viabilidade de conectar Claude Code a um gateway OmniRoute remoto. Não configura o Claude na web nem executa servidores automaticamente. Use somente quando o usuário pedir configuração ou diagnóstico de OmniRoute.
---

# OmniRoute: configuração supervisionada

Fonte principal: https://github.com/diegosouzapw/OmniRoute
Guia Claude Code: https://github.com/diegosouzapw/OmniRoute/wiki/Claude-Code-Configuration

## Limites desta skill

Esta skill é **apenas documentação operacional**. Não inclui binários, não instala OmniRoute, não inicia um gateway, não troca o modelo do Claude e não configura faturamento. Ter esta skill carregada **não é** ter OmniRoute funcionando.

## Diagnóstico inicial

1. Identifique a superfície: Claude.ai Chat, Claude Code na web, Claude Code em terminal local ou terminal em servidor pessoal.
2. Se for Claude.ai Chat ou Claude Code na web, explique que um arquivo de marketplace, por si só, não altera o endpoint dos modelos hospedados pela Anthropic; não prometa roteamento de outros modelos.
3. Se for Claude Code CLI controlado pelo usuário e já existir gateway remoto autorizado, siga a documentação oficial atualizada para apontar o CLI ao gateway, com as variáveis adequadas. Nunca pressupor que um gateway existe.
4. Se ainda não houver gateway, deixe como pendente e não instale nada no equipamento corporativo.
5. Não peça tokens, senhas ou chaves no chat. Não escreva credenciais em repositório, logs, exemplos versionados ou arquivos públicos. Use armazenamento secreto apropriado no ambiente de execução autorizado.
6. Não habilite fallback remoto pago sem autorização explícita e verificação de preço, privacidade e orçamento.
7. Antes de ações que alterem serviços, peça a aprovação aplicável. Preserve configuração e branches já existentes.

## Entrega de diagnóstico

Informe separadamente: (a) preparação do marketplace, (b) instalação da skill, (c) existência do gateway, (d) conectividade, (e) roteamento efetivo e (f) custos/privacidade. Marque como não verificado o que ainda não foi testado.

Nunca represente uma instrução em Markdown como serviço em execução.
