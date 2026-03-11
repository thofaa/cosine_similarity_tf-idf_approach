# NLP Playground: Markov Chains and TF‑IDF + Cosine Similarity

This repository is a **mixed NLP playground** that currently contains:
1) **Markov Chain** based text generation (notebook)  
2) **TF‑IDF + Cosine Similarity** for document/text similarity (notebook)  

**FURTHER PROJECT:**
The longer-term goal is to *connect these ideas* and explore whether we can build a practical pipeline that combines:
- **sequence modeling** ideas from (Hidden) Markov Models, and
- **retrieval / similarity** signals from **TF‑IDF + cosine similarity**,  
to create something like a **hybrid-HMM** -> *HMM + TF-IDF + Cosine similarity**.

---

## Repository contents

- `textgeneration_markovchain.ipynb`  
  Markov Chain text generation experiments.

- `cosine_tf_idf.ipynb`  
  TF‑IDF vectorization + cosine similarity experiments, including comparisons with/without TF‑IDF.

- `HMMtext_for_training.txt`  
  Text data currently stored in the repo (can be used for tokenization/training experiments, especially for markov chain model).

- `README.md`  
  Project overview (this file).

---

## Project 1 — Markov Chain Text Generation

**What it is:**  
A classic probabilistic approach to generate text by learning token transition probabilities.

**Typical flow:**
- preprocess text → tokenize
- build n-gram transitions (order-1, order-2, etc.)
- generate text by sampling next tokens from transition distribution
  
Markov Chains are the stepping stone to **Hidden Markov Models (HMMs)**. HMMs add *hidden states* and an *emission model*, which can help represent “topics/styles/states” underlying observed tokens.

---

## Project 2 — Cosine Similarity with TF‑IDF

**What it is:**  
A bag-of-words baseline to compare texts using TF‑IDF vectors and cosine similarity.

**Typical flow:**
- clean text → tokenize
- build TF, IDF, and TF-IDF matrix
- calculating weight cosine similarity
- rank nearest neighbors / similar sentences
- compare it with no weighted cosine similarity (without TF-IDF approach)
 
**TF‑IDF/cosine can be used as:**
- a **retrieval step** (find candidate similar sentences/segments),
- a **scoring feature** to choose among candidate generations,
- a **weak signal** for clustering/initial state assignment for HMM-style modeling.

---

## Notes on “HMM + cosine similarity + TF‑IDF” feasibility

TF‑IDF + cosine similarity isn’t a standard “emission probability” for an HMM (HMMs usually assume emissions are generated from a probability distribution). But it *can still be useful* in a hybrid system as:
- a retrieval step to choose candidate states/segments,
- a scoring feature for reranking,
- or as an additional signal combined with probabilistic components.
