# Titanic Survival Prediction Project 🚢

This project analyzes the Titanic dataset to predict passenger survival using machine learning models. The steps include data preprocessing, exploratory data analysis, outlier handling, feature engineering, and model implementation.

## Table of Contents 📑

- [Introduction](#introduction)
- [Dataset Description](#dataset-description)
- [Dependencies](#dependencies)
- [Steps](#steps)
  - [Data Preprocessing](#data-preprocessing)
  - [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Outlier Detection and Handling](#outlier-detection-and-handling)
  - [Feature Encoding](#feature-encoding)
  - [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [How to Run](#how-to-run)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Introduction ✨

The Titanic dataset provides demographic and travel details of passengers. The goal of this project is to predict whether a passenger survived the Titanic disaster based on features such as age, gender, ticket class, and fare.

## Dataset Description 📊

The dataset includes the following columns:
- **Survived**: Survival status (0 = No, 1 = Yes) <br> <img width="617" alt="Ekran Resmi 2024-12-10 18 08 26" src="https://github.com/user-attachments/assets/3cecc69d-bd53-46a6-8654-a7dad440e242">

- **Pclass**: Passenger's ticket class (1 = Upper, 2 = Middle, 3 = Lower) <br>
<img width="434" alt="Ekran Resmi 2024-12-10 18 07 49" src="https://github.com/user-attachments/assets/adb73fbd-d8fe-4f43-aaee-f12cc17bfbee">
<br>
- **Name**: Passenger's name<br>
- **Sex**: Gender (male or female) <br> <img width="433" alt="Ekran Resmi 2024-12-10 18 08 07" src="https://github.com/user-attachments/assets/746bf4ea-5665-4450-8789-0fa85b6851c2">

- **Age**: Passenger's age<br>
- **SibSp**: Number of siblings or spouses aboard<br>
- **Parch**: Number of parents or children aboard<br>
- **Fare**: Ticket fare <br> <img width="594" alt="Ekran Resmi 2024-12-10 18 09 11" src="https://github.com/user-attachments/assets/b7b49b6f-a030-4350-b140-93cb33201a19">

- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)<br>
<img width="438" alt="Ekran Resmi 2024-12-10 18 08 53" src="https://github.com/user-attachments/assets/ad79c64b-eda2-41d1-9f98-b9a160fb8604">
<br>
<img width="823" alt="Ekran Resmi 2024-12-10 18 10 41" src="https://github.com/user-attachments/assets/c793bd3e-5078-44f3-88da-064abfb69e64">

## Dependencies 📦

Install the required libraries using the following command:

pip install numpy pandas seaborn matplotlib scikit-learn

## Steps 📝

### Data Preprocessing 🧹
**Handling Missing Values:**
- Missing ages were replaced with the mean value.
- Missing embarkation ports were filled with the most common port.

**Feature Engineering:**
- Created a new feature `FamilySize = SibSp + Parch + 1`.
- Extracted passenger titles from names.

**Dropping Irrelevant Features:**
- Columns like `PassengerId`, `Name`, `Ticket`, and `Cabin` were dropped as they were not useful for prediction.

### Exploratory Data Analysis (EDA) 📉
- Visualized survival distribution based on age, gender, and ticket class.
- Examined correlations between numerical features and survival rate.

### Outlier Detection and Handling 🚨
- Used box plots and statistical thresholds to identify outliers in `Age`, `Fare`, and `SibSp`.
- Outliers were addressed using scaling and capping techniques.

### Feature Encoding 🔢
- Used one-hot encoding to convert categorical variables (`Sex`, `Embarked`) into numerical features.

### Model Training and Evaluation 📈
Implemented and evaluated the following models:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Random Forest Classifier

Metrics evaluated include:
- Accuracy
- Precision
- Recall
- F1 Score

## Results 🏆

The Random Forest model achieved the best accuracy of 85.04%. Below are the key evaluation metrics:

| Model               | Accuracy | Precision | Recall | F1 Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 80.23%   | 0.781     | 0.710  | 0.743    |
| KNN                 | 82.11%   | 0.812     | 0.732  | 0.769    |
| Naive Bayes         | 78.34%   | 0.750     | 0.690  | 0.718    |
| Random Forest       | 85.04%   | 0.850     | 0.820  | 0.834    |

## Future Improvements 🔮

Possible areas for improvement include:
- **Hyperparameter Tuning:** Use GridSearchCV or RandomizedSearchCV to optimize hyperparameters for better model performance.
- **Additional Feature Engineering:** Incorporate derived features such as fare per family member or interaction terms.
- **Advanced Models:** Explore Gradient Boosting models (e.g., XGBoost, LightGBM) and deep learning approaches.
- **Cross-Validation:** Implement k-fold cross-validation to ensure robustness of results.
- **Ensemble Learning:** Combine multiple models (e.g., stacking or blending) to improve performance.
- **Deployment:** Build a web application or API using Flask or FastAPI for real-time predictions.

## How to Run 🚀

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/titanic-survival-prediction.git
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the script to start the analysis:
    ```bash
    python titanic_analysis.py
    ```

