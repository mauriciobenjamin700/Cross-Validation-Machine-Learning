# Aprendendo Sobre Cross Validation

Cross-validation (validação cruzada) é uma técnica estatística utilizada para avaliar o desempenho de um modelo de aprendizado de máquina. Ela é especialmente útil quando se tem um conjunto de dados limitado, pois permite que o modelo seja avaliado de forma mais robusta, utilizando diferentes divisões dos dados para treinamento e teste.

## Vantagens de Usar

A utilização do CV tem altas chances de detectar se o seu modelo está sobreajustado aos seus dados de treinamento, ou seja, sofrendo overfitting

## Processo

O processo de cross-validation envolve dividir o conjunto de dados em subconjuntos (ou "folds") de tamanhos iguais ou aproximadamente iguais. Um dos subconjuntos é retido como conjunto de teste, enquanto os outros são usados para treinar o modelo. Esse processo é repetido várias vezes, de forma que cada subconjunto seja utilizado como conjunto de teste em uma iteração diferente. Ao final, os resultados são combinados para fornecer uma estimativa mais confiável do desempenho do modelo.

### K-Folds

Nesta técnica, o conjunto de dados é dividido em k subconjuntos (ou folds), e o modelo é treinado k vezes, cada vez usando um dos folds como conjunto de teste e os restantes como conjunto de treinamento. Os resultados são então combinados para calcular uma métrica de desempenho média, como acurácia ou erro médio. A Figura a baixo ilustra visualmente o processo do K-Folds, quando K = 5.

[Exemplo Visual de Como Funciona](Images/k-fold-example.png)

#### Valor de K

O valor de K deve ser escolhido cuidadosamente de forma que cada grupo de dados para treino e teste sejam grandes o suficiente para representarem estatisticamente o dataset original. É possível encontrar na literatura a orientação para a utilização de k=5 ou k=10, valores encontrados através de experimentos, mas não é uma regra formal.

Um valor de K mal escolhido pode resultar em uma interpretação errada do desempenho do seu modelo como medidas de avaliação do modelo com alta variância (as medidas podem variar bastante de acordo com os dados utilizados para treinamento).

## Referências

[Cross Validation: Avaliando seu modelo de Machine Learning](https://medium.com/@edubrazrabello/cross-validation-avaliando-seu-modelo-de-machine-learning-1fb70df15b78)
