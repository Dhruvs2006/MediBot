# 🩺 MediBot – AI Powered Medical Chatbot

> An intelligent Medical AI Assistant built using **Retrieval-Augmented Generation (RAG)**, **LangChain**, **FAISS**, **Hugging Face Embeddings**, and **Groq LLMs** to provide context-aware and reliable medical information from trusted medical documents.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red?style=for-the-badge&logo=streamlit)
![LangChain](https://img.shields.io/badge/LangChain-RAG-green?style=for-the-badge)
![FAISS](https://img.shields.io/badge/VectorDB-FAISS-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

---

# 📖 Overview

MediBot is an AI-powered medical chatbot that answers healthcare-related questions using **Retrieval-Augmented Generation (RAG)**.

Instead of relying only on an LLM, MediBot first searches a medical knowledge base built from trusted PDF documents, retrieves the most relevant information using semantic search, and then generates an answer grounded in those documents.

This significantly reduces hallucinations and improves answer reliability.

---

# ✨ Features

- 🩺 AI-powered Medical Question Answering
- 📚 Medical PDF Knowledge Base
- 🔍 Semantic Search using Vector Embeddings
- 🧠 Retrieval-Augmented Generation (RAG)
- ⚡ Fast FAISS Vector Database
- 🤖 Supports Groq Llama 3.3-70B
- 🤗 Supports HuggingFace Inference API
- 💬 Interactive Streamlit Chat Interface
- 📄 Displays Source Documents
- 🔒 Secure API Key Management using `.env`

---

# 🏗️ Project Architecture

```
Medical PDF
      │
      ▼
Text Extraction
      │
      ▼
Text Chunking
      │
      ▼
Sentence Embeddings
      │
      ▼
FAISS Vector Store
      │
      ▼
Similarity Search
      │
      ▼
Relevant Context
      │
      ▼
Groq / HuggingFace LLM
      │
      ▼
Medical Answer
      │
      ▼
Streamlit Interface
```

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Core Programming Language |
| Streamlit | User Interface |
| LangChain | LLM Orchestration |
| FAISS | Vector Database |
| HuggingFace Embeddings | Semantic Embeddings |
| Groq API | High-speed LLM Inference |
| HuggingFace Endpoint | Alternative LLM Backend |
| PyPDF | PDF Processing |
| dotenv | Environment Variables |

---

# 📂 Project Structure

```
MediBot/
│
├── data/
│   └── The_GALE_ENCYCLOPEDIA_of_MEDICINE_SECOND.pdf
│
├── vectorstore/
│   └── db_faiss/
│       ├── index.faiss
│       └── index.pkl
│
├── medibot.py
├── create_memory_for_llm.py
├── connect_memory_with_llm.py
├── requirements.txt
├── Pipfile
├── Pipfile.lock
└── README.md
```

---

# 🚀 Installation

## 1. Clone Repository

```bash
git clone https://github.com/Dhruvs2006/MediBot.git

cd MediBot
```

---

## 2. Create Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔑 Environment Variables

Create a `.env` file in the project root.

For Groq:

```env
GROQ_API_KEY=your_groq_api_key
```

Or for HuggingFace:

```env
HF_TOKEN=your_huggingface_api_key
```

If both are provided, MediBot automatically uses **Groq**.

---

# ▶️ Run the Application

```bash
streamlit run medibot.py
```

The application will launch in your browser.

---

# 💬 Sample Questions

- What are the symptoms of diabetes?
- Explain hypertension.
- What causes asthma?
- What is pneumonia?
- How is malaria treated?
- What are the side effects of antibiotics?

---

# 🧠 How MediBot Works

### Step 1

User asks a medical question.

↓

### Step 2

The question is converted into embeddings.

↓

### Step 3

FAISS retrieves the most relevant document chunks.

↓

### Step 4

The retrieved context is combined with the user query.

↓

### Step 5

Groq / HuggingFace LLM generates a response based only on retrieved information.

↓

### Step 6

The chatbot displays both the answer and source documents.

---

# 📈 Why RAG?

| Traditional LLM | MediBot (RAG) |
|-----------------|---------------|
| May Hallucinate | Context Grounded |
| No Knowledge Source | Uses Medical PDFs |
| Generic Answers | Domain-Specific Responses |
| Less Reliable | More Trustworthy |

---

# 🔮 Future Improvements

- 🔐 User Authentication
- 📤 Upload Custom Medical PDFs
- 🌍 Multi-language Support
- 🧠 Conversational Memory
- ☁️ Cloud Deployment
- 📱 Mobile Responsive UI
- 🖼️ Medical Image Support
- 🔎 Hybrid Search
- 🤖 AI Agent Integration

---

# 📸 Screenshots

Add screenshots here.

```
screenshots/
├── home.png
├── chatbot.png
└── response.png
```

Example:

```markdown
![Home](screenshots/home.png)

![Chat](screenshots/chatbot.png)
```

---

# 📚 Concepts Used

- Retrieval-Augmented Generation (RAG)
- Semantic Search
- Vector Embeddings
- Similarity Search
- FAISS Vector Database
- LangChain
- Prompt Engineering
- Large Language Models
- Streamlit
- Medical Knowledge Retrieval

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository

2. Create a feature branch

```bash
git checkout -b feature-name
```

3. Commit your changes

```bash
git commit -m "Added new feature"
```

4. Push

```bash
git push origin feature-name
```

5. Open a Pull Request

---

# 📄 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Dhruv**

GitHub: **https://github.com/Dhruvs2006**

---

# ⭐ Support

If you found this project helpful, please consider giving it a ⭐ on GitHub.

It helps others discover the project and motivates future improvements.

---

## ❤️ Thank You

Thank you for checking out **MediBot**.

Happy Coding! 🚀
