# airport-system
System Airport

docker-compose --env-file server/.env  up -d
# docker compose up -d  - Inicia todos em modo background (-d)
# docker compose down - Deleta / Apaga os containers e seus dados
# docker compose stop - Para os containers

Regras do Negócio:
● Cada voo tem um aeroporto de origem e uma de destino, uma
numeração única, data e hora de partida.
● O voo não pode ter como origem e destino o mesmo aeroporto, e esses
aeroportos não podem estar situados na mesma cidade.
● Os voos devem possuir no mínimo uma classe, contendo um tipo de
classe, a quantidade de assentos, e o valor para cada assento.
● A quantidade de passagens para um voo é limitada pela quantidade de
assentos disponíveis em cada classe. E não deve haver duas ou mais
classes do mesmo tipo no mesmo voo.
● Os aeroportos ficam situados nas cidades, e cada um possui um nome e
o próprio código aeroportuário IATA que é único.
● As cidades devem possuir nome e a unidade federativa.
● As passagens aéreas representam um assento da classe escolhida. Uma
passagem contém um número de identificação único para controle
interno, os dados do passageiro (nome, cpf, data de nascimento), o preço
total da passagem, e a classe. Não podem ser vendidas mais passagens
do que a capacidade máxima da classe.
● É possível pesquisar por passagens informando os aeroportos de origem
e destino, e a data que deseja. Opcionalmente podem ser filtrados por
valores. O resultado não pode mostrar voos sem assentos disponíveis. E
não podem ser apresentados voos passados.
● As passagens devem ser vinculadas ao visitante que as comprou,
identificando ele com o nome, cpf, data de nascimento e e-mail.
● Cada passagem permite no máximo uma bagagem, e se houver
despache deve ser acrescida uma taxa de 10% do valor do assento ao
valor da passagem. As bagagens possuem uma numeração única para
controle interno.
● Durante a compra, o visitante deverá informar os dados do comprador, a
quantidade de passagens, a classe escolhida, e a lista com os dados de
cada passageiro e se há bagagem a ser despachada.
● Depois de compradas as passagens, é possível emitir os vouchers de
cada uma contendo o número da passagem, número do voo, origem e
destino, e o passageiro, além de indicar se há despacho de bagagem.
● Caso haja despacho de bagagem, é possível emitir também a etiqueta
da bagagem com os números de identificação da passagem e da
bagagem, e o nome do passageiro.
● O limite de tempo para emissão tanto da etiqueta quanto do voucher é
de no máximo 5 horas antes do voo.
