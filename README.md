# Missing_data_case_study
missing data case study

data:missing_data.csv
notebook: missing_data_case_study.ipynb

If we go by the books, the standard ways to deal with missing data are either:
Remove rows including missing values

Replace them with some value. This can be as easy as just using that variable average/mode, it can mean building a model to predict the missing value and replace it with the prediction, as well as countless small variations of those approaches. But at the end of the day, regardless of the actual approach we use to impute missing values, the idea is the same:

Replace them with the value that we think it was the most likely to happen if that value hadn’t been missing

In practice, none of those approaches would work if we are dealing with consumer data. Consumer data are full of missing values. Think about our profiles on FB, LinkedIn, Airbnb, etc. How many fields there are? And how many did we actually fill out? Anything that we did not fill out is a missing value in the corresponding table.

The high high majority of missing values in tech companies come from the fact that the user has chosen to not give that kind of information: by not filling out her profile, or by changing her privacy settings, or even by deleting her cookies. And that’s crucial information for our predictive model that we would lose, if we were replacing or deleting the missing values as above.

Therefore, the best way to deal with missing values is to code them as such in our dataset and use them throughout our analysis. If it is a categorical variable, just create a new level “missing”. If it is a continuous variable, replace the missing value with a very large/small number, clearly outside of the range of the variable, i.e. 10^9 or something like that. And then, use a model which is not affected by outliers, like for instance decision tree-based classifiers.

In this project I explored on how to deal with missing data.
