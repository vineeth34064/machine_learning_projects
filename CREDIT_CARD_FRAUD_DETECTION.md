# Credit Card Fraud Detection

## Project Overview
This project aims to detect fraudulent credit card transactions using a machine learning model. The dataset contains highly imbalanced transaction data, where the number of fraudulent transactions is significantly lower than normal transactions.

## Dataset
The dataset `creditcard.csv` includes 284,807 transactions with 31 features:
- `Time`: Seconds elapsed between this transaction and the first transaction in the dataset.
- `V1` to `V28`: Principal components obtained with PCA, due to confidentiality.
- `Amount`: Transaction Amount.
- `Class`: Response variable, 1 for fraud and 0 otherwise.

## Data Preprocessing
1.  **Handling Imbalanced Data**: The original dataset is highly imbalanced (284,315 normal vs. 492 fraud transactions). To address this, an undersampling technique was applied, creating a new dataset (`newdata`) with an equal number of normal and fraudulent transactions (492 of each).
2.  **Feature and Target Split**: The 'Class' column was separated as the target variable (y), and the remaining columns as features (x).

## Model Training
1.  **Data Splitting**: The balanced dataset (`newdata`) was split into training (70%) and testing (30%) sets using `train_test_split` with `stratify=y` to maintain the class distribution.
2.  **Model**: A Logistic Regression model was used for classification.
3.  **Training**: The model was trained on the `x_train` and `y_train` data.

## Model Evaluation
After training, the model's performance was evaluated using accuracy scores:
-   **Accuracy on Training Data**: 94.19%
-   **Accuracy on Test Data**: 91.55%

## Conclusion
The Logistic Regression model demonstrated good accuracy on both the training and test datasets, indicating its effectiveness in distinguishing between normal and fraudulent credit card transactions after balancing the dataset.

## Libraries Used
-   `pandas`
-   `numpy`
-   `sklearn.model_selection`
-   `sklearn.linear_model`
-   `sklearn.metrics`
