#  Dashboard com índice de saúde financeira no Power Bi

Este projeto tem como objetivo criar um **Índice de Saúde Financeira** a partir de um conjunto de arquivos `.csv`, bem como indicar a saúde financeira de múltiplos estabelecimentos com outras métricas. O conjunto foi disponibilzado pela empresa Visio que compõe os dados das lojas de Lorenzzo Lopez.

---

## Arquivos Utilizados

- receipts.csv: informações principais dos cupons fiscais
- payments.csv: formas de pagamento
- items.csv: itens vendidos por recibo
- discounts.csv: descontos / promoções
- torque.csv: métricas financeiras diárias

---
## Ferramentas utilizadas
- Power bi: Ferramenta de dashboards 
- Python: linguagem de progamação
- GoogleBigQuerry: Ferramenta de big data

## Objetivo

Desenvolver uma métrica de índice de saúde financeira, variando de 0 a 4, com base em quatro variáveis principais:

1. Torque Normalizado
2. Ticket médio normalizado
3. Faturamento normalizado
4: taxa de desconto normalizado
---

## Etapas no Power BI
- Importação dos dados com GoogleBigQuerry
- Criação das relações entre tabelas
- Cálculo de métricas em DAX
- Visualização de dados com o próprio power bi


## Métrica calculada

ISF = ticket_medio_normalizado + faturamento_normalizado + soma_net_torque_normalizado + (1 - descontos-normalizados)

Variando de 0 a 4, o índice representa o quão saudável uma loja está, permitindo uma comparação entre lojas.

Cabe ressaltar que a taxa de desconto não possuem uma relação perfeitamente linear entre receita e taxa de desconto. Portanto, podemos estabelecer outras métricas para avaliar a correlação, como correlação de kendal ou spearmam e entender o comportamento

---

Link do google drive com o dashboard:

https://drive.google.com/file/d/1nLg6dhUUl-OKCepMqxsvFAeu0NUHbkRu/view?usp=sharing


