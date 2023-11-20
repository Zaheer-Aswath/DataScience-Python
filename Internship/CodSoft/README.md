This repository contains the projects I have done during my course of Intership with CodSoft

**Project 1 - TITANIC SURVIVAL PREDICTION**
* Use the Titanic dataset to build a model that predicts whether a passenger on the Titanic survived or not.
* The dataset typically used for this project contains information about individual passengers, such as their age, gender, ticket class, fare, cabin, and whether or not they survived.
* **Uploaded file name:** Codsoft - Data science Internship - Task-1 - TITANIC SURVIVAL PREDICTION
* **Dataset from kaggle:** https://www.kaggle.com/datasets/brendan45774/test-file/
* **Model used:** LogisticRegression
* **Reason for choosing the model:** The target variable in the Titanic dataset is binary: survived (1) or did not survive (0). Logistic Regression is a reasonable starting point given its suitability for binary classification tasks. It is computationally efficient and can handle datasets with a moderate number of features. Logistic Regression performed well with the best accuracy score and hence I settled with the same model.

**Project 2 - IRIS FLOWER CLASSIFICATION**
* The Iris flower dataset consists of three species: setosa, versicolor and virginica. These species can be distinguished based on their measurements. Now, imagine that you have the measurements of Iris flowers categorized by their respective species. Your objective is to train a machine learning model that can learn from these measurements and accurately classify the Iris flowers into their respective species.
* Use the Iris dataset to develop a model that can classify iris flowers into different species based on their sepal and petal measurements.
* **Uploaded file name:** Codsoft - Data science Internship - Task-2 - IRIS FLOWER CLASSIFICATION
* **Dataset from kaggle:** https://www.kaggle.com/datasets/arshid/iris-flower-dataset
* **Model used:** KNeighborsClassifier
* **Reason for choosing the model:** KNN model is straight forward and best suited for smaller dataset, hence it was a reasonable choice given the characteristics of the Iris Flower Classification dataset. The distance-based approach of KNN is well-suited for scenarios where similar instances tend to belong to the same class. Also, KNN provides a parameter (n_neighbors) that allows you to experiment with the number of neighbors considered during prediction. This flexibility makes it easy to observe how changes in this parameter affect the model's performance.

**Project 3 - CREDIT CARD FRAUD DETECTION**
* Build a machine learning model to identify fraudulent credit card transactions.
* Preprocess and normalize the transaction data, handle class imbalance issues, and split the dataset into training and testing sets.
* Train a classification algorithm, such as logistic regression or random forests, to classify transactions as fraudulent or genuine.
* Evaluate the model's performance using metrics like precision, recall, and F1-score, and consider techniques like oversampling or undersampling for improving results.
* **Uploaded file name:** Codsoft - Data science Internship - Task-3 - CREDIT CARD FRAUD DETECTION
* **Dataset from kaggle:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
* **Model used:** RandomForestClassifier Model. Also, used the model with Oversampling method and with Undersampling method
* **Reason for choosing the model:** Credit card fraud datasets often suffer from class imbalance, where fraudulent transactions are rare compared to genuine ones. Random Forest can handle imbalanced datasets to some extent and is less likely to be biased towards the majority class. Random Forest provides a feature importance measure, allowing you to understand the contribution of each feature in making predictions. This can be valuable for interpretability in fraud detection. Also, it can handle noisy and irrelevant features well. In credit card fraud detection, where some features might not be informative, this robustness can be beneficial.
