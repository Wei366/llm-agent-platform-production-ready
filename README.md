# agent-platform-rag-multiagent-eval
# 🚀 AI Agent Platform (RAG + Multi-Agent + Eval)

A production-oriented LLM Agent system with multi-agent collaboration, RAG pipeline, and evaluation harness.

---

## ✨ Features

* 🤖 Multi-Agent System (Planner / Executor / Critic)
* 📚 RAG Pipeline (Hybrid Retrieval + Rerank)
* 🛠️ Tool Calling (Dynamic Tool Registry)
* 🧠 Memory Management (Short-term + Long-term)
* 📊 Evaluation System (Accuracy / Cost / Latency)
* ⚡ FastAPI-based async service

---

## 🏗️ Architecture

```text
User → API → Agent Core → (Tools | RAG | Memory)
```

---

## 🧠 Multi-Agent Design

* **Planner**: Breaks down complex tasks into steps
* **Executor**: Executes each step (tool / RAG)
* **Critic**: Evaluates results and triggers retry

Supports:

* self-reflection loop
* retry mechanism
* failure recovery

---

## 🔍 RAG Pipeline

```text
query → rewrite → hybrid retrieval → rerank → generation
```

* Hybrid retrieval (BM25 + embedding)
* Cross-encoder reranking
* Top-k filtering to reduce noise

---

## 🛠️ Tool System

* Dynamic tool registration (JSON schema)
* Supports:

  * search
  * calculator
  * database query

---

## 📊 Evaluation System

* Golden dataset-based evaluation

* Metrics:

  * correctness
  * hallucination rate
  * latency
  * token cost

* LLM-as-judge for answer evaluation

* Regression testing for prompt / system changes

---

## ⚙️ Tech Stack

* Python / FastAPI
* LangGraph (or custom agent loop)
* Qdrant / Milvus (vector DB)
* Elasticsearch (optional hybrid search)

---

## 🚀 Quick Start

```bash
git clone https://github.com/Wei366/agent-platform
cd agent-platform
pip install -r requirements.txt
uvicorn main:app --reload
```

---

## 📌 Future Work

* GraphRAG integration
* MCP protocol support
* advanced memory compression
* cost optimization (routing / caching)

---

## 🧠 Key Insights

* Multi-agent improves stability for complex tasks
* RAG quality depends more on ranking than retrieval
* Evaluation is critical for iterative improvement

---


