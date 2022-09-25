# Modelo eCommerce simplificado

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

 
