
# Titanic Dataset - Data Cleaning and Preprocessing

## Overview

This project is part of an AI & ML Internship program and focuses on the essential stage of any machine learning pipeline — **data cleaning and preprocessing**. The Titanic dataset has been selected for this task, which contains passenger data from the Titanic disaster.

The aim is to prepare raw data for machine learning by addressing missing values, encoding categorical variables, removing outliers, and cleaning the dataset without altering its real-world interpretability.

---

## Dataset

**Dataset Used**: Titanic Dataset  
**File Name**: `Titanic-Dataset.csv`  
**Source**: [Kaggle - Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)

### Key Features:
- `PassengerId`: Unique ID for each passenger
- `Survived`: Survival status (0 = No, 1 = Yes)
- `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Ticket`, `Fare`, `Cabin`, `Embarked`

---

## Project Structure


````
titanic-preprocessing/
├── Titanic-Dataset.csv             # Original dataset
├── titanic_cleaned.csv             # Cleaned dataset
├── Titanic-Dataset-Cleaning.ipynb  # Jupyter Notebook with preprocessing steps
└── README.md                       # Project documentation
````


---

## Objectives

- Understand the importance of data preprocessing before model building.
- Handle missing values with appropriate techniques.
- Encode categorical variables for ML compatibility.
- Detect and remove outliers.
- Prepare a clean dataset ready for modeling and analysis.

---

## Preprocessing Workflow

### 1. Import Required Libraries
Utilizes Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, and `sklearn`.

---

### 2. Load and Duplicate Dataset
Loads the dataset and creates a copy to preserve the original file.

---

### 3. Inspect Dataset
Inspects data types, basic statistics, and missing values using:
```python
df.info()
df.isnull().sum()
```

---

### 4. Handle Missing Values

* `Age`: Filled with median value
* `Embarked`: Filled with mode
* `Cabin`: Dropped due to high percentage of missing values

---

### 5. Encode Categorical Features

* `Sex`: Encoded using `LabelEncoder` (e.g., male = 1, female = 0)
* `Embarked`: Encoded into integer values

---

### 6. Drop Non-Essential Columns

* Removed `Name` and `Ticket` due to irrelevance in preprocessing

---

### 7. Outlier Detection and Removal

* Visualized using `boxplots` for `Age` and `Fare`
* Removed outliers using the IQR method to improve data quality



---

### 8. Save Cleaned Data

Saved the final cleaned dataset as:

```
titanic_cleaned_real_values.csv
```

---

## How to Run the Notebook

### Option 1: Jupyter Notebook (Local)

1. Ensure Python is installed with `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn`.
2. Place `Titanic-Dataset.csv` in the same directory as the notebook.
3. Open `preprocessing.ipynb` using Jupyter Notebook or VS Code.
4. Run all cells sequentially.