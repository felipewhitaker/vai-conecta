# VAI Conecta

VAI Academy is a Brazillian Edtech e HR tech. It was born from a dream: train Artifical Intelligence (AI) and Advanced Analytics talents, and help them become leaders to make a difference in companies and for society. VAI Academy is part of of Visagio, a strategic consultant group from Rio de Janeiro and currently (2023) present in 30 countries, helping clients in different sectors, such as: finance services, retail and engineering.

## Case explanation

VAI Shoes is a shoes company with a high growth rate. Because it operates in a highly competitive space, the best way to improve it's profitability is through the improvement of the Sales and Operations Planning (S&OP) forecasts. With this in mind, the guiding questions for the project are:

1. How is the forecast built?
2. Is the new forecasting method better than the current one?
3. Which products have the best and worse forecasts?
4. If it was possible to include other variables, what should be included?
5. What are the next steps for the project?

### Data

The description of each file can be seen below. Both files were stored in Git LFS and are inside `data/` folder.

To download the data after cloning this repo, simply run `git lfs checkout`

#### Sales History

File: `tbl_vendas_mensais.csv`
Description: Monthly sales of each SKU

| coluna           | chave    | informação                | tipo    |
|------------------|----------|---------------------------|---------|
| dt_sale primária | primária | Mês e Ano da venda        | Data    |
| id_sku           | primária | Id do SKU                 | Inteiro |
| ds_sku           | -        | Descrição do SKU          | String  |
| ds_category      | -        | Categoria do SKU          | String  |
| ds_product_line  | -        | Linha de produtos do SKU  | String  |
| ds_brand_segment | -        | Segmento da marca do SKU  | String  |
| ds_tecnology     | -        | Tecnologia do SKU         | String  |
| qt_sale          | -        | Quantidade Vendida no Mês | Inteiro |
| vl_sale_price    | -        | vendido no mês (R$)       | Float   |

#### Benchmark Prediction

File: `tbl_previsao_sop.xlsx`
Description: Demand forecast of M+0 to M+3 executed by the S&OP team for each product line

| coluna                       | chave     | informação                                                                         | tipo   |
|------------------------------|-----------|------------------------------------------------------------------------------------|--------|
| dt_sale                      | primária  | Mês e Ano da venda                                                                 | Data   |
| ds_product_line              | primária  | Linha de produtos do SKU                                                           | String |
| qt_sale_sop_forecasting_ m1  | -         | Quantidade de venda prevista  para o mês, em M-1 (1 mês  antes da data da venda)   | Float  |
| qt_sale_sop_forecasting_ m2  | -         | Quantidade de venda prevista  para o mês, em M-2 (2 meses  antes da data da venda) | Float  |
| qt_sale_sop_forecasting_ m3  | -         | Quantidade de venda prevista  para o mês, em M-3 (3 meses  antes da data da venda) | Float  |

### Exploratory Analysis

- Todas as SKUs são vendidas todos os meses?
- Qual é a média e variância de cada um dos produtos? Qual é a distribuição de cada produto?
- Qual foi o comportamento por Linha de Produto, Categoria e SKU?
- Há variação do preço com o tempo? E qual é a distribuição dos preços por Marca, Categoria e SKU?
