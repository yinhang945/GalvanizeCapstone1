# NYC Legally Operating Businesses Analysis(Draft)

My analysis dives into the current NYC Legally Operating Businsses database. Does the number of new business licenses statisticaly significant drops this year compare to previous years?

* [Data Information](#data-information)
    * [Data Gathering](#data-gathering)
    * [Data Cleaning](#data-cleaning)
    * [Data Visulization](#data-vissulization)
* [Hypothesis Testing](#hypothesis-testing)
* [Conclusion](#conclusion)
* [Future Analysis](#future-analysis)

## Data Information
This data set features businesses/individuals holding a DCA license so that they may legally operate in New York City.DCA enforces the Consumer Protection Law and other related business laws throughout New York City. Ensuring a fair and vibrant marketplace for consumers and businesses, DCA licenses moe than 71,000 businesses in 57 different industries. Through targeted outreach, partnerships with community and trade organizations, and informational materials, DCA educates consumers and businesses alike about their rights and responsibilities.

### Data Gathering:
<p align="center">
  <img src="img/NYCOpenData.png">
</p>

Data used for this analysis was gathered from NYCOpenData website.---------

1)  Downloading:  The dataset was downloaded from NYCOpenData website.----- 
2)  Transform:  It was transformed into a clean pandas dataframe through custom functions, located on the ```src``` folder.
3)  Cleansing:  ------------- 

### Data Information:
Data used in the study included DCA License Number, Type(Individual/Business), License Creation/Expiration Date, Industry, and the localtion informations about the business, ie: City, Zipcode, and coordinate in NYC from April 2018 to September 2020.

### Hypothesis Testing:

###### Step 1: Set up the hypothesis
The null hypothesis is that the number of new DCA license created in 2020 has no statistically significant difference to the number of new DCA license created in 2018 and 2019.

Alternative hypothesis is that there is a significant difference to the mean value of new DCA License granted.

>**H0: μ = μ 0**

>**H1: μ ≠ μ 0**

###### Step 2: Select test statistic
To test this hypothesis the t-test was chosen.
The significance level was set at: 0.05

The Welch's t-test, does not assume the two populations from which the samples are drawn have the same variance.

<p align="center">
  <img src="images/z-statistic.png">
</p>

###### Step 3: Set up decision rule
Reject the null hypothesis if p-value is less than our threshold alpha=0.05.
<p align="center" style="width:10%" >
  <img src="images/normdist.png">
</p>

###### Step 4: Compute the test statistic
------------

![](images/z-score.png)

###### Step 5: Conclusion
Given the results of our test we conclude that we must reject the null-hypothesis.  There is enough evidence to say that the number of new DCA license being granted was dropped comparing to the number of new DCA license granted from the previous two years. 
The t-statistics of 14.678045591103883 with a p-value of 3.2720431903438374e-32 well below our 0.05 significance level. 

## Technologies
<p align="center">
  <img src="images/logos.png">
</p>

###### Database:
Data Storage: Mongodb<br>

###### Python:
Data Gathering: Beautiful Soup, Selenium<br>
Data Analysis: Python 3, Numpy, Pandas, Scikit-Learn, Scipy<br>

###### Visualization:
Data Visualization: Tableau, Folium, Matplotlib, Seaborn

## Future Improvements
• Enrich the dataset by continue to run scrapers over a 12 month-period.<br>
• Bring historic data to analyze market trends.<br>
• Incorporate size of all rooms in of all homes.<br>
