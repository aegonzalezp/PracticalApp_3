## Practical Application No. 3 Summary

#### Overview
The business objective is to produce a model to predict if a customer will subscribe a bank 
time deposit. The model should ideally yield interpretable results.

The exercise objective is to compare the performance of the results of k-nearest neighbors, 
logistic regression, decision trees, and support vector machines.

#### Dataset
Our dataset comes from the UCI Machine Learning repository. The data is from a Portugese banking 
institution and is a collection of the results of multiple marketing campaigns. 

URL: https://archive.ics.uci.edu/dataset/222/bank+marketing

The dataset has 41,188 rows with 20 attributes and 1 target. The target is binary being no or yes.

#### Data
The data directory contains two (2) data files in csv format

- bank-additional.csv : Full sample dataset, ordered by date (from May 2008 to November 2010)
- bank-additional-full.csv : 10% of samples (4119), randomly selected from Full sample dataset

The file bank-additional-names.txt contains dataset background information and dataset features
descriptions.

## Summary of findings
Utilized CRISP-DM METHODOLOGY to produce a model to predict if a customer will subscribe 
a bank time deposit. The model should ideally yield interpretable results.  Used four (4) 
different classifiers [k-nearest neighbors, logistic regression, decision trees, and 
support vector machines] to measure performance and results based on accuracy.

| model | Train Time | Train Accuracy | Test Accuracy |
| ----- | ---------- | -------------- | -------------- |
| LogisticRegression | 1.929807 | 0.900142 |0.899571 |
| KNN | 0.109848 | 0.914363 | 0.890669 |
| Decision Tree | 0.235368 | 0.995595 | 0.833697 |
| SVC | 9.677039 | 0.897818 | 0.896820 |
| LogisticRegression Optimize | 17.806170 | 0.900628 | 0.898276 |
| KNN Optimize | 279.344610 | 0.905172 | 0.895849 |
| Decision Tree Optimize | 220.261254 | 0.889008 | 0.890750 |
| SVC Optimize | 615.981198 | 0.897818 | 0.896820 |

Not a significant difference in accuracy between the basic models vs the optimize models. Base 
on our goal to select the best prediction model with ideally interpretable results; the best 
model would be Decision Tree Optimize Model. This model had the second best fit time, optimize 
accuracy is at 89% like the other models, and the results are interpretable by analyzing the 
decision tree.  According to the decision tree the more relevant features are nr.employed, previous 
and month. 

## Next steps
None of the Bank Client data features were important for the prediction.  The decision tree results 
suggest that the campaign acceptance has more to do with call center percitance and customer follow up. 
I find this intriguing and merits further analysis just to define feature importance as it relates 
to campaign acceptance (y). An option would be to perform a Permutation Importance analysis.

### Notebook URL
https://github.com/aegonzalezp/PracticalApp_3/blob/main/prompt_III_AlvaroGonzalez.ipynb




