# MovieGenrePrediction
The Aim of this project is to predict movie genres from movie description. The data used here is from kaggle's movie dataset(https://www.kaggle.com/rounakbanik/the-movies-dataset).

### Strategy Used:
Problem Transformation approach for Multi-label Classification Problem
1. Data Preprocessing :
- Used libraries like nltk and re to preprocess the text data. 
- TFIDF vectorizer for converting preprocessed text into matrix of TF-IDF features(Used top 10000 Features).
- For Target, Used Multi-Label Binarizer to convert Genres into a (samples x classes) binary matrix indicating the presence of a class label.

2. Model Building :
- As this problem is multi-label classification problem, I have used OneVsRestClassifier Algorithm.
- Multiple model  were built using different Sklearn classifiers with OneVsRest Classifier.
- GridSearchCV is used for cross validation and selection of best hyperparameters.

3.Results and Comparision :
Performance of Models on test data, Miro F1_score is used as evaluation metric (class imbalance) 
- LogisticRegression, F1Score : 0.52
- LinearSVC, F1Score : 0.50
- Random Forect Classifier : 0.48
- XGBoost Classifier : 0.30
- LightGradient Boosting Classifier: 0.45,

Among all these models Logistic regression results were better.

### Further Improvements:
- The same problem can also be solved using deep Learning LSTMs and CNNs. 

### References used for this problem are:
1. Predicting Movie Genres using NLP - https://www.analyticsvidhya.com/blog/2019/04/predicting-movie-genres-nlp-multi-label-classification/
2.Machine Learning - Text Classification with Python, nltk, Scikit & Pandas - https://www.youtube.com/watch?v=5xDE06RRMFk&t=1003s
