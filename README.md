# 🏠 Advanced House Price Prediction with Regularized Regression

![GitHub repo size](https://img.shields.io/github/repo-size/your-username/your-repo-name)
![GitHub stars](https://img.shields.io/github/stars/your-username/your-repo-name?style=social)
![GitHub forks](https://img.shields.io/github/forks/your-username/your-repo-name?style=social)

A machine learning project that predicts house sale prices using Linear, Ridge, and Lasso regression models. This repository explores the impact of L1 and L2 regularization on model performance and feature selection.

---

### 📋 Table of Contents
* [Project Overview](#project-overview)
* [Dataset](#dataset)
* [Project Workflow](#project-workflow)
* [Models Implemented](#models-implemented)
* [Evaluation Metrics](#evaluation-metrics)
* [Results Summary](#results-summary)
* [Technologies Used](#technologies-used)
* [Setup and Usage](#setup-and-usage)
* [License](#license)

---

### 📝 Project Overview

This project aims to build a robust model to accurately predict house sale prices. The core objective is to compare a baseline **Linear Regression** model with regularized alternatives—**Ridge (L2)** and **Lasso (L1) Regression**. By doing so, we can observe how regularization helps in preventing overfitting, handling multicollinearity, and performing feature selection, ultimately leading to a more generalized and accurate model.

---

### 📊 Dataset

The project uses the **Ames Housing dataset**, which contains 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa. 

**Key features include:**
* `GrLivArea`: Above grade (ground) living area square feet
* `TotalBsmtSF`: Total square feet of basement area
* `OverallQual`: Rates the overall material and finish of the house
* `YearBuilt`: Original construction date
* `SalePrice`: The property's sale price in dollars (this is the target variable).

---

### ⚙️ Project Workflow

1.  **Data Loading & Initial Exploration:** The dataset is loaded, and its basic properties are examined.
2.  **Exploratory Data Analysis (EDA):** In-depth analysis and visualization are performed to understand feature distributions, correlations, and relationships with the target variable (`SalePrice`).
3.  **Data Preprocessing & Feature Engineering:**
    * Handling missing values.
    * Encoding categorical features (e.g., using One-Hot Encoding).
    * Transforming skewed features (e.g., using log transformation).
    * Scaling numerical features.
4.  **Model Training:** The preprocessed data is used to train the three regression models.
5.  **Hyperparameter Tuning:** For Ridge and Lasso, techniques like cross-validation are used to find the optimal `alpha` (regularization strength).
6.  **Model Evaluation:** The models are evaluated on a held-out test set using various metrics.
7.  **Conclusion:** The results are analyzed to determine the best-performing model.

---

### 🧠 Models Implemented

* **Linear Regression:** A baseline model to establish a benchmark for performance. It fits a linear equation to the data but can be sensitive to outliers and multicollinearity.
* **Ridge Regression (L2 Regularization):** This model adds a penalty term proportional to the square of the magnitude of coefficients. It's effective at shrinking coefficients and preventing overfitting, especially when features are highly correlated.
* **Lasso Regression (L1 Regularization):** This model adds a penalty term proportional to the absolute value of the coefficients. A key advantage is its ability to perform automatic feature selection by shrinking the coefficients of less important features to exactly zero.

---

### 📈 Evaluation Metrics

The models are compared based on the following metrics:
* **R-squared ($R^2$)**: The proportion of the variance in the target variable that is predictable from the features.
* **Mean Absolute Error (MAE)**: The average absolute difference between the predicted and actual values.
* **Root Mean Squared Error (RMSE)**: The square root of the average of squared differences between prediction and actual observation. It penalizes larger errors more.

---

### 🏆 Results Summary

The performance of the models on the test set is summarized below.

| Model               | R² Score | Mean Absolute Error (MAE) | Root Mean Squared Error (RMSE) |
| ------------------- | :------: | :-----------------------: | :----------------------------: |
| Linear Regression   |   0.89   |          \$21,500         |            \$31,000            |
| **Ridge Regression**| **0.91** |        **\$19,800** |          **\$28,500** |
| Lasso Regression    |   0.90   |          \$20,100         |            \$29,200            |

*(Note: These are example values. Replace them with your actual results.)*

**Conclusion:** The **Ridge Regression** model provided the best performance across all metrics, demonstrating the effectiveness of L2 regularization in creating a more robust and accurate model for this dataset.

---

### 💻 Technologies Used
* **Python 3.x**
* **Pandas & NumPy** for data manipulation and numerical operations.
* **Matplotlib & Seaborn** for data visualization.
* **Scikit-learn** for modeling, preprocessing, and evaluation.
* **Jupyter Notebook** for project development and documentation.

---

### 🚀 Setup and Usage

To run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/house-price-prediction.git](https://github.com/your-username/house-price-prediction.git)
    cd house-price-prediction
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook "House Price Prediction.ipynb"
    ```

---

### 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
