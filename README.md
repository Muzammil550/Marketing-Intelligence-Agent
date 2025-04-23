🧠 Sentiment-Aware AI Agent for Intelligent Query Routing & Live Analytics
This project showcases a powerful LangGraph-based AI agent designed to classify sentiment, dynamically route queries, and generate intelligent responses using a multi-stage pipeline powered by MLP classifiers, RAG, Tavily API, and LLMs.

🚀 Project Overview
This intelligent assistant serves as a context-aware conversational agent that responds to user queries based on their sentiment, intent, and topic. It's built using LangChain, FastAPI, and custom-trained machine learning models for real-time performance.

🧩 Key Features
🔍 Sentiment Classification: Classifies user sentiment using sentence embeddings and an MLP classifier with 83% accuracy.

⚡ Smart Query Routing: Routes inputs to:

RAG pipeline (for stored knowledge)

Tavily (for real-time information)

LLMs (for general completions)

🧠 Multi-Agent Architecture: Built using LangGraph to structure nodes and decision logic with memory and prompt parsing.

📊 AI Report Generation: A multi-agent system also generates analytical reports using different LLMs and planning agents.

💾 Saved Classifier: Trained classifier saved as mlp.pkl for easy reuse and production scaling.

🧬 Retrieval Flexibility: Supports multiple types of retrievers — single, multi, and meta/self-query retrievers — from ChromaDB, SQL, or .txt sources.

🛠️ Technologies Used
Python

LangChain, LangGraph

FastAPI

HuggingFace Transformers & Embeddings

Scikit-learn MLPClassifier

ChromaDB, SQL, .txt storage

Tavily API

LLMs: LLaMA 70B, Mistral 8x7B

RAG (Retrieval-Augmented Generation)

Prompt Engineering, Agentic Memory

TypedDict, Pydantic BaseModel

📁 Repository Structure
bash
Copy
Edit
📦 sentiment-routing-agent
 ┣ 📂 models/
 ┃ ┗ 📄 mlp.pkl                # Trained sentiment classifier
 ┣ 📂 agents/
 ┃ ┗ 📄 langgraph_pipeline.py  # LangGraph decision and routing logic
 ┣ 📂 retrievers/
 ┃ ┗ 📄 retriever_config.py    # ChromaDB / SQL / .txt retriever setup
 ┣ 📄 main.py                  # FastAPI endpoint
 ┣ 📄 requirements.txt         # Python dependencies
 ┗ 📄 README.md                # You are here 🚀
📬 API Usage
Once the app is running:

🔗 POST /ask
json
Copy
Edit
{
  "question": "What are the latest trends in marketing?"
}
Response:

json
Copy
Edit
{
  "response": "According to recent marketing reports..."
}
🧪 How to Run Locally
Clone this repo

Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Start the FastAPI app

bash
Copy
Edit
uvicorn main:app --reload
Test the API via browser or Postman at:

arduino
Copy
Edit
http://127.0.0.1:8000/docs
🤝 Contributions
Feel free to fork, open issues, or submit PRs. Feedback and collaboration are welcome!

📜 License
This project is open-source and available under the MIT License.

