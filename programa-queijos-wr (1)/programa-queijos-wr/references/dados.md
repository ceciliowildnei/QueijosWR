# Dados e persistência

## Restrição principal

Usar somente a estrutura Supabase que já existe. Não alterar tabelas, colunas, tipos, chaves ou relacionamentos sem ordem explícita do usuário. Inspecionar a implementação atual antes de escrever consultas.

## Tabelas conhecidas

- `wr_admins`
- `wr_clientes`
- `wr_produtos`
- `wr_pedidos`
- `wr_config`

Os nomes abaixo registram o modelo conhecido, mas o esquema real em uso sempre prevalece.

### `wr_admins`

`id`, `nome`, `telefone`, `pin`, `papel`, `ativo`, `criado_em`, `atualizado_em`.

### `wr_clientes`

`id`, `nome`, `telefone`, `cep`, `rua`, `numero`, `bairro`, `cidade`, `estado`, `complemento`, `observacoes`, `criado_em`, `atualizado_em`.

### `wr_produtos`

`id`, `nome`, `unidade`, `preco`, `ativo`, `criado_em`, `atualizado_em`.

### `wr_pedidos`

`id`, `codigo`, `cliente_id`, `cliente_nome`, `cliente_telefone`, `produto_id`, `produto_nome`, `quantidade`, `preco_unitario`, `total`, `tipo_entrega`, `endereco`, `forma_pagamento`, `status_pagamento`, `status_pedido`, `data_entrega`, `observacoes`, `criado_em`, `atualizado_em`.

## Produtos de referência

- Queijo 1 kg: R$ 35,00.
- Queijo 500 g: R$ 18,00.
- Leite: manter o valor cadastrado no sistema; em divulgações recentes, R$ 5,00 por litro.

Tratar todos os preços como editáveis no banco. Nunca fixá-los na regra de negócio.

## Segurança

- Não colocar credenciais administrativas ou chave de serviço no frontend.
- Não imprimir valores secretos em terminal ou resposta.
- Respeitar as políticas de acesso já configuradas.
- Não substituir a autenticação atual sem solicitação expressa.
