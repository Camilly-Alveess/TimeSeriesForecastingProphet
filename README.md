# Previsão de Séries Temporais com Prophet

## Visão Geral
Este repositório contém uma análise abrangente de previsão de séries temporais usando o modelo Prophet, desenvolvido pelo Facebook. O projeto inclui o desenvolvimento e avaliação de múltiplos modelos de previsão para identificar a melhor abordagem na previsão de valores futuros com base em dados históricos.

## Objetivos
1. Desenvolver modelos de previsão adicionais (m0 a m7) com hiperparâmetros diferentes dos abordados no curso original.
2. Compilar os resultados em um DataFrame de validação para comparar os modelos m0 a m7.
3. Plotar as métricas de validação cruzada para todos os modelos em um único gráfico para avaliação visual do desempenho.
4. Determinar e justificar o melhor modelo com base nas métricas de avaliação.

## Modelos Desenvolvidos
- **m0**: Modelo base com parâmetros padrão.
- **m1**: Ajustado para detecção de changepoints com maior flexibilidade.
- **m2**: Modificou sazonalidades e configurações de changepoints para melhor precisão.
- **m3**: Changepoints personalizados integrados ao modelo.
- **m4**: Changepoints adicionais incluídos para capturar tendências.
- **m5**: Introduzidas sazonalidades personalizadas e diferentes configurações de changepoints.
- **m6**: Ajuste na `changepoint_prior_scale` para flexibilidade nas mudanças de tendência.
- **m7**: Efeitos de feriados incluídos com penalização menor para melhores previsões em feriados.

## Resultados
O desempenho dos modelos foi avaliado usando o Erro Quadrático Médio (MSE) e seu desvio padrão. O DataFrame de validação contém as seguintes métricas:

| Modelo | MSE       | MSE Std   |
|--------|-----------|-----------|
| m0     | 22.119038 | 4.703088  |
| m1     | 12.838094 | 3.583029  |
| m2     | 12.614695 | 3.551717  |
| m3     | 104.966125| 10.245298 |
| m4     | 88.914329 | 9.429439  |
| m5     | 22.119038 | 4.703088  |
| m6     | 22.052465 | 4.696005  |
| m7     | 104.839210| 10.239102 |

O modelo que apresentou o melhor desempenho, com base nas métricas, foi o **m2**, exibindo o menor MSE e variabilidade, indicando sua robustez na previsão.

## Visualização
Todos os modelos foram avaliados por meio de métricas de validação cruzada plotadas em um único gráfico, permitindo uma comparação visual do desempenho entre as diferentes configurações.

