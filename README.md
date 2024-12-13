# Ranked Retrieval Model Comparison

This repository contains the implementation and evaluation of three ranked retrieval models: **TF**, **TF-IDF**, and **Word2Vec**. The purpose of this project is to compare the models in terms of computation time, relevance to queries, and the ranking consistency of retrieved documents.

## **Overview**

Information retrieval involves ranking documents based on their relevance to user queries. This project evaluates the performance of three models:

- **TF**: Term Frequency representation.
- **TF-IDF**: Term Frequency-Inverse Document Frequency representation.
- **Word2Vec**: Pretrained word embedding model.

The models are tested on a dataset of news articles, using the `content` column for text processing.

## **Features**

- Tokenization of documents.
- Ranked retrieval using three different models.
- Evaluation based on:
  1. **Computation Time**
  2. **Relevance to Queries**
  3. **Comparison of Top 10 Retrieved Documents**
- Visualizations of similarity scores and computation time.

## **Dataset**

The dataset contains news articles written by various authors. The main column used for evaluation is:

- **Content**: The body of the news article.

## **Results**

1. **Computation Time**:

   - **TF** is the fastest model (~6.50 seconds).
   - **TF-IDF** is moderately fast (~7.45 seconds).
   - **Word2Vec** is the slowest (~16.17 seconds).

2. **Relevance to Queries**:

   - **TF-IDF** performs the best in terms of relevance.
   - **Word2Vec** captures semantic relationships but may return broader contexts.
   - **TF** has lower relevance due to noise from common terms.

3. **Top 10 Documents Comparison**:
   - **TF-IDF** is consistent in retrieving relevant documents.
   - **Word2Vec** excels in semantic relationships but lacks specificity.
   - **TF** often retrieves less relevant documents.

## **Installation**

1. Clone the repository:

   ```bash
   git clone https://github.com/muhakbarhamid21/ranked-retrieval-model-comparison.git
   ```

2. Navigate to the directory:

   ```bash
   cd ranked-retrieval-model-comparison
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## **Usage**

Run the notebook `TF_TFIDF_Word2Vec_Comparison.ipynb` to execute the following steps:

1. Data preprocessing (tokenization).
2. Implementation of TF, TF-IDF, and Word2Vec models.
3. Evaluation and visualization of results.

## **Dependencies**

- Python 3.8+
- Gensim
- NLTK
- Scikit-learn
- Matplotlib
- Pandas
- NumPy

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.

## **Acknowledgments**

- Dataset Source: [Link to Dataset](https://drive.google.com/file/d/13UUj240WKjosQnLfnveMcOutd0OYxBDF/view?usp=sharing)
- Pretrained Word2Vec Model: [GoogleNews-vectors-negative300]
