## Pandora, oportunidade ou cilada?

Pandora para mim sempre foi uma mecânica do jogo que deixei de lado, pois pelas poucas vezes que testei não compensava o tempo gasto para um retorno tão incerto, porém de tempos para cá houve um grande incentivo para minerar novamente, pois as quests diárias passaram a pagar o custo de manutenção da picareta, então o que eu levar, é lucro, livre de impostos. Agora com maior envolvimento meu nesse evento resolvi salvar os dados gerados na mineração para fazer uma análise matemática da viabilidade de se minerar em Pandora.

![img | { "type": "banner" }](public/img/banners/pandora.png)

Para esse teste usei apenas as minas de cor ciano (verde ou azul), onde o custo de mineração é duas durabilidades da picareta. Verifiquei a probabilidade de avançar em cada etapa e pela matemática você deve avançar ou parar por ali.

Vamos aos dados que coletei:

- etapa 1: {{ data.PANDORA.byLevel.[1].chance }}%
- etapa 2: {{ data.PANDORA.byLevel.[2].chance }}%
- etapa 3: {{ data.PANDORA.byLevel.[3].chance }}%
- etapa 4: {{ data.PANDORA.byLevel.[4].chance }}%
- etapa 5: {{ data.PANDORA.byLevel.[5].chance }}%
- bônus: {{ data.PANDORA.byLevel.[6].chance }}%

Como ainda não realizei testes o suficiente, vamo considerar que a chance de sucesso é sempre de 50% e o de ganhar o bônus é de 10%. Esses valores eu posso mudar depois de ter mais dados.

Para nosso cálculo queremos saber a probabilidade complementar do mesmo evento ocorrer e como aprendemos em matemática da escola, se precisamos disso "e" isso, usamos a multiplicação.

Em fração cada etapa tem 1/2 de chance de acontecer e temos que acertar 5x para ganhar o prêmio máximo. Vamos às chances de sucesso:

- etapa 1: 1/2
- etapa 2: 1/2 \* 1/2 = 1/4
- etapa 3: 1/2 _ 1/2 _ 1/2 = 1/8
- etapa 4: 1/2 _ 1/2 _ 1/2 \* 1/2 = 1/16
- etapa 5: 1/2 _ 1/2 _ 1/2 _ 1/2 _ 1/2 = 1/32

Temos a chance média de conquistar o prêmio máximo de 1 a cada 32 tentativas.

Considerando as minas de cor ciano, que têm um custo de 2 da durabilidade da picareta, dividido pela chance de sucesso, conseguimos estimar o custo médio de durabilidade para se receber a recompensa daquela etapa. Temos os seguintes custos:

- etapa 1: 2 / 1/2 = 4
- etapa 2: 2 / 1/4 = 8
- etapa 3: 2 / 1/8 = 16
- etapa 4: 2 / 1/16 = 32
- etapa 5: 2 / 1/32 = 64

O custo de reparo é de 1 [Jewel of Bless](/items/JEWEL_OF_BLESS) a cada 4 pontos de durabilidade, ou seja o custo é de 1/4. Então o custo por recompensa é de:

- etapa 1: 4 \* 1/4 = 1 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 2: 8 \* 1/4 = 2 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 3: 16 \* 1/4 = 4 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 4: 32 \* 1/4 = 8 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 5: 64 \* 1/4 = 16 [Jewel of Bless](/items/JEWEL_OF_BLESS)

E as recompensas são as seguintes:

- etapa 1: 1 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 2: 3 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 3: 7 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 4: 17 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 5: 33 [Jewel of Bless](/items/JEWEL_OF_BLESS)

Vamos subtrair a recompensa pelo custo e entender o quanto temos de vantagem ou desvantagem a cada etapa:

- etapa 1: 1 - 1 = 0 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 2: 3 - 2 = 1 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 3: 7 - 4 = 3 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 4: 17 - 8 = 9 [Jewel of Bless](/items/JEWEL_OF_BLESS)
- etapa 5: 33 - 16 = 17 [Jewel of Bless](/items/JEWEL_OF_BLESS)

Acho que ficou fácil de ver que minerar até o final é onde conseguiremos o melhor custo recompensa em Pandora e isso que não considerei o bônus aquele que não deixa mais dúvidas de que tentar ter sucesso na etapa 5 é onde conseguiremos mais lucros. Botando a chance de 10% da recompensa bônus de 100 [Jewel of Bless](/items/JEWEL_OF_BLESS), temos a média de 10 [Jewel of Bless](/items/JEWEL_OF_BLESS) de bônus, então a nossa fica:

ETAPA VENCEDORA 5

com lucro de 17 + 10(bônus) = 27 [Jewel of Bless](/items/JEWEL_OF_BLESS)

Agora só considerar o tempo que você gasta para conquistar essas 27 jóias e ver se é um negócio viável para você 😉.
