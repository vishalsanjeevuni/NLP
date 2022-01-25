<!-- Add banner here -->

![shutterstock_1768400198](https://user-images.githubusercontent.com/26355917/151054537-b8da1c51-c8ce-4821-a28a-a8f8f552e4fe.jpg)
# Sentiment Analysis on Medium 2021 data science articles

# How to Analyze Natural Language?
<!-- Add a demo for your project -->

The goals of this project are to create a model, classify text to explore the sentiment present and compare the general sentiment of title between tags

![Random GIF](https://media.giphy.com/media/ZVik7pBtu9dNS/giphy.gif)

# Table of contents

- [Data Info](#project-title)
- [Analysis Plan](#demo-preview)
- [NLP model](#table-of-contents)
- [Text preprocessing](#installation)
- [Exploratory Data Analysis](#usage)
- [Sentiment Analysis](#development)


# Data Info
* Data Source https://www.kaggle.com/viniciuslambert/medium-2021-data-science-articles-dataset

`First five rows of data frame`

![Screen Shot 2022-01-25 at 4 00 16 PM](https://user-images.githubusercontent.com/26355917/151058927-9c707e9e-66e3-422c-908f-70eafbb550b0.png)


# Analysis Plan

Based on the data, I’m interested in performing sentiment analysis on the `title` variable, and statistical analysis on how sentiment varies between tags.
The goal is to create a model, classify text to explore the sentiment present and compare the general sentiment of title between tags

# NLP model

I plan to perform following NLP tasks:
* Text preprocessing using regex and NLTK.
* Exploratory data analysis with pandas and seaborn.
* Sentiment analysis using bag-of-words and a Naive Bayes classifier.

# Text preprocessing

To remove unnecessary characters and words and standardize the casing, following text preprocessing tasks were helpful:

### Noise Removal
* Punctuation
* Stopwords
* URLs
* HTML Tags

### Text Normalization

* Lower Casing

### Preprocessed title variable

![1_jyDkyYa8LcS3L4YyM7oYcg](https://user-images.githubusercontent.com/26355917/151060506-38b344eb-63ce-440a-933c-21a04d5536ab.png)


# Exploratory Data Analysis
### `title count by tag`
![1_3uMLp2DD-I_J9LpDHAZfOQ](https://user-images.githubusercontent.com/26355917/151060663-cf9a3e64-8f7b-4fb5-96e6-8c07bdb0f0f1.png)

### `number of titles per tag`
![1_g7DrMwqlULCNpbuGObpQ9A](https://user-images.githubusercontent.com/26355917/151060927-81edc9bd-a354-460b-8a73-c4731e7abf99.png)

# Sentiment Analysis
Categorized `title` variable into one of two categories:
* Positive
* Negative

Employed Naive Bayes classification to determine the sentiment of the titles in the `title` variable
Created a classifier using Twitter data with known sentiments, then created a feature extractor that identifies when a feature is present in a title.
Created training and testing sets using the `random` library, to randomly select the tweets for each token
Performance of my model on my training set using the `classify()` function

`The 20 most informative features for prediction`

![1_Y0psg7aF__4U2sZbPgUlsQ](https://user-images.githubusercontent.com/26355917/151061303-6483dcf1-cbc1-4baa-a931-3cc26f0e4f25.png)

Evaluation of all the title’s in the medium data Corpus

`Viewing the proportion of the corpus in each class`

![1_JQEcdo7F7mRjx9lpwJJ4zg](https://user-images.githubusercontent.com/26355917/151061695-d9231191-5140-4ae7-a737-5ed18838c1bb.png)

`View the distribution in a countplot`

![1_0A26Iurbg9XqM5XJpICeHA](https://user-images.githubusercontent.com/26355917/151061770-9790c55e-7b3e-4b2d-bb8d-60a72519b9b1.png)

### My model predicts that around 60.2% of the title’s in the corpus are Positive

### Comparison of sentiment by tag

`DataFrame by Sentiment_score`

![1_FyG0_KSw3l1lIho5g4eiXA](https://user-images.githubusercontent.com/26355917/151062015-5692e96d-1961-4525-80d4-ab357b96b0a3.png)

The bar below chart indicates the sentiment by category represents which categories are the most Positive/Negative.

`sentiment by category`

![1_aqbr17TU1hXCyqAIh2v98g](https://user-images.githubusercontent.com/26355917/151062060-408b2c5a-1bae-474b-9c5c-64d55b68d76f.png)

