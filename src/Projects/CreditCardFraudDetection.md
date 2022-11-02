# Credit Card Fraud Detection

>[!summary] Applied Multiple predictive models on CC transaction data to predict whether a CC transaction is fraudulent or not, based on transaction amount, location and other transaction related data.


## Problem Statement
The Credit Card Fraud Detection Problem includes modeling past credit card transactions with the knowledge of the ones that turned out to be a fraud. This model is then used to identify whether a new transaction is fraudulent or not. Our aim here is to detect 100% of the fraudulent transactions while minimizing the incorrect fraud classifications.

## Observations about data
- Highly unbalanced(skewed) data.
	- 492 frauds in 284,807 obs.
- features are numerical values resultant of PCA transformations on original dataset.
- No metadata about original features.
- No missing values.

## Business Questions


## Todos
- [ ] Learn every terminology used in the project thoroughly.
- [ ] Identify how to do this at low level.
- [ ] Watch [youtube videos](https://www.youtube.com/results?search_query=credit+card+fraud+detection) on this topic.
- [ ] Learn more about Credit Card Frauds and how to prevent them.
- [ ] Revise Precision-Recall-f1-Confusion matrix.
- [ ] Type-1 and Type-2 error
- [ ] Revise PCA
- [ ] Test-Train-Validation data
- [ ] Underfitting vs Overfitting
- [ ] Correlation in terms of model features
- [ ] Risk of collinearity
- [ ] oversampled vs undersampled dataset

## Learnings
- Dealing with imbalanced datasets
	> Q: Why does imbalance affect model performance?
	> 
	> A: In general, we want to maximize recall while capping False Positive Rate. But you can classify a lot of charges wrong and still maintain low FPR bc you have large no of true negatives. [^1]
- [More from titles of other notebooks]


# References
- [Google Colab](https://colab.research.google.com/drive/1kUYCtdo6q1ZaiPqXkL-VITU1E5eXUJaJ?usp=sharing)
- Dataset - [Credit Card Fraud Detection Dataset| Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/code)
- Sample Notebooks
	1. [Credit Card Fraud Detection Predictive Models | Kaggle](https://www.kaggle.com/code/gpreda/credit-card-fraud-detection-predictive-models/)
	2. [💳Credit Card Fraud💸Detection🚨ANNs vs XGBoost | Kaggle](https://www.kaggle.com/code/faressayah/credit-card-fraud-detection-anns-vs-xgboost/notebook)
	3. [🏆✍💻Credit Card Fraud Detection-Different Models | Kaggle](https://www.kaggle.com/code/dhirajkumar612/credit-card-fraud-detection-different-models)
- [Fraud Detection with ML - Researchgate](https://www.researchgate.net/project/Fraud-detection-with-machine-learning)
- [Reproducible Machine Learning for Credit Card Fraud detection - Practical handbook](https://fraud-detection-handbook.github.io/fraud-detection-handbook/index.html)
- [Krish-Naik: Credit Card Fraud Detection using Machine Learning from Kaggle - YouTube](https://youtu.be/frM_7UMD_-A)
- [Project 10. Credit Card Fraud Detection using Machine Learning in Python | Machine Learning Projects - YouTube](https://youtu.be/NCgjcHLFNDg)
- [^1]: https://www.kaggle.com/code/faressayah/credit-card-fraud-detection-anns-vs-xgboost/notebook#Why-does-class-imbalanced-affect-model-performance?
- https://muthu.co/mathematics-of-principal-component-analysis/