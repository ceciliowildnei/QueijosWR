# Projeto Queijos WR Pedidos

## Identidade

- Nome: **Queijos WR Pedidos**.
- Lema: **Tradição que vem da nossa família para a sua.**
- Aparência: artesanal e rural, acolhedora, limpa e fácil de usar.
- Paleta: marrom, bege, dourado, amarelo-claro e verde-escuro.
- Logo preferencial: `public/logo-queijos-wr.png`, PNG transparente de alta resolução.
- Exibir o logo no login e no topo; usar `object-fit: contain` para não deformar.

## Arquitetura conhecida

- Aplicação web responsiva em React + Vite.
- Supabase como banco real compartilhado.
- Variáveis: `VITE_SUPABASE_URL` e `VITE_SUPABASE_ANON_KEY`.
- Projeto conhecido: `ceciliowildnei/queijo-leite-pedidos`.
- Preservar o projeto e a base já existentes; não recriar o banco nem misturar implementações antigas.

## Navegação e módulos

- Login por telefone e PIN.
- Dashboard.
- Clientes.
- Produtos.
- Pedidos.
- Pedidos da próxima sexta-feira.
- Entregas.
- Relatórios.
- Administradores.
- Disparo por WhatsApp.
- Link de reserva.

## Fluxos principais

### Cliente

Cadastrar nome, WhatsApp, CEP, rua, número, bairro, cidade, estado, complemento e observações. Integrar busca de CEP via ViaCEP. Permitir localizar cliente por nome ou telefone ao criar pedido.

### Pedido

Selecionar cliente e produto, informar quantidade, preço unitário, entrega, pagamento, data e observações. Calcular total. Permitir acompanhar status do pedido e do pagamento.

### Operação

- Destacar encomendas da próxima sexta-feira.
- Permitir atualização/sincronização dos dados.
- Exibir aviso simples de novo pedido quando o navegador permitir.
- Compartilhar pedidos em tempo real entre celular e computador.
- Gerar visualização adequada para comprovantes e relatórios quando solicitado.

## Diretrizes de experiência

- Priorizar botões grandes, formulários objetivos e textos em português do Brasil.
- Evitar telas densas e opções técnicas para o usuário final.
- Mostrar estados de carregamento, vazio, sucesso e erro.
- Confirmar ações importantes sem criar etapas desnecessárias.

