_**Scope of the Project / Research Question**_:

Under which circumstances an options trader should use a straddle trading strategy based on the Russell 2000 index performance and imminent market disruptions like FOMC announcements and other 'black swan' events?

Given the potential for high volatility and unpredictable outcomes associated with such events, the trader faces the challenge of determining whether to execute a straddle trade.

This decision hinges on analyzing historical correlations between the Russell 2000 and market disruptions, evaluating the magnitude of anticipated volatility, and assessing risk tolerance.

The trader must navigate the complex interplay of market forces to decide whether the potential gains from a straddle position outweigh the associated risks, ensuring informed and strategic decision-making in volatile market conditions.

_**Executive Summary | Recommendations**_:

AI modeling and Data Analysis point directly to the following recommendations:
1. options traders should establish a long straddle position on the Russell 2000 index on the eve of the FOMC announcement, preferably 2-3 trading days in advance (the calendar of FOMC announcements can be viewed [here](https://www.federalreserve.gov/monetarypolicy/fomccalendars.htm))
2. the most closely watched impactful features should be "Range" and "Volume" of Russell 2000; it appears that the trigger threshold lays @ $6B trading volume - this is when moves 'up' and 'down' occur with significant volatility which offsets the price of establishing the straddle trade
3. one of the side observations revealed that the move 'down' is much more volatile than the move 'up'
4. in the majority of cases (81%) data is 'range-bound' and that suggests selling a straddle or strangle ... please find a detailed [analysis and code base here](https://github.com/iheavenAIML/optionsTrading_AIML/blob/main/optionsTrading_classification_russell2000_frequency_B.ipynb)
5. furthermore, out of four AI models used for the classification of index' move 'up', 'down', or 'range-bound' (KNeighborsClassifier, LogisticRegression, DecisionTreeClassifier, and Support Vector Machines) we recommend using the LogisticRegression model for predicting Russell 2000 directional movement
6. taking into account the end date of the available data (March 15, 2024) the result of time series forecasting - using a trained AutoRegressive Moving Average model - suggests that the Russell 2000 index has been at the bottom of its range-bound oscillations and is due for an upward movement [see in-depth AI analysis here](https://github.com/iheavenAIML/optionsTrading_AIML/blob/main/optionsTrading_timeSeries_russell2000_frequency_B.ipynb); looking at the Russell 2000 performance during the last several weeks seems to confirm the accuracy of prediction
7. overall, it appeared that the 'Low' (coefficient|weight = 0.211425), 'High' (coefficient|weight = 0.211729), and 'Open' (coefficient|weight = 0.575283) features of the dataset have the biggest impact on the 'Closing price’
8. lastly, should the prediction of the Russell 2000 closing price become a task for an option trader, then using LinearRegression model will adequately address this undertaking... please see [the following AI usage](https://github.com/iheavenAIML/optionsTrading_AIML/blob/main/optionsTrading_linearRegression_russell2000_frequency_B.ipynb) for closing price prediction

_**Key Steps Performed During Analysis**_:

1. we've explored the data by loading it and analyzing the dataset using functions like `head()`, `info()`, and `describe()` among other Panda's built-in methods
2. we've examined each column individually to understand the type and relevance of data it contained
3. we've identified missing values (39 in total) in the dataset and imputed values based on domain knowledge and its potential impact on the analysis
4. we've looked into any inconsistencies, errors, or anomalies in the data (this could've included duplicate records, incorrect data types, inconsistent formatting, or unexpected values)
5. we've explored relationships between different features in the dataset by utilizing visualization techniques like scatter plots, histograms, and correlation matrices
6. we've incorporated financial markets domain knowledge to guide our exploration
7. and, finally we've kept track of our observations, findings, and any actions taken during the data exploration process and presented them in this very README.md

_**In conclusion**_:

The performed AI modeling and data analysis points to establishing a long straddle position on the Russell 2000 index before FOMC announcements. Key indicators include the "Range" and "Volume" of the index, with significant moves occurring around a $6B trading volume. LogisticRegression is advised for predicting index 'up', 'down', and 'range-bound' movements. Time series forecasting suggests an upward trend for the index, and LinearRegression is effective for predicting closing prices. Detailed analyses and code are available in the provided links.

Want to chat a bit more about the findings? Options trading? Have an opinion that may enhance the results? Let's connect!

Sincerely,
Igor Heaven | (415) 596-4427
