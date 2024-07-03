### MNIST Digit Classification

This Jupyter Notebook explores the MNIST handwritten digit dataset, a classic machine learning problem. The goal is to train a classifier to accurately recognize handwritten digits (0-9).

**Key Steps:**

1. **Data Preparation:**
   - The MNIST dataset is loaded from the `sklearn` library.
   - The dataset is split into training and testing sets.
   - The labels are converted to integers for easier processing.

2. **Binary Classification:**
   - A binary classifier ("5-detector") is created to distinguish between the digit '5' and all other digits.
   - A Stochastic Gradient Descent (SGD) classifier is chosen for its efficiency in handling large datasets.
   - The classifier is trained on the training set.

3. **Performance Evaluation:**
   - Stratified K-Fold cross-validation is used to assess the model's accuracy.
   - A custom `Never5Classifier` is created as a baseline for comparison.
   - A confusion matrix is computed to analyze the types of errors the model makes.
   - Precision, recall, and F1-score are calculated to evaluate the model's performance in more detail.

4. **Precision/Recall Tradeoff:**
   - The relationship between precision and recall is explored by varying the decision threshold.
   - A plot is generated to visualize this tradeoff.

5. **ROC Curve:**
   - The Receiver Operating Characteristic (ROC) curve is plotted to assess the model's ability to distinguish between classes.
   - The Area Under the Curve (AUC) is calculated as a single metric summarizing the ROC curve.
   - The SGD classifier is compared to a Random Forest classifier using ROC curves and AUC.

6. **Multiclass Classification:**
   - The problem is extended to multiclass classification (recognizing all 10 digits).
   - A Support Vector Machine (SVM) classifier is used.
   - The classifier's predictions and decision scores are examined.

7. **Error Analysis:**
   - Cross-validation is performed again with the SGD classifier on scaled data.
   - A confusion matrix is plotted to visualize the errors.
   - The matrix is normalized to focus on the types of errors the model makes relative to the true class.

**Dependencies:**

- numpy
- pandas
- matplotlib
- scikit-learn

**How to Use:**

1. Clone this repository.
2. Install the required dependencies.
3. Run the Jupyter Notebook to train and evaluate the classifiers.
4. Explore the visualizations and metrics to understand the model's performance.
