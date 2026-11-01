# Heart Failure Mortality Prediction

## Project overview

This project explores the Heart Failure Clinical Records dataset and uses classification models to predict whether a death event was recorded during patient follow-up (DEATH_EVENT). The notebook covers an initial data audit, preprocessing, model evaluation and a comparison with a simple baseline. The analysis is exploratory and is not intended for clinical decision-making.

## Dataset and repository contents

The dataset contains 299 patient records and 13 variables, including the target DEATH_EVENT (0 = no recorded death event, 1 = recorded death event). There are 203 records in class 0 and 96 in class 1. The follow-up duration variable (`time`) is not used as a model predictor.

The repository contains the following files:

- `Heart_Mortality_Prediction.ipynb` :- Jupyter notebook with the analysis and results.
- `heart_failure_clinical_records_dataset.csv` :- Dataset used by the notebook.
- `requirements.txt` :- Python package requirements.
- `README.md` :- Project overview and instructions.

## Software and package requirements

A Python environment with Jupyter Notebook is required. The notebook uses NumPy, pandas, Matplotlib, Seaborn and scikit-learn. The required Python packages are listed in `requirements.txt`, including `notebook` or `jupyter` for launching the notebook.

## Setup and instructions to run

1. Download the repository files and keep the notebook and `heart_failure_clinical_records_dataset.csv` in the same folder. The notebook reads the CSV using its filename rather than an absolute path.
2. Open the folder in Jupyter Notebook (for example, by launching Jupyter Notebook from Anaconda Navigator and navigating to the folder).
3. Install any missing packages from `requirements.txt`. In a terminal or Anaconda Prompt, run:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Open `Heart_Mortality_Prediction.ipynb` and select a Python kernel with the installed packages.
5. Use **Kernel → Restart & Run All** to execute the notebook from beginning to end. Running the notebook generates the analysis tables, plots and model evaluation results.

## Work completed in the notebook

The notebook includes data exploration, preprocessing, model training and evaluation.

The dataset is checked for missing values, duplicates, data distribution and potential outliers using boxplots and the IQR method.

The data is divided into training (239), validation (30) and test (30) sets using stratified sampling. Preprocessing includes missing-value imputation, standardisation and feature selection using SelectKBest. A 5-fold stratified cross-validation approach is used for model evaluation.

A baseline model (DummyClassifier) is compared with three classification algorithms:

- Logistic Regression
- Decision Tree
- Random Forest

Model performance is assessed using accuracy, balanced accuracy, precision, recall, F1-score and ROC-AUC. Balanced accuracy is used to select the best-performing model because the dataset has an unequal number of observations in each class.

Detailed analysis, visualisations and model results are available in the Jupyter notebook.

## Repository link

[Heart Failure Mortality Classification GitHub repository](https://github.com/sharadamarathe54-ctrl/heart-failure-mortality-classification)

## References

The following articles and technical documentation provide background information and Python implementation examples relevant to the machine learning methods used in this project.

1. Brownlee, J. (2021). *How to Develop a Random Forest Ensemble in Python*. Machine Learning Mastery.  
   https://machinelearningmastery.com/random-forest-ensemble-in-python/

2. Brownlee, J. (2019). *How To Implement The Decision Tree Algorithm From Scratch In Python*. Machine Learning Mastery.  
   https://machinelearningmastery.com/implement-decision-tree-algorithm-scratch-python/

3. GeeksforGeeks. *Logistic Regression in Machine Learning*.  
   https://www.geeksforgeeks.org/machine-learning/understanding-logistic-regression/

4. GeeksforGeeks. *Random Forest Classifier using Scikit-learn*.  
   https://www.geeksforgeeks.org/random-forest-classifier-using-scikit-learn/

5. Scikit-learn Developers. *Column Transformer with Mixed Types*.  
   https://scikit-learn.org/stable/auto_examples/compose/plot_column_transformer_mixed_types.html

6. Scikit-learn Developers. *SelectKBest — Univariate Feature Selection*.  
   https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html

7. Scikit-learn Developers. *StratifiedKFold — Cross-validation*.  
   https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.StratifiedKFold.html

8. Scikit-learn Developers. *Classification Metrics and Model Evaluation*.  
   https://scikit-learn.org/stable/modules/model_evaluation.html

9. UCI Machine Learning Repository. (2020). *Heart Failure Clinical Records*.  
   https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records

10. Chicco, D., & Jurman, G. (2020). Machine learning can predict survival of patients with heart failure from serum creatinine and ejection fraction alone. *BMC Medical Informatics and Decision Making, 20*, 16.  
    https://doi.org/10.1186/s12911-020-1023-5

## AI Use Declaration

AI tools were used as supplementary resources to support conceptual understanding and learning. The analysis, implementation, and interpretation of results reflect my own work and understanding.