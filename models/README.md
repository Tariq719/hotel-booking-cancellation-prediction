# Trained Model

## Overview

This folder is intended to store the final trained machine learning model for the Hotel Booking Cancellation Prediction project.

The final model was trained using the complete machine learning pipeline, including data preprocessing and the classification algorithm.

---

## Model File

The final trained model file is named:

```text
final_hotel_cancellation_model.pkl
```

However, the trained model file is not included in this GitHub repository because its file size is approximately **521 MB**, which is too large for a standard GitHub web upload.

---

## Reproducing the Model

The complete data preprocessing, model training, hyperparameter tuning, evaluation, comparison, and final model selection process is available in the Jupyter Notebook located in the following directory:

```text
notebooks/
```

To reproduce the trained model, run the complete Jupyter Notebook from the beginning.

The notebook will:

1. Load the hotel booking dataset.
2. Perform data preprocessing.
3. Prepare numerical and categorical features.
4. Create preprocessing pipelines.
5. Split the data into training and testing sets.
6. Train multiple machine learning classification models.
7. Evaluate and compare model performance.
8. Perform hyperparameter tuning.
9. Select the final model.
10. Save the trained model.

---

## Saving the Model

The trained model can be saved using `joblib`:

```python
import joblib

joblib.dump(
    final_model,
    "../models/final_hotel_cancellation_model.pkl"
)
```

---

## Loading the Model

The saved model can be loaded using:

```python
import joblib

loaded_model = joblib.load(
    "../models/final_hotel_cancellation_model.pkl"
)
```

---

## Making Predictions

After loading the trained model, predictions can be generated using:

```python
predictions = loaded_model.predict(X_test)
```

For cancellation probabilities, use:

```python
probabilities = loaded_model.predict_proba(X_test)[:, 1]
```

The predicted class represents whether a hotel booking is expected to be canceled.

---

## Important Note

The complete preprocessing pipeline is included inside the saved model pipeline. Therefore, the same preprocessing steps used during training are automatically applied when making predictions.

This helps ensure consistency between the training process and future predictions.

---

## Project Repository

For the complete project workflow, including:

- Data understanding
- Data cleaning
- Exploratory analysis
- Feature preprocessing
- Machine learning model training
- Model evaluation
- Model comparison
- Hyperparameter tuning
- Final model selection

Please refer to the main project documentation:

```text
README.md
```

and the Jupyter Notebook available in:

```text
notebooks/
```
