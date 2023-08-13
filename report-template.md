## Overview of the Analysis

The main goal of this analysis is to use a type of computer learning called "supervised machine learning" to predict whether borrowers are likely to pay back loans. We used a dataset that included details about loans, like the loan amount, interest rate, borrower's income, and more. The data came from a company that provides loans to people.

We focused on figuring out if a loan is safe ("healthy loan") or risky ("high-risk loan"). This was done by looking at the "loan status" information, where 0 meant a healthy loan and 1 meant a high-risk loan.

Here's what we did step by step:

We split the data into groups for training and testing using a method called "train_test_split."
We used a special kind of math (logistic regression) to build a model using the training data.
We used the model to make predictions about the testing data.
We checked how well our model did using a confusion matrix and a classification report. If things were imbalanced, we used a technique called "RandomOverSampler" to fix it.
We repeated the process with the improved data and checked the model's performance again.
Here are the results for both models:

Machine Learning Model 1 Using train_test_split:

The model was accurate and had a score of 0.99.
For healthy loans (0), it was very good at being precise (getting things right) and recalling (finding them).
For high-risk loans (1), it was pretty good at precision and recall.
Machine Learning Model 2 using RandomOverSampler:

The model had an even better score of 1.00 for accuracy.
For both healthy loans (0) and high-risk loans (1), it was also good at precision and recall.
In Summary:
Both models did well in predicting healthy loans. So, we focused on their performance for high-risk loans.
We looked at precision (getting right results) and recall (finding all the right results) for high-risk loans. A high precision and recall are important to avoid mistakes.
The model using RandomOverSampler seemed better. It had better recall, meaning it found more of the actual high-risk loans. This is important because we want to catch as many risky loans as possible.
Still, it's important to note that even with the better model, there could be some mistakes (false positives). Based on this, I recommend using the RandomOverSampler model because of its improved recall accuracy.T