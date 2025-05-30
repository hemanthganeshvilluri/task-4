Ⅰ. Dataset Selection
We use the Breast Cancer dataset provided by Scikit-learn, which is a commonly used dataset for binary classification. It contains 569 samples of tumors, labeled as either malignant (0) or benign (1), along with 30 numeric features describing the tumor characteristics.

Ⅱ. Data Preparation
The data is loaded and separated into:
   ->Feature matrix (X): Contains the 30 numeric input features.
   ->Target vector (y): Contains binary class labels.
The features and labels are converted into Pandas structures for easier manipulation.

Ⅲ. Train-Test Split & Standardization
The dataset is split into a training set and a test set to evaluate model performance. To ensure reproducibility, a random_state is set during the split.
Feature standardization is performed using a scaler to normalize the input values. This improves model convergence and performance, especially for algorithms like logistic regression.

Ⅳ. Model Training
A Logistic Regression model is created and trained using the training set. This model is suitable for binary classification tasks and uses the sigmoid function to predict probabilities between 0 and 1.

Ⅴ. Model Evaluation
The performance of the model is evaluated on the test set using various metrics:
   ->Confusion Matrix: Shows TP, TN, FP, FN.
   ->Precision & Recall: Measure the accuracy of positive predictions and the ability to find all positives.
   ->F1-Score: Harmonic mean of precision and recall.
ROC Curve and AUC Score: Evaluate the trade-off between true positive rate and false positive rate.

Ⅵ. Threshold Tuning and Sigmoid Explanation
By default, logistic regression uses a threshold of 0.5 to classify samples. This threshold can be adjusted based on use-case requirements (e.g., reducing false negatives).
The sigmoid function used in logistic regression is defined as:
𝜎(𝑧)=1/(1+𝑒^(−𝑧)) 
It maps any real-valued number to a value between 0 and 1, which is interpreted as the probability of the positive class.

Ⅶ. Conclusion
This project demonstrates a full machine learning pipeline for binary classification using logistic regression. It emphasizes data preprocessing, model training, and evaluation, giving a clear overview of performance and interpretability in binary classification problems.
