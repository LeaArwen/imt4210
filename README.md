# IMT4210 - Comparing Text Representation Methods for Phishing Email Detection

This repository contains the Python implementation and experimental analysis for a computational forensics course (IMT4210) project at NTNU.

The project investigates how different text representation methods affect machine-learning-based email classification, with particular attention to classification performance and false positives and false negatives.

Research Questions:
- How does the choice of text representation method affect the performance of machine-learning-based phishing email classification?
- What types of classification errors occur with the different text representation methods?

Dataset:

The project uses the publicly available Phishing Email Dataset on Kaggle (https://www.kaggle.com/datasets/naserabdullahalam/phishing-email-dataset), which combines email records from several sources, including Enron, Ling, CEAS, Nazario, Nigerian Fraud, and SpamAssassin.

The dataset contains two relevant columns:

- text_combined: Email text used for classification.
- label: Binary class label (0 = legitimate, 1 = spam/phishing).

The final experiments used 82,078 records after cleaning. The dataset was divided into 80% training data (65,662 emails) and 20% test data (16,416 emails).

Note: The dataset includes spam as well as phishing-related emails. Consequently, the results should not be interpreted as phishing-only detection performance.
