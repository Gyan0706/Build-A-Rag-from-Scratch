# Build-A-RAG-from-Scratch

This project demonstrates how to build a **Retrieval-Augmented Generation (RAG)** pipeline from scratch using Python. It walks through the process of loading documents, generating embeddings, storing them, and querying them to provide intelligent responses using LLMs.

## 🚀 Features

- 📄 Load text documents from a local folder
- 🧠 Generate vector embeddings using OpenAI or HuggingFace models
- 🗃️ Store embeddings using FAISS (Facebook AI Similarity Search)
- 🔍 Retrieve relevant context from documents based on user queries
- 🧾 Generate context-aware responses using a Language Model

## 📁 Folder Structure

```

build\_rag\_from\_scratch-main/
│
├── data/                    # Text files to index and search
│   ├── behaviuor1.txt
│   ├── behaviuor2.txt
│   └── behaviuor3.txt
│
├── vector\_store/           # FAISS index is saved here
│
├── main.py                 # Main script to run the RAG pipeline
├── requirements.txt        # List of dependencies
└── env.js                  # Stores environment variables (API keys, etc.)

````

## 🔧 Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Gyan0706/Build-A-Rag-from-Scratch.git
   cd Build-A-Rag-from-Scratch
````

2. **Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   venv\Scripts\activate   # On Windows
   # source venv/bin/activate   # On Linux/Mac
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up your environment variables:**
   Create a file named `env.js` in the root folder with your keys:

   ```js
   // env.js
   export const OPENAI_API_KEY = "your_openai_api_key_here";
   ```

5. **Run the main script:**

   ```bash
   python main.py
   ```

## 🧠 How It Works

1. Reads `.txt` files from the `data/` directory.
2. Splits and embeds them using an embedding model (like OpenAI Embeddings).
3. Stores embeddings in a FAISS vector index.
4. Accepts a query, retrieves top relevant chunks from FAISS.
5. Sends those chunks to a Language Model for a final answer.

## 📦 Dependencies

* `openai`
* `faiss-cpu`
* `langchain`
* `tqdm`
* `python-dotenv`

> Make sure your OpenAI key is valid and environment is properly set up.

