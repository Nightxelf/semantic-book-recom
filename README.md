# Semantic Book Recommender

A semantic search-based book recommendation system that retrieves books based on meaning rather than keyword matching. It uses text embeddings and a vector database to match user queries with conceptually similar book descriptions.

---

## Overview

This project improves book recommendations by focusing on semantic similarity. Instead of relying on exact keyword overlap or popularity-based ranking, it interprets the intent behind a query and retrieves books with similar meaning in embedding space.

Example queries supported:

* dark fantasy with moral conflict
* psychological thriller with unreliable narrator
* light romantic story set in Europe
* science fiction involving artificial intelligence

---

## Core Approach

1. Book descriptions are converted into vector embeddings using a text embedding model.
2. These embeddings are stored in a vector database (ChromaDB).
3. User queries are converted into the same embedding space.
4. A similarity search retrieves the closest matches.
5. Optional filters (genre, emotion/tone) refine results.

---

## Features

* Semantic search over book descriptions
* Vector-based retrieval using ChromaDB
* Emotion or tone-based filtering
* Genre/category filtering
* Notebook-based experimentation and evaluation
* Simple query interface for retrieving recommendations

---

## Project Structure

* Data preprocessing: cleaning and standardizing book metadata
* Embedding generation: converting text into vector representations
* Vector storage: storing embeddings in ChromaDB
* Retrieval logic: similarity search and ranking
* Analysis notebooks: exploration, classification, and sentiment analysis
* Application layer: query handling and result presentation

---

## Notebooks / Components

Typical workflow includes:

* data exploration and preprocessing
* embedding generation and similarity search setup
* text classification for genre labeling
* sentiment or emotion analysis of descriptions
* application notebook for querying recommendations

---

## Tech Stack

* Python
* Sentence Transformers (or similar embedding models)
* ChromaDB for vector storage and retrieval
* Pandas and NumPy for data processing
* Scikit-learn / Transformers for NLP tasks
* Jupyter Notebook

---

## Installation

```bash
git clone https://github.com/Nightxelf/semantic-book-recom.git
cd BookRecom

pip install -r requirements.txt
```

---

## Running the Project

If script-based:

```bash
python app.py
```

If notebook-based:

```bash
jupyter notebook
```

Open the relevant notebook and run the cells sequentially.

---

## Example Queries

* Books similar to *1984* but with a more optimistic tone
* Fantasy novels with strong emotional depth
* Psychological thrillers with unreliable narration
* Science fiction focused on artificial intelligence and consciousness

---

## Dataset Requirements

The system expects a dataset containing:

* Book title
* Description or summary
* Genre or category
* Optional emotion/tone labels
* Optional metadata (author, cover image links, etc.)

---

## Future Improvements

* Hybrid search combining semantic + keyword retrieval
* Fine-tuning embeddings on literature-specific datasets
* Recommendation explanation layer (“why this book was suggested”)
* Personalized user profiles
* API deployment using FastAPI with scalable vector storage
