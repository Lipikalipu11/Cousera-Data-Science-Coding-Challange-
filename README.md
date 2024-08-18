# Cousera-Data-Science-Coding-Challange-

Introduction 
In this challenge, I had the opportunity to address a critical and industry-relevant machine learning problem: predicting loan defaults. By leveraging a unique dataset of individuals who received loans in 2021, I developed a model aimed at identifying those at the highest risk of defaulting on their loan payments.

Throughout this task, I approached the problem with the perspective of a data scientist working for a major financial institution, where the goal was to enhance the allocation of resources to borrowers who may need additional support. By predicting the likelihood of defaults, the institution can deploy targeted interventions effectively, reducing the risk of non-payment and improving overall financial outcomes.

The process involved thorough data exploration, feature engineering, and the application of machine learning algorithms to create a predictive model. The final model, with an AUC of 0.75, demonstrated a fair ability to distinguish between those who are likely to default and those who are not, providing valuable insights for the institution.

Overall, this challenge underscored the importance of predictive modeling in financial services and highlighted the potential for data-driven decision-making to enhance operational efficiency and customer support.

Understanding the Datasets
Train vs. Test
In this competition, you’ll gain access to two datasets that are samples of past borrowers of a financial institution that contain information about the individual and the specific loan. One dataset is titled train.csv and the other is titled test.csv.
train.csv contains 70% of the overall sample (255,347 borrowers to be exact) and importantly, will reveal whether or not the borrower has defaulted on their loan payments (the “ground truth”).
The test.csv dataset contains the exact same information about the remaining segment of the overall sample (109,435 borrowers to be exact), but does not disclose the “ground truth” for each borrower. It’s your job to predict this outcome!
Using the patterns you find in the train.csv data, predict whether the borrowers in test.csv will default on their loan payments, or not.
Dataset descriptions
Both train.csv and test.csv contain one row for each unique Loan. For each Loan, a single observation (LoanID) is included during which the loan was active.
In addition to this identifier column, the train.csv dataset also contains the target label for the task, a binary column Default which indicates if a borrower has defaulted on payments.
Besides that column, both datasets have an identical set of features that can be used to train your model to make predictions. Below you can see descriptions of each feature. Familiarize yourself with them so that you can harness them most effectively for this machine learning task!

<img width="879" alt="Screenshot 2024-08-18 at 7 21 49 PM" src="https://github.com/user-attachments/assets/02b43db7-6d03-429c-9585-15a084e8411e">

#Model Prediction 

Fitting Logistic regression 
<img width="961" alt="Screenshot 2024-08-18 at 7 27 03 PM" src="https://github.com/user-attachments/assets/cfc8c8e9-4a7a-456b-b474-f4a51255da9b">


Model Prediction: The model produced predictions (y_pred) indicating whether each individual in the test set is likely to default (1) or not (0).
Model Accuracy: The model achieved an accuracy of approximately 88.6% (0.8859). This indicates that the model correctly classified about 88.6% of the instances in the test set. While this is a relatively high accuracy, it's important to consider other metrics, such as precision, recall, or the AUC, to ensure the model performs well across different aspects of prediction, especially in cases of imbalanced datasets.
Predicted Probabilities: The model also provided predicted probabilities (y_pred_prob) for the likelihood of default for each individual. The shape of the predicted probabilities is consistent with the number of test samples (51,070), confirming that a probability score was generated for each test instance.
Interpretation of Predicted Probabilities: The predicted probabilities range from values like 0.033 to 0.089, suggesting that the model generally predicts a low likelihood of default for most individuals in the test set. This indicates that the model might be conservative in predicting defaults, possibly reflecting the distribution of the data where non-defaults are more common.
Overall Assessment:
The logistic regression model shows strong predictive performance with an accuracy of 88.6%, and it is able to provide detailed probabilities that can be used for further analysis or decision-making. However, it is important to further evaluate the model's performance using additional metrics, especially if there is a significant class imbalance between defaulters and non-defaulters in the dataset.

<img width="780" alt="Screenshot 2024-08-18 at 7 15 37 PM" src="https://github.com/user-attachments/assets/aeff6fae-e6ab-4ab6-8c8f-992d25a23c47">

AUC Value: The AUC value is approximately 0.75. This indicates that the model has a fair ability to distinguish between the positive and negative classes. An AUC of 0.75 means that there is a 75% chance that the model will correctly distinguish a randomly chosen positive instance from a randomly chosen negative instance.

Model Performance:
A perfect model would have an AUC of 1.0, which indicates that the model is excellent at distinguishing between classes.
An AUC of 0.5 represents a model with no discriminative power, equivalent to random guessing.
An AUC of 0.75 suggests that the model performs better than random guessing, but there is still room for improvement.

ROC Curve:
The ROC curve itself shows the trade-off between the True Positive Rate (Sensitivity) and the False Positive Rate (1 - Specificity) for different threshold values.
The curve being above the diagonal line (which represents random guessing) confirms that the model has predictive power.

Conclusion:
The model demonstrates fair discriminatory ability, with an AUC of 0.75, indicating that it is reasonably effective in distinguishing between the two classes but could benefit from further optimization to improve its predictive performance.

Result :
<img width="517" alt="Screenshot 2024-08-18 at 7 30 06 PM" src="https://github.com/user-attachments/assets/2c909cba-f1a7-4443-ac8a-fcc450c629e5">

Finally cleared the challange with the grade of 73%






