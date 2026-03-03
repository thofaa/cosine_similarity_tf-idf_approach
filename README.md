# Cosine Similarity Using TF‑IDF Approach

This repository demonstrates how to compute **document similarity** using **TF‑IDF vectorization** and **cosine similarity** in a practical, notebook-based workflow.

## Repository contents

- `cosine_tf_idf.ipynb` — main Jupyter Notebook containing the implementation and examples.
- `README.md` — project overview (this file).

## What this project does

In the notebook, you’ll typically:
1. Prepare or load a set of text documents.
2. Convert text into numerical vectors using **TF‑IDF**.
3. Compute pairwise similarity scores using **cosine similarity**.
4. Inspect results to find the most similar documents / texts.
5. Compare the result between cosine similarity value with **TF-IDF** approach and without **TF-IDF** approach.

## How to run

### Option A: Run locally (recommended)
1. Clone the repo:
   ```bash
   git clone https://github.com/thofaa/cosine_similarity_using_tf-idf_approach.git
   cd cosine_similarity_using_tf-idf_approach
   ```
   
2. Start Jupyter:
   ```bash
   jupyter notebook
   ```

3. Open and run:
   - `cosine_tf_idf.ipynb`

### Option B: Run in Google Colab
- Upload `cosine_tf_idf.ipynb` to Colab (or open it from GitHub) and run all cells.

## Notes

- TF‑IDF and cosine similarity are widely used for:
  - near-duplicate detection
  - document clustering exploration
  - simple semantic matching / search baselines
