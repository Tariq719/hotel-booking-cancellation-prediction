# Hotel Booking Cancellation Prediction

A machine learning project for predicting whether a hotel booking will be canceled using historical hotel booking data.

This project follows a complete data science and machine learning workflow, including data understanding, data cleaning, preprocessing, model training, evaluation, comparison, hyperparameter tuning, and final model selection.

---

## 📌 Project Overview

This project uses historical hotel booking data containing information about bookings from two types of hotels:

- City Hotel
- Resort Hotel

Each row represents an individual hotel booking.

The dataset contains information related to:

- Hotel type
- Booking characteristics
- Customer details
- Arrival dates
- Length of stay
- Previous booking history
- Market segments
- Reservation information
- Deposit types
- Customer requirements
- Final booking outcomes

The primary objective of this project is to build and compare multiple machine learning classification models to predict whether a hotel booking will be canceled.

---

## 🏨 Business Context

Hotel booking cancellations can create significant challenges for hotel management.

A canceled reservation may result in:

- Loss of expected revenue
- Unoccupied rooms
- Difficulty in demand forecasting
- Inefficient room allocation
- Challenges in staffing and operational planning

By analyzing historical booking data, hotels can better understand customer behavior and identify factors associated with booking cancellations.

Some important business questions include:

- Do customers who book far in advance cancel more frequently?
- Does hotel type affect cancellation behavior?
- Does deposit type influence cancellation rates?
- Which market segments generate the highest number of cancellations?
- Do customers with previous cancellations have a higher probability of canceling again?
- Are repeated guests less likely to cancel their bookings?

---

## 🎯 Project Objectives

The main objective of this project is to prepare the hotel booking dataset for reliable machine learning and develop models for predicting booking cancellations.

The project is divided into two major stages.

### 1. Data Preprocessing

The original dataset is examined and prepared by performing the following tasks:

- Understanding the dataset and business context
- Inspecting the dataset structure
- Checking data types
- Identifying missing values
- Detecting duplicate records
- Investigating invalid or inconsistent values
- Examining potential outliers
- Performing appropriate data cleaning
- Validating the cleaned dataset
- Saving the final cleaned dataset

Every preprocessing decision is based on the meaning and characteristics of the variables rather than applying cleaning techniques blindly.

### 2. Machine Learning

The cleaned dataset is used to train and evaluate multiple machine learning classification models.

The machine learning process includes:

- Defining features and the target variable
- Separating numerical and categorical variables
- Creating a preprocessing pipeline
- Performing train-test splitting
- Training multiple classification algorithms
- Making predictions
- Evaluating model performance
- Comparing models
- Performing hyperparameter tuning
- Selecting the final model

---

## 🤖 Machine Learning Objective

The primary machine learning objective is:

> **Predict whether a hotel booking will be canceled.**

The target variable is:

```text
is_canceled
```

The target variable contains two classes:

- `0` → Booking not canceled
- `1` → Booking canceled

This is therefore a **binary classification problem**.

---

## 📊 Dataset

The project uses historical hotel booking data containing information about bookings from two types of hotels:

- City Hotel
- Resort Hotel

Each row represents an individual hotel booking.

The original dataset is stored in:

```text
datasets/raw/
```

After data cleaning, the processed dataset is stored in:

```text
datasets/cleaned/
```

The cleaned dataset is used as the input for the machine learning stage.

---

## 🧹 Data Preprocessing Workflow

The data preprocessing process follows a structured workflow:

1. Data understanding and inspection
2. Missing value analysis
3. Duplicate analysis
4. Investigation of invalid and inconsistent values
5. Outlier investigation
6. Data cleaning
7. Validation of the cleaned dataset
8. Saving the cleaned dataset

Every preprocessing decision is based on the meaning and characteristics of the variables rather than applying cleaning techniques blindly.

---

# 🔄 Machine Learning Workflow

```text
Cleaned Dataset
       ↓
Feature and Target Selection
       ↓
Train-Test Split
       ↓
Numerical and Categorical Features
       ↓
Preprocessing Pipeline
       ↓
Model Training
       ↓
Prediction
       ↓
Model Evaluation
       ↓
Model Comparison
       ↓
Hyperparameter Tuning
       ↓
Final Model Selection
```

