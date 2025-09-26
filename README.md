# Task 4: Logistic Regression for Breast Cancer Classification

## Project Objective
The objective of this project is to build a binary classifier using logistic regression. The model is trained on the Breast Cancer Wisconsin Dataset to predict whether a tumor is malignant or benign.

---

## Workflow

The project follows a standard machine learning workflow from data preparation to model evaluation.

### 1. Data Preparation
* **Dataset Loading:** The Breast Cancer Wisconsin Dataset was loaded from Scikit-learn.
* **Train-Test Split:** The data was split into training and testing sets to ensure the model is evaluated on unseen data.
* **Feature Standardization:** All features were standardized (scaled) to have a mean of 0 and a standard deviation of 1. This is a crucial step for logistic regression to perform effectively.

### 2. Model Training
A `LogisticRegression` model from the Scikit-learn library was fitted to the standardized training data.

### 3. Model Evaluation
The model's performance was thoroughly evaluated using several key classification metrics:
* **Confusion Matrix:** A confusion matrix was generated to visualize the number of true positives, true negatives, false positives, and false negatives.
* **Classification Report:** A report was created to analyze the model's **precision** and **recall** for each class.
* **ROC-AUC Curve:** The Receiver Operating Characteristic (ROC) curve was plotted, and the Area Under the Curve (AUC) was calculated to assess the model's performance across all classification thresholds.

### 4. Sigmoid Function and Threshold Tuning
* **Sigmoid Function:** The role of the sigmoid function in converting the model's output into a probability between 0 and 1 was explained and visualized.
* **Threshold Tuning:** The process of adjusting the default classification threshold (0.5) was demonstrated to show how it can be tuned to optimize for either precision or recall, depending on the specific problem.

---

## Tools and Libraries Used
* **Python**
* **Pandas**
* **Scikit-learn**
* **Matplotlib** & **Seaborn**

---

## How to Run

1.  Clone the repository to your local machine.
2.  Create and activate a Python virtual environment.
3.  Install the required dependencies from the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```
4.  Open and run the Jupyter Notebook (`.ipynb` file) in a compatible editor like VS Code.
---

## How to Run

1.  Clone the repository to your local machine.
2.  Create and activate a Python virtual environment.
3.  Install the required dependencies from the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```
4.  Open and run the Jupyter Notebook (`.ipynb` file) in a compatible editor like VS Code.