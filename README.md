# hw_m13_venture_capital_funding

This file analyzes Alphabet Soup's Venture Capital records to build a binary classifier neural network model that will help predict successful ventures in the future.

It begins by importing the required libraries and dependancies, and then the csv containing all of the firm's previous investments. Datatypes of the columns are examined, then name and EIN columns are dropped, as they are unimportant to the analysis.

![CSV import](/Images/1.PNG)

![Column dtypes](/Images/2.PNG)

In order to use the `Object` data-type columns, they are assigned to a variable which is fit/transformed using OneHotEncoder, and finally used to create a dataframe with the new encoded variables. From the original dataframe, these variables are dropped, and the new encoded dataframe is concatenated to it to produce a single dataframe containing all of the data necessary for the neural network models.

![Encoded dataframe](/Images/3.PNG)

![Dataframes concated](/Images/4.PNG)

From this encoded dataframe, feature and target variables are created, and then split and transformed into training and testing variables.

![Y variable](/Images/5.PNG)

![X variable](/Images/6.PNG)

![Train-test-split](/Images/7.PNG)

These variables are used to create and run a neural network model, which is then saved as an H5 file.

![First model](/Images/8.PNG)

![First model save](/Images/9.PNG)

This model has a reasonable accuracy score, but loss is a bit high so 3 alernative models are also employed to attempt better results with more hidden layers and nodes, different activation functions, and a combination of the two, respectively.

![Alt model 1](/Images/10/PNG)

![Alt model 2](/Images/11/PNG)

![Alt model 3](/Images/12/PNG)

Despite all of the alterations to the models, each attempt produced similar loss and accuracy scores, so they were each saved in a similar fashion to the first to be tested in the field on future data.

![Results](/Images/13/PNG)

![Alt model saves](/Images/14/PNG)
