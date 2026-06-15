# 🩺 MedQuery AI – Multi-User Medical Report RAG Chatbot

A production-ready AI-powered medical document assistant that enables users to upload their medical reports and receive accurate, context-aware answers grounded strictly in their own documents.

Built using a secure multi-user Retrieval-Augmented Generation (RAG) architecture, MedQuery AI combines modern AI frameworks, vector search, and authentication systems to deliver personalized and privacy-focused medical report analysis.

---

## 🚀 Features

### 🔐 Secure User Authentication

* Google OAuth authentication using NextAuth.
* Protected user sessions and secure access control.
* Personalized document and chat experience for every user.

### 📄 Medical Report Upload

* Upload medical reports in PDF format.
* Automatic document parsing and preprocessing.
* Efficient extraction of report content for AI processing.

### 🧠 Retrieval-Augmented Generation (RAG)

* Document chunking using Recursive Character Text Splitter.
* Semantic embeddings generated using HuggingFace Embeddings.
* Relevant document chunks retrieved using FAISS Vector Search.
* LLM responses grounded in uploaded report context.

### 💬 Intelligent Medical Q&A

* Ask natural language questions about uploaded reports.
* Context-aware answers generated using LLaMA 3.1 8B via Groq.
* Real-time conversational chat interface.

### 🛡️ Privacy & Security

* Separate FAISS vector database for every user.
* Complete user data isolation.
* Prevents cross-user document access and information leakage.
* Medical-domain restricted responses to reduce misuse.

### ⚡ High Performance

* Fast document retrieval using FAISS.
* Low-latency LLM inference through Groq.
* Optimized backend architecture with FastAPI.

---

## 🏗️ System Architecture

```text
User Login
     │
     ▼
Upload Medical Report (PDF)
     │
     ▼
Text Extraction & Chunking
     │
     ▼
Generate Embeddings
     │
     ▼
Store in User-Specific FAISS Vector Store
     │
     ▼
User Query
     │
     ▼
Semantic Retrieval
     │
     ▼
Relevant Context Retrieved
     │
     ▼
LLaMA 3.1 (Groq)
     │
     ▼
Grounded AI Response
```

---

## 🧩 Tech Stack

### Frontend

* Next.js (App Router)
* TypeScript
* Tailwind CSS
* NextAuth (Google OAuth)

### Backend

* FastAPI
* Python
* Uvicorn

### AI & RAG Stack

* LangChain
* Groq (LLaMA 3.1 8B)
* HuggingFace Embeddings
* FAISS Vector Database
* Recursive Character Text Splitter

---

## 🔍 How It Works

### Step 1: Authentication

Users securely log in using Google OAuth.

### Step 2: Document Upload

Medical reports are uploaded in PDF format.

### Step 3: Processing Pipeline

* Extract text from PDF
* Split text into semantic chunks
* Generate vector embeddings
* Store embeddings in a user-specific FAISS index

### Step 4: Question Answering

When a user asks a question:

1. Query is converted into embeddings.
2. Relevant document chunks are retrieved.
3. Retrieved context is passed to the LLM.
4. AI generates an answer grounded in the medical report.

---

## 🎯 Key Engineering Highlights

* Multi-user RAG architecture.
* User-specific vector database isolation.
* Secure authentication and authorization.
* End-to-end AI pipeline implementation.
* Context-aware retrieval system.
* Production-ready FastAPI backend.
* Low-latency inference with Groq.
* Scalable and modular system design.

---

## 🧠 Why RAG Instead of Generic AI?

Traditional AI chatbots rely solely on model knowledge and can generate hallucinated responses.

MedQuery AI improves reliability by:

* Answering strictly from uploaded documents.
* Retrieving relevant report sections before generation.
* Reducing hallucinations through contextual grounding.
* Maintaining user privacy with isolated vector stores.
* Providing personalized document-specific insights.

This results in more accurate, reliable, and explainable responses compared to generic AI assistants.

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/Ronak-Malik/medquery-ai.git
```

### Install Frontend Dependencies

```bash
cd frontend
npm install
```

### Install Backend Dependencies

```bash
cd backend
pip install -r requirements.txt
```

### Environment Variables

```env
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
NEXTAUTH_SECRET=

GROQ_API_KEY=

HUGGINGFACE_API_KEY=
```

### Run Frontend

```bash
npm run dev
```

### Run Backend

```bash
uvicorn main:app --reload
```

---

## 📈 Future Enhancements

* Medical report summarization.
* Multi-document support.
* Chat history persistence.
* PDF annotation and highlighting.
* Voice-based interaction.
* Advanced medical knowledge graph integration.

---


⭐ If you found this project useful, consider giving it a star on GitHub.
