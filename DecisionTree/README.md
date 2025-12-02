# Heart Disease Analysis using Decision Tree

## Project Overview

This project implements a **Decision Tree Classifier** to predict the presence of heart disease in patients based on various health parameters. The model analyzes medical data and provides predictions to help identify individuals at risk of heart disease.

## Problem Statement

**Objective:** Predict whether a person has heart disease or not based on various health parameters.

The target variable indicates the presence (1) or absence (0) of heart disease in the patient.

## Dataset

**File:** `heart.csv`

### Dataset Characteristics
- **Size:** 305 records (after removing duplicates)
- **Features:** 13 medical and demographic attributes
- **Target Variable:** `target` (binary classification: 0 or 1)

### Features
1. **age** - Age of the patient
2. **gender** - Gender (0=Female, 1=Male)
3. **chestPain** - Type of chest pain (0-3)
4. **restingBloodPressure** - Resting blood pressure (mm Hg)
5. **cholesterol** - Serum cholesterol level (mg/dl)
6. **fastingBloodSugar** - Fasting blood sugar > 120 mg/dl (0=No, 1=Yes)
7. **RestingECGresults** - Resting electrocardiographic results (0-2)
8. **maximumHeartRate** - Maximum heart rate achieved
9. **exerciseInducedAngina** - Exercise-induced angina (0=No, 1=Yes)
10. **oldpeak** - ST depression induced by exercise relative to rest
11. **slope** - Slope of the ST segment (0-2)
12. **numberOfMajorVessels** - Number of major vessels (0-3)
13. **thalassemia** - Thalassemia type (0-3)

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Data shape and structure analysis
- Missing values detection
- Data distribution and statistics
- Duplicate record identification and removal
- Outlier detection using box plots

**Key Findings:**
- Removed 1 duplicate record
- Outliers were retained as they represent important medical information
- No missing values in the dataset

### 2. Data Preprocessing
- Feature extraction (X) and target variable (y) separation
- No additional scaling or normalization applied (Decision Tree handles raw values)
- Train-test split: 80% training, 20% testing

### 3. Model Building
- **Algorithm:** Decision Tree Classifier
- **Training Set:** 244 samples
- **Test Set:** 61 samples

### 4. Model Evaluation
- **Accuracy Score:** Calculated using accuracy_score()
- **Classification Report:** Precision, recall, and F1-score for each class
- **Confusion Matrix:** True positives, true negatives, false positives, false negatives
- **Decision Tree Visualization:** Tree structure visualization for interpretability

## Results

The trained Decision Tree model provides:
- Overall accuracy on test data
- Per-class performance metrics
- Confusion matrix for detailed error analysis
- Visual representation of decision rules

## Libraries Used

- **numpy** - Numerical computations
- **pandas** - Data manipulation and analysis
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **scikit-learn** - Machine learning algorithms and metrics

## Key Advantages of Decision Tree

✓ Highly interpretable and easy to understand  
✓ No data normalization required  
✓ Handles both numerical and categorical data  
✓ Provides feature importance insights  
✓ Performs well on medical datasets  

## Files in This Project

- `Heart_Disease_Analysis.ipynb` - Main Jupyter notebook with complete analysis
- `heart.csv` - Dataset containing patient health records
- `README.md` - This documentation file

## How to Run

1. Ensure Python 3.x is installed with required libraries:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn
   ```

2. Open the Jupyter notebook:
   ```bash
   jupyter notebook Heart_Disease_Analysis.ipynb
   ```

3. Run all cells sequentially to execute the complete analysis and model training

## Dataset Source

This dataset appears to be derived from the UCI Machine Learning Repository's Heart Disease dataset, containing real medical data used for research and educational purposes.

## Future Enhancements

- Hyperparameter tuning for optimal tree depth
- Cross-validation for robust model evaluation
- Feature importance analysis
- Comparison with other algorithms (Random Forest, SVM, etc.)
- Feature selection to identify most important predictors

## Notes

- Medical data quality is prioritized; outliers are retained as they may represent important clinical cases
- The model is for educational purposes and should not replace professional medical diagnosis
- Continuous monitoring and validation with new data is recommended for deployment

---

**Last Updated:** December 2025
