# 📈 Projeto de Análise de Vendas e Segmentação de Clientes (E-commerce Olist)

Este projeto implementa todo o ciclo de vida da Análise de Dados, transformando dados brutos de transações de um e-commerce brasileiro (Olist) em insights acionáveis de negócio. O objetivo final é segmentar clientes (RFM) e otimizar as estratégias de marketing e logística.

---

## 🎯 Resultados e Principais KPIs

O Dashboard final no Power BI (disponível na pasta `/reports/`) revela os seguintes KPIs consolidados:

| KPI Chave | Valor Global | Insight |
| :--- | :--- | :--- |
| **Receita Total** | R$ 16,4 Milhões (Aprox.) | Base para o cálculo de rentabilidade. |
| **Volume de Pedidos** | 97.500 Pedidos Únicos | Volume real de transações na base. |
| **Ticket Médio** | R$ 167,87 (Aprox.) | Valor médio gasto por pedido. |
| **Segmento VIP** | [Sua % de clientes VIP] | Foco para programas de retenção. |

---

## 🛠️ Stack Tecnológica

* **Linguagem de Análise:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização e Relatório:** Power BI (para Dashboard)
* **Estatística:** Matplotlib, Seaborn, Análise RFM
* **Versionamento:** Git/GitHub

---

## 📊 Estrutura do Projeto e Metodologia

O projeto seguiu a metodologia CRISP-DM simplificada, dividida em quatro fases principais:

### Fase 1: ETL (Extract, Transform, Load)
* **Objetivo:** Consolidar 9 arquivos CSV separados (Dados de Pedidos, Itens, Clientes, Pagamentos, Produtos, etc.) em uma Tabela Mestra única.
* **Destaque:** Uso intensivo da função `pd.merge()` para recriar o esquema do banco de dados relacional e tratamento de valores nulos (NaT/NaN).

### Fase 2: Análise Exploratória de Dados (EDA)
* **Objetivo:** Calcular KPIs primários e identificar tendências.
* **Destaque:** Criação de colunas temporais (`Feature Engineering`) para análise de sazonalidade e cálculo do **Tempo Real de Entrega** vs. **Tempo Estimado** (KPI Logístico).

### Fase 3: Desafio Avançado (Análise RFM)
* **Objetivo:** Segmentar clientes com base no seu valor comportamental.
* **Destaque:** Cálculo de **Recência (R)**, **Frequência (F)** e **Valor Monetário (M)**, seguido da aplicação do método **Quantile** para atribuir *scores* e categorizar clientes em segmentos (Ex: Campeões, Em Risco).

### Fase 4: Data Storytelling e Deploy
* **Objetivo:** Apresentar os *insights* em um formato consumível.
* **Destaque:** Construção de um Dashboard interativo no Power BI e uso de medidas **DAX** para lidar com duplicação de dados (utilizando a medida `SUMX` para garantir a precisão da Receita Total).

---

## 💡 Recomendações de Negócio

1.  **Atenção ao Ticket Médio:** Focar campanhas de *upselling* em estados de alto volume (como SP) para capitalizar a demanda existente e aumentar o valor médio por transação.
2.  **Retenção de VIPs:** O segmento de clientes **Campeões/VIPs** (identificado pelo RFM) deve receber ofertas exclusivas para garantir a retenção e a recorrência de receita.
3.  **Planejamento Sazonal:** Antecipar a estocagem no Q4 (Novembro/Black Friday) e planejar promoções agressivas nos meses de baixa receita (Janeiro/Fevereiro).

---

## 🚀 Como Executar o Projeto

1.  Clone o repositório: `git clone https://www.youtube.com/watch?v=X49Wz3icO3E`
2.  Crie e ative um ambiente virtual.
3.  Instale as bibliotecas necessárias: `pip install pandas numpy matplotlib seaborn jupyter`
4.  Execute os Notebooks na pasta `/notebooks/` em ordem (1.0, 2.0, 3.0) para replicar a análise.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para criar problemas (issues) ou enviar solicitações de pull (pull requests) para melhorias ou correções.

## :memo: Licença

Esse projeto está sob a licença MIT.

---

*Este projeto foi desenvolvido por [Gabriel Santos/GabrielSantos777].*