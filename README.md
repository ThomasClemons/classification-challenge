# classification-challenge
Assignment for AI/ML Bootcamp Module 13 Challenge
---------------------------------------------------------------------

## Description

Our assignment was to simulate working as an Internet Service Provider (ISP).  I've been tasked with improving the email filtering system for its customers. I've been provided with a dataset that contains information about emails, with two possible classifications: spam and not spam. The ISP wants me to take this dataset and develop a supervised machine learning (ML) model that will accurately detect spam emails so it can filter them out of its customers' inboxes.

I created two classification models to fit the provided data, and evaluated which model is more accurate at detecting spam. I created a logistic regression model and a random forest model for this evaluation.

This challenge consists of the following subsections:
- Step 1: Split the data into training and testing sets
- Step 2: Scale the features
- Step 3: Create a logistic regression model
- Step 4: Create a random forest model
- Step 5: Evaluate the models


## Getting Started

### Dependencies

- Python 3.10
- Jupyter Notebook


### Installing

- Clone this repo to your environment


### Executing program
- Open '**spam_detector.ipynb**' in Jupyter Notebook
- Step through the notebook to see my data preparation and analysis by clicking the "Run" button.
- The results are displayed after each step.
---
**Step 1: Split the Data into Training and Testing Sets**  
1. Read the data from https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv into a Pandas DataFrame.

2. I made a prediction as to which model I expected to do better.

> **My Prediction: Since I don't know a lot about the data and don't have an opportunity to ask any clarifying quesitons, I predict Random Forest will perform better that Logistic Regression.  In general, Random Forest seems more robust than Logistic Regression in modeling connections between the predictor values and the result.  Random Forest uses predictions of numerous decision trees to make a final prediction, it handles linear and non-linear relationships between the variables, and handles high-dimensional data with less risk of overfitting.**
>

3. I created the labels set (y) from the “spam” column, and then created the features (X) DataFrame from the remaining columns.

> **NOTE:**
> A value of 0 in the “spam” column means that the message is
> legitimate. A value of 1 means that the message has been
> classified as spam.

4. I checked the balance of the labels variable (y) by using the value_counts function.

5. I split the data into training and testing datasets by using train_test_split.
---
**Step 2: Scale the Features**  

1. I created an instance of StandardScaler.

2. I fit the Standard Scaler with the training data.

3. I scaled the training and testing features DataFrames using the transform function.
---
**Step 3: Create a Logistic Regression Model**  

1. I fit a logistic regression model by using the scaled training data (X_train_scaled and y_train) with random_state set to 1.

2. I saved the predictions on the testing data labels by using the testing feature data (X_test_scaled) and the fitted model.

3. I evaluated the model’s performance by calculating the accuracy score of the model.
---
**Step 4: Create a Random Forest Model**  

1. I fit a random forest classifier model by using the scaled training data (X_train_scaled and y_train).

2. I saved the predictions on the testing data labels by using the testing feature data (X_test_scaled) and the fitted model.

3. I evaluated the model’s performance by calculating the accuracy score of the model.
---
**Step 5: Evaluate the Models**  

I answered the following questions:

> ***Question 1:  Which model performed better?***
> 
> **Answer:  The Random Forest model performed better on this data than Logistic Regression.  The Random Forest Accuracy Score is 0.961 and Logistic Regression Accuracy Score is 0.923.**
>
> ***Question 2:  How does that compare to your prediction?***
>
> **Answer:  I predicted Random Forest and the results match my prediction.**
>
---
## Help

- Please execute all steps in the notebook.  The results of above steps are used in subsequent steps. 


## Authors

- Author:  Tom Clemons

## Version History

- 0.1
    - Initial Release

## Acknowledgments

- None