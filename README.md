# Breast Cancer Classification Using PCA and Logistic Regression

# Introduction

In this data analytics project, I analyzed a breast cancer dataset to build a machine learning model capable of accurately classifying tumors as either malignant or benign. The goal was to demonstrate my skills in data analysis, dimensionality reduction, model building, and evaluation techniques commonly used in the industry.

# Dataset

I used the **Breast Cancer Wisconsin Dataset**, a widely used dataset from scikit-learn, consisting of 569 samples and 30 features representing tumor characteristics. Each tumor sample was labeled as either malignant (dangerous) or benign (non-dangerous).

The features include:
- Mean radius, texture, perimeter, area, smoothness, compactness, concavity, symmetry, fractal dimension, and additional statistical measures.

# Steps Taken

# 1. Data Preparation
- Loaded the dataset using scikit-learn.
- Checked for missing values and inconsistencies (none found in this clean dataset).
- Standardized the dataset using `StandardScaler` to ensure each feature has an equal influence on the analysis.

# 2. Dimensionality Reduction (PCA)
- I applied Principal Component Analysis (PCA) to simplify the dataset by reducing its dimensionality.
- PCA reduced the original 30 features down to just 3 principal components.
- These 3 components retained approximately **73% of the original data variance**, significantly simplifying the model while preserving most of the essential information.

# 3. Splitting the Data
- The dataset was split into two sets:
  - **70% Training Set**: To train the Logistic Regression model.
  - **30% Testing Set**: To evaluate the accuracy and generalization of the model on unseen data.

# 4. Model Training (Logistic Regression)
- I chose a Logistic Regression model due to its effectiveness in binary classification tasks.
- Trained the model on the PCA-reduced training data to learn how to classify tumors based on the three principal components.

# 5. Model Evaluation
- Evaluated the model's accuracy using the test data, achieving an impressive accuracy of approximately 98.25%.
- Generated a Receiver Operating Characteristic (ROC) curve and calculated the Area Under the Curve (AUC) as an additional performance measure.
- Achieved an AUC of approximately 0.98, indicating a highly accurate model that effectively distinguishes between malignant and benign tumors.

# 6. Results Visualization
- Clearly visualized the ROC curve to showcase the trade-off between sensitivity (correctly identifying malignant tumors) and specificity (correctly identifying benign tumors).

# Results

- Accuracy: ~98.25%
- ROC-AUC: ~0.98

These results demonstrate that my model effectively reduces complexity through PCA while significantly enhancing classification accuracy.

# Alternative Approaches

Although PCA performed excellently, I considered alternative methods like Linear Discriminant Analysis (LDA) as well, which uses label information to enhance class separation. Exploring such supervised dimensionality reduction methods could potentially improve results further in future iterations.

## Technologies Used
- Python
- NumPy
- Pandas
- scikit-learn
- Matplotlib

## How to Run This Project

1. Clone the repository
```bash
git clone https://github.com/yourusername/breast-cancer-classification.git
```

2. Install the required libraries
```bash
pip install -r requirements.txt
```

3. Run the project
```bash
python main.py
```
