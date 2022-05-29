Overview of the Analysis

Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans. That is why we’ll use various techniques to train and evaluate models with imbalanced classes. We will use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.  We will attmept to use variables such as loan size, interest rate, borrower income, debt to income ratio, number of accounts borrowers have, derogatory marks, and total debts to predict whether a given loan will default.  When we use the value_counts function, we see that default loans are only 3% of the dataset, with the other 97% of the data comprising of non-defaulted loans. This is evidence that the data is imbalanced.  We divide the dataset into training and testing data. We then use a logistic regression mopdel is used to fit the model and make predictions. Because the dataset is imbalanced, we use RandomOverSampler to resample the training data.



Results

Model 1 - Accuracy: 95% - Precision: 100% for non-default and 85% for default loans - Recall: 99% for non-default and 91% for default loans

Model 2 - Accurancy: 99% - Precision: 100% for non-default and 84% for default loans - Recall: 99% for non-default and 99% for default loan



Summary
The main takaway from our analysis is that the oversampling method does a better job at categorizing defaulted loans than our original logistic regression model. Despite similar precision scores, the recall values for model two show that the oversampling method does a better job at categorizing default loans than model 1.  It is worth noting that both models do an equally good job of predicting non-default loans, but model 2's accuracy score of 99% is better than 95% because of model 2's ability to predict loans that were defaulted on.  Since we are looking for the most accurate model (and because prediting defaulted loans is the reason this modeling is valuable to the financial industry), Model 2 is the clear choice.

