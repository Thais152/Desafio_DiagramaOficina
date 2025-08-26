# Desafio diagrama da Oficina | Treinamento DIO

O diagrama tem como contexto uma oficina mecânica, na qual o cliente realiza um pedido de revisão periódica ou conserto de algum veículo. A equipe responsável análisa o pedido e cria uma ordem de serviço, contando com o preço das peças e de todos os serviços ofertados. A partir disso, e a autorização do cliente, a equipe responsável pode dar continuidade ao serviço.

As entidades desse diagrama são: Mecânico, equipe responsável, cliente, pedido, ordem de serviço, peças e serviços.

## 📜📜📜 Explicando o diagrama (Suas entidades e relacionamentos)
- ### Mecânico e Equipe responsável: 
Cada mecânico faz parte de uma equipe responsável em um relacionamento de (1:n). Um ou mais mecânicos compôem uma equipe e uma equipe é composta por um ou mais mecânicos. Então, neste caso, um mecânico não pode fazer parte de duas equipes distinstas. 
- ### Ordem de serviço, serviços, peças: 
A partir da geração da ordem de serviço, também há a indicação do valor a ser pago pelo cliente. Para gerar esse valor, é feito soma do valor de cada serviço prestado e de cada peça usada no conserto ou revisão. Portanto, existe um relacionamento entre a ordem de serviço e as entidades serviços e peças de (N:M). Uma ou mais peças estão contidas na ordem e um ou mais serviços irão compor a ordem.
- ### Cliente e pedido: 
Cada cliente poderá fazer um ou mais pedidos, porém um pedido poderá ser feito apenas por um cliente, se tornando uma relação de (1:n). E o pedido terá como atributo "Tipo de pedido", esclarecendo se é uma revisão ou conserto. E, claro, o atributo booleano "Liberado", que contém a informação de autorização do cliente após a ordem de serviço ser criada, a partir da analise da equipe responsável explicada no próximo tópico. 
- ### Equipe responsável e pedido:
Após o pedido ser feito pelo cliente, ele será analisado pela equipe responsável, em uma relação de (1:n). Uma equipe está responsável por um ou mais pedidos, mas um pedido será analisado por apenas uma equipe.
- ### Ordem de serviço e pedido:
A partir da análise feita, a equipe gera uma ou mais ordens de serviços relacionadas a um pedido, sendo uma relação de (1:n). Um pedido pode gerar um ou mais ordens, mas uma ordem está relacionada a um único pedido.