---

## 📂 Feature and Target Selection

The dataset is divided into:

- **X** → Input features
- **y** → Target variable

The target variable is:

```text
is_canceled
```

The remaining selected variables are used as input features for predicting whether a booking will be canceled.

---

## ✂️ Train-Test Split

The dataset is divided into training and testing data.

The training data is used to train the machine learning models, while the testing data is kept separate to evaluate how well the trained models perform on unseen data.

---

## ⚙️ Data Preprocessing Pipeline

A Scikit-learn preprocessing pipeline is used to process numerical and categorical features consistently.

### Numerical Features

Numerical features are processed using:

- Appropriate missing value handling
- `StandardScaler`

### Categorical Features

Categorical features are processed using:

- Appropriate missing value handling
- `OneHotEncoder`

The preprocessing steps are combined using a `ColumnTransformer` and integrated into the machine learning pipeline.

This approach helps reduce the risk of data leakage and ensures that the same preprocessing steps are applied consistently during training, testing, and future predictions.

---

# 🤖 Classification Models

The project includes:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier

Each model is trained using the same prepared training and testing data to support a fair comparison.

---

# 📈 Model Evaluation

Each model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Classification Report
- Confusion Matrix
- ROC Curve
- Training Accuracy
- Testing Accuracy

Training and testing accuracy are compared to assess possible overfitting.

---

## Accuracy

```text
Accuracy = Correct Predictions / Total Predictions
```

## Precision

Measures how many bookings predicted as canceled were actually canceled.

## Recall

Measures how many actual canceled bookings were correctly identified.

## F1 Score

Provides a balance between precision and recall.

## ROC-AUC Score

Measures the model's ability to distinguish between canceled and non-canceled bookings across different classification thresholds.

---

# 📊 Model Comparison

After training and evaluating all models, their performance metrics are collected and compared.

The comparison includes:

- Training Accuracy
- Testing Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score

The final model is selected based on the combined evaluation results rather than relying on a single metric.

---

# 🔧 Hyperparameter Tuning

Hyperparameter tuning is performed on selected models to improve model performance.

The process includes:

- Defining a parameter grid
- Performing cross-validation
- Identifying the best parameter combination
- Evaluating the tuned model on the test dataset

---

# 🏆 Final Model Selection

The final model is selected based on:

- ROC-AUC Score
- F1 Score
- Precision
- Recall
- Overall Accuracy
- Generalization performance
- Comparison between training and testing accuracy

The goal is to select a model that provides reliable and balanced performance on unseen data.

---

# 📁 Project Structure

```text
hotel-booking-cancellation-prediction/
│
├── datasets/
│   ├── raw/
│   └── cleaned/
├── images/
├── models/
│   └── README.md
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   └── 02_Machine_Learning.ipynb
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

# 📦 Installation

```bash
git clone https://github.com/Tariq719/hotel-booking-cancellation-prediction.git
cd hotel-booking-cancellation-prediction
pip install -r requirements.txt
```

---

# ▶️ Usage

1. Run the data cleaning notebook.
2. Generate and save the cleaned dataset.
3. Run the machine learning notebook.
4. Train and evaluate the classification models.
5. Compare the model performance.
6. Perform hyperparameter tuning where applicable.
7. Select the final model based on the evaluation results.

---

# 🔁 Reproducibility

The trained model file is not included in this repository because the final serialized model file is too large for a standard GitHub repository upload.

The complete workflow can be reproduced using the datasets and Jupyter notebooks included in this repository.

---

# 🔮 Future Improvements

- Additional feature engineering
- Advanced hyperparameter optimization
- Additional boosting algorithms
- Feature importance analysis
- Model explainability
- Deployment using Streamlit or Flask
- Interactive prediction interface

---

# 📄 License

This project is licensed under the MIT License.

See the [LICENSE](LICENSE) file for more information.

---

# 👤 Author

**Tariq Nawaz**

Machine Learning and Data Science Enthusiast

---

⭐ If you find this project useful, consider giving the repository a star.
