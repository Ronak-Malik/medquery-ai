🩺 MedQuery AI
Multi-User Medical Report RAG Chatbot

MedQuery AI is a full-stack AI application that allows users to upload their medical report (PDF) and ask contextual questions grounded strictly in their own document.

Built using a secure multi-user RAG (Retrieval-Augmented Generation) architecture.

⚙️ Architecture =

User Login → Upload PDF → Chunk & Embed → Store in FAISS → Retrieve Relevant Context → LLM Response

🚀 Main Features =

1.🔐 Google Authentication (NextAuth)

2.📄 User-specific PDF upload

3.🧠 RAG-based contextual answering

4.🗂️ Separate FAISS vectorstore per user

5.💬 Real-time chat interface

6.🛡️ Medical-domain restricted responses

7.🚫 No cross-user data leakage

🧩 Tech Stack
Frontend

Next.js (App Router)

TypeScript

Tailwind CSS

NextAuth (Google OAuth)

Backend

FastAPI

Python

Uvicorn

AI Stack

LangChain

Groq (LLaMA 3.1 8B)

HuggingFace Embeddings

FAISS Vector Database

Recursive Character Text Splitter

🧠 Why Use This Over Generic AI Models?

Unlike general AI chatbots, MedQuery AI:

1.Answers only from your uploaded medical report

2.Uses Retrieval-Augmented Generation to reduce hallucinations

3.Isolates each user’s data securely

4.Prevents non-medical misuse

5.Provides document-grounded, context-aware responses

6.This ensures higher accuracy, privacy, and reliability compared to generic AI models.

