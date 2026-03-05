# Conversational PDF Question Answering using RAG

## Project Overview
This project implements a Conversational Retrieval-Augmented Generation (RAG) system that allows users to ask questions about a PDF document. Unlike traditional PDF question answering, the system maintains conversation history and supports multi-turn dialogue.

The application retrieves relevant document sections using vector search and generates responses using a locally hosted language model through Ollama.

---

## Features
- PDF document ingestion and preprocessing
- Semantic search using FAISS vector database
- Local embedding model
- Conversational memory support
- Multi-turn question answering
- Command-line chatbot interface

---

## Technologies Used
- Python 3.11
- LangChain
- FAISS
- Ollama (Local LLM)
- Sentence Embeddings
- Jupyter Notebook

---

## How to Run

1. Create virtual environment

python -m venv venv311
venv311\Scripts\activate


2. Install dependencies

pip install -r requirements.txt


Run the notebook and execute all cells.

---

## Dataset
GPT-4 Technical Report PDF used for conversational testing.(saved as rag_paper.pdf)

---

## Challenges Faced
- Initially, incorrect document sections were retrieved due to semantic similarity with evaluation content.
- Smaller language models produced hallucinated responses, requiring prompt refinement.
- Managing chat history required trimming to prevent performance slowdown.
- Ensuring responses remained grounded in document context required careful prompt engineering.

---

## Observations
The conversational RAG approach significantly improved interaction quality compared to single-turn PDF QA systems. Maintaining message history enabled natural follow-up questions and improved contextual understanding.

---

## Conclusion
This project demonstrates how conversational memory combined with retrieval mechanisms can create an effective document assistant capable of grounded and context-aware dialogue.