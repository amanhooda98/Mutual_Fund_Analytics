🟢 MUTUAL FUND ANALYTICS USING PANDAS 🟢\
\
Preface :

This analysis aims to compare the three major categories of mutual funds
:\
\
1.Equity :\
Equity funds primarily invest in stocks, and hence go by the name of
stock funds as well. They invest the money pooled in from various
investors from diverse backgrounds into shares/stocks of different
companies. The gains and losses associated with these funds depend
solely on how the invested shares perform (price-hikes or price-drops)
in the stock market. Also, equity funds have the potential to generate
significant returns over a period. Hence, the risk associated with these
funds also tends to be comparatively higher.


2.Debt :\
Debt funds invest primarily in fixed-income securities such as bonds, securities and treasury bills. They invest in various fixed income instruments such as Fixed Maturity Plans (FMPs), Gilt Funds, Liquid Funds, Short-Term Plans, Long-Term Bonds and Monthly Income Plans, among others. Since the investments come with a fixed interest rate and maturity date, it can be a great option for passive investors looking for regular income (interest and capital appreciation) with minimal risks. 



3.Hybrid :\
As the name suggests, hybrid funds (Balanced Funds) is an optimum mix of bonds and stocks, thereby bridging the gap between equity funds and debt funds. The ratio can either be variable or fixed. In short, it takes the best of two mutual funds by distributing, say, 60% of assets in stocks and the rest in bonds or vice versa. Hybrid funds are suitable for investors looking to take more risks for ‘debt plus returns’ benefit rather than sticking to lower but steady income schemes. 


Data Sources :


Mutual fund historical data was obtained using the mftool library(https://github.com/NayakwadiS/mftool),
Historical data for NIFTY50 index was obtained from yahoo finance and extracted in a csv format. The collected data is of the last 5 years.
Detailed steps of how the data was extracted can be found in the jupyter notebook. 


Project Walkthrough :

* I have selected 3 mutual funds from each of the above mentioned categories, these 3 were top rated in their categories as per moneycontrol.com, calculated the mean of all 3 in each category , this mean will represent the particular category in the analysis

* normalized the data to aid in better comparison ( refer the jupyter notebook)

* The result after merging the data was as represented in the following plot :

![Alt text](image-1.png)

Findings :

* Equity mutual funds have shown the highest returns of **194.57 %** in 5 years in comparison to **65.28 %** of NIFTY50 index,
and a CAGR of **24.12 %**.

* Debt mutual funds have shown the lowest returns of **44.29 %** in 5 years and a CAGR of **7.61 %**

* Hybrid mutual funds have shown returns of **85.90 %** and CAGR of **13.2 %**

Parameters to judge risk and reward ( Alpha α and Beta β) :

* Alpha : Alpha measures the return on an investment above what would be expected based on its level of risk. It’s also sometimes used as a simple measure of whether an asset outperformed an appropriate benchmark such as NIFTY50 in this case, 
for an example if nifty has moved up by X % in a time frame , and a mutual fund has moved by Y % in the same time frame 
Y/X will define its α , an α > 1 indicates higher returns than the benchmark, which is desirable ,
In our analysis we have considered the post covid recovery time frame to calculate the alpha, where equity has shown significant growth, but at what risk ?
Here comes beta β into the picture.


* Beta : Beta, or the beta coefficient, measures volatility relative to the market and can be used as a risk measure. The market always has a beta of 1, so betas above 1 are considered more volatile than the market, while betas below 1 are considered less volatile.
for an example if nifty has dropped by X % and a mutual fund has dropped by Y % , then Y/X will define its beta β,
a β <1 indicates better stability with respect to the market.
In our analysis , we have considered the market fall during covid, and during the second quarter of 2022.



Conclusion :

* Equity mutual funds had both alpha and beta parameters more than one which means they are for sure giving the most returns of all, but they are much more volatile , which makes it unsuitable for people who dont want to take as much risk and looking for short term investments.

* Debt mutual funds have a low alpha, but have an even lower beta, which makes them almost invulnerable to equity market conditions, you can see the same in the graph. they are good alternatives to bank FDs considering they have no lock in period and give similar or better returns.

* Hybrid mutual funds aim to capitalize on the equity market gains , but also try to balance the volatility with some investments being in debt instruments, they might be a good option for a investor who doesnt directly want to jump into equity funds but wants higher return than bank FDs


The interactive Tableau dashboard for the comparison can be found on the below link :


https://public.tableau.com/views/Mutual_Fund_Analytics/Dashboard1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link
<div class='tableauPlaceholder' id='viz1693748563716' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Mu&#47;Mutual_Fund_Analytics&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Mutual_Fund_Analytics&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Mu&#47;Mutual_Fund_Analytics&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>               