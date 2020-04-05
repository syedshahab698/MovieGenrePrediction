# MovieGenrePrediction
The Aim of this project is to predict movie genres from movie description. The data used here is from kaggle's movie dataset(https://www.kaggle.com/rounakbanik/the-movies-dataset).

### Strategy Used:
Multi-label Classification Problem
1. Data Preprocessing :
- Used libraries like nltk and re to preprocess the text data. 
- TFIDF vectorizer for converting preprocessed text into matrix of TF-IDF features(Used top 10000 Features).
- For Target, Used Multi-Label Binarizer to convert Genres into a (samples x classes) binary matrix indicating the presence of a class label.

2. Model Building :
- As this problem is multi-label classification problem, I have used OneVsRestClassifier Algorithm.
- Multiple model  were built using different Sklearn classifiers with OneVsRest Classifier.
- GridSearchCV is used for cross validation and selection of best hyperparameters.

3.Results and Comparision :


### References used for this problem are:
1. Predicting Movie Genres using NLP - https://www.analyticsvidhya.com/blog/2019/04/predicting-movie-genres-nlp-multi-label-classification/
2.Machine Learning - Text Classification with Python, nltk, Scikit & Pandas - https://www.youtube.com/watch?v=5xDE06RRMFk&t=1003s
