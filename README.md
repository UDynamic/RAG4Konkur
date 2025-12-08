# KonkurRAG  
AI-Powered PhD Exam Preparation Using Retrieval-Augmented Generation

KonkurRAG is an intelligent study assistant designed to help candidates prepare for the Iranian PhD entrance exam in Computer Science (AI). It leverages a RAG pipeline built on 10+ years of historical exam questions to provide precise, exam-aligned learning.

---

## 🚀 Features

### RAG-Based Retrieval
- Retrieves similar past exam questions
- Searches by topic, difficulty, or pattern
- Uses embeddings + reranking for high accuracy

### Smart Explanations
- Generates clear walkthroughs for AI, ML, DSA, math, and reasoning questions
- Provides step-by-step logic aligned with exam style

### Personalized Study Guidance
- Detects weak topics automatically
- Recommends what to study next
- Builds targeted quizzes from real exam data

### Pattern Mining
- Identifies repeated question types
- Highlights high-yield topics
- Tracks your progress over time

---

## 🛠️ Architecture

RAG Pipeline:
PDF Exams → Text Chunking → Metadata Tagging → Embedding Model (E5/BGE) → Vector Store (Chroma/Weaviate/Qdrant) → Reranker → LLM (GPT / LLaMA) → Query Response Engine

---

## 📁 Project Structure

konkurrag/
  data/
    pdfs/               (Raw exam PDFs)
    processed/          (Extracted & cleaned text)
    metadata.json       (Tags: year, topic, difficulty)

  src/
    ingestion/          (PDF parsers, chunkers)
    embeddings/         (Embedding models & vector store)
    retriever/          (Similarity search + reranking)
    generator/          (LLM answer generator)
    pipeline.py         (Full RAG pipeline)
    api/                (Optional REST API)

  notebooks/
    exploration.ipynb
    analysis.ipynb      (Pattern mining & topic mapping)

  README.md

---

## 📦 Installation

Run the following:

git clone https://github.com/yourusername/konkurrag
cd konkurrag
pip install -r requirements.txt

---

## ▶️ Usage

Example: Run a query

from konkurrag.pipeline import ask
answer = ask("Teach me AVL tree rotations with examples")
print(answer)

Example: Retrieve similar past questions

ask("Show me past exam questions about Lagrange multipliers")

---

## 🧩 To-Do (Roadmap)

- Add exam difficulty prediction
- Add spaced-repetition flashcards
- Add UI dashboard (Streamlit)
- Add question auto-classifier
- Add progress analytics

---

## 🏆 Why KonkurRAG?

Because the best teacher is 10 years of real exam data combined with LLM intelligence.  
No randomness. No clutter. Pure exam-focused learning.

---

## 📜 License
MIT License.
