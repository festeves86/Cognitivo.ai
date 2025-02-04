# Cognitivo.ai

a. Como foi a definição da sua estratégia de modelagem?

A estratégia de modelagem partiu de uma análise exploratoria para determinacao quais variaveis estão correlacionadas com a variavel resposta room_type. Algumas variáveis categoricas foram transformadas para poder compor o modelo.

b. Como foi definida a função de custo utilizada?

A funcao de custo utilizada foi a binary crossentropy que é suitable para problemas de classificação.

c. Qual foi o critério utilizado na seleção do modelo final?

O critério para definir o modelo foi a acurácia final da solucao (em detrimento da explicabilidade) e portanto optou-se por usar em um modelo de Deep Learning dada sua capacidade de extrair hidden patterns para determinar a variável resposta.

d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?

O criterio utilizado para validar o modelo consistiu em dividir o dataset de forma randomica de forma 80% do dataset serviu para treinar o modelo e 20% do dataset serviu para validar o modelo.

e. Quais evidências você possui de que seu modelo é suficientemente bom?

O modelo chegou a um f1-score de 100% na predição dos diferentes room_types conforme matriz de classificação abaixo.

|                | precision | recall | f1-score | support |
|----------------|-----------|--------|----------|---------|
|     Entire_Apt | 1         | 1      | 1        | 3692    |
|     Hotel_Room | 1         | 1      | 1        | 16      |
| Private_Room   | 1         | 1      | 1        | 1282    |
|  Shared_Room   | 1         | 1      | 1        | 110     |
|                |           |        |          |         |
|       accuracy |           |        | 1        | 5100    |
|      macro avg | 1         | 1      | 1        | 5100    |
| weighted avg   | 1         | 1      | 1        | 5100    |

Ainda olhando a confusion matrix verificamos que o modelo apenas se enganou 3 vezes em uma amostra de 5100

|      |    |      |     |
|------|----|------|-----|
| 3960 | 0  | 2    | 0   |
| 0    | 16 | 0    | 0   |
| 1    | 0  | 1281 | 0   |
| 0    | 0  | 0    | 110 |
