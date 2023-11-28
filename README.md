# Spam Detection Using Support Vector Machine

## Overview
This project focuses on spam detection using a Support Vector Machine (SVM) model. The dataset used is obtained from Kaggle and contains labeled spam and ham (non-spam) emails. The goal is to train a model to accurately classify emails as either spam or ham based on their content.

## Dataset
The dataset consists of a collection of emails labeled as spam or ham. It includes the following columns:

- **v1**: The label column, indicating whether the email is spam or ham.
- **v2**: The text content of the email.

## Dataset Source
The dataset is sourced from Kaggle. You can find the dataset on Kaggle's [Spam Collection](https://www.kaggle.com/uciml/sms-spam-collection-dataset).

## Data Preprocessing
### Loading the Dataset
The dataset is loaded into a Pandas DataFrame using `pd.read_csv('spam.csv', encoding='latin-1')`.

### Handling Null Values
Null values in the dataset are replaced with empty strings to ensure smooth data processing.

### Labeling
Emails labeled as spam are assigned the value 0, and those labeled as ham are assigned the value 1.

## Model Training
### Train-Test Split
The dataset is split into training and testing sets using `train_test_split` from `sklearn.model_selection`.

### Feature Extraction
The text data is transformed into feature vectors using `TfidfVectorizer` from `sklearn.feature_extraction.text`.

### Label Encoding
Labels are encoded into numerical values using `LabelEncoder` from `sklearn.preprocessing`.

### SVM Model
A Linear Support Vector Machine model is initialized and trained using the training data.

## Model Evaluation
The model's accuracy is evaluated on both the training and testing datasets using the `accuracy_score` metric from `sklearn.metrics`.

## Prediction on New Emails
### Input Emails
Sample emails are provided for prediction.

### Feature Extraction for Input Emails
The same `TfidfVectorizer` is used to transform input emails into feature vectors.

### Prediction
The trained SVM model predicts whether each input email is spam or ham.

## How to Use
1. Install dependencies: `pip install numpy pandas scikit-learn`.
2. Download the dataset (`spam.csv`) from [Kaggle's Spam Collection](https://www.kaggle.com/uciml/sms-spam-collection-dataset) and place it in the project directory.
3. Run the provided Jupyter Notebook or Python script.
4. Explore model accuracy and make predictions on new emails.

## Contributors
Anamika Sadh

## Acknowledgments
Dataset source: Kaggle's Spam Collection.

## License
This project is licensed under the MIT License.
