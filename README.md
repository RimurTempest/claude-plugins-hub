# Claude Plugins Hub

Catálogo pessoal do GitHub **RimurTempest** para **OmniRoute**, **claude-mem**, **Headroom** e **Task Observer**, com foco em preparação **100% pela nuvem**, sem downloads ou instalações no computador corporativo.

**Situação atual:** o catálogo está preparado no GitHub; **nenhum plugin foi instalado ou ativado na conta Claude** e **nenhum servidor OmniRoute foi iniciado**.

## Conteúdo

| Componente | Origem | Disponível no catálogo | O que realmente instala |
|---|---|---|---|
| **claude-mem** | [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem) | `claude-mem` | Plugin original de Claude Code, com hooks e serviço de memória; exige runtime e configuração |
| **Headroom** | [headroomlabs-ai/headroom](https://github.com/headroomlabs-ai/headroom) | `headroom` | Plugin oficial de hooks; compressão depende do runtime/proxy adequado |
| **Task Observer** | [rebelytics/one-skill-to-rule-them-all](https://github.com/rebelytics/one-skill-to-rule-them-all) | `task-observer` | Plugin/skill original; análise de trabalho e propostas para aprovação |
| **OmniRoute** | [diegosouzapw/OmniRoute](https://github.com/diegosouzapw/OmniRoute) | `omniroute-setup` | **Só um guia** de integração; **não** instala nem executa o gateway |

O manifesto do catálogo está em [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json). Os plugins externos são referenciados diretamente nos repositórios originais: **não** foram copiados, alterados ou incorporados ao código deste projeto.

## Usar no Claude sem instalar no computador corporativo

### Claude.ai Chat pelo navegador

No Claude, **Personalizar → Plugins** permite adicionar plugins compatíveis e importar pacotes personalizados, conforme as opções disponíveis em sua conta e plano. Entretanto, **adicionar este repositório como contexto ou URL não equivale a instalar os plugins do catálogo**. O catálogo `marketplace.json` se destina ao gerenciador de plugins do **Claude Code**, e não executa hooks nem serviços no chat web.

O **Task Observer** oferece um modo específico para chat web: um documento de *handoff* ao fim da sessão. O autor orienta a instalar o pacote `.skill` completo pelas configurações do Claude. Esse fluxo pode exigir transferir o pacote — não foi executado neste projeto.

### Claude Code no navegador (`claude.ai/code`)

Conecte sua conta GitHub e selecione um repositório para trabalhar na nuvem. O Claude Code na web pode consultar os arquivos e instruções do projeto, mas **não disponibiliza o comando interativo `/plugin`**; por isso, registrar este marketplace não é uma etapa realizável por esse comando na interface web. Em especial, arquivos estáticos **não** permitem redirecionar a inferência hospedada do Claude por OmniRoute.

### Claude Code em terminal autorizado (outro ambiente, não o computador corporativo)

Se no futuro houver um ambiente pessoal/remoto autorizado com Claude Code CLI e suporte a plugins, os comandos para registrar o marketplace e selecionar os plugins serão:

```text
/plugin marketplace add RimurTempest/claude-plugins-hub
/plugin install claude-mem@rimurtempest-plugins-hub
/plugin install headroom@rimurtempest-plugins-hub
/plugin install task-observer@rimurtempest-plugins-hub
/plugin install omniroute-setup@rimurtempest-plugins-hub
```

**Não execute esses comandos no computador corporativo.** Os dois primeiros podem instalar dependências ou iniciar processos no ambiente onde forem usados; o OmniRoute real é um gateway à parte. Além disso, plugins com hooks, serviços locais ou comunicação externa devem ser revisados antes de serem autorizados. O claude-mem pode processar e armazenar histórico de sessões; confira políticas e custos do fornecedor antes da ativação.

## Restrições de segurança e custos

- Nenhum token, senha, cookie, credencial, dado da empresa ou arquivo corporativo deve ser publicado neste repositório.
- Não vincule serviços privados da empresa nem conceda permissões corporativas sem autorização do responsável.
- Não instale binários, runtimes, agentes, extensões, serviços ou proxies no computador corporativo.
- Não assuma que plugins, gateways, proxies ou provedores de IA são gratuitos. Verifique as condições e peça autorização antes de qualquer serviço pago.
- Este repositório **não** altera os projetos J.A.R.V.I.S. nem faz alterações automáticas em produção.

## Como validar futuramente

1. Verificar o JSON e a correspondência entre nomes e fontes do marketplace.
2. Num ambiente pessoal/autorizado com CLI, executar `claude plugin validate` para obter a validação oficial.
3. Instalar cada plugin individualmente; revisar permissões, hooks, conexões externas e custos.
4. Confirmar a operação real de cada serviço com um teste específico, sem credenciais públicas.

### Referências

- [Formato oficial de marketplaces do Claude Code](https://code.claude.com/docs/en/plugin-marketplaces)
- [Referência de marketplace](https://code.claude.com/docs/en/plugins/marketplace-reference)
- [Plugins no Claude (web e desktop)](https://support.claude.com/pt/articles/13837440-usar-plugins-no-claude)
- [OmniRoute no Claude Code](https://github.com/diegosouzapw/OmniRoute/wiki/Claude-Code-Configuration)
- [Task Observer — instruções do autor](https://github.com/rebelytics/one-skill-to-rule-them-all#quick-install)

**Propriedade:** catálogo pessoal de RimurTempest. Os projetos listados pertencem aos seus respectivos autores e mantêm suas licenças originais.
