<h1 align="center">📄 PDF-RAG: Intelligent Document Question Answering</h1>

<p align="center">
  An intelligent Retrieval-Augmented Generation (RAG) system for answering
  questions from PDF documents using semantic search and a Large Language Model.
</p>

---

## 📌 Overview

PDF-RAG is an intelligent question-answering system designed to retrieve relevant information from PDF documents and generate answers based on the retrieved context.

The system combines PDF text extraction, text chunking, semantic embeddings, vector similarity search, and a Large Language Model to provide context-aware answers.

The project uses Sentence Transformers to generate embeddings, FAISS for efficient similarity search, and Mistral-Nemo-Instruct-2407 for answer generation.

---

## ✨ Features

- 📄 PDF document processing
- 🔤 Automatic text extraction
- ✂️ Text chunking
- 🧠 Semantic text embeddings
- 🔎 Similarity search using FAISS
- 🤖 Mistral Large Language Model
- 💬 Context-based question answering
- 🎯 Retrieval-Augmented Generation (RAG)
- 📚 Question answering over document content
- 🚫 Reduces unsupported answers by restricting responses to retrieved context

---

## 🏗️ System Architecture

```text
                PDF Document
                     │
                     ▼
              Text Extraction
                     │
                     ▼
                Text Chunking
                     │
                     ▼
           Sentence Embeddings
                     │
                     ▼
              FAISS Index
                     │
                     │
User Question ───────┘
       │
       ▼
Question Embedding
       │
       ▼
Similarity Search
       │
       ▼
Relevant Context
       │
       ▼
Mistral Language Model
       │
       ▼
Generated Answer
