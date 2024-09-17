# 🚗 Previsão de Produção e Vendas de Veículos

## 📄 Visão Geral do Projeto
Este projeto tem como foco a análise de dados de produção e vendas de veículos para prever tendências futuras, ajudando montadoras a otimizar a gestão de estoques. O conjunto de dados inclui séries temporais sobre produção e vendas de veículos, com o objetivo de prever se haverá aumento ou diminuição no estoque até dezembro de 2024. O projeto envolve decomposição de séries temporais, testes de estacionariedade e previsão utilizando o modelo ARIMA.

Além disso, foi utilizado um conjunto de dados separado para analisar o desempenho de alunos com base em horas de estudo, taxa de presença e notas anteriores, aplicando técnicas de limpeza de dados e explorando possíveis relações entre esses fatores.

## 📊 Descrição dos Conjuntos de Dados

### Dados de Produção e Vendas de Veículos (CP4 Time Series.xlsx):

* Este conjunto de dados contém séries temporais relacionadas à produção e vendas de diversos tipos de veículos ao longo de vários períodos.
  
* As colunas incluem:
  * Produção: Dados mensais sobre a produção de veículos.
  * Vendas: Dados mensais sobre a venda de veículos.

### Dados de Desempenho Acadêmico de Alunos (CP4 Data Cleaning.csv):
* Este conjunto de dados contém informações sobre o desempenho acadêmico de alunos, incluindo:
  * Horas de Estudo por Semana: Valores variando de 0 a 20 horas semanais.
  * Taxa de Presença: Valores variando de 25% a 100%.
  * Notas Anteriores: Valores de 25 a 100, representando as notas anteriores dos alunos.

##🔍 Análises Realizadas

### análise de Séries Temporais (Produção e Vendas de Veículos):
1. **Decomposição Sazonal:** Aplicação da função seasonal_decompose para identificar tendências e sazonalidades nas séries de produção e vendas com um período de 24 meses.
2. **Teste de Estacionariedade:** Uso da função adfuller para testar a estacionariedade das séries. Se não estacionárias, as séries são transformadas para a primeira diferença e o teste é repetido.
3. **Modelos ARIMA:** Teste de modelos ARIMA com diferentes ordens (1,1,1), (2,1,2) e (12,1,12). O critério BIC foi utilizado para selecionar o modelo mais adequado.
4. **Projeção de Produção e Vendas:** Utilizando o modelo ARIMA selecionado, foi feita uma previsão para o mês de dezembro de 2024, para estimar quantos veículos serão produzidos e vendidos, ajudando a determinar se haverá excesso de estoque ou escassez.

### Limpeza e Análise de Dados de Desempenho Acadêmico:
1. **Tratamento de Valores Incorretos:** Limpeza de valores fora dos limites esperados para variáveis como horas de estudo, presença e notas, substituindo valores incorretos pelos máximos ou mínimos permitidos.
2. **Substituição de Valores Nulos:** Valores ausentes foram substituídos pela média das colunas correspondentes.
3. **Normalização dos Dados:** Análise da coluna de Parent Education Level, ajustando as categorias que estavam fora do padrão e contabilizando novamente as observações por categoria.

## 🛠️ Tecnologias Utilizadas

* Python para análise de dados e modelagem de séries temporais.
* Bibliotecas: pandas, numpy, matplotlib, seaborn, statsmodels, scipy

## ✍️ Autor

* Mateus Iago Sousa Conceição 
* Estudante de Engenharia de Software - FIAP

  ---

  # 🚗 Vehicle Production and Sales Forecasting

## 📄 Project Overview
This project focuses on analyzing vehicle production and sales data to forecast future trends, helping manufacturers optimize inventory management. The dataset includes time series data on vehicle production and sales, with the goal of predicting whether there will be an increase or decrease in stock by December 2024. The project involves time series decomposition, stationarity tests, and ARIMA model forecasting.

Additionally, a separate dataset was used to analyze student performance based on study hours, attendance rates, and previous grades. Data cleaning techniques were applied to explore potential relationships between these factors.

## 📊 Dataset Description

### Vehicle Production and Sales Data (CP4 Time Series.xlsx):

* This dataset contains time series data related to the production and sales of various types of vehicles over several periods.
* The columns include:
  * Production: Monthly data on vehicle production.
  * Sales: Monthly data on vehicle sales.

### Student Performance Data (CP4 Data Cleaning.csv):
* This dataset contains information about student academic performance, including:
  * Study Hours per Week: Ranging from 0 to 20 hours per week.
  * Attendance Rate: Ranging from 25% to 100%.
  * Previous Grades: Ranging from 25 to 100, representing students' previous grades

## 🔍 Analysis Performed

### Time Series Analysis (Vehicle Production and Sales):

1. **Seasonal Decomposition:** Applied the seasonal_decompose function to identify trends and seasonality in the production and sales series using a 24-month period.
2. **Stationarity Test:** Used the adfuller function to test the stationarity of the series. If non-stationary, the series was transformed to its first difference, and the test was repeated.
3. **ARIMA Models:** Tested ARIMA models with different orders (1,1,1), (2,1,2), and (12,1,12). The BIC criterion was used to select the most suitable model.
4. **Forecasting Production and Sales:** Using the selected ARIMA model, a forecast for December 2024 was made, estimating the number of vehicles to be produced and sold, determining whether there will be excess or shortage of inventory.

### Data Cleaning and Student Performance Analysis:

1. **Handling Incorrect Values:** Cleaned values outside the expected limits for variables like study hours, attendance, and grades, replacing incorrect values with the maximum or minimum allowed.
2. **Handling Missing Values:** Replaced missing values with the mean of the respective columns.
3. **Normalizing Data:** Analyzed the Parent Education Level column, adjusting categories that were incorrectly classified and recalculating the number of observations for each category.

## 🛠️ Technologies Used

* Python for data analysis and time series modeling.
* Libraries: pandas, numpy, matplotlib, seaborn, statsmodels, scipy

## ✍️ Author

* Mateus Iago Sousa Conceição 
* Data Science Student
