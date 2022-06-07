### deep-learning-challenge 
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
    <li>dividing the data into a target array (IS_SUCCESSFUL) and features arrays,
    <li>applying the `train_test_split` to create a testing and a training dataset,
    <li>and finally, using `StandardScaler` to scale the training and testing sets
    </ul>
<br>
more words


RESULTS:<br>
The <b>first model</b> was run with the bin cutoffs for APPLICATION_TYPE at 600 and CLASSIFICATION at 300<br>
The model with layer1 = 9 and layer2 = 15 had Loss: 0.5511097075501267, Accuracy: 0.7269970774650574<br>
The model with layer1 = 10 and layer2 = 13 had Loss: 0.5513412412610068, Accuracy: 0.7289795875549316<br>
<br>
A loss value of 55 indicates that the model can be further optimized. The accuracy percent shows that 72% of the model's predicted values align with the true values in the original dataset.
<br>
<br>
<br>
<i>To see if I can get closer to 75% accuracy I am going to change the cutoff for the bins.</i><br>
The <b>second model</b> was run with the bin cutoffs for APPLICATION_TYPE at 800 (added two application types to "other") and CLASSIFICATION at 1000 (added one classification to "other")<br>
The model with layer1 = 9 and layer2 = 15 had Loss: 0.5580132460038099, Accuracy: 0.7246647477149963<br>
The model with layer1 = 10 and layer2 = 13 had Loss: 0.5558303427765737, Accuracy: 0.724781334400177<br>

Again, a loss value of 55 indicates that the model can be further optimized. The accuracy percent shows that 72% of the model's predicted values align with the true values in the original dataset.
<br>
<br>
<br>
<i>To see if I can get closer to 75% accuracy I am going to change the cutoff for the bins and change the number of nodes.</i><br>
For the <b>third model</b> was run with the bin cutoffs for APPLICATION_TYPE at 500 (removing several application types from "other") and CLASSIFICATION at 100 (removing several classification from "other")<br>
The model with layer1 = 9 and layer2 = 18 had Loss: 0.5513618771953416, Accuracy: 0.7262973785400391<br>
<br>
<br>
<br>
<i>To see if I can get closer to 75% accuracy I am going to add another hidden layer.</i><br>
For the <b>fourth model</b> was run with the bin cutoffs for APPLICATION_TYPE at 500 and CLASSIFICATION at 100.<br>
The model with layer1 = 9, layer2 = 18, and layer3 = 27 had Loss: 0.551749932981441, Accuracy: 0.7261807322502136<br>
<br>
<br>
<br>

## My Code
* VSCode: 