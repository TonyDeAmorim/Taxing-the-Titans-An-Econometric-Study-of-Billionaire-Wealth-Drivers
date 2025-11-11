# Taxing the Titans An Econometric Study of Billionaire Wealth Drivers



## Project presentation


## Data sets presentation
For this project we decided to center our work on a dataset made by the The Peterson Institute for International Economics. This institute is an "independent non-profit, non-partisan research organization dedicated to strengthening prosperity and human welfare in the global economy through expert analysis and practical policy solutions". The dataset was made by the thinktank in 2016 and describes more than billionaires over 23 variables such as citizenship, origin of wealth and net worth. Every source is used in the research paper to find the data is available in the raw dataset, which can be downloaded freely here : https://www.piie.com/publications/working-papers/origins-superrich-billionaire-characteristics-database   

As we want to focus our research on the impact of taxation on billionaires' behaviors, we wanted to use data about wealth taxation in every country. However, tax rates are hard to find and are often unavailable in countries where billionaires live (they surprisingly avoid countries with high taxation !). To remediate to this issue, we decide to use the ratio of taxation as a % of total revenue for the governement. This data captures the idea that the more important tax revenue is for a country's budget, the more likely it is that this country applies high level of taxation. Following this idea, we use the freely accessible dataset of the world bank "Tax revenue (% of GDP)" available here : https://data.worldbank.org/indicator/GC.TAX.TOTL.GD.ZS

We still wanted to have a more precise idea of real taxation so we also decided to work on the "Taxes on income, profits and capital gains (% of revenue)" dataset of the world bank, even if a lot of countries are missing (especialy for old values). The data set is available here : https://data.worldbank.org/indicator/GC.TAX.YPKG.RV.ZS

To complete our study and have a better understanding of the different trends in the billionaires' world, we use a custom dataset from the IMF data explorer to select several macroeconomics variables such as :

- GDP in PPP (https://data.imf.org/en/Data-Explorer?datasetUrn=IMF.RES:WEO(9.0.0)&INDICATOR=PPPGDP) : We included GDP in Purchasing Power Parity to capture the overall economic performance and living standards of each country, as wealth creation and billionaire emergence are closely linked to the size and strength of national economies.
- Inward Direct investment, Net (liabilities less assets) (https://data.imf.org/en/Data-Explorer?datasetUrn=IMF.STA:DIP(12.0.0)&INDICATOR=INWD_D_NETLA_FALL_ALL) : This variable reflects a country’s ability to attract foreign capital, serving as a proxy for its economic openness and fiscal attractiveness, key factors influencing where billionaires choose to invest or reside.
- Investment and Capital Stock Dataset (ICSD) (https://data.imf.org/en/datasets/IMF.FAD:ICSD) : data for investment and capital stock for the general government, private sector and public-private partnerships, across the Fund member countries.We use the ICSD to measure the scale and composition of national investment, as higher levels of capital accumulation and infrastructure development create environments conducive to wealth expansion.
- Interest rate : (https://data.imf.org/en/datasets/IMF.STA:MFS_IR) : The interest rate captures the stance of monetary policy and the cost of capital, both of which directly affect asset valuation, investment incentives, and consequently the growth of billionaire wealth.


The IMF data explorer is usable following this link : https://data.imf.org/en/Data-Explorer