# Final Project Group Formation and Data Check

## Group members

- Yuki Ikeda (UNI: yi2220)

- Zhenyu Yuan (UNI: zy2492)

## Questions

We want to deepen the insight given in the report by the Pew Research Center:

https://www.pewresearch.org/science/2019/11/25/u-s-public-views-on-climate-and-energy/

1. Although the survey pointed out supported parties as a relevant factor, are educations or incomes also related to the opinion toward climate change issues (ex. whether the climate change is due to human activities or just natural patterns in global climate)? We address this issue upon trying to control other relevant effects such as supported parties.
2. From the survey, it is seen that Democrats are more likely to say that the federal government is doing too little for key aspects of the environment, and Democrats are more likely to think the climate change is due to human activities. With respect to this, are Democrats (Republicans) also more (less) recognizing that the climate changes are affecting their local communities (no matter what the reason of the change is) in the first place? We address this issue upon trying to control other relevant effects such as regions.
3. From the survey, it is seen that majority of people think that they should decrease the oil drilling or coal mining, and they should increase natural electricity generations such as one by wind or land heat. However, their opinion is separate with respect to whether they should increase the new clear power plants (Yes:49% vs No:49%). Here, how do factors (sex, age, party, income, regions,…) relate to the choice Yes and No.
4. The survey includes some questions about the respondents’ personality. Is personality affecting one’s attitude towards climate changes and willingness to take actions to reduce climate change?
5. Has the public’s attitude towards climate change evolved over time? Does this change correlate with the change in election outcomes? Is it different across regions and groups?

 

## Database to be used

### American Trends Panel (ATP) by the Pew Research Center

https://www.pewresearch.org/american-trends-panel-datasets/

The Pew Research Center has been conducting nationwide randomized surveys on social issues for many years. Questions related to environmental issues include:

- The climate change is due to human activities or just natural patterns in global climate.
- The federal government is doing too little for key aspects of the environment.
- We should decrease oil drilling/ coal mining.
- We should increase natural sources of electricity generations.
- We should increase nuclear power plants.

It also includes basic attributes of respondents such as age, sex, political party, region, education and income, which enables us to connect those basic attributes to their opinion.

The sample size is large enough (N > 1,000), and so is the number of variables (100+ questions). Since it has weights assigned to each sample in order to modify the imbalance of attributes of respondents compared to some benchmark sources such as *Gender 2017 American Community Survey*, we can present unbiased aggregated figures.

Climate change is a frequent topic in the ATP, so we can make comparison over time. (A note: since respondents to different surveys are not the same, it’s an aggregation of cross-sectional data instead of panel data.)

### US Election Data

https://www.fec.gov/introduction-campaign-finance/election-and-voting-information/

This is released by the Federal Election Commission and contains each state’s votes to each candidate in each federal election.

## How to answer the questions above using the data

- For question 1, the existing report above suggests the strong relationship between a party one supports and his/her opinion. Hence, we should control parties, when we conduct an analysis for this question. Here, this data is useful since we can calculate for each party whether there is a firm relationship of opinion toward each climate change issue with their incomes or educations.

- For question 2, the existing report above suggests people living in the Pacific region are more likely to experience some climate change. Here, it is known that there are more Democrats in the Pacific region. Hence, we should control regions, when we conduct an analysis for this question. This is where this data comes in since for every region we can calculate the proportions of those who are recognizing that the climate change is affecting their community among each party, comparing the proportions of the two parties in each region. 

- For question 1 and 2, we can also perform the statistical test of the difference of ratios.

- For question 3, we can calculate and compare the proportions of Yes and No for each candidate factor such as sex, age, party, income and regions. We can also conduct the chi-squared t tests to add independent analyses.

- For question 4, we can utilize the data from ATP Wave 33 (Apr 2018), Wave 55 (Oct 2019), and Wave 67 (Apr 2020), which contain similar questions about climate change. We can use parcoords to illustrate the change across time.
- For question 5, since Waves 33 and Wave 67 are conducted on elections years, we can relate them with the outcomes of the elections. We can use a difference-in-difference method to check whether there's a correlation between the change in attitude towards climate change and the change in election outcomes. We can further analyze by region or by demographic factors.

 