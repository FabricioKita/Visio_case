#  Dashboard com índice de saúde financeira no Power Bi

Este projeto tem como objetivo criar um **Índice de Saúde Financeira** a partir de um conjunto de arquivos `.csv`, bem como indicar a saúde financeira de múltiplos estabelecimentos com outras métricas. O conjunto foi disponibilzado pela empresa Visio que compõe os dados das lojas de Lorenzzo Lopez.

---

## Arquivos Utilizados

- `receipts.csv`: informações principais dos cupons fiscais
- `payments.csv`: formas de pagamento
- `items.csv`: itens vendidos por recibo
- `discounts.csv`: descontos / promoções
- `torque.csv`: métricas financeiras diárias

---

## Objetivo

Desenvolver uma métrica de índice de saúde financeira, variando de 0 a 4, com base em quatro variáveis principais:

1. Media do Torque normalizado
2. Ticket médio normalizado
3. Receita líquida do último mês normalizada
4: 1 - taxa de desconto normalizado
---

Indice de saúde financeira = Media do Torque normalizado + Ticket médio normalizado + Receita líquida do último mês normalizada + (1 - taxa de desconto)

Variando de 0 a 4, o índice representa o quão saudável uma loja está, permitindo uma comparação entre lojas.

Cabe ressaltar que a taxa de desconto não possuem uma relação perfeitamente linear entre receita e taxa de desconto. Portanto, podemos estabelecer outras métricas para avaliar a correlação, como correlação de kendal ou spearmam e entender o comportamento

---

