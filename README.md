# 📊 Relatório de Projeto de Machine Learning com AWS SageMaker Canvas

## Introdução 🤔
Olá, este é o relatório do meu projeto de Machine Learning utilizando a plataforma AWS SageMaker Canvas, que permite criar modelos de aprendizado de máquina sem a necessidade de codificação. O objetivo deste projeto foi prever a demanda de produtos em estoque com base em um conjunto de dados fornecido.

## 1. Selecionando Dataset

### Descrição do Conjunto de Dados
O conjunto de dados utilizado contém informações detalhadas sobre o estoque e as vendas de produtos. O dataset possui as seguintes colunas:

- **item_id**: Identificação do produto
- **Location**: Localização
- **time_stamp**: Data
- **demand**: Demanda do produto
- **price**: Preço do produto
- **Product_category**: Categoria do produto

## 2. Treinando Dataset

### Análise das Métricas de Performance
Após o treinamento do modelo no SageMaker Canvas, as métricas de performance foram as seguintes:

- **Métrica de otimização (accuracy)**: 97.650%
- **Média do F1 Score**: 97.568%
- **Média de precisão (precision)**: 97.712%
- **Média de recall**: 97.650%
- **Perda de validação (validation loss)**: 0.085

### Colunas Mais Influentes
As colunas que mais influenciam as previsões foram identificadas como:

- **price**: 34.289%
- **Product_category**: 30.178%
- **demand**: 25.094%
- **time_stamp**: 7.439%
- **Location**: 3.000%

## 3. Prevendo Valores

### Previsão

Utilizei o modelo treinado para prever a demanda de estoque. Abaixo estão as principais observações a partir das previsões geradas:

- **Impacto do preço na previsão de item_id**

![image](https://github.com/user-attachments/assets/d9f8194d-101d-4b73-a120-1aac004ef5c0)

- **Predições vs. Valores Reais**

![image](https://github.com/user-attachments/assets/e88d78be-b8b0-4b80-aa16-a2a585398606)



### Conclusões e Insights
- **Impacto do Preço**: O preço mostrou ser a característica mais importante para o modelo, influenciando significativamente as previsões de demanda.

- **Desempenho do Modelo**: O modelo teve um desempenho robusto, com uma precisão média superior a 97%. Isso demonstra que o modelo é confiável para prever a demanda de estoque.

- **Distribuição das Predições**: As visualizações mostraram que o modelo conseguiu capturar a maioria das tendências de demanda, com algumas discrepâncias menores entre previsões e valores reais.

## 4. Realizando Previsões

### Dados de Entrada Utilizados
Para testar o modelo, utilizei os seguintes dados de entrada:

| Coluna              | Valor              |
|---------------------|--------------------|
| Location            | Seattle            |
| time_stamp          | 01/10/2024 12:00 am|
| demand              | 235.9              |
| price               | 103                |
| Product_category    | Appliances         |

Esses dados foram inseridos na ferramenta de previsão do AWS SageMaker Canvas para gerar previsões específicas.

### Resultados das Previsões
O modelo gerou as seguintes previsões de demanda para diferentes `item_id`:

| item_id | Prediction (%) |
|---------|----------------|
| sku-090 | 55.234         |
| sku-079 | 4.210          |
| sku-183 | 6.845          |
| sku-146 | 4.112          |
| sku-041 | 3.978          |

**Insight Principal**: O `sku-090` apresentou a maior probabilidade de demanda, com 55.234%, indicando que é o item mais provável de ser demandado com base nos dados fornecidos.

## Análise dos Resultados

### Impacto do Preço na Predição do item_id
A análise visual revelou que o preço tem um impacto significativo nas previsões. O gráfico mostra como a variação do preço influencia a demanda prevista para o item_id específico.

### Comparação entre Valores Previstos e Reais
A comparação entre as previsões e os valores reais mostrou que o modelo conseguiu prever a demanda com uma boa precisão, embora algumas variações menores possam ser observadas.

## Considerações Finais
A previsão de demanda utilizando o AWS SageMaker Canvas mostrou-se eficaz. O item `sku-090` foi identificado como o mais provável de ser demandado, o que pode ajudar na otimização do estoque e nas estratégias de marketing. Estou satisfeito com os resultados alcançados e ansioso para continuar explorando e aprimorando minhas habilidades em Machine Learning. Este projeto foi uma excelente oportunidade para aplicar conceitos teóricos em uma plataforma prática e poderosa como o AWS SageMaker Canvas.

