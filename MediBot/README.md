🩺 MediBot — AI Powered Medical Chatbot

An intelligent AI-powered medical chatbot built using Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG) to provide accurate, context-aware, and trustworthy medical responses from verified medical documents.

The system leverages semantic search, vector databases, and modern LLM orchestration frameworks to reduce hallucinations and generate source-grounded healthcare answers.

🚀 Features
📚 PDF-based medical knowledge ingestion
🔍 Semantic search using vector embeddings
🧠 Retrieval-Augmented Generation (RAG)
🤖 LLM-powered medical question answering
📄 Source citation and traceability
💬 Interactive Streamlit chat interface
⚡ Fast vector retrieval with FAISS/Chroma
🔒 Secure API key management using .env
🧩 Modular and scalable architecture
🏗️ Project Architecture
Medical PDFs
      ↓
Text Extraction
      ↓
Chunking
      ↓
Embeddings Generation
      ↓
Vector Database
      ↓
Semantic Retrieval
      ↓
LLM + Prompt Template
      ↓
Medical Answer Generation
      ↓
Streamlit Chat Interface
🧠 Tech Stack
Technology	Purpose
Python	Core programming language
LangChain	LLM orchestration framework
Hugging Face	Embedding & LLM models
Mistral 7B	Open-source LLM
Sentence Transformers	Text embeddings
FAISS / ChromaDB	Vector database
Streamlit	Frontend UI
PyPDF	PDF text extraction
dotenv	Environment variable management
📂 Folder Structure
MediBot/
│
├── data/                  # Medical PDFs
├── vectorstore/           # Saved vector embeddings
├── src/
│   ├── helper.py
│   ├── prompt.py
│   ├── retriever.py
│   ├── embeddings.py
│   └── chains.py
│
├── app.py                 # Streamlit frontend
├── requirements.txt
├── store_index.py         # Vector DB creation
├── .env
└── README.md
⚙️ Installation
1️⃣ Clone Repository
git clone https://github.com/yourusername/MediBot.git
cd MediBot
2️⃣ Create Virtual Environment
Windows
python -m venv venv
venv\Scripts\activate
Linux / Mac
python3 -m venv venv
source venv/bin/activate
3️⃣ Install Dependencies
pip install -r requirements.txt
🔑 Environment Variables

Create a .env file:

HUGGINGFACEHUB_API_TOKEN=your_huggingface_api_key
📚 Add Medical PDFs

Place your medical documents inside:

data/

Example:

data/Gale-Encyclopedia-of-Medicine.pdf
🧠 Create Vector Database

Run:

python store_index.py

This process:

extracts PDF text
chunks documents
generates embeddings
stores vectors in FAISS/ChromaDB
▶️ Run the Application
streamlit run app.py
💬 Example Queries
What are symptoms of diabetes?

How is lung cancer treated?

What causes high blood pressure?

Explain symptoms of malaria.
🧩 How RAG Works
Step 1 — User Query

User asks:

"What are symptoms of cancer?"
Step 2 — Embedding Generation

The query is converted into vector embeddings.

Step 3 — Semantic Retrieval

Top relevant chunks are retrieved from vector database.

Step 4 — Prompt Construction

Retrieved context + user query are passed into the LLM prompt.

Step 5 — LLM Response

The model generates a contextual medical answer based only on retrieved documents.

🔍 Why Use RAG?
Traditional LLM	RAG-Based Chatbot
Hallucinates	Context grounded
No citations	Source references
Static knowledge	Dynamic documents
Less reliable	More trustworthy
📈 Future Improvements
🔐 User Authentication
📤 Upload custom PDFs
🧠 Conversational memory
🌐 Multi-language support
🖼️ Multi-modal RAG
☁️ Cloud deployment
🧪 Unit & integration testing
🧠 Hybrid Search + Re-ranking
🤖 Agentic workflow integration
🧪 Advanced Concepts Used
Retrieval-Augmented Generation (RAG)
Semantic Search
Vector Embeddings
Chunking & Overlap
Prompt Engineering
Similarity Search
Vector Databases
LLM Orchestration
Source Traceability
Hallucination Reduction
📊 Example Architecture Diagram
                ┌────────────────────┐
                │  Medical PDFs      │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Text Chunking      │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Embedding Model    │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Vector Database    │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Semantic Retriever │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Mistral 7B LLM     │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Streamlit UI       │
                └────────────────────┘
📸 UI Preview
👤 User:
What are symptoms of diabetes?

🤖 MediBot:
Common symptoms of diabetes include increased thirst,
frequent urination, fatigue, blurred vision, and slow healing wounds.

📄 Source:
Page 142 — Gale Encyclopedia of Medicine
🤝 Contributing

Contributions are welcome!

Fork repository
Create new branch
Commit changes
Push branch
Open Pull Request
📜 License

This project is licensed under the MIT License.

👨‍💻 Author

Developed by Dhruv
AI/ML Engineer | Generative AI Enthusiast

⭐ Support

If you found this project useful:

⭐ Star the repository
🍴 Fork the project
🧠 Share with others
📌 Keywords
AI Chatbot
Medical Chatbot
LLM
RAG
LangChain
FAISS
Streamlit
Mistral 7B
Vector Database
Semantic Search
Generative AI
Hugging Face
Prompt Engineering
Healthcare AI
