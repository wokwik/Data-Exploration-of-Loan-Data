# (Dataset Exploration Title)
## by (Salih Alborno)


## The Dataset

This analysis is carried out on a loans data set from Prosper.

- The data set contains 113,937 loans with 81 variables representing features collected on those given loans, such as loan amount, borrower rate (or interest rate), current loan status, borrower income, borower rate, estimated return, effective yield, and many more.

- The dataset is divided into two periods; pre Jul 2009 and post Jul 2009. This analysis focused on post Jul 2009. This is because post Jul 2009 data set includes extra set of metrics such as Estimated Return, and Estimated Loss and using various borrower scoring and ratings algorithms which can help in loan analysis. Also post Jul 2009 data set is a much longer period spanning 6 years vs 2 years for pre Jul 2009 period. 

- The data set was first explored by identifying a number of key questions:
    1 - What factors affect a loan’s outcome status?

    2 - What affects the borrower’s APR or interest rate?

    3 - What determines returns amount for lenders?

    4 - Are there differences between loans depending on how large the original loan amount was?

- Given the lack of data on declined/rejected loans, question 1 was deemed out of scope. Also, our analysis around loan amount was parked aside in favour of investigating questions 2 and 3, where there where the analysis revealed some interesting findings.


## Summary of Findings

The exploratory analysis found in uda_Part_I_exploration_submit.ipynb explored many aspects of the data set and used many visulisations to determine which features in the data influence LenderYield and EstimatedReturn. There were some dead ends and also there were many findings along the way. For this summary, we have chosen key explorations and visulisations that highlight key observations, which are summarised in this list:

- The loan company made changes over time, where 36 month term loans were offered first, then 12 months and 60 months term loans were introduced in Nov 2010.

- Debt Consolidation was found to be the most popular loan category by large, followed by Home Improvement and Business categories.

- 12 months loans were found to be less profitable than 36 months and 60 months term loans and were stopped in Apr 2013.

- Lenderyield and EstimatedRetrun are found to increase as ProsperRating (Alpha) and ProsperScore worsened. A large number of Hight Risk loans (HR) were at 0.3 LenderYield.

- EstimatedLoss and EstimatedEffectiveYield are found to have changed over time, where in 2009-2010 were calcualted based on fixed offset values assigned according to ProsperRating (Alpha) and ProsperScore levels. Since then, the offset seems to have been depricated, in favour of a more direct linear relationship.  

- AverageEstimated Return reached its highest value (0.115) in 2011, but declined since then to reach its lowest ever value (0.072) in 2014.


### Key Insights for Presentation

This is a list of key insights gleaned from the data with some details:

### Focusing on post Jul 2009 data

- Examining the data set revealed that post Jul 2009 have rich set of metrics such as Estimated Return, Estimated Effective yield and Estimated Loss and have various borrower scoring and ratings scales used in loan analysis when compared to compared to pre Jul 2009 data.

- Also, pre Jul 2009 data covers a shorter span than post Jul 2009, where post Jul 2009 data set covers 6 years vs 2 years for pre Jul 2009 data set. 

- Therefore, our analysis will focus on the post Jul 2009 data set to glean relationships and insights on loan metrics used for determining rates and ROI.

### Loan Terms by Year

- The data shows that 36 months loans have been since the begining, however 12 months and 60 months loans were introduced in Nov 2010.

- While 60 months loans continued to 2014, 12 months loans seem to have been stopped in Apr 2013.

- This, again, confirms that focusing on Post Jul 2009 data for this analysis of data is more sensible.

### LenderYield vs EstimatedReturn

- EstimatedReturn have narrow spread of values, when compared to LenderYield values have wider spread of values when compared to EstimatedReturn.

- 12 months term loans are found to be less profitable than 36 and 60 months term loans.

- 36 months term loans are found to have some loans with negative EstimatedReturn, which is not the case 12 and 60 months term loans.

### Loan Categories

- Debt Consolidation is the most popular loan category by a large degree.

- Ignoring "Other", Home Improvement and Business are the next two most popular loan categories consecutively.

### Prosper Rating (Alpha) influence on LenderYield

- LenderYield are found to increase as the ProsperRating (Alpha) worsened.

