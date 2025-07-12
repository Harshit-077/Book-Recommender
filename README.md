# 📚 Book Recommender System

Welcome to the **Book Recommender System** — a semantic search engine for books that helps users discover titles based on the meaning of their queries rather than exact keyword matches. This project leverages **LangChain**, **FAISS**, and **Hugging Face Transformers** to provide intelligent recommendations and content classification.

---

## 🚀 Features

- 🔎 Content-Based Recommendation  
  Recommends books using semantic similarity between the user's query and book descriptions.

- ⚡ Efficient Vector Search with FAISS  
  Fast nearest-neighbor search over dense embeddings for real-time responses.

- 🧠 Language Model-Powered Embeddings  
  Uses modern language models to capture the *meaning* behind text.

- 🧾 LinkedIn Highlight Classifier (Bonus Feature)  
  Classifies user text (e.g., achievements, experiences) into suitable LinkedIn categories using **zero-shot classification** with Hugging Face’s `facebook/bart-large-mnli`.

---

## 🛠️ Tech Stack

| Component        | Tech Used                             |
|------------------|----------------------------------------|
| Programming Lang | Python                                 |
| Vector Store     | FAISS (Facebook AI Similarity Search)  |
| NLP              | LangChain, Hugging Face Transformers   |
| Dataset Handling | pandas                                 |

---

## 📂 Dataset

This project uses the **7K Books Dataset** from Kaggle:

- 📦 Source: [Kaggle Notebook by @aiswaryarana](https://www.kaggle.com/code/aiswaryarana/7k-books)
- ✅ Features: `isbn13`, `title`, `authors`, `description`, `categories`, `average_rating`, etc.
- 🧠 Used for: Creating semantic embeddings from book descriptions and metadata to drive recommendations.

You can download and explore the dataset [here](https://www.kaggle.com/code/aiswaryarana/7k-books).

The `books.csv` file in this repository is derived from this dataset. The `description` column is especially important, as it is used to generate text embeddings that power the recommendation engine via FAISS.

---

## 🧠 How It Works

1. **Book embeddings** are created from book descriptions using a language model (via LangChain).
2. **FAISS** indexes these embeddings for fast retrieval.
3. When a user inputs a query (e.g., "books about AI ethics"), the system:
   - Embeds the query
   - Searches for the top `k` most similar book embeddings
   - Returns the matching book entries

---

## 📌 Future Work

 1. Add collaborative filtering for user-based recommendations
 2. Build a web interface using Streamlit
 3. Enable hybrid search (metadata + semantic)
 4. Deploy as an API
