# RAG From Scratch

This repository is a comprehensive, hands-on guide to building Retrieval-Augmented Generation (RAG) systems from scratch using Python and LangChain. Each notebook explores a different aspect of the RAG landscape, from basic retrieval to advanced query transformation, routing, and indexing strategies.

---

## Table of Contents

- [Overview](#overview)
- [Notebooks](#notebooks)
  - [1. rag_basic.ipynb](#1-rag_basicipynb---rag-basics)
  - [2. rag_indexing.ipynb](#2-rag_indexingipynb---advanced-indexing)
  - [3. rag_query_transformation.ipynb](#3-rag_query_transformationipynb---query-transformations)
  - [4. rag_retrieval.ipynb](#4-rag_retrievalipynb---retrieval--re-ranking)
  - [5. rag_routing.ipynb](#5-rag_routingipynb---routing--query-construction)
- [Setup](#setup)
- [References](#references)

---

## Overview

Large Language Models (LLMs) are powerful but limited by their static training data. Retrieval-Augmented Generation (RAG) enhances LLMs by grounding their outputs in up-to-date, external documents. This repository demonstrates how to build and experiment with RAG pipelines, covering:

- Document loading, chunking, and embedding
- Vectorstore indexing and retrieval
- Query rewriting and fusion
- Routing and metadata filtering
- Advanced retrieval and re-ranking

---

## Notebooks

### 1. `rag_basic.ipynb` - RAG Basics

- **Goal:** Introduce the core RAG pipeline: document loading, splitting, embedding, indexing, retrieval, and generation.
- **Topics:**
  - Setting up LangChain and OpenAI API keys
  - Loading web documents and splitting into chunks
  - Embedding with OpenAI
  - Storing and retrieving with Chroma vectorstore
  - Simple RAG chain for question answering
  - Token counting, cosine similarity, and prompt engineering

---

### 2. `rag_indexing.ipynb` - Advanced Indexing

- **Goal:** Explore advanced indexing strategies for RAG, including multi-representation and multi-modal approaches.
- **Topics:**
  - Multi-vector and parent document retrievers
  - Summarization for indexing
  - RAPTOR and ColBERT integration
  - Indexing Wikipedia and web content
  - Using RAGatouille for ColBERT-based retrieval

---

### 3. `rag_query_transformation.ipynb` - Query Transformations

- **Goal:** Demonstrate advanced query transformation techniques to improve retrieval quality.
- **Topics:**
  - Multi-query generation (multiple perspectives)
  - RAG-Fusion and Reciprocal Rank Fusion (RRF)
  - Decomposition into sub-questions
  - Recursive and individual answering of sub-questions
  - Step-back prompting
  - HyDE (Hypothetical Document Embeddings)
  - End-to-end RAG chains with query rewriting

---

### 4. `rag_retrieval.ipynb` - Retrieval & Re-ranking

- **Goal:** Focus on retrieval strategies and re-ranking for improved answer quality.
- **Topics:**
  - RAG-Fusion and RRF for document ranking
  - Cohere Re-Rank integration
  - Contextual compression retrievers
  - CRAG (Composable RAG) and Self-RAG
  - Impact of long context windows

---

### 5. `rag_routing.ipynb` - Routing & Query Construction

- **Goal:** Explore routing queries to the correct retriever or index and constructing structured queries.
- **Topics:**
  - Logical and semantic routing using function-calling and embeddings
  - Branching logic for multi-index retrieval
  - Semantic prompt routing (e.g., math vs. physics)
  - Query structuring for metadata filters (e.g., YouTube transcripts)
  - Using Pydantic schemas for structured search

---

## Setup

1. **Clone the repository:**
   ```sh
   git clone <repo-url>
   cd rag-from-scratch-main
   ```

2. **Install dependencies:**
   Each notebook lists required packages at the top. Typical requirements:
   ```sh
   pip install langchain_community tiktoken langchain-openai langchainhub chromadb langchain youtube-transcript-api pytube cohere ragatouille
   ```

3. **API Keys:**
   - Set your OpenAI and (optionally) Cohere API keys as environment variables.
   - For LangSmith tracing, set your LangChain API key.

4. **Run Notebooks:**
   Open the notebooks in VS Code or Jupyter and follow the instructions in each section.

---

## References

- [LangChain Documentation](https://python.langchain.com/)
- [RAG Quickstart](https://python.langchain.com/docs/use_cases/question_answering/quickstart)
- [LangChain Blog](https://blog.langchain.dev/)
- [RAGatouille (ColBERT)](https://github.com/karpathy/ragatouille)
- [Cohere Re-Rank](https://txt.cohere.com/rerank/)
- [YouTube Transcript API](https://github.com/jdepoix/youtube-transcript-api)

---

## License

MIT

---

**Explore, experiment, and extend!**  
This repository is designed for learning and prototyping RAG systems with modern LLM