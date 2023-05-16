# deep-learning-challenge

Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

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


Overview of the analysis
The purpose of this analysis is to create a binary classifier to predict whether applicants will be successful if funded by Alphabet Soup. 

Results
•	Data Preprocessing
o	“IS_SUCCESSFUL" is the target for my model
o	Features for my model: “APPLICATION_TYPE”, “AFFILICATION”, “CLASSIFICATION”, “USE_CASE”, “ORGANIZATION”, “STATUS”, “INCOME_AMT”, “SPECIAL_CONSIDERATIONS”, “ASK_AMT”
o	“NAME” and “EIN” should be removed from the input data because they are neither targets nor features. 
•	Compiling, Training and Evaluating the Model
o	80 and 30 Neurons, 2 hidden layers and 2 activation functions I selected for my neural network model, set application counts and classification counts less than 1000. I was not able to achieve the target model performance. The accuracy is only 72.4%
o	I then only removed “EIN”, add one layer and set units equal to 5, activation is relu, and add an output layer and set units equal to 1, activation is sigmoid, epochs is 50. The accuracy is over 75%. 
o	I also tried to remove “NAME”, using 4 layers (300, 200, 100, 50 neurons) and set activation functions equal to relu, set application counts and classification counts less than 300, set apochs equal to 200 but the accuracy is only 72.7%.
o	I also tried to remove “EIN”, set application counts and classification counts less than 300, using 5 layers (400, 300, 200, 100, 50  neurons) and set activation functions equal to relu, set apochs equal to 50. The accuracy is 79%

Summary
	It appears that keeping the “NAME” column is very important in achieving the target. This means choosing the dataset before preprocessing is very import. When I run apochs less than 100, it works well and spent less time running the results. Getting more layers and neurons also help getting a higher accuracy. 
