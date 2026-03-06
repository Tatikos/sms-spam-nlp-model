# SMS Spam/Ham NLP Pre-processing Pipeline

## Overview
This project implements a configurable Natural Language Processing (NLP) pipeline to clean, process, and analyze a dataset of SMS messages classified as Spam or Ham. It demonstrates fundamental text pre-processing techniques and uses class-conditional statistics to identify domain-specific stopwords.

## Key Features
* **Custom Pre-processing Pipeline:** Implements modular functions for tokenization, lowercasing, punctuation and digit removal, NLTK stopword removal, lemmatization, and Porter stemming.
* **Domain-Specific Stopword Detection:** Calculates Relative Document Frequency (RDF) to find and filter out words that act as stopwords specifically within the SMS domain.
* **Vocabulary Analysis:** Tracks and visualizes the reduction in token and vocabulary sizes at each step of the cleaning process.
* **Frequency Distributions:** Isolates and identifies the most frequent tokens exclusive to Spam, exclusive to Ham, and shared across both classifications.

## Tech Stack
* **Language:** Python
* **Libraries:** NLTK, Matplotlib, Hugging Face `datasets`
* **Environment:** Jupyter Notebook

## Dataset
The project uses the `sms_spam` dataset loaded directly via the Hugging Face library. It contains 747 Spam messages and 4,827 Ham messages.

## Generated Outputs
Running the notebook generates several text-based reports:
* `domain_stopwords.txt`: The top domain-specific stopwords along with their SPAM and HAM RDF scores.
* `vocabulary_sizes.txt`: A step-by-step breakdown of vocabulary reduction.
* `only_spam.txt` & `only_ham.txt`: The top 10 frequent tokens unique to each category.
* `spam_ham.txt`: The top 10 frequent tokens shared between both categories.
