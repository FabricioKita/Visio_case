# Relatório de Análise Financeira — Índice de Saúde das Lojas

## 1. Visão geral do problema

### 1.1 Contexto geral
Lorenzzo Lopes, um empreendedor de 45 anos busca entender melhor o comportamento dos seus estabelecimentos por meio de métricas e insights dos seus dados.

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

## Principais insights

Ranking final:

- highway-praça-ekin: 1,41
- highway-rua-bens-perdidos: 1,53
- highway-avenida-nova-balanca: 2,0
- highway-adidas-shopping: 2,97


Dentre todas as lojas analisadas, a que teve maior e menor métrica, respectivamente, foram a highway-adidas-shopping e highway-praca-ekin. Confirmando que a praca-ekin demanda uma atenção maior entre todas as lojas.

Encontramos picos sazonais perto do final e início do mês, e nos últimos meses essa tendência também se encontra no meio do mês. Indicando uma possibilidade de ajuste de equipe ou preparo técnico nos dias em que há picos faturamento e produtividade.

Loja Highway-adidas-shopping se destaca como um excelente benchmark para as outras lojas. Talvez o posicionamento possa influenciar, porém boas práticas de gerenciamento e administração também podem ser replicadas em outras lojas como exemplo.

Loja Highway-nova-balanca se destaca com altas taxas de desconto sobre seu faturamento. A taxa de desconto é calculada dividindo o a quantidade dde descontos pelo seu faturamento bruto. Portanto, uma redução na taxa de desconto pode resultar em um ticket médio mais alto.

## Recomendações a curto prazo:

- Utilizar dos dias de picos como estratégia para realocação de equipe podem ajudar a maximizar o ROI e realocar recursos de maneiras estratégicas.
- Utilizar da loja Highway-adidas-shopping como um benchmark para as outras lojas pode ser viável dentro do contexto analisado. Avaliar quais estratégias foram utilizadas nessa loja em comparação com as outras pode ajudar a aumentar o índice de saúde financeira das outras lojas.
- Ajustar a taxa de descontos da loja Highway-nova-balanca pode ser viável no contexto de aumento de ticket médio dos clientes.

## Limitações e próximos passos:

- Utilizar do NPS para avaliar não somente a saúde financeira, mas como também a satisfação dos clientes.
- Aprimorar o índice de saúde financeira para termos uma evolução ao longo do tempo.
- avaliação contínua das métricas apresentadas.
