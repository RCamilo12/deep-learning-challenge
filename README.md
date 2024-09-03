# deep-learning-challenge

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll 

Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

We are using the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

- DATA PREPROCESSING
Our target variable was the IS_SUCCESFUL column, that has a value of 1 in case the campaign was successful and 0 in the other case. The remaining variables were out features, excepting for EIN and NAME that were dropped at the beginning of the process.

For optimization processes we also tried to drop STATUS and SPECIAL_CONSIDERATIONS as we thought this features were not neccesary in the model and could optimize the value of accuracy in one of our attempts to do so. 

- COMPILING, TRAINING AND EVALUATING THE MODEL
We were not able to acheive our goal for accuracy in the first case and that is why we tried to make optimization of the model, by:

1) Drop some columns: As said before STATUS and SPECIAL_CONSIDERATIONS were considered as non-important features.
2) Epochs changed to 70: We thought the model may have an overfitting problem because of the amount of data it has, so we decided to drop the epoch number a little to corroborate.
3) Changing the activation function to Leaky ReLU: We thought that maybe with some negative values that the model was not being able to indentify or process our accuracy was small. Therefore, we tried to change the activation function to Leaky ReLU, a function that has a range from -infinity to infinity and that is good to use when the data has  outliers, which could be the case in a huge dataset like the one we currently have.