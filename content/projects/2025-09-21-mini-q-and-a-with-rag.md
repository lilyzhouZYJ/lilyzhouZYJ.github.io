---
title: "Mini Q&A with RAG"
summary: "a command-line Q&A application that uses RAG to answer questions about texts and webpages; includes 2 implementations of RAG"
tags: ["ML/AI"]
showTags: true
date: 2026-01-07
---

This project includes two implementations of a tiny Q&A application using RAG.

1. **Raw RAG implementation** - a lightweight implementation built from scratch
2. **RAG using LangChain** - a more production-ready approach using LangChain

Both implementations include:

- loading and chunking text content
- creating vector embeddings and storing them in vector store
- querying the content using natural language questions
- producing AI-generated answers based on the retrieved context

Currently, the raw RAG implementation supports retrieving text files, while the LangChain implementation supports retrieving webpages.

### GitHub repo

[lilyzhouZYJ/mini-q-and-a-with-rag](https://github.com/lilyzhouZYJ/mini-q-and-a-with-rag)

### Example usage

Run the app (raw-implementation) using:

```
python3 rag/q_and_a_app.py --path rag/test.txt
```

`test.txt` contains the first 10 chapters of Jane Austen's Pride and Prejudice.

The output, including 2 sample questions, is below. The app was able to answer questions about the text in its own words!

```
(1) Loading content...
 - loaded 25 chunks total
(2) Building vector store...
 - vector store loaded from storage
(3) Initializing LLM...
Question: what does Mrs. Bennett want Mr. Bennett to do?
Answer: Mrs. Bennet wants Mr. Bennet to visit Mr. Bingley as soon as he comes into the neighborhood, as she is eager for him to meet one of their daughters and hopes that he may fall in love with one of them. She believes that Mr. Bingley, being a single man of large fortune, would be a fine match for one of her daughters.

Question: How did Mr. Bennett respond to Mrs. Bennett's request?
Answer: Mr. Bennet responded to Mrs. Bennet's request to visit Mr. Bingley by initially expressing indifference and saying he saw no occasion to visit. He suggested that Mrs. Bennet and the girls could go or even send them by themselves, indicating that he was not particularly eager to make the visit himself. Ultimately, despite his reluctance, he did visit Mr. Bingley, but only after assuring his wife that he would not go, which he later revealed to the family as a surprise.
```