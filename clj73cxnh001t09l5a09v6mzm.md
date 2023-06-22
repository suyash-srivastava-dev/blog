---
title: "What is NLP?( Natural Language Processing)"
seoTitle: "What is NLP ?"
seoDescription: "Natural language processing (NLP) is the ability of a computer program to understand human language as it is spoken and written -- referred to as natural la"
datePublished: Thu Jun 22 2023 12:00:15 GMT+0000 (Coordinated Universal Time)
cuid: clj73cxnh001t09l5a09v6mzm
slug: what-is-nlp
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1687435382546/9687e093-8df7-4fc4-8dba-c5dea20c73e5.png
tags: ai, nlp, transformers, aidemos, nlp-transformers

---

NLP is a field of linguistics and machine learning for human language. Its motive is to understand the words and the context of words.

### Key NLP tasks

* **Classification of sentences:** categorizing the sentence into fixed classes. ex: email classification into spam or ham, sentiment analysis of the reviews
    
* **Classifying words in sentences**:
    
    * **POS (Part of Speech) tagging**: Grammatical components of a sentence, identifying words as nouns, verbs, adjectives, etc
        
    * **NER (named entities recognition) tagging:** identifying named entities from a person, location, or organization.
        
* **Text Generation**: Fill in the blanks in a text with masked words as per the sequence context or probability of the next word.
    
* **Question Answering**: Given a question and a context, extract the answer for the question based on the information provided in the context.
    
* **Text Summarization**: Summarizing a text passage with the given context.
    
* **Machine Translation:** From source language to a target language conversion.
    

### Transformer

Transformers are a type of neural network architecture that are used in natural language processing (NLP) tasks, as mentioned above. Transformers work by using a technique called self-attention, which allows them to learn relationships between different parts of a sequence. This is in contrast to recurrent neural networks (RNNs), which can only learn relationships between adjacent elements in a sequence.

Transformers were first introduced in the paper "**Attention Is All You Need**" by Vaswani et al. (2017)(*will cover it later 😊*). Since then, they have been shown to achieve state-of-the-art results on a variety of NLP tasks.

Here are some of the advantages of using transformers in NLP:

* They are able to learn long-range dependencies in text.
    
* They are parallelizable, which makes them faster to train.
    
* They have been shown to achieve state-of-the-art results on a variety of NLP tasks.
    

Here are some of the disadvantages of using transformers in NLP:

* They require a large amount of data to train.
    
* They can be computationally expensive to train.
    
* They are not as well-suited for tasks that require sequential reasoning.
    

### Example transformer for sentiment analysis

Will be using transformer from [Huggingface](https://huggingface.co/docs/transformers/index)

1. Install the transformer library
    
    ```python
    !pip install transformers
    ```
    
2. Use the model for classification
    
    ```python
    from transformers import pipeline
    
    classifier = pipeline("sentiment-analysis")
    classifier("This is the worst possible product. Nothing works in this.")
    ```
    
    *Output*
    
    ```bash
    [{'label': 'NEGATIVE', 'score': 0.9998025298118591}]
    ```
    

[Collab notebook](https://github.com/suyash-srivastava-dev/A4I/blob/c4cc43b5f0988c7ed722323a54585e9b7bd9c6b8/Colab/NLP_01.ipynb)