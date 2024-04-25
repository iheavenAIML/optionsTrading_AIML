_**Scope of the project / Research Question**_:

Under which circumstances an options trader should use a straddle trading strategy based on the Russell 2000 index performance and imminent market disruptions like FOMC announcements and other 'black swan' events?

Given the potential for high volatility and unpredictable outcomes associated with such events, the trader faces the challenge of determining whether to execute a straddle trade.

This decision hinges on analyzing historical correlations between the Russell 2000 and market disruptions, evaluating the magnitude of anticipated volatility, and assessing risk tolerance.

The trader must navigate the complex interplay of market forces to decide whether the potential gains from a straddle position outweigh the associated risks, ensuring informed and strategic decision-making in volatile market conditions.

_**Executive Summary** (work in progress)_:

make a Russell 2000 movement prediction:

the result of time series forecasting using a trained AutoRegressive Moving Average model suggests that the Russell 2000 index has been at the bottom of its range-bound oscillations since mid-2022 and it is due for upward movement in the next 21 weeks (see in-depth AI analysis here <link to notebook here>)

identify the most influential factors (independent variables) affecting Russell 2000 closing price (target variable):

it looks like 'Low' (theta = 0.998335), 'High' (theta = 0.998062), and 'Open' (theta = 0.995538) have the biggest impact on the 'Closing price’

using LinearRegression() model options traders will be able to predict the closing price of Russell 2000 index with MSE = 0.000593 which indicates good model performance<link <link to notebook here>

classify movement prediction as ‘move up’, ‘move down’, or ‘range-bound’

tbd

make an options trading strategy recommendation based on the predictors’ outcome

tbd


Please find an in-depth data analysis and AI modeling with the code base in the following file: <link to notebook here>

_**Key Steps Performed During Analysis**_:

1. we've explored the data by loading it and analyzing the dataset using functions like `head()`, `info()`, `describe()` among other Panda's build-in methods
2. we've examined each column individually to understand the type and relevance of data it contained
3. we've identified missing values (39 in total) in the dataset and imputed values based on domain knowledge and its potential impact on the analysis
4. we've looked into any inconsistencies, errors, or anomalies in the data (this could've included duplicate records, incorrect data types, inconsistent formatting, or unexpected values)
5. we've explored relationships between different features in the dataset by utilizing visualization techniques like scatter plots, histograms, and correlation matrices
6. we've incorporated financial markets domain knowledge to guide our exploration
7. and, finally we've kept track of our observations, findings, and any actions taken during the data exploration process and presented them in this very README.md

_**In conclusion** (work in progress)_:

tbd

Want to chat a bit more about the findings? Options trading? Have an opinion that may enhance the results? Let's definitely connect!

Sincerely,
Igor Heaven | (415) 596-4427
