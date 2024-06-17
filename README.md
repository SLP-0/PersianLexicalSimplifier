# Text Lexical Simplification in Persian

Welcome to the repository for my master's thesis on "Text Lexical Simplification in Persian." This project explores various machine learning and natural language processing (NLP) techniques to simplify complex Persian text, making it more accessible and understandable.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Thesis Abstract](#thesis-abstract)
- [Usage](#usage)
- [Notebook Details](#notebook-details)
- [License](#license)

## Overview

This project aims to leverage machine learning methods and transformer-based models to simplify Persian texts lexically. The notebook includes various methodologies and experiments conducted using models such as SVM, MLP, BiLSTM, and BERT.

## Features

- **Machine Learning Models**: Implementation of Support Vector Machines (SVM), Multi-Layer Perceptron (MLP), and Bidirectional Long Short-Term Memory (BiLSTM) networks.
- **Transformer Models**: Utilization of BERT for contextual text simplification.
- **Evaluation**: Comprehensive evaluation metrics and results to demonstrate the efficacy of each model.
- **Novelty**: First-of-its-kind approach to Persian text simplification using state-of-the-art techniques.

## Thesis Abstract

Understanding written texts is essential in everyday life. However, text comprehension can be a complex task for language users, especially for second language learners or people with reading disorders. Therefore, text simplification can help many in the manner of written text comprehension. In this thesis, we tried to solve the problem of text complexity for readers by automating the simplification process. As the first step we try to give a definition for the concept of lexical complexity and propose lexical complexity features in Persian language. For data preparation, we first merged two corpora, Miras and Farsi Wikipedia, and after preprocessing textual data, we selected five thousand random words from them and extracted predefined complexity features for each word. Also, for each word we extracted a phrase containing the target word. Then, we presented the words along with their corresponding phrases to five participants chosen from different language user groups for binary labeling of complexity or simplicity of each word based on the lexical complexity definition. In this way, a dataset was created to build a simplification algorithm with features such as word length, word frequency in two corpora and vowel-to-consonant ratio in the word. To create a complex word identification model, this data was given to 3 models. These models were based on MLP, Bi-LSTM and BRF. Also, we fine tuned ParsBert large language model to identify complex words in a given text. Bi-LSTM based model achieved the highest score in F1 with 0.56. In the substitution generation step, we first concatenated the initial sentence and the sentence with masked complex target word and fed it to Roberta masked language model to suggest substitute words for the target word. As for the last step, to select the most proper substitute, we considered four selection critiques: frequency, similarity, loss and mask model suggestion order. After ranking substitutes based on the criterions, the word with highest ranking was chosen as the final suggested word. Then we replaced it and presented the final simplified sentence as the output. We used the SARI metric to evaluate these models and the Bi-LSTM based model achieved the best score which is 26.10. Also, we compare each ranking criterions separately. Mask model suggestion order worked better as the only ranking criterion. It is noteworthy that this approach has been implemented in the Persian language for the first time.

Keywords: Natural Language Processing, Persian Text Simplification, Lexical Complexity Prediction, Masked Language Model

## Usage

0. Open in colab:
    
    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SLP-0/lexical-simplification-fa/blob/main/thesis_notebook.ipynb)

1. Open the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

2. Navigate to `thesis_notebook.ipynb` and open it.

3. Run the cells sequentially to reproduce the results and follow along with the experiments.

## Notebook Details

- **Data Preparation**: Steps to clean and preprocess the Persian text data.
- **Model Training**: Training procedures for SVM, MLP, BiLSTM, and BERT models.
- **Evaluation**: Performance metrics and evaluation methods used to assess the models.
- **Visualization**: Graphs and charts to visualize the results and comparisons between models.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

