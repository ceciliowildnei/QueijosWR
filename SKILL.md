---
name: programa-queijos-wr
description: Criar, reconstruir, corrigir, testar e evoluir o sistema web “Queijos WR Pedidos”, incluindo identidade visual, login, administradores, clientes, produtos, pedidos, entregas, pagamentos, dashboard, relatórios, WhatsApp e reservas. Usar quando o usuário mencionar Programa Queijos WR, Queijos WR Pedidos, sistema de queijo e leite, ou pedir alterações no projeto ceciliowildnei/queijo-leite-pedidos. Preservar o Supabase existente e nunca alterar tabelas ou relacionamentos sem instrução explícita.
---

# Programa Queijos WR

## Objetivo

Construir e manter um único sistema online, simples e responsivo para registrar e acompanhar vendas de queijo e leite em tempo real no computador e no celular.

## Antes de agir

1. Ler [references/projeto.md](references/projeto.md) para requisitos, visual e fluxos.
2. Ler [references/dados.md](references/dados.md) antes de tocar em persistência, autenticação, produtos, clientes ou pedidos.
3. Inspecionar o projeto e as integrações disponíveis antes de propor alterações.
4. Tratar o sistema e o banco atuais como fonte da verdade. Não misturar projetos antigos.

## Regras obrigatórias

- Manter 100% do Supabase existente, incluindo tabelas, colunas e relacionamentos.
- Não criar migrations, tabelas ou relacionamentos sem pedido explícito do usuário.
- Salvar e ler dados reais no Supabase; não usar `localStorage` ou um JSON `app_state` como banco principal.
- Usar apenas um repositório e um endereço final de produção.
- Preservar a identidade Queijos WR e usar o arquivo de logo existente quando disponível.
- Manter preços editáveis no cadastro de produtos; valores iniciais são dados de referência, não constantes no código.
- Pedir ação manual somente quando a ferramenta realmente não puder executá-la.
- Não expor PINs, chaves, tokens ou variáveis secretas em respostas, logs, commits ou código cliente.

## Fluxo de execução

1. Identificar se a solicitação é criação, correção, atualização visual, dado, teste ou publicação.
2. Examinar os arquivos e o estado atual antes de editar.
3. Fazer a menor alteração completa que atenda ao pedido.
4. Validar build, lint ou testes disponíveis.
5. Quando houver interface executável, testar o fluxo afetado no navegador e em largura móvel.
6. Para mudanças de dados, confirmar que a aplicação continua lendo e gravando no Supabase existente.
7. Para publicação, verificar o endereço de produção e os fluxos essenciais.
8. Informar de modo direto o que foi feito, os arquivos alterados, o que foi testado e o único endereço que deve ser usado.

## Critérios de conclusão

- Login funciona com telefone e PIN.
- Dados cadastrados em um dispositivo ficam disponíveis em outro.
- Cliente, produto e pedido persistem no Supabase.
- Totais, status do pedido e status do pagamento são coerentes.
- Layout funciona no computador e no celular.
- Nenhuma tabela ou relação existente foi alterada inadvertidamente.
