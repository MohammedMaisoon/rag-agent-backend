# rag-agent-backend
Zero-cost Agentic RAG system built with self-hosted n8n, OpenRouter, Qdrant vector database, and Hugging Face embeddings. Features automated context retrieval, window memory, and multi-tool orchestration.
# 🤖 Agentic RAG Assistant (Zero-Cost Stack)

An autonomous Retrieval-Augmented Generation (RAG) assistant built using a completely free, open-source, and self-hosted AI architecture. This project uses **n8n** as the orchestrator to dynamically query custom vector embeddings from **Qdrant** using **Hugging Face** inference, and reasons over answers via **OpenRouter**.

---

## 🏗️ Architecture Overview
![n8n](https://img.shields.io/badge/n8n-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC2626?style=for-the-badge&logo=qdrant&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)

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
