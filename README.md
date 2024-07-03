# Fake News Classifier

## Academic Context

This project was developed as part of the coursework for "Computational Intelligence Fundamentals" a subject at the Faculty of Technical Sciences. 
All models were trained on Google Colab, and the notebooks have been copied from there.

## Project Overview

This project aims to classify news articles as either "fake" or "unreliable" using machine learning models. The dataset is sourced from Kaggle's Fake News dataset. Various models, including Naive Bayes and transformers (TinyBERT, DistilBERT), are compared. All models were trained on Google Colab, and the notebooks have been copied from there.

## Problem Description

The challenge is to accurately identify fake news articles, which can often be based on partially true information that is distorted or presented out of context. This requires models that can evaluate the credibility of sources, the balance of tone, and the accuracy of information.

## Data Overview

### Primary Dataset

The primary dataset includes approximately 20,000 rows and multiple columns, focusing on topics such as world news and politics:

- **id** - unique identifier for each article
- **title** - the article's headline
- **text** - article's body used for training the models
- **author** - the author of the article
- **label** - the target variable categorizing articles as "fake" (1) or "not fake" (0)

### Evaluation Dataset

An additional dataset is used exclusively for evaluation purposes. This dataset contains text and label columns and covers a relatively similar range of topics, ensuring a meaningful comparison during the evaluation phase:

- **text** - article's body used for evaluating the models
- **label** - the target variable categorizing articles as "fake" (1) or "not fake" (0)

## Models

### Naive Bayes

- Trained with and without preprocessing.

### Transformers

- **TinyBERT, DistilBERT**

### Evaluation

Both Naive Bayes and transformer models were:

- Tested on both the original test set and a different dataset to evaluate generalization.
- Evaluated based on accuracy, precision, recall, and F1-score.


## Results

- Naive Bayes showed consistent performance across different datasets, indicating relatively good generalization.
- Transformers achieved high accuracy on the test set of training dataset but showed poor generalization on second dataset, indicating sensitivity to specific training data characteristics.

![Results](https://github.com/matejaaj/Fake-News-Classifier/blob/main/results.png)

## Conclusion

The performance analysis of transformers indicates that these models are sensitive to the specific characteristics of the training set. When trained on a different dataset and tested on the original one, the results improved, suggesting the need for more diverse training data.
- **False Negatives:** Transformers misclassified true news as fake due to structured narratives and balanced tone.
- **False Positives:** Fake news was incorrectly classified as true due to emotional tone, political bias, and sensationalist language.

## Future Work

- **More Diverse Datasets:** Collecting and using a larger number of diverse datasets to improve the generalization capabilities of the models. Diverse data will enable the models to better recognize different writing styles and contextual differences between reliable and unreliable news.

- **Shift Focus from "Fake" to "Unreliable" News:** Categorizing news as reliable and unreliable allows for a broader range of assessment. A news article can be unreliable for several reasons, such as unverified information, poor sources, sensationalist tone, or biased presentation. This allows for finer granularity in classification and helps users better understand the reliability level of the news.

