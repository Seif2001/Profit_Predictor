# Corporatica_MLIntern_Seifeldin_Elshabshiri

# Table of Contents

1. [Description](#desc)
2. [Approach](#app)
3. [Chosen Architecture](#arch)
3. [Steps](#steps)
4. [Results and Remarks](#randc)
5. [Time](#time)


<a name="desc"></a>
## Description
In this project, I created a deep learning model using tensorflow that takes 329 parameters or features as inputs and the output is the profit. This is a binary logistic regression problem, because the output column was turned into a binary output, instead of real numbers, in which if the output was above 15 it would be 1 and if it is less than 15 then it is 0.

<a name="app"></a>
## Approach
In this project the output is a binary number, either 0 or 1, so logistic regression was chosen as the architecture for this solution. We first prepare the data, then split the data into training and testing sets, then train on the training set, and then see how we did using the testing set.

<a name="arch"></a>
## Chosen Architecture
Because this is a binary problem, a logistic regression architecture was chosen. This was accompanied with a sigmoid as the acitvation function, and a binary cross entropy as the loss function. In addition, 2 dense layers were added, I found that this gave a better accuracy and loss then just having 1 dense layer. The archiecture of the model is similar to the one in the photo, however with one extra dense layer before the output.
![arch](https://carpentries-incubator.github.io/ml4bio-workshop/assets/logit_nodes.png)  


<a name="steps"></a>
## Steps
1. To start, data wrangling and preperation had to be done. First we check if there area any NaN values in the enire dataset, there were none.
2. Next I looked for columns that had categorical values, this was tested by checking the unique values of each column, if they were greater than 2 and less than 10 then I took them as categorical columns.
3. Next I turn the selected columns into a one hot encoding of each category.
4. Next I checked the correlation of each column with each other, then took only the correlation of each column to the output colun then ranked them based on the highest correaltion to the lowest.
5. Now the data is ready, so we split the data into the X columns, the input columsn, and y column, the ouptut column.
6. We further split the data into a validation, test and train sets, in which 75% of the data is training data, 12.5% is validation data and 12.5% is test data.
7. We define the model having an acivation function of sigmoid, because the output is 0 or 1, 1 dense layers, one that takes all the parameters as the input and outputs 1 number, and the adagrad function as the optimizer.
8. Then we train the model with a binary corss entropy as the loss function, again because it is a binary logisitic regression problem.

<a name="randc"></a>
## Results and Remarks
The model had an optimal accuracy of 95%, this was tested on the test data, which was new data that the model had never seen before.

Remarks: Experimenting with the hyperparameters can result in a better accuracy, however this is the best accuracy that I found while experimenting myself.

<a name="time"></a>
## Time
The whole project took around 4 hours to complete and was completed in the span of 2 days.
The data preparation took around 2 hours and the training also took around 2 hours.
