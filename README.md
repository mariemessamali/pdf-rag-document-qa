<h1 align="center">📄 PDF-RAG: Intelligent Document Question Answering</h1>

<p align="center">
  An intelligent Retrieval-Augmented Generation system for answering questions
  from PDF documents using semantic search and a Large Language Model.
</p>

---

## 📌 Overview

PDF-RAG is an intelligent question-answering system that allows users to ask
questions about the content of PDF documents.

The system combines document processing, semantic embeddings, vector search,
and a Large Language Model to retrieve relevant information from the document
and generate accurate answers based only on the retrieved context.

The project uses FAISS for efficient similarity search and Mistral-Nemo-Instruct
for answer generation.

## ✨ Features

- 📄 PDF document processing
- ✂️ Text chunking
- 🧠 Semantic text embeddings
- 🔎 Similarity search using FAISS
- 🤖 Mistral Large Language Model
- 💬 Context-based question answering
- 🎯 Retrieval-Augmented Generation (RAG)
- 🚫 Prevents answers outside the provided document context

## 🏗️ System Architecture

```text
PDF Document
     ↓
Text Extraction
     ↓
Text Chunking
     ↓
Sentence Embeddings
     ↓
FAISS Vector Index
     ↓
User Question
     ↓
Question Embedding
     ↓
Similarity Search
     ↓
Relevant Context
     ↓
Mistral Language Model
     ↓
Generated Answer
