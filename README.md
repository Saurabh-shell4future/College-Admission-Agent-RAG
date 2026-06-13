# 🏛️ College Admission Agent (RAG-Based)

## 📌 Project Overview

This project implements an AI-powered **College Admission Agent** using a decoupled **Retrieval-Augmented Generation (RAG)** architecture.  
The system automates parsing, retrieval, and summarization of admission guidelines, eligibility metrics, and institutional databases using natural language interaction.

It transforms static data into conversational intelligence with **context-aware and zero-hallucination responses** for students.

Developed under **IBM SkillsBuild AICTE Internship 2026**, using:
- IBM Cloud Lite  
- Langflow  
- IBM watsonx.ai  
- IBM Granite Models  

---

## 🎯 Problem Statement

Build a system that can automatically answer student queries related to:

- Admission policies  
- Eligibility criteria  
- Courses available  
- Fee structure  
- Deadlines  
- FAQs  

✔ Must ensure **accurate, data-grounded responses**  
✔ Must avoid hallucination using RAG

---

## 🛠️ Technologies Used

- Langflow (Orchestration Layer)  
- IBM watsonx.ai Platform  
- IBM Granite LLMs  
- FAISS Vector Database  
- IBM watsonx Orchestrate  
- Python 3.10+  
- REST APIs  

---

## ✨ Key Features

- Natural language admission chatbot  
- Multi-turn query handling  
- Smart course eligibility mapping  
- Zero-overlap chunking (1000 size, 0 overlap)  
- Fast semantic search using FAISS  
- Enterprise cloud deployment via IBM watsonx  

---

## 🏗️ System Architecture

Raw Dataset (20,000 Records)
↓
Langflow Text Splitter (\n, overlap=0)
↓
FAISS Vector Index
↓
User Query
↓
watsonx Orchestrate API
↓
JSON Parser Block
↓
IBM Granite Model (watsonx.ai)
↓
Final Grounded Response



---

## 🔄 Workflow

1. User sends query  
2. Query converted into embeddings  
3. FAISS finds nearest data  
4. Relevant context extracted  
5. Sent to IBM Granite model  
6. Response generated and returned  

---

## 💻 Implementation

### 1. Langflow RAG Pipeline
- CSV ingestion  
- Text splitting  
- Embedding generation  
- FAISS indexing  
- JSON orchestration  

### 2. watsonx Orchestrate Agent
- Custom tool setup  
- Cloud deployment  
- API-based flow tracking  

---

## 📂 Repository Structure
