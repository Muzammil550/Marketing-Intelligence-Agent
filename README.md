# 🤖 Sentiment-Aware AI Query Routing Agent

A LangGraph-powered AI assistant that intelligently classifies user sentiment, dynamically selects the best response path—**RAG**, **Tavily Web Search**, or **LLMs**—and continuously learns through memory-enhanced interactions. Designed for real-time analytics, marketing insights, and personalized user responses.

---

## 🧠 Project Overview

This assistant performs **sentiment classification** and routes queries based on their emotional tone and content relevance using:

- ✅ **MLP Sentiment Classifier** (trained to 83% accuracy)
- 📚 **Retrieval-Augmented Generation (RAG)** with ChromaDB, SQL, and .txt documents
- 🌐 **Live Web Search** via Tavily API
- 🧬 **LLMs** (LLaMA 70B, Mistral) for fallback or generic queries
- 🧠 **LangChain Memory** for adaptive, stateful responses

---

## 📌 Features

- 🔍 **Sentiment Detection**: Sentence transformer + MLP classifier (.pkl saved for reuse)
- 📡 **Multi-Retriever Query Routing**: Choose between single/multi/meta retrievers
- 🔄 **Conditional Agent Flow**: Route inputs based on sentiment, topic, and recency
- 💬 **Contextual Memory**: Retains previous interactions for consistent responses
- 🛠 **LangGraph Workflow**: Modular, node-based logic for transparent routing

---

## ⚙️ Technologies Used

| Type             | Tools & Libraries |
|------------------|-------------------|
| Language         | Python |
| Backend API      | FastAPI |
| AI Frameworks    | LangChain, LangGraph |
| LLMs             | LLaMA 70B, Mistral 8x7B |
| Embeddings       | HuggingFace Sentence Transformers |
| Classifier       | Scikit-learn MLPClassifier |
| Retrieval Layer  | ChromaDB, SQL, Text |
| Search API       | Tavily |
| Other Tools      | Prompt Engineering, TypedDict, Pydantic |

---

## 🗂 Directory Structure

```bash
📦 sentiment-agent/
├── app.py                  # FastAPI app with POST endpoint
├── classifier/
│   ├── mlp.pkl             # Trained MLP sentiment model
│   └── train_classifier.py # Classifier training script
├── retrievers/
│   ├── rag.py              # RAG retriever logic
│   └── tavily_search.py    # Tavily API integration
├── agents/
│   └── langgraph_agent.py  # LangGraph conditional agent logic
├── memory/
│   └── memory_store.py     # Agent memory management
├── utils/
│   └── helpers.py          # Utilities and prompt formatters
├── requirements.txt        # Python dependencies
