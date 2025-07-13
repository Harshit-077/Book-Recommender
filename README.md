# 📚 Book Recommender

A semantic-powered, emotion-filtered book recommendation app built with Python, LangChain, and Gradio.

## 🔍 Features

- **Semantic Search**: Understands natural-language queries (e.g., "A story about forgiveness") using Hugging Face embeddings.
- **Emotion-Aware Ranking**: Sort recommendations by tone — Happy, Surprising, Angry, Suspenseful, or Sad.
- **Category Filtering**: Filter results by genre/category with an "All" fallback.
- **Clean UI**: 8-column, 2-row image gallery powered by Gradio.
- **Compact Previews**: Book cover, title, author(s), and a short description snippet.

## 🧰 Tech Stack

- [LangChain](https://www.langchain.com/) for document embedding & semantic retrieval
- [Hugging Face](https://huggingface.co/) embeddings
- [ChromaDB](https://www.trychroma.com/) as a local vector store
- Pandas & NumPy for data processing
- Gradio for building an interactive web UI
- `python-dotenv` for environment config

## 🚀 Quick Start

```bash
git clone https://github.com/Harshit-077/Book-Recommender.git
cd Book-Recommender

# Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate   # macOS/Linux
# On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Make sure the following files are present in the data/ directory:
# - books_with_emotions.csv
# - tagged description.txt
# - cover-not-found.jpg

# Run the website
python gradio-dashboard.py

```

## ⚙️ Key Logic

##### retrieve_semantic_recommendations():<br>
Retrieves top matching descriptions using LangChain + Chroma<br>
Filters by category<br>
Sorts by emotional tone using scores<br>
##### recommend_books():<br>
Formats results into (image, caption) tuples for Gradio gallery<br>
##### Gradio UI:<br>
Accepts natural language input<br>
Dropdowns for category and emotional tone<br>
Displays recommendations in a grid layout<br>

## 💡 Future Ideas

Add download/export for recommendations<br>
Add loading animation during search<br>
Integrate external book metadata (e.g., Goodreads API)<br>
Host using Docker or Hugging Face Spaces<br>

## 👨‍💻 Author

Harshit Sharma<br>
GitHub: Harshit-077

