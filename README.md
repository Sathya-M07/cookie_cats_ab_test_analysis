#Cookie Cats A/B Test Analysis

#Business Question
Should cookie cats move the first progression gate from level 30 to level 40?
Does moving the gate hurt player retention?

##Data 
-Source: Cookie cats mobile game A/B test dataset(kaggle)
-Sample Size: 90,189 users randomly assigned to gate_30 (control) or gate_40 (treatment)
-Metrics: Day-1 retention ,Day-7 retention,total game rounds played

##Method 
-Two proportion Z-test on retention_1 and retention_7
-95% confidence intervels for each group 
-Boostrap resampling (10000 iterations) to independently validate the z-test results
-Power analysis to confirm sample size was sufficient to detect the observed effect

##key findings
-Day-1 retention: No statistically significant difference between gate_30 and gate_40 (p=0.074)
-Day-7 retention: statistically significant difference (p=0.0016) -gate_30 retains more players than gate_40
-Results were confirmed independently via boostrap resampling 

##Recommendation 
-Keep the first gate at level 30. Moving it to level 40 does not improve short-term engagement and significantly reduces day-7 retention,indicating a negative long term impact on player engagement.

##Files
-'cookie_cats_ab_test_analysis.ipynb' - full analysis notebook
