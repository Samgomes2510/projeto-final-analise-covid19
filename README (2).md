# Impacto da COVID-19 na Saúde Pública no Brasil

## Objetivo

Este projeto tem como objetivo analisar os impactos da pandemia de COVID-19 no Brasil, utilizando dados públicos do BigQuery para entender a evolução dos casos e óbitos ao longo do tempo, além de calcular a taxa de letalidade e destacar padrões relevantes por estado.

## Fonte dos Dados

Os dados foram obtidos do banco público do Google Cloud BigQuery:

- Dataset: `bigquery-public-data.covid19_open_data`
- Tabela utilizada: `data_by_region`

## Etapas do Projeto

### 1. Seleção dos Dados
Foram selecionados dados da tabela `data_by_region`, filtrando informações do Brasil no período de **01/04/2020 a 31/12/2023**, com foco nas colunas:
- `date`
- `subregion1_name` (estados)
- `cumulative_confirmed`
- `cumulative_deceased`

### 2. Análise Exploratória dos Dados (EDA)
Realizada com Python (Pandas/Matplotlib/Seaborn), abordando:
- Evolução temporal dos casos confirmados
- Evolução dos óbitos
- Estados com maior número de casos
- Estados com maior número de óbitos
- Taxa de letalidade (calculada como: `óbitos / casos confirmados`)

### 3. Tratamento e Preparação dos Dados
- Preenchimento de valores ausentes
- Criação da coluna `fatality_rate` (taxa de letalidade)
- Conversão de datas
- Agrupamento por estado e período

### 4. Visualizações
As visualizações foram desenvolvidas no **Looker Studio**, com os seguintes gráficos:

- Tabela com total de casos e óbitos por estado
- Gráfico de linha: evolução de casos confirmados
- Gráfico de linha: evolução de óbitos
- Gráfico de barras: comparativo entre estados
- Gráfico de mapa geográfico: distribuição de óbitos por estado
- Taxa de letalidade (campo calculado em porcentagem)

### 5. Painel Interativo
Acesse o painel interativo com as visualizações aqui:  
**[Clique para acessar o painel no Looker Studio](https://lookerstudio.google.com/reporting/34a362b3-967e-4b24-b2ca-037005e1518c)**

## Ferramentas Utilizadas

- Google BigQuery
- Google Cloud Platform
- Python (Pandas, Matplotlib, Seaborn)
- Google Looker Studio
- Google Colab

## Principais Insights

- O estado com maior número de óbitos foi **São Paulo**.
- A maior taxa de letalidade ocorreu no estado do **Rio de Janeiro** durante o ano de 2021.
- A curva de casos apresentou seu pico em **março de 2021**.
- Houve uma queda consistente nos novos casos a partir do segundo semestre de 2022.

## Autor

**Samuel Gomes dos Santos**  
Aluno do curso de Formação de Analista de Dados — EBAC  
[GitHub: github.com/Samgomes2510](https://github.com/Samgomes2510)