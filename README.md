# deep-learning-challenge 
# Charity Funding Predictor

### This assignment was to create an algorithm to predict whether or not applicants for funding will be successful if funded by a ficitional non-profit foundation.
----------------------------
----------------------------

## Process
I was given a CSV file that I read into Pandas. This file contained more than 34,000 organizations that have received funding from the fictional foundataion along with several columns of metadata about each orginazation.
<br>
<br>
I preprocessed the data by:
    <ul><li>dropping non-beneficial columns,
    <li>finding the number of data points for each unique value for each of the columns that had more than 10 unique values - APPLICATION_TYPE and CLASSIFICATION,
    <li>choosing a cutoff point of 600 and 300, respectivley, to bin rare categorical values together into a new value called "Other",
    <li>using `pd.get_dummies()` to convert categorical data to numeric,
    <li>divided the data into a target array (IS_SUCCESSFUL) and features arrays,
    <li>applying the `train_test_split` to create a testing and a training dataset,
    <li> and finally, I used `StandardScaler` to scale the training and testing sets
    </ul>

<br>
more words

## My Code
* VSCode: 