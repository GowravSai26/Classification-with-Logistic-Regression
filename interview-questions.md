# Task 4: Interview Questions and Answers

### 1. How does logistic regression differ from linear regression?
The fundamental difference lies in the type of problem they solve.

* **Linear Regression** is used for **regression tasks**, where the goal is to predict a **continuous numerical value** (e.g., predicting the price of a house). Its output can be any real number.
* **Logistic Regression** is used for **classification tasks**, where the goal is to predict a **categorical outcome** (e.g., predicting if a tumor is malignant or benign). Its output is a probability between 0 and 1.

---
### 2. What is the sigmoid function?
The sigmoid function is the core mathematical function in logistic regression. It's an "S"-shaped curve that takes any real-valued number and maps it to a value between 0 and 1. This output is then interpreted as a probability.

The formula is:
$$S(z) = \frac{1}{1 + e^{-z}}$$



---
### 3. What is precision vs recall?
Precision and recall are two essential metrics for evaluating a classifier, especially when classes are imbalanced.

* **Precision:** Answers the question, "Of all the times the model predicted a positive outcome, how often was it correct?" It measures the quality of the positive predictions.
    $$ \text{Precision} = \frac{\text{True Positives}}{\text{True Positives + False Positives}} $$

* **Recall:** Answers the question, "Of all the actual positive cases, how many did the model correctly identify?" It measures the model's ability to find all positive instances.
    $$ \text{Recall} = \frac{\text{True Positives}}{\text{True Positives + False Negatives}} $$

There is often a trade-off between the two; improving one can lower the other.

---
### 4. What is the ROC-AUC curve?
* **ROC (Receiver Operating Characteristic) Curve:** This is a graph that shows a classifier's performance across all possible thresholds. It plots the **True Positive Rate (Recall)** against the **False Positive Rate**.
* **AUC (Area Under the Curve):** This is a single number that represents the entire area underneath the ROC curve.

**Significance:** An AUC of 1.0 means the model is a perfect classifier, while an AUC of 0.5 means the model is no better than random guessing. It helps summarize a model's overall performance.

---
### 5. What is the confusion matrix?
A confusion matrix is a table that summarizes the performance of a classification model by showing the counts of correct and incorrect predictions for each class. It's the basis for calculating most other classification metrics.

The matrix is structured as follows:

|                   | **Predicted: Negative** | **Predicted: Positive** |
| :---------------- | :-------------------- | :-------------------- |
| **Actual: Negative** | True Negative (TN)    | False Positive (FP)   |
| **Actual: Positive** | False Negative (FN)   | True Positive (TP)    |

---
### 6. What happens if classes are imbalanced?
If the classes are imbalanced (e.g., 99% of data is class A and 1% is class B), a model can achieve very high accuracy by simply always predicting the majority class. This makes the model useless for identifying the minority class. In such cases, **accuracy** is a misleading metric, and you should rely on **precision, recall, and the F1-score** instead.

---
### 7. How do you choose the threshold?
The classification threshold (by default 0.5) is the probability value used to make a final decision. The optimal threshold depends entirely on the business problem and the cost of errors.

* If the cost of a **False Negative** is high (e.g., failing to detect a disease), you would **lower the threshold** to increase recall (catch more true positives).
* If the cost of a **False Positive** is high (e.g., flagging a valid transaction as fraud), you would **raise the threshold** to increase precision.

---
### 8. Can logistic regression be used for multi-class problems?
Yes. While logistic regression is naturally a binary classifier, it can be extended for multi-class classification using two main strategies:

* **One-vs-Rest (OvR):** Trains a separate binary classifier for each class against all other classes combined.
* **Multinomial Logistic Regression:** Uses a "softmax" function, which is a generalization of the sigmoid function, to output a probability for each of the multiple classes. Most modern libraries like scikit-learn handle this automatically.