# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

# Análise Preditiva de Estoque

## Introdução
Este repositório contém uma análise preditiva realizada com base em um conjunto de dados que inclui as seguintes colunas: `ID_PRODUTO`, `DATA_EVENTO`, `PRECO`, `QUANTIDADE_ESTOQUE`. A análise foi conduzida utilizando o SageMaker Canvas para prever a quantidade de estoque de produtos.

## Dados Utilizados
Os dados utilizados na análise contêm as seguintes colunas:

- **ID_PRODUTO**: Identificador único do produto.
- **DATA_EVENTO**: Data do evento relacionado ao produto.
- **PRECO**: Preço do produto.
- **QUANTIDADE_ESTOQUE**: Quantidade de estoque disponível do produto.

## Relatório de Desempenho do Modelo
Abaixo estão as métricas de desempenho do modelo preditivo gerado:

- **Avg. wQL**: 0.278
- **MAPE**: 1.808
- **WAPE**: 0.486
- **RMSE**: 30.465
- **MASE**: 0.693

### Resumo das Métricas

- **Avg. wQL (Weighted Quantile Loss)**: Mede a perda quantílica ponderada, que é útil para avaliar a precisão das previsões em diferentes quantis.
- **MAPE (Mean Absolute Percentage Error)**: Calcula o erro percentual absoluto médio entre os valores previstos e os valores reais. É útil para entender a precisão relativa das previsões.
- **WAPE (Weighted Absolute Percentage Error)**: É uma versão ponderada do MAPE, que leva em consideração a importância relativa dos diferentes valores.
- **RMSE (Root Mean Squared Error)**: Mede a raiz do erro quadrático médio, que é a média das diferenças quadradas entre os valores previstos e os valores reais. É sensível a grandes erros.
- **MASE (Mean Absolute Scaled Error)**: Calcula o erro absoluto médio escalado, que é útil para comparar a precisão do modelo com um modelo de referência simples, como a média histórica.

## Impacto das Colunas na Precisão do Modelo
As colunas que mais contribuíram para a precisão do modelo são:

1. **Holiday_BR**: 87.84%
2. **PRECO**: 12.16%

## Visualização
![Relatório de Desempenho do Modelo](https://github.com/bfitzner100/lab-aws-sagemaker-canvas-estoque/blob/main/analise.png)

## Conclusão
A análise preditiva demonstrou que a variável `Holiday_BR` teve o maior impacto na precisão do modelo, seguida pelo `PRECO`. Essas informações são cruciais para entender os fatores que influenciam a quantidade de estoque e podem ser usadas para otimizar a gestão de inventário.

## Próximos Passos
1. **Refinamento do Modelo**: Ajustar o modelo para melhorar ainda mais a precisão.
2. **Integração**: Integrar o modelo preditivo com sistemas de gestão de estoque para automação.
3. **Monitoramento Contínuo**: Monitorar o desempenho do modelo e atualizar conforme necessário.
