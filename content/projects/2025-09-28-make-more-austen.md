---
title: "MakeMoreAusten (WIP)"
summary: "a multi-model text generation app that writes in the voice of Jane Austen"
tags: ["ML/AI"]
showTags: true
date: 2025-09-28
---

This project implements a multi-model text generation system trained on Jane Austen's works. It is inspired by Andrej Karpathy's makemore library, but while makemore is a character-level framework, this project extends it to the word-level.

### GitHub repo

[lilyzhouZYJ/make_more_austen](https://github.com/lilyzhouZYJ/make_more_austen)

### Currently supported models

**Probabilistic bigram model:**
- bigram model that uses count-based probabilities to generate predictions

Example output:

```
Generated text: "she must be sure you mean to think to which"

Word predictions for 'catherine':
Top 5 words after 'catherine': s (0.140), was (0.080), and (0.058), <END> (0.046), had (0.042)
```

**Neural-network bigram model:**
- uses word embeddings and neural network, more expressive than count-based bigram model
- configurable architecture (embedding dimension, learning rate, epochs)

Example output:

```
Generated text: "she had been very much pleased with her own"

Word predictions for 'elizabeth':
Top 5 words after 'elizabeth': was (0.082), <END> (0.064), and (0.061), s (0.060), had (0.060)
```

**MLP (Multi-Layer Perceptron) model:**
- uses multiple words as context
- more sophisticated than bigram models by considering longer sequences
- supports mini-batch training for better efficiency
- configurable context length (block size), hidden dimensions, and training parameters

Example output:

```
Generated text: "he had a considerable independence besides two good livings"

Context predictions for 'and the book':
Top 5 words after 'and the book': her (0.968), ladies (0.024), many (0.006), about (0.001), room (0.000)
```