# Semantic Vector Database with HNSW & RAG

This project is a semantic vector database built from scratch in C++17. It supports multiple nearest neighbour search algorithms, document retrieval, and a Retrieval-Augmented Generation (RAG) pipeline using Ollama.

The project also includes a web-based interface to visualize vector embeddings, compare search algorithms, and chat with uploaded documents.

---

## Features

- Custom implementation of HNSW (Hierarchical Navigable Small World)
- KD-Tree based nearest neighbour search
- Brute Force search for comparison
- REST API built in C++
- Interactive web interface
- PCA-based vector visualization
- Multiple distance metrics
  - Cosine Similarity
  - Euclidean Distance
  - Manhattan Distance
- Document insertion and chunking
- Semantic document retrieval
- Local RAG pipeline using Ollama
- AI chat over uploaded documents

---

## Tech Stack

### Backend

- C++17
- REST API
- Custom HNSW
- KD-Tree
- Brute Force Search

### Frontend

- HTML
- CSS
- JavaScript
- Canvas API

### AI

- Ollama
- nomic-embed-text
- llama3.2

---

## Search Algorithms

The application supports three search methods:

- HNSW (Approximate Nearest Neighbour)
- KD-Tree
- Brute Force

The benchmark section in the UI compares the latency of these algorithms.

---

## REST API

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/items` | Get all vectors |
| POST | `/insert` | Insert a vector |
| DELETE | `/delete/{id}` | Delete a vector |
| GET | `/search` | Semantic search |
| GET | `/benchmark` | Compare search algorithms |
| GET | `/hnsw-info` | HNSW statistics |
| GET | `/status` | Ollama status |
| POST | `/doc/insert` | Insert document |
| GET | `/doc/list` | List documents |
| DELETE | `/doc/delete/{id}` | Delete document |
| POST | `/doc/search` | Retrieve relevant chunks |
| POST | `/doc/ask` | Ask questions using RAG |

---

## Project Structure

```
Semantic-Vector-Database
│
├── backend/
├── frontend/
├── screenshots/
├── CMakeLists.txt
└── README.md
```

---

## Screenshots

### Main Dashboard

(Add screenshot here)

### Search Results

(Add screenshot here)

### Knowledge Base

(Add screenshot here)

### AI Chat

(Add screenshot here)

### Benchmark

(Add screenshot here)

---

## Running the Project

Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Build the project

```bash
mkdir build
cd build
cmake ..
cmake --build .
```

Run Ollama

```bash
ollama serve
ollama pull nomic-embed-text
ollama pull llama3.2
```

Run the backend server.

Finally, open `index.html` in your browser.

---
## Third-Party Libraries

- cpp-httplib (MIT License)
- nlohmann/json (MIT License)

---

## Note

The frontend can be viewed independently, but document retrieval and AI chat require the C++ backend and Ollama to be running locally.

---

## Author

Kanishka

Biochemical Engineering  
IIT (BHU) Varanasi
