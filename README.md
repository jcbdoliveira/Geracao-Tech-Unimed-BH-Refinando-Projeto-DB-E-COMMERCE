# Refinando um Projeto Conceitual de Banco de Dados – E-COMMERCE

O esquema deverá ser adicionado a um repositório do Github para futura avaliação do desafio de projeto. Adicione ao Readme a descrição do projeto conceitual para fornecer o contexto sobre seu esquema.

# Objetivo:
Refine o modelo apresentado acrescentando os seguintes pontos:

    1. Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
    2. Pagamento – Pode ter cadastrado mais de uma forma de pagamento; 
    3. Entrega – Possui status e código de rastreio;

# Resolução proposta

Para o item 1 **Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações** modelei duas entidades chamadas **Pessoa Fisica** e **Pessoa Juridica** uma para cada tipo de pessoa. Estas estidades são especializações da entidade **Cliente**

Para o item 2 **Pagamento – Pode ter cadastrado mais de uma forma de pagamento**. Foi modelado uma entidade chamada **Meios de pagamento** que representa um relacionamento de muitos para muitos entre o cliente e as diversas formas de pagamento que ele possa ter. Em nosso mini-mundo modelo duas formas de pagamento **Cartão de credito/debito** e **PIX**.
Também modelamos uma entidade chamada **Pagamento** que mapeia o uso do meio de pagamento no pedido. Imaginei que o pedido pode ter mais de uma forma de pagamento, dois cartões por exemplo.

No item 3. **Entrega – Possui status e código de rastreio** adicionei um atributo na entidade **Produtos por pedido** chamado Codigo de rastreio. Fiz isto imaginando que poderia comprar produtos que serão entregues separadamente.
Outra solução foi implementar a entidade **Status do pedido** para registrar as movimentações da entrega e gerar histórico.
