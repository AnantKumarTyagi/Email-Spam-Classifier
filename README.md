# Email-Spam-Classifier
An end-to-end Natural Language Processing (NLP) and Machine Learning project to classify emails and SMS messages as "Spam" or "Not Spam" (Ham).

This project covers the entire machine learning pipeline—from data cleaning and exploratory data analysis (EDA) to text preprocessing, model building, web application development, and cloud deployment.

# Table of Contents
[Demo](#demo)
[Features](#features)
[Tech Stack](#tech-stack)
[Dataset](#dataset)
[Project Workflow](#project-workflow)


## Demo
The end product of this project is a web application where users can input an email or SMS message and instantly check if it is flagged as Spam or Not Spam.

## Features
Real-time Classification: Instantly predicts whether a message is spam.
Interactive UI: Built with Streamlit for a clean and user-friendly experience.
Robust Text Preprocessing: Handles tokenization, lowercase conversion, and the removal of stop words, punctuation, and special characters.
High Precision Model: Utilizes a Multinomial Naive Bayes algorithm, heavily optimized for high precision to avoid false positives (flagging a genuine message as spam).

## Tech Stack
Programming Language: Python
Data Manipulation & Analysis: Pandas, NumPy
Data Visualization: Matplotlib, Seaborn, WordCloud
NLP & Text Processing: NLTK (Natural Language Toolkit)
Machine Learning: Scikit-Learn (TF-IDF Vectorizer, Multinomial Naive Bayes)
Web App Framework: Streamlit


## Dataset
This project uses the SMS Spam Collection Dataset provided by the UCI Machine Learning Repository. You can also use any standard Email Spam dataset, as the pipeline logic remains identical.

## Project Workflow
Data Cleaning: Dropped irrelevant columns, renamed generic columns for readability, handled missing values, encoded target variables, and removed duplicate entries.

Exploratory Data Analysis (EDA):
Analyzed the distribution of Spam vs. Ham (Imbalanced dataset).
Extracted new features like the number of characters, words, and sentences per message.
Visualized text frequencies using Histograms, Pairplots, Heatmaps, and WordClouds.


Text Preprocessing:

Converted all text to lowercase.
Tokenized sentences into individual words.
Removed non-alphanumeric characters, stop words, and punctuation.
Applied Stemming (using NLTK's PorterStemmer) to reduce words to their root form.
Model Building & Evaluation:
Converted text data into numerical vectors using TfidfVectorizer.
Trained multiple algorithms (GaussianNB, MultinomialNB, BernoulliNB, Random Forest, SVC, Extra Trees).
Selected Multinomial Naive Bayes as the final model because it achieved an excellent balance of accuracy (97%+) and perfect precision (100%), ensuring no normal messages are mistakenly classified as spam.

Web Application: Created a front-end interface using Streamlit (app.py), integrating the serialized TF-IDF vectorizer and the trained Naive Bayes model (.pkl files).
