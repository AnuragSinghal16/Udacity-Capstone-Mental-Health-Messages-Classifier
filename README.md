# Udacity-Capstone-Mental-Health-Messages-Classifier

## Introduction
The main aim of this project was to utilise the power of machine learning and natural language processing (NLP) to develop a robust classifier capable of accurately identifying and categorizing mental health-related messages. By doing so, the project aims to provide a valuable tool for mental health professionals, support groups, and online platforms to better understand and address the specific needs of individuals reaching out for help.

## Methodology
1. Two classification models were used to categorise mental health messages into various categories for this project, Random Forest Classifier & Ada Boost Classifier.
2. Data was first pre-processed using "pandas" library. Pandas was also useful in performing initial data analysis on the data.
3. In a classification model, converting categorical data into numeric data is a very crucial step to make it more readable for the model. Pandas' ".get_dummies" function allowed to convert categorical variables into columns with a binary value of 0 and 1.
4. Text data usually can contain various noise or irrelevant characters which are of no use and keeping them in the data can reduce the quality of model performance significantly. A function "tokenize" will treat this issue and lower text data, tokenize it by words, and lemmatize text.
5. Finally, 2 pipelines will be used to train the models separately. The pipeline will transform text data using sklearn's "TfidfTransformer" package and vectorize data using 'CountVectorizer" which will use the "tokenize" function as input.

## Files
1. model.ipynb - the main code that builds the model
2. data.zip -  due to the size of the dataset, the file is converted to .zip and uploaded. Please decompress file to access .csv. This is the training and test dataset used to build the model
3. Here is the blog link - https://medium.com/@anuragsinghal1610/udacity-capstone-mental-health-messages-classificatioi-847d2293472a

## Performance & Evaluation
  ![image](https://github.com/user-attachments/assets/9e410c52-3dbc-4df8-9b13-134a494f9095)

The bar chart compares the performance of two classifiers: Random Forest and AdaBoost. The Random Forest classifier excels in Precision, significantly outperforming AdaBoost, indicating that when it predicts positive, it’s more likely correct. However, AdaBoost surpasses Random Forest in Recall and F1-score, suggesting it’s better at identifying all relevant positive instances and maintaining a balance between Precision and Recall. Both classifiers have relatively close Accuracy scores, but AdaBoost has a slight edge.

As seen in the results above, the random forest classifier is able to deliver high precision but lags in recall and f1 score. One obvious and potential improvement to the existing model is to improve its recall, this will allow more messages to be categorised and more people helped if this model is deployed to a live chatbot service.

![image](https://github.com/user-attachments/assets/40ea77ab-d9c5-4017-82df-da0af52967b4)

More importantly, categories such as “suicidal” should be treated with utmost sincerity and action to improve its precision and recall could be the most important next step.

## Acknowledgments
A very big thanks to Udacity for giving me the opportunity to build this project!

data - https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health
