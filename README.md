# 📉 Dashboard de Rentabilidade: Vendas, Custos e Margem de Lucro

Este projeto foca na análise da saúde financeira das vendas, avaliando o impacto dos custos de envio no lucro final e monitorando o cumprimento de metas mensais através de KPIs.

## 🎯 Respostas às Perguntas de Negócio
O projeto foi construído para resolver os seguintes desafios:
1. **Modos de Envio**: Qual o faturamento por categoria de envio (Standard, Second Class, etc)? Visualizado em um *Gráfico de Cascata*.
2. **Eficiência Logística**: Quais mercados possuem o maior custo médio de envio? (Análise via *Treemap*).
3. **Gestão de Metas (KPI)**: Monitorização da meta de 350 para o valor de venda mensal. 
4. **Análise de Lucratividade**: Cálculo do Lucro (Venda - Custo de Envio) por categoria de produto.
5. **Evolução da Margem**: Comportamento da Margem de Lucro ao longo do tempo.

## 🛠️ Tecnologias Utilizadas
* **Power BI**: Modelagem em esquema estrela (Star Schema) conectando 4 tabelas.
* **DAX**: 
    * `Lucro = SUM(Vendas[Valor Venda]) - SUM(Vendas[Custo Envio])`
    * `Margem de Lucro % = DIVIDE([Lucro], SUM(Vendas[Valor Venda]))`
    * `Média de Venda = AVERAGE(Vendas[Valor Venda])`
* **Data Modeling**: Relacionamento entre as tabelas Clientes, Pedidos, Produtos e Vendas.

## 📊 Estrutura dos Dados
* **Dimensão Cliente**: Segmento e localização.
* **Dimensão Produto**: Categorias e Subcategorias.
* **Fato Vendas**: Valores financeiros, quantidades e custos operacionais.

## 📸 Visualização
*(Adicione aqui o print do seu dashboard)*
![Dashboard de Rentabilidade](screenshots/kpi_metas.png)

---
*Projeto desenvolvido para prática de Business Intelligence com foco em análise de lucro e metas.*
