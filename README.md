# Taxing the Titans An Econometric Study of Billionaire Wealth Drivers


## Project presentation
# Taxing the Titans: Billionaire Wealth Drivers

This repository contains an econometric analysis of billionaire wealth distribution and the potential impacts of global taxation.

## Project Overview
This study investigates the relationship between national macroeconomic indicators—such as GDP, Foreign Direct Investment (FDI), and Tax Revenue—and the concentration of ultra-high-net-worth individuals. It further models "flight risk" probabilities to evaluate the effectiveness of the Zucman 2% tax proposal under different international coordination scenarios.

## Key Econometric Insights
* **Market Scale:** GDP is the strongest determinant; a doubling of GDP is associated with an 89.5% increase in the number of billionaires.
* **Taxation Paradox:** Higher aggregate tax pressure does not significantly deter billionaires, likely because high-tax jurisdictions offer better institutional quality and public services.
* **Openness:** Increased FDI and international connectivity are positively correlated with billionaire presence.

## Flight Risk & Simulation Results
The project utilizes a logistic transformation to convert individual risk scores (based on sector mobility, wealth origin, and geography) into relocation probabilities.

### Revenue Collection Efficiency
| Scenario | Average Flight Prob (μϵ) | Collection Efficiency |
| :--- | :---: | :---: |
| **France Alone** | 18.7% | 78.4% |
| **G7 Coordination** | 10.1% | 89.6% |
| **G20 Coordination** | 7.1% | 92.8% |
| **Near-Global** | 4.0% | 95.9% |

## Methodology Summary
The analysis was performed using **R** with the following diagnostic rigor:
* **Multicollinearity:** Tested via Variance Inflation Factor (VIF), showing no meaningful correlation between regressors.
* **Normality:** Shapiro-Wilk test confirmed normally distributed residuals (p = 0.78).
* **Heteroscedasticity:** Breusch-Pagan test indicated constant error variance (p = 0.73).

---
**Authors:** Philipine Poirier & Tony De Amorim  
**Date:** January 8, 2026

## Data sets presentation
For this project we decided to center our work on a dataset made by the The Peterson Institute for International Economics. This institute is an "independent non-profit, non-partisan research organization dedicated to strengthening prosperity and human welfare in the global economy through expert analysis and practical policy solutions". The dataset was made by the thinktank in 2016 and describes more than billionaires over 23 variables such as citizenship, origin of wealth and net worth. Every source is used in the research paper to find the data is available in the raw dataset, which can be downloaded freely directly on the page of the article [The Origins of the Superrich: The Billionaire Characteristics Database](https://www.piie.com/publications/working-papers/origins-superrich-billionaire-characteristics-database)

As we want to focus our research on the impact of taxation on billionaires' behaviors, we wanted to use data about wealth taxation in every country. However, tax rates are hard to find and are often unavailable in countries where billionaires live (they surprisingly avoid countries with high taxation !). To remediate to this issue, we decide to use the ratio of taxation as a % of total revenue for the governement. This data captures the idea that the more important tax revenue is for a country's budget, the more likely it is that this country applies high level of taxation. Following this idea, we use the freely accessible dataset of the world bank [Tax revenue (% of GDP)](https://data.worldbank.org/indicator/GC.TAX.TOTL.GD.ZS) 

To complete our study and have a better understanding of the different trends in the billionaires' world, we use a combination of World Bank's datasets to select several macroeconomics variables such as :

- [Foreign direct investment, net inflows (% of GDP)](https://data.worldbank.org/indicator/BX.KLT.DINV.WD.GD.ZS) : This variable reflects a country’s ability to attract foreign capital and international firms. It serves as a proxy for economic openness, institutional quality and fiscal attractiveness, all of which can influence where billionaires choose to locate their activities, structure their assets, or establish residence.
- [Gross capital formation (% of GDP)](https://data.worldbank.org/indicator/NE.GDI.TOTL.ZS) : This indicator measures the share of resources devoted to investment in physical capital (infrastructure, machinery, buildings, etc.). A high level of capital formation signals dynamic investment and growth potential, creating more opportunities for large firms to expand and for individuals to accumulate very large fortunes, including billionaire-level wealth.
- [Total population](https://data.worldbank.org/indicator/SP.POP.TOTL) Population size captures the potential size of the internal market and the scale of demand for goods and services. Larger populations can support larger firms and more diversified economic activities, increasing the probability that extremely large fortunes emerge. In addition, we use population to normalise our results (for example, by looking at the number or total wealth of billionaires per inhabitant), which allows for more meaningful comparisons across countries of very different sizes.

Due to a data accessibility constraint we also used a dataset from the IMF accessible with the following instructions :

- Go to the [IMF data explorer](https://data.imf.org/en/Data-Explorer)
- Select the "World Economic Outlook (WEO)" dataset
- Select the "Gross domestic product (GDP), Current prices, Purchasing power parity (PPP) international dollar, ICP benchmarks 2017-2021" indicator
- Select "All" as a Time Period
- Download "Data on this page" in a csv format   

We included GDP in Purchasing Power Parity.  This variable captures the overall economic performance and living standards of each country, adjusted for price level differences. Since wealth creation and the emergence of billionaires are closely linked to the size, productivity and income level of national economies, PPP-adjusted GDP is a natural control variable to account for cross-country differences in economic capacity.
