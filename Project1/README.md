Project 1: Standardized Test Analysis

### Problem Statement

Mr. Abu recently got job offer and need to migrate to California, United States. His son, Samad just recently turn 17 years old and is migrating to US with him. Mr. Abu in dilemma to find best college to admit his son and how to secure place in that top flight college too. The goal of this survey is to find possible universities for Mr Abu’s son to enter with their requirement scores. This includes the best states with high entrance test scores to live in.

### Data Dictionary

#### ACT_2019 Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT_2019|List of states in United States| 
|participation|float|ACT_2019|Rate of participation in each state| 
|composite|float|ACT_2019|Mean of total ACT's subject marks for each state| 

#### ACT_2017 Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT_2017|List of states in United States| 
|participation|float|ACT_2017|Rate of participation in each state|
|english|float|ACT_2017|Total mean score of each state for english test| 
|math|float|ACT_2017|Total mean score of each state for math test| 
|reading|float|ACT_2017|Total mean score of each state for reading test|
|science|float|ACT_2017|Total mean score of each state for science test|
|composite|float|ACT_2017|Mean of total ACT's subject marks for each state|

#### SAT_2019 Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT_2019|List of states in United States| 
|participation|float|SAT_2019|Rate of participation in each state|
|ebrw|int|SAT_2019|Total mean score of each state for evidence-based-reading-and-writing test| 
|math|int|SAT_2019|Total mean score of each state for math test|
|total|int|SAT_2019|Mean of total SAT's subject marks for each state|

#### SAT_2017 Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT_2017|List of states in United States| 
|participation|float|SAT_2017|Rate of participation in each state|
|ebrw|int|SAT_2017|Total mean score of each state for evidence-based-reading-and-writing test| 
|math|int|SAT_2017|Total mean score of each state for math test|
|total|int|SAT_2017|Mean of total SAT's subject marks for each state|

#### SAT/ACT_BY_College Dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|school|object|SAT/ACT_BY_College|List of schools in United States|
|test_optional|category| SAT/ACT_BY_College|List of category of test for implying ACT/SAT test in school in United States|
|applicants|int|SAT/ACT_BY_College| Rate of applicant in each schools in US|
|accept_rate|int|SAT/ACT_BY_College| Rate of acceptance from total applicant in the US country|
|sat_total_25th_percentile|float| SAT/ACT_BY_College| Total median of 25th percentile of student that passed sat test in each schools in US|
|sat_total_75th_percentile|float| SAT/ACT_BY_College| Total median of 75th percentile of student that passed sat test in each schools in US|
|act_total_25th_percentile|float| SAT/ACT_BY_College| Total median of 25th percentile of student that passed act test in each schools in US|
|act_total_75th_percentile|float| SAT/ACT_BY_College| Total median of 75th percentile of student that passed act test in each schools in US|

### Summary of Project Analysis

Trend of each dataset is analysed. Some brief insight gain:
- Higher population is found to cause lower total marks of each test
- Higher tuition cost fees in a state tend to have better scoring marks
- Higher cost of living (reflecting higher income state) also  tend to have better scoring marks

### Conclusions And Recommendation
- at least median mark for scores to achieve
- high living cost is also associate with stricter n more achiever result in that area
-also choose school that is non optional test for higher chance
- low participant school show greater marks in each test.
- sat has higher particpation mean than act
- cost of tuition fees, living, participation, lowest & ideal scores mark are recommended features for new student to consider when selecting which entrance test to pick for which type of college.

### Resources Use in The Survey:
- Top rank universities. Does United States possess valuable & competitive universities?

    + source: https://www.mastersportal.com/ranking-country/82/united-states.html

- Cost of living in US's state (top 10)

    + source: https://meric.mo.gov/data/cost-living-data-series

- Average cost of college in US

    + source: https://educationdata.org/average-cost-of-college-by-state#:~:text=Massachusetts%20has%20the%20highest%20average,%2411%2C686%20per%20year%20on%20average.




