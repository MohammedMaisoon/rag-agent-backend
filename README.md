# rag-agent-backend
Zero-cost Agentic RAG system built with self-hosted n8n, OpenRouter, Qdrant vector database, and Hugging Face embeddings. Features automated context retrieval, window memory, and multi-tool orchestration.
# 🤖 Agentic RAG Assistant (Zero-Cost Stack)

An autonomous Retrieval-Augmented Generation (RAG) assistant built using a completely free, open-source, and self-hosted AI architecture. This project uses **n8n** as the orchestrator to dynamically query custom vector embeddings from **Qdrant** using **Hugging Face** inference, and reasons over answers via **OpenRouter**.

---
n8n agentic-rag qdrant openrouter huggingface langchain ai-agent vector-database

## 🏗️ Architecture Overview

```text
[ User / Chat UI ] 
        │
        ▼
[ n8n AI Agent Workflow ]
        │
        ├──► Memory: Window Buffer Memory
        │
        ├──► Embeddings: Hugging Face Inference Model
        │
        ├──► Vector Store: Qdrant Vector DB (Retriever Tool)
        │
        └──► LLM Router: OpenRouter API (Auto / Llama / Qwen)
