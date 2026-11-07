# IMT4210 – Comparing Text Representation Methods for Phishing Email Detection

This repository contains the Python notebook and experimental analysis for my IMT4210 Computational Forensics project at NTNU.

The project compares three text representation methods for email classification using Logistic Regression:

- Bag of Words (BoW)
- TF-IDF with unigrams
- TF-IDF with unigrams and bigrams

The aim is to examine how the choice of text representation affects classification performance and the types of errors made. The results are also discussed in relation to the potential use of automated email classification in digital forensic investigations.

## Research Questions

1. How does the choice of text representation affect the classification performance of Logistic Regression?
2. How do classification errors differ between the text representation methods?

## Dataset

The project uses the publicly available [Phishing Email Dataset on Kaggle](https://www.kaggle.com/datasets/naserabdullahalam/phishing-email-dataset), which combines emails from several sources, including Enron, Ling, CEAS, Nazario, Nigerian Fraud, and SpamAssassin.

The following columns are used:

- `text_combined`: Email text used for classification.
- `label`: Binary class label (0 = legitimate, 1 = spam/phishing).

After removing exact duplicate emails, the dataset contains 82,078 records. The data is divided into 80% training data (65,662 emails) and 20% test data (16,416 emails), using a stratified split.

**Note:** The positive class includes both spam and phishing-related emails. The results therefore reflect classification of this combined category, rather than phishing detection alone.

## Running the Notebook

The experiments were conducted in Google Colab using Python and scikit-learn.

To reproduce the experiments:

1. Download `projectIMT4210.ipynb` from this repository.
2. Download `phishing_email.csv` from the Kaggle dataset linked above.
3. Open the notebook in Google Colab.
4. Upload the CSV file to Colab or make it accessible through Google Drive.
5. Check that the dataset path in the notebook points to the correct file.
6. Run all cells in order.

The notebook includes dataset inspection, cleaning, model training, evaluation, confusion matrices, and analysis of classification errors.

### Python Libraries

The main libraries used are:

- pandas
- NumPy
- scikit-learn
- Matplotlib

The experiments were conducted using Python 3.13.18 and scikit-learn 1.6.1.

## Results

Bag of Words achieved the highest overall classification performance, with an accuracy of 98.76% and an F1-score of 0.9882. The error analysis also showed that some emails were misclassified by all three models and that error rates varied according to message length and class.

The complete results and discussion are provided in the submitted project report.
