## Analyzing nationwide SAT and ACT scores in view of participation rates

### Problem Statement
Our town mayor is looking to improve the educational outcomes for high school graduates. This is a very broad directive, and so to narrow the scope of inquiry I chose to use nationwide SAT and ACT score and participation data for each state to inform an assessment of how well a given state is performing.  I sought to determine how participation rate might associate with score and then identify states that are performing either particularly well or particularly poorly so that the characteristics and policies of these states can be examined in greater detail.

## Executive Summary
After loading the data, I made a thorough investigation of it and removed rows with missing values, corrected incorrect entries based on the source data found on the College Board's website, and otherwise readied the data for numerical analysis and visualization.  With the ACT and SAT data thus formatted I merged the two datasets to allow for simultaneous analysis.  Next I produced a data dictionary  for the reader's reference, with updates later on as I added derived features according to my curiosity.  After that, I proceeded to investigate the basic numerical and statistical properties of each feature, looked at relationships between features, and generated aggregates such as the mean value across years for like features for each state.  I also inspected within state year over year changes.  To get a better visual grasp of distributions and relationships, I made a number of graphs.  These graphs allowed for the identification of states that can be the targets of further inquiry and research. 

### Data Dictionary
Below is a dictionary of the merged dataframe that served as the basis for my inquiry.
|Feature|Type|Dataset|Description|
|---|---|---|---|
|State|object|test_df|The state to which the observations pertain|
|2017_ACT_Participation|float|test_df|Proportion of the state's 2017 HS graduates who took the ACT| 
|2017_SAT_Participation|float|test_df|Proportion of the state's 2017 HS graduates who took the SAT|
|2017_ACT_Score|float|test_df|Mean ACT Composite score of the state's 2017 HS graduates|
|2018_ACT_Score|float|test_df|Mean ACT Composite score of the state's 2018 HS graduates|
|2019_ACT_Score|float|test_df|Mean ACT Composite score of the state's 2019 HS graduates|
|2017_SAT_Score|float|test_df|Mean SAT Total score of the state's 2017 HS graduates|
|2018_SAT_Score|float|test_df|Mean SAT Total score of the state's 2018 HS graduates|
|2019_SAT_Score|float|test_df|Mean SAT Total score of the state's 2019 HS graduates|
|ACT_Score_Avg|float|test_df|Mean of statewide ACT scores across 2017, 2018 and 2019|
|SAT_Score_Avg|float|test_df|Mean of statewide SAT scores across 2017, 2018 and 2019|
|ACT_Part_Avg|float|test_df|Mean of statewide ACT participation across 2017, 2018 and 2019|
|SAT_Part_Avg|float|test_df|Mean of statewide SAT participation across 2017, 2018 and 2019|

### Main Points, Findings, and Results
Over the course of my exploration of the data, it quickly became clear that participation rate has an inverse relationship with test score.  This consistent relationship suggests that it is the better prepared students who are motivated to take the less popular exam in an effort to optimize their chance of admittance to their desired institution.  It is seen very clearly in a year to year anlaysis of ACT score changes within each state.  SAT scores generally did not change nearly as much and so it is less easy to discern the within state relationship between score and participation.  The advantage the 100% participation rate states have is not having to worry about selection bias thwarting analysis of the state's educational progression or regression.

This study reveiled a few states that are worth investigating to determine if any actionable steps can be taken to improve educational outcomes for the town's students.  From the analysis of ACT scores, Wisconsin with 20.43, Utah with 20.33, Montana with 20.03, Kentucky with 20.00, and Wyoming with 20.00 are all worth investigating for their comparatively solid scores, while Nevada's low average score of 17.8 beckons inquiry as a negative example.  

For the SAT, there were fewer states with extremely high participation.  However, New Hampshire's score of 1058 (.96 participation) and Connecticut's score of 1047 (full participation) are notable.  In contrast, the Distric of Columbia's SAT average score of 967 (.95 participation) could be useful as a negative example.

I chose to use the average of three years of test scores in identifying the above states as there will be inherently less variation in the scores.

### Observations and Conclusions
I have identified a key relationship between participation rates and average test score results.  Viewing the data all together, the higher a state's participation on an exam, the lower the score on that exam.  Thus, conclusions can only readily be drawn from data for states with full participation.  Otherwise there is likely a pronounced selection bias, where less motivated students forego taking the exam.  I conclude that it would be beneficial to require exam participation for graduating high school seniors.  Only then can reliable data be gathered and analyzed for the purpose of tracking educational outcomes.

### Next Steps
From our present analysis, I believe futher research should be made into what underlies the success and failure of the previously mentioned states -- Wisconsin, Utah, Montana, Kentucky, Wyoming, Nevada, New Hampshire, Connecticut, and the Distric of Columbia.

### Bibliography
https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows -- ACT Score and Participation 
https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/ -- SAT Score and Participation

