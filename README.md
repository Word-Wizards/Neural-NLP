# Assignment 1: Train Word2Vec on peS2o Dataset (AllenNLP)
- This project demonstrates the entire process, from preprocessing the dataset, initializing the Word2Vec model with TF-IDF-based vectors, to calculating document similarities using cosine similarity.

## Team: Word Wizard
- Dhruvi Shah(202211032)
- Dipen Padhiyar(202211058)
- Vipasha Vaghela(202211002)
- Vivek Soni(202211069)

## Assignment Overview:
- We have generated sentence embeddings) on peS2o dataset (or arxiv dataset) by training data of 3000 documents are used, while a test dataset of 1000 documents is used.
- We have preprocess the document data to remove stopwords, urls, bullets, apostrophe, hyphens, enumerations 
- We have generated input context matrix with sentences as lingustic unit from TFIDF, and generate Embedding via scratch word2Vec model.
- We have initialize the Word2Vec model using the TF-IDF vectors as the context matrix. Here TF-IDF vectors assigned to each sentence in  training dataset and We used these vectors as the initial embeddings for Word2Vec. It sets the initial vectors for each word in the Word2Vec vocabulary based on their TF-IDF weights. For each test document, we have calculated the average Word2Vec vector by taking the mean of the Word2Vec vectors of all the tokens in the document. Tokens that are not in the Word2Vec vocabulary are ignored. If a word exists in both the Word2Vec model vocabulary and the TF-IDF weight dictionary, its Word2Vec vector is updated by multiplying it with the TF-IDF weight. This step customizes the initial vectors based on TF-IDF information.
- It combines Word2Vec's context-based word embeddings with the information about word importance provided by TF-IDF.
- We have evaluated our word2vec model by getting cosine similarity scores on pair of sentences, to get idea about similarity.


