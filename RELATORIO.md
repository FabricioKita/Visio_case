# Relatório de Análise Financeira — Índice de Saúde das Lojas

## 1. Visão geral do problema

### 1.1 Contexto geral
Lorenzzo Lopes, um empreendedor de 45 anos busca entender melhor o comportamento dos seus estabelecimentos. Lorenzzo acredita fielmente 

### 1.2 Perguntas
As principais perguntas que direcionaram esta análise foram:
- Como comparar a performance financeira de lojas distintas?
- Quais lojas estão com bom desempenho e quais precisam de atenção?
- Quais insights tiramos dos dados?


## 2. Fonte e preparação de dados

### 2.1 Arquivos CSV utilizados
Foram utilizados os seguintes arquivos:
- receipts.csv: 
- items.csv: 
- payments.csv: 
- discounts.csv: 
- torque.csv:
- dados_dash1.csv


### 2.2 Etapas no Power BI
- Importação dos dados com BQ
- Criação das relações entre tabelas
- Cálculo de métricas em DAX
- Visualização de dados com o próprio power bi

## 3. Construção do Índice de Saúde Financeira

### 3.1 Métricas utilizadas (normalizadas entre 0 e 1)

Foram utilizadas  4 variáveis para a construção da métrica, dentre elas: Torque, ticket médio, taxa de desconto e faturamento. Todas foram normalizadas devidamente utilizando o mínimo e o máximo entre as lojas.
Cada uma das variáveis tem uma atuação distinta na métrica, mas resumidamente teremos:

Lojas com alta pontuação tendem a ter:
- conceder menos descontos
- ter maior faturamento
- ter melhor ticket médio
- apresentar melhor desempenho operacional (torque)

O índice de saúde financeira é calculado da seguinte forma:

ISF = ticket_medio_normalizado + faturamento_normalizado + soma_net_torque_normalizado + (1 - descontos-normalizados)

Todos os códigos estão descritos no .ipynb


