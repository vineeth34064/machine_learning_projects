# Spam/Ham Email Classifier

## Project Overview
This project implements a machine learning model to classify emails as either 'spam' or 'ham' (legitimate email). The goal is to build a robust classifier that can distinguish between unwanted promotional or malicious emails and important personal or professional correspondence.

## Dataset
The model was trained and evaluated using the `mail_data.csv` dataset, which contains email messages labeled as 'spam' or 'ham'.

## Methodology

### 1. Data Preprocessing
*   Missing values were handled by replacing them with empty strings.
*   Email categories ('spam' and 'ham') were converted into numerical labels (0 for spam, 1 for ham) using label encoding.

### 2. Feature Extraction
*   The text data from the email messages was transformed into numerical feature vectors using **TF-IDF Vectorization**. This technique assigns weights to words based on their frequency in a document and across the entire corpus, highlighting words that are important in a specific email but not common everywhere.

### 3. Model Training
*   A **Logistic Regression** model was chosen for classification due to its effectiveness in binary classification tasks and its interpretability.
*   The data was split into training and testing sets (80% training, 20% testing) to evaluate the model's generalization capability.

## Performance

The trained Logistic Regression model achieved the following accuracies:
*   **Accuracy on Training Data**: 0.9677 (or approximately 96.77%)
*   **Accuracy on Test Data**: 0.9668 (or approximately 96.68%)

These high accuracy scores indicate that the model performs well in distinguishing between spam and ham emails on both seen and unseen data.

## How to Use (Prediction Example)

To predict whether a new email is spam or ham, you can use the trained `features_extraction` (TF-IDF Vectorizer) and `model` (Logistic Regression Classifier):

```python
# Example input email
input_mail = ["Congratulations! You've won a free iPhone. Click here to claim your prize!"]

# Convert the input text to feature vectors using the trained TF-IDF vectorizer
input_features = features_extraction.transform(input_mail)

# Make a prediction using the trained Logistic Regression model
prediction = model.predict(input_features)

# Interpret and print the prediction
if (prediction[0] == 1):
    print('Ham mail')
else:
    print('Spam mail')
```

This will output whether the `input_mail` is classified as 'Ham mail' or 'Spam mail'.
