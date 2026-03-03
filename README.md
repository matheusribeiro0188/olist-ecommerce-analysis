# 📦 Análise de E-commerce — Olist Dataset

Análise exploratória completa do dataset público da **Olist**, maior plataforma de e-commerce do Brasil. O projeto cobre desde a exploração inicial com SQL até a visualização interativa no Power BI, passando por análise em Python com geração de gráficos.

---

## 📊 Visão Geral dos Resultados

| Métrica | Valor |
|---|---|
| Total de pedidos (entregues) | 96.478 |
| Faturamento total | R$ 13.591.643,70 |
| Ticket médio por pedido | R$ 137,75 |
| Média de avaliações | 4,09 / 5,0 |
| Tempo médio de entrega | ~12 dias |
| Estados atendidos | 27 |

---

## 🗂️ Estrutura do Projeto

```
olist-analysis/
│
├── data/                          # CSVs do dataset original
│   ├── olist_orders_dataset.csv
│   ├── olist_order_items_dataset.csv
│   ├── olist_customers_dataset.csv
│   ├── olist_products_dataset.csv
│   ├── olist_sellers_dataset.csv
│   ├── olist_order_payments_dataset.csv
│   ├── olist_order_reviews_dataset.csv
│   ├── olist_geolocation_dataset.csv
│   └── product_category_name_translation.csv
│
├── sql/
│   └── projeto_olist.sql          # Queries exploratórias (SQL)
│
├── notebooks/
│   └── Olist.ipynb                # Análise em Python (pandas + matplotlib + seaborn)
│
├── imagens/
│   └── Graficos e print do dashboard
│
└── README.md
```

---

## 🛠️ Tecnologias Utilizadas

- **SQL** — exploração inicial, filtros, agregações e JOINs
- **Python** — pandas, matplotlib, seaborn (Google Colab)
- **Power BI** — dashboard interativo com KPIs e gráficos

---

## 🔍 Etapas da Análise

### 1. SQL — Exploração dos Dados
Exploração das 9 tabelas do dataset com foco em:
- Contagem e filtragem de pedidos por status
- Agrupamentos por estado, categoria e método de pagamento
- Cálculo de ticket médio via subquery
- Rankings com `ORDER BY` e `LIMIT`

### 2. Python — Análise Exploratória
Após o carregamento e tratamento dos dados (conversão de datas, verificação de nulos), foram geradas 6 visualizações:

- **Faturamento por Estado** — top 10 estados por receita total
- **Ticket Médio por Estado** — receita / pedidos únicos por estado
- **Faturamento por Categoria** — top 10 categorias de produtos
- **Evolução de Vendas por Mês** — série temporal de pedidos entregues
- **Tempo Médio de Entrega por Estado** — média de dias entre compra e entrega
- **Custo Médio de Frete por Estado** — média do valor de frete por estado

### 3. Power BI — Dashboard Interativo
Dashboard com 4 KPIs e 3 gráficos interativos, filtrado apenas para pedidos com status `delivered`.

---

## 💡 Principais Insights

**1. Sazonalidade — pico no fim de ano**
A evolução mensal mostra crescimento expressivo entre outubro e novembro, com queda em dezembro. O pico ocorre *antes* das festas, indicando comportamento de antecipação de compras. Recomendação: reforço de estoque e campanhas com 3 a 4 meses de antecedência.

**2. Categorias que mais faturam**
As categorias de maior receita são `beleza_saude`, `relogios_presentes`, `cama_mesa_banho` e `informatica_acessorios` — categorias típicas de presentes, o que reforça o padrão sazonal.

**3. Concentração regional em SP**
São Paulo lidera com folga no faturamento total. O ticket médio por estado aponta oportunidade de estratégias de upsell e bundles para aumentar o valor médio de compra nos demais estados.

**4. Cartão de crédito domina os pagamentos**
74% dos pagamentos são feitos com cartão de crédito, com média de 2,85 parcelas por compra. Boleto representa 19%. Parcelamento em 3x sem juros pode reduzir fricção e aumentar conversão.

**5. Frete elevado no Norte e Nordeste**
Estados como PB e RR apresentam os maiores custos médios de frete e maiores tempos de entrega, o que pode inibir a conversão. Campanhas com frete subsidiado e kits de produtos são estratégias indicadas.

**6. Boa satisfação dos clientes**
Média de avaliações de 4,09/5,0. A margem de melhoria está concentrada nos estados com maior tempo de entrega, onde a experiência logística impacta diretamente a nota.

---

## 📁 Dataset

Dataset público disponível no Kaggle:
[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

## 👤 Autor: Matheus Ribeiro
Linkedin :https://www.linkedin.com/in/matheus-ribeiro-3ba591173/

Feito como projeto de portfólio de análise de dados.
