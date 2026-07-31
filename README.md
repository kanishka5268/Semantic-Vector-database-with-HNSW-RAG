# Semantic-Search-Engine-with-HNSW-RAG

A high-performance **Vector Database** developed in **C++** that supports semantic search using multiple nearest-neighbor search algorithms. The project also implements a **Retrieval-Augmented Generation (RAG)** pipeline by integrating a local Large Language Model (LLM) through **Ollama**, enabling users to query their own documents using natural language.

The application includes an interactive web interface for vector search, document management, benchmarking, and visualization of semantic relationships.

---

## Features

- Implemented three vector search algorithms:
  - Hierarchical Navigable Small World (HNSW)
  - KD-Tree
  - Brute Force Search
- Supports multiple distance metrics:
  - Cosine Similarity
  - Euclidean Distance
  - Manhattan Distance
- RESTful API for vector insertion, deletion, retrieval, and benchmarking
- Retrieval-Augmented Generation (RAG) pipeline using Ollama
- Automatic document chunking and embedding generation
- Interactive web interface for semantic search
- PCA-based visualization of vector embeddings
- Benchmarking module for comparing search algorithms

---

## System Architecture

```
                 User Query
                      │
                      ▼
              Embedding Model
            (nomic-embed-text)
                      │
                      ▼
             HNSW Vector Index
                      │
              Top-K Retrieval
                      │
                      ▼
            Retrieved Documents
                      │
                      ▼
           Local LLM (llama3.2)
                      │
                      ▼
             Generated Response
```

---

## Technology Stack

### Programming Language
- C++17

### Backend
- cpp-httplib
- REST APIs

### Search Algorithms
- HNSW
- KD-Tree
- Brute Force Search

### AI Components
- Ollama
- nomic-embed-text
- llama3.2
- Retrieval-Augmented Generation (RAG)

### Frontend
- HTML
- CSS
- JavaScript

---

## Project Workflow

### Semantic Search

```
Text Query
      │
      ▼
Generate Embedding
      │
      ▼
Vector Similarity Search
      │
      ▼
Top-K Similar Results
```

---

### RAG Pipeline

```
User Question
       │
       ▼
Embedding Generation
       │
       ▼
Vector Retrieval
       │
       ▼
Relevant Context
       │
       ▼
LLM Inference
       │
       ▼
Generated Answer
```

---

## Search Algorithms

### Hierarchical Navigable Small World (HNSW)

- Production-grade Approximate Nearest Neighbor search
- Graph-based indexing
- Optimized for large-scale vector retrieval
- Approximate search complexity: O(log N)

---

### KD-Tree

- Space-partitioning data structure
- Efficient for low-dimensional vectors
- Used for comparison with HNSW

---

### Brute Force Search

- Computes distance against every stored vector
- Exact nearest-neighbor search
- Baseline implementation for benchmarking

---

## Distance Metrics

- Cosine Similarity
- Euclidean Distance
- Manhattan Distance

---

## REST API

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/search` | Search nearest vectors |
| POST | `/insert` | Insert vector/document |
| DELETE | `/delete` | Delete vector |
| POST | `/doc/ask` | Ask questions using RAG |
| GET | `/benchmark` | Compare search algorithms |
| GET | `/hnsw-info` | Retrieve HNSW statistics |

---

## Project Highlights

- Implemented a vector database from scratch in C++
- Developed three independent nearest-neighbor search implementations
- Integrated semantic embeddings using Ollama
- Built an end-to-end Retrieval-Augmented Generation pipeline
- Designed REST APIs for vector management
- Visualized embedding distributions using PCA
- Benchmarked multiple search algorithms on the same dataset

---

## Future Improvements

- PDF document ingestion
- Persistent vector storage
- Metadata-based filtering
- User authentication
- Docker deployment
- Hybrid keyword + semantic search

---

## Learning Outcomes

This project helped strengthen my understanding of:

- Vector Databases
- Semantic Search
- Approximate Nearest Neighbor Algorithms
- HNSW
- KD-Trees
- REST API Development
- Retrieval-Augmented Generation (RAG)
- Large Language Models
- Embedding Models
- Information Retrieval
- C++ System Design

---

## Acknowledgements

This project was developed as a learning-focused implementation to gain practical experience with modern semantic search systems, vector databases, and Retrieval-Augmented Generation workflows.
