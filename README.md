# Bank Marketing ML — Term Deposit Prediction
This project applies supervised machine learning techniques to predict whether a bank customer will subscribe to a term deposit based on demographic, financial, and campaign-related features. The goal is to evaluate and compare multiple classification models and use data visualization to support model interpretation and performance analysis.

## How to get started
In order to get this project running please download the code using the git clone command

  - 'git clone git@github.com:ashrivastav33/bank-marketing-ml-classifiers.git'

## Note
- We are making an assumption you already are familiar with using Jupyter Notebook using tools like Google Colab or Jupyter etc.
- You will need an internet connection to download/read the dataset or csv file

## Project Structure

### - /data/bank-additional-full.csv    ---> Stores the dataset used for this project
### - /code/bank-marketing-ml_ashri33.ipynb            ---> Stores the code/jupyter notebook used for this project

# Dataset

  - Source: Bank Marketing Dataset
  - Target Variable: y (Subscription: yes/no)
  - Feature Types:
       - Categorical: job, marital status, education, contact, month, housing, loan
       - Continuous: age, campaign, duration, euribor3m, emp.var.rate, cons.price.idx

## Results

Confusion Matrix for KNN classifier

<img width="437" height="389" alt="image" src="https://github.com/user-attachments/assets/a13595b6-464c-4b51-969e-ba60b2960230" />

Model Training time and accuracy

| Model | Train_Time | Train_Accuracy | Test_Accuracy |
|---|---|---|---|
| Logistic Regression | 0.834787 | 0.901123 | 0.897305 |
| KNN	| 0.016028 | 0.913505	| 0.888080 |
| Decision Tree | 0.396105 | 0.995357	| 0.838917 |
| SVM	| 185.017094	| 0.905250	| 0.896941 |



## Conclusion

- Logistic Regression and SVM achieved the strongest overall performance, with the highest test accuracy (~89.7%) and solid AUC scores.
- SVM matched Logistic Regression in accuracy but required significantly longer training time, making it less efficient computationally.
- KNN showed competitive accuracy and minimal training time,
- Decision Trees exhibited overfitting, with near-perfect training accuracy but noticeably lower test accuracy.
- The confusion matrix shows that all models perform better at predicting non-subscribers than subscribers, highlighting class imbalance and the need for threshold tuning or class weighting.

### Learning

- This was a fun and helpful learning exercise that made it easier to understand how different machine learning models perform on real data.
- Comparing the models helped show that training time can increase a lot with larger datasets, especially for more complex models like SVM.
- Overall, the exercise helped build confidence in evaluating models using multiple metrics and understanding that model selection involves trade-offs, not just accuracy.
  
## Next Steps and Recommendations

 - We can explore more scenarios to learn meaningful insights
 - Relying solely on accuracy can be misleading due to class imbalance; evaluating precision, recall, and F1-score provides a more complete and reliable assessment of model performance, particularly for identifying subscribed customers.

