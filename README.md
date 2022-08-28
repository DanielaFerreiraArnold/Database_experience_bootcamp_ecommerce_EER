# eCommerce_dio.com

Digital Innovation One 
Bootcamp: DATABASE EXPERIENCE

Primeiro desafio de projeto: Refinando um Projeto Conceitual de Banco de Dados.

Criar um modelo iniciando um projeto de Banco de Dados, modelando por Entidade Relacionamento (Enhanced Entity Relationship).


NARRATIVA

Produto
* Os produtos são vendidos por uma única plataforma online. Contudo, estes podem ter vendedores distintos (terceiros).
* Cada pordutos possui um fornecedor.
* Um ou mais produtos podem compor um pedido.

Cliente
* O cliente pode se cadastrar no site com seu CPF ou CNPJ.
* O endereço do cliente irá determinar o valor do frete.
* Um cliente pode comprar mais de um pedido. Este tem um período de carência para devolução do produto.

Pedido
* Os pedidos são criados por clientes e possuem informações de compra, endereço e status da entrega.
* Um produto ou mais compõem o pedido.
* O pedido pode ser cancelado.

Fornecedor 
* Um fornecedor pode fornecer um ou mais produtos e um produto pode ser disponibilizado por um ou mais fornecedores.
* Um terceiro fornecedor pode vender seus produtos na plataforma. Podem haver vários terceiros vendendo seus produtos.

Estoque
* O produto deve constar em estoque e deve ser possível consultar o estoque.
* O produto pode estar em um determinado estoque. Pode haver mais de um local de estoque.
* Pode haver mais de um produto em estoque e pode haver mais estoque com mais de um produto. 

Este contexto reduzido de e-commerce foi modelado juntamento com as aulas. O objetivo do desafio foi refinar
o modelo apresentado em curso, acrescentando os seguintes pontos:

1. Cliente PJ e PF - Uma pessoa pode ser PJ ou PF, mas não pode ter as duas informações;
2. Pagamento - Pode ter cadastrado mais de uma forma de pagamento;
3. Entrega - Possui status e código de rastreio.

  Para o primeiro ponto, foi feita uma especialização da entidade cliente, sendo criadas duas novas entidades (Cliente_J e Cliente_PF), as quais herdam 
as informações do da entidade Cliente, para não haver repetição de informações como: nome e endereço.

  Para o segundo caso, pagamento, foi criada uma entidade "Formas_pagamento", contendo as seguintes opções de pagamento:
Pix, boleto e cartão de crédito. Para cartão de crédito, foi criada uma entidade separada, pois esta forma de pagamento possui informações
específicas. Caso essa forma for selecioanda, a entidade "Formas_pagamento" irá obter as imormações que foram herdadas. 
Foi criada uma outra entidade, Pedido_has_Formas_pagamento, pois um pedido pode ser pago com mais de uma forma de pagamento, 
o qual o cliente pode selecionar no fechamento do pedido. Além disso, uma fomra de pagamento não é exclusiva de somente um pedido, 
por isso existe um relacionamento de N:M.

  Sobre a Entrega, decidi criar uma entidade especializada, a qual é herdada por Pedido, uma vez que o peido é feito.
Essa entidade contém informações como: confirmação do pedido, data de envio, previsão de entrega, código de rastreamento e transportadora responsável.

  Dentro de pedido, foi acrescentado o atributo "Cancelamento/devolução/troca". Por meio deste atributo, 
o cliente poderá consultar politicas de cancelamento, devolução e troca e entrar em contato com o vendedor para fazer sua solicitação. 
Isso será fetio por meio de código, sem necessidade de criar uma outra endidade. 
