
# 🍕 Local AI Agent With RAG (CSV)

A **local AI assistant** that answers questions about a pizza restaurant using **retrieval-augmented generation (RAG)**. The agent retrieves relevant reviews from a local CSV file and provides context-aware answers using a local LLM.

---

## ✨ Features

- **Retrieval-Augmented Generation (RAG):** Improves LLM responses by fetching relevant data.  
- **Local LLM integration:** Runs on your machine via Ollama, no API keys required.  
- **Interactive Q&A:** Ask questions in the terminal and get grounded answers.  
- **Modular Design:** Separate retriever logic for flexible data sources.

---

## 🛠️ Tech Stack

- Python 3.10+  
- [LangChain](https://www.langchain.com/) – LLM orchestration framework  
- [LangChain-Ollama](https://python.langchain.com/docs/integrations/llms/ollama) – Local LLM integration  
- [Chroma](https://www.trychroma.com/) – Vector database for embeddings  
- Virtual Environment (`venv`)

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/LeonTang-LeonTang/-Local_AI_Agent_With_RAG_CSV.git
cd -Local_AI_Agent_With_RAG_CSV
```

### 2. Create and activate a virtual environment
```bash
python3 -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4.Run the agent
```bash
python main.py
```

## 🧩 How It Works

1.	User types a question in the terminal.
2.	The retriever (vector.py) fetches relevant reviews from CSV.
3.	Reviews and the question are combined into a prompt template.
4.	Ollama LLM generates a grounded answer.
## 📂 Project Structure
```bash
.
├── main.py          # Interactive Q&A entry point
├── vector.py        # Retriever logic for fetching relevant reviews
├── requirements.txt # Python dependencies
├── README.md        # This file
├── venv/            # Virtual environment (not committed)
```
## 🔮 Possible Improvements
•	Add a web UI (Streamlit or FastAPI)

•	Support multiple restaurants or datasets

•	Fine-tune embeddings for better retrieval relevance

•	Add logging for queries and results

## ⚡ Usage Example
```bash
python main.py
```

## Sample interaction:
```bash
-------------------------------
Ask your question (q to quit):
> What pizzas are recommended?
> The AI recommends the Margherita and Pepperoni pizzas based on customer reviews.
```