- A large number of High Risk (HR) Loans are shown to have LenderYield at 0.3 causing a large peak to appear at 0.3 in the LenderYield Histogram plot.

### ProsperRating (Alpha) influence on EstimatedReturn

- EstimatedReturn are found to also increase as the ProsperRating (Alpha) worsened.

### High Risk Loans Anomality

- High Risk Loans are all found to be be awarded 30 months terms only

### LenderYield by Category

- All Categories are shown to have LenderYield increase as ProsperRating (Alpha) worsens.

- Debit Consolidation Category is by large the most common loan type, followed by much smaller nubmer of loans awarded to Home Improvement and Business categories.

- There are a significant number of uncategorised loans, which are assigned to the category "Other".

### EstimatedReturn by Category

- All Categories are also shown to have EstimatedReturn increase as ProsperRating (Alpha) worsens.

### ProsperRating (Alpha) Influence on Loan Metrics

- EstimatedLoss is found to be directly related to ProsperRating (Alpha) levels.

- Distinct horizontal plot bands in the EstimatedLoss plot are directly associated with different ProsperRating (Alpha) levels.

- Also groups of diagonal bands of data are correlated with the ProsperRating (Alpha) levels.

### ProsperScore Influence on Loan Metrics

- ProsperScore is also shown to have a direct influence on EstimatedLoss, EstimatedEffectiveYield, and thus EstimatedReturn.

- The horizontal rows in the EstimatedLoss plot and the diagonal rows in the EstimatedEffectiveYield are found to correspond to ProsperScore levels.

### CreditScoreRangeLower Scale on Loan Metrics

- LenderYield and EstimatedLoss are found to be impacted by CreditScoreRangeLower levels, where their values gradually increased as ProsperScore levels worsened.

- This is also reflected on the derived EstimatedEffectiveYield and EstimatedReturn, where a gradual change is observed in the plots due to CreditScoreRangeLower levels.

### Loan Terms Differences

- 12 and 60 months Term loans form diagonal swarm of data, and therefore are governed by an incremental increase of EstimatedLoss instead of fixed bands of horizontal points.

- 36 months Term loans seem to have both incremental diagonal plot swarm and fixed horizontal plot bands in the EstimatedLoss plot.

- 36 months Term loans have loans with negative EstimatedEffectiveYield and EstimatedReturn whilest 12 and 60 months Term loans have only positive EstimatedEffectiveYield and EstimatedReturn.

### Yealy Differences (I)

- 2009-2010 years are associated with the fixed EstimatedLoss values,that is associated with PropserRating (Alpha) and ProsperScore levels, shown as horizontal bands and rows.

- 2011-2014 years are associated with the incremental EstimatedLoss values,that is associated with PropserRating (Alpha) and ProsperScore levels, shown as diagonal swarm.

- 2009-2010 years have loans with negative EstimatedEffectiveYield and EstimatedReturn, whilest 2011-2014 have loans with only positive EstimatedEffectiveYield and EstimatedReturn.

### Yealy Differences (II)

- Overall, higher BorrowerRate is associated with lower ProsperRating (Alpha) levels.

- Inspecting each year separately shows different characterstics in the EstimatedLoss, EstimatedEffectiveYield, and EstimatedReturn plots.

    - In years 2009 and 2010, EstimatedLoss and EstimatedEffectiveYield values are adjusted to fixed levels according to ProsperRating (Alpha), thus resulting into distinct bands and rows in the plots that contributed to large variance in their values.

    - In years 2011 to 2013 EstimatedLoss and EstimatedEffectiveYield are adjusted to fixed levels according to ProsperRating (Alpha) levels but with much lesser variance, which eliminated negative EstimatedReturn loans.

    - The plots show year 2014 have a perfectly linear BorrowerRate vs EstimatedLoss and EstimatedEffectiveYield plots, where they increased in a linear fashion as ProsperRating (Alpha) worsened with nearly zero variance, which also eliminated negative EstimatedReturn loans. 

### Avg EstimatedReturn by Year

- The changes observed above seem to have caused loans' EstimatedReturn to reach its highest value (0.125) in the year 2011,

- But it has decreased since then and dropped sharply after 2012 to reach its lowest value in 2014 (0.085).

