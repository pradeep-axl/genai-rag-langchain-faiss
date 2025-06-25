# 🤖 Retrieval-Augmented Generation (RAG) Pipeline with LangChain, FAISS & Streamlit

This project showcases a lightweight **RAG pipeline** that allows you to chat with your documents using **LangChain**, **FAISS**, and **Streamlit**. It demonstrates how to embed documents, store them as vectors, and retrieve relevant chunks for contextual LLM answers.

## 🎯 Problem

Large Language Models (LLMs) like GPT-4 are powerful but lack knowledge of your internal documents. How can you enable **custom Q&A** on private files like PDFs, text, or CSVs?

## ✅ Solution

A **RAG architecture** where:
- Docs are parsed and chunked
- Vectors are generated via embeddings
- Stored in a FAISS vector store
- Queried context is passed to an LLM for accurate answers

## 🧠 Architecture
User ↔ Streamlit UI ↔ LangChain → FAISS (search) → LLM (OpenAI/HF)
↘ Embedded Document Vector Store

## 🔧 Stack

| Component | Tool                            |
|-----------|---------------------------------|
| Ingestion | LangChain Document Loaders      |
| Embedding | OpenAI / HuggingFace Embeddings |
| Storage   | FAISS                           |
| Retrieval | LangChain                       |
| Interface | Streamlit                       |
| Optional  | Pinecone, LangGraph, FastAPI    |

## 📁 Repo Structure
```
genai-rag-pipeline/
├── app/
│   └── streamlit_app.py
├── rag/
│   ├── loader.py
│   ├── embedder.py
│   └── retriever.py
├── data/
│   └── sample_docs/
├── notebooks/
└── README.md
```

## ⚙️ Features

- Load PDF, TXT, or CSV documents
- Automatic chunking and embedding
- Vector storage via FAISS
- LLM-powered query answering
- Simple UI with Streamlit

## 🚀 Quickstart

```bash
# Install dependencies
pip install -r requirements.txt

# Run the Streamlit app
streamlit run app/streamlit_app.py

```
## 🔄 Future Improvements
- Switch FAISS to Pinecone or ChromaDB
- Deploy via Docker + FastAPI
- Add PDF OCR for scanned docs
- Multi-document search

## 📣 Author

**Pradeep Kumar**  
[LinkedIn](https://www.linkedin.com/in/pradeep22saini/) | [Portfolio](#)

---
