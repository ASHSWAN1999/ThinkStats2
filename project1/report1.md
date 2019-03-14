# Age and Generation Affect Happiness Levels in Marriage… A Little 

### By Ashley Swanson


In the past hundred years, countless variables have changed surrounding the attitudes, frequencies, and constructs of marriage. So, what does this mean for happiness levels of marriages throughout time? 

With higher divorce rates in recent years, we might expect there to be higher rates of happiness among those that remain married. The legalization of gay marriage may also add to an upward trend in marriage happiness, along with first marriages happening later in life, which may imply that individuals are putting more thought into compatibility. Alternatively, lower rates of marriage over time could indicate a growing negative climate towards marriage, reflected in lower levels of happiness. And gender roles have shifted dramatically over the decades, which could have had any number of effects. To observe the cumulative results of all of these changes, we can use data analysis to gather insight on trends in marital happiness. 

Let’s start by examining the general trend of happiness over time. I will be examining the Happiness in Marriage variable from the General Social Survey (data collected by NORC at the University of Chicago). The survey asked respondents from 1971 to present the following question:

>Taking things all together, how would you describe your marriage? Would you say that your marriage is very happy, pretty happy, or not too happy?

Across the entire dataset, 63% of people said they were very happy, 34% said pretty happy, and 3% said not too happy. Accordingly, we will plot year against the percentage of people survey in that year that marked “very happy”. Here’s the plot.

_Figure 1: Happiness in Marriage Over Time_

![Minion](https://github.com/ASHSWAN1999/ThinkStats2/blob/master/project1/fig1.png)


This model shows a statistically significant negative trend, with a pvalue under 0.01. The effect size is quite small given that the percentage of reported happy marriages decreases by 0.13% per year. This means that over the course of 30 years, reported happiness levels have decreased by about 4%. An rsquared value of 0.367 tells us that roughly a third of the effect on marital happiness can be explained by the year in which a respondent answered.  

So clearly there is a trend present over time, but it truthfully isn’t hugely impactful. However, there are other factors that can vary with time that might affect marital contentedness, such as the age of a respondent when they answer the question. 

As people go through life, they have different experiences that might improve or deteriorate their relationships. For example, the honeymoon phase is much less strenuous than a couple that has three kids they have to look after. Couples may be prior to getting a promotion at work that sucks up their spare time. Of course these timelines vary for everybody, and not every couple shares the same experiences. But analyzing the percentage of reported “very happy” marriages against the ages of the respondents seems like a good way of identifying trends. 

_Figure 2: Happiness in Marriage vs Age_

![Minion](https://github.com/ASHSWAN1999/ThinkStats2/blob/master/project1/fig2.png)


Figure 2 suggests a significant relationship between age and marital happiness wherein reported happiness levels decrease until the early 40's and increase again from there. There is likely more noise in extreme ages due to a smaller number of respondents. To quantify these tendencies, we will split the data into two sections: respondents 42 and under, and respondents over 42. 

_Figure 3: Happiness in Marriage vs Age: 42 and Under_

![Minion](https://github.com/ASHSWAN1999/ThinkStats2/blob/master/project1/fig3.png)


The effect size of this trend is about -0.45%, meaning that over the course of these two decades nearly 10% fewer respondents report happy marriages. It is important to note that, while age is the variable being tested, these other life-event based variables, such as birth of children and career progression, are much more likely to cause the trend than age itself. An rsquared value of 0.316 means that nearly a third of variability in happiness is explained by age for those 42 and under. 

_Figure 4: Happiness in Marriage vs Age: Over 42_

![Minion](https://github.com/ASHSWAN1999/ThinkStats2/blob/master/project1/fig4.png)


The upward trend past 42 has a smaller effect size of about 0.2% per year. So, over the course of 4 decades, there is an 8% increase in happiness levels compared to those at age 42. While this growth rate is about half the size of the decay rate before age 42, it is sustained for over 40 years, causing total happiness levels to nearly rebound from the negative effects of the first 20 years. The rsqaured value, 0.424, indicates that age becomes a more substantial indicator of marital happiness beyond early 40’s.

The downfall of this model is that 60-year-olds surveyed in 2018 are lumped in with 60-year-olds surveyed in 1971, and these people may have had very different experience with marriage than their predecessors. One way to get at this is by examining marital contentedness based on the year people were born, known as their cohort. This helps to reveal generational trends. 

_Figure 5: Happiness in Marriage vs Cohort_

![Minion](https://github.com/ASHSWAN1999/ThinkStats2/blob/master/project1/fig5.png)


The extreme noise on the upper and lower bounds suggest that there is not enough data before 1900 and after 1990 to analyse these years. Therefore, we will zoom in to analyse years with more data points.

_Figure 6: Happiness in Marriage vs Cohort: Quadratic Fit_

![Minion](https://github.com/ASHSWAN1999/ThinkStats2/blob/master/project1/fig6.png)


Visually, the quadratic model explains the relationship between cohort and happiness in marriage very well. The effect size has a heavy overall downward trend of -19.9% per year and a quadratic coefficient of 0.005% per year. In human terms this means that those born in 1900 reported happiness levels 13.3% higher than those born in 1950. After 1950, percentages started slowly climbing again, rebounding by about 10.5% by 2000. An rsquared value of 0.444 tells us that the year one was born has the most explanatory power among time, age, and cohort.
