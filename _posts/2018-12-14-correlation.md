---
title: "Answering"
bg: grey
color: white
fa-icon: search
---

### Answering the question!

Now that we get a sense of how the dataset is composed, and which kind of relationship there are, we can tackle our main question: is there a correlation between number of countries involved and their economical/financial services? 

We are going to use the following index:

* [Gini index](https://data.worldbank.org/indicator/SI.POV.GINI): it is a statistical measure of distribution used as a gauge of economic inequality, measuring income distribution or, less commonly, wealth distribution among a population. The coefficient ranges from  0% to  100%. 
* [Perceived Corruption index](https://www.transparency.org/research/cpi/overview): It tries measure how corrupt country's public sectors are seen to be.
* [Service ecxports (BoP,US dollars)](https://www.export.gov/article?id=Aspects-of-Service-Exports): A brief overview of exporting services overseas. This information is taken from "A Basic Guide to Exporting" provided by the U.S. Commercial Service to assist U.S. companies in exporting.
* financial exports as a percentage of:
* human development index:
* tax on income percentage: 


## Correlation Analysis

The Gini index and the entities origin country frequency has a correlation value equal to ``` 0.37058975049658943 ``` with a p-value of ```0.018572682928927605 ```. If this probability is lower than the conventional 5% ( 95% confidence interval for the correlation coefficient) the correlation coefficient is called statistically significant.
In other words the correlation  between the Gini index and entities country frequency is indeed correct and significant. However, it is weakly correlated, because there were a lot of outliers that we removed and it confers only countries cited between 5 and 8000 times with a Gini index less than 40, in other words poor countries as seen in the figure below.

![country distribution](img/gini_entity.png "gini entity")


The second index is the perceived corruption index. In this case there is also a very low correlation between the officers country frequency and the corruption index  of ``` 0.2903529327551021 ``` with p-value ```0.000247455687383302```. 

![country distribution](img/corruption_officer.png "gini entity")

This correlation is statically significant. However the majority of the countries are cited less than 200 times. This result makes sense, the more the country is perceived to be corrupted, the more it is cited. Corrupted countries have corrupted officers. 

![country distribution](img/corruption_address.png "gini entity")

The perceived corruption index is also correlated with the Panama address with 0.31385266422046715 and p value 8.235035924362218e-05. The correlation is lower with the the intermediary with 0.22905312295895672 and p value 0.02637461882225528. 
![country distribution](img/corruption_interm.png "gini entity")

The third index is the service exports (BoP,US dollars). With this we want to show that service countries have more entities and officers cited. In fact service countries have more money laundry and have more money transactions with the offshore countries. In fact there is a low correlation between the service exports and the officers with a correlation value of ```0.3544542144618415``` and p-value ```1.2191864422245798e-05```. 

![country distribution](img/service_officer.png "gini entity")

Since in the service exports we are more interested in the financial services we checked with the fourth index is the insurance and financial services as percentage of service exports. As expected the correlation is higher in this case with the officer countries with ```0.4102701171441421``` and p-value ```3.9620220677934937e-07```.

![country distribution](img/inssurance_officer.png "gini entity")

From the previous graph we saw that the origin countries are correlated with the corruption and the service exports. For this reason we plot the perceived corrution as a function of the service exports for each country and we find a correlation value of ```0.5458846576026938``` with p-value ```7.216328423040093e-13```. This may indicates that the service country are maybe more corrupted ones. 

![country distribution](img/service_corruption.png "gini entity")

The last index is the human development index  and there is a logarithmic correlation with the Panama entries, officers and intermediaries of around ```0.4207873006904997``` and p-value ```2.8349214305321715e-06```. 

![country distribution](img/hdi_officer.png "gini entity")

This means that the countries which are more developed appears more often in the papers. This result comes as a surprise, in the sense that we were expecting the less developed countries to be more cited. 

Finally we decided to check correlation with arguably the main reason behind transfering funds and properties to the fiscal paradise, namely the percentage of taxes on income. 

![country distribution](img/tax_officer.png "gini entity")

As expected we found a correlation, however it is smaller than what we tought with a correlation value of ```0.2490335967272295``` and p-value of ```0.018604013880805865``` between the tax percentage and the frequency of officers countries. 
Officers in countries with high taxes tend slightly more to evade taxes and put their money in fiscal paradises, but there are a multiplicity of factors to take into account, for examples bad governments have a higher chance of seizing properties and possessions.

Last but not least, from the following plot we can see that there are power players coming from almost all bins with a corruption index ranging from 0 to 100. Although we can notice that most of of the power players come from CPI indexes ranging from 25-50.

![country distribution](img/power_players_corruption_index.png "pagerank corruption")