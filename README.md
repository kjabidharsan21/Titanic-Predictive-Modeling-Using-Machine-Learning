# Titanic Survival Prediction Using Machine Learning

# Project Overview

This project focuses on building and evaluating machine learning models using the **Titanic dataset** to predict whether a passenger survived the Titanic disaster.

The project was developed as a practical implementation of **pervised machine learning**, covering the complete workflow from data preprocessing to model training, evaluation, and comparison.

The main objective is to understand how passenger information such as **age, gender, passenger class, fare, and port of embarkation** can be used to predict survival outcomes.

# Dataset

The project uses the Titanic passenger dataset, which contains information about passengers who were on board the Titanic.

The target variable used for classification is:

* **Survived** – indicates whether the passenger survived or not.

  * `0` – Did not survive
  * `1` – Survived

The dataset includes features such as:

* Passenger class (`Pclass`)
* Sex (`Sex`)
* Age (`Age`)
* Number of siblings/spouses aboard (`SibSp`)
* Number of parents/children aboard (`Parch`)
* Passenger fare (`Fare`)
* Port of embarkation (`Embarked`)

# Data Preprocessing

Before applying machine learning algorithms, the dataset was cleaned and prepared for modeling.

The preprocessing steps included:

1. Loading the Titanic dataset using Pandas.
2. Checking the first few records.
3. Examining the dataset structure and data types.
4. Identifying missing values.
5. Filling missing values in the `Age` column using the median.
6. Filling missing values in the `Embarked` column using the mode.
7. Removing unnecessary columns such as:

   * `PassengerId`
   * `Name`
   * `Ticket`
   * `Cabin`
8. Converting categorical variables into numerical values using one-hot encoding.
9. Saving the processed dataset as `cleaned_titanic.csv`.

This preprocessing makes the dataset suitable for machine learning algorithms.

# Machine Learning Models

# 1. Decision Tree Classifier

A Decision Tree classifier was implemented to predict passenger survival.

The model was configured with a maximum depth of 5 to control the complexity of the tree and reduce the possibility of overfitting.

The dataset was divided into:

* **80% training data**
* **20% testing data**

The model's performance was evaluated using classification accuracy.

# 2. Random Forest Classifier

A Random Forest classifier was also implemented.

Random Forest combines multiple decision trees and uses their combined predictions to produce a more robust classification result.

The model was created using **100 decision trees**.

The same 80/20 training and testing approach was used so that the performance of the models could be compared fairly.

# Model Comparison

The project compares the performance of the **Decision Tree** and **Random Forest** models.

Accuracy is calculated for both models to determine how well they predict passenger survival.

This comparison helps identify which algorithm performs better on the prepared Titanic dataset.

# Confusion Matrix

A confusion matrix was generated for the Random Forest model to get a more detailed understanding of its classification performance.

The confusion matrix shows:

* **True Positives** – passengers correctly predicted as survivors
* **True Negatives** – passengers correctly predicted as non-survivors
* **False Positives** – passengers predicted as survivors but who did not survive
* **False Negatives** – passengers predicted as non-survivors but who actually survived

A visual confusion matrix was also generated using Matplotlib and Scikit-learn.

# ROC Curve and AUC

The project also evaluates the Random Forest model using a **ROC curve**.

The ROC curve shows the relationship between:

* True Positive Rate
* False Positive Rate

The **ROC-AUC score** is calculated to measure the model's ability to distinguish between passengers who survived and those who did not.

A higher AUC value indicates better classification performance.

# Feature Importance

Feature importance was calculated using the Random Forest model.

This helps identify which passenger characteristics contributed most to the model's survival predictions.

The feature importance values are displayed using a bar chart, making it easier to understand the relative contribution of each feature.

# Linear Regression

In addition to the classification models, Linear Regression was implemented as a separate regression experiment.

In this part of the project:

* `Fare` is used as the target variable.
* The remaining available features are used as input variables.
* The dataset is divided into training and testing sets.
* A Linear Regression model is trained on the training data.

The regression model is evaluated using:

* **Mean Absolute Error (MAE)**
* **Mean Squared Error (MSE)**
* **R² Score**

This provides practical experience with both **classification and regression techniques** within the same dataset.

# Technologies Used

The project was developed using Python and the following libraries:

* **Python**
* **Pandas** – data loading and preprocessing
* **Scikit-learn** – machine learning and model evaluation
* **Matplotlib** – data visualization
* **Jupyter Notebook** – development and experimentation


# Files in the Project

| File                  | Description                                             |
| --------------------- | ------------------------------------------------------- |
| `Titanic-Dataset.csv` | Original Titanic dataset                                |
| `cleaned_titanic.csv` | Preprocessed dataset used for modeling                  |
| `Untitled.ipynb`      | Jupyter Notebook containing the complete implementation |

# Key Learning Outcomes

Through this project, I gained practical experience in:

* Understanding and preparing a real-world dataset
* Handling missing values
* Removing unnecessary features
* Encoding categorical variables
* Splitting data into training and testing sets
* Building classification models
* Implementing Decision Trees
* Implementing Random Forest
* Comparing machine learning models
* Evaluating classification accuracy
* Creating and interpreting confusion matrices
* Understanding ROC curves and AUC scores
* Analyzing feature importance
* Implementing Linear Regression
* Evaluating regression models using MAE, MSE, and R²

# Conclusion

This project demonstrates a complete machine learning workflow using the Titanic dataset. Rather than directly applying an algorithm to raw data, the project covers the important stages of **data preprocessing, model development, evaluation, and interpretation**.

The project also provides a comparison between Decision Tree and Random Forest classification techniques and uses evaluation methods such as accuracy, confusion matrix, ROC-AUC, and feature importance to understand model performance.

Overall, this project helped strengthen my practical understanding of **supervised machine learning and model evaluation using Python and Scikit-learn**.
