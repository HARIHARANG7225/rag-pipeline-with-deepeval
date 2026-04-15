# End-to-End RAG Pipeline using LlamaIndex, ChromaDB, Gemini, and DeepEval

This project demonstrates an **end-to-end Retrieval-Augmented Generation (RAG) pipeline** built using **LlamaIndex**, **ChromaDB**, **Google Gemini**, and **DeepEval**.

The system loads documents, splits them into chunks, creates embeddings, stores them in a vector database, retrieves relevant content for a given query, generates answers using an LLM, and evaluates the response quality.

---

## Project Overview

The purpose of this project is to build a **document-based Question Answering system** using RAG architecture.

Instead of relying only on the LLM's pretrained knowledge, this system retrieves relevant document context and uses it to generate more grounded answers.

---

## Workflow

### 1. Load Documents
- Reads files from a local `data` directory
- Validates that the data folder exists before processing

### 2. Chunk Documents
- Uses `TokenTextSplitter`
- Splits documents into chunks of fixed size
- Maintains overlap between chunks to preserve context

### 3. Generate Embeddings
- Uses **GoogleGenAIEmbedding**
- Converts text chunks into vector representations

### 4. Store in Vector Database
- Uses **ChromaDB**
- Stores document embeddings for semantic retrieval

### 5. Build Vector Index
- Creates a `VectorStoreIndex` from the vector store
- Enables similarity-based document retrieval

### 6. Query with LLM
- Uses **Gemini 2.5 Flash**
- Retrieves top relevant chunks and generates final answer

### 7. Evaluate the Response
- Uses **DeepEval**
- Measures answer relevancy score
- Returns reasoning behind the evaluation

---

## Tech Stack

- Python
- LlamaIndex
- ChromaDB
- Google Gemini
- DeepEval
- python-dotenv

---

## Features

- End-to-end RAG pipeline
- Document ingestion and chunking
- Gemini embedding integration
- Chroma vector storage
- Semantic retrieval
- LLM-powered question answering
- Answer relevancy evaluation
- Modular and practical workflow

---

## Installation

```bash
pip install llama-index chromadb llama-index-vector-stores-chroma llama-index-embeddings-google-genai llama-index-llms-gemini python-dotenv deepeval


