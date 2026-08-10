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


🔄 How It Works

The system follows a Retrieval-Augmented Generation pipeline:

The PDF document is loaded and processed.
Text is extracted from the PDF.
The extracted text is divided into smaller chunks.
Each text chunk is converted into a numerical embedding.
The embeddings are stored in a FAISS vector index.
The user's question is converted into an embedding.
FAISS searches for the most relevant document chunks.
The retrieved chunks are provided as context to the language model.
The Mistral model generates an answer using the retrieved context.
If the required information is not available in the retrieved context, the system can indicate that the document does not contain the requested information.

🧠 Retrieval-Augmented Generation

Retrieval-Augmented Generation (RAG) combines information retrieval with text generation.

Instead of relying only on the knowledge stored inside the language model, the system first searches the provided document for relevant information.

The retrieved information is then passed to the language model as context.

This approach helps the system provide answers that are grounded in the content of the uploaded document.

User Question
      ↓
Retrieve Relevant Information
      ↓
Provide Retrieved Context
      ↓
Language Model
      ↓
Final Answer
🛠️ Technologies Used
Technology	Purpose
Python	Main programming language
PyTorch	Deep learning framework
Hugging Face Transformers	Language model loading and generation
Mistral-Nemo-Instruct-2407	Answer generation
Sentence Transformers	Text embedding generation
FAISS	Vector similarity search
PyPDF2	PDF text extraction
NumPy	Numerical processing
