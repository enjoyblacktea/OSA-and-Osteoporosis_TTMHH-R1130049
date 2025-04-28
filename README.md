# OSA-and-Osteoporosis_TTMHH-R1130049
## Population selection.ipynb

This project filters and compares data from a master dataset based on multiple reference files. The overall process is as follows:

---

### 1. Data Loading
- Use `Pathlib` to load all `.csv` files from the folder `Data Set/csv` into a dictionary for easy access.

### 2. Parameter Setup
- Specify the **base file** (`2017-2022-Meger.csv`) and key feature column (`id_number`).
- Define feature mappings for reference files using `去個資編號`.

### 3. Data Filtering
- Filter rows in the base file based on matching `id_number` values from reference files.
- Avoid duplicates and display counts for OSA and BMD samples.
- Save filtered data to `2017-2022-filter.csv`.

### 4. Advanced Comparison
- Categorize data into samples found only in OSA reports, only in BMD reports, and in both.

### 5. Duplicate Check
- Check for duplicate `id_number` values in the filtered data and display results.

### 📂 Output
- Save the filtered dataset as `2017-2022-filter.csv`.
- Display summary statistics and duplicates during execution.

---

## Data Preprocessing & Model Evaluation

### 1. Data Preprocessing
- Remove rows with missing BMI or OSA results.
- Filter BMI (18.5 ≤ BMI ≤ 60) and age (50 ≤ age ≤ 85) to ensure valid ranges.

### 2. Feature Analysis
- Perform T-tests for continuous features and Chi-square tests for categorical features to assess their relation to `OSA_result`.

### 3. Model Definition
- Use multiple models: Logistic Regression, Random Forest, XGBoost, AdaBoost, and SVM.

### 4. Cross-Validation
- Perform 10-fold cross-validation for model evaluation (accuracy and ROC curve analysis).

### 5. Hyperparameter Tuning
- Optionally tune hyperparameters for models like Random Forest and XGBoost.

### 6. Feature Grouping & Range Filtering
- Group BMI into ranges and filter the dataset based on feature ranges before training.

### 7. AUC Calculation
- Calculate AUC for training and validation sets to assess model performance.

### 8. Results Output
- Save accuracy and AUC results, and export ROC curve images.

### 9. Additional Analysis
- Calculate Variance Inflation Factor (VIF) to detect multicollinearity and plot correlation matrices.
