COVID-19 and Global Happiness Analysis
This project explores the relationship between the spread of COVID-19 and key global happiness indicators such as GDP per capita, social support, and life expectancy. It combines COVID-19 case data with the Worldwide Happiness Report to investigate how a country’s well-being metrics correlate with the infection rate.

Objective
To:

Understand how COVID-19 infection rates vary across countries.

Analyze if countries with higher happiness indicators were more or less affected.

Visualize and interpret correlations between socioeconomic factors and pandemic severity.

Datasets Used
1. COVID-19 Time Series (Johns Hopkins University)
covid19_Confirmed_dataset.csv — Cumulative confirmed cases.

covid19_deaths_dataset.csv — Cumulative death counts.

Columns: Province/State, Country/Region, Lat, Long, followed by daily case counts.

2. Worldwide Happiness Report
worldwide_happiness_report.csv

Columns include:

Country or region

GDP per capita

Social support

Life expectancy (or similar, e.g. Healthy life expectancy)

Other happiness-related metrics

Key Steps and Methodology
1. Data Cleaning
Removed unnecessary columns (Lat, Long, Province/State) from COVID datasets.

Grouped COVID data by country and computed cumulative totals.

Standardized column names in the happiness report for easier merging.

2. Feature Engineering
Calculated Max Infection Rate as the highest daily jump in confirmed cases for each country.

Selected three core features from the happiness report:

GDP per capita

Social support

Life expectancy

3. Data Merging
Combined the COVID-19 infection rate data with happiness indicators using the country as the key.

4. Exploratory Data Analysis (EDA)
Used pairplot and heatmap to analyze variable relationships and correlations.

Plotted scatterplots to visualize:

GDP per capita vs. Max Infection Rate

Social Support vs. Max Infection Rate

Insights
Correlation patterns suggest a non-linear relationship between infection rate and happiness factors.

Logarithmic plots helped normalize highly skewed data and highlight trends more clearly.

Potential socioeconomic insights were derived from combining health data with well-being metrics.

Requirements
Python 3.8+

Libraries:

pandas

numpy

seaborn

matplotlib
