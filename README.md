# 🚀 Retrieval-Augmented Generation (RAG) using Llama 3.1 70B, Groq API, ChromaDB & LangChain

## 📌 Project Overview

This project demonstrates a complete **Retrieval-Augmented Generation (RAG)** pipeline using **Llama 3.1 70B**, **Groq API**, **LangChain**, **ChromaDB**, and **Hugging Face Embeddings**.

The system allows users to upload or process PDF documents, convert them into vector embeddings, store them in a vector database, and perform intelligent question-answering based on the document content.

Instead of relying solely on the Large Language Model's pre-trained knowledge, the model retrieves relevant information from the document and generates context-aware responses.

---

## 🎯 Objectives

* Build an end-to-end RAG application
* Enable document-based Question Answering
* Reduce LLM hallucinations using retrieved context
* Store document embeddings in a vector database
* Integrate Groq-hosted Llama 3.1 70B for fast inference

---

## 🛠️ Tech Stack

### Programming Language

* Python

### Frameworks & Libraries

* LangChain
* ChromaDB
* Hugging Face Embeddings
* Groq API
* Unstructured
* Requests

### Large Language Model

* Llama 3.1 70B Versatile

### Vector Database

* ChromaDB

### Embedding Model

* HuggingFace Embeddings

---

## 🏗️ Architecture

```text
PDF Document
      │
      ▼
Document Loader
      │
      ▼
Text Chunking
      │
      ▼
Embedding Generation
      │
      ▼
Chroma Vector Database
      │
      ▼
Retriever
      │
      ▼
Llama 3.1 70B (Groq API)
      │
      ▼
Answer Generation
```

---

## 🔄 Workflow

### Step 1: Document Acquisition

A PDF document is downloaded and stored locally.

### Step 2: Document Loading

The document is loaded using:

```python
UnstructuredFileLoader
```

### Step 3: Text Chunking

The content is split into manageable chunks:

```python
chunk_size = 2000
chunk_overlap = 400
```

### Step 4: Embedding Creation

Text chunks are converted into vector embeddings using:

```python
HuggingFaceEmbeddings()
```

### Step 5: Vector Storage

Embeddings are stored in:

```python
ChromaDB
```

### Step 6: Retrieval

Relevant chunks are retrieved based on user queries.

### Step 7: Response Generation

The retrieved context is passed to:

```python
Llama-3.1-70B-Versatile
```

through the Groq API to generate accurate responses.

---

## ✨ Features

* PDF Question Answering
* Retrieval-Augmented Generation (RAG)
* Vector Search with ChromaDB
* Fast Inference using Groq API
* Semantic Search
* Context-Aware Responses
* Reduced Hallucinations
* Scalable Architecture

---

## 📂 Project Structure

```bash
RAG-Llama3-Groq-ChromaDB/
│
├── data/
│   └── documents.pdf
│
├── vector_db/
│
├── notebooks/
│   └── RAG_using_LLAMA3_70B.ipynb
│
├── requirements.txt
│
└── README.md
```

---

## 🚀 Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/RAG-Llama3-Groq-ChromaDB.git

cd RAG-Llama3-Groq-ChromaDB
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 API Configuration

Create a Groq API key from:

https://console.groq.com

Set your API key:

```python
os.environ["GROQ_API_KEY"] = "YOUR_API_KEY"
```

---

## 💬 Example Query

```python
query = "What are the built-in functions available in Python?"
```

### Output

```text
The document contains several Python built-in functions including:
print(), len(), type(), range(), input(), max(), min(), sum(), etc.
```

---

## 📈 Benefits of RAG

* Improves factual accuracy
* Uses external knowledge sources
* Supports domain-specific documents
* Minimizes hallucinations
* Enhances enterprise AI applications

---

## 🔮 Future Enhancements

* Multi-PDF Support
* Conversational Memory
* Hybrid Search
* Reranking Models
* Streamlit Frontend
* Docker Deployment
* Cloud Deployment (AWS/Azure/GCP)
* Citation-Based Answers

---

## 👨‍💻 Author

**Banala Ratna Raju**

AI/ML Engineer | Generative AI Developer

### Skills

* Generative AI
* Retrieval-Augmented Generation (RAG)
* LangChain
* Llama 3
* Vector Databases
* ChromaDB
* Machine Learning
* Deep Learning
* Python

⭐ If you found this project useful, consider giving it a star.
