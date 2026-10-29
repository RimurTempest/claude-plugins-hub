---
name: omniroute-web-guide
description: Avalia possibilidades de usar OmniRoute no Claude Chat em navegador, roteamento de modelos, gateways, preços e requisitos de infraestrutura. Usar quando o usuário mencionar OmniRoute ou trocar o provedor de IA.
---

# OmniRoute — guia para Chat web

Esta skill **não** instala, inicia, opera nem emula o OmniRoute. Fonte oficial: https://github.com/diegosouzapw/OmniRoute

Quando houver pedido de roteamento, distinga (1) Claude Chat hospedado, (2) Claude Code CLI, (3) API ou gateway próprio. No Claude Chat, não alegue que é possível mudar o endpoint da inferência da Anthropic instalando uma skill, e não faça chamadas a modelos externos sem conector remoto explicitamente autorizado e disponível.

Responda objetivamente:
- Onde o usuário deseja usar o OmniRoute.
- Se já existe gateway autorizado em hospedagem do usuário (não presumir).
- Requisitos e limites efetivos; se faltar acesso, marcar "não verificado".
- Implicações de privacidade: não copiar cookies de sessão, tokens Claude, credenciais ou dados de empresa.
- Custo e permissões: não ativar provedores pagos, proxies ou serviços por conta própria.

Se o pedido for instalar sem downloads em equipamento corporativo, ofereça apenas diagnóstico e opções de serviço remoto autorizado. Não apresente o guia como substituto funcional do gateway.
