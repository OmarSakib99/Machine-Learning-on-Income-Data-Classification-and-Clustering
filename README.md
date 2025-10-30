# Income Prediction and Clustering Analysis

This project explores a dataset containing income information to perform both classification and clustering tasks. The goal is to predict income levels and identify potential groupings within the data.

## Project Steps

1.  **Data Loading and Preprocessing**:
    *   Loaded the `income.csv` dataset.
    *   Checked for missing values and dropped rows with missing information.
    *   Identified and removed duplicate entries.
    *   Examined variable data types.
    *   Analyzed the value counts for categorical features.

2.  **Feature Engineering**:
    *   Encoded binary categorical variables (`sex`) using numerical representation.
    *   Encoded ordinal categorical variables (`education`) with a numerical scale.
    *   Applied one-hot encoding to other nominal categorical variables (`workclass`, `marital-status`, `occupation`, `relationship`, `race`).

3.  **Model Building and Evaluation (Classification)**:
    *   Split the dataset into training and testing sets.
    *   Applied Min-Max scaling to normalize the features.
    *   Built and evaluated two classification models: Logistic Regression and Support Vector Machine (SVC).
    *   Performed 10-fold cross-validation to assess the average accuracy of the models.
    *   Optimized the Logistic Regression model using GridSearchCV to find the best hyperparameters.
    *   Evaluated the optimized Logistic Regression model on the testing dataset.
    *   Optimized the Support Vector Machine model using GridSearchCV to find the best hyperparameters.
    *   Evaluated the optimized Support Vector Machine model on the testing dataset.

4.  **Clustering Analysis (K-Means)**:
    *   Applied K-Means clustering with 2 clusters to the normalized training data.
    *   Examined the number of samples in each cluster.
    *   Identified prototype samples for each cluster.
    *   Evaluated the accuracy of the K-Means clustering results by comparing cluster labels to the original income variable.
    *   Used the Elbow method to determine the optimal number of clusters.

## Key Findings

*   The dataset initially contained missing values and duplicates, which were addressed during the preprocessing phase.
*   After preprocessing, the dataset was reduced to 21,537 unique entries.
*   Both Logistic Regression and Support Vector Machine models achieved similar average cross-validation accuracies (around 80.8% for LR and 80.0% for SVC) on the training data.
*   Hyperparameter tuning with GridSearchCV slightly improved the average cross-validation accuracy for both models.
*   The testing accuracy for the optimized Logistic Regression model was approximately 78.8%, and for the optimized SVC model was approximately 79.3%.
*   The K-Means clustering analysis with 2 clusters showed an accuracy of around 63% when comparing cluster assignments to the income variable. This suggests that while there are some patterns, income is not strictly separable into two clusters based on the available features using K-Means.
*   The Elbow method indicated that 2 or 3 clusters might be appropriate for this dataset.

This project provides a basic analysis of the income dataset using common machine learning techniques for classification and clustering. Further work could involve exploring other algorithms, more advanced feature engineering, or different evaluation metrics.
